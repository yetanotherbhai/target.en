---
description: You can track the number of times a single visitor visits your site.
seo-description: You can track the number of times a single visitor visits your site.
seo-title: Number of Visits
solution: Target
title: Number of Visits
topic: Standard
uuid: 89048c96-b31a-43e8-b337-2e8ad419bbba
index: y
internal: n
snippet: y
translate: y
---

# Number of Visits

For a profile attribute, write a script to increment a counter whenever a new session is recognized. You'll then reference the script profile parameter in several expression targeters (target tab), which will be used in the campaign edit page. Here is the script:

```
user.numVisits 
 
if(user.sessionId!=user.getLocal('lastSessionId')) { 
 
   user.setLocal('lastSessionId', user.sessionId); 
 
   return (user.get('numVisits') || 0) + 1; 
 
} 
```

Create five expression targets (you may choose more):

```
0visits: 
return typeof(user.get('numVisits')) == 'undefined'; 
 
1visit: 
return user.get('numVisits') == 1; 
 
2to9visits: 
return user.get('numVisits') > 1 &amp;&amp; user.get('numVisits') < 10; 
 
10to19visits: 
return user.get('numVisits') >= 10 &amp;&amp; user.get('numVisits') < 20; 
 
over20visits: 
return user.get('numVisits') >= 20;
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
