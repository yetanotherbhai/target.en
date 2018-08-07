---
description: This section contains the information you need to successfully transition from Target Classic to Target Standard/Premium.
keywords: operational milestones;migration;migrate from target classic to target standard
seo-description: This section contains the information you need to successfully transition from Target Classic to Target Standard/Premium.
seo-title: Transitioning from Target Classic to Target Standard or Premium
solution: Target
title: Transitioning from Target Classic to Target Standard or Premium
topic: Premium
uuid: e2266fde-7a18-440a-8179-a0185b9c648a
index: y
internal: n
snippet: y
translate: y
---

# Transitioning from Target Classic to Target Standard or Premium

## Transitioning from Target Classic to Target Standard or Premium {#concept_00A8245A46284AEEB145884D4C27562A}This section contains the information you need to successfully transition from Target Classic to Target Standard/Premium.

<table id="table_1DAD8293D4A447D9932083FB9488EAA2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>On November 14, 2017, Target Classic will be decommissioned. For information about Target Classic APIs, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_target-api-documentation.html" format="html" scope="external"> Transitioning from Target Legacy APIs to Adobe I/O </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

If you already have mboxes on your page from a former ` Test&amp;Target`implementation, then these mboxes can still be used in the new interface. The updated ` mbox.js` file is still required, but these mboxes can be selected for activities and edited using the Visual Experience Composer. 
Transitioning from Target Classic to Target Standard/Premium involves the following process:


<table id="table_D073B8829DF1465C8B29D57EB54F894A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Step </th> 
   <th colname="col2" class="entry"> Task </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step1_icon.png" id="image_0050CF8470484B43B5A8012F7302FD7E" /> </td> 
   <td colname="col2"> Understand <a href="c_target-transition-classic-to-standard.xml#concept_2EAFCB49FAC240F18AF247DC26F0DF3F" format="dita" scope="local"> terminology differences </a> between Target Classic and Target Standard/Premium </td> 
   <td colname="col3"> Several terms and concepts have been updated or made more consistent across the Adobe Marketing Cloud </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step2_icon.png" id="image_41D6C134EAD548C1980D1C56CC4CB7D0" /> </td> 
   <td colname="col2"> Log in to the Marketing Cloud. </td> 
   <td colname="col3"> <p>See <a href="c_getting_started.xml#task_5467C72DAFCB4BB583762CAAFC00A5CF" format="dita" scope="local"> Access Target from the Marketing Cloud </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step3_icon.png" id="image_D31FE4FDBC7141C292D5AD2B00F400F8" /> </td> 
   <td colname="col2"> Consider how some <a href="c_target-transition-classic-to-standard.xml#concept_D8DB7801889A464D9197A739F7B185A7" format="dita" scope="local"> Target Classic advanced features </a> change in Target Standard/Premium. </td> 
   <td colname="col3"> <p>When considering advanced features, you must:</p> <p> 
     <ul id="ul_B434B4D469084E18B2E924A85587AE34"> 
      <li id="li_9526E63734254CAB85C6D8FA121265B2">Migrate the advanced features you use.</li> 
      <li id="li_E6E18351C9E24DB79102566B7E8D4548">Recognize that some advanced features are not necessary for migration, either because they are implemented differently in Target Standard/Premium or they are not supported.</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step4_icon.png" id="image_4C429EEA1589439CB117348B2EEF4409" /> </td> 
   <td colname="col2"> Complete a series of <a href="c_target-transition-classic-to-standard.xml#concept_E0415E44D209458DA30D8A207D08048E" format="dita" scope="local"> operational milestones </a> to make sure your migration to Target Standard/Premium is successful. </td> 
   <td colname="col3"> <p> 
     <ol id="ol_856FDD76806C46A48F71C8ACAE09C7AD"> 
      <li id="li_1A8D0414D37A4BDBB8A65C24435C3AF9"> <a href="../ov2/c_target-implement.xml#concept_60B748DE4293488F917E8F1FA4C7E9EB" format="dita" scope="local"> Deploy either mbox.js or at.js </a> on your site. </li> 
      <li id="li_B03B24268B694738988CD249553D95BB">Deactivate and archive or delete Target Classic activities when they end.</li> 
      <li id="li_F72684DBE4B7443CA79B3C1BBB1E10AB">Move evergreen activities to Target Standard/Premium.</li> 
      <li id="li_713D296DCD944C739C74142C7D4A1F88">Rebuild your <a href="../target/c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> audiences </a> in Target Standard/Premium. </li> 
      <li id="li_4CA965C210124C31AF925362E5214345">Create all of your new <a href="../target/c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> activities </a> in Target Standard/Premium </li> 
      <li id="li_A8EA4D8E564841299EE0E5BCA016A638">Run a test using the <a href="../target/c_experiences.xml#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Visual Experience Composer </a>. </li> 
     </ol> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Transition FAQ {#concept_77EDF4621DB840119CD31EFBE62C62DD}Frequently asked questions to help you transition from Target Classic to Target Standard/Premium. 
<draft-comment otherprops="merge">
  ov/c_transition-faq.xml 
</draft-comment>
## What are key dates/milestones of the decommissioning of the Target Classic (Test&Target) user interface that I should be aware of? {#section_C66AAD6CD46749FDA3B49BD6D5095EBB}

We have been reaching out to existing Target Classic customers with plenty of time to transition before any milestones of the Target Classic user interface are reached. We have provided access to the new Adobe Target user interface to all customers contracted on legacy offerings, so that they can begin to adopt the new solution architecture for all of their needs. They can naturally transition their activities into the new UI over time. As stated, the new Adobe Target UI is backward-compatible in terms of implementation and can be accessed on any contracted offering immediately.
Although users will migrate to the new Adobe Target Premium or Adobe Target Standard offerings during the renewal process, below are key milestone dates to keep in mind regarding access to and usage of the Target Classic user interface.
Adobe Target Classic (Test&amp;Target) will be decommissioned in November 2017.

* **September 14, 2017 (Phase 1):**No new campaigns can be created in Target Classic; existing campaigns can still be edited. 

* **October 17, 2017 (Phase 2):**Read/Only status for all users; no new campaigns and no editing of existing campaigns in Target Classic. 
  APIs that are linked to your Target Classic account will be decommissioned. These API calls are based on a username and password-based authentication and use the hostname ` testandtarget.omniture.com`. If your API calls contain a user name and password in the request URL, you must transition to Adobe I/O APIs. 

* **November 14, 2017 (Phase 3):**Decommissioning of Target Classic; no access to UI. 
  The remaining APIs will be decommissioned.


We made the initial announcement to all users of the Target Classic user interface of these plans in September 2016.

## What happens if there is a campaign still running when Target Classic is deprecated? {#section_9C40A72D2BA04277AE5C42BAF1D39C90}

Your campaigns will still deliver as always. You can view them in the new interface and deactivate them after the end-of-life date for Target Classic. We'd recommend that you move them over to Target Standard/Premium beforehand, but nothing will actually stop working if you don't. You won't be able to view the campaign details or modify the campaign though. You'll just be able to change the state and view reports.

## Can I still work with campaigns, audiences, and offers created in Target Classic in the new Target Standard/Premium UI? {#section_807EEABC65774A6E86D87DB8D0D0C86D}


* Campaigns created in Target Classic display in Target Standard/Premium and can be activated, deactivated, and archived with the new UI. You cannot delete Campaigns created in Target Classic using Target Standard/Premium.

* Audiences created in Target Classic display in Target Standard/Premium and can be deleted with the new UI.

* Offers created in Target Classic can be fully edited with the new UI.



## What about if I am a Recommendations Classic customer? Will the current transition effort also apply to this user interface? {#section_8F2E5F8923824CD990D78A4255D61678}

Reach our to your Adobe account team to see our new innovations in Recommendations with Adobe Target Premium. The new Recommendations includes a new visual guided workflow; industry- and page-specific best practices and governance; Adobe Analytics-enhanced segmentation and reporting; and new personalized recommendations algorithms. There are videos and documentation here to get you started: [ Adobe Target Transition Hub ](https://docs.adobe.com/content/AdobeTarget/transition-hub.html). 

## What are the requirements for taking full advantage of the unified Adobe Marketing Cloud profile, Analytics integration, and other core services of Adobe Experience Cloud? {#section_D8A09BF3EAE84FE6AB5738C122BFF3EA}

Visit the [ Adobe Target Transition Hub ](https://docs.adobe.com/content/AdobeTarget/transition-hub.html) for more detailed information on the requirements and steps you should take to enable these services. Two options include: 

* (Recommended) [ at.js ](https://marketing.adobe.com/resources/help/en_US/target/ov2/c_target-atjs-implementation.html#) Version 1.0.0 or later. at.js is the new Target library, designed for greater efficiency and security, and also optimized for single-page applications. 

* [ mbox.js ](https://marketing.adobe.com/resources/help/en_US/target/ov/t_mbox_download.html#) version 53 or later. (Version 58 or later is recommended). 


Your organization also needs to be both an Adobe Analytics Standard or Premium customer, as well as being an existing Adobe Target Standard or Premium customer. The Visitor ID service needs to be implemented on your site, and then a provisioning request needs to be made for the server-to-server integration to be enabled in the back-end. Provisioning, under normal circumstances, takes less than a week.
For more information on implementation, see [ Understanding the Target JavaScript Libraries ](c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB). 

## What happens to existing activities created with the AEM 6.1-6.3 / Target integration after the end-of-life date for the Target Classic user interface? {#section_E064ACAF9D044157B6A4BEC904872E8F}

While the Adobe Experience Manager (AEM) 6.1-6.3 integration with Target does use a Target Classic API user behind the scenes, this is managed separately from the Target UI transition and will not be affected by the end-of-life plans. If you would like to set up an new integration with AEM and Target you will need to send a request to Adobe’s provisioning team, who can set up this integration for you.

## Who should I reach out to for assistance with setting up a transition plan or any technical assistance required? {#section_1C79914C333C482BA041E9B7764C4056}

You can reach out to your Account team, a Customer Success Manager, or your Consultant for any specific or custom questions relative to your account and implementation that you have concerning your transition. ClientCare is also available 24X7 for any immediate technical issues that arise.

## Where do I find more resources on transition and potential next steps and requirements, as well as guidance? {#section_563CB23D8A50407790E16AC7C684C6EC}

Adobe Target Product Marketing, Product Management, Consulting, and Training teams have made major investments in developing resources to assist with your transition plan with more detailed information on any subject related to the transition, as well as knowledge sharing on how to quickly get up to speed and get the most value from the new Adobe Target interface.
These can all be found on the [ Adobe Target Transition Hub ](https://docs.adobe.com/content/AdobeTarget/transition-hub.html). Be sure to check the hub regularly for updates on upcoming webinars/trainings/labs and knowledge-sharing events. We will send reminders on the key milestone dates as they approach, and how you can build momentum on your transition efforts. 
>## Use the New Target Interface FAQs {#concept_E9589B024F1840D6B7B78AB181854409}Frequently asked questions that will help you use the Target Standard/Premium UI as transition from Target Classic to Target. 
<draft-comment otherprops="merge">
  ov/c_use-target-interface-faq.xml 
</draft-comment>
## How do I log in to the new Adobe Target user interface? {#section_60692854D49B40D5BBAF7D4AB46DF8D1}

Nearly all existing Target Classic (Test&amp;Target) customers have been provisioned for the new Adobe Target user interface. Admin user(s) of your existing account should already have credentials and access to invite users into the new user interface. If there is an issue with your access, or your Admin does not have the proper credentials, reach out to your Account team or Customer Success Manager for assistance, or try having the Admin sign up for an Adobe ID with an existing account email address at [ www.marketing.adobe.com ](https://www.marketing.adobe.com) to recover his or her credentials. Next, each individual user who wants to be invited by their Admin into the new user interface will need his or her own Adobe ID. 
If you haven't already signed up for an Adobe ID, you can do so at [ www.marketing.adobe.com ](https://www.marketing.adobe.com). After your Adobe ID is registered, your Admin user can invite you with the appropriate user role/permissions into the new Adobe Target user interface. If you are an Adobe Marketing Cloud administrator, the following links tell you how to add users and assign roles: 

* Target Standard: [ Users ](c_user_management.md#concept_501166A5F8FB4964A3AAA15D6095C6BE)
* Target Premium: [ Properties ](property_channel.md#concept_E396B16FA2024ADBA27BC056138F9838)

For more information on Administrator first steps, and how to invite users and apply their user roles and permissions, visit the article and video within our dedicated Transition Guide section of Adobe Target Help: [ Getting Started ](c_getting_started.md#concept_7F9DBAA507FD4F0C8E3678A7F1EEF9B4). 

## What changes have been made to terminology? {#section_9A2144AB91B54C51B737210132207005}

We have made some changes to the solution terminology to better align with Adobe Experience Cloud and the solutions within it. Below are the most notable changes:
For a list of the notable changes, see [ Terminology Comparison Between Target Classic and Standard ](c_target-transition-classic-to-standard.md#concept_2EAFCB49FAC240F18AF247DC26F0DF3F). 

## Do I need to change my implementation to use the new Adobe Target UI? {#section_38F3F2E9B5DA4A27A91B0EE48DF97C1C}

No, you can begin to use the new UI immediately. The interface is backward-compatible with any existing Target Classic (Test&amp;Target) implementation using the form-based workflow for regional mboxes, or even the [ Visual Experience Composer ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) (VEC) with a legacy global mbox across your site(s). 
However, it will be good to plan an upgrade to an updated global mbox version (and turning off any non-required regional mboxes for a more streamlined implementation). You should also consider using the new [ at.js library ](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17), which works asynchronously and is built for optimal performance with both traditional web and single page application frameworks. the at.js library also provides security improvements. This upgrade will streamline your implementation, while allowing you to take full advantage of all of the rich functionality provided in the VEC. For more information about the advantages of using at.js, see [ at.js Frequently Asked Questions ](c_target-atjs-implementation.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769). 
It may also be a good time to coordinate this upgrade with the implementation of our Visitor ID service, code that will allow you to take advantage of the Profiles &amp; Audience core service and a unified progressive Adobe Experience Cloud profile. The Visitor ID Service provides the foundation for our server-to-server integration (shared audiences &amp; reporting) with Adobe Analytics and other integrations throughout Adobe Experience Cloud.
For more specific technical considerations for upgrading your Adobe Target implementation, see [ Understanding the Target JavaScript Libraries ](c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB). 

## How do I augment my Adobe Target/Adobe Marketing Cloud profile data with additional 1st-party CRM data and other data sources? {#section_12617140D5D548E593FC578F0DCFD21C}

CRM and additional 1st-party data feeds can be regularly scheduled to batch upload in a similar fashion as they were in Target Classic (Test&amp;Target) utilizing our batch profile upload API. However, an easier method is provided by the Adobe Marketing Cloud Profiles &amp; Audiences core service, specifically the Customer Attributes feature. You can access this feature by selecting the "Profiles &amp; Audiences" option listed under the core services list within the top Adobe Marketing Cloud navigation.
You will then be taken to a shared Adobe Marketing Cloud Audience library that lists all of your shared audiences across the cloud. Click the "Customer Attributes" selection in the top navigation; drag and drop a CSV file into the Customer Attributes interface; parse the data and append attributes for ingestion into Adobe Target. If you are already bringing these additional CRM attributes into Adobe Analytics, and have the integration between the two solutions, these attributes will also be available to Adobe Target. Lastly, you can also pass data directly into Adobe Target using the global mbox.
For more information, see [ Customer Attributes ](c_visitor_profile.md#concept_16C5C434D32D4EB1AD44A71821F3DEE8). 

## Where is my activity dashboard and how does it work? {#section_75264867D72741A1B16B2B97CD115CA9}

Your Activity List is the first thing you see when you click into Adobe Target. In fact, it acts as your central dashboard for all Target activities, regardless of their origin.
You'll find a list with many filters that allows you to see all of your existing Adobe Target activities in relative states (active, inactive, ended, etc). You'll also be able to see the source of these activities: if they were built in Adobe Target, in Adobe Experience Manager (leveraging the new native integration), or even in Adobe Target Classic (Test&amp;Target). Target Classic Workflow campaigns can be seen and tracked from the new Activity List; however, when clicked on you will be taken back to that user interface to make any edits or changes to an existing Campaign. Note the ability to edit campaigns will be removed according to the schedule discussed in [ Transition FAQ ](c_target-transition-classic-to-standard.md#concept_77EDF4621DB840119CD31EFBE62C62DD). 
You are able to launch any activity type, including A/B, Auto-Allocate, Auto-Target, Multivariate, Experience (Rules-based) Targeting, Automated Recommendations, and Automated Personalization from the unified drop-down menu connected to the "+Create Activity" blue button in the upper right of the Activity List. All activity types are now standardized on a similar 3-step guided visual workflow.
For more information about managing your Activity List, see [ Activities ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). 

## How do I set up Activities in the new Target UI? {#section_EECD9305F6ED4074BEB377B84A8FA8BC}



<table id="table_3DE8D17B584F4C42B3EBF6E38DED15BE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Activity Type </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>How do I set up an A/B…N test?</p> </td> 
   <td colname="col2"> <p>An A/B…n test is faster and easier to accomplish than it ever has been within the new three-step guided visual workflow, which provides ease of use for a non-technical marketer, while also providing more advanced features for power users of the solution to take advantage of.</p> <p>You begin by selecting "A/B test" in the "+Create Activity" drop-down menu, and then select either the site page or the form-based workflow for activity setup. Then proceed with the following steps:</p> <p> 
     <ol id="ol_5BF4FB1B688D4B148B6DFCF8E1D9AB57"> 
      <li id="li_669A2A4D047B4CAB8A179FE70962B6EE"> <p>Create: Leverage our Visual Experience Composer (VEC) to browse to and select any location on the site and make experience variations through a rich visual editing menu. This is achieved through DOM manipulation, and enabled through our single line of code implementation to the page. You can create single or multiple variations; basic or more complex text, image, or design changes; or even leverage a side-by-side code editor to validate the code changes, directly edit the code, or add custom code. You can also easily extend the test to multiple pages, or a sequence of pages, or validate experience variations with responsive design in mobile viewports.</p> </li> 
      <li id="li_8FA485E76BD64777908EC9115EA14927"> <p>Target: Select the audience to include in the test, and either manual or automated decisioning to use to find the results.</p> </li> 
      <li id="li_DD7AB05242504062AF02B4F586EA6C20"> <p>Goals &amp; Settings: Select the reporting audiences and metrics, or Adobe Analytics as your reporting source, as well as designate activity prioritization and other settings. From your test overview, you can review the test framework, share experience URLs for QA, and even approve and launch your test, if you have the required permissions.</p> </li> 
     </ol> </p> <p>For a more detailed walk-through of the A/B testing workflow, see <a href="../target/t_test_ab.xml#task_68C8079BF9FF4625A3BD6680D554BB72" format="dita" scope="local"> Create an A/B Test </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>What is the new Auto-Allocate (machine-learning algorithm) option in testing?</p> </td> 
   <td colname="col2"> <p>Auto-Allocate is a new selection within the “Target” part of the three-step guided visual workflow for A/B…n testing. It leverages a machine-learning algorithm to redirect traffic to the winning variant within an activity, offering the potential to speed up the time it takes to reach statistical confidence on the winning variant while also improving conversion lift within the activity. It is most valuable when you want statistical confidence on the winning variant faster, and with more success, but you are less concerned with performance of the other variants within an activity.</p> <p>For more information, see <a href="../target/automated_traffic_allocation.xml#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Auto-Allocate </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>What is the new Auto-Target (machine-learning algorithm) option in testing?</p> </td> 
   <td colname="col2"> <p>Auto-Allocate is a new selection within the “Target” part of the three-step guided visual workflow for A/B…n testing. Auto-Target uses advanced machine learning to identify multiple high-performing marketer-defined experiences, and serves the most tailored experience to each visitor based on their individual customer profile and the behavior of previous visitors with similar profiles, in order to personalize content and drive conversions.</p> <p>For more information, see <a href="../target/c_auto-target-to-optimize.xml#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>How do I set up an Automated Personalization (AP) activity?</p> </td> 
   <td colname="col2"> <p>Automated Personalization is an Adobe Target Premium capability that leverages several machine-learning algorithms to help you automatically personalize individual experience variations to each individual visitor based on what is most predictive of conversion in their user profile data.</p> <p>Automated Personalization is very powerful in uncovering what are the most effective profile data attributes and targeting rules for maximizing conversion lift, based on a single conversion or maximizing the value of multiple conversions over time.</p> <p>Automated Personalization also follows the three-step guided visual workflow that any other activity follows. You can even automatically personalize combinations of elements on a page in a similar fashion to a Multivariate Test if multiple variations in multiple locations are selected in the Visual Experience Composer. The algorithms self-learn and self-optimize over time, while providing reports on the algorithm and the individual experience variations’ performance, along with a detailed Insights report that shows the relative predictability of different profile attributes per experience variation.</p> <p>For more information, see <a href="../target/t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>How do I launch an experience (rules-based) targeting activity?</p> </td> 
   <td colname="col2"> <p>Experience Targeting (XT), also referred to as rules-based targeting, follows the same three-step guided visual workflow as setting up an A/B…n test and a Multivariate test. You begin by visually creating or selecting the targeted experience variation, then selecting the audience that will be targeted within this experience and how they will be targeted, and finally the goals and settings that will be tracked in the activity. A callout here is that multiple different audiences can be targeted with a different experience within the same activity for ease in comparing performance of experience targeting different experiences to different audiences.</p> <p> For more information, see <a href="../target/t_experience_target.xml#task_A53DF336CB9F4D7BB87EF2106099EFC4" format="dita" scope="local"> Experience Targeting </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>How do I set up a Multivariate Test (MVT)?</p> </td> 
   <td colname="col2"> <p>Setting up a Multivariate test follows the same three-step guided visual workflow as an A/B…n test, with the exception that multiple elements within the visual experience composer can be selected to make combinations of experience variations to include in the test.</p> <p>These combinations of experience variations can be visually QA-ed, with ease of inclusion/exclusion of particular combinations within our full factorial multivariate test activity type. The second and third steps in the activity workflow (Target and Goals &amp; Settings) follow the same process as an A/B…n test.</p> <p>Adobe Analytics as the reporting source can also be selected, if the Analytics-Target integration is in place. The reporting shows how each combination performed within the activity, with the ability to select top and bottom performing combinations for ease of reporting. There is also a location contribution report that will tell you what experience type is most effective in terms of your success metrics and conversion goal.</p> <p>Note that Multivariate testing in Adobe Target Standard and Adobe Target Premium is rendered as full factorial, unlike fractional factorial in Target Classic (Test&amp;Target) while allowing you the ability to delete unwanted combinations.</p> <p>For more information, see <a href="../mvt/c_multivariate_testing.xml#concept_628695CDC71B449B8DCC2F5654C11499" format="dita" scope="local"> Multivariate Test </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>How do I set up a Recommendations activity?</p> </td> 
   <td colname="col2"> <p>Automated Recommendations is an Adobe Target Premium capability and no longer requires a separate interface; you can launch a recommendations activity from within the new unified UI by selecting the Recommendations option from the “+Create Activity” blue button drop-down menu. You can then choose a URL on your web or mobile site, or select the form-based workflow for any offsite location, including emails, where you want to deliver recommendations.</p> <p>There are many new benefits and innovations to the new Recommendations workflow. It follows the same three-step guided visual workflow as our other activities.</p> <p>There are new segment-based and user-profile based algorithms to choose from, along with category affinity, custom weighting control, and other refinements for improving the accuracy of the suggested product, content, videos, collateral, etc. that you display. Recommendations provides industry- and page-level suggestions on criteria (a.k.a. algorithm) templates that you can customize. Recommendations also lets you customize the criteria along with a pre-built or custom design. You can visually preview the recommendations that will be generated.</p> <p>The new collections library allows the non-technical marketer to make sub-collections of your content/product feed based on any metadata or custom attribute. Criteria (algorithms) can be tested and performance can be validated based on any defined audience or success metric, or you can use Adobe Analytics for even deeper drill down with the Analytics/Target integration.</p> <p>For information, see <a href="../recs/c_recommendations.xml#concept_7556C8A4543942F2A77B13A29339C0C0" format="dita" scope="local"> Recommendations </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## How do I build, edit, and source my audience segments? How does the Audience Library work? {#section_090163B581214514812CA85732CA0BF3}

You can access your central Audience Library in Adobe Target at any time to build, edit, and source audiences for your activities. You can select Audiences from the top navigation throughout the solution. You also have direct access to the Audience Library for selection of an audience to include in any activity at step 2 - "Target" - of any activity setup.
In the Activity Library, out-of-box and previously built audiences are accessible for reuse or further edit. There are also audiences that have been shared from other Adobe Experience Cloud solutions, such as Adobe Analytics and Adobe Audience Manager.
You can select and edit an existing audience with the stylus icon on the audience line; all changes made to an audience definition will automatically update wherever that audience is being used. You can also select "+Create Audience" from the blue button at the top right of the Audience Library to build out your audience utilizing a familiar attribute menu to what you are accustomed to in Target Classic (Test&amp;Target ). Target utilizes AND/OR Boolean logic to allow you to be very specific in terms of what attributes comprise your audience definition. Any custom attribute passed in or defined through profile scripts can also be leveraged for defining audiences. Once complete, your audience is available from the central Audience Library for any current or future activity.
For more detailed information, see [ Select Audience ](t_test_ab.md#concept_A268236C1224451DB7844BF67F41A087) and [ Audiences ](c_target.md#concept_A782F8481A5041EBA75103CB26376522). 

## If I am also an Adobe Analytics customer, how do I leverage all of the benefits of the server-to-server integration between Adobe Analytics & Adobe Target? {#section_6610DE6342AE4C17A7A283A4AA9988D9}

If you are contracted on both Adobe Analytics Standard/Premium and Adobe Target Standard/Premium you are eligible to use the new innovative Adobe Analytics &amp; Adobe Target integration, which provides true data-driven optimization and personalization. After implementation, it requires no further custom development, management, or oversight of existing code. It is a server-side integration on the back-end.
The implementation does require the following to ensure successful data flow between the two solutions:

* Ensure you are on the appropriate H Code or AppMeasurement in your Analytics implementation and a recent version of mbox.js/Target.js/AT.js in your Target implementation.

* You must be provisioned to use the Visitor ID service.


You are then able to utilize Adobe Marketing Cloud shared audiences and take action upon them in Adobe Target. Native Adobe Analytics reporting in Adobe Target is available, as well as the ability to drill down in test reports in either solution with any audience segment or success metric defined and tracked in Analytics.
For more information, see [ Analytics for Target Implementation ](a4t.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A). 

## Can I copy an activity to reuse as a template? {#section_D8C98212A8FB4AFD9EAC1153C7E64C69}

Yes, it's as easy as selecting the copy icon at the activity listing within the central Activity List. This is a good way to speed up activity set-up when you are tracking similar metrics or targeting the same audiences across multiple activities.
Copying an activity is covered within this broader help article on [ Activities ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). 

## How do I set up an offsite activity (for example, in email template or in an Internet-connected device or screen)? {#section_A8D3C587AF374A8B8FD2C9C9EA4D1AD9}

In order to select an off-site location to deliver an activity to, including an email template, partner site, or even a location on an Internet-connected device or screen (such as an ATM), you will want to select the form-based workflow in that first pop-up prior to entering the three-step guided workflow. You can then select the off-site location within the drop-down in the workflow and build out the remainder of the activity in a similar fashion to how you built a campaign in Target Classic (Test&amp;Target).
For more detailed information on the form-based workflow, see [ Experiences ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

## How do I set up activities within my mobile apps? {#section_D76B7DC8CE7E4AAEA29CDEBF3EF70AD6}

Customers who have included mobile app volume in their existing contract can extend their optimization and personalization program into mobile apps. Adobe Target can be enabled for use in mobile apps by either the Adobe Mobile Services SDK or leveraging our APIs.
To launch any of the activity types within a mobile application, select the activity type within the "+Create Activity" drop-down menu in the upper right corner of the activity list, then select the form-based experience composer in the first pop-up prior to entering the three-step guided workflow. You can then select the mobile application location/tag within the drop-down in the workflow and build out the remainder of the activity in a similar fashion to how you built a campaign in Target Classic (Test&amp;Target).
For more detailed information on the form-based workflow, see [ Experiences ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

## How do I create and reuse profile scripts? {#section_1EE4CC788D134E7F923E98CEC7C9294D}

You can use profile scripts to capture visitor attributes across multiple visits. Profile scripts are code snippets defined within Adobe Target using a form of server-side JavaScript. For example, you might use a profile script to capture how frequently a visitor visits your site, and when that user last visited.
Profile Scripts are built in a similar fashion to how you've previously built them in Target Classic (Test&amp;Target ). In fact, profile scripts built in Target Classic (Test&amp;Target) will be available for use within the new user interface. Profile scripts can be found in the Audience List as a selection on the left navigation. You are then placed in a profile script library that allows you to manage your existing profile scripts as well as write the code for new ones.
For more information, see [ Profile Script Attributes ](c_visitor_profile.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2). 

## How do I perform campaign and experience (offer) level targeting? {#section_8FB9AEE838ED460AB14D9D7B141D6F8A}

Campaign and offer-level targeting can still be achieved within the new Adobe Target user interface. For experience-level (offer) targeting, select the Experience Targeting (XT) activity type as described above, which lets you assign each experience to a specific audience. Campaign-level targeting is done on Step 2 of every activity workflow. Select the audience from your Audience Library.
Target Standard/Premium also give you the ability to assign multiple audiences to a specific experience (imagine experience B that has versions in English and Spanish, or a price discount that is presented in both Dollars and Pounds). To assign multiple audiences to a single experience, the gear icon at the top of the visual experience composer while you are in a selected experience variation, then click the Audience option in the menu to select audiences to target the selected variation to within an activity.
For more information, see [ Multiple Experience Versions in an A/B Test ](t_test_ab.md#task_0138112E283A4A5B9F8AB9AAF2FBC2FF). 

## How do I access the code to see the changes I am making or insert custom code? {#section_7B109B34338045A5BBCA75AC0D6BB141}

For those users who still want to access the code for QA (validate code changes being made behind the visual experience composer), to make direct edits to the code, or to insert their own custom code, a side-by-side code editor within the Visual Experience Composer is accessible to view and edit code alongside the visual edits being made. Custom code can be inserted easily as well .
For more information, see [ Code Editor ](c_vec_code_editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5). 

## How do I perform a URL redirect? {#section_3022755764C34EB6B7F6CEF7B0955F57}

Redirecting an experience variation to a completely different URL is easily selected within the Visual Experience Composer. Click the selected experience variation’s tab in the left navigation as you are adding experiences, then select the hyperlink icon that lets you put in the URL for redirect.
For more information, see [ Redirect to a URL ](t_redirect_offer.md#task_9578678D42784F5EB9638F8AC8C911FA). 

## How do I extend my activity to a multi-page/funnel test or targeted activity? {#section_8CCB168459A24ED4849CE08F5D681049}

There is a very elegant and streamlined approach for adding additional pages into a test or targeted activity from within the Visual Experience Composer. From a specific experience or page, you can select to “add additional pages” from the drop-down menu connected to the gear icon in the upper navigation. It then allows you to designate the URL for the next page in the sequence and to make additional edits or create experience variations to this next page in the sequence. The sequence can be clicked through, modified, and QAed in this tabbed framework easily.
For more information, see [ Multipage Activity ](c_experiences.md#concept_277E096063E14813AC5D8EDFA1D2ED48). 

## How do I apply my experience variations to a group of pages (template testing)? {#section_89C9BFE2FC0242A49EF0885B70BFC5C8}

You can easily apply an experience variation to a group or category of pages, what we call “template testing,” by selecting the URL option in the drop-down menu connected to the gear icon in the top navigation of the Visual Experience Composer while in a selected experience variation. Then, select the template rules for applying the experience variation to groups of pages relative to URL, Domain, Hash (#) fragment, Query, or mbox parameter.
For more information, see [ Include the Same Experience on Similar Pages ](c_experiences.md#task_2539D51A18044F82B0D9895636546781). 

## How do I embrace responsive web design to see and customize my experience variations for different devices? {#section_50A57F38FF174629A35525D1C9DB6AC2}

You can view and make specific modifications to a responsive design site based on any screen size you designate or any custom mobile viewport you wish to customize. You can see this by selecting the Mobile Viewport menu option in the drop-down connected to the gear icon in the top navigation, then setting any mobile viewport you wish to see and reuse for modifying the experience per device or screen.

## How do I get my product/content feed into Adobe Target and where can I manage the metadata (where are my collections managed)? {#section_A276A7770E7049049D0E99449D59CD92}

Product feeds (products, videos, articles, etc.) can be regularly scheduled to feed into Adobe Target via Adobe Analytics, Google Product Feed, or FTP Upload. The Catalog and Collections can then be managed by clicking on the Recommendations option in the top navigation of the solution. Collections can be built based on any available combination of metadata attributes. Collections can be selected from within a Recommendations activity set up by clicking on the Recommendations experience variation as you are reviewing it in the Visual Experience Composer and then selecting the collection you want to apply to the results set.
For more information, see [ Products ](c_products.md#concept_FD935A24D98745FFB2447933FCEB8062). 
>## Terminology Comparison Between Target Classic and Standard {#concept_2EAFCB49FAC240F18AF247DC26F0DF3F}Target Standard introduces several terms and concepts that are different than those used in Target Classic. These terms are shared across the Adobe Marketing Cloud, so your marketing teams can easily work together. 
<draft-comment otherprops="merge">
  ov/c_target-terminology-compare.xml 
</draft-comment>This video explains the terminology changes between Target Classic and Target Standard/Premium.


<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Adobe Target Terminology Changes </th> 
   <th colname="col3" class="entry"> 3:32 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/JjilhQxLgOA/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/JjilhQxLgOA/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_4578966D6A6F444FAE10252554142D79">Understand terminology differences between Target Classic and Target Standard/Premium</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Key terms from Target Classic (formerly Test&amp;Target) have changed in Target Standard:


<table id="table_52D42488D90A45E0827D40C4AA53CEB4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Target Classic Terms and Concepts </th> 
   <th colname="col2" class="entry"> Target Standard Terms and Concepts </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 1:1 </td> 
   <td colname="col2"> <p> <a href="../target/t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a> </p> <p>Automated Personalization is available as part of the Target Premium solution. It is not included with Target Standard without a Target Premium license. If you have a Target Premium license, the Target Premium card replaces the Target Standard card in the Adobe Marketing Cloud.</p> <p>Major differences between 1:1 and Automated Personalization include:</p> 
    <ul id="ul_65DD19A8E21F4E2B82D20D7EB639C353"> 
     <li id="li_2AAD68D77901410CB05E178450329077">Modeling groups have been replaced by reporting groups</li> 
     <li id="li_A01666CAE91749C288EED7081EF2AC79">The new Random Forest algorithm creates individual decision trees for each model offer. <p>This algorithm creates more efficient models by retaining the information that the Residual Variance Model algorithm discards after a decision is made that does not use that data. The Decision Tree Ensemble algorithm uses this data to learn faster, providing faster results.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Campaign </td> 
   <td colname="col2"> <p> <a href="../target/c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activity </a> </p> <p>Formerly called "campaigns", activities are managed in the centralized Activity List, which you reach as soon as you click into the Adobe Target user interface.</p> <p>Activities have a broader definition than only a campaign. They include tests and content targeted to a specific audience. Every activity has an objective and a goal. The objective is a high-level description of what you hope to achieve with the activity. The goal clearly specifies what action a visitor performs to count as a success. For example, you might want to increase revenue (objective), measured by the number of page views of your Checkout Confirmation page (goal).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Campaign Summary </td> 
   <td colname="col2"> <p>Activity diagram</p> <p>The Activity diagram shows the audience, experiences, and other information for an activity. The diagram leads you through the creation and editing of an activity.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Campaign Targeting </td> 
   <td colname="col2"> <p> <a href="../target/c_target.xml#concept_A782F8481A5041EBA75103CB26376522" format="dita" scope="local"> Activity Targeting </a> </p> <p>Activities are targeted to a specific audience. Visitors are evaluated during each page load to determine whether they still meet the audience criteria. In Target Classic, activity entrants are evaluated one time for campaign entry and continue to see content until they convert, even if their segment membership changes.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Click from Display Mboxes </td> 
   <td colname="col2"> <p> <a href="../target/r_success_metrics.xml#concept_BC6753401F4048A980439C6AEAA907CC" format="dita" scope="local"> "Clicked a Link" </a> </p> <p>Target Classic only tracks clicks inside mboxes used in the campaign, and the user must land on a page with the <span class="filepath"> mbox.js </span> file. Standard tracks clicks on any element on the page, with no code required other than the single <span class="filepath"> mbox.js </span> reference, and no page destination limitations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Conversion </td> 
   <td colname="col2"> <p>Conversion</p> <p>The conversion event is set to "always convert" in Target Standard. The visitor always sees the test content.</p> <p>In Target Classic, a visitor who converts and then reenters the campaign is counted as a new user.</p> <p>In Target Standard, a visitor who converts and then renters the campaign is not counted as a new user. However, each time that visitor converts, the conversion is counted.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mboxes Around Content Areas </td> 
   <td colname="col2"> <p> <a href="../ov2/c_target-implement.xml#concept_60B748DE4293488F917E8F1FA4C7E9EB" format="dita" scope="local"> A single line of code is referenced once per page </a>. This JavaScript library manages all communication required between your site and Adobe Target. You can also continue to use mboxes already on your site for displaying content and tracking user behavior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Offers </td> 
   <td colname="col2"> <p> <a href="../target/c_manage_content.xml#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Content </a> </p> <p>Content refers to both HTML offers and image "assets." The Content Library in Standard stores images and HTML offers. Images can be delivered directly to your site if you are an Adobe Scene7 customer. If you do not use Scene7, you can reference images hosted on your own server or content delivery network (CDN).</p> <p>Although you can create HTML offers separately from the activity, they are typically set up using the Visual Experience Composer during activity creation. If you use the Visual Experience Composer to change content on your site, those changes are specific to that experience and do not get saved to the Content Library for reuse.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Segments </td> 
   <td colname="col2"> <p> <a href="../target/c_target.xml#concept_A782F8481A5041EBA75103CB26376522" format="dita" scope="local"> Audiences </a> </p> <p>Formerly called "segments" or "audience segments," audiences are managed from the central Audience Library, which includes out-of-the-box and custom created audiences within Adobe Target, as well as audiences sourced from other Adobe Experience Cloud solutions (leveraging our People core service in Adobe Experience Cloud).</p> <p>An audience, like a Target Classic segment, is a set of site visitors who meet specific criteria. Activities are often targeted at a specific audience. An audience might be visitors who use a particular browser, operating system, search engine, or any of several other criteria. Multiple criteria can be combined to define an audience.</p> <p>Separate audiences can be created for content delivery or reporting. Reusable segments in Target Classic are synced with Target Standard for use in Activities.</p> <p>Audiences are created globally. In other words, any audience you create is available in the Audiences list for reuse in other activities.</p> </td> 
  </tr> 
 </tbody> 
</table>

>## Technical Implementation {#concept_0505A57DBDD04AA48BC988553E049239}How you implement Target depends on whether you use mbox.js or at.js, and whether you use Adobe DTM. 
<draft-comment otherprops="merge">
  ov/c_trans-technical-implementation.xml 
</draft-comment>The technical implementation phase is complete when you have completed the following steps:


<table id="table_85803800F7E443F8A2FDAC8267B364BD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Step </th> 
   <th colname="col2" class="entry"> Task </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step1_icon.png" id="image_F0F2AF68C34544D3856622AE07408FEA" /> </td> 
   <td colname="col2"> Implement mbox.js or at.js, with no incompatible plugins. <p> <p type="important">Note:  If you are moving from <span class="keyword"> Target Classic </span> to <span class="keyword"> Target Standard/Premium </span> and want to continue using <span class="filepath"> mbox.js </span>, you must download a new <span class="filepath"> mbox.js </span> file from the <span class="keyword"> Target Standard/Premium </span> UI and update your web pages accordingly, even if you already have <span class="filepath"> mbox.js </span> deployed. This is especially important if you are planning to edit page content in the <span class="wintitle"> Visual Experience Composer </span> (VEC) in <span class="keyword"> Target Standard/Premium </span> (see <a href="../target/vec-best-pracitces-and-troubleshooting.xml#concept_E284B3F704C04406B174D9050A2528A6" format="dita" scope="local"> Visual Experience Composer Best Practices and Limitations </a>). However, there are advantages when using the newer <span class="keyword"> Target </span> JavaScript <span class="codeph"> at.js </span> library that you should consider during the transition. For more information, see <a href="../ov2/c_target-implement.xml#concept_60B748DE4293488F917E8F1FA4C7E9EB" format="dita" scope="local"> Understanding the Target JavaScript Libraries </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step2_icon.png" id="image_B2F94231CCDC407BB07F98E1237ADEFB" /> </td> 
   <td colname="col2"> A global mbox firing successfully either across your site globally or on pages where testing or tracking will occur. </td> 
  </tr> 
 </tbody> 
</table>

***Optional: My organization uses Adobe DTM to deploy the Marketing Cloud*** 
Follow the [ deployment steps for DTM ](https://marketing.adobe.com/resources/help/en_US/dtm/target/). 
***My digital properties are deployed on the latest library files for Target, either at.js or mbox.js V53+*** 
Either update your [ mbox.js ](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420) file or update to [ at.js ](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17). 

>[!NOTE]
>
>mbox.js V58 is the minimum version if using Marketing Cloud Core Services.



## mbox.js {#section_22295EBBD27445C3B9AC12DF24B90141}

Choose the option below that applies to you:

* ***I want to use my JavaScript library to auto-deploy my target-global-mbox for a Single Line of Code implementation*** Make sure the Auto Create option in the mbox.js download settings is enabled. To set the Auto Create option, click ** ` Setup` ** > ** ` Implementation` ** > ** ` Edit mbox.js Settings` **, then enable ** ` Auto create global mbox` **. 

  >[!NOTE]
  >
  >If you are on a Target Classic SKU, you might exceed your allotted number of server calls.


* ***I already have a global mbox deployed (hard coded) and want to keep it*** Ensure that the Auto Create option in the mbox.js download settings is enabled. To set the Auto Create option, click ** ` Setup` ** > ** ` Implementation` ** > ** ` Edit mbox.js Settings` **, then enable ** ` Auto create global mbox` **. 

* ***I have already deployed (hard coded) a global mbox, but I want to get rid of it in favor of auto deployment*** 
    1. Make sure the Auto Create option in the mbox.js download settings is enabled. To set the Auto Create option, click ** ` Setup` ** > ** ` Implementation` ** > ** ` Edit mbox.js Settings` **, then enable ** ` Auto create global mbox` **. 

    1. Remove your hard coded global mbox from your site code.
    1. Deploy the mbox.js file with these settings enabled.


  >[!NOTE]
  >
  >If you are on a Target Classic SKU, you might exceed your allotted number of server calls.


* ***I want to migrate to only a global mbox to reduce server calls*** 
    1. Make sure no Target Classic campaigns are running against your classic regional [ mboxes ](c_getting_started.md#concept_85E01D9DD0B64BD3A138C2D3DB83BD57).
    1. [ Deactivate ](c_activities.md#table_B68BB1AD61394C749822FF4938E404E7) other mboxes in the Target UI first to verify site experience.
    1. Remove Target Classic regional mboxes from your site code.

  For information about implementing mbox.js, see [ Mbox.js Implementation ](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420). 



## at.js {#section_1A3EA327724846E2B8DD49D82CBA5817}

***My digital property uses a Single Page Application Design and I want to use at.js instead of mbox.js*** 
Review the [ at.js documentation ](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) to make sure your Target implementation is compatible with the at.js library file. 
***Our deployment of Target uses Response Plugins*** 
Audit Response Plugins for illegal methods deprecated in the file. See [ at.js Plugins ](c_target-atjs-implementation.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF). 
***Our mbox.js features custom code modifications or other edits*** 
Audit Custom Code for illegal methods deprecated in the file, for example AAM&gt;Target. See [ at.js Limitations ](c_target-atjs-implementation.md#concept_FA99E4D6EC274552BF45E01AFB76CCAE). 
***We make sure of custom site code using documented mbox.js methods*** 
Audit site code for illegal methods deprecated in the file, such as mboxFactory. See [ at.js Limitations ](c_target-atjs-implementation.md#concept_FA99E4D6EC274552BF45E01AFB76CCAE). 
***We fire a global mbox on a hash change, route change, or state change*** 
Work with Adobe Target Consulting to build an SPA Framework Plan for implementation.

## Next Step {#section_9DAF58FBB4D8458784A93692C46E0514}

[ Advanced Feature Considerations ](c_target-transition-classic-to-standard.md#concept_D8DB7801889A464D9197A739F7B185A7) 
>## Advanced Feature Considerations {#concept_D8DB7801889A464D9197A739F7B185A7}If you use certain Target Classic advanced features, be aware of the considerations in this topic when transitioning to Target Standard/Premium. 
<draft-comment otherprops="merge">
  ov/c_trans-advanced-feature-considerations.xml 
</draft-comment>The advanced feature considerations phase is complete when you have either:


|  Step  | Task  |
|---|---|
|   ![](../a4t/graphics/step1_icon.png)  | Migrated the advanced features you use.  |
|   ![](../a4t/graphics/step2_icon.png)  | Deemed the advanced features unnecessary for migration.  |


## Target Classic Advanced Feature Considerations {#section_4FD5C0D0E39F42B884C27B5FB1445A29}

***I use Expression Targets*** 
Consider any of the following alternatives:

* Migrate your Expression Targets to [ Profile Scripts ](c_visitor_profile.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)
* Use the [ customized audiences capabilities ](c_audiences.md#concept_65BE870D290E412D8BBF557EEA67C271) in Target Standard/Premium to re-create your audiences
* Use [ Analytics ](https://marketing.adobe.com/resources/help/en_US/reference/) or [ Audience Manager ](https://marketing.adobe.com/resources/help/en_US/aam/c_aam_home.html)

***I use Monitoring Campaigns*** 
Similar to plugins, in Target Standard/Premium, content from multiple activities can be returned to a single mbox call. In Target Standard/Premium, the ` Monitoring Campaign` you would have set up in Target Classic can be set up as an A/B or Experience Targeting activity with a low activity priority to ensure that content from other activities is seen by visitors. Visitors will still be incremented appropriately in the low-priority activities' reports. For more information, see [ Priority ](c_activities.md#concept_1780C11FEA57440499F0047DD6900E0F). 

## Recently Added Features {#section_62F97EE4775C45ED8719E6D227361982}

The following features have been recently added to Target Standard/Premium:

* [ Target by Latitude and Longitude ](c_target_rules.md#concept_5B4D99DE685348FB877929EE0F942670) 

* [ Response Tokens ](c_response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4) (Plug-ins in Target Classic) 

* [ Remote Offers ](c_manage_content.md#concept_657016A0E6174C22B89036E9C8A0170F) 

* [ Host group management ](c_hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E) 


>## Managing the Transition {#concept_E0415E44D209458DA30D8A207D08048E}Operational milestones help you determine whether your migration is complete. 
<draft-comment otherprops="merge">
  ov/c_trans-operational-milestones.xml 
</draft-comment>Check the following operational milestones:


<table id="table_C6EF0E7850B94C0BA2713F081EA6937C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Step </th> 
   <th colname="col2" class="entry"> Milestone </th> 
   <th colname="col3" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step1_icon.png" id="image_8EDE37E33BAC44F4A98DF71698FF58B7" /> </td> 
   <td colname="col2"> <a href="../ov2/c_target-implement.xml#concept_60B748DE4293488F917E8F1FA4C7E9EB" format="dita" scope="local"> Deploy either mbox.js or at.js </a> on your site </td> 
   <td colname="col3"> <p>Deploy one of the following:</p> 
    <ul id="ul_46B825DED1234424A2E57A02E10A60DA"> 
     <li id="li_2FDCAB8D9E944606B3EFEDDF874E0CF1"> <a href="../ov2/c_target-atjs-implementation.xml#concept_8AC8D169E02944B1A547A0CAD97EAC17" format="dita" scope="local"> at.js </a> </li> 
     <li id="li_B6A321C4A3BE492BA39B075ECA362D0D"> <a href="t_mbox_download.xml#task_4EAE26BB84FD4E1D858F411AEDF4B420" format="dita" scope="local"> mbox.js </a> version 53 or later (if not using Marketing Cloud <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/core-services-overview.html" format="https" scope="external"> Core Services </a>) </li> 
     <li id="li_6302DF7D889440B5A269D6D421024AA6">mbox.js version 58 or later (if using Marketing Cloud Core Services)</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step2_icon.png" id="image_3A43329215D34B569536B706E625DBA3" /> </td> 
   <td colname="col2"> Deactivate and archive or delete Target Classic activities when they end </td> 
   <td colname="col3"> Build a deactivation schedule for any remaining Target Classic activities. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step3_icon.png" id="image_392B266D65A3455FBC936B5F892B3883" /> </td> 
   <td colname="col2"> Move evergreen activities to Target Standard/Premium </td> 
   <td colname="col3"> Re-create your evergreen campaigns in Target Standard (or hard code if available) and close the Target Classic campaigns. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step4_icon.png" id="image_CF7C2F5F3955448FBC8B2BD53D91AD41" /> </td> 
   <td colname="col2"> Rebuild your <a href="../target/c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> audiences </a> in Target Standard/Premium (Audiences + Expression Targets) </td> 
   <td colname="col3"> Use the <a href="../target/c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> customized audiences capabilities </a> in Target Standard/Premium to re-create your audiences. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step5_icon.png" id="image_8BD96B901C2E4AB2A8748176D101F102" /> </td> 
   <td colname="col2"> Create all of your new <a href="../target/c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> activities </a> in Target Standard/Premium </td> 
   <td colname="col3"> Set all Target Classic users to Read Only or Editor to prevent new activities from being published from Target Classic. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../a4t/graphics/step6_icon.png" id="image_49449656FE924B02B1B63A350CE6EF4A" /> </td> 
   <td colname="col2"> Run a test using the <a href="../target/c_experiences.xml#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Visual Experience Composer </a> </td> 
   <td colname="col3"> Verify successful delivery and reporting. </td> 
  </tr> 
 </tbody> 
</table>

