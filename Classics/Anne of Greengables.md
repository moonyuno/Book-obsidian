---
cssclasses:
  - classic-note
title: "Anne of Green Gables"
author: "L. M. Montgomery"
original_title: "Anne of Green Gables"
original_year: 1908
edition: ""
publisher: ""
language: English
status: Unread
rating: ""
pages_read: 0
pages_total: 0
word_count:
cover: https://images.thalia.media/-/BF750-750/af88724ae356440e944721be63838e03/anne-of-green-gables-taschenbuch-lucy-maud-montgomery-englisch.jpeg
genre:
  - Coming-of-Age
  - Children's Literature
  - Domestic Fiction
mood:
  - Cozy
  - Pastoral
  - Whimsical
  - Heartwarming
  - Bittersweet
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
> When elderly siblings Marilla and Matthew Cuthbert decide to adopt a boy to help with the work at Green Gables, they are astonished when eleven-year-old Anne Shirley arrives instead. Red-haired, fiercely imaginative and incapable of saying anything in fewer words than absolutely necessary, Anne quickly turns their quiet life in Avonlea upside down.
>
> As she finds friendship, rivalry, belonging and a home she never expected to have, Anne grows from an impulsive orphan into a young woman whose imagination remains every bit as vivid as when she first arrived on Prince Edward Island.

## My Notes

## Characters

### Anne Shirley

### Marilla Cuthbert

### Matthew Cuthbert

### Diana Barry

### Gilbert Blythe

### Rachel Lynde

## Quotes

## Edition Notes