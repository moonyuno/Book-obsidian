---
title: Three Hundred Years of Longing
author: Mu Su Li
original_title: ""
status: Unread
rating:
volumes_read: 0
volumes_total: 4
genre: [Danmei, Historical, Xianxia, Fantasy]
mood: [emotional, sad, hopeful, reflective]
started:
finished:
cover: https://m.media-amazon.com/images/I/81aW05lKVFL._SL1500_.jpg
banner: https://i.pinimg.com/1200x/e0/aa/6d/e0aa6dc1dfd728b1e988f94bea460dbc.jpg
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
> Floating above the Boundless Sea is Tealspire—a towering, thirty-three-story prison built to contain fiends, where the damned are forgotten and demons waste away. At its summit, Wu Xingxue awakens with blood on his hands, chains at his feet, and no memory of how he arrived. The life he once led as a nobleman of Magpie Haven is gone, replaced by confinement and confusion.
> Disoriented and stripped of everything, Wu Xingxue is no longer a pampered aristocrat—he’s an archfiend. But fate has other plans. His awakening stirs the legendary Tianxiu Immortal, Xiao Fuxuan: a cold, enigmatic figure with the word _mian_ etched into his neck, wielding a power steeped in divine judgment.
> As Tealspire begins to collapse around them, the two must forge a reluctant alliance to survive its fall—and face whatever awaits below. Yet the mysteries only deepen. Why did Tealspire fall? What became of Wu Xingxue’s former life? And who, truly, is the Tianxiu Immortal?


