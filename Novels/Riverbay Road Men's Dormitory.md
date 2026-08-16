---
title: Riverbay Road Men's Dormitory
author: Fei Tian Ye Xiang
original_title: ""
status: Unread
rating: ""
volumes_read: 0
volumes_total: 2
genre: [Danmei, Modern, Slice of Life]
cover: "https://m.media-amazon.com/images/S/compressed.photo.goodreads.com/books/1736781413i/217045766.jpg"
pairing: ""
themes: []
mood: [lighthearted, funny, emotional, hopeful]
pages:
started: 
finished: ""
statuspub: complete
en_published: 2 
synopsis: ""
my_notes: ""
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
> Multimillionaire movie director Zhang Yuwen has it all—fame, fortune, and a successful career. But what he really craves is to create a novel he can call true art. Passionate about this dream, he abandons the film industry to pursue writing full-time, only to hit an unexpected roadblock: his characters feel flat, lacking the authenticity he longs for. The problem? Zhang Yuwen has spent most of his life alone and hasn’t had much real-world interaction to draw from.
As a single gay man with a luxurious villa full of empty rooms, Zhang Yuwen comes up with an unconventional solution. Why not rent those rooms out to other gay men and use them as inspiration for his novel’s characters? Enter his four new roommates: Yan Jun, a single father; Chen Hong, a fitness coach; Zheng Weize, a shy young livestreamer; and Chang Jinxing, a playboy and aspiring photographer. Each brings their own unique story and quirks, giving Zhang Yuwen the perfect opportunity to study real people up close.

## My Notes

## Characters

## Quotes
