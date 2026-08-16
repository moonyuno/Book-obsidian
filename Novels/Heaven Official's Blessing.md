---
title: "{{Heaven Official's Blessing}}"
author: Mo Xiang Tong Xiu
original_title: "`天官赐福`"
genre: [Danmei, Xianxia, Historical, Fantasy]
mood: [emotional, adventurous, sad, hopeful]
rating: ⭐⭐⭐
cover: https://m.media-amazon.com/images/I/91XkwAUMy8L._SL1500_.jpg
status: On Hold
volumes_read: 3
volumes_total: 8
started: 2023-03-01
finished:
banner: https://i.pinimg.com/1200x/31/eb/31/31eb31f9db5914d9ce301f9ad69fb917.jpg
en_published: 8
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
>Born the crown prince of a prosperous kingdom, Xie Lian was renowned for his beauty, strength, and purity. His years of dedicated study and noble deeds allowed him to ascend to godhood. But those who rise may also fall, and fall he does--cast from the heavens and banished to the world below.  
>Eight hundred years after his mortal life, Xie Lian has ascended to godhood for the third time, angering most of the gods in the process. To repay his debts, he is sent to the Mortal Realm to hunt down violent ghosts and troublemaking spirits who prey on the living. Along his travels, he meets the fascinating and brilliant San Lang, a young man with whom he feels an instant connection. Yet San Lang is clearly more than he appears... What mysteries lie behind that carefree smile?


