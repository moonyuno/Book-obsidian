---
cssclasses:
  - classic-note
title: "A Street Cat Named Bob"
author: "James Bowen"
original_title: "A Street Cat Named Bob"
original_year: 2012
edition: ""
publisher: ""
language: ""
status: Unread
rating: ""
pages_read: 0
pages_total: 0
word_count:
cover: https://m.media-amazon.com/images/S/compressed.photo.goodreads.com/books/1331779332i/12394068.jpg
genre:
  - Memoir
  - Nonfiction
  - Animals
mood:
  - Heartwarming
  - Emotional
  - Hopeful
  - Bittersweet
  - Uplifting
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
> James Bowen is struggling to rebuild his life while earning what he can as a street musician in London when he discovers an injured ginger tomcat in the hallway of his building. Despite barely being able to look after himself, James takes the cat in, nurses him back to health and names him Bob.
>
> James expects Bob eventually to return to life on the streets. Bob has other ideas. He begins following James everywhere, and the bond that develops between them gradually transforms both of their lives.

## My Notes

## Characters

### James Bowen

### Bob

## Quotes

## Edition Notes