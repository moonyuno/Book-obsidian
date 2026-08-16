---
title: Panguan
author: Mu Su Li
original_title: ""
status: Unread
rating: ""
volumes_read: 0
volumes_total: 4
genre: [Danmei, Modern, Historical, Supernatural, Cultivation]
cover: https://sevenseasentertainment.com/wp-content/uploads/2025/09/panguanDN1_coverFRONT.jpg
mood: [mysterious, emotional, dark, hopeful]
started: 
finished: ""
statuspub: licensed
en_published: 0

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
> As a panguan, a cultivator tasked with putting the dead to rest, Wen Shi has spent a thousand years sending souls on to their next life. But without a soul of his own, he’s trapped in an endless cycle of rebirth, desperately searching for the lost pieces of himself.
Now, reborn for the twelfth time, he feels a constant hunger that can only be satisfied by consuming the dark miasma that clings to the dead. So when failed panguan Xie Wen responds to Wen Shi’s ad for a roommate, Wen Shi is taken aback by the dense miasma cloaking the handsome young man. Smug and irritating, Xie Wen instantly becomes Wen Shi’s most tempting meal. Yet the longer Wen Shi spends with Xie Wen, the more mysterious he seems. Xie Wen appears to know things about Wen Shi even Wen Shi has forgotten—things that could end his millennium of lonely wandering.

## My Notes

## Characters

## Quotes
