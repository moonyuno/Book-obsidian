---
cssclasses:
  - classics-dashboard
exclude: true
sort_classics: Year
filter_author: ""
filter_period: All
---

<div class="cl-hero">
  <div class="cl-kicker">PERSONAL LIBRARY</div>
  <div class="cl-hero-title">The Classics</div>
  <div class="cl-hero-subtitle">Old books, beautiful editions, questionable people making terrible decisions.</div>
</div>

```dataviewjs
const pages = dv.pages('"Classics"').array();

function ratingNumber(r) {
    if (!r) return 0;

    const s = String(r);

    const stars = (s.match(/⭐/g) || []).length;
    if (stars) return stars;

    const slash = s.match(/(\d+(?:\.\d+)?)\s*\/\s*5/);
    if (slash) return Number(slash[1]);

    const n = Number(s);
    return isNaN(n) ? 0 : n;
}

const total = pages.length;
const reading = pages.filter(p => p.status === "Reading").length;
const unread = pages.filter(p => p.status === "Unread" || !p.status).length;
const finished = pages.filter(p => p.status === "Finished").length;
const onHold = pages.filter(p => p.status === "On Hold").length;

const rated = pages
    .map(p => ratingNumber(p.rating))
    .filter(n => n > 0);

const avg =
    rated.length
        ? (
            rated.reduce((a, b) => a + b, 0) /
            rated.length
          ).toFixed(1)
        : "–";

const stats = dv.container.createEl(
    "div",
    { cls: "cl-stats" }
);

function stat(number, label, accent = false) {
    const card = stats.createEl(
        "div",
        {
            cls:
                "cl-stat-card" +
                (accent ? " accent" : "")
        }
    );

    card.createEl(
        "span",
        {
            cls: "cl-stat-num",
            text: String(number)
        }
    );

    card.createEl(
        "span",
        {
            cls: "cl-stat-label",
            text: label
        }
    );
}

stat(total, "Books");
stat(reading, "Reading", true);
stat(onHold, "On Hold");
stat(unread, "Unread");
stat(finished, "Finished");
stat(avg === "–" ? "–" : `⭐ ${avg}`, "Avg Rating");
```

---

**Sort:** `INPUT[inlineSelect(option(Title), option(Author), option(Rating), option(Progress), option(Year), option(Length), option(Date Added)):sort_classics]`
&nbsp;&nbsp;
**Author:** `INPUT[text(placeholder(author...)):filter_author]`
&nbsp;&nbsp;
**Period:** `INPUT[inlineSelect(option(All), option(Before 1800), option(1800s), option(1900s), option(2000s)):filter_period]`

---

```dataviewjs
const allPages = dv.pages('"Classics"').array();

const cur = dv.current();

const sortBy =
    cur.sort_classics || "Title";

const authorFilter =
    String(cur.filter_author || "")
        .trim()
        .toLowerCase();

const period =
    cur.filter_period || "All";


function clean(value) {
    return value == null
        ? ""
        : String(value)
            .replace(/\{\{|\}\}/g, "")
            .trim();
}


function ratingNumber(r) {
    if (!r) return 0;

    const s = String(r);

    const stars =
        (s.match(/⭐/g) || []).length;

    if (stars) return stars;

    const slash =
        s.match(
            /(\d+(?:\.\d+)?)\s*\/\s*5/
        );

    if (slash)
        return Number(slash[1]);

    const n = Number(s);

    return isNaN(n) ? 0 : n;
}


function progressOf(p) {
    const read =
        Number(p.pages_read || 0);

    const total =
        Number(p.pages_total || 0);

    if (!total)
        return null;

    return {
        read,
        total,
        ratio:
            Math.max(
                0,
                Math.min(
                    1,
                    read / total
                )
            )
    };
}


function periodMatches(p) {
    if (period === "All")
        return true;

    const y =
        Number(p.original_year);

    if (!y)
        return false;

    if (period === "Before 1800")
        return y < 1800;

    if (period === "1800s")
        return y >= 1800 && y <= 1899;

    if (period === "1900s")
        return y >= 1900 && y <= 1999;

    if (period === "2000s")
        return y >= 2000;

    return true;
}


function baseFilter(p) {
    if (
        authorFilter &&
        !clean(p.author)
            .toLowerCase()
            .includes(authorFilter)
    ) {
        return false;
    }

    return periodMatches(p);
}


function sortPages(pages) {
    const arr =
        [...pages];

    arr.sort(
        (a, b) => {
            if (sortBy === "Title") {
                return (
                    clean(a.title) ||
                    a.file.name
                ).localeCompare(
                    clean(b.title) ||
                    b.file.name
                );
            }

            if (sortBy === "Author") {
                return clean(a.author)
                    .localeCompare(
                        clean(b.author)
                    );
            }

            if (sortBy === "Rating") {
                return (
                    ratingNumber(b.rating) -
                    ratingNumber(a.rating)
                );
            }

            if (sortBy === "Progress") {
                const ap =
                    progressOf(a)?.ratio || 0;

                const bp =
                    progressOf(b)?.ratio || 0;

                return bp - ap;
            }

            if (sortBy === "Year") {
                return (
                    Number(a.original_year || 0) -
                    Number(b.original_year || 0)
                );
            }

            if (sortBy === "Length") {
                return (
                    Number(b.word_count || 0) -
                    Number(a.word_count || 0)
                );
            }

            if (sortBy === "Date Added") {
                const at =
                    a.file.ctime?.toMillis?.() ||
                    0;

                const bt =
                    b.file.ctime?.toMillis?.() ||
                    0;

                return bt - at;
            }

            return 0;
        }
    );

    return arr;
}


function renderCard(p, grid) {
    const card =
        grid.createEl(
            "div",
            { cls: "cl-card" }
        );

    const coverWrap =
        card.createEl(
            "div",
            { cls: "cl-cover-wrap" }
        );

    const link =
        coverWrap.createEl(
            "a",
            {
                cls:
                    "internal-link cl-cover-link",
                attr: {
                    href: p.file.path
                }
            }
        );

    if (p.cover) {
        link.createEl(
            "img",
            {
                cls: "cl-cover",
                attr: {
                    src: String(p.cover)
                }
            }
        );
    }

    if (p.original_year) {
        card.createEl(
            "div",
            {
                cls: "cl-year-badge",
                text:
                    String(
                        p.original_year
                    )
            }
        );
    }

    const info =
        card.createEl(
            "div",
            { cls: "cl-info" }
        );

    info.createEl(
        "a",
        {
            cls:
                "cl-title internal-link",
            text:
                clean(p.title) ||
                p.file.name,

            attr: {
                href: p.file.path
            }
        }
    );

    if (p.author) {
        const field =
            info.createEl(
                "div",
                { cls: "cl-field" }
            );

        field.createEl(
            "div",
            {
                cls: "cl-label",
                text: "AUTHOR"
            }
        );

        field.createEl(
            "div",
            {
                cls: "cl-value",
                text:
                    clean(p.author)
            }
        );
    }

    if (p.status) {
        const field =
            info.createEl(
                "div",
                { cls: "cl-field" }
            );

        field.createEl(
            "div",
            {
                cls: "cl-label",
                text: "STATUS"
            }
        );

        field.createEl(
            "div",
            {
                cls: "cl-value",
                text:
                    clean(p.status)
            }
        );
    }

    const prog =
        progressOf(p);

    if (prog) {
        const pct =
            Math.round(
                prog.ratio * 100
            );

        const field =
            info.createEl(
                "div",
                { cls: "cl-field" }
            );

        field.createEl(
            "div",
            {
                cls: "cl-label",
                text: "PROGRESS"
            }
        );

        field.createEl(
            "div",
            {
                cls: "cl-value",
                text:
                    `${prog.read}/${prog.total} pages · ${pct}%`
            }
        );

        const bar =
            info.createEl(
                "div",
                {
                    cls:
                        "cl-progress-wrap"
                }
            );

        bar.createEl(
            "div",
            {
                cls:
                    "cl-progress-bar",

                attr: {
                    style:
                        `width:${pct}%`
                }
            }
        );
    }

    if (p.word_count) {
        const count =
            Number(p.word_count);

        const field =
            info.createEl(
                "div",
                { cls: "cl-field" }
            );

        field.createEl(
            "div",
            {
                cls: "cl-label",
                text: "LENGTH"
            }
        );

        field.createEl(
            "div",
            {
                cls: "cl-value",
                text:
                    `${Math.round(
                        count / 1000
                    ).toLocaleString()}k words`
            }
        );
    }

    if (p.rating) {
        const field =
            info.createEl(
                "div",
                { cls: "cl-field" }
            );

        field.createEl(
            "div",
            {
                cls: "cl-label",
                text: "RATING"
            }
        );

        field.createEl(
            "div",
            {
                cls: "cl-value",
                text:
                    String(p.rating)
            }
        );
    }
}


function renderSection(
    title,
    emoji,
    statuses
) {
    const pages =
        sortPages(
            allPages.filter(
                p =>
                    statuses.includes(
                        p.status ||
                        "Unread"
                    ) &&
                    baseFilter(p)
            )
        );

    dv.header(
        2,
        `${emoji} ${title}`
    );

    if (!pages.length) {
        dv.container.createEl(
            "div",
            {
                cls: "cl-empty",
                text:
                    "Nothing here yet."
            }
        );

        return;
    }

    const grid =
        dv.container.createEl(
            "div",
            { cls: "cl-grid" }
        );

    for (const p of pages)
        renderCard(p, grid);
}


renderSection(
    "Currently Reading",
    "📖",
    ["Reading"]
);

renderSection(
    "On Hold",
    "🕯️",
    ["On Hold"]
);

renderSection(
    "The Library",
    "🏛️",
    ["Unread"]
);

renderSection(
    "Finished",
    "❦",
    ["Finished"]
);

const dropped =
    allPages.filter(
        p =>
            p.status === "Dropped" &&
            baseFilter(p)
    );

if (dropped.length) {
    renderSection(
        "Abandoned to History",
        "🥀",
        ["Dropped"]
    );
}
```