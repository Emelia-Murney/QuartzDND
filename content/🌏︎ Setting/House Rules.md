---
title: House Rules
tags:
  - HouseRule
---
Here is a list of all the house rules:
```dataviewjs
let pages = dv.pages('"content/🌏︎ Setting/House rules"');
for (let i = 0; i < pages.length; i++) {
	let page = pages[i];
	dv.span("- [[" + page.file.name + "]]");
}
```


