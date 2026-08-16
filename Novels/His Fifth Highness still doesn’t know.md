---
title: "His Fifth Highness Still Doesn't Know"
author: "Mai Xiang Ji Ne"
original_title: "五殿下还在受骗"
status: Unread
rating: ""
volumes_read: 0
volumes_total: 1
genre:
  - Danmei
  - Xianxia
  - Fantasy
  - Historical
  - Romance
  - Comedy
  - Supernatural
mood: []
cover: https://m.media-amazon.com/images/S/compressed.photo.goodreads.com/books/1767449077i/223726733.jpg
started: 
finished: ""
statuspub: Complete
en_published: 1
pairing: "Jing Feirong x Chu Yanchuan"
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
> Jing Feirong is the fifth son of the Heavenly Emperor and a dragon prince expected to inherit a great destiny. Unfortunately, his cultivation has left him under constant pressure, and his impulsive, emotional nature has made him rather easy for others to deceive. [97][105]
> 
> When Jing Feirong is forced into a marriage with Chu Yanchuan, an aloof and impossibly beautiful god who is centuries older than him, he declares that he would rather throw himself from the God-Slaying Platform than accept the arrangement. [98][109]
> 
> His resolve does not survive long after the wedding. On their wedding night, Chu Yanchuan reveals a surprisingly tender side, and Jing Feirong quickly becomes a lovestruck, clingy dragon husband who is convinced that he has finally found domestic happiness. [97][105]
> 
> But Chu Yanchuan is far more difficult to understand than his beautiful face suggests. While Jing Feirong is busy falling head over heels, hidden motives, divine politics, and misunderstandings begin to threaten their marriage. And when Chu Yanchuan suddenly talks about divorce, Jing Feirong is left wondering how a marriage between a god and a dragon could possibly be ended so easily. [98][109]
> 
> A light-hearted xianxia romance about an overly trusting fifth prince, a seemingly detached god, and a relationship in which Jing Feirong is almost always the last person to realise what is really going on.

## My Notes

## Characters

## Quotes
