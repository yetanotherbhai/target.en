---
description: If a month has gone by since a shopper bought a pack of 30-day disposable contact lenses, maybe it's time to offer it at a discount.
keywords: Targeting
seo-description: If a month has gone by since a shopper bought a pack of 30-day disposable contact lenses, maybe it's time to offer it at a discount.
seo-title: Recency of Purchase, Visit, Photo Upload, Etc.
solution: Target
title: Recency of Purchase, Visit, Photo Upload, Etc.
uuid: 93ff8581-4847-4d6d-961a-71bbe60b003c
index: y
internal: n
snippet: y
translate: y
---

# Recency of Purchase, Visit, Photo Upload, Etc.

How about reminding a user who hasn't uploaded a photo to your site in three weeks that their gallery is getting stale?
For a profile attribute, write a script that calculates how many days elapsed since the last conversion. A conversion doesn't have to be a purchase. It could be uploading a video, visit to a lead generation form, etc. You'll then reference the script profile parameter in several expression targeters (target tab), which will be used in the campaign edit page. Note that the " ` new Date()`" function brings back time in EDT. Here is the script: 

```
user.recency 
 
if (mbox.name == 'orderThankyouPage') { 
 
   user.setLocal('lastPurchaseTime', new Date().getTime()); 
 
} 
 
if (mbox.name == 'someMbox') { 
 
   var lastPurchaseTime = user.getLocal('lastPurchaseTime'); 
 
   if (lastPurchaseTime) { 
 
      return ((new Date()).getTime()-lastPurchaseTime) / (3600 * 24 * 1000); 
 
   } 
 
}
```

Create some expression targets:

```
no_purchases: 
return typeof(user.get('recency')) == 'undefined'; 
 
within_1day: 
return user.get('recency') < 1; 
 
within_1week: 
return user.get('recency') >= 1 &amp;&amp; user.get('recency') < 7; 
 
within_1month: 
return user.get('recency') >= 7 &amp;&amp; user.get('recency') < 31; 
 
over_1month: 
return user.get('recency') >= 31
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
