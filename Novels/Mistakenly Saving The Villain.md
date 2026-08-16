---
title: "{{Mistakenly Saving The Villain}}"
author: Feng Yu Nie
original_title: ""
status: Reading
rating: ⭐⭐⭐⭐
tags: []
cover: https://m.media-amazon.com/images/I/91a-oNOjgnL._SL1500_.jpg
volumes_read: 2
volumes_total: 4
translation: ""
pairing: ""
themes: []
has_donghua: false
has_manhua: false
genre: [Danmei, Xianxia, Historical, Transmigration]
mood: [funny, emotional, adventurous] 
started: 2026-02-03
finished:
synopsis: ""
my_notes: ""
banner: https://i.pinimg.com/736x/41/68/ce/4168cee567498eb2ae3bd6acb79e084a.jpg
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
> 
---
>[!synopsis]
>When medical student Song Qingshi dies and wakes up in a historical fantasy novel, he’s tasked with rescuing the tragic protagonist from a life of misery. There’s just one problem—he has no idea who the protagonist is.  
>Instead of saving the hero, Song Qingshi accidentally rescues Yue Wuhuan, an enslaved man renowned for his striking beauty and trained in the art of seduction. Now determined to help his traumatized new patient heal, Song Qingshi offers everything he can: Medicine, therapy, emotional support, even a shared bed—strictly for his patient’s well-being, of course.  
>But Yue Wuhuan wants more than healing. He wants revenge. And most of all, he wants Song Qingshi all to himself.



---

### Short Summary to catch up again
- SQ was in a coma for 10 years while YW developed new techniques to save him (Blood King Vines and Devil Mask Snake Venom)
- he now wears a golden mask in public to hide the venoms effects
- An Long finds this very sus and sends letters to the valley
- He eventually comes to the valley and him and YW have a beef
- To stop them from killing each other, SQ proposes on going on vacation together
- During that, YW is plotting to eliminate every threat to his beloved SQ
- YW is manipulating An Long into thinking he killed SQ and that he will never forgive him

- in the end, SQ asks YW if they are only friends or more