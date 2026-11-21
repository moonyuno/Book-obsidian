---
cssclasses:
  - classic-note
title: "Treasure Island"
author: "Robert Louis Stevenson"
original_title: ""
original_year: 1883
edition: ""
publisher: ""
language: "English"
status: Unread
rating: ""
pages_read: 0
pages_total: 200
word_count: 
cover: "https://fcs-img.s3.amazonaws.com/1ebda62b-7f02-4fab-8e39-a5e6016ae6b4/f2aff7f8-1b03-49f4-8e89-b32a014a87f4/XL.jpg"
genre: ["Coming-of-Age", "Historical Fiction", "Adventure", "Pirate Fiction"]
mood: []
started:
finished:
---

```dataviewjs
const p = dv.current();

const h =
    dv.container.createEl(
        "div",
        { cls: "cl-note-header" }
    );

if (p.cover) {
    h.createEl(
        "img",
        {
            cls: "cl-note-cover",
            attr: {
                src: String(p.cover)
            }
        }
    );
}

const m =
    h.createEl("div");

if (p.author) {
    m.createEl(
        "div",
        {
            cls: "cl-note-author",
            text: String(p.author)
        }
    );
}

if (p.original_year) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text:
                "First published: " +
                p.original_year
        }
    );
}

if (p.edition) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text:
                "Edition: " +
                p.edition
        }
    );
}

if (p.publisher) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text:
                "Publisher: " +
                p.publisher
        }
    );
}

if (p.language) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text:
                "Language: " +
                p.language
        }
    );
}
if (p.genre) {
    const genres = dv.array(p.genre)
        .array()
        .map(g => String(g));

    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text: "Genre: " + genres.join(" · ")
        }
    );
}

if (p.word_count) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text:
                Number(
                    p.word_count
                ).toLocaleString() +
                " words"
        }
    );
}
```

`INPUT[inlineSelect(option(Unread), option(Reading), option(On Hold), option(Finished), option(Dropped)):status]`
`INPUT[inlineSelect(option(⭐), option(⭐⭐), option(⭐⭐⭐), option(⭐⭐⭐⭐), option(⭐⭐⭐⭐⭐)):rating]`

Pages:
`INPUT[number:pages_read]`
/
`INPUT[number:pages_total]`

---

> [!synopsis] Synopsis
>

## My Notes

## Characters

## Quotes

## Edition Notes