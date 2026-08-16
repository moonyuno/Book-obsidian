---
title: "{{Stars of Chaos}}"
author: priest
original_title: Sha Po Lang
status: Unread
rating:
tags: []
cover: https://m.media-amazon.com/images/I/81rKG80HGqL._SL1500_.jpg
volumes_read: 0
volumes_total: 5
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre: [Danmei, Historical, Political, Fantasy]
mood: [emotional, adventurous, tense, dark]
started:
finished:
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/736x/e8/67/27/e86727d2baa75ec256e8527a524c2e5f.jpg
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


---
>[!synopsis]
>The discovery of violet gold, a vital fuel for steam-powered machines, propelled the empire of Great Liang into an age of prosperity. But for Chang Geng, a young man raised on the impoverished northern border, the concerns of the empire are as distant as the stars above.  
>When raiders from the north attack Chang Geng’s small village, he discovers that the life he knows is a lie. His mother, his teacher, and even his godfather whom he trusted more than any other, Shen Shiliu, are not what they seem. As enemy nations close in, Chang Geng follows his godfather to the heart of the imperial capital, where a greater fate lies in store for him.



