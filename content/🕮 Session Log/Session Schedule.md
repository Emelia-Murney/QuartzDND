---
title: Session Schedule
tags:
  - Session
---
## Overview

A list of all sessions and when they took place can be viewed below. It will link to the individual session's notes.

```dataviewjs
let pages = dv.pages('"content/🕮 Session Log/Sessions"');
let values = [];
for (let i = 0; i < pages.length; i++) {
	values.push(pages[i]);
}
values.sort((a,b)=> Number(a.file.name.split(" ")[1])-Number(b.file.name.split(" ")[1]));
for (let i = 0; i < pages.length; i++) {
	let page = values[i];
	const myDateTime = DateTime.fromSeconds(Number(page.Date) / 1000);
	dv.span("- [[" + page.file.name + "]]: " + page.subtitle + " --- " + myDateTime.setLocale('en').toLocaleString(DateTime.DATE_HUGE));
}
```

- [[Session 0]]: `$= dv.page("Session 0").subtitle` --- `$= dv.page("Session 0").Date`
- [[Session 1]] --- 7th December 2024
- [[Session 2]] --- 13th December 2024
- [[Session 3]] --- 10th January 2025
- [[Session 4]] --- 16th January 2025
- [[Session 5]] --- 24th January 2025
- [[Session 6]] ---  
- [[Session 7]] --- 
- [[Session 8]] --- 1st March 2025
- [[Session 9]] --- 8th March 2025