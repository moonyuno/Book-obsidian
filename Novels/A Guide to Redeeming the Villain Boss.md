---
title: "A Guide to Redeeming the Villain Boss"
author: "Shan Jiu"
original_title: "反派boss救赎指南"
status: Unread
rating: ""
volumes_read: 0
volumes_total: 1
genre:
  - Danmei
  - Xianxia
  - Fantasy
  - Transmigration
  - Romance
  - Drama
  - Adventure
mood: []
started: 
finished: ""
statuspub: not licensed
en_published: 0
pairing: "Fu Pianlou x Xie Zheng"
cover: "https://daosearch.io/img/cover/c740f80f79feb544c504/360/aHR0cHM6Ly9pNi1zdGF0aWMuamp3eGMubmV0L3RtcC9iYWNrZW5kL2F1dGhvcnNwYWNlL3MxLzUzLzUyMjkxLzUyMjkwNjgvMjAyMzEyMTYwNDU2NTBfMzAwXzQyMC5qcGc.jpg"
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
> Xie Zheng is abruptly dragged into a cultivation novel called *Wendao* and informed that he has been selected by System 011 for a very important mission.
>
> Somewhere in this world is Fu Pianlou, the future villain boss destined to blacken completely and eventually destroy everything around him.
>
> Xie Zheng's assignment is simple: travel back to Fu Pianlou's childhood, rescue him from his miserable fate, shower him with love and become the salvation that prevents him from ever turning into the villain.
>
> Xie Zheng has another proposal.
>
> Why not simply kill him now?
>
> The system refuses.
>
> Fine. Then Xie Zheng will raise him badly enough that he never becomes powerful enough to destroy the world.
>
> Unfortunately, Fu Pianlou has a secret of his own. A demon dwelling within his unusual left eye has told him that this is already his eleventh lifetime. Every time, someone appears when he is thirteen, treats him with impossible tenderness and claims to care for him—because that person has been sent to complete a mission.
>
> This time, Fu Pianlou is determined not to be fooled.
>
> So when Xie Zheng rescues him from human traffickers, Fu Pianlou waits suspiciously for the inevitable gentle reassurance.
>
> Instead, Xie Zheng informs him that he owns his contract now and expects obedience.
>
> When they begin living together, Fu Pianlou assumes the hardship must be an elaborate attempt to lower his guard.
>
> Then he discovers Xie Zheng contemplating whether killing him might still be easier.
>
> And when Fu Pianlou finally reveals that he knows all about the mysterious system supposedly controlling their relationship, Xie Zheng simply drags System 011 out and tells the two of them to sort it out themselves.
>
> Somewhere between cultivation, repeated lives, suspicious motives and Fu Pianlou's increasingly elaborate misunderstandings, the straightforward redemption mission begins to unravel.
>
> Because Fu Pianlou has spent lifetime after lifetime believing that every kindness shown to him must have an ulterior motive—and Xie Zheng may be the first person who refuses to treat him like either a predetermined villain or a fragile creature waiting to be saved.

## My Notes

## Characters

## Quotes