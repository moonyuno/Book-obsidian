---
title: "{{Nan Chan}}"
author: Tang Jiu Qing
original_title: ""
status: Unread
rating: 
tags: []
cover: https://www.danmeinews.com/wp-content/uploads/2023/07/Untitled-4.jpg
volumes_read: 0
volumes_total: 3
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre: [Danmei, Xianxia, Historical, Mystery]
mood: [dark, emotional, mysterious, sad]
started:
finished:
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/1200x/1f/a6/ff/1fa6ff71a48cb2c49c71175163e71f10.jpg
en_published: 2
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

>[!synopsis]
>A disgraced immortal thought long dead. A shape-shifting fish with a mind of its own. A cryptic copper bell that seems to lead them on a wild goose chase—or is it something more?
>After committing patricide against the Supreme Father, Jinglin is annihilated for his betrayal, but instead of fading into oblivion, he awakens—weak and diminished—in a secluded courtyard. His only companions: a mysterious bell, a silent stone figure, and a talking fish that soon transforms into a child whom he names Cangji.
>When the bell is lost during an attack on their quiet abode, Jinglin and Cangji set off to retrieve it. The trail it leaves behind winds through a series of puzzling, harrowing cases—each one embodying a different form of human suffering. As the mysteries deepen, so do the questions: What is the bell’s true purpose? Why has it chosen this path? And what awaits them at the end of the journey?
>Follow Jinglin and Cangji as they unravel a tapestry of memories, desires, and intrigue in a quest for the truth that may be better never uncovered…
>_“I have experienced all the eight sufferings of the world._  
>_I do not ask for nirvana, but for you.”_





---