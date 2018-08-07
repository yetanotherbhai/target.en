---
description: Target Standard changes the communication between your site and Adobe Target.
seo-description: Target Standard changes the communication between your site and Adobe Target.
seo-title: Implementation
solution: Target
title: Implementation
topic: Standard
uuid: a3c508b7-c326-43bb-af86-5ab938f8d5a6
index: y
internal: n
snippet: y
translate: y
---

# Implementation

Target Classic uses mboxes around each area on your page. These mboxes are not required in Standard. Instead, one JavaScript library referenced on each page is all you need to run your optimization activities.
`Target Standard` updates and supplements the `mbox.js` with a reference to a new `target.js` file. The `target.js` file is hosted by Adobe. `Target.js` makes it possible to edit content on any page using the Visual Experience Composer, even if the page does not contain predefined mboxes. You must also reference this file on every page on your site. For example, you might add it to your global header. 
To use `Target Standard`, you must [download and host the updated mbox.js](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420) file that includes the reference to `target.js`. 
To manage content, `Target` makes a call on your page. This call allows `Target` to deliver content, and to track visitor behavior for use in targeting and reporting. Traditionally, the call has been made with an mbox around a specific physical area on your page. With the updated `mbox.js` and `Target Standard`, a call is automatically made to `Target` from every page that references the `mbox.js` file. This one call made at the top of the page is all that is required for `Adobe Target`to deliver Target activities, track clicks, and track most success metrics. This file contains the libraries needed for all of your activities. You do not need to maintain different activity-specific versions of the file. 
If you already have mboxes on your page from a former `Test&amp;Target`implementation, then these mboxes can still be used in the new interface. The updated `mbox.js` file is still required, but these mboxes can be selected for activities and edited using the Visual Experience Composer. 
**What Target Standard Changes on Your Site** 
Use Target Standard to modify a visitor's experience. You can:

* Visually edit text and HTML
* Change link destinations
* Swap the content of an element with new content.
* Remove an element from a page (area used by element is collapsed)
* Hide an element on the page (area used by element remains as white space)
* Change the CSS class for an element.
* Track clicks on an element.
* Create goals (success metrics) for the page or for clickable elements.
* Visually simulate an activity.

**Mbox Counting** 
The updated `mbox.js` makes a call to `Target` on each page, which is counted as an mbox call for contractual purposes. All of these calls are rolled up under the `target-global-mbox` name in the Usage report in Target Classic ( ** `Locations` ** > ** `Usage` **). Any traditional mboxes on your site continue to count as mbox calls. 
