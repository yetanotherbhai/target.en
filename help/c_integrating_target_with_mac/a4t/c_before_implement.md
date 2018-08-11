---
description: Several changes occur in your data collection process when enabling Analytics as the reporting source for Target (A4T).
keywords: Recommendations
seo-description: Several changes occur in your data collection process when enabling Analytics as the reporting source for Target (A4T).
seo-title: Before You Implement
solution: Target
title: Before You Implement
topic: Premium
uuid: 3eaad3d6-9ba2-41a8-bfc8-12d9e0d7b8a4
index: y
internal: n
snippet: y
translate: y
---

# Before You Implement

This video explains how to use Adobe Analytics as a reporting source in Adobe Target to drive the analysis of your optimization program. 



<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Analytics for Target (A4T) </th> 
   <th colname="col3" class="entry"> 4:32 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/eS_LeNmcJug/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/eS_LeNmcJug/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_536EBE8EF3D34C2BBB43043DA339F371"> <p>Explain what A4T is and why you would use it </p> </li> 
      <li id="li_BCE359271A534D8D9F880C98A0D8811B"> <p>Explain how A4T works </p> </li> 
      <li id="li_0CACB4D122324A659025639A3567DC6F"> <p>Understand the prerequisites needed before using A4T </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Before you decide to use this integration, review the following sections and consider the impact to your reporting processes: 

* [ Implementation Requirements ](../../c_integrating_target_with_mac/a4t/c_before_implement.md#section_A0D2EF18033D4C3997B08A6EBB34C17A)
* [ Things to Know Before you Implement ](../../c_integrating_target_with_mac/a4t/c_before_implement.md#section_50D49CC52E11414089C89FB67F9B88F5)
* [ Latency ](../../c_integrating_target_with_mac/a4t/c_before_implement.md#section_9489BE6FD21641A4844E591711E3F813)
* [ Supplemental ID ](../../c_integrating_target_with_mac/a4t/c_before_implement.md#section_2C1F745A2B7D41FE9E30915539226E3A)

## Implementation Requirements {#section_A0D2EF18033D4C3997B08A6EBB34C17A}


>[!IMPORTANT]
>
>Before you can begin using A4T, you need to request that your account be provisioned for the integration. Use[ this form ](http://www.adobe.com/go/audiences) to request to be provisioned. 



This A4T integration requires that you implement the following library versions, depending on whether you want to use redirect offers with A4T or not: 



<table id="table_34391C80AE954618AE91D6AE654D3985"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Requirements Needed for A4T </th> 
   <th colname="col2" class="entry"> Requirements Needed for Redirect Offers Using A4T </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>This integration requires that you implement the following library versions (or newer) if you do not plan on using redirect offers with A4T: </p> <p> 
     <ul id="ul_4D98A3886E10443B930094BE9D47A2F2"> 
      <li id="li_06A9C85450E64D05AD3D45FE20DA4A53"> <p>Adobe Analytics: <span class="filepath"> appMeasurement.js </span> version 1.7.0. </p> </li> 
      <li id="li_3D79F3BD5B52402A8DC81875F510370B"> <p>Experience Cloud Visitor ID Service: <span class="filepath"> visitorAPI.js </span> version 1.8.0. </p> </li> 
      <li id="li_351A2616F18444DF951F16A977BD9FAC"> <p>Adobe Target (depending on your implementation): <span class="filepath"> at.js </span> version 0.9.1 or <span class="filepath"> mbox.js </span> version 61. </p> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p>To use redirect offers with A4T, you must implement the following library versions (or newer): </p> <p conref="a4t-library-requirements.xml#ditacomponent_13103211D36E4EAEA4E9F779B2490E76/p_A816444144144867B5266CA4D5F69F4A"> </p> </td> 
  </tr> 
 </tbody> 
</table>

Download and deployment instructions are listed in [ Adobe for Target Implementation ](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_a4timplementation.html). 

## Things to Know Before You Implement {#section_50D49CC52E11414089C89FB67F9B88F5}


* This integration is enabled on new activities when you select to use Analytics as the reporting source. After you make the implementation changes described in this document, your existing activities are not impacted. 

* The process of setting up Analytics as the reporting source for Target includes several implementation steps, followed by a provisioning step. It is a good idea to read through the process as described below before implementing. After you complete these steps, you will be ready to use Analytics as your reporting source as soon as it is enabled for you. The provisioning process can take up to five business days. 

* The Visitor ID service creates a shared Visitor ID across the Experience Cloud. While it does not replace the Target mboxPC id or Audience Manager UUID, it does replace the way Analytics identifies new visitors. If set up properly, returning Analytics visitors should also be identified via their old Analytics ID to prevent visitor cliffing. Similarly, because the Target mboxPCid remains intact, no Target visitor profile data is lost when you upgrade to the Visitor ID service. 

* The Visitor ID service must execute before your Analytics and Target page code. Make sure that ` VisitorAPI.js` appears above the tags for all other Experience Cloud products. 


## Latency {#section_9489BE6FD21641A4844E591711E3F813}

After this integration is enabled, you will experience an additional 5-10 minutes of latency in Adobe Analytics. This latency increase allows data from Analytics and Target to be stored on the same hit, allowing you to break down tests by page and site section. 

This increase is reflected in all Adobe Analytics services and tools, including the live stream and real-time reporting, and applies in the following scenarios: 

* For live stream, real-time reports &amp;amp; API requests, and current data for traffic variables, only hits with a supplemental data ID are delayed. 

* For current data on conversion metrics, finalized data, and data feeds, all hits are delayed an additional 5-7 minutes. 

Be aware that the latency increase starts after you implement the Experience Cloud visitor ID service, even if you have not fully implemented this integration. 

## Supplemental ID {#section_2C1F745A2B7D41FE9E30915539226E3A}

All Target calls used by an A4T activity to deliver content or record the goal metric must have a corresponding Analytics hit that shares the same supplemental ID for A4T to work properly. 

Hits that contain data from Analytics and Target contain a supplemental data ID. You can see this ID in the [ Adobe Debugger ](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=debugger) as the ` sdid` parameter. For example: ` sdid=2F3C18E511F618CC-45F83E994AEE93A0`. This ID is generated anytime the following criteria are in place: 

* The visitor ID service is in implemented 

* A version of [!DNL  mbox.js] that supports this integration is implemented. 

When troubleshooting, be sure to confirm that the supplemental ID is present on Analytics hits. 
