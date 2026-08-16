---
title: "{{Remnants of Filth}}"
author: Rou Bao Bu Chi Rou
original_title: ""
status: Reading
rating: ⭐⭐⭐⭐
tags: []
cover: https://m.media-amazon.com/images/I/91Zawa5yTPL._SL1500_.jpg
volumes_read: 5
volumes_total: 7
translation: ""
pairing: ""
themes: []
genre:
  - Danmei
  - Xianxia
  - Historical
mood:
  - emotional
  - dark
  - sad
  - tense
started: 2026-06-24
finished:
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/1200x/7c/ed/77/7ced775a05eca2e6e43c3f195d966d11.jpg
en_published: 7
statuspub: complete
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


>[!synopsis]
>In the aftermath of Gu Mang’s defeat of the Demonblood Beast, Mo Xi rallies Chonghua’s troops to face the Liao Kingdom. But there is little hope for victory. The blood pool left by the beast’s death draws ever closer to the city walls, and the wicked Hua Po’an appears unstoppable. Just as all seems lost, the enigmatic Jiang Fuli reappears with an astonishing magical item—an ancient artifact with the ability to alter the past.  
>Mo Xi is presented with one last chance to avert Chonghua’s tragic future and save everyone he’s lost, though the cost to himself could be unimaginable. He is faced with a choice: How much more can he sacrifice for his beloved, and for the nation they both call home?



