---
title: "{{Guardian}}"
author: priest
original_title: ""
status: Unread
rating:
genre: [Danmei, Modern, Urban Fantasy, Mystery]
mood: [mysterious, emotional, dark]
started:
finished:
tags: []
cover: https://images.thalia.media/-/BF2000-2000/76873bd770a046c2b31ca3a06d006369/guardian-zhen-hun-novel-vol-1-taschenbuch-priest-englisch.jpeg
volumes_read: 0
volumes_total: 3
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/736x/8c/53/5b/8c535b1d5f74e9d6b4bc848b6ecbd8b3.jpg
en_published: 3
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
>Zhao Yunlan heads up a covert division of the Ministry of Public Security that deals with the strange and unusual, blurring the line between the mortal realm and the Netherworld. His cocky, casual attitude conceals both a sharp mind and an arsenal of mystical tools and arcane knowledge.  
>While investigating a gruesome death at a local university, Zhao Yunlan crosses paths with the reserved Professor Shen Wei. Zhao Yunlan is immediately intrigued by Shen Wei’s good looks and intense gaze, and the attraction between them is immediate and powerful, even as Shen Wei tries to keep his distance. Shen Wei and his secrets are a puzzle Zhao Yunlan feels compelled to solve as mysterious circumstances throw them together, and their connection becomes impossible to deny.




