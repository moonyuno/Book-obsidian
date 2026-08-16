---
title: There's Something Wrong With the Chief
author: Yang Su
original_title: ""
status: Unread
rating: ""
volumes_read: 0
volumes_total: 4
genre: [Danmei, Historical, Political]
cover: https://sevenseasentertainment.com/wp-content/uploads/2024/10/govSickDN1_coverFRONT.jpg
mood: [emotional, tense, dark, adventurous]
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
> Xiahou Lian, the youngest assassin of the infamous Qiye Garden enclave, has infiltrated the prestigious Xie household on a vague but deadly mission. Posing as a servant under Xie Jinglan, the youngest son of the family, he bides his time, awaiting orders. But as the days pass, an unexpected bond forms between them—mark and assassin alike—throwing a wrench in Xiahou Lian’s plans. The decision he makes will land him in dire straits with the Qiye Garden, while Xie Jinglan walks free.
> Two years later, their paths cross again in the Imperial Palace. Forced to walk a perilous tightrope of secrecy, both boys hide dangerous truths from one another. Something is terribly wrong, and they can both feel it. As one of those secrets spirals into mortal danger, an assassin from Qiye Garden—familiar and fearsome—arrives with an ultimatum that threatens to tear their fragile bond apart.

## My Notes

## Characters

## Quotes
