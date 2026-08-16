---
title: Dinghai Fusheng Records
author: Fei Tian Ye Xiang
original_title: 定海浮生录
status: Unread
rating:
volumes_read: 0
volumes_total: 6
genre:
  - Danmei
  - Historical
  - Fantasy
  - Xianxia
mood:
  - emotional
  - dark
  - adventurous
  - sad
started:
finished:
cover: https://m.media-amazon.com/images/I/91l6XqMDmiL._SL1500_.jpg
banner: https://i.pinimg.com/736x/5b/f7/16/5bf716556b19d63c9fddfc9d3d394ece.jpg
en_published: 4
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
> Once, ancient China was brimming with magic…but three hundred years ago, the Spiritual Qi of the Heavens and Earth dried up in the Silence of All Magic. Hundreds of years with no spiritual qi have allowed resentment to build unchecked, and it’s only a matter of time before calamity descends and the world is plunged into chaos and destruction. Once-powerful exorcists have done their best to preserve their legacy in the centuries since, but now only one remains: Chen Xing, now tasked with venturing out into the war-torn world to prevent the impending apocalypse.
> Chen Xing’s sole magical ability is a heart lamp, a supernatural light source that’s supposed to guide him to the destined Protector who will fight at his side. The heart lamp picks Xiang Shu, a mysterious stranger with no interest in being a hero—but fate has other plans for them both. A terrifying conspiracy looms over the Divine Land, and whether Xiang Shu likes it or not, Chen Xing may be his only hope of thwarting the impending darkness.



