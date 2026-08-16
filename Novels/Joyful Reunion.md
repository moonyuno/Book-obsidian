---
title: "{{Joyful Reunion}}"
author: Fei Tian Ye Xiang
original_title: ""
status: Unread
rating:
genre: [Danmei, Historical, Wuxia]
mood: [emotional, tense, dark]
started:
finished:
tags: []
cover: https://m.media-amazon.com/images/I/81jbcM5qmYL._SL1500_.jpg
volumes_read: 0
volumes_total: 6
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/1200x/a9/bf/42/a9bf427fd42bd3b27ffa421470e3c098.jpg
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


>[!synopsis]
>For as long as he can remember, Duan Ling has been an unwanted child. Raised by his deceased mother’s neglectful family, he’s grown up battered and mistreated. But his life takes a fateful turn when a stranger named Lang Junxia arrives at the Duan estate, claiming to be sent by the father Duan Ling never knew he had.  
>Whisked away to the capital of the Liao Empire, Duan Ling is thrust into a treacherous world of political intrigue and power struggles far beyond his comprehension. But Lang Junxia has promised his father will come for him, and Lang Junxia never lies.  
>As he prepares for a destiny greater than he ever imagined, Duan Ling finds himself at the heart of a story that could alter the fate of empires—and shake the world itself.






