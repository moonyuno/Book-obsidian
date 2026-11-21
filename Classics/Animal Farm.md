---
cssclasses:
  - classic-note
title: "Animal Farm"
author: "George Orwell"
original_title: "Animal Farm"
original_year: 1945
edition: ""
publisher: ""
language: English
status: Unread
rating: 
pages_read: 0
pages_total: 0
word_count:
cover: https://m.media-amazon.com/images/I/91Lbhwt5RzL._AC_UF894,1000_QL80_.jpg
genre:
  - Political Satire
  - Allegory
  - Dystopian Fiction
  - Novella
mood:
  - Satirical
  - Dark
  - Ironic
  - Political
  - Bleak
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
> The animals of Manor Farm, exhausted by neglect and exploitation, overthrow their human owner and take control of the farm themselves. Inspired by the hope of creating a society in which all animals are equal, they establish their own rules and begin building a new life free from human domination.
>
> But as the pigs gradually assume more authority, the ideals of the revolution begin to change. Under Napoleon's leadership, power becomes increasingly concentrated, the past is rewritten, and the distinction between the old rulers and the new ones becomes harder to see.

## My Notes

## Characters

### Napoleon

### Snowball

### Boxer

### Clover

### Squealer

### Old Major

### Benjamin

### Mr Jones

## Quotes

## Edition Notes