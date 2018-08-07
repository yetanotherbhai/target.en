---
description: If user intent is demonstrated by action, then repeated action increases confidence in that intent.
seo-description: If user intent is demonstrated by action, then repeated action increases confidence in that intent.
seo-title: Frequency
solution: Target
title: Frequency
topic: Standard
uuid: 692bb129-6427-4dc6-9b15-aac24059983e
index: y
internal: n
snippet: y
translate: y
---

# Frequency

So why not deliver a different offer to a visitor who has purchased five times rather than once? You can also gain insight by measuring the frequency of certain clicks. For example, clicking repeatedly into a high-heeled shoe category provides information about a user's gender, valuable for targeted content.
In the Profile Attributes list, write a script that increments a counter whenever something notable occurs. This could be:

* A purchase
* Uploading a picture or video
* Clicking on a special category or section of the site
* Using the search box

Here's a script that increments the counter whenever an mbox called ` orderConfirm` is seen: 

```
user.purchaseFrequency 
 
if (mbox.name == 'orderConfirm') { 
 
   return (user.get('purchaseFrequency') || 0) + 1; 
 
} 
```

Create some expression targets:

```
buys_never: 
return typeof(user.get('purchaseFrequency')) == 'undefined'; 
 
buys_sometimes: 
return user.get('purchaseFrequency') > 0 &amp;&amp; user.get('purchaseFrequency') < 3; 
 
buys_often: 
return user.get('purchaseFrequency') >= 3 
```

This one looks for the video upload page in the url:

```
user.uploadFrequency 
 
if (page.url.indexOf('upload_video.html) > -1) { 
 
   return (user.get('uploadFrequency') || 0) + 1; 
 
} 
```

Create some expression targets:

```
uploads_never: 
return user.get('uploadFrequency') == 0; 
 
uploads_sometimes: 
return user.get('uploadFrequency') > 0 &amp;&amp; user.get('uploadFrequency') < 10; 
 
uploads_often: 
return user.get('uploadFrequency') >= 10 
```

These scripts determine a visitor's gender, giving a higher weight to search results than category clicks, since a search term implies heavy intent:

```
user.femaleFrequency 
 
if (page.param('category').indexOf('blouses')) { 
 
   return (user.get('femaleFrequency') || 0) + 1; 
 
} 
 
else if (page.param('search_query').indexOf('blouse')) { 
 
   return (user.get('femaleFrequency') || 0) + 5; 
 
} 
 
user.maleFrequency 
 
if (page.param('category').indexOf('tuxedos')) { 
 
   return (user.get('maleFrequency') || 0) + 1; 
 
} 
 
else if (page.param('search_query').indexOf('tuxedo')) { 
 
   return (user.get('maleFrequency') || 0) + 5; 
 
} 
```

Create expression targets, which use a simple heuristic to determine a visitor's gender.

```
male: 
var maleFrequency = user.get('maleFrequency'); 
return maleFrequency &amp;&amp; maleFrequency > user.get('femaleFrequency') &amp;&amp; maleFrequency > 10; 
 
female: 
var femaleFrequency = user.get('femaleFrequency'); 
return femaleFrequency &amp;&amp; femaleFrequency > user.get('maleFrequency') &amp;&amp; femaleFrequency > 10;
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
