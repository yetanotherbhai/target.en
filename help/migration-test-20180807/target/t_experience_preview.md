---
description: Experience URLs can be generated for Target Automated Personalization activities to see experience content directly on your site before the activity is live for preview and QA purposes. Experience URLs bypass targeting to force viewing of a particular experience.
keywords: experience preview;experience urls;generate urls;view experience urls
seo-description: Experience URLs can be generated for Target Automated Personalization activities to see experience content directly on your site before the activity is live for preview and QA purposes. Experience URLs bypass targeting to force viewing of a particular experience.
seo-title: Share Preview URLs for Automated Personalization Outside of Target
solution: Target
title: Share Preview URLs for Automated Personalization Outside of Target
topic: Standard
uuid: 0d6316d8-67d9-432c-9b8b-851a03a85441
index: y
internal: n
snippet: y
translate: y
---

# Share Preview URLs for Automated Personalization Outside of Target


>[!NOTE]
>
>The Activity QA mode lets you create Activity URLs for other types of activities. For more information, see[Activity QA](c_activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) 

.
To use experience URLs, you have to share the links generated from Target, and not the final URL you land on when viewing the experience. Also, if the content changes, new URLs must be generated. If you generates new URLs, old ones may not work.
Use experience URLs to share experiences with team members and to QA experiences across browsers and environments, without creating a separate QA activity. This feature is particularly useful if a site is complex, or if your security policies do not allow the site to be viewed in a simulator.

>1. Create an Automated Personalization activity.

>       The activity does not have to be live to preview an experience.
>1. Click the activity to open it.
>1. Click ** `View Experience URLs` **, then specify the URL.

>    
>    * If you are using the Visual Experience Composer, the default URL you specified for the activity is entered automatically. You can change this URL and add others, if desired.
>    * If you are using the Form-Based Experience Composer, no default URL is entered automatically. You must specify all URLS you want to preview.

>       You can add multiple URLs, which is useful when running a multi-page test or a template test and you want to preview the activity on more than one page.
>       A modal window displays links to your experiences on your site to get a "true preview" of the experiences outside of Target's Visual Experience Composer. You must share the links from the message to share the preview. Clicking a link and then copying the resulting URL from the page won't work because the URL contains a parameter that only displays the page correctly when you access the page from the link in the message. Instead, copy the text in the modal window and email the whole text to your team.
>       If you then make changes to the experience, make sure to generate new preview links for your team by returning to the modal window and clicking "share" to get new links.

>       >[!NOTE]
>       >
>       >The preview links open in new tabs and require that the pop-up blocker on your browser is disabled.

>       You can also click the Link icon  ![](../graphics/link_icon.png) to view the experience URL. 
>1. Click ** `Generate URLs` **, then click each experience to preview it..
>1. Click ** `Done` **.
