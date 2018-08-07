---
description: Target Standard uses a modified version of the Adobe Target mbox.js file.
seo-description: Target Standard uses a modified version of the Adobe Target mbox.js file.
seo-title: Mbox Implementation
solution: Target
title: Mbox Implementation
topic: Standard
uuid: 9ea357c8-5739-4bde-b2cf-1f36292a3602
index: y
internal: n
snippet: y
translate: y
---

# Mbox Implementation

To use the new Adobe Target Visual Experience Editor, you must include an additional line of JavaScript as part of your `mbox.js` file. 
If you have both `Target Standard` and `Target Classic`, you can use the following procedure to update your `mbox.js file`. If you use `Target Standard` but do not have `Target Classic`, contact ClientCare or your consultant or account manager to set up a `target.js` file. 

>1. Click ** `Setup` ** > ** `Implementation` ** in `Target Standard`.
>1. Click ** `Download mbox.js` ** and follow the prompts to save the file.

>1. Create the [ `mbox.js` reference](https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Referencing_mboxjs.html) on the website.


>       >[!IMPORTANT]
>       >
>       >The reference must be the last item before the closing `</head>` tag in the `<head>` section of your pages. If the reference is not the last item, serious display or performance issues could result. See [Mbox Technical Details](https://marketing.adobe.com/resources/help/en_US/target/#target-Mbox_Technical_Details) for more information. 

>1. Upload the saved `mbox.js` file to the location in your hosting environment that you specified in the code.

