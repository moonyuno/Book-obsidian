---
title: Thrice Married to a Salted Fish
author: Bi Ka Bi
original_title: ""
status: Unread
rating: ""
volumes_read: 0
volumes_total: 4
genre: [Danmei, Historical, Political, Transmigration]
cover: https://sevenseasentertainment.com/wp-content/uploads/2024/10/married_thrice_DN1_coverFRONT.jpg
mood: [emotional, funny, tense, reflective]
started: 
finished: ""
statuspub: ongoing
en_published: 3

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
> Ten years of exhaustive study, tedious research, and sleepless nights have suddenly been rendered meaningless for aspiring Imperial Physician Lin Qingyu. In the midst of his work, he receives instructions to put everything aside and marry Lu Wancheng, the sickly son of the marquis—all in the hopes that this sacred union will heal the illness that plagues the young master.
> However, Lin Qingyu quickly discovers that Lu Wancheng isn’t just an ill-fated aristocrat—in fact, the man has a mysterious twinkle in his eye, and insights that could help Lin Qingyu outmaneuver even royalty. With that, Lu Wancheng proposes an idea to his new male bride, one that will help send Lin Qingyu back home to continue his studies and fulfill his dreams.
> As feelings bloom between these new allies, a dark truth looms over their tenuous bond—one that threatens to rip them apart in both sickness and health.

## My Notes

## Characters

## Quotes
