---
title: "{{Run Wild}}"
author: "Wu Zhe"
original_title: "Saye"        # chinesischer Originaltitel
status: "Unread"       # Ungelesen / Am Lesen / Gelesen / Dropped
rating: 
volumes_read: 0
volumes_total: 6
genre:
mood: 
started:
finished:
cover: https://sevenseasentertainment.com/wp-content/uploads/2024/06/runWildDN1_coverFRONT.jpg   
banner: https://i.pinimg.com/736x/cd/5a/23/cd5a2341356ccdca08ac082e9fa6662c.jpg
en_published: 5
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

> [!synopsis] Synopsis
> Unwanted by his adoptive parents, Jiang Cheng leaves home to live in a cold, gray city with his deadbeat dad whose only talent is feeding a gambling addiction. Alone save for his suitcase, the rebellious teenage boy arrives at the train station ready to face his miserable new life.
> But the moment he steps off the platform, Jiang Cheng meets the peculiar young girl Gu Miao, along with her big brother Gu Fei—a boy his age with a musical staff shaved into his hair. Rumor has it that Gu Fei is bad news with dark secrets of his own, but Jiang Cheng still finds himself pulled toward the withdrawn delinquent thanks to Gu Miao and, perhaps, fate. The unlikely friendship that blossoms between them shows Jiang Cheng the hidden depths of Gu Fei…and the hidden depths of his own feelings. Features exclusive new art!





