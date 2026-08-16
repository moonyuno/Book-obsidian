---
title: "Codename: Anastasia"
author: "Boy Season"
original_title: "코드네임 아나스타샤"
status: Unread
rating: ""
volumes_read: 0
volumes_total: 1
genre:
  - Korean Novel
  - BL
  - Spy Thriller
  - Action
  - Modern
cover: https://cdn.thestorygraph.com/koeg0jjutys41gdm8bkif0th2z9n
mood: []
started: 
finished: ""
statuspub: Completed
en_published: 0
pairing: "Kwon Taekjoo x Zhenya"
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



> [!synopsis] Synopsis
> NIS ace agent Kwon Taekjoo is dispatched from South Korea to Moscow on a high-risk mission. 
> His objective: uncover the identity and location of “Anastasia,” a deadly weapon born from a secret collaboration between Russia and North Korea—a project capable of reshaping global power. 
> To assist him, Taekjoo is assigned a local partner known only as Zhenya, a man whose connections range from Russian politicians and business elites to the underworld mafia.
> Zhenya’s easygoing, cheerful demeanor clashes violently with his sudden bursts of brutality, leaving Taekjoo constantly on edge and unsure whether to trust him. 
> As the operation spirals out of control and enemies close in, the line between ally and threat blurs, and Taekjoo finds himself increasingly entangled not only in international conspiracy—but in the dangerous, magnetic pull of Zhenya himself. 

## My Notes

## Characters

## Quotes