---
description: Frequently asked questions that will help you use the Target Standard/Premium UI as transition from Target Classic to Target.
keywords: transition;migration;migrate from target classic to target standard
seo-description: Frequently asked questions that will help you use the Target Standard/Premium UI as transition from Target Classic to Target.
seo-title: Use the New Target Interface FAQs
solution: Target
title: Use the New Target Interface FAQs
uuid: 0f944b80-87b8-4ced-9ceb-48d6477d7b1e
index: y
internal: n
snippet: y
translate: y
---

# Use the New Target Interface FAQs

This section contains the following information:

* [ How do I log in to the new Adobe Target... ](c_use-target-interface-faq.md#section_60692854D49B40D5BBAF7D4AB46DF8D1) 

* [ What changes have been made to terminology? ](c_use-target-interface-faq.md#section_9A2144AB91B54C51B737210132207005) 

* [ Do I need to change my implementation to use the... ](c_use-target-interface-faq.md#section_38F3F2E9B5DA4A27A91B0EE48DF97C1C) 

* [ How do I augment my Adobe Target/Adobe Marketing Cloud profile data with additional 1st-party CRM data and other data sources? ](c_use-target-interface-faq.md#section_12617140D5D548E593FC578F0DCFD21C) 

* [ Where is my activity dashboard and how does it work... ](c_use-target-interface-faq.md#section_75264867D72741A1B16B2B97CD115CA9) 

* [ How do I set up Activities in the new Target... ](c_use-target-interface-faq.md#section_EECD9305F6ED4074BEB377B84A8FA8BC) 

* [ How do I build, edit, and source my audience segments? How does the Audience Library work? ](c_use-target-interface-faq.md#section_090163B581214514812CA85732CA0BF3) 

* [ If I am also an Adobe Analytics customer, how do I leverage all of the benefits of the server-to-server integration between Adobe Analytics &amp; Adobe Target? ](c_use-target-interface-faq.md#section_6610DE6342AE4C17A7A283A4AA9988D9) 

* [ Can I copy an activity to reuse as a template... ](c_use-target-interface-faq.md#section_D8C98212A8FB4AFD9EAC1153C7E64C69) 

* [ How do I set up an offsite activity (for example, in email template or in an Internet-connected device or screen)? ](c_use-target-interface-faq.md#section_A8D3C587AF374A8B8FD2C9C9EA4D1AD9) 

* [ How do I set up activities within my mobile apps... ](c_use-target-interface-faq.md#section_D76B7DC8CE7E4AAEA29CDEBF3EF70AD6) 

* [ How do I create and reuse profile scripts? ](c_use-target-interface-faq.md#section_1EE4CC788D134E7F923E98CEC7C9294D) 

* [ How do I perform campaign and experience (offer) level targeting? ](c_use-target-interface-faq.md#section_8FB9AEE838ED460AB14D9D7B141D6F8A) 

* [ How do I perform a URL redirect? ](c_use-target-interface-faq.md#section_3022755764C34EB6B7F6CEF7B0955F57) 

* [ How do I extend my activity to a multi-page/funnel test or targeted activity? ](c_use-target-interface-faq.md#section_8CCB168459A24ED4849CE08F5D681049) 

* [ How do I apply my experience variations to a group... ](c_use-target-interface-faq.md#section_89C9BFE2FC0242A49EF0885B70BFC5C8) 

* [ How do I embrace responsive web design to see and... ](c_use-target-interface-faq.md#section_50A57F38FF174629A35525D1C9DB6AC2) 

* [ How do I get my product/content feed into Adobe Target and where can I manage the metadata (where are my collections managed)? ](c_use-target-interface-faq.md#section_A276A7770E7049049D0E99449D59CD92) 



## How do I log in to the new Adobe Target user interface? {#section_60692854D49B40D5BBAF7D4AB46DF8D1}

Nearly all existing Target Classic (Test&amp;Target) customers have been provisioned for the new Adobe Target user interface. Admin user(s) of your existing account should already have credentials and access to invite users into the new user interface. If there is an issue with your access, or your Admin does not have the proper credentials, reach out to your Account team or Customer Success Manager for assistance, or try having the Admin sign up for an Adobe ID with an existing account email address at [ www.marketing.adobe.com ](https://www.marketing.adobe.com) to recover his or her credentials. Next, each individual user who wants to be invited by their Admin into the new user interface will need his or her own Adobe ID. 
If you haven't already signed up for an Adobe ID, you can do so at [ www.marketing.adobe.com ](https://www.marketing.adobe.com). After your Adobe ID is registered, your Admin user can invite you with the appropriate user role/permissions into the new Adobe Target user interface. If you are an Adobe Marketing Cloud administrator, the following links tell you how to add users and assign roles: 

* Target Standard: [ Users ](c_user_management.md#concept_501166A5F8FB4964A3AAA15D6095C6BE)
* Target Premium: [ Properties ](property_channel.md#concept_E396B16FA2024ADBA27BC056138F9838)

For more information on Administrator first steps, and how to invite users and apply their user roles and permissions, visit the article and video within our dedicated Transition Guide section of Adobe Target Help: [ Administrator First Steps ](start_target.md#task_9F178DC9A2244357896DE50B43C844D8). 

## What changes have been made to terminology? {#section_9A2144AB91B54C51B737210132207005}

We have made some changes to the solution terminology to better align with Adobe Experience Cloud and the solutions within it. Below are the most notable changes:
For a list of the notable changes, see [ Terminology Comparison Between Target Classic and Standard ](c_target-terminology-compare.md#concept_2EAFCB49FAC240F18AF247DC26F0DF3F). 

## Do I need to change my implementation to use the new Adobe Target UI? {#section_38F3F2E9B5DA4A27A91B0EE48DF97C1C}

No, you can begin to use the new UI immediately. The interface is backward-compatible with any existing Target Classic (Test&amp;Target) implementation using the form-based workflow for regional mboxes, or even the [ Visual Experience Composer ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) (VEC) with a legacy global mbox across your site(s). 
However, it will be good to plan an upgrade to an updated global mbox version (and turning off any non-required regional mboxes for a more streamlined implementation). You should also consider using the new [ at.js library ](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17), which works asynchronously and is built for optimal performance with both traditional web and single page application frameworks. the at.js library also provides security improvements. This upgrade will streamline your implementation, while allowing you to take full advantage of all of the rich functionality provided in the VEC. For more information about the advantages of using at.js, see [ at.js Frequently Asked Questions ](c_target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769). 
It may also be a good time to coordinate this upgrade with the implementation of our Visitor ID service, code that will allow you to take advantage of the Profiles &amp; Audience core service and a unified progressive Adobe Experience Cloud profile. The Visitor ID Service provides the foundation for our server-to-server integration (shared audiences &amp; reporting) with Adobe Analytics and other integrations throughout Adobe Experience Cloud.
For more specific technical considerations for upgrading your Adobe Target implementation, see [ Understanding the Target JavaScript Libraries ](c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB). 

## How do I augment my Adobe Target/Adobe Marketing Cloud profile data with additional 1st-party CRM data and other data sources? {#section_12617140D5D548E593FC578F0DCFD21C}

CRM and additional 1st-party data feeds can be regularly scheduled to batch upload in a similar fashion as they were in Target Classic (Test&amp;Target) utilizing our batch profile upload API. However, an easier method is provided by the Adobe Marketing Cloud Profiles &amp; Audiences core service, specifically the Customer Attributes feature. You can access this feature by selecting the "Profiles &amp; Audiences" option listed under the core services list within the top Adobe Marketing Cloud navigation.
You will then be taken to a shared Adobe Marketing Cloud Audience library that lists all of your shared audiences across the cloud. Click the "Customer Attributes" selection in the top navigation; drag and drop a CSV file into the Customer Attributes interface; parse the data and append attributes for ingestion into Adobe Target. If you are already bringing these additional CRM attributes into Adobe Analytics, and have the integration between the two solutions, these attributes will also be available to Adobe Target. Lastly, you can also pass data directly into Adobe Target using the global mbox.
For more information, see [ Customer Attributes ](c_working-with-customer-attributes.md#concept_16C5C434D32D4EB1AD44A71821F3DEE8). 

## Where is my activity dashboard and how does it work? {#section_75264867D72741A1B16B2B97CD115CA9}

Your Activity List is the first thing you see when you click into Adobe Target. In fact, it acts as your central dashboard for all Target activities, regardless of their origin.
You'll find a list with many filters that allows you to see all of your existing Adobe Target activities in relative states (active, inactive, ended, etc). You'll also be able to see the source of these activities: if they were built in Adobe Target, in Adobe Experience Manager (leveraging the new native integration), or even in Adobe Target Classic (Test&amp;Target). Target Classic Workflow campaigns can be seen and tracked from the new Activity List; however, when clicked on you will be taken back to that user interface to make any edits or changes to an existing Campaign. Note the ability to edit campaigns will be removed according to the schedule discussed in [ Transition FAQ ](c_transition-faq.md#concept_77EDF4621DB840119CD31EFBE62C62DD). 
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
     </ol> </p> <p>For a more detailed walk-through of the A/B testing workflow, see <a href="../target/t_test_create_ab.xml#task_68C8079BF9FF4625A3BD6680D554BB72" format="dita" scope="local"> Create an A/B Test </a>. </p> </td> 
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
For more detailed information, see [ Select Audience ](c_ab_audience.md#concept_A268236C1224451DB7844BF67F41A087) and [ Audiences ](c_target.md#concept_A782F8481A5041EBA75103CB26376522). 

## If I am also an Adobe Analytics customer, how do I leverage all of the benefits of the server-to-server integration between Adobe Analytics & Adobe Target? {#section_6610DE6342AE4C17A7A283A4AA9988D9}

If you are contracted on both Adobe Analytics Standard/Premium and Adobe Target Standard/Premium you are eligible to use the new innovative Adobe Analytics &amp; Adobe Target integration, which provides true data-driven optimization and personalization. After implementation, it requires no further custom development, management, or oversight of existing code. It is a server-side integration on the back-end.
The implementation does require the following to ensure successful data flow between the two solutions:

* Ensure you are on the appropriate H Code or AppMeasurement in your Analytics implementation and a recent version of mbox.js/Target.js/AT.js in your Target implementation.

* You must be provisioned to use the Visitor ID service.


You are then able to utilize Adobe Marketing Cloud shared audiences and take action upon them in Adobe Target. Native Adobe Analytics reporting in Adobe Target is available, as well as the ability to drill down in test reports in either solution with any audience segment or success metric defined and tracked in Analytics.
For more information, see [ Analytics for Target Implementation ](c_a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A). 

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
For more information, see [ Profile Script Attributes ](c_script_profile_attributes.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2). 

## How do I perform campaign and experience (offer) level targeting? {#section_8FB9AEE838ED460AB14D9D7B141D6F8A}

Campaign and offer-level targeting can still be achieved within the new Adobe Target user interface. For experience-level (offer) targeting, select the Experience Targeting (XT) activity type as described above, which lets you assign each experience to a specific audience. Campaign-level targeting is done on Step 2 of every activity workflow. Select the audience from your Audience Library.
Target Standard/Premium also give you the ability to assign multiple audiences to a specific experience (imagine experience B that has versions in English and Spanish, or a price discount that is presented in both Dollars and Pounds). To assign multiple audiences to a single experience, the gear icon at the top of the visual experience composer while you are in a selected experience variation, then click the Audience option in the menu to select audiences to target the selected variation to within an activity.
For more information, see [ Multiple Experience Versions in an A/B Test ](t_target-experience-to-multiple-audiences.md#task_0138112E283A4A5B9F8AB9AAF2FBC2FF). 

## How do I access the code to see the changes I am making or insert custom code? {#section_7B109B34338045A5BBCA75AC0D6BB141}

For those users who still want to access the code for QA (validate code changes being made behind the visual experience composer), to make direct edits to the code, or to insert their own custom code, a side-by-side code editor within the Visual Experience Composer is accessible to view and edit code alongside the visual edits being made. Custom code can be inserted easily as well .
For more information, see [ Code Editor ](c_vec_code_editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5). 

## How do I perform a URL redirect? {#section_3022755764C34EB6B7F6CEF7B0955F57}

Redirecting an experience variation to a completely different URL is easily selected within the Visual Experience Composer. Click the selected experience variation’s tab in the left navigation as you are adding experiences, then select the hyperlink icon that lets you put in the URL for redirect.
For more information, see [ Redirect to a URL ](t_redirect_offer.md#task_9578678D42784F5EB9638F8AC8C911FA). 

## How do I extend my activity to a multi-page/funnel test or targeted activity? {#section_8CCB168459A24ED4849CE08F5D681049}

There is a very elegant and streamlined approach for adding additional pages into a test or targeted activity from within the Visual Experience Composer. From a specific experience or page, you can select to “add additional pages” from the drop-down menu connected to the gear icon in the upper navigation. It then allows you to designate the URL for the next page in the sequence and to make additional edits or create experience variations to this next page in the sequence. The sequence can be clicked through, modified, and QAed in this tabbed framework easily.
For more information, see [ Multipage Activity ](c_multipage_activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48). 

## How do I apply my experience variations to a group of pages (template testing)? {#section_89C9BFE2FC0242A49EF0885B70BFC5C8}

You can easily apply an experience variation to a group or category of pages, what we call “template testing,” by selecting the URL option in the drop-down menu connected to the gear icon in the top navigation of the Visual Experience Composer while in a selected experience variation. Then, select the template rules for applying the experience variation to groups of pages relative to URL, Domain, Hash (#) fragment, Query, or mbox parameter.
For more information, see [ Include the Same Experience on Similar Pages ](t_temtest.md#task_2539D51A18044F82B0D9895636546781). 

## How do I embrace responsive web design to see and customize my experience variations for different devices? {#section_50A57F38FF174629A35525D1C9DB6AC2}

You can view and make specific modifications to a responsive design site based on any screen size you designate or any custom mobile viewport you wish to customize. You can see this by selecting the Mobile Viewport menu option in the drop-down connected to the gear icon in the top navigation, then setting any mobile viewport you wish to see and reuse for modifying the experience per device or screen.

## How do I get my product/content feed into Adobe Target and where can I manage the metadata (where are my collections managed)? {#section_A276A7770E7049049D0E99449D59CD92}

Product feeds (products, videos, articles, etc.) can be regularly scheduled to feed into Adobe Target via Adobe Analytics, Google Product Feed, or FTP Upload. The Catalog and Collections can then be managed by clicking on the Recommendations option in the top navigation of the solution. Collections can be built based on any available combination of metadata attributes. Collections can be selected from within a Recommendations activity set up by clicking on the Recommendations experience variation as you are reviewing it in the Visual Experience Composer and then selecting the collection you want to apply to the results set.
For more information, see [ Products ](c_products.md#concept_FD935A24D98745FFB2447933FCEB8062). 
