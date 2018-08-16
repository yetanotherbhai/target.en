---
description: null
seo-description: null
seo-title: 2015 Releases
title: 2015 Releases
uuid: 0f5094da-6f10-4d0b-abe2-e6f5e673d022
index: y
internal: n
snippet: y
translate: y
---

# 2015 Releases


## Adobe Target Standard/Premium 15.10.1 (November 2, 2015) {#section_B5135D75FA0D42A1A3C2711CA3A1B812}

This release includes the following features and enhancements: 



<table id="table_EE13D9B959DA4FB0AD6BC03FBF78AEF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1">Export/Download Summary reports for Automated Personalization and Recommendations Premium </entry> <entry colname="col2"> <p>The ability to download data in a .csv format for quick import into Excel or other data analysis programs has been added to Automated Personalization and Recommendations Premium. </p> <p>This feature was previously only available for A/B, Experience Targeting, and Multivariate activities. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Auto-Allocate in A/B Tests </p> </td> 
   <td colname="col2"> <p> You now have the option to automatically allocate traffic to increase overall campaign lift and discover winning experiences faster. This algorithm increases the overall campaign performance while maintaining the integrity of an A/B test. </p> <p>The algorithm relies on measured performance (e.g. conversion rate) and confidence intervals to produce a traffic distribution that is changed up to twice per hour. </p> <p>Key Benefits </p> <p> 
     <ul id="ul_A41C74C0C7C844F3A923CD6EA5D5D952"> 
      <li id="li_86D3C6A4993F4DC0907BF42986E6CCD1">Preserves the integrity of an A/B test by ensuring that visitors remain in the same experience, like they do in a manual A/B test </li> 
      <li id="li_B849EB2709F84831A1B7A4F312EAFA7E">Finds a statistically significant winner faster than a manual A/B test </li> 
      <li id="li_3F258C6DEB7245E2924115C5628BC3C6">Provides higher average campaign lift than a manual A/B test </li> 
      <li id="li_C9E82388B93E4A298000984B69CBAEDE">Allows you to toggle to a manual test at any time </li> 
     </ul> </p> <p>See <a href="../c_activities/automated_traffic_allocation/automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Customer Attributes </p> </td> 
   <td colname="col2"> <p> Upload 1st party data, called Customer Attributes, using the Experience Cloud core service and choose attributes to share to Target. This functionality launched in March for Analytics and now integrates directly with Target. </p> <p> For example, you might use customer data such as membership status (gold, silver, etc.), purchase history, favorite destination, local store, and so on in your CRM or eCommerce/POS system. Now you can upload that data to Experience Cloud. After the user authenticates on your site, Target can match that data to their web behavior. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/attributes.html" format="https" scope="external"> Customer Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Multiple companies are available when selecting Analytics as the reporting source for Target. </p> </td> 
   <td colname="col2"> <p>When selecting Analytics as the reporting source for Target, you select an Analytics report suite to receive Target activity data. To do this, first choose from any of the Analytics companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to Adobe Target will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the Adobe Experience Cloud to try again. If the report suite is still missing from the list, please contact Customer Care. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/c_integrating_target_with_analytics.html" format="https" scope="external"> Integrating Target with Analytics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New Built-in Options for Audience Creation </p> </td> 
   <td colname="col2"> <p>There are new built-in audience options: </p> <p> 
     <ul id="ul_16E7B53E324B4FB79E1B1E97A1CE65AC"> 
      <li id="li_60B55A81119E48FE83639B9740A2FD21">Target visitors based on which language they use on their browser. This is more accurate than geo-based language targeting. </li> 
      <li id="li_84CAAE7E02CA48FA9C7C00C0415046B6">Target visitors based on browser version, not just which browser is being used. </li> 
      <li id="li_AAF8170CAF4C45BB965D1A9A4E9204D5">You can now Target multiple browsers rather than only one. </li> 
     </ul> </p> <p>See <a href="../c_target/c_audiences/c_target_rules/c_browser.md#concept_221D8EEF53CC45AEACEB17CF336A3658" format="dita" scope="local"> Browser Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p class="Premium">Exclude Past Purchases </p> </td> 
   <td colname="col2"> <p>Target now automatically excludes previously purchased items from a visitor's recommendations. This option can be disabled for any criteria. </p> <p>All out-of-the-box criteria now have this option enabled, including those used in activities that were running prior to this release. If you do not want to exclude past purchases, you should edit those activities. </p> <p>See <a href="../c_recommendations/c_algorithms/t_create_new_algorithm.md#task_28DB20F968B1451481D8E51BAF947079" format="dita" scope="local"> Inclusion Rules </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p> Attribute Weighing </p> </td> 
   <td colname="col2"> <p> Recommendations ranking rules have changed for criteria. This change affects existing Recommendations. </p> <p> Use attribute weighting to "nudge" the algorithm. Marketers can influence the algorithm based on important description or metadata about the content catalog. Apply a higher weighting to these on-sale items so they show more often in the recommendation. Non-sale items are not completely excluded, but they display less often. Multiple weightings can be applied to the same algorithm, and the weightings can be tested on split traffic in the recommendation. </p> <p>These new weights have automatically been applied to all activities. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_attribute_weighting.html" format="https" scope="external"> Attribute Weighting </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Set the Time for Feed Processing </p> </td> 
   <td colname="col2"> <p>Specify the time when you want a feed to update. </p> <p>See <a href="../c_recommendations/c_products/c_feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Create Feed </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Use the Feed List to Set a Feed to Never Run </p> </td> 
   <td colname="col2"> <p>From the feed list, set a feed to never run if you do not want to update that feed. </p> <p>See <a href="../c_recommendations/c_products/c_feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Create Feed </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Set a New Criteria Type Based on Content Similarity </p> </td> 
   <td colname="col2"> <p>An item-based criteria that can be used for the following: </p> <p> 
     <ul id="ul_86BDF2DE0FCE4665A2985D0C56E50A53"> 
      <li id="li_D83669F9019B431891E072C973B317D7">Current items with similar attributes </li> 
      <li id="li_4E45848423F2450999C699C64E0EE9E2">Last purchased item with similar attributes </li> 
      <li id="li_901D4AAF7BE244FCB9277DC7EDD91E32">Custom attributes that match a specified entity.id and use items with similar attributes </li> 
      <li id="li_49D52B0182F346E982C11A0C2DA50B4F">Last viewed item with similar attributes </li> 
      <li id="li_2DBAF32476AC435EB57D08D96CB55683">Most viewed item with similar attributes </li> 
     </ul> </p> <p>See <a href="../c_recommendations/c_algorithms/t_create_new_algorithm.md#task_28DB20F968B1451481D8E51BAF947079" format="dita" scope="local"> Inclusion Rules </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New Activity List Filters </td> 
   <td colname="col2"> <p>Several filters have been added to help you show the activities you are most interested in seeing in the Activities list. </p> <p>See <a href="../c_activities/c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Enhancement: Industry-Relevant Criteria Configuration </p> </td> 
   <td colname="col2"> <p>Irrelevant options during setup have been eliminated. In the past, some setup options for some industry verticals, such as Media, were not always relevant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>New Out-of-the-Box Criteria </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_47E67312A04E414EB797F9AE2A1F7599"> 
      <li id="li_5EDF9006145B4498B2EAD95D642057C5">More Videos Like This </li> 
      <li id="li_6A8DAACE7CD741D0BB766EBCB52BCD88">More Articles Like This </li> 
      <li id="li_1B44AB35B045416B8D8B72C428750822">More Content Like This </li> 
      <li id="li_FEC84CCF3DF3444DAB39F4764DE897B0">More Slideshows Like This </li> 
      <li id="li_5E874ACB5B004CACBDB4F8FF217BC593">More Products Like This </li> 
     </ul> </p> <p>See <a href="../c_recommendations/c_algorithms/c_algorithms.md#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Improved reporting details shown when using Analytics as your reporting source. </td> 
   <td colname="col2"> <p>The details shown by default in an Analytics report when using A4T now match the details shown in the Target report. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* Fixed an issue in the Global Experience Composer that prevented dragging a corner to resize a custom viewport.


**Known Issues** 

The following known issues have been reported: 


*


## Adobe Target Standard/Premium 15.9.1 (September 30, 2015) {#section_A54204291A99476688E8C0BD8255F93C}

This release includes the following features and enhancements: 



<table id="table_907A952F54084C2A9C61F10E2B7A7BFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Mobile Web Experience Composer </td> 
   <td colname="col2"> <p> View your site as it looks on various mobile devices and different screen sizes. Set responsive site breakpoints once and use them across your activities to make sure your optimization activities look great on all the devices your visitors use. </p> <p>See <a href="../c_experiences/c_mobile_viewports/c_mobile_viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5" format="dita" scope="local"> Mobile Viewports for Responsive Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Location targeting on form-based activity creation </td> 
   <td colname="col2"> <p> Apply targeting to your mbox locations to limit where your activity displays. </p> <p>See <a href="../c_experiences/t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Export/Download Summary reports for Automated Personalization and Recommendations Premium </entry> <entry colname="col2"> <p>The ability to download data in a .csv format for quick import into Excel or other data analysis programs has been added to Automated Personalization and Recommendations Premium. </p> <p>This feature was previously only available for A/B, Experience Targeting, and Multivariate activities. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> Background color selection in Visual Experience Composer for MVT and Automated Personalization activities </td> 
   <td colname="col2"> <p>A color picker enables you to set background colors when editing Automated Personalization and Multivariate Test activities. </p> <p>This feature was previously only available for A/B and Experience Targeting activities. </p> <p>See <a href="../c_experiences/r_viztarget_options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rich Text and HTML editing in Visual Experience Composer for MVT and Automated Personalization activities </td> 
   <td colname="col2"> <p> Text and HTML formatting in a word processor-like window when editing Automated Personalization and Multivariate Test activities. </p> <p> This feature was previously only available for A/B and Experience Targeting activities. </p> <p>These actions provide rich-text editing capabilities by adding HTML tags or applying styles. These modifications by the rich-text editor for any action can be seen in its source view. Users can press the HTML button in the rich-text editor to see the source view. The styles added by the rich-text editor can interfere with customer websites' styles. In this case, users can go to the source view and edit the modifications to align them with their websites' styles. </p> <p>See <a href="../c_experiences/r_viztarget_options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p class="Premium">Form-based recommendations </p> </td> 
   <td colname="col2"> <p> Create recommendations activities for non-site locations including emails, consoles, kiosks, etc. </p> <p>See <a href="../c_experiences/t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p> Display information about the key in the design </p> </td> 
   <td colname="col2"> <p>Show the key item in your Recommendations design. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_customizing_a_template.html" format="https" scope="external"> Customizing a Design </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Automated Personalization </p> <p>Conversion-based report </p> </td> 
   <td colname="col2"> <p> If the optimization goal is a conversion metric, then the Offer Detail report now shows the impact of the top predictive variables in lift and incremental conversions. This report was only revenue-based before, so this ability ensures that activities with no revenue data still produce relevant and actionable insights. </p> <p>See <a href="../c_reports/c_reports_ap.md#concept_C02BAFC922114A44846998FD956E345A" format="dita" scope="local"> Automated Personalization Reports </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adobe Campaign e-mail integration with Target Standard </td> 
   <td colname="col2"> <p> Previously, it was required to use Target Classic to set up a targeted e-mail campaign using Adobe Campaign. With the release of two new features in Target Standard (form-based activity creation and redirect offers) it is now possible to use Target Standard to set up a targeted e-mail campaign with Adobe Campaign. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/c_campaign_and_target.html" format="https" scope="external"> Integrating Target with Adobe Campaign </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Redirect Offers in Form-Based activity creation </td> 
   <td colname="col2"> <p> Support for the redirect offers functionality of Target Classic added in Target Standard form-based activity creation flow. </p> <p>See <a href="../c_experiences/t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Experience URLs in activities no longer use on-site cookie </td> 
   <td colname="col2"> <p> The preview experience URLs available per activity are now more reliable. Easily copy the URLs and share with other team members, even if they don't use Adobe Target. </p> <p> <p>Note:  Updated experience URLs only work on activities created after July 30, 2015. Older activities continue to use the cookie-based preview functionality. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Reporting enhancement for Analytics as the reporting source for Target </p> </td> 
   <td colname="col2"> <p> Click to view the full Analytics report directly from the activity report page. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/c_reporting.html" format="https" scope="external"> Reporting </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Activity List performance improvements </td> 
   <td colname="col2"> <p>Greatly improved the load time for activities in the list. Searching and filtering are much faster, particularly when there are a lot of activities in the list. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* Fixed an issue that prevented Target report suites from showing up in the Target report suite selector, after being enabled for Analytics for Target.
*


**Known Issues** 

The following known issues have been reported: 


*


## Adobe Target Standard/Premium 15.8.1 (August 20, 2015) {#section_1C26CB72316A404DB655EBE655F5B8C1}

The goal of this release is to provide feature parity with Target Classic. The most commonly used features of Target Classic are now available in Target Standard. 

This release includes the following features and enhancements: 



<table id="table_DF5B434D639345B4ACE2467B8966A908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Create and edit profile scripts </td> 
   <td colname="col2"> <p>Profile scripts run profile attribute "catchers" on each mbox request. When an mbox request is received, Target runs any relevant profile scripts, determines which activity should run, and displays content that is appropriate to that activity and that experience, then tracks the success of the activity. This enables you to track information about the visit, such as the visitor's location, time of day, number of times that visitor has been to the site, if they've purchased before and so on. This information is then added to the visitor's profile so you can better track that visitor's activity on your site. </p> <p>See <a href="../c_target/c_visitor_profile/c_profile_parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profile Attributes </a>. 
     <!--(Copy help from Classic)--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Confidence interval for binary metrics </td> 
   <td colname="col2"> <p>Updated reports using Target-based data show the confidence interval of the lift, compared to the control. </p> <p>See <a href="../c_reports/c_conversion_rate/c_confidence_level_and_confidence_interval.md#concept_0D0002A1EBDF420E9C50E2A46F36629B" format="dita" scope="local"> Confidence Level and Confidence Interval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Download export activity report data </td> 
   <td colname="col2"> <p>Download data in a .csv format for quick import into Excel or other data analysis programs. This feature works for A/B, Experience Targeting, and Multivariate activities. </p> <p>See <a href="../c_reports/c_reports.md#section_3099BC87DCAE46A2B075E1FF5B6552A6" format="dita" scope="local"> Downloading Reports </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rich text and HTML editing in Visual Experience Composer </td> 
   <td colname="col2"> <p>Text formatting options are available when editing text and HTML for A/B and Experience Targeting activities in the Visual Experience Composer. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML. </p> <p>See <a href="../c_experiences/r_viztarget_options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Background color selection in Visual Experience Composer </td> 
   <td colname="col2"> <p>A color picker enables you to set background colors when editing A/B and Experience Targeting activities in the Visual Experience Composer. This option is not available if a background image is set. </p> <p>See <a href="../c_experiences/r_viztarget_options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Archive activity </td> 
   <td colname="col2"> <p>Send an activity to the archive. You can approve an archived activity to make it active again. Activities in the archive do not display by default in the Activities list. </p> <p>See <a href="../c_activities/c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization </p> <p>Offer-level targeting </p> </td> 
   <td colname="col2"> <p>Allows marketers to apply targeting rules to offers in Automated Personalization. Makes it possible to exclude specific offers from being shown to a specified group of people. </p> <p>See <a href="../c_activities/t_automated_personalization/t_ap_target_offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E" format="dita" scope="local"> Target AP Offers </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1"> <p>Automated Personalization </p> <p>Conversion-based Offer Detail report </p> </entry> <entry colname="col2">Reporting improvement. This new functionality allows the Offer Detail report to report using lift and incremental conversions, metrics that are aligned with the optimization goal. Previously, the Offer Detail report in Automated Personalization always reported on revenue even though the optimization goal was a click-based conversion rate, whether or not the activity had revenue being passed in. This required marketers to specify "estimated revenue per conversion" in the Goals and Metrics page for the report to be meaningful. </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Show number of activities using design </p> </td> 
   <td colname="col2"> <p>The design library shows how many live and inactive activities are using each design. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_create_recs_activity.html" format="https" scope="external"> Creating a Recommendations Activity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Customized dynamic title displays in design </p> </td> 
   <td colname="col2"> <p>Choose a title to display when using a particular design. This title does not have to match the title displayed to visitors on the page. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_create_new_algorithm.html" format="https" scope="external"> Create a New Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>API Token </p> </td> 
   <td colname="col2"> <p>You can set your Client API token from Recommendations Premium. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_setup.html" format="https" scope="external"> Settings </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1" outputclass="premium"> <p>Recommendations Premium </p> <p>Key item's attributes can show in design </p> </entry> <entry colname="col2">The key item, the item your recommendations are based on, such as the item the visitor is currently viewing or the item in the cart, is dynamically shown in the recommendations. In cases where there is no key, a random displays in that template location. </entry> </row> --> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> When entering a URL for an activity or a new page within an activity, a menu shows the most recent and most frequently used URLs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>You can now target multiple mobile devices without requiring a profile script.</p> <p>See <a href="../c_target/c_audiences/c_target_rules/c_mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobile </a>. 
     <!--<p> <ul id="ul_1F4F703828A845FF82D9797A2B36D801"> <li id="li_E69E5AEAD1914EB29AB0A4234057A481">Browser language </li> <li id="li_81D2E07A84A34E7BBCB2F8DF5C7AEE22">Browser version </li><li id="li_ADB0B297EF0941FC86441C2D5932C13A">Multiple mobile devices </li> </ul> </p>--> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Target Standard/Premium 15.7.1 (July 30, 2015) {#section_9C888BFD04A94DD58616D3F67D209CCC}

This release includes the following features and enhancements: 



<table id="table_46FF5AF77D824ADC941B1E472234F05C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity change log </td> 
   <td colname="col2"> <p>The change log lists changes made to an activity. The action and the user are listed with a timestamp for each change. </p> <p>See <a href="../c_activities/t_change_log.md#task_D6F224E8CE8346699187D21CD9A2B4AB" format="dita" scope="local"> Activity Change Log </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multipage activity </td> 
   <td colname="col2"> <p>A multipage activity enables you to create a story over multiple pages, with a design that is specific to each page. </p> <p>For example, you might want to test an offer for free shipping with purchases above a certain amount. You might want that offer to appear on your landing page, a category page, and certain product pages, but you want it to be a different size and in a different location on each page type. You could display a prominent offer on your home page, then reinforce that offer with smaller offers on other relevant pages. </p> <p>You can also use a multipage activity to define different layouts for your desktop and non-responsive mobile sites. </p> <p>See <a href="../c_experiences/c_multipage_activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48" format="dita" scope="local"> Multipage Activity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based activity creation </td> 
   <td colname="col2"> <p>Create an activity without using the Visual Experience Composer. Instead, choose locations and offers through a form. With this, Target Standard activities can be delivered in emails, mobile apps, kiosks, and other places that don't work with a Visual Experience Composer. </p> <p>See <a href="../c_experiences/t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New mbox.js </p> </td> 
   <td colname="col2"> <p> Version 58 of mbox.js ensures the Experience Cloud Visitor ID service is ready before the Target calls are made. This ensures that audience data shared through the Profiles and Audiences core service are available on the same hit. However, flicker can occur on the page while Target waits for the service to return, so full QA is important before upgrading. This mbox.js version is only available via API. </p> <p>See the <a href="https://marketing.adobe.com/resources/help/en_US/target/ov/r_mboxjs_change_log.html" format="https" scope="external"> mbox.js change log </a> for information about each version of mbox.js. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Configurable success metrics </td> 
   <td colname="col2"> <p> Fine-grained options let you determine how to count success metrics. Options include counting the metric per impression or once per visitor, and choosing whether to keep the user in the activity or removing them. This is equivalent to the "advanced options" for success metrics available in Target Classic. </p> <p>See <a href="../r_success_metrics/r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Experience Targeting experience limit removed. </td> 
   <td colname="col2"> The previous limit of ten experiences in Experience Targeting has been removed. </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration <TGT-9897> </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
  <tr> 
   <td colname="col1"> Mbox.js management and editing options </td> 
   <td colname="col2"> <p>All mbox.js configuration and editing is now available within Target Standard. You no longer need to make modifications in Target Classic. </p> <p>See <a href="https://marketing-beta.adobe.com/resources/help/target/ov/r_advanced_mboxjs_settings.html" format="https" scope="external"> Advanced mbox.js Settings </a>. 
     <!--Beta link--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Real-time profile syncing for 3rdPartyId data </td> 
   <td colname="col2"> When a site visitor logs in mid-session and gets a 3rdpartyId, all previously-loaded profile attributes tied to the 3rdPartyId are now immediately available. See <a href="../c_target/c_audiences/c_target_rules/c_visitor_profile.md#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Visitor Profile </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations Premium: Facet Name Search </td> 
   <td colname="col2"> You can now search for a facet name. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Automated Personalization: Post-goal metric tracking </td> 
   <td colname="col2"> <p> Previously, Target restarted an experience when the visitor hit the modeling goal. Now, users can be kept in the activity for tracking purposes after reaching the modeling goal. </p> <p> For example, often an Automated Personalization activity is used to improve click-rates, and that is set as the modeling goal. However, it's important to see how increased click-rates lead to final conversion, so tracking through the final conversion is essential. </p> See <a href="../c_activities/t_automated_personalization/t_automated_personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


*
*
*
*


**Known Issues** 

The following known issues have been reported: 


*


## Adobe Target Standard/Premium 15.6.1 (June 25, 2015) {#section_43FEA310830E4E8E853FAB56B12B1301}

This release includes the following features and enhancements: 



<table id="table_C0B37E1730014ADA8C36310093F5C43A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Configurable success metrics </p> </entry> <entry colname="col2"> <p>Includes advanced options for success metrics, such as <varname>count once</varname>, <varname>restart new experience</varname>, and so on. The default for new activities is now <varname>count once</varname>, replacing the former default of <varname>always convert</varname>. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer compatibility improvements </p> </td> 
   <td colname="col2"> <p> A new account-wide setting to make it easier for Target to generate the right CSS selectors. For example, it can be specified if Target should use classes or IDs. This improves compatibility with AEM. This setting can be overridden per activity </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/ov/t_account_preferences.html" format="https" scope="external"> Account Preferences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting support for Analytics as a reporting source </p> </td> 
   <td colname="col2"> <p>You can now use Analytics as a reporting source for Experience Targeting activities. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/r_xt_goals_and_settings.html" format="https" scope="external"> Goals and Settings </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1"> <p>New mbox.js </p> </entry> <entry colname="col2"> <p>Version 58 of mbox.js adds asynchronous loading. This enables the Visitor ID service to load before the first call is made to Target. This ensures that audience sharing is available on the first hit, which is important if you use the profiles and audiences core service. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: Visual indication of model status </p> </td> 
   <td colname="col2"> <p> Once a predictive model passes the required quality criteria and is deemed valid, it is considered ready and is used to calculate a personalized score for offer decisioning. A clock icon changes to a check mark when the model is ready and Target is able to begin delivering personalized content. Since lift is expected only after the models are ready, the visual indication allows you to set the right expectation. Use the traffic estimator in the Visual Experience Composer to get a guideline of when the models will be ready. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_ap_traffic_estimator.html" format="https" scope="external"> Estimate the Traffic Required for Success </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium Recommendations: Browse and Navigate in the Visual Experience Composer </p> </td> 
   <td colname="col2"> <p> Allows you to open the visual experience composer on one page, and then follow links and form submissions to reach other pages on your site, such as a shopping cart. Once on the page you want to test, flip the Visual Experience Composer back to "Compose" mode and create your experiences. For example, you can change a message on the Shipping page, then test it against the default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium Recommendations: Faceted Catalog Search </p> </td> 
   <td colname="col2"> <p> Provides a more robust way to search your catalog. Also makes it easier to narrow down the search results to very specific set of products. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p> You will now see Target Classic campaigns within the Target Standard Activities list. If you want to filter out Target Classic campaigns and only view Target Standard you can use the "Source" search filter option. For example, to view only Adobe Target Standard activities select the source filter and type "Adobe Target" as the source. The ability to view activities created in Recommendations Classic or Adobe Mobile Services will be added in a future release. </p> <p>You can activate and deactivate activities created in other solutions using the Target user interface. For all other changes you will be need to edit the activities in the source solution. </p> <p> For activities created in other solutions, audience information is not visible on the Overview page. View the audience information in the solution where the activity was created. </p> <p>See <a href="../c_activities/c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


*
*
*
*
*
*
*


## Adobe Target Standard/Premium 15.5.1_Hotfix (May 28, 2015) {#section_D751F55A3812417FAA72BD6872AE3C2A}

This hotfix release includes the following fixes: 


*
*
*


## Adobe Target Standard/Premium 15.5.1 (May 21, 2015) {#section_FF0F959908784AF0906EFB9E8324F207}

This release includes the following features and enhancements: 



<table id="table_3985F758176F4884A94AFDFB78B24209"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Custom code entry and editing in Visual Experience Composer </p> </td> 
   <td colname="col2"> <p>Enables you to see, edit, and add new actions using a code editor within the Visual Experience Composer. </p> <p>See <a href="../c_experiences/c_vec_code_editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Add JavaScript and CSS to the top of your page </p> </td> 
   <td colname="col2"> <p> Add JavaScript code to your page(s) right below the <span class="codeph"> &amp;lt;body&amp;gt; </span> tag, without requiring the selection of an element on your page. </p> <p>See <a href="../c_experiences/c_vec_code_editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New Audience Creation Options </p> </td> 
   <td colname="col2"> <p>You can now target by the following (located in the Geo section when creating an audience): </p> <p> 
     <ul id="ul_FE1E3605FB8042E9B5E80C0DB0C6C2AD"> 
      <li id="li_6D112A4DB2344B4E9F1B84E943A43DD8">ISP </li> 
      <li id="li_5C95F3F55D194D81905F8138FB546288">Network domain </li> 
      <li id="li_63E3606516BC4FFC8C91E49297542464">Connection speed (options are: broadband, dialup, mobile, t1, t3, satellite) </li> 
     </ul> </p> <p>See <a href="../c_target/c_audiences/c_audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium New Features </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6DC206CB52E34498BC762FCCF77807AA"> 
      <li id="li_B26568D642974F17B4B2D6E42CFDC5B9"> <p>New Preview mode to view designs with JavaScript </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_create_recs_activity.html" format="https" scope="external"> Create a Recommendations Activity </a>. </p> </li> 
      <li id="li_B8D1ADE874D244F198CBD3387ED3E310"> <p>Catalog Search now supports free search for English language </p> </li> 
      <li id="li_EB8D595EA8A84B37A3262F76543E1B05"> <p>Account-level support for inputting a static, base url to prepend to all relative <span class="codeph"> entity.thumbnailUrl </span> values </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_setup.html" format="https" scope="external"> Setup </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Recommendations Premium Enhancements </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_1CF5F2D0CDE84DDC9C445B5CD878EEAA"> 
      <li id="li_EB225752776449C6B21C2B2514B508C5"> <p>Improvements to design preview in VEC </p> </li> 
      <li id="li_2CD8267EF166421DBB6EFBF704625848"> <p>Layout improvements on out-of-the-box designs </p> </li> 
      <li id="li_D737754C200844638B536A3BE02E9C5F"> Collection shown in targeting diagram <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_collections.html" format="https" scope="external"> Collections </a>. </p> </li> 
     </ul> </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_recommendations.html" format="https" scope="external"> Recommendations </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Recommendations Classic functionality now supported in Recommendations Premium </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E0D6A9C12B514DE3B3EA753BB4D56662"> 
      <li id="li_2A728C8938834162A0C0C1C926AC5DD9"> Partial template rendering <p>See <a href="../c_recommendations/c_algorithms/t_create_new_algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96" format="dita" scope="local"> Content Settings </a>. </p> </li> 
      <li id="li_B1DFC829D19B4570AB5A7F937C7EF2CC"> Specify backup rules per criteria </li> 
      <li id="li_F8C9690CEC974E37B72A85C2FACFAA6D"> Support FTPS for product feeds <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_feeds_create.html" format="https" scope="external"> Create Feed </a>. </p> </li> 
      <li id="li_3C0FA493C87345E4BE994936DF0D0162"> Custom algorithms now appear automatically as criteria <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_algorithms.html" format="https" scope="external"> Criteria </a>. </p> </li> 
      <li id="li_5B074C9FB3CB46EBA6EB4D8B1098480E"> Hourly automatic reindexing of product catalogs for customers without feeds <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_catalog_search.html" format="https" scope="external"> Catalog Search </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: QA links added </p> </td> 
   <td colname="col2"> <p> You can now preview how your experiences will look when delivered. View and share links to your AP experiences on your site to get a "true preview" of the experiences outside of Target's Visual Experience Composer. </p> <p>See <a href="../c_activities/t_automated_personalization/t_automated_personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics-powered MVT: Preview experience from Performance report </p> </td> 
   <td colname="col2"> <p>When using Analytics as the reporting source for multivariate tests, you can preview your MVT activities from the Performance report. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> A/B tests and Experience Targeting: three-step activity creation flow </p> </td> 
   <td colname="col2"> <p> <a href="../c_activities/t_test_ab/t_test_create_ab/t_test_create_ab.md#task_68C8079BF9FF4625A3BD6680D554BB72" format="dita" scope="local"> Create A/B </a>and <a href="../c_activities/t_experience_target/t_xt_create/t_xt_create.md#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local"> Experience Targeting </a> activity in three steps instead of four. This change makes the process of creating these activities more like the workflow of other activities types, such as Automated Personalization and Multivariate Tests. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics as a reporting source is available with most activity types. </p> </td> 
   <td colname="col2"> <p> The A/B with Analytics activity type no longer exists. The option of using Analytics as your reporting source is now available on the Goal &amp;amp; Settings page for all activity types except Automated Personalization and Experience Targeting. As a result, there is no longer a separate activity type called A/B Test with Analytics Data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p> You will now see Target Classic campaigns within the Target Standard Activities list. If you want to filter out Target Classic campaigns and only view Target Standard you can use the "Source" search filter option. For example, to view only Adobe Target Standard activities select the source filter and type "Adobe Target" as the source. The ability to view activities created in Recommendations Classic or Adobe Mobile Services will be added in a future release. </p> <p>See <a href="../c_activities/c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Export Order Audit Report </p> </td> 
   <td colname="col2"> <p> Ability to export/download Order Audit Report added to Target reports. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beta: A4T lift and confidence </p> </td> 
   <td colname="col2"> <p> Lift and confidence now available for Analytics' standard metrics and custom events. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


*
*
*
*


## Adobe Target Standard/Premium15.3.1 (March 26, 2015) {#section_591371851693496C820175753F588E73}

This release includes the following features and enhancements: 



<table id="table_5A2F2058ACFB455E9F69484CA0C8D3DE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer improvements </p> </td> 
   <td colname="col2"> <p>Content that only appears on hover, such as flyout menus and mini-carts, is now selectable for editing in the Visual Experience Composer. </p> <p>See <a href="../c_experiences/c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Traffic Estimator </p> </td> 
   <td colname="col2"> <p>The Traffic Estimator, formerly available only in the Multivariate Test activity type, is now available for Automated Personalization activities. </p> <p>See <a href="../c_activities/t_automated_personalization/t_ap_traffic_estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714" format="dita" scope="local"> Estimate the Traffic Required for Success </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Visual Preview </p> </td> 
   <td colname="col2"> <p>Visually preview every content combination inside the Visual Experience Composer. </p> <p>See <a href="../c_activities/t_automated_personalization/t_ap_preview_experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> Preview Experiences for an Automated Personalization Test </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: Improved content viewing </p> </td> 
   <td colname="col2"> <p>You can now see every item that qualifies for a collection or exclusion when viewing or editing the collection. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_recommendations.html" format="https" scope="external"> Recommendations </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: Improved search results </p> </td> 
   <td colname="col2"> <p>The total number of items that meet each search string is displayed. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_recommendations.html" format="https" scope="external"> Recommendations </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Upload Customer Attributes in Adobe Analytics </p> </td> 
   <td colname="col2"> <p>Analytics users who capture enterprise customer data in a customer relationship management (CRM) database can upload that data into the Experience Cloud. </p> <p>Once the data is in the Experience Cloud, you can, for example, create an audience segment in Analytics that includes customer attributes in the segment definition, and then share that audience with Target. </p> <p> <p>Note:  Target is not yet able to consume raw customer attributes directly. </p> </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/attributes.html" format="https" scope="external"> Customer Attributes </a> in the Experience Cloud Product Documentation.. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* For Analytics for Target based activities, the Lift and Confidence columns are now hidden for Analytics metrics where the calculations cannot be performed.
* Fixed an issue where the short format of the ` charset` metatag was not recognized in the Enhanced Experience Composer


**Known Issues** 


*
* mbox.js version 56 moved the "extra JavaScript" section so it is executed before global mbox. All settings in v56+ are name spaced. If there are functions declared in "extra JavaScript," they must be prefixed with window. See [ mbox.js Change Log ](https://marketing.adobe.com/resources/help/en_US/target/ov/r_mboxjs_change_log.html). 



## Adobe Target 15.2.1 (February 19, 2015) {#section_9AA19B060D814E08A673FB752E21D0C3}

This release includes the following features and enhancements: 



<table id="table_1558E5A5BAB64CC281C193F5A49E2ECE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p class="premium">New activity type: Recommendations </p> </td> 
   <td colname="col2"> <p>Recommendations activities automatically display products or content that might interest your customers based on previous user activity. Recommendations help direct customers to relevant items they might otherwise not know about. </p> <p>Recommendations is available as part of the Target Premium solution. It is not included with Target Standard without a Target Premium license. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mbox.js v56 </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4D4AEAC314964ECFA6C3A2669233060F"> 
      <li id="li_F71CE15AD70E4A6E9216521E8AE2B102"> Changes for Premium Recommendations to support passing parameters into global mbox </li> 
      <li id="li_11F777D04DE04B848F681997C6458C8B"> Adds a 5 second timeout to the target.js load call. In the rare case that the file doesn't load, the page will render and no Target Standard activities will display. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


*


## Adobe Target 15.1.1 (January 22, 2015) {#section_FC6412353DE64E848FFD5E8EFF72C7C7}

This release includes the following features and enhancements: 



<table id="table_4BA8DA701BC64427957355E144570EFE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> New activity type: Multivariate test </td> 
   <td colname="col2"> <p> A full-factorial multivariate test compares all possible combinations of offers in your content areas to help you determine the best possible combination of content. Multivariate tests also show which content in which areas most contributes to activity success. A common use of multivariate tests is to optimize an entire page after you've used an A/B test to determine an optimal layout. With the multivariate test, you can optimize the individual assets on the page (such as the main image, headlines, or promotional content). </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/mvt/c_multivariate_testing.html" format="https" scope="external"> Multivariate Test </a> for more information. </p> <p>For an introductory video, see <a href="https://my.adobeconnect.com/p2k6u8iiu6l/" format="https" scope="external"> https://my.adobeconnect.com/p2k6u8iiu6l/ </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browse to pages and in-page elements in the Visual Experience Composer </td> 
   <td colname="col2"> <p> Allows you to open the visual experience composer on one page, and then follow links and form submissions to reach other pages on your site, such as a shopping cart. Once on the page you want to test, flip the Visual Experience Composer back to "Compose" mode and create your experiences. For example, you can change a message on the Shipping page, then test it against the default. </p> <p> The Browse mode also lets you interact with a page to get to the right state, such as going through an image carousel, open a mini-cart, or close a pop-up. Once the page is in the state you need, flip to "Compose" mode and create your test. </p> <p> Currently works with A/B tests, experience targeting, and A/B tests with Analytics. </p> <p>See <a href="../c_experiences/c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobile device targeting </td> 
   <td colname="col2"> You can select mobile device options when creating an audience. <p>See <a href="../c_target/c_audiences/c_audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Audiences </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Click tracking (Automated Personalization) </td> 
   <td colname="col2"> <p>You can now track clicks in Automated Personalization. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mboxTrace debugging utility </td> 
   <td colname="col2"> <p> Examine details about your Target page implementation and activity/experience delivery status for improved troubleshooting. </p> <p>See <a href="../c_manage_content/c_content_trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Troubleshooting Content Delivery </a> for more information. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* Fixed an issue where scrolling did not work properly in IE10.

