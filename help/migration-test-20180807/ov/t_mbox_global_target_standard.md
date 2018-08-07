---
description: By default, Target Standard creates a global mbox called target-global-mbox, which is used to run activities created in Target Standard. However, if you have already created a global mbox on your pages for your legacy implementations, you can use that mbox for your Target Standard activities.
keywords: global mbox;target classic;use global mbox from target classic
seo-description: By default, Target Standard creates a global mbox called target-global-mbox, which is used to run activities created in Target Standard. However, if you have already created a global mbox on your pages for your legacy implementations, you can use that mbox for your Target Standard activities.
seo-title: Using a Global mbox from a Legacy Implementation
solution: Target
subtopic: Getting Started
title: Using a Global mbox from a Legacy Implementation
topic: Standard
uuid: 8daa83c1-bc82-41b0-b7c3-89c1ab3d24ae
index: y
internal: n
snippet: y
translate: y
---

# Using a Global mbox from a Legacy Implementation


>[!NOTE]
>
>You can have only one global mbox per account.


To use your existing global mbox for both `Target Standard` and your legacy implementation, you must set a few parameters. 

>1. Go to `Target Standard`, then click ** `Setup` ** > ** `Implementation` **.

>       By default, `Auto Create Global Mbox` is enabled, and the custom global mbox is named `target-global-mbox`. 
>1. If you want to use an existing mbox, disable `Auto Create Global Mbox`, and specify the name of a previously created global mbox in the `Custom Global Mbox` field.

>       The `Custom Global Mbox` drop-down lists all mboxes in your account. If you want to use an mbox that does not yet exist, create the mbox in Target Classic. 
>1. Click ** `Save` **.

>       The mbox.js settings for your account are updated.
>1. Download the new `mbox.js` file and reference it on your site.

>       After you've updated your production site with the new `mbox.js` file, you are ready to set your preferences. 
>1. Click ** `Setup` ** > ** `Preferences` **.
>1. In the `Custom Global Mbox` field, specify the name of the global mbox you selected on the Implementation page.
>1. Click ** `Submit` **.

>       All existing activities update to use the specified global mbox, including activities that have previously been created and implemented.
