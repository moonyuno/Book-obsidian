---
title: Copper Coins
author: Mu Su Li
original_title: ""
status: Unread
rating:
volumes_read: 0
volumes_total: 3
genre: [Danmei, Historical, Mystery, Wuxia]
mood: [mysterious, dark, emotional]
started:
finished:
cover: https://sevenseasentertainment.com/wp-content/uploads/2024/10/copper_coins_DN1_coverFRONT.jpg
banner: https://i.pinimg.com/1200x/a1/d9/a8/a1d9a8001471ca4f6bbd077a9155955c.jpg
en_published: 3
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

> [!synopsis] Synopsis
> Under the pale glow of dawn, Xue Xian—once a mighty dragon, now a handmade paper effigy—is moments away from being exorcised. The worst part? He doesn’t see it coming. Spellbound into his form alongside the ever-irritating Jiang Shining—a restless ghost caught up in the dragon’s misfortunes—the two must navigate a perilous path to settle long-standing scores.
> Enter Xuanmin, an enigmatic monk drawn to the ruins of Jiang Manor by the lingering traces of a sinister curse. Finding two crude paper figures he surmises to be evil spirits, he tosses them into his pouch, taking the dragon and ghost along for the ride. Furious at his new predicament, Xue Xian swears revenge: If he must suffer this journey, he’ll make sure the aloof monk suffers right alongside him.
> Thus begins an unusual pilgrimage, where three unlikely companions—an exiled dragon, a restless ghost, and a monk without a past—must unravel the tangled mysteries of their fates.

---



