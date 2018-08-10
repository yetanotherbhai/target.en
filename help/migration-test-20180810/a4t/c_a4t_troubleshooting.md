---
description: This topic covers some common issues that have been encountered when using Analytics as the reporting source for Target (A4T).
keywords: partial data;partial-data;A4T;discrepancies;analytics for target;orphaned;virtual report suite;phantom;troubleshooting;unstitched;inflated;unspecified
seo-description: This topic covers some common issues that have been encountered when using Analytics as the reporting source for Target (A4T).
seo-title: Troubleshooting Analytics and Target Integration (A4T)
solution: Target
subtopic: Multivariate Test
title: Troubleshooting Analytics and Target Integration (A4T)
topic: Standard
uuid: 7f1a308b-2446-4bd8-83ba-3a9bd700e6ab
index: y
internal: n
snippet: y
translate: y
---

# Troubleshooting Analytics and Target Integration (A4T)


## Activities do not show data in Analytics , but are instead listed as "unspecified." {#section_EB97F0499B0E40E69A21C30DC539BF67}

There are several reasons why this could happen: 


* Classification in [!DNL  Target] hasn't fully processed. 

  Classification can take as many as 24 hours to process from the first save of the activity. 

* The report suite doesn't contain any data, but [!DNL  Target] has tried to classify hits. [!DNL  Target] cannot classify data until the first hit occurs. 

  Ensure that the report suite has had at least one hit. 

* The classification call from [!DNL  Target] to [!DNL  Analytics] failed. 

  [ Contact Customer Care ](r_release_notes.md#reference_ACA3391A00EF467B87930A450050077C) for assistance. 



Sometimes data displays correctly in reports, but then reverts back to "unspecified" because a new activity was added that hasn’t completed classification. Remember that it can take as many as 24 hours to classify reports after the first save. 


>[!NOTE]
>
>No data is lost when listed as "unspecified." The data is properly assigned to the appropriate activity or experience after the classification runs.



## My Analytics data shows an inflated visit or visitor count since starting A4T. {#section_4BE374E573D44FB7918611699B74F58E}

For more information, see [ Minimizing Inflated Visit and Visitor Counts in A4T ](c_a4t_troubleshooting.md#concept_A515C2DE126E44B6AD97754C2C6D5235). 

## Estimated lift in revenue metric does not show correct data. {#section_35D766E5E4D347C39E15D08AA883FBB0}

Lift and confidence details are not available in Analytics. They are, however, available in the Target reports. 

## Activities do not appear in Analytics reports. {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

A4T activities require an analytics tracking server to be specified. See [ Using an Analytics Tracking Server ](a4t.md#task_72077BA7E93C4A65A715A18F32228823) to make sure your Analytics Tracking Server is set up correctly. 


>[!NOTE]
>
>If you use Adobe Analytics as your activity's reporting source, you do not need to specify a tracking server during activity creation if you are using ` mbox.js` version 61 (or later) or ` at.js` version 0.9.1 (or later). The ` mbox.js` or ` at.js` library automatically sends tracking server values to [!DNL  Target]. During activity creation, you can leave the [!UICONTROL  Tracking Server] field empty on the [!UICONTROL  Goals &amp;amp; Settings] page. 



## My Analytics segments don't appear in Target. {#section_DEE87F1557834F448E99381D3D02EEEF}

Make sure you have the right permissions before you start creating A4T activities: 


* You must belong to the Web Services Access group in Adobe Analytics to be able to use Analytics as the reporting source for Target. 

* You must be a member of one or more Marketing Cloud groups that have access to Analytics and Target. 

* Verify that Analytics and Target appear in the Marketing Apps section of the left navigation. 



## Bounce rates, bounces, and exits metrics appear as positives in reports. {#section_B5C3D56EF0344407AE67ABEB93037F5A}

This is a known issue. 

Although these metrics are negative, the lift is shown as if they were positive in the Target reports. For example, even though you want a lower bounce rate, the higher bounce rate is shown as the winner with highest lift. Be aware of these and similar metrics, and whether you'd prefer to decrease or increase the numbers, when making decisions based on your reports. 

## The report suite I need does not appear. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

The list of report suites that appears in Target Standard/Premium is the list of report suites that have been configured for Analytics as the reporting source for Target. This means you might not see every report suite you have. If you don't see the report suite you are looking for, you should contact Client Care to get it enabled. 

## I'm not seeing as much data in reports as expected. {#section_75002584FA63456D8D9086172925DD8D}

Review your implementation, especially on pages where your visitors qualify for experiences and ensure that the supplemental data IDs match in the [!DNL  Target] and [!DNL  Analytics] calls. In the [!DNL  Target] call, the supplemental ID is contained in the ` mboxMCSDID` parameter. In the [!DNL  Analytics] call, the supplemental ID is contained in the ` sdid` parameter. 

If there is no supplemental data ID in the [!DNL  Target] call, confirm that the [!DNL  VisitorAPI.js] file is loaded before [!DNL  at.js] or [!DNL  mbox.js]. If there is no supplemental data ID in the [!DNL  Analytics] call, confirm that the [!DNL  Target] call fires before the [!DNL  Analytics] call. 

For more information, see [ Analytics for Target Implementation ](a4t.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) or contact [ Customer Care ](r_release_notes.md#reference_ACA3391A00EF467B87930A450050077C). 


<table id="table_08DC686833144E6BAB92A78A98B56CAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>On November 14, 2016, <span class="keyword"> Adobe Analytics </span> changed the way some data is processed for customers using <span class="keyword"> Analytics </span> reporting for <span class="keyword"> Target </span> (A4T). These changes bring <span class="keyword"> Adobe Target </span> data into better alignment with the data model for <span class="keyword"> Adobe Analytics </span>. These changes were rolled out for all customers using A4T. These changes specifically address an issue where some customers have noticed an inflated visitor count when <span class="keyword"> Target </span> activities are running. </p> <p> <p>Note:  This change is not retroactive. If your historical reports show inflated counts, and you would like to exclude them from your reports, you can create a virtual report suite, as explained below. </p> </p> <p>Additionally, several JavaScript libraries have been updated to help minimize inflated counts. We recommend that you upgrade to the following library versions (or newer): </p> <p id="p_A816444144144867B5266CA4D5F69F4A"> 
     <ul id="ul_1FE7990C3F51461EAD3A1FA03EB40FC4"> 
      <li id="li_48BFEAC3E7964DA98BB49BE1725E3F26"> <p>Marketing Cloud Visitor ID Service: <span class="filepath"> visitorAPI.js </span> version 2.3.0 or later. </p> </li> 
      <li id="li_A3EEB21E43C54D62B039154CB2E75168"> <p>Adobe Analytics: <span class="filepath"> appMeasurement.js </span> version 2.1. </p> </li> 
      <li id="li_2F6C0B81896E4247A10E31B63EC08720"> <p>Adobe Target: <span class="filepath"> at.js </span> version 0.9.6 or later. </p> <p>The <span class="filepath"> mbox.js </span> library does not support redirect offers with A4T. Your implementation must use <span class="filepath"> at.js </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## What Changed? {#section_9CCF45F5D66D48EBA88F3A178B27D986}

When [!DNL  Adobe Analytics] is used to measure [!DNL  Target] activities (called A4T), [!DNL  Analytics] collects additional data that is not available when there is no [!DNL  Target] activity on the page. This is because the [!DNL  Target] activity fires a call at the top of the page, but [!DNL  Analytics] typically fires its data collection calls at the bottom of the page. In the implementation of A4T to date, we included this additional data whenever a [!DNL  Target] activity was active. Going forward, we will include this additional data only when both the [!DNL  Target] and [!DNL  Analytics] tags have fired. 

## Why did Adobe Making this Change? {#section_92380A4BD69E4B8886692DD27540C92A}

Adobe prides itself on data accuracy and quality. When the [!DNL  Target] tag fires, but the [!DNL  Analytics] tag does not, we are recording “partial data” (sometimes called "unstitched hits"), which would not be captured by [!DNL  Analytics] were there no [!DNL  Target] activity. Although including this partial data in [!DNL  Analytics] reporting does provide additional information, it also creates inconsistency with historical data from periods when there were no [!DNL  Target] activities running. This can cause problems for [!DNL  Analytics] users who are analyzing trends over time. In the interest of ensuring data consistency in [!DNL  Analytics], we will be excluding all partial data. 

## What Contributes to Partial Data? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

We have seen some customers with very high rates of partial data in [!DNL  Analytics]. This can result from improper implementation, but there are legitimate causes as well. 

The identified causes of partial data include the following: 


* **Misaligned Report Suite IDs (Implementation): **The report suite specified during activity setup does not match the report suite on the page where the test is delivered. This looks like partial data because the data cannot be reconciled on [!DNL  Analytics] servers. 

* **Slow Pages: **Because [!DNL  Target] calls are at the top of the page and [!DNL  Analytics] calls are typically at the bottom of the page, if the page loads slowly, it increases the likelihood of a visitor leaving the page after the [!DNL  Target] call fires, but before the [!DNL  Analytics] call. This can be especially problematic on mobile web sites where connections are often slower. 

* **Page Errors: **If there are JavaScript errors or other scenarios where each of the touchpoints do not fire (Marketing Cloud ID service, Target, and Analytics), partial data will result. 

* **Redirect Offer(s) in Target Activity: **Redirect offers immediately send a user to a different page, which means the [!DNL  Analytics] call does not fire on the first page. 


  >[!NOTE]
  >
  >After November 14, 2016, customers will no longer be able to create A4T activities with redirect offers.


* **Old Versions of the Libraries: **Over the past year Adobe has made several improvements to our JavaScript libraries ( [!DNL  appMeasurement.js], ` at.js/mbox.js`, and ` visitorAPI.js`) to make sure data is sent as efficiently as possible. To learn more about implementation requirements, see [ Before You Implement ](a4t.md#concept_046BC89C03044417A30B63CE34C22543). 



## What are the Best Practices to Reduce Partial Data? {#section_065C38501527451C8058278054A1818D}

We recommend reviewing the following steps, in order, to reduce partial data collection: 



<table id="table_46ECBA452D8A4DB692F1CD4E8A1F0B0B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Step </th> 
   <th colname="col2" class="entry"> Task </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <img href="graphics/step1_icon.png" id="image_21F30BBFC0A249F8B0E1A50EBBEED77D" /> </td> 
   <td colname="col2"> <p>Make sure the report suite selected in <span class="keyword"> Target </span> is the same as the one on the page(s) where the activity will be presented. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="graphics/step2_icon.png" id="image_76B61DEABE3849CCB39135FDD7399EAA" /> </td> 
   <td colname="col2"> <p>Ensure the <span class="codeph"> visitorAPI.js </span>, <span class="codeph"> appMeasurement.js </span>, <span class="codeph"> mbox.js </span>/ <span class="codeph"> at.js </span> libraries are on A4T compatible versions. To learn more about implementation requirements, see <a href="a4t.xml#concept_046BC89C03044417A30B63CE34C22543" format="dita" scope="local"> Before You Implement </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="graphics/step3_icon.png" id="image_9933AC9D3A884BD9814A6B697610CAE9" /> </td> 
   <td colname="col2"> <p>Check to make sure the SDID is getting set on all <span class="keyword"> Target </span> and <span class="keyword"> Analytics </span> calls leaving the page and that they match. </p> <p>Do this by using a network analyzer or debugging tool to ensure that the <span class="codeph"> mboxMCSDID </span> parameter on <span class="keyword"> Target </span> call(s) matches the SDID parameter in the <span class="keyword"> Analytics </span> call. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="graphics/step4_icon.png" id="image_844E896941E2489A943BE10AD710ED36" /> </td> 
   <td colname="col2"> <p>Confirm that the implementation libraries load in the correct order on your sites. For more information, see <a href="a4t.xml#concept_CE78750AC2A4487D8ACD9369B3EAC85A" format="dita" scope="local"> Analytics for Target Implementation </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## How Can I See How Much Partial Data I Have? {#section_89B663E2824A4805AB934153508A0F4B}

Although this information is not available directly in [!DNL  Analytics], you can contact Adobe Customer Care to retrieve a Partial Data report. This report is intended to aid in debugging. 

## How Can I View Historical Trends Without Partial Data? {#section_4C9DED560FAD4428B362DDA2064897C3}

Because this processing change affects data only after the release date (November 14, 2016), if you would like to adjust your historical metrics to match, we recommend that you create a segment to exclude partial data. 

The following information relating to this change includes instructions to help you define the segment and apply it to a virtual report suite so that this segment is always applied to your [!DNL  Analytics] views. 

In most situations, a [!DNL  Target]&nbsp;hit is stitched with an&nbsp; [!DNL  Analytics]&nbsp;hit on each webpage. This stitching happens if there is a consistent SDID in both the&nbsp; [!DNL  Target]&nbsp;and [!DNL  Analytics]&nbsp;call and a [!DNL  Marketing Cloud ID] (MCID) in the&nbsp; [!DNL  Analytics]&nbsp;call on the same page. [!DNL  Target] typically has the MCID as well, but if the call to [!DNL  Target] happens before the visitor ID returns, the hit will still be stitched because of the SDID. Also, the user must remain on the page long enough to fire an&nbsp; [!DNL  Analytics]&nbsp;call after a&nbsp; [!DNL  Target]&nbsp;call was fired. This is the ideal scenario. 

**Partial-Data Hits: **Users sometimes don't remain on a page long enough to send an [!DNL  Analytics] call, but [!DNL  Target] has a proper MCID. This results in partial-data hits (hits with no [!DNL  Analytics] page view). If these users come back to your site and view a page containing [!DNL  Analytics] code, they'll be properly counted as returning visitors. These are hits that would have been lost if you had only [!DNL  Analytics] code on the page. Some clients don't want data for these hits because they inflate certain metrics (visits) and deflate other metrics (page views per visit, time per visit, and so forth). You will also see visits without any page views. However, there are still valid reasons for keeping this data. 

To minimize partial-data hits, you can make your page load faster, update to the latest versions of the libraries, or create a [ virtual report suite ](https://marketing.adobe.com/resources/help/en_US/reference/virtual-report-suites.html) that excludes those hits. For step-by-step instructions, see [ Creating Virtual Report Suites ](https://marketing.adobe.com/resources/help/en_US/reference/vrs-create.html) in the [!DNL  Analytics] product documentation. 

The following illustration shows for the segment definition for the virtual report suite: 

![](graphics/ts_a4t.png) 

When creating the virtual report suite, specify the following configuration for the segment definition (as shown in the above illustration): 


<ul class="simplelist"> 
 <li> <b>Show Hit:</b> </li> 
 <li> Analytics for Target: Exists </li> 
 <li> And </li> 
 <li> Page Views: Does not exist </li> 
 <li> And </li> 
 <li> Custom Link Instances: Does not exist </li> 
 <li> And </li> 
 <li> Download Link Instances: Does not exist </li> 
 <li> And </li> 
 <li> Exit Link Instances: Does not exist </li> 
</ul>



**Orphaned Hits:&amp;nbsp;**In fewer situations, users don't remain on the page long enough for an Analytics call and Target didn't get a proper MCID. These are what we define as "orphaned" hits. These hits represent customers that rarely return and they inflate visit and visitor counts inappropriately. 

To minimize these "orphaned" hits, you can create a [ virtual report suite ](https://marketing.adobe.com/resources/help/en_US/reference/vrs-create.html) that excludes those hits, as explained above. 

## What Does this Mean for my Target Reporting? {#section_AAD354C722BE46D4875507F0FCBA5E36}

Once this change occurs, you might see a decrease in new visitors and visits to live tests because Adobe will not process incoming partial data. Conversions and hits to other Analytics metrics will not change. 
