---
title: "{{Grandmaster of Demonic Cultivation}}"
author: Mo Xiang Tong Xiu
original_title: Mo Dao Zu Shi
status: Finished
rating: ⭐⭐⭐⭐⭐
tags: []
cover: https://m.media-amazon.com/images/I/81eIhgXI90L._SL1500_.jpg
volumes_read: 5
volumes_total: 5
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre: [Danmei, Xianxia, Historical]
mood: [emotional, adventurous, dark, funny]
started: 2022-03-01
finished: 2022-07-01
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/1200x/cb/c2/3a/cbc23aecb0b22815b9c810a6a069a793.jpg
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
>Wei Wuxian was once one of the most outstanding men of his generation, a talented and clever young cultivator who harnessed martial arts, knowledge, and spirituality into powerful abilities. But when the horrors of war led him to seek a new power through demonic cultivation, the world's respect for his skills turned to fear, and his eventual death was celebrated throughout the land.  
  >Years later, he awakens in the body of an aggrieved young man who sacrifices his soul so that Wei Wuxian can exact revenge on his behalf. Though granted a second life, Wei Wuxian is not free from his first, nor the mysteries that appear before him now. Yet this time, he'll face it all with the righteous and esteemed Lan Wangji at his side, another powerful cultivator whose unwavering dedication and shared memories of their past will help shine a light on the dark truths that surround them.
  



---