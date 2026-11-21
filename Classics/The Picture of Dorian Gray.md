---
cssclasses:
  - classic-note
title: "The Picture of Dorian Gray"
author: "Oscar Wilde"
original_title: "The Picture of Dorian Gray"
original_year: 1890
edition: ""
publisher: ""
language: English
status: Unread
rating: ""
pages_read: 0
pages_total: 0
word_count: 78000
cover: https://images.thalia.media/-/BF750-750/107cbefdd6054cd9b9ffe0d8771d33a2/das-bildnis-des-dorian-gray-gebundene-ausgabe-oscar-wilde.jpeg
genre:
  - Classic
  - Gothic
  - Philosophical Fiction
  - Decadent Literature
mood:
  - Gothic
  - Dark Academia
  - Decadent
  - Psychological
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
> Dorian Gray is a beautiful young man whose portrait is painted by the artist Basil Hallward. After meeting the cynical Lord Henry Wotton, Dorian becomes obsessed with youth, beauty and pleasure, wishing that the portrait might age in his place. As his life grows increasingly corrupt, the painting begins to bear the physical and moral consequences that Dorian himself appears able to escape.

## My Notes

## Characters

### Dorian Gray

### Lord Henry Wotton

### Basil Hallward

## Quotes

## Edition Notes