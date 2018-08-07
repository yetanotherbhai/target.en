---
description: Information to help your technical staff understand the mbox.js implementation and how it might affect your site.
keywords: implementation;mbox.js;dom manipulation library;target.js;visual experience composer;iframe;angular sites;single page applications;single page app;SPA
seo-description: Information to help your technical staff understand the mbox.js implementation and how it might affect your site.
seo-title: What mbox.js Does
solution: Target
subtopic: Getting Started
title: What mbox.js Does
topic: Standard
uuid: 73dc4244-32c7-4e75-b70e-3abe58a17c29
index: y
internal: n
snippet: y
translate: y
---

# What mbox.js Does

Target Standard requires `mbox.js` version 58 or later. For instructions on how to download and update `mbox.js`, see [Mbox Implementation](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420). 
For Target Standard, `mbox.js` calls another JavaScript file, `target.js`. `Target.js` is hosted by Adobe and is automatically updated by Adobe. There is nothing you need to do to update `target.js`, and there are no client-specific customizations. 
`Target.js` creates an mbox called `target-global-mbox` in the `<head>` section of your page. 
`Target.js` is called from `mbox.js` by a line of JavaScript code added to the `Extra JavaScript` field in `mbox.js`. The only way to disable `target.js` is not to include this line of code, thus also disabling `Target`. 
`Target.js` has two functions in `Target`: 

* DOM manipulation
* Enables visual elements of the `Visual Experience Composer`

The following sections contain more information:

* [DOM Manipulation](c_mbox_technical.md#section_169F8D4C077948DCB4F891ABBB03FF63)
* [Target.js and the Visual Experience Composer](c_mbox_technical.md#section_2B3FF6AC5B8D431C83D9EDCF53CB1472)
* [Considerations for Angular Sites](c_mbox_technical.md#section_16D76F16077A434FAE8CEC6FD43BE6D7)


## DOM Manipulation {#section_169F8D4C077948DCB4F891ABBB03FF63}

`Target.js` controls the DOM manipulation library used by Standard. To display the content of a website, `target.js` references `sizzle.js` (version1.10.8-pre). `Sizzle.js` enables the HTML element selectors. Other than `sizzle.js`, only native JavaScript is used. No jquery is required. 
In addition, the following snippet is used for polling the DOM:
`https://github.com/dperini/ContentLoaded` 
## Target.js and the Visual Experience Composer {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

When you use the `Visual Experience Composer` to set up an experience for an activity, your web page is opened in an iFrame. When the iFrame is loaded, Standard sends an HTML5 `postMessage` API call. `Target.js` detects any `postMessage` calls and includes the following JavaScript libraries on the website: 

* For thumbnail generation: `http://html2canvas.hertzen.com/`
* For cross-domain query: `Admin.js`, `CDQ.base.js`, `CDQ.host.js`, `admin.css`, used to send messages across the iFrames. These scripts allow Adobe to send data between the pages.


## Considerations for Angular Sites and Single-Page Applications {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

If you are implementing Target in an Angular site or in any Single-Page Application (SPA), you should use the `at.js` library instead of `mbox.js`. 
For more information, see [at.js Implementation](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17). 
