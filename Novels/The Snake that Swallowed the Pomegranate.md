---
title: "The Snake That Swallowed the Pomegranate"
author: "Carpe XD"
original_title: "석류를 삼킨 뱀"
status: Unread
rating: ""
volumes_read: 0
volumes_total: 5
genre:
  - Korean Novel
  - BL
  - Fantasy
  - Historical
  - Mystery
  - Smut
cover: https://i.imgur.com/ZiBYhwM.jpeg
started: 
finished: ""
statuspub: Completed
en_published: 0
pairing: "Nain x Ran Gwen x Amon"
---

```dataviewjs
const p = dv.current();
const h = dv.container.createEl("div", { cls: "nnote-header" });
if (p.cover) h.createEl("img", { attr: { src: String(p.cover) }, cls: "nnote-cover" });
const m = h.createEl("div", { cls: "nnote-meta" });
if (p.author) m.createEl("div", { text: String(p.author), cls: "nnote-author" });
if (p.original_title) m.createEl("div", { text: String(p.original_title), cls: "nnote-orig" });
if (p.pairing) m.createEl("div", { text: String(p.pairing), cls: "nnote-pairing" });
if (p.published) m.createEl("div", { text: "EN release: " + String(p.published), cls: "nnote-pub" });
if (p.en_published > 0) {
  const enNum = Number(p.en_published);
  const enTotal = p.volumes_total ? Number(p.volumes_total) : 0;
  const isComplete = enTotal > 0 && enNum >= enTotal;
  const enText = "EN: " + enNum + "/" + (enTotal || "?") + (isComplete ? " (complete)" : " vols out");
  m.createEl("div", { text: enText, cls: "nnote-en" });
}
const genres = Array.isArray(p.genre) ? p.genre.join(" · ") : (p.genre || "");
if (genres) m.createEl("div", { text: genres, cls: "nnote-genre" });
```

`INPUT[inlineSelect(option(Unread), option(Reading), option(On Hold), option(Finished), option(Dropped)):status]` `INPUT[inlineSelect(option(⭐), option(⭐⭐), option(⭐⭐⭐), option(⭐⭐⭐⭐), option(⭐⭐⭐⭐⭐)):rating]` `INPUT[number:volumes_read]` / `INPUT[number:volumes_total]` `BUTTON[vol-plus]` `BUTTON[vol-minus]` `BUTTON[btn-start]` `BUTTON[btn-finish]`

> [!mb-defs]-
> ```meta-bind-button
> id: vol-plus
> style: default
> label: "+ Vol"
> actions:
>   - type: runTemplaterFile
>     templateFile: "Templates/Increment Volume.md"
> ```
> ```meta-bind-button
> id: vol-minus
> style: default
> label: "- Vol"
> actions:
>   - type: runTemplaterFile
>     templateFile: "Templates/Decrement Volume.md"
> ```
> ```meta-bind-button
> id: btn-start
> style: default
> label: "Start"
> actions:
>   - type: runTemplaterFile
>     templateFile: "Templates/Set Started Date.md"
> ```
> ```meta-bind-button
> id: btn-finish
> style: default
> label: "Finished"
> actions:
>   - type: runTemplaterFile
>     templateFile: "Templates/Set Finished Date.md"
> ```



> [!synopsis] Synopsis
> In the prosperous land of Trastasa, the god Amon rules from a dazzling temple with his human consort Nain at his side. [web:86][web:97]
> Nain lives in a world of divine beauty, but Amon’s devotion is possessive and unsettling, making love feel dangerously close to being devoured. [web:86][web:95]
> When a new concubine named Ran Gwen arrives, rare pink hair and eyes immediately draw Amon’s attention, and Nain is consumed by jealousy. [web:70][web:86]
> But Ran Gwen is not what Nain expects: he shows an eerie interest in Nain himself, not in Amon, and that interest starts to unravel the careful balance of Nain’s life. [web:70][web:86]
> What begins as jealousy and suspicion turns into a tangled mix of desire, obsession, misunderstanding, and dangerous attraction inside a temple that is beautiful on the surface and deeply rotten underneath. [web:70][web:97]

## My Notes

## Characters

## Quotes
