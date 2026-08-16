---
title: This Demon Venerable Also Wants to Know
author: Cyan Wings
original_title: ""
status: Unread
rating: ""
volumes_read: 0
volumes_total: 3
genre: [Danmei, Xianxia, Historical, System]
cover: https://www.danmeinews.com/wp-content/uploads/2025/01/devilvenerable-vol-1-cover.jpg
mood: [funny, adventurous, emotional]
started: 
finished: ""
statuspub: ongoing
en_published: 2

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
> Demonic sect leader, Wenren E, accidentally stumbles upon a romance novel featuring tragedy and plot holes. Most importantly, it seems to mirror his own world. In the novel, he is destined to die for the sake of a woman he doesn’t care about, driving his subordinate Yin Hanjiang’s descent into madness and destruction.
> First of all… Why?! None of it makes sense to him, and he isn’t about to let it happen either. Armed with this forbidden knowledge, he decides to rewrite his own story—starting by saving Yin Hanjiang.
> As they journey through bloodied battlefields, snowy wastelands, and illusionary realms, their bond deepens, shaped by loyalty, sacrifice, and something far more dangerous: love. With demonic cultivation threatening his soul and an ancient Blood Demon rising once more, Wenren E must face the past that broke him, the future that awaits him, and the man who would follow him into hell. Can a man forged in blood learn to choose love over fate?

## My Notes

## Characters

## Quotes
