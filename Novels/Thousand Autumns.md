---
title: "{{Thousand Autumns}}"
author: Meng Xi Shi
original_title:
rating: ⭐⭐⭐⭐
cover: https://m.media-amazon.com/images/I/91HTPk9msPL._SL1500_.jpg
status: Finished
volumes_read: 5
volumes_total: 5
genre: [Danmei, Historical, Wuxia]
mood: [emotional, tense, mysterious, dark]
started: 2023-05-02
finished: 2026-01-05
volumes: 5/5
banner: https://i.pinimg.com/736x/20/eb/ad/20ebad53b34027d5349f7a57fe0947dc.jpg
en_published: 5
statuspub: finished
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
> Yan Wushi, leader of the demonic [[Huanyue Sect]], is a master cultivator, a brilliant strategist, and an incurable cynic. In his philosophy, every human heart is ruled by cruelty and selfishness. Anyone who believes otherwise is either a liar or a fool.  
> Enter the humble Shen Qiao, leader of the Daoist sect at Xuandu Mountain. He is both gracious and charitable, and exactly the type of do-gooder that Yan Wushi despises.  
> When Shen Qiao suffers a shocking loss in a duel and is left for dead, Yan Wushi happens upon him and concocts a plan to teach him about the wretchedness of humanity. He’ll take Shen Qiao under his wing, test the limits of his faith, and lure him into demonic cultivation. After all, it is easy to remain righteous atop a mountain peak that touches the heavens. But a thousand autumns toiling on the blood-soaked earth will break any man.






