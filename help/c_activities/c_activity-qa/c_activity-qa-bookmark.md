---
description: Information to help you use the Target QA bookmarklet to force Target to release you from QA mode.
keywords: qa;preview;bookmarklet;preview links
seo-description: Information to help you use the Target QA bookmarklet to force Target to release you from QA mode.
seo-title: Activity QA Bookmarklet
solution: Target
title: Activity QA Bookmarklet
topic: Advanced,Standard,Classic
uuid: aee07350-c55a-4e08-a9f8-f04ac0d5ff46
index: y
internal: n
snippet: y
translate: y
---

# Activity QA Bookmarklet

Because [ QA mode](../../c_activities/c_activity-qa/c_activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) is sticky, after you browse a website in QA mode, your Target session must expire or you need to have Target release you from QA mode before you can view your site like a typical visitor. Use the QA Target bookmarklet to force yourself out of QA mode. 

To use the Target QA bookmarklet, drag the following bookmarklet to your browser's Bookmarks Toolbar: 

**Bookmarklet:** [ Release Adobe Target Activity QA](javascript:(function () {var parts = window.location.href.split('at_preview_token',2); if (parts.length > 1) {window.location.href = parts[0].concat('at_preview_token=');} })();) 

The bookmarklet should then appear on the toolbar for re-use. 

You can also manually force yourself out of QA mode by loading a page on your site with the ` at_preview_token` parameter with an empty value (for example, ` http://www.mysite.com/?at_preview_token=`). 
