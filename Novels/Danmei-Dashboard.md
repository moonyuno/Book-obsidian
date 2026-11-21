---
cssclasses:
  - danmei-dashboard
exclude: true
banner: https://i.imgur.com/dHT0AOf.png
sort_novels: Volumes
filter_author: ""
filter_year: All
---



```dataviewjs
// grab a random quote from the Quotes note and display it at the top
// idk why sometimes quotePage comes back undefined even when the note exists but ok
const quotePage = dv.page("Quotes");
let quotes = [];
if (quotePage && quotePage.file && quotePage.file.path) {
    const content = await dv.io.load(quotePage.file.path);
    if (content) {
        quotes = content.split("\n").map(l => l.trim())
            .filter(l => l.startsWith('"') || l.startsWith('\u201c'));
    }
}
if (quotes.length === 0) {
  const f = dv.container.createEl("div", { cls: "dg-footer" });
  f.createEl("span", { text: "✦ " });
  f.createEl("em", { text: "Add quotes to your Quotes note to see them here." });
  f.createEl("span", { text: " ✦" });
} else {
  const pick = quotes[Math.floor(Math.random() * quotes.length)];
  const m = pick.match(/(.+?)\s*[\u2014—-]\s*([^\u2014—-]+)$/);
  const f = dv.container.createEl("div", { cls: "dg-footer" });
  if (m) {
    f.createEl("span", { text: "✦ " });
    f.createEl("em", { text: m[1].trim() });
    f.createEl("span", { text: " ✦" });
    f.createEl("div", { text: "— " + m[2].trim(), cls: "dq-attr" });
  } else {
    f.createEl("span", { text: "✦ " });
    f.createEl("em", { text: pick });
    f.createEl("span", { text: " ✦" });
  }
}
```

---

```dataviewjs
// stats block — counts all danmei novels by status and computes avg rating
const folder = "Novels";
const pages  = dv.pages(`"${folder}"`);
const total    = pages.length;
const reading  = pages.where(p => p.status === "Reading").length;
const finished = pages.where(p => p.status === "Finished").length;
const unread   = pages.where(p => p.status === "Unread" || !p.status).length;
const dropped  = pages.where(p => p.status === "Dropped").length;
const onhold   = pages.where(p => p.status === "On Hold").length;

// rating can come in as stars, as "4/5", or just a number — handle all three
function getRating(r) {
  if (!r) return 0;
  const s = String(r);
  const stars = (s.match(/⭐/g) || []).length;
  if (stars > 0) return stars;
  const slash = s.match(/(\d+)\s*\/\s*(\d+)/);
  if (slash) return Number(slash[1]);
  const num = Number(s);
  return isNaN(num) ? 0 : num;
}

const rated = pages.where(p => getRating(p.rating) > 0);
const avg = rated.length > 0
  ? (rated.map(p => getRating(p.rating)).array().reduce((a,b)=>a+b,0) / rated.length).toFixed(1)
  : "–";
const avgStars = avg !== "–" ? "⭐".repeat(Math.round(Number(avg))) + " " + avg : "–";

dv.container.createEl("div", { cls: "dash-stats" }).innerHTML = `
  <div class="stat-card"><span class="stat-num">${total}</span><span class="stat-label">Total</span></div>
  <div class="stat-card accent"><span class="stat-num">${reading}</span><span class="stat-label">Reading</span></div>
  <div class="stat-card"><span class="stat-num">${onhold}</span><span class="stat-label">On Hold</span></div>
  <div class="stat-card"><span class="stat-num">${finished}</span><span class="stat-label">Finished</span></div>
  <div class="stat-card"><span class="stat-num">${unread}</span><span class="stat-label">Unread</span></div>
  <div class="stat-card"><span class="stat-num">${dropped}</span><span class="stat-label">Dropped</span></div>
  <div class="stat-card"><span class="stat-num">${avgStars}</span><span class="stat-label">Avg Rating</span></div>
`;
```

---

**Sort by:** `INPUT[inlineSelect(option(Title), option(Author), option(Rating), option(Date Added), option(Progress), option(Volumes)):sort_novels]` &nbsp;&nbsp; **Author:** `INPUT[text(placeholder(author...)):filter_author]` &nbsp;&nbsp; **Year:** `INPUT[inlineSelect(option(All), option(2021), option(2022), option(2023), option(2024), option(2025), option(2026)):filter_year]`

---

## 🔥 Currently Reading

```dataviewjs
const folder = "Novels";
const cur = dv.current();
const sortBy = cur.sort_novels || "Title";
const filterAuthor = (cur.filter_author || "").toLowerCase().trim();
const filterYear = cur.filter_year || "All";

// strips out Templater leftover {{ }} junk from string fields
const stripTemplaterJunk = s => s ? String(s).replace(/\{\{|\}\}/g, "").trim() : "";

// parse volumes_read/volumes_total — they can be two separate fields or a single "x/y" string
// this took me forever to figure out lol
function getProgress(p) {
  if (p.volumes_read != null && p.volumes_total != null)
    return { readVols: Number(p.volumes_read), totalVols: Number(p.volumes_total) };
  if (!p.Volumes) return null;
  const m = String(p.Volumes).match(/(\d+)\s*\/\s*(\d+)/);
  return m ? { readVols: Number(m[1]), totalVols: Number(m[2]) } : null;
}

function renderNovel(p, grid) {
  const card = grid.createEl("div", { cls: "dvjs-card" });

  // cover — make it a link so you can click through to the note
  const cw = card.createEl("div", { cls: "dvjs-cover-wrap" });
  const cl = cw.createEl("a", { cls: "internal-link dvjs-cover-link", attr: { href: p.file.name } });
  if (p.cover) cl.createEl("img", { attr: { src: String(p.cover) }, cls: "dvjs-cover" });

  // EN license badge — color comes from statuspub
  const enNum = parseInt(p.en_published) || 0;
  let spub = String(p.statuspub || "").toLowerCase().trim();
  if (spub && spub !== "not licensed" && spub !== "not_licensed") {
    card.createEl("div", {
      cls: "dvjs-en-badge " + spub,
      text: enNum > 0 ? String(enNum) : "—"
    });
  }

  const info = card.createEl("div", { cls: "dvjs-info" });
  const novelTitle = stripTemplaterJunk(p.title) || p.file.name;
  info.createEl("a", { text: novelTitle, cls: "dvjs-title internal-link", attr: { href: p.file.name } });

  if (p.author) {
    const f = info.createEl("div", { cls: "dvjs-field" });
    f.createEl("div", { text: "AUTHOR", cls: "dvjs-label" });
    f.createEl("div", { text: stripTemplaterJunk(p.author), cls: "dvjs-value" });
  }
  if (p.status) {
    const f = info.createEl("div", { cls: "dvjs-field" });
    f.createEl("div", { text: "STATUS", cls: "dvjs-label" });
    f.createEl("div", { text: stripTemplaterJunk(p.status), cls: "dvjs-value" });
  }

  const vol = getProgress(p);
  if (vol) {
    const pct = vol.totalVols > 0 ? Math.round((vol.readVols / vol.totalVols) * 100) : 0;
    const fv = info.createEl("div", { cls: "dvjs-field" });
    fv.createEl("div", { text: "VOLUMES", cls: "dvjs-label" });
    fv.createEl("div", { text: `${vol.readVols}/${vol.totalVols} · ${pct}%`, cls: "dvjs-value" });
    const bw = info.createEl("div", { cls: "dvjs-progress-wrap" });
    bw.createEl("div", { cls: "dvjs-progress-bar", attr: { style: `width:${pct}%` } });
  }
  if (p.rating) {
    const f = info.createEl("div", { cls: "dvjs-field" });
    f.createEl("div", { text: "RATING", cls: "dvjs-label" });
    f.createEl("div", { text: String(p.rating), cls: "dvjs-value" });
  }
}

function calcProgressRatio(p) {
  const v = getProgress(p);
  return v && v.totalVols > 0 ? v.readVols / v.totalVols : 0;
}

let pages = dv.pages(`"${folder}"`).where(p => p.status === "Reading");
if (filterAuthor) pages = pages.where(p => (p.author || "").toLowerCase().includes(filterAuthor));
if (filterYear !== "All") pages = pages.where(p => String(p.published) === String(filterYear));

if (sortBy === "Title")           pages = pages.sort(p => stripTemplaterJunk(p.title) || p.file.name);
else if (sortBy === "Author")     pages = pages.sort(p => stripTemplaterJunk(p.author));
else if (sortBy === "Rating")     pages = pages.sort(p => -(parseFloat(String(p.rating || "").replace(/[^0-9.]/g,"")) || 0));
else if (sortBy === "Date Added") pages = pages.sort(p => p.file.ctime, "desc");
else if (sortBy === "Progress")   pages = pages.sort(p => -calcProgressRatio(p));
else if (sortBy === "Volumes")    pages = pages.sort(p => -(p.volumes_total != null ? Number(p.volumes_total) : 0));

if (!pages.length) { dv.paragraph(""); }
else {
  const grid = dv.container.createEl("div", { cls: "dvjs-grid" });
  for (const p of pages) renderNovel(p, grid);
}
```

---

## 🟠 On Hold

```dataviewjs
const folder = 'Novels';
const cur = dv.current();
const sortBy = cur.sort_novels || 'Title';
const filterAuthor = (cur.filter_author || '').toLowerCase().trim();
const filterYear = cur.filter_year || 'All';

const stripTemplaterJunk = s => s ? String(s).replace(/\{\{|\}\}/g, '').trim() : '';

// same volume parsing as the reading section — copy-pasted because why not
const parseVolumes = function(p) {
    if (p.volumes_read != null && p.volumes_total != null)
        return { readVols: Number(p.volumes_read), totalVols: Number(p.volumes_total) };
    if (!p.Volumes) return null;
    const m = String(p.Volumes).match(/(\d+)\s*\/\s*(\d+)/);
    return m ? { readVols: Number(m[1]), totalVols: Number(m[2]) } : null;
};

// on-hold cards are the same layout, I just wanted a different function name here
function makeCard(p, grid) {
    const card = grid.createEl('div', { cls: 'dvjs-card' });
    const cw = card.createEl('div', { cls: 'dvjs-cover-wrap' });
    const cl = cw.createEl('a', { cls: 'internal-link dvjs-cover-link', attr: { href: p.file.name } });
    if (p.cover) cl.createEl('img', { attr: { src: String(p.cover) }, cls: 'dvjs-cover' });

    // EN license badge — color based on statuspub property
    const enNum = parseInt(p.en_published) || 0;
    const spub = String(p.statuspub || '').toLowerCase().trim();
    if (spub && spub !== 'not licensed' && spub !== 'not_licensed') {
        card.createEl('div', {
            cls: 'dvjs-en-badge ' + spub,
            text: enNum > 0 ? String(enNum) : '—'
        });
    }

    const info = card.createEl('div', { cls: 'dvjs-info' });
    info.createEl('a', { text: stripTemplaterJunk(p.title) || p.file.name, cls: 'dvjs-title internal-link', attr: { href: p.file.name } });

    if (p.author) {
        const f = info.createEl('div', { cls: 'dvjs-field' });
        f.createEl('div', { text: 'AUTHOR', cls: 'dvjs-label' });
        f.createEl('div', { text: stripTemplaterJunk(p.author), cls: 'dvjs-value' });
    }
    if (p.status) {
        const f = info.createEl('div', { cls: 'dvjs-field' });
        f.createEl('div', { text: 'STATUS', cls: 'dvjs-label' });
        f.createEl('div', { text: stripTemplaterJunk(p.status), cls: 'dvjs-value' });
    }

    const vol = parseVolumes(p);
    if (vol) {
        const pct = vol.totalVols > 0 ? Math.round((vol.readVols / vol.totalVols) * 100) : 0;
        const f = info.createEl('div', { cls: 'dvjs-field' });
        f.createEl('div', { text: 'VOLUMES', cls: 'dvjs-label' });
        f.createEl('div', { text: `${vol.readVols}/${vol.totalVols} · ${pct}%`, cls: 'dvjs-value' });
        const bw = info.createEl('div', { cls: 'dvjs-progress-wrap' });
        bw.createEl('div', { cls: 'dvjs-progress-bar', attr: { style: `width:${pct}%` } });
    }
    if (p.rating) {
        const f = info.createEl('div', { cls: 'dvjs-field' });
        f.createEl('div', { text: 'RATING', cls: 'dvjs-label' });
        f.createEl('div', { text: String(p.rating), cls: 'dvjs-value' });
    }
}

// filter then sort — using .array() + .filter() here because I kept getting weird dv errors with chained .where()
let allOnHold = dv.pages(`"${folder}"`).array().filter(p => p.status === 'On Hold');
if (filterAuthor) allOnHold = allOnHold.filter(p => (p.author || '').toLowerCase().includes(filterAuthor));
if (filterYear !== 'All') allOnHold = allOnHold.filter(p => String(p.published) === String(filterYear));

// sort by rating but unrated go to bottom
if (sortBy === 'Title')           allOnHold.sort((a,b) => (stripTemplaterJunk(a.title)||a.file.name).localeCompare(stripTemplaterJunk(b.title)||b.file.name));
else if (sortBy === 'Author')     allOnHold.sort((a,b) => stripTemplaterJunk(a.author).localeCompare(stripTemplaterJunk(b.author)));
else if (sortBy === 'Rating')     allOnHold.sort((a,b) => (parseFloat(String(b.rating||'').replace(/[^0-9.]/g,''))||0) - (parseFloat(String(a.rating||'').replace(/[^0-9.]/g,''))||0));
else if (sortBy === 'Date Added') allOnHold.sort((a,b) => b.file.ctime - a.file.ctime);
else if (sortBy === 'Volumes')    allOnHold.sort((a,b) => (b.volumes_total != null ? Number(b.volumes_total) : 0) - (a.volumes_total != null ? Number(a.volumes_total) : 0));

if (!allOnHold.length) { dv.paragraph(''); }
else {
    const grid = dv.container.createEl('div', { cls: 'dvjs-grid' });
    for (const p of allOnHold) makeCard(p, grid);
}
```

---

## 📚 Unread

```dataviewjs
const folder = "Novels";
const cur = dv.current();
const sortBy = cur.sort_novels || "Title";
const filterAuthor = (cur.filter_author || "").toLowerCase().trim();
const filterYear = cur.filter_year || "All";
const stripTemplaterJunk = s => s ? String(s).replace(/\{\{|\}\}/g, "").trim() : "";

// unread cards don't need a progress bar since nothing's been read yet
// TODO: maybe add pairing here later
function renderNovel(p, grid) {
  const card = grid.createEl("div", { cls: "dvjs-card" });
  const cw = card.createEl("div", { cls: "dvjs-cover-wrap" });
  const cl = cw.createEl("a", { cls: "internal-link dvjs-cover-link", attr: { href: p.file.name } });
  if (p.cover) cl.createEl("img", { attr: { src: String(p.cover) }, cls: "dvjs-cover" });

  const enNum = parseInt(p.en_published) || 0;
  const spub = String(p.statuspub || "").toLowerCase().trim();
  if (spub && spub !== "not licensed" && spub !== "not_licensed") {
    card.createEl("div", {
      cls: "dvjs-en-badge " + spub,
      text: enNum > 0 ? String(enNum) : "—"
    });
  }

  const info = card.createEl("div", { cls: "dvjs-info" });
  info.createEl("a", { text: stripTemplaterJunk(p.title) || p.file.name, cls: "dvjs-title internal-link", attr: { href: p.file.name } });

  if (p.author) {
    const f = info.createEl("div", { cls: "dvjs-field" });
    f.createEl("div", { text: "AUTHOR", cls: "dvjs-label" });
    f.createEl("div", { text: stripTemplaterJunk(p.author), cls: "dvjs-value" });
  }
  if (p.status) {
    const f = info.createEl("div", { cls: "dvjs-field" });
    f.createEl("div", { text: "STATUS", cls: "dvjs-label" });
    f.createEl("div", { text: stripTemplaterJunk(p.status), cls: "dvjs-value" });
  }

  // idk why dataview sometimes reads volumes_total as a string but ok
  const volDisplay = p.volumes_total != null
    ? (String(p.volumes_read ?? 0) + "/" + String(p.volumes_total))
    : (p.Volumes ? String(p.Volumes) : null);
  if (volDisplay) {
    const f = info.createEl("div", { cls: "dvjs-field" });
    f.createEl("div", { text: "VOLUMES", cls: "dvjs-label" });
    f.createEl("div", { text: volDisplay, cls: "dvjs-value" });
  }
}

let pages = dv.pages(`"${folder}"`).where(p => p.status === "Unread" || !p.status);
if (filterAuthor) pages = pages.where(p => (p.author || "").toLowerCase().includes(filterAuthor));
if (filterYear !== "All") pages = pages.where(p => String(p.published) === String(filterYear));
if (sortBy === "Title")       pages = pages.sort(p => stripTemplaterJunk(p.title) || p.file.name);
else if (sortBy === "Author") pages = pages.sort(p => stripTemplaterJunk(p.author));
else if (sortBy === "Date Added") pages = pages.sort(p => p.file.ctime, "desc");
else if (sortBy === "Volumes") pages = pages.sort(p => -(p.volumes_total != null ? Number(p.volumes_total) : 0));

if (!pages.length) { dv.paragraph(""); }
else {
  const grid = dv.container.createEl("div", { cls: "dvjs-grid" });
  for (const p of pages) renderNovel(p, grid);
}
```

---

## ✅ Finished

```dataviewjs
// finished novels — sorted by rating by default since this is basically my rec list
const folder = "Novels";
let cur = dv.current();
let sortBy = cur.sort_novels || "Rating";
let filterAuthor = (cur.filter_author || "").toLowerCase().trim();
let filterYear = cur.filter_year || "All";

const stripTemplaterJunk = s => s ? String(s).replace(/\{\{|\}\}/g, "").trim() : "";

// inline the card rendering this time, no separate function needed
let pages = dv.pages(`"${folder}"`).where(p => p.status === "Finished");
if (filterAuthor) pages = pages.where(p => (p.author || "").toLowerCase().includes(filterAuthor));
if (filterYear !== "All") pages = pages.where(p => String(p.published) === String(filterYear));

// sort by rating but unrated go to bottom
if (sortBy === "Title")           pages = pages.sort(p => stripTemplaterJunk(p.title) || p.file.name);
else if (sortBy === "Author")     pages = pages.sort(p => stripTemplaterJunk(p.author));
else if (sortBy === "Rating")     pages = pages.sort(p => -(parseFloat(String(p.rating || "").replace(/[^0-9.]/g,"")) || 0));
else if (sortBy === "Date Added") pages = pages.sort(p => p.file.ctime, "desc");
else if (sortBy === "Volumes")    pages = pages.sort(p => -(p.volumes_total != null ? Number(p.volumes_total) : 0));

if (!pages.length) {
  dv.paragraph("");
} else {
  const grid = dv.container.createEl("div", { cls: "dvjs-grid" });

  for (const p of pages) {
    const card = grid.createEl("div", { cls: "dvjs-card" });

    const cw = card.createEl("div", { cls: "dvjs-cover-wrap" });
    const cl = cw.createEl("a", { cls: "internal-link dvjs-cover-link", attr: { href: p.file.name } });
    if (p.cover) cl.createEl("img", { attr: { src: String(p.cover) }, cls: "dvjs-cover" });

    // EN volumes published badge
    const enNum = parseInt(p.en_published) || 0;
    const spub = String(p.statuspub || "").toLowerCase().trim();
    if (spub && spub !== "not licensed" && spub !== "not_licensed") {
      card.createEl("div", {
        cls: "dvjs-en-badge " + spub,
        text: enNum > 0 ? String(enNum) : "—"
      });
    }

    const info = card.createEl("div", { cls: "dvjs-info" });
    const novelTitle = stripTemplaterJunk(p.title) || p.file.name;
    info.createEl("a", { text: novelTitle, cls: "dvjs-title internal-link", attr: { href: p.file.name } });

    if (p.author) {
      const fa = info.createEl("div", { cls: "dvjs-field" });
      fa.createEl("div", { text: "AUTHOR", cls: "dvjs-label" });
      fa.createEl("div", { text: stripTemplaterJunk(p.author), cls: "dvjs-value" });
    }
    if (p.status) {
      const fs = info.createEl("div", { cls: "dvjs-field" });
      fs.createEl("div", { text: "STATUS", cls: "dvjs-label" });
      fs.createEl("div", { text: stripTemplaterJunk(p.status), cls: "dvjs-value" });
    }

    const volDisplay = p.volumes_total != null
      ? (String(p.volumes_read ?? 0) + "/" + String(p.volumes_total))
      : (p.Volumes ? String(p.Volumes) : null);
    if (volDisplay) {
      const fv = info.createEl("div", { cls: "dvjs-field" });
      fv.createEl("div", { text: "VOLUMES", cls: "dvjs-label" });
      fv.createEl("div", { text: volDisplay, cls: "dvjs-value" });
    }
    if (p.rating) {
      const fr = info.createEl("div", { cls: "dvjs-field" });
      fr.createEl("div", { text: "RATING", cls: "dvjs-label" });
      fr.createEl("div", { text: String(p.rating), cls: "dvjs-value" });
    }
  }
}
```

---

## 🚫 Dropped

```dataviewjs
const folder = 'Novels';
const cur = dv.current();
const sortBy = cur.sort_novels || 'Title';
const filterAuthor = (cur.filter_author || '').toLowerCase().trim();
const filterYear = cur.filter_year || 'All';
const stripTemplaterJunk = s => s ? String(s).replace(/\{\{|\}\}/g, '').trim() : '';

// using parseInt here for the en badge count — same as everywhere else
function makeCard(p, grid) {
  let card = grid.createEl('div', { cls: 'dvjs-card' });
  const cw = card.createEl('div', { cls: 'dvjs-cover-wrap' });
  const cl = cw.createEl('a', { cls: 'internal-link dvjs-cover-link', attr: { href: p.file.name } });
  if (p.cover) cl.createEl('img', { attr: { src: String(p.cover) }, cls: 'dvjs-cover' });

  // EN license badge — color based on statuspub property
  const enNum = parseInt(p.en_published) || 0;
  const spub = String(p.statuspub || '').toLowerCase().trim();
  if (spub && spub !== 'not licensed' && spub !== 'not_licensed') {
    card.createEl('div', {
      cls: 'dvjs-en-badge ' + spub,
      text: enNum > 0 ? String(enNum) : '—'
    });
  }

  const info = card.createEl('div', { cls: 'dvjs-info' });
  info.createEl('a', { text: stripTemplaterJunk(p.title) || p.file.name, cls: 'dvjs-title internal-link', attr: { href: p.file.name } });

  if (p.author) {
    const f = info.createEl('div', { cls: 'dvjs-field' });
    f.createEl('div', { text: 'AUTHOR', cls: 'dvjs-label' });
    f.createEl('div', { text: stripTemplaterJunk(p.author), cls: 'dvjs-value' });
  }
  if (p.status) {
    const f = info.createEl('div', { cls: 'dvjs-field' });
    f.createEl('div', { text: 'STATUS', cls: 'dvjs-label' });
    f.createEl('div', { text: stripTemplaterJunk(p.status), cls: 'dvjs-value' });
  }

  // volume display — no progress bar for dropped novels, just the count
  const volDisplay = p.volumes_total != null
    ? (String(p.volumes_read ?? 0) + '/' + String(p.volumes_total))
    : (p.Volumes || null);
  if (volDisplay) {
    const f = info.createEl('div', { cls: 'dvjs-field' });
    f.createEl('div', { text: 'VOLUMES', cls: 'dvjs-label' });
    f.createEl('div', { text: String(volDisplay), cls: 'dvjs-value' });
  }
}

// filter using .array() here — chaining .where() on dropped was giving me trouble once
let droppedList = dv.pages(`"${folder}"`).array().filter(p => p.status === 'Dropped');
if (filterAuthor) droppedList = droppedList.filter(p => (p.author || '').toLowerCase().includes(filterAuthor));
if (filterYear !== 'All') droppedList = droppedList.filter(p => String(p.published) === String(filterYear));

if (sortBy === 'Title')           droppedList.sort((a,b) => (stripTemplaterJunk(a.title)||a.file.name).localeCompare(stripTemplaterJunk(b.title)||b.file.name));
else if (sortBy === 'Author')     droppedList.sort((a,b) => stripTemplaterJunk(a.author).localeCompare(stripTemplaterJunk(b.author)));
else if (sortBy === 'Date Added') droppedList.sort((a,b) => b.file.ctime - a.file.ctime);
else if (sortBy === 'Volumes')    droppedList.sort((a,b) => (b.volumes_total != null ? Number(b.volumes_total) : 0) - (a.volumes_total != null ? Number(a.volumes_total) : 0));

if (!droppedList.length) { dv.paragraph(''); }
else {
  const grid = dv.container.createEl('div', { cls: 'dvjs-grid' });
  for (const p of droppedList) makeCard(p, grid);
}
```

---

## 🎲 Random Pick

```dataviewjs
// picks a random unread danmei novel — just reload to get a different one
const folder = "Novels";
const stripTemplaterJunk = s => s ? String(s).replace(/\{\{|\}\}/g, "").trim() : "";

const unread = dv.pages(`"${folder}"`).array().filter(p => p.status === "Unread" || !p.status);

if (!unread.length) { dv.paragraph(""); }
else {
  const p = unread[Math.floor(Math.random() * unread.length)];
  const grid = dv.container.createEl("div", { cls: "dvjs-grid" });
  const card = grid.createEl("div", { cls: "dvjs-card" });

  const cw = card.createEl("div", { cls: "dvjs-cover-wrap" });
  const cl = cw.createEl("a", { cls: "internal-link dvjs-cover-link", attr: { href: p.file.name } });
  if (p.cover) cl.createEl("img", { attr: { src: String(p.cover) }, cls: "dvjs-cover" });

  // EN license badge — color based on statuspub property
  const enNum = parseInt(p.en_published) || 0;
  const spub = String(p.statuspub || "").toLowerCase().trim();
  if (spub && spub !== "not licensed" && spub !== "not_licensed") {
    card.createEl("div", {
      cls: "dvjs-en-badge " + spub,
      text: enNum > 0 ? String(enNum) : "—"
    });
  }

  const info = card.createEl("div", { cls: "dvjs-info" });
  info.createEl("a", { text: stripTemplaterJunk(p.title) || p.file.name, cls: "dvjs-title internal-link", attr: { href: p.file.name } });

  if (p.author) {
    const f = info.createEl("div", { cls: "dvjs-field" });
    f.createEl("div", { text: "AUTHOR", cls: "dvjs-label" });
    f.createEl("div", { text: stripTemplaterJunk(p.author), cls: "dvjs-value" });
  }
  if (p.Volumes) {
    const f = info.createEl("div", { cls: "dvjs-field" });
    f.createEl("div", { text: "VOLUMES", cls: "dvjs-label" });
    f.createEl("div", { text: String(p.Volumes), cls: "dvjs-value" });
  }
  info.createEl("div", { text: "↺ Reload for a new pick", cls: "dvjs-label", attr: { style: "margin-top:6px" } });
}
```
