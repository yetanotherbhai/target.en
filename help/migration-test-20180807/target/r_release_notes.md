---
description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
keywords: contact;legal;technical support;tech support;support;service;capability;billing;feedback
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
seo-title: Target Release Notes
solution: Target
title: Target Release Notes
topic: Standard
uuid: 52a30d21-bcf9-43f4-9646-9aa71940fa22
index: y
internal: n
snippet: y
translate: y
---

# Target Release Notes

## Target Release Notes {#reference_8FE40B43A5A34DDF8F26A53D55EE036A}These release notes provide information about features, enhancements, fixes, and known issues for each 
<keyword>
  Target Standard 
</keyword> and 
<keyword>
  Target Premium 
</keyword> release.
<a id="section_209FD0D5FA5B4EC2AEABB2CC7901612F"></a>



<table id="table_1DAD8293D4A447D9932083FB9488EAA2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>On November 14, 2017, Target Classic will be decommissioned. For everything you need to know about making the move from Target Classic to the new Adobe Target Standard/Premium, see <a href="../ov/c_target-transition-classic-to-standard.xml#concept_00A8245A46284AEEB145884D4C27562A" format="dita" scope="local"> Transitioning from Target Classic to Target Standard or Premium </a>. For information about Target Classic APIs, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_target-api-documentation.html" format="html" scope="external"> Transitioning from Target Legacy APIs to Adobe I/O </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Platform (January 18, 2018) {#section_F6A0DC31636D403F92BDB9DCE7A3F6ED}

This release includes the following features and enhancements:


<table id="table_0F5BF9370E214302BDFE0AC2D66EC773"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>at.js</p> </td> 
   <td colname="col2"> <p>at.js 1.2.3 adds support for JSON offers. JSON offers are supported only in activities created using the Form-based Experience Composer. Currently the only way to use JSON offers is via direct API calls. See <a href="c_manage_content.xml#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> Create JSON Offers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Other changes</p> </td> 
   <td colname="col2"> <p>Exclusion rules, catalogs, algorithm inclusion rules, and run-time filtering are now case in-sensitive.</p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 18.1.1 (January 23, 2018) {#section_3A2216543B064D6F82EC03E1F8AEC74D}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.




<table id="table_872FE2BE61CC4A5CA369D9A6C730686E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Audiences</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_42D7C86043C94A7BBA5ED405B2902E3A"> 
      <li id="li_50F2A7D05AB244E18D263A476BD906B3"> <p>You can now create Time Frame audiences without start or end dates. This lets you use the same audience in multiple activities (without making a copy of the audience) while controlling the start and end dates at the activity level. See <a href="c_target_rules.xml#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. (TGT-25975) </p> </li> 
      <!--<li id="li_0A4BF407694F4B0C99A6F020916A193A"> <p>While viewing an audience’s definitions pop-up card from the Audience Library, you can now see other activities that reference that audience, if applicable. This way you can avoid accidental impact to other activities while editing audiences. Previously, when you tried to delete an audience that was referenced by other activities, a warning displayed informing you that the audience cannot be deleted with at max 10 activities referencing the audience. See <xref href="c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local">About Audiences</xref>. (TGT- 26275) </p> </li>--> 
      <li id="li_6F08D63BC4F040859D51C47C3521C5E1"> <p>Copy and Edit functionality is available for activity-only audiences when you hover over an audience on the Choose Audience &gt; Activity Only Audience page. Previously, this functionality existed only for Library audiences. See <a href="c_audiences.xml#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Creating an Activity-Only Audience </a>. (TGT-27410) </p> </li> 
      <li id="li_A8CF45E6DC37401AA273F7D6CF617524"> <p>Activity-only audiences across activities can have the same name. Previously, duplicate names would result in the addition of time stamps—a duplicate audience named “Target on Weekday” would get saved as “Target on Weekday-1456732099201.”</p> <p>Library audiences continue to require unique names. (TGT-17967)</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reports</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C595EEF916494342AD99FF0FDF999927"> 
      <li id="li_8C74478D3480406591DC876F69C19329"> <p>You can now view confidence intervals for continuous variables. (TGT-22085)</p> </li> 
      <li id="li_21B31F91685C46CAA47688FDE5735312"> <p>Target now displays lift bounds when statistically significant in reports.(TGT-27301, TGT-27794, and TGT-26387)</p> </li> 
     </ul> </p> <p>See <a href="c_reports.xml#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Report Settings </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_BD0C5B260E7E4F139FBC1FBA286C0B81"> 
      <li id="li_FCDBABE6C5034A3596F5BBF024245FB9"> <p>Target now supports creation of JSON offers in the Offer Library for use in the Form-Based Experience Composer. See <a href="c_manage_content.xml#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> Create JSON Offers </a>. (TGT-27064) </p> </li> 
      <li id="li_5500AE7DCF4146E88E4619382CE8E836"> <p>You can now view the activities that reference a code offer in each offer's definition pop-up card. This functionality does not apply to image offers. See <a href="c_manage_content.xml#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. (TGT- 26277) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_63613AD2D744442AA12CD23F4DAC75B4"> 
      <li id="li_4DD5CF06D93A4083BCB34A4FFA293C89"> <p>The UI now displays the status of uploading custom algorithm data for recommendations. See <a href="../recs/c_algorithms.xml#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> Uploading Custom Criteria </a>. (TGT-23891) </p> </li> 
      <li id="li_14FCFDD0A0E84B47AF1488DB4DDF197B">The Value is Present and Value is Not Present operators are now available while creating algorithm inclusion rules. See <a href="../recs/t_create_recs_activity.xml#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. (TGT-24110) </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Target Insider newsletter</p> </td> 
   <td colname="col2"> <p>The Adobe Target Insider is a monthly newsletter for members of the Adobe Target community. Learn about product updates and future plans, personalization and optimization tips and tricks, customer successes, upcoming events, information-filled white papers, popular blog posts, and more. Read the <a href="https://theblog.adobe.com/stay-optimized-adobe-target-insider-newsletter/" format="https" scope="external"> announcement letter </a> to learn more. </p> <p> <a href="https://www.adobe.com/subscription/adobe_target_newsletter.html" format="html" scope="external"> Subscribe to the newsletter </a> to help you deliver the exceptional customer experiences that drive business success. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 
This ` Target` release includes the following customer-facing enhancements, fixes, and changes: 

* You can now scroll the page while rearranging experiences on Step 2 of the three-step guided workflow while creating activities. (TGT-27652)

* You can right-click an activity from the Activity List to open the activity in a new tab. For example, in Firefox, right-click the desired activity &gt; Open Link in New Tab. (TGT-27409)

* Made performance improvements to the Designs page (Recommendations &gt; Designs). The speed to display and search for designs has been improved. (TGT-21792)

* at.js is now the default implementation option to download. (TGT-24676)

* URL validation now allows the use of double hyphens in the URL. Previously, a URL with double hyphens could not be loaded into the Visual Experience Composer (VEC). (TGT-28176)

* Multiple UI localization fixes for supported languages.



## Release Notes for Other Adobe Target Capabilities {#section_9EB425262A1947D18953F98CF3D4EE71}

Use the following links to view release notes for Target capabilities other than Target Standard and Target Premium:

* [ Recommendations Classic release notes ](https://marketing.adobe.com/resources/help/en_US/rec/r_whatsnew-recs.html)
* [ Search&amp;Promote release notes ](https://marketing.adobe.com/resources/help/en_US/snp/c_searchpromote_release_notes.html)


## Documentation Changes, Past Release Notes, and Marketing Cloud Release Notes {#section_1BC5F5208DA548E9B4344A0836E4B943}

In addition to the notes for each release, the following resources provide additional information:


<table id="table_9729DAEA57B44D8D9751785BAA43A729"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Resource </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="r_doc_change.xml#reference_366123CF00994BACBBF9BBDF2C4D840C" format="dita" scope="local"> Documentation Changes </a> </p> </td> 
   <td colname="col2"> <p>View detailed information about updates to this guide that might not be included in these release notes.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="c_past-release-notes.xml#concept_314253EBB7FF47AD8F7CF29B91964362" format="dita" scope="local"> Past Release Notes </a> </p> </td> 
   <td colname="col2"> <p>View information about new features and enhancements in previous releases of <span class="keyword"> Target Standard </span> and <span class="keyword"> Target Premium </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="http://wwwimages.adobe.com/content/dam/acom/en/marketing-cloud/testing-targeting/54658.en.target.capabilities.whats-new-fall-2016.pdf" format="pdf" scope="external"> What’s New in Adobe Target 2016 </a> (PDF) </p> </td> 
   <td colname="col2"> <p>Display a graphical review of features released in 2016.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/whatsnew/" format="https" scope="external"> Marketing Cloud Release Notes </a> </p> </td> 
   <td colname="col2"> <p>View the latest release notes for the <span class="keyword"> Adobe Marketing Cloud </span> solutions. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}



<table id="table_51A9CF02F1A34B6497DB81657E4893FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Priority Product Update list</p> </td> 
   <td colname="col2"> <p>To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update:</p> <p> <a href="https://www.adobe.com/subscription/priority-product-update.html" format="html" scope="external"> https://www.adobe.com/subscription/priority-product-update.html </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Current and upcoming release notes</p> </td> 
   <td colname="col2"> <p>For information about the current month's Target releases, including prerelease information, see the <a href="https://marketing.adobe.com/resources/help/en_US/target/rn/" format="https" scope="external"> Adobe Target Release Notes </a> page. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Known Issues and Resolved Issues {#concept_625C3A16B7F24D4B82EFF130F0945541}Information about known issues for this release of 
<keyword>
  Target 
</keyword>. Also includes information about issues that have been resolved. 
<draft-comment otherprops="merge">
  target/known-issues-resolved_issues.xml 
</draft-comment>
## Known Issues {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

The following table lists the known issues for this release:


<table id="table_929058720A9E451CB414D9FD5975A804"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Exclusion groups</p> </td> 
   <td colname="col3"> <p>The following are known issues with exclusion groups:</p> <p> 
     <ul id="ul_02C8799C07AD482692BDFEC180549331"> 
      <li id="li_33078A32F9EC427FB02CB8ACDAE37144"> <p>When auto-dedupe is applied after creating exclusion groups, the count on the activity diagram might be incorrect in the UI.</p> </li> 
      <li id="li_888157037C824C83B36852803201B95F"> <p>When existing activity with Exclusion Group is edited, the manual inclusions might not be correctly reflected in the UI.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Recommendations</p> </td> 
   <td colname="col3"> <p>The following are known issues with Recommendations activities:</p> <p> 
     <ul id="ul_CEFE1D0E9CCE4A0AB641DF6E667CAF63"> 
      <li id="li_51505434C8134075BDD0D270A165174F"> <p>Recommendations "error.restapi.algorithmProfileAttributeInvalid" error occurs when specific profile attributes are used as the criteria key.</p> </li> 
      <li id="li_57221CEAABBB4CE3BE4BDC0D542013A6"> <p>When Back Promotion is used in a Recommendations activity, Criteria inclusion filters don't apply on backup ERs.</p> </li> 
      <li id="li_C23794FE085945C3BF77E318A385E340"> <p>When you edit or copy a Recommendations activity that uses an Attribute Promotion rule, the "Has missing field" error displays when clicking <span class="wintitle"> Save </span>. </p> <p>Workaround: To resolve this issue, open the Promotion dialog box and click <span class="wintitle"> Save </span>, after which the activity will be saved. (KB-1535) </p> </li> 
      <li id="li_A7C21AFDAEEA4A66A82D7F06968530EE"> <p>The Recommendation Feeds UI does not show the correct status of indexing. The backend jobs are functioning correctly, but the UI is not able to fetch and display the current state.</p> <p>Workaround: An Alternative way to determine if a Recommendation Feed for a given Host Group has indexed properly is to check the Product Search UI (logged in as Admin) and view the last indexing time. This timestamp represents the last time the feed for a given host group was indexed. (TGT-27116)</p> </li> 
      <li id="li_76600BEA49E24BB6A0BC619A0B16495F"> <p>Recommended products might not display values up to two decimal points. For example, if you try to display the value in the design as 35.00, Recommendations displays 35 (no decimal points rather than two decimal points). (RECS-5972)</p> <p>Workaround: Pass the value of the entity into two <span class="codeph"> entity.attributes </span>. The first, `entity.value`, is a reserved parameter that expects a double. The second, can be a custom <span class="codeph"> entity.attribute </span> that will store the value of the entity as a string to allow for proper rending. </p> <p>For example:</p> <p> 
        <codeblock>
          "entity.value"&nbsp;:&nbsp;35.00, 
         "entity.displayValue"&nbsp;:&nbsp;"35.00", 
        </codeblock> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multivariate Test (MVT) activities </td> 
   <td colname="col3"> <p>In an MVT activity, the winner shown in the table and graph are not consistent when checking metrics. This occurs if auser switches from Summary to Graph View, then switches back to Summary View, changes a metric and then switches to Graph View. When this issue occurs, the Summary View always shows the correct winner. If the user never switches Graph View between Summary views, the Graph View shows the correct winner.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>at.js</p> </td> 
   <td colname="col3"> <p>The following are known issues with <span class="codeph"> at.js </span>: </p> <p> 
     <ul id="ul_31477BC709A84ECEBA8F5DDF1DC9335F"> 
      <li id="li_4E4ACBC00B03428F9965DBA56EB69838"> <p>When a page is loaded into the Visual Experience Composer (VEC), Target needs to determine if the global mbox setting is enabled or disabled and whether entityID or categoryID is present at the location where the user is trying to apply the recommendation in the VEC. Based on this information the criteria list is filtered. The default list has filtered algorithms, but the <a href="../recs/c_algorithms.xml#task_2203616ABBE342B6ADAB08F278D794FA" format="dita" scope="local"> Compatible checkbox </a> lets you view the complete algorithms list. </p> <p>When using <span class="filepath"> at.js </span>, the <span class="wintitle"> Compatibility </span> checkbox is hidden, so you cannot see incompatible algorithms. </p> <p>This issue applies only to Recommendations activities that use the VEC.</p> <p>As a workaround, you should disable the <span class="wintitle"> Filter Incompatible Criteria </span> option in Recommendations &gt; Settings. After disabling this setting, all criteria (compatible and incompatible) will be shown in the criteria picker. (TGT-25949) </p> </li> 
      <li id="li_93AFF74669DB4E44A59AEE966B95EDDB"> <p>Mboxes not firing on Microsoft Explorer 11 browsers after upgrading to <span class="codeph"> at.js </span> version 1.0 due to the interaction between <span class="keyword"> at.js </span> and Visitor API 2.2.0. This issue affects <span class="codeph"> at.js </span> version 0.9.6 and later. (TNT-27600) </p> </li> 
      <li id="li_D8EC246312F24D0585EA8998AF38A8B9"> <p> <span class="codeph"> at.js </span> might not work with Cordova/Hybrid apps because first-party cookies are not currently supported in them. (TNT-26166) </p> <p>As a workaround, configure <span class="codeph"> at.js </span> with the "x-only" option enabled and pass <span class="filepath"> mboxThirdPartyId </span> in calls to manage users. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mbox.js</p> </td> 
   <td colname="col3"> <p>The <span class="codeph"> mbox.js </span> library does not support client-side templating languages, such as Handlebars and Mustache. The <span class="codeph"> at.js </span> library does support these languages. </p> <p> <p>Note:  The <span class="codeph"> mbox.js </span> library is no longer being developed. All customers should migrate from <span class="codeph"> mbox.js </span> to <span class="codeph"> at.js </span>. For more information, see <a href="../ov2/c_target-atjs-implementation.xml#task_DE55DCE9AC2F49728395665DE1B1E6EA" format="dita" scope="local"> Migrate to at.js from mbox.js </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Redirect offers</p> </td> 
   <td colname="col3"> <p>The following are known issues with redirect offers:</p> <p> 
     <ul id="ul_961891B771FA40A3A34D48CF08E28F55"> 
      <li id="li_496FD2182D654079944732439E3A5837"> <p>A race condition on your page might cause page views on the original page and on the redirect page to be counted. Updates are planned in Q1 2018 to the <span class="filepath"> at.js </span> implementation to ensure that this race condition can be avoided. For more information about the issue and a workaround, see <a href="../a4t/c_a4t-faq-redirect-offers.xml#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Redirect Offers - A4T FAQ </a>. </p> </li> 
      <li id="li_63A5A8139A96453F84A7E095B2A93FF0"> <p>Redirect activities in <span class="codeph"> at.js </span> implementations cause the preview URL to enter into a loop (the offer is delivered repeatedly). </p> <p>This issue does not impact the actual delivery of the offer. (TGT-23019)</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Implementation: Global Mbox Auto Create</p> </td> 
   <td colname="col3"> <p>On the <span class="wintitle"> Implementation </span> tab ( <span class="wintitle"> Setup </span> &gt; <span class="wintitle"> Implementation </span>) the <span class="wintitle"> Global Mbox Auto Create </span> field will be "false" by default for a newly provisioned tenant. </p> <p>When <span class="filepath"> mbox.js </span> is downloaded for the first time after provisioning, the <span class="wintitle"> Global Mbox Auto Create </span> field is set to "true" in the downloaded <span class="filepath"> mbox.js </span> file and in the <span class="keyword"> Target </span> backend, but it will continue to display as "false" on the <span class="wintitle"> Implementation </span> page in the UI until the page is refreshed (after the page is refreshed, the status will be "true.") </p> <p> <span class="filepath"> at.js </span> will be downloaded with <span class="codeph"> global_mbox_autocreate = false </span> for a newly provisioned tenant. If <span class="filepath"> mbox.js </span> is downloaded first, <span class="codeph"> global_mbox_autocreate </span> is set to "true" and <span class="filepath"> at.js </span> will also be downloaded with <span class="codeph"> global_mbox_autocreate = true </span>. (TGT-15929) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Form-based Experience Composer</p> </td> 
   <td colname="col3"> <p>Using the Form-based Experience Composer, you can associate an audience with a location. However, if you select the same audience at the location level and in the Targeting step, you receive a sync error message. This is an invalid setup. In an upcoming release, Target will mark audiences as invalid if the same audience is selected twice. (TGT-27754)</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Success metircs</p> </td> 
   <td colname="col3"> <p>Success metrics with the advanced option "How will the count be incremented" set to "every impression" or "every impression (excluding refreshes)" cannot be used as a success metric that another metric is dependent on.</p> <p>When a success metric is set to be incremented on every impression, Target counts the visitor again every time the visitor visits this success metric. Target then resets the success metric "membership" to 0 so it can count again on the next impression. Thus, if another metric requires this metric to have been seen first, Target will never recognize that the user has seen the first metric.</p> </td> 
  </tr> 
 </tbody> 
</table>


## Resolved Issues {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

As known issues above are resolved, they will be moved to the following table and additional notes, if necessary, will be added.

<table id="table_EB9EA3918D594B5CB8155E77E5931793"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col3" class="entry"> Description </th> 
   <th colname="col4" class="entry"> Notes </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js</p> </td> 
   <td colname="col3"> <p>The algorithm for extracting the top-level domain that should be used when saving cookies has changed in <span class="codeph"> at.js </span> version 0.9.6. Because of this change, cookies cannot be saved to addresses that use IP. Most of the time, IP addresses are used for testing purposes, but as workarounds you can use DNS entries, adjust the hosts file on a local box, or <a href="../ov2/c_target-ats-functions.xml#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> use the <span class="codeph"> targetGlobalSettings() </span> at.js function insert a code snippet to support IP addresses </a>. </p> </td> 
   <td colname="col4"> <p>This issue was remedied in at.js version 1.2.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enterprise User Permissions for Target Premium</p> </td> 
   <td colname="col3"> <p>As part of the Enterprise Permissions migration, all Target Premium user management was moved from the Adobe Target UI to Adobe Admin Console.</p> <p>As a result of the migration, there are two potential issues you should be aware of:</p> <p> 
     <ul id="ul_1EEA21A2B8A6467B8F3DD4C5637DA0F0"> 
      <li id="li_0AF3A22632A34709A8BD0BAF24546DE9"> <p>Non-admin users received an email indicating that they now have access to Adobe Target. This indicates that the migration was completed for your organization. The email itself can be disregarded.</p> </li> 
      <li id="li_B55732FDA9244FC08331204C09427002"> <p>Following the migration, there have been some reports of previously disabled users reappearing in the Adobe Admin Console. This could be an issue for your organization if disabled users in the Adobe Admin Console were still appearing on your user list in Target prior to the migration. We recommend that administrators review the list of users in Admin Console to validate access.</p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p>This issue was fixed on August 30, 2017</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activity Creation</p> </td> 
   <td colname="col3"> <p>An issue with the 17.6.2 release may have affected activities created and/or updated between June 22, 2017 and June 29, 2017. Activities with the following were affected:</p> <p> 
     <ul id="ul_1B2B60770A584FB0A10B368040BCD2AA"> 
      <li id="li_AF342C0F1A684830999D70EE8740317E">Any experiences that were rearranged in Experience Targeting (XT) would have reverted back to the original order</li> 
      <li id="li_759123BB5827459D95445A78E5641B4E">Any segment rules local to the activity (not saved within an audience) would have been lost: combined audiences, location refinements, and any rules on success metrics.</li> 
     </ul> </p> <p>No other activities were affected.</p> <p> <p type="important">Note:  This issue is not fixed automatically. You must re-save any activity that was affected to fix the issue. </p> </p> </td> 
   <td colname="col4"> <p>This issue was fixed on June 29, 2017</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Form-Based Experience Composer</p> </td> 
   <td colname="col3"> <p>The following known issues have been reported when using the Form-Based Experience Composer:</p> <p> 
     <ul id="ul_25843F865BCE43E6A81361FD43AD8B15"> 
      <li id="li_83F6C9576DE64EF1A8FDE3E3FCDD3606"> <p>If you use the Form-Based Experience Composer with an mbox other than the auto-created global mbox ( <span class="codeph"> target-global-mbox </span>), and then choose an engagement metric as a success metric, the metric increments only on pages that have the mbox used in the activity. As an example, if your mbox is <span class="codeph"> homepage_mbox </span>, the <span class="wintitle"> Pages Per Visit </span> metric is the number of hits to the <span class="codeph"> homepage_mbox </span> during that visit. (TGT-22789) </p> </li> 
      <li id="li_6296B3AD67F94577BED07A8E05AE6DB5"> <p>A JavaScript exception is thrown when you delete an experience in an Experience Targeting (XT) activity when using the Form-Based Experience Composer during step 1 of the process. (TGT-24366)</p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p>The first issue was fixed in the Target 17.3.1 release (March 2017).</p> <p>The second issue was fixed in the Target 17.6.1 release (June 2017).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>at.js</p> </td> 
   <td colname="col3"> <p>Since the release of <span class="keyword"> Target </span> 17.4.1 (April 27, 2017), using the Insert Image action in the Visual Experience Composer (VEC) causes the offer content to not be delivered when using the at.js library. </p> </td> 
   <td colname="col4"> <p>A fix for this issue has been made to <span class="codeph"> at.js </span> version 0.9.7 released May 22, 2017. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Recommendations</p> </td> 
   <td colname="col3"> <p> <span class="keyword"> Recommendations </span> feeds take longer to process than expected. (COR-2836) </p> </td> 
   <td colname="col4"> <p>Fixed in the Target 16.10.1 release.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting: A/B and Experience Targeting (XT) activities</p> </td> 
   <td colname="col3"> <p>Between April 27 at 9:00 p.m. PST and May 5 at 6:00 a.m. PST, A/B and XT activities created or edited with any metrics using the “Viewed a Page” conversion action (that were not based on other metrics), might have incorrectly recorded conversions. This issue is now resolved; however, reporting on the “Viewed a Page” conversion action for these activities during the impacted time period might not be accurate and, unfortunately, cannot be corrected. We recommend that for any decisions based on “Viewed a Page” conversion actions for these activities you rely only on data recorded before or after the impacted period.</p> <p>Reporting data for other metrics can still be used because they were not impacted.</p> </td> 
   <td colname="col4"> <p>Fixed in the Target 17.4.3 hotfix.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers: A/B and Experience Targeting (XT) activities</p> </td> 
   <td colname="col3"> <p>The delivery and preview was impacted for offers in A/B and XT activities having at least two experiences and that were either created or edited using the Form-Based Experience Composer between Friday April 28 (9 p.m. PT) and Monday May 1 (9:15 p.m. PT). Only offers with default content were displayed.</p> </td> 
   <td colname="col4"> <p>Fixed in the Target 17.4.3 hotfix.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>at.js</p> </td> 
   <td colname="col3"> <p>The following actions caused the offer to not be delivered when using the Visual Experience Composer (VEC) and at.js: Move and Rearrange.</p> </td> 
   <td colname="col4"> <p>A fix for this issue was made to <span class="codeph"> at.js </span> version 0.9.6. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reports</p> </td> 
   <td colname="col3"> <p>The ability to view multiple metrics in a report, included in the Target 17.3.1 release (March 30, 2017) has been removed due to unexpected behavior. This feature will be available again in an upcoming release.</p> </td> 
   <td colname="col4"> <p>The ability to view multiple metrics in a report was included in the Target 17.4.1 release (April 27, 2017).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers</p> </td> 
   <td colname="col3"> <p>Images deleted from the <span class="wintitle"> Image Offers </span> library ( <span class="wintitle"> Offers </span> &gt; <span class="wintitle"> Image Offers </span>) remain visible in the UI. In an upcoming release, these deleted images will no longer display. In the meantime, deleted images display in the UI, but have a status of <span class="wintitle"> Deleted </span>. (TGT-23793) </p> </td> 
   <td colname="col4"> <p>Fixed in the Target 17.4.1 release (April 27, 2017).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>at.js</p> </td> 
   <td colname="col3"> <p>When users attempt to download <span class="codeph"> at.js </span> from the <a href="../ov2/c_target-atjs-implementation.xml#concept_2FA0456607D04F82B0539C5BF5309812" format="dita" scope="local"> Implementation details </a> page after updating <span class="codeph"> at.js </span> settings, <span class="codeph"> mbox.js </span> is downloaded instead of <span class="codeph"> at.js </span>. (TGT-23069) </p> </td> 
   <td colname="col4"> <p>Fixed in the Target 17.3.1 release (March 30, 2017).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Global exclusion rules</p> </td> 
   <td colname="col3"> <p>Global exclusion rules are taking 10-20 minutes to propagate to the edge for Premium Recommendations. (RECS-5270)</p> </td> 
   <td colname="col4"> <p>Fixed in the <span class="keyword"> Recommendations </span> 17.2.2.0 release (March 6, 2017). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics for Target (A4T) reporting</p> </td> 
   <td colname="col3"> <p>Reports are not updated when the reporting metric is switched. This is a UI issue. There is no impact on reporting data collection or delivery. (TGT-22970)</p> </td> 
   <td colname="col4"> <p>Fixed in the <span class="keyword"> Target </span> 17.2.2.0 release (February 24, 2017). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>CSV reports</p> </td> 
   <td colname="col3"> <p>Downloaded reports do not honor the <span class="wintitle"> Exclude Extreme Orders </span> setting. (TGT-21871) </p> </td> 
   <td colname="col4"> <p>Fixed in the <span class="keyword"> Target </span> 17.2.1.0 release. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## System Status Updates {#concept_5CBDF506BEFA40E483CC7DE0DA915EAD}Use the 
<keyword>
  Adobe 
</keyword> 
<wintitle>
  System Status 
</wintitle> page to view the status of 
<keyword>
  Adobe 
</keyword> products and 
<keyword>
  Marketing Cloud 
</keyword> solutions, including 
<keyword>
  Target 
</keyword>. This page helps you determine whether problems you might encounter are due to system updates or routine maintenance. 
<draft-comment otherprops="merge">
  target/system-status-updates.xml 
</draft-comment>Access the ` System Status` page by going to the following URL: 
[ ` http://status.adobe.com` ](http://status.adobe.com) 
![](graphics/system status.png) 
The available statuses include:

<ul class="simplelist"> 
 <li> Normal </li> 
 <li> Minor Incident </li> 
 <li> Major Incident </li> 
 <li> Reported Event </li> 
 <li> Maintenance </li> 
</ul>


` Ad Hoc Analysis` and ` Marketing Reports &amp; Analytics` were undergoing maintenance when this illustration was created. All other products and solutions were functioning normally. It is always good practice to check this page if you experience problems when using Target. 
An in-product notification always displays during the monthly ` Target` release, but minor updates sometimes occur and will be listed on this page. 
>## Contacting Adobe {#reference_ACA3391A00EF467B87930A450050077C}Client Care is prepared to help you solve any issues that might arise. This page contains the information you need when contacting Client Care to expedite a resolution. 
<draft-comment otherprops="merge">
  target/r_problem.xml 
</draft-comment>
## Basic Information {#section_CC8B206F58D6495C9372D5C0D4055CF6}

If you encounter issues or have questions when using Target, you have a number of options
For questions, you can ask the Adobe Target experts in the [ Marketing Cloud community ](https://forums.adobe.com/community/experience-cloud/marketing-cloud/target) ( ` https://forums.adobe.com/community/experience-cloud/marketing-cloud/target`) or ask us on Twitter at [ @AdobeExpCare ](http://twitter.com/adobeexpcare) ( ` http://twitter.com/adobeexpcare`). 
For technical issues or to log a bug you can contact Customer Care. To contact Customer Care by telephone, call 1-800-497-0335. Toll free numbers outside the United States can be found on the [ Adobe Digital Marketing Customer Care Regional Phone Numbers ](https://helpx.adobe.com/contact/dma-external/DMACustomeCareRegionalPhoneNumbers.html) page ( ` https://helpx.adobe.com/contact/dma-external/DMACustomeCareRegionalPhoneNumbers.html`). When asked to select an option for your product, press 3 to contact the Target team. 
E-mail Customer Care at ` tt-support@adobe.com`. 
For the quickest triage of your issue, please have the following basic information ready when you are contacting us:


<table id="table_6D7C22189503440CB76720C632E479C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Summary</p> </td> 
   <td colname="col2"> <p>Brief summary of the overall issue</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Account information</p> </td> 
   <td colname="col2"> <p>Company Name</p> <p>Admin Number</p> <p>Campaign Name</p> <p>Type of Campaign</p> <p>Report Suite/Report Suite ID (if regarding a Target to SiteCatalyst integration)</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Steps to reproduce</p> </td> 
   <td colname="col2"> <p>Include as much detail as possible, including any URLs needed to duplicate as well as the expected result.</p> <p>Include enough detail that somebody unfamiliar with Target should be able to follow the directions and reproduce the problem.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Priority</p> </td> 
   <td colname="col2"> <p>P1 (most important) to P4 (least important).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Business impact</p> </td> 
   <td colname="col2"> <p>What is the impact to your business? For example, is this issue causing revenue loss or rendering the product unusable, and is there a viable workaround?</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Expectations</p> </td> 
   <td colname="col2"> <p>What do you expect to happen?</p> </td> 
  </tr> 
 </tbody> 
</table>

Also prepare information related to the specific issue. For example, one of the most common problems received by Client Care is that mboxes load too slowly. For this issue, helpful data includes:

* A Firebug trace showing the repeatable slowness to a URL or host. A gomez report with one or two outlying requests is not enough data to analyze or troubleshoot the issue.

* A screenshot of a traceroute from the machine running the firebug TO 70.42.13.100. This is very important. The EDGE networks are worldwide so it is very difficult to determine where the client is being sent. For example, if you can reproduce the issue from your desktop in your office, say "I can reproduce this from my desktop and I am homed to EDGE 20."

* Your client code and the mbox name (if you have it).
* The number of mboxes embedded in the page. Is it a single mbox of many on the page that is slow?

* How repeatable is the slowness with the given mbox on the given page? Providing a Firebug trace shows Client Care a one-time case scenario. If you can provide statistical data, such as "the lowest I've seen is 300ms, highest I've seen is 1.1 seconds and I've tested 50 times," it will help to facilitate a solution.

* Information regarding anything unusual about your campaigns. Is there a high number of segments? (For example, do you update segments 3 to 4 times per hour in the admin interface?) This information helps Client Care understand the interaction between the admin interfaces and the edges for this campaign. Frequent updates to the campaign mean frequent reloads from the central server, which can force more remote calls or cache reloads.

* Any other data you think might be helpful.


## In Case of an Outage {#section_2CB3BC53E4C641F38D50949E2E7A2886}

If you suspect there is an outage, first check the [ Marketing Cloud System Status page ](http://status.adobe.com) ( ` http://status.adobe.com`) This has a record of all outages, incidents and maintenance for Marketing Cloud Solutions, including Target, and includes latest updates from our Tech Ops team. If you still require assistance, please ensure you know the following in addition to the information listed above when you contact Customer Care: 

* Time outage started
* Explanation of what is occurring
* Scope
* Expectation of resolution (ETA, severity, and so on)

>## Contact and Legal Information {#concept_34A1CA16F2244D42930BB77846A5ABBB}Information to help you contact Adobe and to understand the legal issues concerning your use of this product and documentation. 
<draft-comment otherprops="merge">
  target/c_contact_and_legal.xml 
</draft-comment>
## Help & Technical Support {#section_354AC2658BA84A2A96E64C5B2C43B73B}

The Adobe Marketing Cloud Customer Care team is here to assist you and provides a number of mechanisms by which they can be engaged:

* [ Check the Marketing Cloud help pages for advice, tips, and FAQs ](http://helpx.adobe.com/marketing-cloud.html)
* [ Ask us a quick question on Twitter @AdobeExpCare ](https://twitter.com/adobeexpcare)
* [ Log an incident in our customer portal ](https://customers.omniture.com/login.php)
* [ Contact the Customer Care team directly ](http://helpx.adobe.com/marketing-cloud/contact-support.html)
* [ Check availability and status of Marketing Cloud Solutions ](http://status.adobe.com/)
To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update:
[ http://response.adobesystemsinc.com/content/customer-success-subscription ](http://response.adobesystemsinc.com/content/customer-success-subscription) 

## Service, Capability & Billing {#section_FA4F5274FDFE4DF7BB079E575877DFC2}

Dependent on your solution configuration, some options described in this documentation might not be available to you. As each account is unique, please refer to your contract for pricing, due dates, terms, and conditions. If you would like to add to or otherwise change your service level, or if you have questions regarding your current service, please contact your Account Manager.

## Feedback {#section_8154D6D712054220A90D85FA8E92933E}

We welcome any suggestions or feedback regarding this solution. Enhancement ideas and suggestions for the Analytics suite [ can be added to our Customer Idea Exchange ](https://my.omniture.com/login/?r=%2Fp%2Fsuite%2Fcurrent%2Findex.html%3Fa%3DIdeasExchange.Redirect%26redirectreason%3Dnotregistered%26referer%3Dhttp%253A%252F%252Fideas.omniture.com%252Ft5%252FAdobe-Idea-Exchange-for-Omniture%252Fidb-p%252FIdeaExchange3). 

## Legal {#section_A6E1844D4AC2485CADBF6D05116E3D59}


<ul class="simplelist"> 
 <li> © 2018 Adobe Systems Incorporated. All Rights Reserved. </li> 
 <li> Published by Adobe Systems Incorporated. </li> 
</ul>

[ Terms of Use ](http://www.adobe.com/go/marketingcloud_terms_of_use) | [ Privacy Center ](http://www.adobe.com/privacy.html) 
Adobe and the Adobe logo are either registered trademarks or trademarks of Adobe Systems Incorporated in the United States and/or other countries. A trademark symbol (®, ™, etc.) denotes an Adobe trademark.
All third-party trademarks are the property of their respective owners. Updated Information/Additional Third Party Code Information available at [ http://www.adobe.com/go/thirdparty ](http://www.adobe.com/products/eula/third_party/). 
