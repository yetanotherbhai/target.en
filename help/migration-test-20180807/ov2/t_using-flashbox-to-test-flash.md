---
description: There are multiple ways to test and target Flash content.
keywords: Implementation;mbox.js non javascript;mbox;adbox;email
seo-description: There are multiple ways to test and target Flash content.
seo-title: Use Flashbox to Test Flash
solution: Target
subtopic: Getting Started
title: Use Flashbox to Test Flash
topic: Standard
uuid: 8cf26370-ea57-4e70-aa0b-39447a0c6fb7
index: y
internal: n
snippet: y
translate: y
---

# Use Flashbox to Test Flash

Generic ActionScript classes can be used to "instrument" any Flash file with targeting capabilities.
You can learn more about Flashbox by following the Flash Integration tutorial here: [http://www.adobe.com/devnet/flash/articles/fl_tnt_overview.html](http://www.adobe.com/devnet/flash/articles/fl_tnt_overview.html). 
To change more than just static elements in Flash, you can use the Flash ActionScript classes available for Target. With these classes you can create Flashboxes that work quite similarly to mboxes to return different content to the Flash file to change the viewer's experience.

>[!NOTE] {class="- topic/note "}
>
>Flashbox developer documentation is available by clicking `Display Ads` > `Flashbox classes`. Contact your support professional for more information. 


The process for creating an AdBox for a Flash file is the same as for an image Adbox (see [Creating an AdBox for an Image](t_testing-content-with-the-adbox.md#task_24C59DF05D454066BC33D9FCC4A841D9)), with these differences: 

>1. Use page as the content type and make the default link to your swf file.

>       `http://myClientCode.tt.omtrdc.net/m2/myClientCode/ubox/page?mbox=adflash_abc_320x200&amp;mboxDefault= http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Eswf` 
>1. To complete QA, use the embed src tag on the dummy page as you would a Flash file.

>       `<embed src=http://myClientCode.tt.omtrdc.net/m2/myClientCode/ubox/page ?mbox=ad123&amp;mboxDefault= http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Eswf>` 
