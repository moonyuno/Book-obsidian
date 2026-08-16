
```dataviewjs
const folder = "Novels";
const all = dv.pages('"' + folder + '"').array();
// Charts use only novels you've engaged with (not unread)
const active = all.filter(p => ["Finished","Reading","On Hold"].includes(p.status));

// ── Helpers ──────────────────────────────────────────────
function parseList(val) {
  if (!val) return [];
  if (Array.isArray(val)) return val.map(v => String(v).trim()).filter(Boolean);
  return String(val).split(",").map(v => v.trim()).filter(Boolean);
}

function parseRating(r) {
  if (!r) return 0;
  const s = String(r);
  const stars = (s.match(/⭐/g) || []).length;
  if (stars > 0) return stars;
  const n = Number(s.replace(/[^0-9.]/g, ""));
  return isNaN(n) ? 0 : (n > 5 ? Math.round(n / 2) : n);
}

function parseDate(d) {
  if (!d) return null;
  const p = new Date(String(d));
  return isNaN(p.getTime()) ? null : p;
}

function makeBar(parent, pct, color, width) {
  width = width || 160;
  const wrap = parent.createEl("div", { cls: "st-bar-wrap" });
  wrap.style.width = width + "px";
  const fill = wrap.createEl("div", { cls: "st-bar-fill" });
  fill.style.width = Math.round(pct / 100 * width) + "px";
  fill.style.background = color;
}

function makeRow(parent, label, pct, color, value, labelWidth) {
  const row = parent.createEl("div", { cls: "st-row" });
  const lbl = row.createEl("span", { cls: "st-row-lbl", text: label });
  if (labelWidth) lbl.style.minWidth = labelWidth;
  makeBar(row, pct, color, 180);
  row.createEl("span", { cls: "st-row-val", text: String(value) });
}

function sectionTitle(parent, text) {
  parent.createEl("div", { cls: "st-section-title", text: text });
}

// ── Stats ─────────────────────────────────────────────────
const finished = all.filter(p => p.status === "Finished");
const reading  = all.filter(p => p.status === "Reading");
const onhold   = all.filter(p => p.status === "On Hold");
const unread   = all.filter(p => p.status === "Unread" || !p.status);
const dropped  = all.filter(p => p.status === "Dropped");
const rated    = all.filter(p => parseRating(p.rating) > 0);
const avgRating = rated.length > 0
  ? (rated.reduce((a, p) => a + parseRating(p.rating), 0) / rated.length).toFixed(2)
  : "—";
const totalVolsRead  = all.reduce((a, p) => a + (Number(p.volumes_read)  || 0), 0);
const totalVolsTotal = all.reduce((a, p) => a + (Number(p.volumes_total) || 0), 0);
const totalPages     = all.reduce((a, p) => a + (Number(p.pages) || 0), 0);
const readPct = totalVolsTotal > 0 ? Math.round(totalVolsRead / totalVolsTotal * 100) : 0;

// ── Reading speed ──────────────────────────────────────────
const readTimes = finished.map(p => {
  const s = parseDate(p.started), f = parseDate(p.finished);
  if (!s || !f) return null;
  const days = Math.round((f - s) / 86400000);
  return days > 0 ? { title: String(p.title || p.file.name).replace(/\{\{|\}\}/g, "").trim(), days } : null;
}).filter(Boolean);
const avgDays = readTimes.length > 0 ? Math.round(readTimes.reduce((a, x) => a + x.days, 0) / readTimes.length) : null;
const fastest = readTimes.length > 0 ? readTimes.reduce((a, x) => x.days < a.days ? x : a) : null;
const slowest = readTimes.length > 0 ? readTimes.reduce((a, x) => x.days > a.days ? x : a) : null;

// ── Books per month ────────────────────────────────────────
const thisYear = new Date().getFullYear();
const MONTHS = ["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];
const bpm = Array(12).fill(0);
finished.forEach(p => {
  const d = parseDate(p.finished);
  if (d && d.getFullYear() === thisYear) bpm[d.getMonth()]++;
});

// ── Moods ──────────────────────────────────────────────────
const MOOD_COLORS = {
  adventurous: "#4ade80", emotional: "#ec4899", dark: "#6b7280",
  funny: "#f43f5e", mysterious: "#f97316", tense: "#a855f7",
  lighthearted: "#f9a8d4", sad: "#3b82f6", hopeful: "#eab308",
  inspiring: "#14b8a6", reflective: "#6366f1"
};
const moodMap = {};
active.forEach(p => {
  parseList(p.mood).forEach(m => { const k = m.toLowerCase(); if (k) moodMap[k] = (moodMap[k] || 0) + 1; });
});
const moodEntries = Object.entries(moodMap).sort((a, b) => b[1] - a[1]);
const moodTotal = moodEntries.reduce((a, [, v]) => a + v, 0);

// ── RENDER ─────────────────────────────────────────────────
const root = dv.container.createEl("div");

// Overview cards
const cards = root.createEl("div", { cls: "st-cards" });
function makeCard(parent, num, label, cls) {
  const c = parent.createEl("div", { cls: "st-card" + (cls ? " " + cls : "") });
  c.createEl("span", { cls: "st-big", text: String(num) });
  c.createEl("span", { cls: "st-lbl", text: label });
}
makeCard(cards, all.length, "Total Novels");
makeCard(cards, finished.length, "Finished", "green");
makeCard(cards, reading.length + onhold.length, "In Progress", "gold");
makeCard(cards, unread.length, "Unread");
makeCard(cards, dropped.length, "Dropped");
makeCard(cards, avgRating, "Avg Rating");
makeCard(cards, totalVolsRead + "/" + totalVolsTotal, "Volumes Read");
if (totalPages > 0) makeCard(cards, totalPages.toLocaleString(), "Total Pages");

// Overall progress bar
const barWrap = root.createEl("div", { cls: "st-overall-bar" });
const barFill = barWrap.createEl("div", { cls: "st-overall-fill" });
barFill.style.width = readPct + "%";

// Books per month
sectionTitle(root, "📅 Books Finished Per Month (" + thisYear + ")");
const monthChart = root.createEl("div", { cls: "st-chart" });
const maxBpm = Math.max(...bpm, 1);
MONTHS.forEach((m, i) => makeRow(monthChart, m, (bpm[i] / maxBpm) * 100, "hsl(0 60% 42%)", bpm[i], "40px"));

// Reading speed
sectionTitle(root, "⏱️ Reading Speed");
if (avgDays === null) {
  root.createEl("div", { cls: "st-empty", text: "Add started & finished dates to your novel notes to see reading speed." });
} else {
  const speedCards = root.createEl("div", { cls: "st-speed-cards" });
  function makeSpeedCard(parent, num, label, cls) {
    const c = parent.createEl("div", { cls: "st-speed-card" + (cls ? " " + cls : "") });
    c.createEl("span", { cls: "st-speed-num", text: String(num) });
    c.createEl("span", { cls: "st-speed-lbl", text: label });
  }
  makeSpeedCard(speedCards, avgDays + " days", "average time to finish");
  if (fastest) makeSpeedCard(speedCards, fastest.days + "d", "fastest: " + fastest.title, "green");
  if (slowest) makeSpeedCard(speedCards, slowest.days + "d", "slowest: " + slowest.title);
}

// Rating distribution
sectionTitle(root, "⭐ Rating Distribution");
const ratingChart = root.createEl("div", { cls: "st-chart" });
[5,4,3,2,1].forEach(star => {
  const count = active.filter(p => parseRating(p.rating) === star).length;
  const pct = all.length > 0 ? (count / all.length) * 100 : 0;
  makeRow(ratingChart, "⭐".repeat(star), pct, "hsl(0 60% 42%)", count);
});

// Moods
sectionTitle(root, "🎭 Moods");
if (moodEntries.length === 0) {
  root.createEl("div", { cls: "st-empty", text: "Add mood: [emotional, dark] to your novel notes to see this chart." });
} else {
  const moodWrap = root.createEl("div", { cls: "st-mood-wrap" });
  const pie = moodWrap.createEl("div", { cls: "st-pie" });
  let deg = 0;
  const segs = moodEntries.map(([key, count]) => {
    const color = MOOD_COLORS[key] || "#888";
    const angle = (count / moodTotal) * 360;
    const seg = color + " " + deg.toFixed(1) + "deg " + (deg + angle).toFixed(1) + "deg";
    deg += angle;
    return seg;
  });
  pie.style.background = "conic-gradient(" + segs.join(", ") + ")";
  const legend = moodWrap.createEl("div", { cls: "st-mood-legend" });
  moodEntries.forEach(([key, count]) => {
    const row = legend.createEl("div", { cls: "st-legend-row" });
    const dot = row.createEl("span", { cls: "st-legend-dot" });
    dot.style.background = MOOD_COLORS[key] || "#888";
    row.createEl("span", { cls: "st-legend-name", text: key });
    row.createEl("span", { cls: "st-legend-val", text: String(count) });
  });
}

// Genres
sectionTitle(root, "📚 Genres");
const genreMap = {};
active.forEach(p => {
  parseList(p.genre).forEach(g => { const k = String(g).trim(); if (k) genreMap[k] = (genreMap[k] || 0) + 1; });
});
const topGenres = Object.entries(genreMap).sort((a, b) => b[1] - a[1]);
if (topGenres.length === 0) {
  root.createEl("div", { cls: "st-empty", text: "Add genre: [Xianxia, Historical] to your novel notes to see this chart." });
} else {
  const genreChart = root.createEl("div", { cls: "st-chart" });
  const maxG = topGenres[0]?.[1] || 1;
  topGenres.forEach(([genre, count]) => makeRow(genreChart, genre, (count / maxG) * 100, "hsl(220 45% 40%)", count));
}

// Top authors
sectionTitle(root, "✍️ Top Authors");
const authorMap = {};
active.forEach(p => { const a = p.author ? String(p.author).trim() : "Unknown"; authorMap[a] = (authorMap[a] || 0) + 1; });
const topAuthors = Object.entries(authorMap).sort((a, b) => b[1] - a[1]).slice(0, 8);
const authorChart = root.createEl("div", { cls: "st-chart" });
const maxA = topAuthors[0]?.[1] || 1;
topAuthors.forEach(([name, count]) => makeRow(authorChart, name, (count / maxA) * 100, "hsl(2 55% 38%)", count, "160px"));



// EN license status
sectionTitle(root, "🏷️ EN License Status");
const enGroups = { complete: 0, ongoing: 0, upcoming: 0, "not licensed": 0 };
active.forEach(p => { const sp = String(p.statuspub || "").toLowerCase().trim(); if (enGroups[sp] !== undefined) enGroups[sp]++; });
const enColors = { complete: "#22c55e", ongoing: "#eab308", upcoming: "#3b82f6", "not licensed": "#6b7280" };
const enChart = root.createEl("div", { cls: "st-chart" });
const maxEn = Math.max(...Object.values(enGroups), 1);
Object.entries(enGroups).forEach(([key, count]) => makeRow(enChart, key, (count / maxEn) * 100, enColors[key], count));


