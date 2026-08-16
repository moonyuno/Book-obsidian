---
title: "{{Case File Compendium}}"
author: Rou Bao Bu Chi Rou
original_title: ""
status: Unread
rating:
tags: []
cover: https://m.media-amazon.com/images/I/81XxFXlIoaL._SL1500_.jpg
volumes_read: 0
volumes_total: 10
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre: [Danmei, Modern, Mystery, Thriller] 
mood: [dark, mysterious, tense, emotional]
started:
finished:
synopsis: ""
my_notes: ""
volumes: 0/10
banner: https://i.pinimg.com/736x/62/e7/77/62e7776a662744b70a81f7bd191f6518.jpg
en_published: 8
statuspub: ongoing
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

>[!synopsis] Synopsis
>Wealthy and handsome, yet mentally unstable—He Yu has returned home from overseas with one goal in mind: to win the heart of Xie Xue, the girl of his dreams. However, in his time away, he has nursed more than unrequited feelings. He must confront his long-held grudge against Xie Xue’s overprotective brother, Xie Qingcheng, who doesn’t think He Yu capable of love.  But history is not easily rewritten. As He Yu’s former doctor, Xie Qingcheng is the only person in the world who truly understands He Yu’s volatile mental illness. When the two are involved in an explosive incident that exposes a dark secret, Xie Qingcheng’s suspicions about He Yu are confirmed. Now, He Yu must confront his own demons…including his dark obsession with Xie Qingcheng.


---



## My Notes

## Characters

## Quotes
