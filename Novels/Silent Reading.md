---
title: "{{Silent Reading}}"
author: priest
original_title: ""
status: Unread
rating:
tags: []
cover: https://m.media-amazon.com/images/I/81vkCuQcLdL._SL1500_.jpg
volumes_read: 0
volumes_total: 6
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre: [Danmei, Modern, Mystery, Thriller]
mood: [mysterious, emotional, dark, tense]
started:
finished:
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/736x/8a/02/5b/8a025ba4cd8e0e9ac61515932b3ce9d8.jpg
en_published: 3
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
>A young man’s body is found outside a glitzy high-rise on the West Side of Yancheng—dressed for celebration, strangled, and left with a sheet of paper covering his face. One word is scrawled across it: money.  
>To Sergeant Luo Wenzhou, head of the Criminal Investigation Team at the Yancheng Municipal Public Safety Bureau, it’s just another case in a city rife with power plays and buried secrets. But as he digs deeper with his team, what begins as a straightforward homicide unravels into something far murkier—reaching into the city’s darkest corners of wealth, privilege, and police corruption.  
>And then there’s Fei Du: the aloof, razor-sharp CEO of the Fei Corporation, who seems to know far too much about the murder—and about Luo Wenzhou himself. Once a troubled youth with ties to Luo Wenzhou’s past, Fei Du now walks a fine line between brilliant ally and inscrutable suspect. His insights are disturbingly precise. His motives? Frustratingly opaque.  
>As the investigation twists through layers of trauma and moral ambiguity, Luo Wenzhou finds himself reluctantly drawn toward the very man who unsettles him most. But in a city where justice is easily bought and truth wears many masks, can either man afford to trust the other?


