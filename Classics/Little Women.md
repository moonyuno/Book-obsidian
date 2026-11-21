---
cssclasses:
  - classic-note
title: "Little Women"
author: "Louisa May Alcott"
original_title: "Little Women"
original_year: 1868
edition: ""
publisher: ""
language: English
status: Unread
rating: ""
pages_read: 0
pages_total: 0
word_count:
cover: https://m.media-amazon.com/images/I/81XxP9qyfzL.jpg
genre:
  - Coming-of-Age
  - Domestic Fiction
  - Family Saga
mood:
  - Cozy
  - Nostalgic
  - Heartwarming
  - Bittersweet
  - Romantic
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
> In Civil War-era Massachusetts, the four March sisters—Meg, Jo, Beth and Amy—grow up together while their father is away at war. Though the family has little money, their home is filled with affection, imagination and the steady guidance of their mother, Marmee.
>
> Each sister dreams of a different future: Meg longs for a comfortable home, fiercely independent Jo wants to become a writer, gentle Beth finds happiness in music and family, and ambitious Amy dreams of art and refinement. As childhood gradually gives way to adulthood, the sisters encounter friendship, love, disappointment, grief and the difficult question of what kind of lives they truly want to lead.

## My Notes

## Characters

### Josephine "Jo" March

### Margaret "Meg" March

### Elizabeth "Beth" March

### Amy March

### Marmee

### Theodore "Laurie" Laurence

### Mr. Laurence

## Quotes

## Edition Notes