---
description: By default, Target Standard creates a global mbox called target-global-mbox, which is used to run activities created in Target Standard. However, if you have already created a global mbox on your pages for your Target Classic campaigns, you can use that mbox for your Target Standard activities.
seo-description: By default, Target Standard creates a global mbox called target-global-mbox, which is used to run activities created in Target Standard. However, if you have already created a global mbox on your pages for your Target Classic campaigns, you can use that mbox for your Target Standard activities.
seo-title: Using a Global Mbox from Target Classic
solution: Target
title: Using a Global Mbox from Target Classic
topic: Standard
uuid: 48a17115-93e2-401e-ae1b-6acb3894cecf
index: y
internal: n
snippet: y
translate: y
---

# Using a Global Mbox from Target Classic


>[!NOTE]
>
>You can have only one global mbox per account.


To use your existing global mbox for both `Target Standard` and `Target Classic`, you must set a few parameters. 

>1. Go to `Target Standard`, then click ** `Setup` ** > ** `Implementation` **.

>       `Auto Create Global Mbox``target-global-mbox`1. If you want to use an existing mbox, disable `Auto Create Global Mbox`, and specify the name of a previously created global mbox in the `Custom Global Mbox` field.

>       `Custom Global Mbox`1. Click ** `Save` **.

>1. Download the new `mbox.js` file and reference it on your site.

>       Once you've updated your production site with the new `mbox.js` file, you are ready to set your preferences. 
>1. Click ** `Setup` ** > ** `Preferences` **.
>1. In the `Custom Global Mbox` field, specify the name of the global mbox you selected on the Implementation page.

>1. Click ** `Submit` **.

