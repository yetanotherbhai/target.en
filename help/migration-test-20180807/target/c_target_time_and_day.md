---
description: Does a visitor behave differently based on the day or time? For example, is behavior different during work hours than after work hours?
seo-description: Does a visitor behave differently based on the day or time? For example, is behavior different during work hours than after work hours?
seo-title: Time of Day and Day of Week
solution: Target
title: Time of Day and Day of Week
topic: Standard
uuid: 2e87c9c3-db53-4ed4-b5cd-493474fd0c3b
index: y
internal: n
snippet: y
translate: y
---

# Time of Day and Day of Week

Select ** ` Segments` ** > ** ` Expression Targets` **, then write a script that examines the day and time. In order to use the visitor's local time, use the special * ` profile.browserTime` * variable. Note that this requires ` mbox.js` version 36 or later. Here is the strategy for work hours versus after work hours, but you can modify for your unique situation: 
Create two expression targets:
**work_hours (eg. M-F 9am-6pm):** 

```
var today = profile.browserTime; 
 
var hour = today.getHours(); 
 
var day = today.getDay(); 
 
return (day >= 1) &amp;&amp; (day <= 5) &amp;&amp; (hour >= 9) &amp;&amp; (hour <= 17);
```

**after_work:** 

```
var today = profile.browserTime; 
 
var hour = today.getHours(); 
 
var day = today.getDay(); 
 
return !((day >= 1) &amp;&amp; (day <= 5) &amp;&amp; (hour >= 9) &amp;&amp; (hour <= 17));
```

If you're not concerned with the visitor's local time, instantiate a JavaScript Date object instead. In this case, you will be using the Target server local time, which is EST, so adjust your times appropriately:
**work_hours (eg. M-F 9am-6pm):** 

```
var today = new Date(); 
 
var hour = today.getHours(); 
 
var day = today.getDay(); 
 
return (day >= 1) &amp;&amp; (day <= 5) &amp;&amp; (hour >= 9) &amp;&amp; (hour <= 17);
```

**after_work:** 

```
var today = new Date(); 
 
var hour = today.getHours(); 
 
var day = today.getDay(); 
 
return !((day >= 1) &amp;&amp; (day <= 5) &amp;&amp; (hour >= 9) &amp;&amp; (hour <= 17));
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
Once the expression targets are created, create a campaign and target the experiences accordingly. Note that you should use an experience targeting activity ("landing page campaign" in Target Classic) if your intention is for visitors to switch experiences based on the time. Otherwise, they won't switch to the ` after_work` experience if they're already in the ` work_hours` experience. 
