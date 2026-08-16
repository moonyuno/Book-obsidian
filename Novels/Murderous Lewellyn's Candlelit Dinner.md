---
title: "Murderous Lewellyn's Candlelit Dinner"
author: "Sumnagi"
original_title: "살인마 르웰린 씨의 낭만적인 정찬"
status: Unread
rating: ""
volumes_read: 0
volumes_total: 6
genre:
  - Korean Novel
  - BL
  - Mystery
  - Thriller
  - Historical
cover: https://images.thalia.media/00/-/8682d466cdf542af89395e31c5a74089/murderous-lewellyn-s-candlelit-dinner-1-taschenbuch-sumnagi.jpeg
started: 
finished: ""
statuspub: Completed
en_published: 5
pairing: "Shavonne x Lewellyn"
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
> Shavonne is a poor ghostwriter barely scraping by in a run-down apartment on the infamous Ira Street — a neighbourhood plagued by poverty, violence, and a string of unsolved murders. Before he can make sense of the strange notes appearing on his door every morning, he becomes fixated on his peculiar new neighbour Lewellyn: a strikingly handsome young man who spends his days peeling onions on the staircase outside Shavonne's unit. After finally accepting a dinner invitation, Shavonne makes a gruesome discovery in Lewellyn's bedroom — a corpse. Now caught between fear and an inexplicable pull toward his dangerous neighbour, Shavonne must figure out whether Lewellyn is his greatest threat… or the only one truly on his side.



## My Notes

## Characters

## Quotes
