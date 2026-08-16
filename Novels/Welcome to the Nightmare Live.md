---
title: "Welcome to the Nightmare Live"
author: "桑沃 (Sāng Wò)"
original_title: "欢迎进入梦魇直播间"
status: Unread
rating: ""
volumes_read: 0
volumes_total: 1
genre:
  - Danmei
  - Infinite Flow
  - Horror
  - Thriller
  - Survival Game
cover: https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRDAaPmKqVMwl4carSEYjo0cPD_V9Zs05VjAgK3-ifbn3XsovC0KAx6MGg&s=10
mood: []
started: 
finished: ""
statuspub: Ongoing (CN, text under revision)
en_published: 0
pairing: "Wen Jianyan x ???"
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
> Wen Jianyan is a professional fraudster, best at saying whatever people—or ghosts—want to hear. 
> One day, he is suddenly forced to become a rookie streamer in the Nightmare Livestream, a deadly broadcast where failure means real death. 
> Determined to survive, Wen Jianyan decides to weaponize his only true talent: lying. 
> He scams teammates, viewers, NPCs, even evil spirits, turning every dungeon into a stage where he twists rules, breaks the system, and walks away alive while everyone waits for the day he finally crashes and burns. 
> But as the missions grow stranger and more dangerous, and high-level tasks start involving intimate “interactions” with ghosts and eldritch beings, Wen Jianyan realizes that some existences behind the screen are very real—and one terrifying “top boss” seems intent on turning a fake CP into something far more dangerous. 

## My Notes

## Characters

## Quotes
