---
title: "{{Scum Villain's Self-Saving System}}"
author: Mo Xiang Tong Xiu
original_title: ""
status: Finished
rating: ⭐⭐⭐⭐
tags: []
cover: https://m.media-amazon.com/images/I/91Spe++JppL._SL1500_.jpg
volumes_read: 4
volumes_total: 4
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre:
  - Danmei
  - Xianxia
  - Historical
  - Transmigration
  - System
mood:
  - funny
  - emotional
  - adventurous
started: 2026-03-03
finished: 2026-06-20
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/736x/51/79/62/5179629d079a6533f92d54c9b9384c28.jpg
en_published: 4
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
>Half-demon Luo Binghe rose from humble beginnings and a tortured past to become unrivaled in strength and beauty. With his dominion over both the Human and Demon Realms and his hundreds-strong harem, he is truly the most powerful protagonist...in a trashy webnovel series!  
>At least, that's what Shen Yuan believes as he finishes reading the final chapter in Proud Immortal Demon Way. But when a bout of rage leads to his sudden death, Shen Yuan is reborn into the world of the novel in the body of Shen Qingqiu--the beautiful but cruel teacher of a young Luo Binghe. While Shen Qingqiu may have the incredible power of a cultivator, he is destined to be horrifically punished for crimes against the protagonist. The new Shen Qingqiu now has only one course of action: get into Luo Binghe's good graces before the young man's rise to power or suffer the awful fate of a true scum villain!


