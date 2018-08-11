---
description: By default, Target Standard creates a global mbox called target-global-mbox, which is used to run activities created in Target Standard. However, if you have already created a global mbox on your pages for your legacy implementations, you can use that mbox for your Target Standard activities.
keywords: global mbox;target classic;use global mbox from target classic
seo-description: By default, Target Standard creates a global mbox called target-global-mbox, which is used to run activities created in Target Standard. However, if you have already created a global mbox on your pages for your legacy implementations, you can use that mbox for your Target Standard activities.
seo-title: Using a Global mbox from a Legacy Implementation
solution: Target
subtopic: Getting Started
title: Using a Global mbox from a Legacy Implementation
topic: Standard
uuid: a9b5d601-fea9-419e-b4bf-4e15247b9efe
index: y
internal: n
snippet: y
translate: y
---

# Using a Global mbox from a Legacy Implementation


>[!NOTE]
>
>You can have only one global mbox per account.



To use your existing global mbox for both [!DNL  Target Standard] and your legacy implementation, you must set a few parameters. 

>1. Go to [!DNL  Target Standard], then click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] **.

>       By default, [!UICONTROL  Auto Create Global Mbox] is enabled, and the custom global mbox is named ` target-global-mbox`. 
>1. If you want to use an existing mbox, disable [!UICONTROL  Auto Create Global Mbox], and specify the name of a previously created global mbox in the [!UICONTROL  Custom Global Mbox] field.

>       The [!UICONTROL  Custom Global Mbox] drop-down lists all mboxes in your account. If you want to use an mbox that does not yet exist, create the mbox in Target Classic. 
>1. Click ** [!UICONTROL  Save] **.

>       The mbox.js settings for your account are updated. 
>1. Download the new ` mbox.js` file and reference it on your site.

>       After you've updated your production site with the new ` mbox.js` file, you are ready to set your preferences. 
>1. Click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Preferences] **.
>1. In the [!UICONTROL  Custom Global Mbox] field, specify the name of the global mbox you selected on the Implementation page.
>1. Click ** [!UICONTROL  Submit] **.

>       All existing activities update to use the specified global mbox, including activities that have previously been created and implemented. 
