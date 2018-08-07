---
description: To allow a Web page to contact the Adobe Target server, any page that includes an mbox must reference the mbox.js file where it is saved on the host.
keywords: Dynamic tag management
seo-description: To allow a Web page to contact the Adobe Target server, any page that includes an mbox must reference the mbox.js file where it is saved on the host.
seo-title: Reference Mbox.js with Dynamic Tag Manager
solution: Target
title: Reference Mbox.js with Dynamic Tag Manager
uuid: e673c35a-599d-4a7e-be23-7481d63b0fb2
index: y
internal: n
snippet: y
translate: y
---

# Reference Mbox.js with Dynamic Tag Manager


>1. Log in to Dynamic tag management.
>1. On the Overview page, click ** `Add a Tool` **, then click ** `Tool Type` ** > ** `Adobe Target` **.
>1. Name the tool, then click ** `Create Tool` **.
>1. In the Target tool, then click ** `Settings` ** > ** `Open Editor` **.
>1. In Edit Code, paste an empty JavaScript comment, then click ** `Save and Close` **.

>       `/* */`1. On the Settings page, click ** `Save Changes` **.
>1. Click ** `Rules` ** > ** `Page Load Rules` **.
>1. Create a new rule with the following configuration:

>       | **Page Load Rule** |Synchronous Mbox.js |
>       |---|---|
>       | **Condition** |Top of Page |

>1. Expand ** `JavaScript / Third Party Tags` **, then click ** `Add New Script` ** with the following configuration:

>       | **Tag Name** |Synchronous Mbox.js |
>       |---|---|
>       | **Type** |Sequential JavaScript |
>       | **Enable** |Execute Globally |
>       | **Content** |Paste in the contents of your `mbox.js` file as downloaded from the Adobe Target interface. |

>1. Click ** `Save Code` ** > ** `Save Rule` ** > ** `Approve and Publish Changes` **.
