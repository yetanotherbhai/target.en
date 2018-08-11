---
description: Experience URLs can be generated for Target Automated Personalization activities to see experience content directly on your site before the activity is live for preview and QA purposes. Experience URLs bypass targeting to force viewing of a particular experience.
keywords: experience preview;experience urls;generate urls;view experience urls
seo-description: Experience URLs can be generated for Target Automated Personalization activities to see experience content directly on your site before the activity is live for preview and QA purposes. Experience URLs bypass targeting to force viewing of a particular experience.
seo-title: Share Experience URLs to Preview Automated Personalization Outside of Target
solution: Target
title: Share Experience URLs to Preview Automated Personalization Outside of Target
title_outputclass: premium
topic: Standard
uuid: 9f248e19-8b42-403f-9d28-edc131762499
badge: assets/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Share Experience URLs to Preview Automated Personalization Outside of Target


>[!NOTE]
>
>The Activity QA mode lets you create Activity URLs for other types of activities. For more information, see[ Activity QA](c_activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) 

.

To use experience URLs, you have to share the links generated from Target, not the final URL you land on when viewing the experience. Also, if the content changes, new URLs must be generated. If you generates new URLs, old ones may not work. 

Use experience URLs to share experiences with team members and to QA experiences across browsers and environments, without creating a separate QA activity. This feature is particularly useful if a site is complex, or if your security policies do not allow the site to be viewed in a simulator. 

>1. Create an [ Automated Personalization activity](t_create_ap_activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) or click the activity to open it.

>       The activity does not have to be live to preview an experience. 
>1. On the activity summary page, click on the three vertical dots, then click ** [!UICONTROL  View Experience URLs] **.
>1. Review and/or specify your URLs.

>    
>    * If you are using the Visual Experience Composer, the default URL you specified for the activity is entered automatically and a link is generated for each experience in your activity. You can change this URL and add others, if desired.
>    * If you are using the Form-Based Experience Composer, no default URL is entered automatically. If you haven't previously created Experience URLs, click **Add New URL**. You must specify all URLs you want to preview as well as a name for each URL.


>       You can add multiple URLs, which is useful when running a multi-page test or a template test and you want to preview the activity on more than one page. 

>       A modal window displays links to your experiences on your site to get a "true preview" of the experiences outside of Target's Visual Experience Composer. You must share the links from the message to share the preview. Clicking a link and then copying the resulting URL from the page won't work because the URL contains a parameter that only displays the page correctly when you access the page from the link in the message. Instead, copy the text in the modal window and email the whole text to your team. 
>1. Click ** [!UICONTROL  Generate All] **, then click each experience to preview it.
>   If you then make changes to the experience, make sure to generate new preview links for your team by returning to the modal window and clicking **Generate all** to get new links. 

>   **Note:** The preview links open in new tabs and require that the pop-up blocker on your browser is disabled. 
>
>1. Click each experience name to preview the activity.

>       The page opens, displaying the activity. 
>1. Click ** [!UICONTROL  Done] ** to return to the activity summary.
