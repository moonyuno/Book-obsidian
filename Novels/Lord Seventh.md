---
title: "Lord Seventh"
author: "Priest"
original_title: "七爷"
status: Unread
rating: ""
volumes_read: 0
volumes_total: 1
genre:
  - Danmei
  - Historical
  - Fantasy
  - Reincarnation
  - Political Intrigue
  - Romance
  - Drama
mood: []
started: ""
finished: ""
statuspub: Completed
en_published: 0
pairing: "Jing Beiyuan x Wu Xi"
cover: "https://lordseventhby7.carrd.co/assets/images/gallery01/cd0e830a_original.jpg?v=117caabd"
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
> Jing Beiyuan has already died six times.
>
> Across six different lives, his fate has repeatedly revolved around the same person: Helian Yi, the man he loved, supported and helped ascend the throne—and the man whose path to power ultimately ended with Jing Beiyuan's death.
>
> When he is given a seventh life, Jing Beiyuan unexpectedly awakens once again in his original body, years before everything went wrong.
>
> This time, however, he remembers.
>
> He remembers the court, the conspiracies, the people who will betray one another and the bloody struggle that will eventually determine who inherits the throne. More importantly, after six lifetimes of devotion and disappointment, Jing Beiyuan is finally tired.
>
> He has no intention of repeating the same love story again.
>
> Unfortunately, knowing the future does not mean he can simply escape it.
>
> Still a young prince trapped within the capital's political web, Jing Beiyuan must once again navigate competing princes, imperial schemes, assassinations and the increasingly dangerous struggle surrounding Helian Yi's rise to power. Outwardly, he maintains the image of an idle, pleasure-loving nobleman who would rather drink and sleep than involve himself in politics. Beneath it, he is far older, colder and more calculating than anyone around him realizes.
>
> Then Wu Xi enters his life.
>
> Wu Xi is the young heir of Nanjiang, sent to the capital as a political hostage. Proud, straightforward and fiercely loyal, he is almost painfully sincere in a world where Jing Beiyuan has learned to distrust nearly everything.
>
> What begins as an unlikely connection slowly becomes something Jing Beiyuan has not experienced in any of his previous lives: a relationship that is not built around sacrifice for someone destined to become emperor.
>
> But letting go of six lifetimes is not simple, and neither is surviving the seventh.
>
> Against a backdrop of succession struggles, political manipulation, war and old debts, Jing Beiyuan must decide whether this life will merely become another variation of the same tragedy—or whether, for once, he can choose to live it for himself.

## My Notes

## Characters

### Jing Beiyuan

### Wu Xi

### Helian Yi

## Quotes
