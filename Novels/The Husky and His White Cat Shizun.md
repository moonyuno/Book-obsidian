---
title: "{{The Husky and His White Cat Shizun}}"
author: Rou Bao Bu Chi Rou
original_title: ""
status: Finished
rating: ⭐⭐⭐⭐⭐
tags: []
cover: https://m.media-amazon.com/images/I/91E1N-SMGgL._SL1500_.jpg
volumes_read: 11
volumes_total: 11
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre:
  - Danmei
  - Xianxia
  - Historical
  - Rebirth
mood:
  - emotional
  - dark
  - sad
  - tense
started: 2026-04-06
finished: 2026-06-20
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/1200x/33/6b/7a/336b7abae28e9ce3ee3b2583293bc254.jpg
en_published: 11
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
>Cruel tyrant Taxian-jun killed his way to the throne and now reigns as the first ever emperor of the mortal realm. Yet somehow, he is unsatisfied. Left cold and bereft, abandoned by all he held dear, he takes his own life...only to be reborn anew.  
>Awakening in the body of his younger self--Mo Ran, a disciple of the cultivation sect Sisheng Peak--he discovers the chance to relive his life. This time, he vows to attain the gratification that once eluded him: all who defied him will fall, and never again will they treat him like a dog. His greatest fury is reserved for Chu Wanning, the coldly beautiful and aloofly catlike cultivation teacher who betrayed and thwarted Mo Ran time and again in their last life.  
>Yet as Mo Ran shamelessly pursues his own goals in this life he thought lost, he begins to wonder if there might be more to his teacher--and his own feelings--than he ever realized.


