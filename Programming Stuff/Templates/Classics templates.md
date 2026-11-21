---
cssclasses:
  - classic-note
title: "{{TITLE}}"
author: "{{VALUE:author|label:Author}}"
original_title: "{{VALUE:originalTitle|label:Original title|optional}}"
original_year: {{VALUE:year|label:First published|type:number|optional}}
edition: "{{VALUE:edition|label:Edition|optional}}"
publisher: "{{VALUE:publisher|label:Publisher|optional}}"
language: "{{VALUE:English,German,French,Other|name:language|label:Language}}"
status: Unread
rating: ""
pages_read: 0
pages_total: {{VALUE:pages|label:Pages|type:number|optional}}
word_count: {{VALUE:words|label:Word count|type:number|optional}}
cover: "{{VALUE:cover|label:Cover URL|optional}}"
genre: {{VALUE:Gothic,Horror,Romance,Coming-of-Age,Dystopian,Science Fiction,Historical Fiction,Literary Fiction,Mystery,Fantasy,Satire,Philosophical Fiction|name:genre|label:Genre|multi|custom|format:yaml}}
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