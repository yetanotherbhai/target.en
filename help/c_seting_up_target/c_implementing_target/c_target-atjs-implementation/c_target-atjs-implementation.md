---
description: The at.js library is a new implementation library for Adobe Target designed for both typical web implementations and single-page applications.
keywords: Target Standard;at.js;implementation
seo-description: The at.js library is a new implementation library for Adobe Target designed for both typical web implementations and single-page applications.
seo-title: at.js Implementation
solution: Target
title: at.js Implementation
topic: Standard
uuid: 739ae139-e6ac-4d19-84ff-a6b4ebcbd09e
index: y
internal: n
snippet: y
translate: y
---

# at.js Implementation

Among other benefits, [!DNL  at.js] improves page-load times for web implementations and provides better implementation options for single-page applications. 

[!DNL  at.js] replaces [!DNL  mbox.js] for [!DNL  Target] implementations. The [!DNL  at.js] library also includes the components that were included in [!DNL  target.js], so there is no longer a call to [!DNL  target.js]. 


>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 with FP-11577 (or later) supports at.js implementations with its Adobe Target Cloud Services integration. For more information, see[ Feature Packs ](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) and [ Integrating with Adobe Target ](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in the *Adobe Experience Manager 6.2 documentation*. 



To use [!DNL  at.js], replace the [!DNL  mbox.js] reference on pages where you want to implement it. You cannot use both [!DNL  mbox.js] and [!DNL  at.js] on a single page. However, you can use either on each page on your site. 

The [!DNL  at.js] library works for existing implementations using the ` mboxCreate()`, ` mboxDefine()`, and ` mboxUpdate()` functions and supports new functionality focused on single-page-app based implementations. 

You can use [!DNL  at.js] anywhere you currently use [!DNL  mbox.js]. 

The [!DNL  at.js] library offers several improvements over the [!DNL  mbox.js] library, including: 


* Completely asynchronous communication via cross domain AJAX 
  >[!IMPORTANT]
  >
  >Although [!DNL  at.js] communicates with the [!DNL  Target] servers asynchronously, the [!DNL  at.js] file itself must load synchronously in the ` &amp;lt;head&amp;gt;` section of your page. Ideally, it should be one of the first scripts loaded. Once loaded, [!DNL  at.js] executes mbox calls asynchronously through ` XMLHttpRequest`, and does not block page rendering. 


* No more blocking calls
* No ` document.write()` used
* No immediate execution of JavaScript in [!DNL  Target] responses
* Better timeout and error handling 
    * Customizable [ timeout ](../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/cmp_at.js_Functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF) per call
    * No reloads on timeouts


* Functions designed specifically for single-page apps/MVC frameworks


**at.js - Advantages and Implementation Best Practices (26:43)** 

This video is a recording of " [ Office Hours ](../../../c_adobe-customer-care-office-hours.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)," an initiative led by the Adobe Customer Care team. 


* How the at.js library works 

* The advantages of at.js over mbox.js 

* How at.js manages flicker 

* Error handling in at.js 

* Debugging methodologies 

* Known issues and future roadmap 



>[!VIDEO](https://video.tv.adobe.com/v/22223/) 
