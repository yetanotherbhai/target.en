---
description: Use QA URLs to perform easy end-to-end activity QA with preview links that never change, optional audience targeting, and QA reporting that stays segmented from live activity data.
keywords: qa;preview;preview links
seo-description: Use QA URLs to perform easy end-to-end activity QA with preview links that never change, optional audience targeting, and QA reporting that stays segmented from live activity data.
seo-title: Activity QA
solution: Target
title: Activity QA
topic: Advanced,Standard,Classic
uuid: c2fcabbb-35b4-4551-b725-525b85518039
index: y
internal: n
snippet: y
translate: y
---

# Activity QA


<a id="section_CF715867CAC34DE397D8712C99AC86D8"></a>

This section contains the following information:

* [Overview](c_activity-qa.md#section_11B761A522A14E61978275772210A4C2) 

* [Accessing and Sharing a QA URL](c_activity-qa.md#section_1C59BAA247B247BDB125D1BE8EAD4547) 

* [Considerations](c_activity-qa.md#section_B256EDD7BFEC4A6DA72A8A6ABD196D78) 



## Overview {#section_11B761A522A14E61978275772210A4C2}

Activity QA lets you fully test your Target activities prior to launching them live. The Activity QA functionality includes:

* Links to share with team members that never change or require regeneration, regardless of updates made to the experiences or activities

* Audience conditions optionally respected so marketers can test targeting criteria or ignore targeting criteria to QA the appearance of experiences without having to meet the audience conditions

* QA reporting is captured so that marketers can confirm that metrics are incrementing as expected and the QA report data is kept separate from production reporting (for non-A4T reporting)

* The ability to preview an experience in isolation or in conjunction with other live activities satisfying the delivery criteria (Page/mbox/audience).

* The ability to QA the entire "user journey." You can access your site once with the QA link and then browse the entire site while in Activity QA. You remain in Activity QA until you end the session or until you use the [QA Target bookmarklet](c_activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) to force yourself out of Activity QA. This feature is particularly useful if you have an activity spanning multiple web pages. 



## Accessing and Sharing a QA URL {#section_1C59BAA247B247BDB125D1BE8EAD4547}


1. From an activity's `Overview` page (all types except Automated Personalization), click the ** `Activity QA` ** link. 
   ![](../graphics/qa link.png) 

1. Configure the following settings:
   ![](../graphics/qa link config.png) 

    * **Match Audience Rules to See Experiences:**Sometimes you want to confirm that your audience matching works. Other times you just want to check the look and feel of the activity. If this setting is toggled to the "on" position, testers must meet targeting requirements to qualify to see the experiences. For Experience Targeting (XT) activities, a single activity URL is provided. The experience you see is determined by you qualifying for one of the targeting rules. 
      If this setting is toggled to the "off" position, clicking the links show you the experiences regardless of whether you qualify or not. When performing QA, you can switch back and forth between requiring or not requiring that audience targeting is respected.

    * **Show Default Content for All Other Activities:**If this option is toggled to the "on" position, default content is shown for all other activities (for example, the preview will be shown in isolation without considering all other live activities on the same page/mbox. 
      If this setting is toggled to "off," consider the following:
    
        * If there are collisions between the activity you are testing and other live activities, [normal priority rules](c_priority.md#concept_1780C11FEA57440499F0047DD6900E0F) apply. Because of this, it is possible you won't see the activity you are intending to QA. 

        * Metrics increment for the viewed activities, but only in the QA reporting environment.





1. Click ** `Done` ** to save your changes. 

1. Share the Activity Link URLs with members of your organization for testing.
   Activity Links never expire and you do not need to resend links if someone makes changes to an activity or experience. However, if you apply a different audience from the Audience Library, rather than simply editing the activity, a new link is generated that you'll need to re-share.
   Each Activity Link URL (for Exp A, Exp B, etc.) lets you start the user journey from the corresponding experience. You can click the URL generated for an experience and then proceed with normal site browsing to see experiences on multiple pages (if multiple pages exist). Only one URL is generated per experience, even if the experience spans multiple pages (template testing or multi-page testing). You can navigate the site to see the other pages because the Activity QA is sticky.

1. To see reports generated from Activity Link URLs, click the activity's ** `Reports` ** page, click the ** `Settings` ** icon (  ![](graphics/icon_gear.png) ), then select ** `QA Mode` ** from the ** `Environment` ** drop-down list. 



## Considerations {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}


* The `Activity QA` link displays on the `Overview` page of all activity types except for Automated Personalization (AP). You can use [Preview links](t_experience_preview.md#task_586C6655A6FD4AF08F5678FC3F481EFC) for AP activities. 

* Activity QA URLs are available with activities with Analytics as the reporting source (A4T). Hits generated while performing QA using Activity QA will flow to the same report suite where the activity's data will flow even after the activity goes live.

* Activity QA does not display content for archived activities or activities that are past its end date.

* Activities imported into Target Standard/Premium (from Target Classic, for example) do not support QA URLs.

* In Auto-Allocate, Auto-Target, and Recommendations activities, the model will not be affected by the visits captured in Activity QA.

* Because Activity QA is sticky, after you browse a website in Activity QA, your Target session must expire or you need to have Target release you from Activity QA before you can view your site like a typical visitor. Use the [Target QA bookmarklet](c_activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) to force yourself out of Activity QA. 
  You can also manually force yourself out by loading a page on your site with the `at_preview_token` parameter with an empty value (for example, `http://www.mysite.com/?at_preview_token=`). 

* If you specified "URL is" while creating the activity ([refinements in the Form-based Composer](t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) or [page delivery options in the Visual Experience Composer)](r_viztarget_options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), the QA URL will not work because Activity QA appends URL parameters. To solve this issue, click the QA URL to go to your site, remove the appended parameters from the URL, then load the new URL. 

* 3rd-party cookies must be enabled in Safari browsers for Activity QA to work properly.

* If an activity uses multiple experience audiences (for example, a UK and US site that are included in the same activity), QA links aren’t generated for the four combinations (Experience A/ US Site, Experience A/ UK Site, Experience B/ US Site, Experience B/ UK Site). Only two QA links (Experience A and Experience B) are created and users must qualify for the appropriate audience to see the page. A UK QA person couldn’t see the US site.


