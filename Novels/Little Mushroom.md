---
title: "{{Little Mushroom}}"
author: Shisi
original_title: ""
status: Unread
rating:
tags: []
cover: https://images.thalia.media/-/BF2000-2000/2fcf2d5b75754baea83237b394f0f156/little-mushroom-wrong-but-still-right-1-taschenbuch-yishisizhou.png
volumes_read: 0
volumes_total: 2
translation: ""
pairing: ""
themes: []
has_donghua: false
genre: [Danmei, Sci-Fi, Post-Apocalyptic]
mood: [dark, emotional, sad]
started:
finished:
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/1200x/48/ff/19/48ff191ec07197e51e8a70d204e78506.jpg
en_published: 0
statuspub: upcoming
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
> 
>[!synopsis]
>In the year 2020, humanity was nearly wiped out by cosmic radiation. Over the next one hundred years, living creatures began to change and mutate while the remaining humans struggled to survive in man-made bases.  
>Down in the Abyss, a home to mutated xenogenics, there lived a sentient mushroom. Nourished by the flesh and blood of the deceased An Ze, the mushroom took on the form of its host and even adopted a similar name: An Zhe. Seeking his missing spore, harvested by humans, An Zhe is determined to make it to the human base to retrieve what’s his. But the closer he gets to the base, the higher his risk of death increases. Unfortunately for An Zhe, there are those who prowl the streets seeking xenogenics like himself—known as Judges, they inspect and eliminate non-humans without a second thought, sparing no one. And when An Zhe finds himself under the scrutiny of Colonel Lu Feng—the most perceptive and merciless of the Judges—he somehow goes undetected but not unsuspected. Lu Feng knows there’s something off about An Zhe and he’s not letting him out of his site until he figures it out.



