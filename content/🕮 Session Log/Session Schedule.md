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
const dateMap = new Map();
for (let i = 0; i < pages.length; i++) {
	values.push(pages[i]);
}
values.sort((a,b)=> Number(a.file.name.split(" ")[1])-Number(b.file.name.split(" ")[1]));
for (let i = 0; i < pages.length; i++) {
	let page = values[i];
	const myDateTime = DateTime.fromSeconds(Number(page.Date) / 1000);
	if (dateMap.has(myDateTime.weekdayLong)) {
		dateMap.set(myDateTime.weekdayLong, dateMap.get(myDateTime.weekdayLong)+1);
	} else {
		dateMap.set(myDateTime.weekdayLong, 1);
	}
	dv.span("- [[" + page.file.name + "]]: " + page.subtitle + " --- " + myDateTime.setLocale('en').toLocaleString(DateTime.DATE_HUGE));
}
dv.span("");
dv.span("The number of sessions to take place on a day of the week is:");
for (const [key, value] of dateMap) { 
	dv.span("- " + key + ": " + value);
}
```
