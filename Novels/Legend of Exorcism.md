---
title: "{{Legend of Exorcism}}"
author: Fei Tian Ye Xiang
original_title: ""
status: Unread
rating:
genre: [Danmei, Historical, Fantasy, Xianxia]
mood: [adventurous, emotional, funny]
started:
finished:
tags: []
cover: https://m.media-amazon.com/images/I/81uab24yjLL._SL1500_.jpg
volumes_read: 0
volumes_total: 8
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/1200x/5b/9d/53/5b9d538c34c725e217283fe9f6bde249.jpg
en_published: 5
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
> 
>[!synopsis]
>In the mystical Taihang Mountains, where magic flows and powerful yao roam, Hongjun has grown up sheltered from the human world. A half-yao himself, he’s never had reason to leave—until the mountain’s ruler sends him on a dangerous mission: hide his true nature and join the Great Tang Department of Demonic Exorcism in Chang’an.  
>Upon arriving in the bustling capital, Hongjun meets Li Jinglong, a luckless soldier with no spiritual power tasked with leading a team of extraordinary exorcists. Together, they and their enigmatic companions must face the dark forces threatening the city. But as a bond begins to bloom between Hongjun and Li Jinglong, Hongjun wonders: Can he trust Li Jinglong with the truth of who—and what—he is?



