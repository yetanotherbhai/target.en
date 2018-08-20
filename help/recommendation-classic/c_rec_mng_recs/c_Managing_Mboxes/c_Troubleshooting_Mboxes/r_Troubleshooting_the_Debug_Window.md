---
description: If the Debug window does not appear as expected, use the information in this topic to solve the problem.
seo-description: If the Debug window does not appear as expected, use the information in this topic to solve the problem.
seo-title: Troubleshooting the Debug Window
solution: Target
title: Troubleshooting the Debug Window
topic: Recommendations
uuid: 95da560b-135e-4499-b503-070273f54642
index: y
internal: n
snippet: y
translate: y
---

# Troubleshooting the Debug Window


>**If the Debug window does not appear:** 

>
>* Confirm the ` mbox.js` reference is correct on all Web pages with the mboxes.
>* Confirm you have downloaded the ` mbox.js` into a folder with public permissions.


>** If the Debug window appears but enabled = false:** 

>
>* Delete your cookies and clear cache. Close and reopen a browser and reload the page.
>* If ` enabled=false` persists, seek and remove JavaScript errors. Some common errors include: >
>    * Improper termination of quotes in mbox arguments
>    * Spelling mistakes in your mbox functions
>    * Script tags that are not invoked or that are not closed


>* If ` enabled=false` persists, contact your account representative. 



>** If the mboxes are not listed in the mboxDebug popup window, or if mboxes appear blank on the page, review your page code for the following:** 

>
>* Confirm the ` mbox.js` reference is correct on all Web pages with the mboxes.
>* Confirm that any tag opened before the mbox script is closed after the mbox script.
>* Remove JavaScript errors.
>* Scrub layout to support DOM rendering by all browser types.


>Mboxes insert new nodes into the DOM tree as the browser creates it. Each brand of browser has its own implementation of the W3C DOM specification, so mboxes can affect page rendering differently based on the browser type. Specify absolute sizes of table cells and images to help the browser more accurately display a page's HTML layout. 
>[!MORE_LIKE_THIS] {class="- topic/related-links "}* [ Mbox Troubleshooting Guide ](r_Mbox_Troubleshooting_Guide.md#reference_45B74286990B4B9883A3B46B0FDFE1C8)* [ Troubleshooting Resources ](r_Troubleshooting_Resources.md#reference_1DCDDAC4BAA348148BBD628587A3F669)