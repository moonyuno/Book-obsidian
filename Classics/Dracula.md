---
cssclasses:
  - classic-note
title: "Dracula"
author: "Bram Stoker"
original_title: "Dracula"
original_year: 1897
edition: ""
publisher: ""
language: English
status: Unread
rating: ""
pages_read: 0
pages_total: 0
word_count:
cover: "https://images.thalia.media/-/BF750-750/760cb5128be84f9d909dc244a80295e8/bram-stoker-dracula-english-edition-taschenbuch-bram-stoker-englisch.jpeg"
genre:
  - Gothic
  - Horror
  - Epistolary Fiction
mood:
  - Dark
  - Atmospheric
  - Haunting
  - Suspenseful
  - Victorian
started:
finished:
---

```dataviewjs
const p = dv.current();

const h = dv.container.createEl(
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

const m = h.createEl("div");

if (p.author) {
    m.createEl(
        "div",
        {
            cls: "cl-note-author",
            text: String(p.author)
        }
    );
}

if (p.original_title && p.original_title !== p.title) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text: String(p.original_title)
        }
    );
}

if (p.original_year) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text: "First published: " + p.original_year
        }
    );
}

if (p.edition) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text: "Edition: " + p.edition
        }
    );
}

if (p.publisher) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text: "Publisher: " + p.publisher
        }
    );
}

if (p.language) {
    m.createEl(
        "div",
        {
            cls: "cl-note-meta-line",
            text: "Language: " + p.language
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
                Number(p.word_count).toLocaleString() +
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
> When Jonathan Harker travels to Transylvania to assist the mysterious Count Dracula with a property purchase in England, he soon realises that his host is no ordinary nobleman. After escaping the Count’s castle, Harker returns home only to find that Dracula has already begun extending his influence into England.
>
> As strange illnesses, nocturnal visitations and unexplained deaths begin to spread, a small group led by Professor Abraham Van Helsing joins forces to uncover the truth and stop the Count before his power grows beyond their control.

## My Notes

## Characters

### Count Dracula

### Jonathan Harker

### Mina Harker

### Lucy Westenra

### Professor Abraham Van Helsing

### Dr John Seward

### Arthur Holmwood

### Quincey Morris

### Renfield

## Quotes

## Edition Notes