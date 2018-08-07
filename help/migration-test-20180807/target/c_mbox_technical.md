---
description: These details are provided to help your technical staff understand the mbox.js implementation and how it might affect your site.
seo-description: These details are provided to help your technical staff understand the mbox.js implementation and how it might affect your site.
seo-title: Technical Implementation Details
solution: Target
title: Technical Implementation Details
topic: Standard
uuid: efb35754-73a7-457a-afad-0bd6d9fee5a6
index: y
internal: n
snippet: y
translate: y
---

# Technical Implementation Details

Target Standard requires `mbox.js` version 44 or later. `Mbox.js` is hosted by the client and is not dynamic. To update or otherwise change `mbox.js`, you must download a new version, make any changes you want to make, then upload the new file to your hosting environment. Downloading and editing `mbox.js` requires that you either have access to Target Classic or, if you don't have access to Classic, that you work with your account representative to update `mbox.js`. For instructions on how to download and update `mbox.js`, see [Mbox.js Download](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420). 
For Target Standard, `mbox.js` calls another JavaScript file, `target.js`. `Target.js` is hosted by Adobe and is automatically updated by Adobe. There is nothing you need to do to update `target.js`, and there are no client-specific customizations. 
`Target.js` creates an mbox called `target-global-mbox` in the `<head>` section of your page. 
`Target.js` is called from `mbox.js` by a line of JavaScript code added to the `Extra JavaScript` field in `mbox.js`. The only way to disable `target.js` is not to include this line of code, thus also disabling Target Standard. 
`Target.js` has two functions in Standard: 

* DOM manipulation
* Enables visual elements of the Visual Experience Composer

**DOM Manipulation** 
`Target.js` controls the DOM manipulation library used by Standard. To display the content of a website, `target.js` references `sizzle.js` (version1.10.8-pre). `Sizzle.js` enables the HTML element selectors. Other than `sizzle.js`, only native JavaScript is used. No jquery is required. 
In addition, the following snippet is used for polling the DOM: `https://github.com/dperini/ContentLoaded`. 
**Target.js and the Visual Experience Composer** 
When you use the Visual Experience Composer to set up an experience for an activity, your web page is opened in an iFrame. When the iFrame is loaded, Standard sends an HTML5 `postMessage` API call. `Target.js` detects any `postMessage` calls and includes the following JavaScript libraries on the website: 

* For thumbnail generation: `http://html2canvas.hertzen.com/`
* For cross-domain query: `Admin.js`, `CDQ.base.js`, `CDQ.host.js`, `admin.css`, used to send messages across the iFrames. These scripts allow Adobe to send data between the pages.

**Considerations for Angular Sites** 
If you are setting up Target on an Angular site, consider the following tips.
You might have more success using the `TNT.createGlobalMbox()` function instead of `mboxCreate()` and `mboxUpdate()`. This provides the advantage of being able to leverage the `targetPageParams()` function to pass mbox parameters. So: 

1. On page load, `mbox.js` loads and triggers `TNT.createGlobalMbox()`. 

1. On view change, `targetPageParams()` adds parameters and `TNT.createGlobalMbox()` fires again. 


