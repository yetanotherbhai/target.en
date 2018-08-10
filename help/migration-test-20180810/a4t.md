---
description: Adobe "Analytics for Target" (A4T) is a cross-solution integration that lets you create activities based on Analytics conversion metrics and audience segments. This integration lets you use Analytics reports to examine your results. If you use Analytics as the reporting source for an activity, all reporting and segmentation for that activity is based on Analytics data collection.
keywords: analytics tracking server;A4T;Adobe Marketing Cloud debugger;reporting source
seo-description: Adobe "Analytics for Target" (A4T) is a cross-solution integration that lets you create activities based on Analytics conversion metrics and audience segments. This integration lets you use Analytics reports to examine your results. If you use Analytics as the reporting source for an activity, all reporting and segmentation for that activity is based on Analytics data collection.
seo-title: Adobe Analytics as the Reporting Source for Adobe Target (A4T)
solution: Target
subtopic: Multivariate Test
title: Adobe Analytics as the Reporting Source for Adobe Target (A4T)
topic: Standard
uuid: 01c36f49-659a-458f-9bda-27463a17388f
index: y
internal: n
snippet: y
translate: y
---

# Adobe Analytics as the Reporting Source for Adobe Target (A4T)

## Adobe Analytics as the Reporting Source for Adobe Target (A4T) {#concept_7540C8C04259434AB6EE33B09F47A1DE}Adobe "Analytics for Target" (A4T) is a cross-solution integration that lets you create activities based on Analytics conversion metrics and audience segments. This integration lets you use Analytics reports to examine your results. If you use Analytics as the reporting source for an activity, all reporting and segmentation for that activity is based on Analytics data collection.This video explains how to use Adobe Analytics as a reporting source in Adobe Target to drive the analysis of your optimization program. 



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


## A4T Overview {#section_92B66069210C40DBA937790E8CC596CF}

The Analytics for Target integration between Analytics and Target provides powerful analysis and timesaving tools for your optimization program. 

The three primary benefits of using Analytics data in Target are: 


* Marketers can dynamically apply Analytics success metrics or reporting segments to Target activity reports at any time. It is not required to specify everything before running the activity. 

* A single source of data eliminates the variance that occurs when collecting data in two separate systems. 

* Your existing Adobe Analytics implementation collects all required data. There is no need to implement mboxes on pages for the sole purpose of collecting data for reports. Although, it is still recommended that you implement an order confirmation mbox for Automated Personalization (AP) activities. 




>[!IMPORTANT]
>
>Before you can begin using A4T, you need to request that your account be provisioned for the integration. Use[ this form ](http://www.adobe.com/go/audiences) to request to be provisioned. 




>[!NOTE]
>
>The integration that enables Adobe Analytics as the data source for Adobe Target (A4T) represents the next generation of the Test&amp;amp;Target to SiteCatalyst plug-in. This plug-in has been deprecated, but is still supported for customers who already use it.



If you use Analytics as the reporting source for an activity, all reporting and segmentation for that activity is based on Analytics. 

All Analytics metrics, including calculated metrics, are available in Target Standard/Premium and the Target Activities report in Analytics. Likewise, any segment available in Analytics can be applied to both solutions. You can apply the metric or audience to the report in Target Standard/Premium after the test has started, or even after the test has completed. 

Every metric is included, including any customer or calculated metrics that are built-in in Analytics. 

Data appears in these reports approximately an hour after it is collected from site. All metrics, segments, and values in the reports come from the report suite you selected when you set up the activity. 

Keep the following points in mind when considering using A4T: 


* To use Adobe Analytics as the reporting source for Adobe Target, both you and your company must have access to Adobe Analytics and to Adobe Target. [ Contact your account representative ](r_release_notes.md#concept_34A1CA16F2244D42930BB77846A5ABBB) if you need either solution. 

* You can send A4T data from a single Target account to multiple Analytics companies that are tied to the same Marketing Cloud organization as the Target account. 

* The reporting source is set for each activity. Target continues to collect data to use in reporting and Target data is still available if you prefer to base an activity on data collected by Target. 

* You must use one reporting source or the other. You cannot collect data for a single activity from both sources. 

* When using A4T, all success metrics available to your activities are Analytics metrics. However, your goal metric can be based on an mbox call. For example, you can use Target's out-of-the-box click-tracking capabilities with A4T instead of having to implement Analytics click-tracking code. 

* When viewing reporting of an A4T activity in the Target UI, you are viewing Analytics data. For example, if you use the Visitor metric in Target, you are using the Analytics Visitor metric, not the Target Visitors metric, which is now called Entrants. This difference is especially important for basic traffic metrics (Visitors, Visits, Page Views) and conversion metrics. 

* Any existing Target activities continue to use Target data collection and are not affected by enabling A4T. 

* Only one mbox-based metric is allowed when using Analytics as the reporting source. 

* A server-to-server call from Target to Analytics sends activity and experience information to Analytics. This integration does not result in additional server calls for either Target or Analytics. 



## Supported Activity Types {#section_F487896214BF4803AF78C552EF1669AA}

The following table shows you which activity types support Analytics as the reporting source (A4T): 



<table id="table_3FB19416FBDD441ABC338554D34BED0A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Activity Types </th> 
   <th colname="col3" class="entry"> A4T Compatible? </th> 
   <th colname="col5" class="entry"> Notes, if applicable </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A/B activity with manual traffic split </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A/B activity with Auto-Allocate </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A/B activity with Auto-Target </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting (XT) </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Multivariate test (MVT) </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col5"> <p>Requires mbox-based goal metric goal to get the Element Contribution report. </p> <p>The Element Contribution Report does not currently support Analytics metrics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Automated Personalization (AP) activity </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Recommendations activity </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mobile App </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col5"> <p>Supported with the <span class="keyword"> Mobile Services </span> SDK, version 4.13.1 or later. </p> <p>For more information, see the <a href="https://marketing.adobe.com/resources/help/en_US/mobile/" format="https" scope="external"> Mobile Services documentation </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Email </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Server Side Delivery API </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AEM 6.1 (or earlier) Cloud Service Integration </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AEM 6.2 (or later) Cloud Service Integration </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col5"> <p>For more information, see <a href="https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html" format="html" scope="external"> Integrating with Adobe Target </a> in the Adobe Experience Manager 6.2 documentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Any activity using a Redirect offer </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col5"> <p>There are stricter minimum requirements for using redirect offers with A4T. For more information, see <a href="c_a4t-faq-redirect-offers.xml#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Redirect Offers - A4T FAQ </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Because all activity types do not yet support A4T, it is recommended that you keep or implement important conversion mboxes, such as the "orderConfirmPage" mbox. 

## Examples of A4T Reports {#section_F0A43A1CB2F04E8282B909E4D7034361}

To view A4T reports in [!DNL  Target], click ** [!UICONTROL  Activities] **, click the desired activity from the list that uses [!DNL  Analytics] as its reporting source > then click the ** [!UICONTROL  Reports] ** tab. 


>[!NOTE]
>
>You can use the [!UICONTROL  Reporting Source] drop-down list at the top of the [!UICONTROL  Activities] page to display only activities that use [!DNL  Analytics] as the reporting source. 



You can toggle between the [!UICONTROL  Table View] (  ![](../target/graphics/icon table view report.png) ) and [!UICONTROL  Graph View] (  ![](../target/graphics/icon graph view report.png) ) of the report by clicking the appropriate icon at the top right side of the report. 

The following illustration shows the [!UICONTROL  Graph View] of an A4T report with the [!UICONTROL  Report Metric] drop-down list displaying the available [!DNL  Analytics] goal metrics: 

![](graphics/a4t report graph1.png) 

The following illustration shows the [!UICONTROL  Graph View] of an A4T report with the [!UICONTROL  Audience] drop-down list displaying the available [!DNL  Analytics] audiences: 

![](graphics/a4t report graph2.png) 

The following illustration shows the [!UICONTROL  Table View] of an A4T report: 

![](graphics/a4t report table.png) 

To view the report in [!DNL  Analytics] rather than in [!DNL  Target], click ** [!UICONTROL  View in Analytics] ** along the top of the report. 
>## Before You Implement {#concept_046BC89C03044417A30B63CE34C22543}Several changes occur in your data collection process when enabling Analytics as the reporting source for Target (A4T). 
<draft-comment otherprops="merge">
  a4t/c_before_implement.xml 
</draft-comment>This video explains how to use Adobe Analytics as a reporting source in Adobe Target to drive the analysis of your optimization program. 



<table id="table_215B5503BFAC4E71B1C391B6FBA255AC"> 
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
     <ul id="ul_3864D312D22F45B291E771CFC0C08F49"> 
      <li id="li_DDFA641B86D64EE18B078EA39370C3B2"> <p>Explain what A4T is and why you would use it </p> </li> 
      <li id="li_361537A9114B4FFA99AE24EAC775686D"> <p>Explain how A4T works </p> </li> 
      <li id="li_0E580D91F89B4F7C9DAE0E8E39E2D084"> <p>Understand the prerequisites needed before using A4T </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Before you decide to use this integration, review the following sections and consider the impact to your reporting processes: 

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
      <li id="li_3D79F3BD5B52402A8DC81875F510370B"> <p>Marketing Cloud Visitor ID Service: <span class="filepath"> visitorAPI.js </span> version 1.8.0. </p> </li> 
      <li id="li_351A2616F18444DF951F16A977BD9FAC"> <p>Adobe Target (depending on your implementation): <span class="filepath"> at.js </span> version 0.9.1 or <span class="filepath"> mbox.js </span> version 61. </p> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p>To use redirect offers with A4T, you must implement the following library versions (or newer): </p> <p id="p_A816444144144867B5266CA4D5F69F4A"> 
     <ul id="ul_1FE7990C3F51461EAD3A1FA03EB40FC4"> 
      <li id="li_48BFEAC3E7964DA98BB49BE1725E3F26"> <p>Marketing Cloud Visitor ID Service: <span class="filepath"> visitorAPI.js </span> version 2.3.0 or later. </p> </li> 
      <li id="li_A3EEB21E43C54D62B039154CB2E75168"> <p>Adobe Analytics: <span class="filepath"> appMeasurement.js </span> version 2.1. </p> </li> 
      <li id="li_2F6C0B81896E4247A10E31B63EC08720"> <p>Adobe Target: <span class="filepath"> at.js </span> version 0.9.6 or later. </p> <p>The <span class="filepath"> mbox.js </span> library does not support redirect offers with A4T. Your implementation must use <span class="filepath"> at.js </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Download and deployment instructions are listed in [ Adobe for Target Implementation ](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_a4timplementation.html). 

## Things to Know Before You Implement {#section_50D49CC52E11414089C89FB67F9B88F5}


* This integration is enabled on new activities when you select to use Analytics as the reporting source. After you make the implementation changes described in this document, your existing activities are not impacted. 

* The process of setting up Analytics as the reporting source for Target includes several implementation steps, followed by a provisioning step. It is a good idea to read through the process as described below before implementing. After you complete these steps, you will be ready to use Analytics as your reporting source as soon as it is enabled for you. The provisioning process can take up to five business days. 

* The Visitor ID service creates a shared Visitor ID across the Marketing Cloud. While it does not replace the Target mboxPC id or Audience Manager UUID, it does replace the way Analytics identifies new visitors. If set up properly, returning Analytics visitors should also be identified via their old Analytics ID to prevent visitor cliffing. Similarly, because the Target mboxPCid remains intact, no Target visitor profile data is lost when you upgrade to the Visitor ID service. 

* The Visitor ID service must execute before your Analytics and Target page code. Make sure that ` VisitorAPI.js` appears above the tags for all other Marketing Cloud products. 


## Latency {#section_9489BE6FD21641A4844E591711E3F813}

After this integration is enabled, you will experience an additional 5-10 minutes of latency in Adobe Analytics. This latency increase allows data from Analytics and Target to be stored on the same hit, allowing you to break down tests by page and site section. 

This increase is reflected in all Adobe Analytics services and tools, including the live stream and real-time reporting, and applies in the following scenarios: 

* For live stream, real-time reports &amp;amp; API requests, and current data for traffic variables, only hits with a supplemental data ID are delayed. 

* For current data on conversion metrics, finalized data, and data feeds, all hits are delayed an additional 5-7 minutes. 

Be aware that the latency increase starts after you implement the Marketing Cloud visitor ID service, even if you have not fully implemented this integration. 

## Supplemental ID {#section_2C1F745A2B7D41FE9E30915539226E3A}

All Target calls used by an A4T activity to deliver content or record the goal metric must have a corresponding Analytics hit that shares the same supplemental ID for A4T to work properly. 

Hits that contain data from Analytics and Target contain a supplemental data ID. You can see this ID in the [ Adobe Debugger ](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=debugger) as the ` sdid` parameter. For example: ` sdid=2F3C18E511F618CC-45F83E994AEE93A0`. This ID is generated anytime the following criteria are in place: 

* The visitor ID service is in implemented 

* A version of [!DNL  mbox.js] that supports this integration is implemented. 

When troubleshooting, be sure to confirm that the supplemental ID is present on Analytics hits. 
>## Analytics for Target Implementation {#concept_CE78750AC2A4487D8ACD9369B3EAC85A}Several steps are required when implementing 
<keyword>
  Adobe Analytics 
</keyword> as the reporting source for 
<keyword>
  Target 
</keyword> (A4T). 
<draft-comment otherprops="merge">
  a4t/c_a4timplementation.xml 
</draft-comment>
## Implementation Steps {#section_73961BAD5BB4430A95E073DE5C026277}

The following table describes the steps required to deploy this integration to your site. 

<table id="table_1683413EA0E34DBC9291832647B68E96"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Step </th> 
   <th colname="col1" class="entry"> Task </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <img href="graphics/step1_icon.png" id="image_21F30BBFC0A249F8B0E1A50EBBEED77D" /> </td> 
   <td colname="col1"> <p>Request provisioning for Analytics and Target. </p> </td> 
   <td colname="col2"> <p>After you implement <span class="keyword"> Analytics </span> as the reporting source for <span class="keyword"> Target </span>, you must be provisioned for <span class="keyword"> Analytics </span> and <span class="keyword"> Target </span>. Use <a href="http://www.adobe.com/go/audiences" format="http" scope="external"> this form </a> to request to be provisioned. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img href="graphics/step2_icon.png" id="image_76B61DEABE3849CCB39135FDD7399EAA" /> </td> 
   <td colname="col1"> <p>Set up user permissions </p>. </td> 
   <td colname="col2"> <p>User account requirements must be met before you can create an <span class="keyword"> Adobe Analytics </span>-based activity in <span class="keyword"> Adobe Target </span>. See <a href="a4t.xml#concept_4BC06CAB00BF46FF9362AFE98656B083" format="dita" scope="local"> User Permission Requirements </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img href="graphics/step3_icon.png" id="image_9933AC9D3A884BD9814A6B697610CAE9" /> </td> 
   <td colname="col1"> <p>Implement the Marketing Cloud Visitor ID service. </p> </td> 
   <td colname="col2"> <p>The visitor ID service lets you identify users across <span class="keyword"> Marketing Cloud </span> solutions. You must implement or migrate to the required version of the Marketing Cloud Visitor ID. For more information, see "Implementation Requirements" in <a href="a4t.xml#concept_046BC89C03044417A30B63CE34C22543" format="dita" scope="local"> Before You Implement </a>. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-target.html" format="html" scope="external"> Implement the Marketing Cloud ID Service for Target </a> in the <i>Marketing Cloud Visitor ID Service documentation</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img href="graphics/step4_icon.png" id="image_844E896941E2489A943BE10AD710ED36" /> </td> 
   <td colname="col1"> <p>Update AppMeasurement for JavaScript or s_code. </p> </td> 
   <td colname="col2"> <p>You must implement or migrate to the required version of <span class="codeph"> appMeasurement.js </span>. For more information, see "Implementation Requirements" in <a href="a4t.xml#concept_046BC89C03044417A30B63CE34C22543" format="dita" scope="local"> Before You Implement </a>. </p> <p>For new implementations, see <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=js_implementation" format="https" scope="external"> Analytics JavaScript Implementation </a>. </p> <p>For a migration, see <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=appmeasure_mjs_migrate" format="http" scope="external"> Migrating to AppMeasurement for JavaScript </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img href="graphics/step5_icon.png" id="image_1C4293CA98F04EE2ADA69EAB95BDE8B1" /> </td> 
   <td colname="col1"> <p>Download and update <span class="codeph"> at.js </span> or <span class="codeph"> mbox.js </span>. </p> </td> 
   <td colname="col2"> <p>You must implement or migrate to the required version of <span class="codeph"> at.js </span> or <span class="codeph"> mbox.js </span> using your production account. No modifications are required on the code. </p> <p>For more information, see "Implementation Requirements" in <a href="a4t.xml#concept_046BC89C03044417A30B63CE34C22543" format="dita" scope="local"> Before You Implement </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col01"><image href="graphics/step3_icon.png" id="image_02CFDC007BF1486AA312698EBFFA79F7"></image> </entry> <entry colname="col1"> <p>Edit <codeph>mbox.js</codeph> </p> </entry> <entry colname="col2"> <p>On the <uicontrol>Mbox Edit</uicontrol> page in Adobe Target, add the following code to the <uicontrol>Extra JavaScript</uicontrol> portion of your <codeph>mbox.js</codeph> file: </p> <codeblock outputclass="syntax javascript">document.write('&lt;script&nbsp;src="'&nbsp;+&nbsp;document.location.protocol&nbsp;+&nbsp;'//cdn.tt.omtrdc.net/cdn/target.js"&gt;&lt;/script&gt;');</codeblock> </entry> </row> --> 
  <tr> 
   <td colname="col01"> <img href="graphics/step6_icon.png" id="image_C17DA86A4D9A483DB862F5970A1EEEF1" /> </td> 
   <td colname="col1"> <p>Host <span class="codeph"> mbox.js </span> or <span class="codeph"> at.js </span>. </p> </td> 
   <td colname="col2"> <p>If you previously deployed <span class="codeph"> mbox.js </span> or <span class="codeph"> at.js </span>, you can replace your existing file with the updated version. For more information, see "Implementation Requirements" in <a href="a4t.xml#concept_046BC89C03044417A30B63CE34C22543" format="dita" scope="local"> Before You Implement </a>. </p> <p>Otherwise, this file can be hosted along with the Visitor ID service and AppMeasurement for JavaScript files. These files must be hosted on a web server that is accessible to all pages on your site. You need the path to these files in the next step. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img href="graphics/step7_icon.png" id="image_CA8C5C4F0B7C40CEBFD7725663EE7BFD" /> </td> 
   <td colname="col1"> <p>Reference <span class="codeph"> at.js </span> or <span class="codeph"> mbox.js </span> on all site pages. </p> </td> 
   <td colname="col2"> <p> Include <span class="codeph"> at.js </span> or <span class="codeph"> mbox.js </span> below <span class="codeph"> VisitorAPI.js </span> by adding the following line of code in the <span class="codeph"> &amp;lt;head&amp;gt; </span> tag on each page: </p> <p>For <span class="codeph"> at.js </span>: </p> 
    <codeblock class="syntax html">
      &lt;script&nbsp;language="JavaScript"&nbsp;type="text/javascript"&nbsp; 
     src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"&gt;&lt;/script&gt; 
    </codeblock> <p>For <span class="codeph"> mbox.js </span>: </p> 
    <codeblock class="syntax html">
      &lt;script&nbsp;language="JavaScript"&nbsp;type="text/javascript"&nbsp; 
     src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/mbox.js"&gt;&lt;/script&gt; 
    </codeblock> <p>It is essential that <span class="codeph"> VisitorAPI.js </span> is loaded before <span class="codeph"> at.js </span> or <span class="codeph"> mbox.js </span>, so if you are updating an existing <span class="codeph"> at.js </span> or <span class="codeph"> mbox.js </span> file, make sure that you verify the load order. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img href="graphics/step8_icon.png" id="image_D44ABBFE1308454B955F733D2E6C88EA" /> </td> 
   <td colname="col1"> <p>Validate the implementation. </p> </td> 
   <td colname="col2"> <p>Load your pages after you have updated the JavaScript libraries to confirm that the <span class="codeph"> mboxMCSDID </span> parameter values in Target calls match the <span class="codeph"> sdid </span> parameter value in the Analytics page-view call. </p> <p>This is especially important to confirm in Single Page Applications (SPAs) where the order of calls is not always predictable. </p> <p> <p>Note:  The matching of these values is required in order for A4T to function correctly. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img href="graphics/step9_icon.png" id="image_57C8A469F046405D87CEEECBD8B37815" /> </td> 
   <td colname="col1"> <p>(Optional) Remove previous integration code. </p> </td> 
   <td colname="col2"> <p>We recommend that you remove the previous integration to simplify your implementation and eliminate the need to sort out discrepancies between the systems. You can remove any code you might have deployed for a previous SC to T&amp;T integration, including <span class="codeph"> mboxLoadSCPlugin </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img href="graphics/step10_icon.png" id="image_9F30EFDCBBE140368431A18F39B50DE5" /> </td> 
   <td colname="col1"> <p>Enable the options for using Analytics as the reporting source for Target. </p> </td> 
   <td colname="col2"> <p>In <span class="keyword"> Target </span>, click <span class="uicontrol"> Setup </span> &gt; <span class="uicontrol"> Preferences </span> and choose either <span class="uicontrol"> Select per activity </span> or <span class="uicontrol"> Adobe Analytics </span> to enable the options. </p> <p> 
     <ul id="ul_151FF5A080E14A10879710E599626DD6"> 
      <li id="li_25DB177CEC6142A9A5039D0A6E892BEB"> <span class="uicontrol"> Select per activity </span> lets you choose between <span class="keyword"> Target </span> and <span class="keyword"> Analytics </span> when creating each activity. </li> 
      <li id="li_DFD453742EA245DBB827E6F3C02362D4"> <span class="uicontrol"> Adobe Analytics </span> sets <span class="keyword"> Analytics </span> as the reporting source for all activities that you create. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## User Permission Requirements {#concept_4BC06CAB00BF46FF9362AFE98656B083}User account requirements to create an Adobe Analytics-based activity in Adobe Target (A4T). 
<draft-comment otherprops="merge">
  a4t/c_account_reqs.xml 
</draft-comment>Before a report suite can be selected when defining an Analytics activity, you need both an Analytics user account and a Target user account. Your user accounts must be configured as described in the following sections: 

## Adobe Marketing Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

See [ Join the Marketing Cloud ](https://marketing.adobe.com/resources/help/en_US/mcloud/link_accounts.html) for more information. 

* **Linked Accounts**. Your Analytics and Target user accounts must be linked to your Adobe ID. To verify, open ** [!UICONTROL  Account Settings] ** > ** [!UICONTROL  Organization &amp;amp; Product Access] **. 
  ![](graphics/linking.png)
* **Marketing Cloud group membership**. You must be a member of one or more Marketing Cloud groups that have access to Analytics and Target. Verify that ** [!UICONTROL  Analytics] ** and ** [!UICONTROL  Target] ** appear in the ** [!UICONTROL  Marketing Apps] ** section of the left navigation: 
  ![](graphics/analytics-target-access.png) Also verify that when you click on Analytics you see your full Analytics account. If you only see a welcome page with no access to your data, relink your account. 


## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}


* **Analytics report suite access: **Before creating or viewing reports for an Analytics-powered activity, you must be a member of the ** [!UICONTROL  All Report Access] ** group, or member of a group that has access to at least one report in the report suite that you want to use. If you are unable to view reports, make sure you are a member of one of these groups. See [ Groups ](https://marketing.adobe.com/resources/help/en_US/reference/groups.html) for more information. 

* **Web Services Access Group: ** You must belong to the Web Services Access group in Adobe Analytics to be able to use Analytics as the reporting source for Target. 


## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

No additional privileges are required. 
>## Activity Creation {#task_FE48F7B077C44A5BA015B087428412EF}You can configure an activity in Target Standard/Premium to use Adobe Analytics as the reporting source (A4T). 
<draft-comment otherprops="merge">
  a4t/t_campaign_creation.xml 
</draft-comment>Before you set up an activity that uses Analytics as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks on your shopping cart. Choose a final success metric for the activity. Although you can select additional metrics at any time in Analytics, you must still specify a particular metric you expect this test to affect. 

**Target Standard/Premium** 

Creating a Target Standard activity that uses Analytics as the reporting source is similar to setting up a regular Target Standard activity, with a few important differences. For example, you cannot select a segment for reporting while creating the activity because all segments available in Analytics can be applied when viewing a report. 

>1. Click ** [!UICONTROL  Create Activity] **.


>       >[!NOTE]
>       >
>       >An activity name cannot include the "%" character if Analytics is used as the reporting source.

>1. Select the activity type and begin setting up the activity.
>1. When you get to the ** [!UICONTROL  Settings] ** portion of the activity creation flow, choose ** [!UICONTROL  Adobe Analytics] ** and specify your company.
>1. Select a report suite.

>       You can choose any report suite that is available to you in Adobe Analytics. The report suite defines where the collected data will be available. Virtual report suites are not included in the report suite list. 

>       You might encounter two possible errors while selecting the report suite: 

>    
>    * You get an error that no report suites are available, but your account is properly set up. 

>      You might need to check your Analytics company. If your Marketing Cloud account is tied to more than one Analytics company, log out of Target, and log in to Analytics under the right company. Then return to Target, and the report suites will load. 

>    * You don't see the report suite that you expect. 

>      Only report suites that are provisioned to connect to Adobe Target will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the Adobe Marketing Cloud to try again. 



>       If the report suite(s) is still missing from the list, please [ contact Customer Care ](r_release_notes.md#reference_ACA3391A00EF467B87930A450050077C). 
>1. Specify your tracking server.

>       See [ Using an Analytics Tracking Server ](a4t.md#task_72077BA7E93C4A65A715A18F32228823). 


>       >[!NOTE]
>       >
>       >If you use Adobe Analytics as your activity's reporting source, you do not need to specify a tracking server during activity creation if you are using ` mbox.js` version 61 (or later) or ` at.js` version 0.9.1 (or later). The ` mbox.js` or ` at.js` library automatically sends tracking server values to [!DNL  Target]. During activity creation, you can leave the [!UICONTROL  Tracking Server] field empty on the [!UICONTROL  Goals &amp;amp; Settings] page. 

>1. Define the experience.
>1. Specify the activity goal.

>       You are required to select a success metric to use as a goal for each test. Your activity goal is the conversion activity that signals a successful activity. It is best practice never to run a test without having a goal to improve in some specific way. You can choose any Analytics metric available in the Analytics metric selector. 


>       >[!NOTE]
>       >
>       >You can send a custom Target-based metric to Analytics rather than relying only on Analytics data. For example, you can monitor clicking on a page, which is usually not tracked by Analytics. This custom metric is sent to Analytics automatically from the Target server, and appears as the "Target Conversion" metric in the metrics selector in Analytics. The Target Conversion metric is empty if you choose to use Analytics metrics.


>       Setting a goal doesn't mean you can't use another metric when evaluating test results. The goal is, however, a reminder of the one thing you want to improve with the activity. 

>       The visitor remains in the activity after they reach the goal. The visitor continues to see activity content but is not counted as a new activity entry. 


>       >[!NOTE]
>       >
>       >When setting up an activity after setting up Analytics as your reporting source, there is no option to set up audiences for reporting. Analytics segments are available in the Target Activities report.

>1. Click ** [!UICONTROL  Save] **.

>## Using an Analytics Tracking Server {#task_72077BA7E93C4A65A715A18F32228823}If you are using an older version of 
<codeph>
  at.js 
</codeph> or 
<codeph>
  mbox.js 
</codeph>, you must specify an analytics tracking server for activities that use Analytics for Target (A4T). 
<draft-comment otherprops="merge">
  a4t/t_analytics_tracking_server.xml 
</draft-comment>
>[!NOTE]
>
>If you use Adobe Analytics as your activity's reporting source, you do not need to specify a tracking server during activity creation if you are using ` mbox.js` version 61 (or later) or ` at.js` version 0.9.1 (or later). The ` mbox.js` or ` at.js` library automatically sends tracking server values to [!DNL  Target]. During activity creation, you can leave the [!UICONTROL  Tracking Server] field empty on the [!UICONTROL  Goals &amp;amp; Settings] page. 



To ensure that data from Target goes to the correct location in Analytics, A4T requires an analytics tracking server to be sent in all calls to Modstats from Target. For implementations using multiple tracking servers you can use the Adobe Marketing Cloud Debugger to determine the correct tracking server for your activity. 

The debugger should be viewed on a page where the activity will be delivered to ensure you select the correct tracking server. You can also specify a default tracking server for each account. Contact Customer Care to specify or modify the default. 

>1. From the page on which you are creating your activity, open the Adobe Marketing Cloud Debugger.

>       If you have not installed the debugger, follow the [ Adobe Debugger installation instructions ](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger_install.html). 

>       ![](graphics/Screen_DebuggerTrackServ.png) 

>       The analytics tracking server is found in the SiteCatalyst Image section of the debugger. The field is called *First Party Cookies* or *Third Party Cookies* depending on the implementation, and the Analytics tracking server value will be in one of these formats: >    
>    * (for CNAME implementations) 

>    * (for non-RDC implementations) 

>    * (for RDC implementation) 



>       *Company* represents the Analytics company name, *metrics* is an example of a CNAME value, and *d1* is an example of an Analytics data center. 
>1. Copy the entire contents of the field.
>1. In the [!UICONTROL  Reporting Settings] section of the [!UICONTROL  Goal &amp;amp; Settings] screen of your activity, paste the tracking server information in the ** [!UICONTROL  Tracking Server] ** field.


>       >[!NOTE]
>       >
>       >You must select Adobe Analytics as the Reporting Source for your activity for the Tracking Server field to be available.

>## Reporting {#concept_716AF8D545AD404EAAEE99A6DB7B9483}Using Analytics as your reporting source for Target (A4T) gives you access to Analytics reports for your Target activities. 
<draft-comment otherprops="merge">
  a4t/c_reporting.xml 
</draft-comment>You can view reports for your activities in both Analytics and Target Standard/Premium. 

## Overview {#section_035A62D65608423285D8A5A54731E2C5}

Both Analytics and Target reports measure entrants (the people who enter the tests), rather than visitors to the site. 

Every time a visitor sees activity content on the page, Target makes a direct server-to-server call to Analytics, including which activity and experience the visitor saw. Target also calls Analytics whenever the conversion is made. Analytics adds the conversion as a specific new Analytics event named "Activity Conversion," which is tracked along with other data collected by Analytics. 

When the Select operation is used and you sort on *Entrants*, then only experiences that received entrants during the selected time period are displayed in the reports. 


>[!NOTE]
>
>Reports powered by Target have a latency of four minutes. For activities powered by A4T, in both the Target and Analytics reports, it can take up to 24 hours after the activity is initially saved before the report data can be broken down by experiences. The data collected in that first 24 hours is still accurate and is assigned to the right experience.



## Reports in Analytics {#section_F6884872DC864AE7913587FAED4CD11C}

In Analytics, click ** [!UICONTROL  Target] ** > ** [!UICONTROL  Target Activities] ** in the left menu. In Target, the activity's reports automatically show Analytics data, metrics, and segments. Data appears in these reports approximately an hour after it is collected from the site. All metrics, audiences, and values in the reports come from the report suite you selected when you set up the activity. 

In Analytics, use the Target Activities report to view the results of your Target activity. Test&amp;Target (Legacy) Reports provides information about your old Test&amp;Target plug-in style page integrations and does not include Analytics for Target data. In the Activities report, view information about your Target experiences. Click ** [!UICONTROL  Metrics] **, then select the ** [!UICONTROL  Target] ** metric type. Two metrics are available for your report: 


* **Activity Entries: **Matches the Entrants number in the Target report. 

* **Activity Conversions: **Matches the Custom Conversions number in the Target report. 




>[!NOTE]
>
>Target lift and confidence details are also available in Analytics. For more information, see[ Target Lift and Confidence Report Type ](https://marketing.adobe.com/resources/help/en_US/reference/report_target_lift_confidence.html) in the Adobe Analytics product documentation. 





<table id="table_AB508EF6FCC644BEB3E4A874E70565C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <img href="graphics/warning.jpg" id="image_38751CD382D741D09736B02A609DD863" /> </td> 
   <td colname="col2"> <p>If your Target Activities report in Analytics lists "unspecified" instead of listing your activities, an update is required to your provisioned account. Please contact Customer Care to resolve this issue. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Reports in Target {#section_C0D1F17F88374B6690BF904D7B83B42E}

When Analytics is used as the reporting source, reports in Target Standard show the data gathered from Analytics. The report differs somewhat from other Target Standard reports: 


* The Audiences list shows the audiences available to your Analytics report suite. 

* The Metric list shows every metric available through Analytics. 

  Every metric is available, including any custom or calculated metrics that are built-in in Analytics. 

  Be aware that any numbers that increase are shown as positives in the report, even when an increase is actually undesired. For example, even though you want a lower bounce rate, the higher bounce rate is shown as the winner with highest lift. Be aware of these and similar metrics, and whether you'd prefer to decrease or increase the numbers, when making decisions based on your reports. 



You can apply the metric or audience to the report in Target after the test has started, or even after the test has completed. You don't have to know exactly what you want to measure beforehand. 

Click to view the full Analytics report directly from the activity report page. 

## Activity Creation {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

During activity creation, you must specify a goal for the activity on the [!UICONTROL  Settings] page. This goal becomes the default metric for the report and is always listed as the first option in the metrics selector. You cannot select segments for reporting like you would for a regular Target activity. A test with Analytics uses Adobe Analytics segments rather than Target Standard audiences. 

## Performing Offline Calculations for Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

You can perform offline calculations for A4T, but it requires a step with data exports in [!DNL  Analytics]. 

For more information, see [ Performing Offline Calculations for Analytics for Target (A4T) ](c_reports.md#section_B34BD016C8274C97AC9564F426B9607E). 
