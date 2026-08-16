---
title: "{{Peerless}}"
author: Meng Xi Shi
original_title: ""
status: Unread
rating:
tags: []
cover: https://m.media-amazon.com/images/I/81eZxMJZQJL._SL1500_.jpg
volumes_read: 0
volumes_total: 5
translation: ""
pairing: ""
themes: []
genre: [Danmei, Historical, Wuxia, Mystery]
mood: [mysterious, tense, emotional, dark]
started:
finished:
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/736x/17/8d/ef/178defc530dea3ba0873ff57dc76c7c1.jpg
en_published: 5
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
>On a snowy night, an envoy sent by the Kingdom of Khotan is ambushed on the road, massacred with his escort. Not a living soul remains, and the attackers vanish—along with a precious jade intended as tribute to the Emperor of Sui. A member of the emperor’s secret intelligence agency, the Jiejian Bureau, pursues the case: the formidable deputy chief, Feng Xiao. His investigation takes him to Liugong City, where top martial artists from across the land gather for a mysterious auction.  
>But a rival intelligence agency, the Zuoyue Bureau, has business in the same city—and they have sent Cui Buqu, an ailing but brilliant man who hides more secrets than even Feng Xiao. Equally proud, the two immediately clash in a battle of wits, but neither can crack the case alone. To solve the mystery before the trail goes cold, they will have to join hands to uncover the truth…however unwillingly.





