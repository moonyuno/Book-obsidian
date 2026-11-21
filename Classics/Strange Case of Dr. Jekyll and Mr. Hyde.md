---
cssclasses:
  - classic-note
title: "Strange Case of Dr Jekyll and Mr Hyde"
author: "Robert Louis Stevenson"
original_title: "Strange Case of Dr Jekyll and Mr Hyde"
original_year: 1886
edition: ""
publisher: ""
language: English
status: Unread
rating: ""
pages_read: 0
pages_total: 0
word_count:
cover: https://www.hachettebookgroup.com/wp-content/uploads/2025/04/9781402794544.jpg
genre:
  - Gothic
  - Horror
  - Psychological Fiction
  - Novella
mood:
  - Dark
  - Atmospheric
  - Unsettling
  - Mysterious
  - Philosophical
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
> London lawyer Gabriel Utterson becomes increasingly disturbed by the connection between his respectable friend Dr Henry Jekyll and a violent, deeply unsettling man named Edward Hyde. Jekyll has altered his will so that Hyde will inherit everything should he disappear, yet refuses to explain why.
>
> As Hyde's behaviour grows more brutal and Jekyll retreats further from society, Utterson begins investigating the strange relationship between the two men. What he uncovers reveals a horrifying experiment and a struggle between virtue and corruption taking place far closer to Jekyll than anyone imagined.

## My Notes

## Characters

### Dr Henry Jekyll

### Edward Hyde

### Gabriel John Utterson

### Dr Hastie Lanyon

### Mr Poole

### Richard Enfield

## Quotes

## Edition Notes