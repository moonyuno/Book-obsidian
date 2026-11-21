---
cssclasses:
  - classic-note
title: "The Phantom of the Opera"
author: "Gaston Leroux"
original_title: "Le Fantôme de l'Opéra"
original_year: 1910
edition: ""
publisher: ""
language: English
status: Unread
rating: ""
pages_read: 0
pages_total: 0
word_count:
cover: https://images.thalia.media/-/BF750-750/47542f0c03aa4f6eb927e3bfac1ad985/the-phantom-of-the-opera-gebundene-ausgabe-gaston-leroux-englisch.jpeg
genre:
  - Gothic
  - Mystery
  - Horror
  - Romance
mood:
  - Gothic
  - Theatrical
  - Haunting
  - Melancholic
  - Obsessive
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

if (p.original_title) {
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
            text:
                "Genre: " +
                genres.join(" · ")
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
> Beneath the splendour of the Paris Opera House lurks a mysterious figure known only as the Opera Ghost. When the young soprano Christine Daaé begins receiving lessons from an unseen musical genius, she believes the voice belongs to the Angel of Music promised to her by her late father. But the man behind the voice is Erik, a brilliant and disfigured recluse who has built his world beneath the theatre and developed a dangerous obsession with her.
>
> As Christine is drawn between Erik and her childhood friend Raoul, strange accidents, threats and disappearances begin to plague the opera house, forcing her deeper into the Phantom's hidden world.

## My Notes

## Characters

### Christine Daaé

### Erik

### Raoul de Chagny

### The Persian

### Madame Giry

## Quotes

## Edition Notes