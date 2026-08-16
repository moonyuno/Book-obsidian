---
title: "{{The Disabled Tyrant's Beloved Pet Fish}}"
author: Xue Shan Fei Hu
original_title: Canji Baojun De Zhangxin Yu Chong
status: Unread
rating:
tags: []
cover: https://images.thalia.media/-/BF2000-2000/2c9adf7856c744328d3cface8ce2820a/the-disabled-tyrant-s-beloved-pet-fish-canji-baojun-de-zhangxin-yu-chong-novel-vol-1-taschenbuch-xue-shan-fei-hu-englisch.jpeg
volumes_read: 0
volumes_total: 4
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre:
  - Danmei
  - Historical
  - Fantasy
  - Transmigration
mood:
  - funny
  - emotional
  - lighthearted
started: 
finished:
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/1200x/7f/ac/f2/7facf26783d95983838d281709bebc8f.jpg
en_published: 4
statuspub: finished
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
>After Li Yu _stays_ up all night to read an engrossing webnovel, he finally falls asleep–only to wake up in the world of the novel itself. And not as himself, but as a helpless fish! Shocked and dismayed, Li Yu quickly realizes that he must live in a tank owned by Mu Tianchi, the tyrant of the novel who never speaks. Whatever force brought Li Yu into this world warns him that there’s only one way to become human again: to win over the cold Mu Tianchi and change his harsh ways. But Li Yu has no idea how to do that, especially as a powerless, palm-sized carp. Can a little fish really swim its way into a tyrant’s heart?


