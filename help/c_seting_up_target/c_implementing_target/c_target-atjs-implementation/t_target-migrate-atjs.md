---
description: Migrating from mbox.js to at.js is a straightforward process.
keywords: Target;at.js;migrate to at.js;readiness;audit at.js;integrate at.js
seo-description: Migrating from mbox.js to at.js is a straightforward process.
seo-title: Migrate to at.js from mbox.js
solution: Target
title: Migrate to at.js from mbox.js
topic: Standard
uuid: 5f4fedd2-9b7b-4ba2-9807-a84dd05c35f2
index: y
internal: n
snippet: y
translate: y
---

# Migrate to at.js from mbox.js

Use the following steps to migrate from [!DNL  mbox.js] to [!DNL  at.js] and to check your migration: 

>1. Determine your organization's [ browser support ](r_supported_browsers.md#reference_01B4BF99E7D545A7998773202A2F6100) requirements.
>1. Check your website's current [!DNL  mbox.js] implementation for capabilities that are not supported by [!DNL  at.js].

>       When auditing your implementation, look for the following: 

>       **What types of mboxes do you currently use?** 



>    <table id="table_B728D875E392457CB304D82CA85348BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Auto-created global mbox </p> </td> 
   <td colname="col2"> <p> The auto-created global mbox is created when the only line of <span class="keyword"> Target </span> code on your site is the <span class="filepath"> mbox.js </span> file. That file automatically generates an mbox call. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Global, empty <span class="codeph"> mboxCreate </span> </p> </td> 
   <td colname="col2"> <p>It is recommended that you switch to the auto-created global mbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wrapping <span class="codeph"> mboxCreate </span> </p> </td> 
   <td colname="col2"> <p>Migration should be simple, as long as your <span class="codeph"> mboxCreate() </span> is preceded by the <span class="codeph"> &amp;lt;div class="mboxDefault"&amp;gt;&amp;lt;/div&amp;gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxUpdate </p> </td> 
   <td colname="col2"> <p> Migration should be simple when <a href="cmp_at.js_Functions.xml#reference_61B2B9F351344CF5B0915D5AFD21C5FE" format="dita" scope="local"> <span class="codeph"> mboxUpdate() </span> </a> is used in conjunction with <span class="codeph"> mboxDefine() </span> or <a href="cmp_at.js_Functions.xml#reference_E68805FE86C64792B2066DB17B253D74" format="dita" scope="local"> <span class="codeph"> mboxCreate() </span> </a>. <span class="codeph"> mboxUpdate() </span> does not update the auto-created global mbox or an mbox originally created by <span class="codeph"> getOffer() </span>. In these circumstances, <a href="cmp_at.js_Functions.xml#reference_C81525D1598A4A1199740DCAB81A7FDF" format="dita" scope="local"> a combination of <span class="codeph"> getOffer() </span> and <span class="codeph"> applyOffer() </span> </a> should be used to replace <span class="codeph"> mboxUpdate() </span> when migrating to at.js. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom clicktracking mboxes, including mboxTrack </p> </td> 
   <td colname="col2"> <p>We recommend that you update your code to use <a href="cmp_at.js_Functions.xml#reference_7E0F19368F9C4BC38F1E5DC5E717E487" format="dita" scope="local"> trackEvent() </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>       **Do you have any customizations to your [!DNL  mbox.js] file?** 

>    
>    * mboxParameters()
>    * mboxSupported()
>    * mboxCookieDomain()
>    * Extra Javascript
>    * Other locations


>       Most of the [ mbox.js objects and methods ](r_variables_profiles_parameters_methods.md#section_8C78059D15D9452F95636A5640188537) (such as ` mbox`, ` mboxCurrent`, ` mboxFactoryDefault`, ` mboxFactories`, and others) are not supported. Alternate approaches might be possible to accomplish what you are trying to do. 

>       **Do you have [!DNL  mbox.js] on any of your web pages?** 

>       You cannot use both [!DNL  at.js] and [!DNL  mbox.js] on the same web page. However, you can use the two JavaScript libraries on two different pages of the same website. 

>       The mbox cookie is the main way Adobe stitches the visitor from page to page. As part of your QA process, you should confirm that the cookie is being preserved and read correctly as the visitor moves back and forth between pages with [!DNL  at.js] and those with [!DNL  mbox.js]. Make sure the same ` mboxPC` and ` mboxSession` values are passed in the mbox calls, regardless of which section of the site ( [!DNL  at.js] or [!DNL  mbox.js]) the visitor first lands on and which section originally sets the cookie. If you use 3rd-party cookies in your implementation, ensure that those values stay the same as you browse the site. 

>       **Do you integrate [!DNL  Target] with any other Adobe solutions?** 

>    
>    * Analytics (A4T)
>    * Analytics (legacy integration)
>    * AAM (backend)
>    * AAM (legacy frontend)
>    * AEM
>    * Data Workbench


>       Some of the legacy integrations are not supported by [!DNL  at.js]. For more information, see the [ Integrations ](c_target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) page. 

>       **Do you integrate [!DNL  Target] with any 3rd-party tools?** 

>    
>    * Other Analytics tools
>    * Other DMPs
>    * Demandbase
>    * Click-tale
>    * Other


>       These integreations might need to be adjusted to work with [!DNL  at.js]. For more information, see the [ Integrations ](c_target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) page. 

>       **Do you use a tag manager?** 

>    
>    * Dynamic Tag Management
>    * Ensighten
>    * Tealium
>    * Signal/BrightTag


>       For more information, see [ at.js Integrations ](c_target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39). 


>       >[!NOTE]
>       >
>       >If you are not currently using a tag manager to deploy [!DNL  Target], now might be a good time to consider it. Adobe's [ Dynamic Tag Management ](https://dtm.adobe.com) is free to [!DNL  Target] customers and is the recommended method to deploy [!DNL  Target]. For more information, see [ Best Practices for Implementing Adobe Target using Dynamic Tag Management ](https://marketing.adobe.com/resources/help/en_US/dtm/target/). 

>1. Verify that all current activities and integrations are working as expected.

>       Here are some things you can do while testing to confirm that [!DNL  at.js] is working as expected: 

>    
>    * Make sure all of your current activities work with the new JavaScript library. 

>    * Confirm that all [ integrations ](c_target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) and [ plugins ](c_target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) work as expected. 

>    * Make sure you are comfortable [ debugging ](c_target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) with the approaches available with [!DNL  at.js]. 


