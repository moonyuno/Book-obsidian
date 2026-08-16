---
title: "{{Ballad of Sword and Wine}}"
author: Tang Jiu Qing
original_title: ""
status: Unread
rating:
volumes_read: 0
volumes_total: 8
genre: [Danmei, Historical, Political, Wuxia]
mood: [dark, emotional, tense, mysterious]
started:
finished:
en_published: 7
statuspub: ongoing
banner: https://i.imgur.com/6amilOc.png
cover: https://images.thalia.media/-/BF2000-2000/39e69429247547a09402abe46c631f8d/ballad-of-sword-and-wine-qiang-jin-jiu-novel-vol-1-taschenbuch-tang-jiu-qing-englisch.jpeg
---

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


>[!synopsis] Synopsis
>Shen Zechuan is the eighth son of the traitorous Prince of Jianxing, a man who doomed his cities and people to destruction at the hands of the foreign enemy. As the only surviving member of his reviled line, Shen Zechuan is dragged to the capital in chains. He bears the hatred of the nation, but no one's hate burns hotter than that of Xiao Chiye, the youngest son of the powerful Prince of Libei.  
>Xiao Chiye would love nothing more than to see Shen Zechuan dead--but against all odds, he clings to life. Rather than succumb to his family's disgrace, he becomes a thorn in Xiao Chiye's side, clawing his way into the cutthroat political world of the capital. Yet as these two bitter enemies beat against the bonds of their fate, they find themselves kindred spirits, unlikely allies...and perhaps something more.
## My Notes

## Characters

## Quotes
