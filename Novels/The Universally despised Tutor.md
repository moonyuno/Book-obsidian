---
title: "The Universally Despised Grand Tutor"
author: "Meng Huan"
original_title: "太傅他人人喊打"
status: Unread
rating: ""
volumes_read: 0
volumes_total: 1
genre:
  - Danmei
  - Historical
  - Romance
  - Political Intrigue
  - Drama
  - Action
  - Psychological
mood: []
started: 
finished: ""
statuspub: not licensed
en_published: 0
pairing: "Ji Huaizhen x Tuoba Yanchi"
cover: https://i.imgur.com/jIDZU2s.jpeg
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
> Ji Huaizhen is the Grand Tutor of Great Qi—and quite possibly one of the most hated men in the entire country. Ruthless, vindictive, shameless, and frighteningly good at surviving, he has spent years scheming his way through court politics without caring how many enemies he leaves behind.
>
> Unfortunately, being universally despised becomes considerably less convenient once the country falls.
>
> With Great Qi destroyed, his sister dead, and the young Crown Prince left in his care, Ji Huaizhen suddenly finds himself fleeing with his nephew while surrounded by people who would be delighted to see him suffer for everything he has done.
>
> Their best hope of survival lies with Tuoba Yanchi, a young warrior tied to the very people Ji Huaizhen ought to fear. Luckily, Ji Huaizhen has never encountered a disastrous situation he could not attempt to escape through shameless lying.
>
> So he tells the Crown Prince not to worry. Tuoba Yanchi is apparently his uncle's old lover. In fact, they practically married when they were seventeen. All the boy has to do is call him "Dad" at the appropriate moment.
>
> There is only one small problem: Tuoba Yanchi's feelings are tied to a man from his past, and Ji Huaizhen knows far more about that man than he intends to reveal.
>
> What begins as another of Ji Huaizhen's manipulations becomes tangled in mistaken identities, war, political schemes, betrayal, revenge, and old feelings that were never as simple as either man believed.

## My Notes

## Characters

## Quotes