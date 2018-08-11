---
description: The at.js library is a new implementation library for Adobe Target designed for both typical web implementations and single-page applications.
keywords: Target Standard;at.js;implementation
seo-description: The at.js library is a new implementation library for Adobe Target designed for both typical web implementations and single-page applications.
seo-title: at.js Implementation
solution: Target
title: at.js Implementation
topic: Standard
uuid: 36c99962-720d-4528-92c9-89069730c665
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
    * Customizable [ timeout ](cmp_at.js_Functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF) per call
    * No reloads on timeouts


* Functions designed specifically for single-page apps/MVC frameworks


This video is a recording of " [ Office Hours ](c_adobe-customer-care-office-hours.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)," an initiative led by the Adobe Customer Care team. 



<table id="table_DC2EFE9B1E1D4FB69CB0D44AE1B2367E"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> at.js - Advantages and Implementation Best Practices </th> 
   <th colname="col3" class="entry"> 26:43 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://video.tv.adobe.com/v/22223/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://video.tv.adobe.com/v/22223/</iframe>
     </div> </p> </td> 
   <td colname="col3"> 
    <ul id="ul_531000D579CC439E8A970E613094466B"> 
     <li id="li_8BC24EBD02AC4CEE99CCC750462E99DC"> <p>How the at.js library works </p> </li> 
     <li id="li_421652E5FD6C4BE2A19DA592EBC47627"> <p>The advantages of at.js over mbox.js </p> </li> 
     <li id="li_B4A75BFA187F471B82ED159A895AE3E9"> <p>How at.js manages flicker </p> </li> 
     <li id="li_94479C7A03C54343A81B8C99AA7C5506"> <p>Error handling in at.js </p> </li> 
     <li id="li_461233D829364C8187CB2CE891816364"> <p>Debugging methodologies </p> </li> 
     <li id="li_1F17C87CB70B4A55BB6286F31FD9A9E4"> <p>Known issues and future roadmap </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

