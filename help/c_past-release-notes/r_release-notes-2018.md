---
description: null
seo-description: null
seo-title: Release Notes - 2018
title: Release Notes - 2018
uuid: 34f7deb5-8b00-4547-aceb-ec04c2b6386f
index: y
internal: n
snippet: y
translate: y
---

# Release Notes - 2018


## at.js Version 1.5.0 (June 22, 2018) {#section_53C622F4978F4BC9ACD932D4B7194C12}



<table id="table_B332A93D4A6E4568BA3F7FA8EC0787F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js version 1.5.0 is now available. </p> <p> <p>Note:  The issue numbers in parentheses are for internal Adobe use. </p> </p> <p> 
     <ul id="ul_41FE0EED2D8B4ADE84FC4CA0FA0CE8A0"> 
      <li id="li_2DC17381CB7949AFA35B054B9CA723FA"> <p>The details of the <span class="codeph"> at-request-succeeded </span> event contain the redirect flag. This flag can be used to determine if the page will be redirected to a different URL. If you want to know the URL, subscribe to <span class="codeph"> at-content-rendering-redirect </span>. (TNT-29834) </p> </li> 
      <li id="li_2852878862724BB2BD475C8FC7BF20DA"> <p>Fixed an issue that caused <span class="codeph"> window.targetGlobalSettings.enabled </span> to fail with a runtime exception if it was set to false. (TNT-29829) </p> </li> 
      <li id="li_96E5E409B36444F1B0E3E2606DC03996"> <p>Fixed an issue that caused the page to fail while loading in the Visual Experience Composer (VEC) if using custom code to a fire global mbox request and using body hiding. (TNT-29795) </p> </li> 
      <li id="li_818AA4EDDAC04D8B9BB4BA708D6BEF99"> <p>Added support for <span class="codeph"> screenOrientation </span>, <span class="codeph"> devicePixelRatio </span>, and <span class="codeph"> webGLRenderer </span>. These new Target request parameters are used for iPhone X and other modern device detection. For more information, see <a href="../target/c_mobile.xml#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobile </a>. (TNT-29781) </p> </li> 
      <li id="li_87E3FB8B423C472AB1EE0DF2D7C64885"> <p>Fixed an issue where the Adobe Audience Manager (AAM) location hint wasn't always sent. (TNT-29695) </p> </li> 
      <li id="li_E9E5A5035AC24F54ADEF5447E3F15D3B"> <p>For browsers that support it, at.js 1.5.0 switches to MutationObserver for selector polling. Versions prior to at.js 1.0.0 used a MutationObserver polyfill, which proved to be problematic. To avoid the polyfill issues, version1.5.0 uses the following pseudo code to decide which scheduling mechanism to use: </p> <p> 
        <codeblock>
          if&nbsp;MutationObserver&nbsp;is&nbsp;supported 
         &nbsp;&nbsp;scheduler&nbsp;=&nbsp;MutationObserver 
         else&nbsp;if&nbsp;document&nbsp;is&nbsp;visible 
         &nbsp;&nbsp;scheduler&nbsp;=&nbsp;requestAnimationFrame 
         else 
         &nbsp;&nbsp;scheduler&nbsp;=&nbsp;setTimeout 
        </codeblock> </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 18.6.1 (June 20, 2018) {#section_B63C660815B245DA9922BE33E03734A1}

This release includes the following features and enhancements: 


>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.





<table id="table_5A60FFE5E86148F4BDC6A7031D03D6BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>When you click an action in the Modifications panel, the VEC automatically scrolls the web page and the corresponding element is highlighted. You no longer need to manually scroll down to find the HTML element that was affected by the modification. </p> <p style="text-align: center;"> <img href="../assets/modifications panel.png" id="image_6E01280636E34ADDA9527AD18A34310B" /> </p> <p>(TGT-30441) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Supported browsers </p> </td> 
   <td colname="col2"> <p>Added Microsoft Edge support for the Target UI and for content delivery. </p> <p>For more information, see . <a href="../ov/r_supported_browsers.xml#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Supported Browsers </a> (TGT-14102) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p>The Recently Viewed Items criteria now returns results specific to a given <a href="../ov2/c_hosts.xml#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> environment </a>. If two sites belong to different environments and a visitor switches between the two sites, each site shows only recently viewed items from the appropriate site. If two sites are in the same environment and a visitor switches between the two sites, the visitor will see the same recently viewed items for both sites. </p> <p>For more information, see <a href="../recs/t_create_new_algorithm.xml#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B" format="dita" scope="local"> Base the Recommendation on a Recommendation Key </a>. (RECS-5865) </p> </td> 
  </tr> 
 </tbody> 
</table>



**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following enhancements, fixes, and changes: 


* The Backup row of the Recommendations CSV download now has a leading "*" (double quotes enclosing an asterisk) instead of * (a single asterisk). 

* The Top Sold / Top Viewed row in the Recommendations CSV download no longer has a leading comma. 



## Target Platform Changes (June 19, 2018) {#section_0638BD69F3C640479A2A258AD78C0884}

This release includes the following enhancement: 


>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.




* Updated the device list to include the latest phone models. Added the capability to deliver targeted content to specific iPhone models by using the Device Marketing Name or Device Model. 

  Customers using the Mobile SDK do not need to do anything to leverage this functionality. Customers using ` at.js` must upgrade to ` at.js` version 1.5.0. 

  For more information, see [ Mobile ](c_mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89). (TNT-26714 &amp; TNT-28288) 



## Target Download API (June 5, 2018) {#section_B8729DA10F18433C8D8E01B04F308ED2}

You can use the recommendations download API to download your recommendations in a .CSV file that can be viewed in a spreadsheet or text editor. For improved security, starting on **June 5, 2018**, Target will block HTTP requests and allow only HTTPS requests. 

## Target Standard/Premium 18.5.1 (May 22, 2018) {#section_7C1427793C2A48DBAC39F8290717DC5B}

This release includes the following features and enhancements: 


>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.





<table id="table_1C51F61184684072BC69AD15BA68BEBB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Reports </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_8D08FE4AC7D748EFB2BBFF87DBDC5CE5"> 
      <li id="li_B8929C19276D42168A28A3775CDEDFB3"> <p>You can save up to ten different presets of an individual activity's report after configuring it as desired (metrics, audiences, advanced settings, and so forth). All Target users can display, edit, and delete the various presets, regardless of who created them. (TGT-21268) </p> </li> 
      <li id="li_7ADA62F2ACA049C9B4A8986B09A9F4AA"> <p>You can configure an individual activity's report as desired and then save that configuration as your default/favorite preset. This is the view that displays whenever you view that activity's report going forward. (TGT-10082) </p> </li> 
      <li id="li_DC63C04F3A884BDDA55B5515E4643B7B"> <p>Alerts and messages inside reports let you know if one (or more) audience, metric, host group, or experience has been deleted from a previously configured preset report. The alert or message instructs you to choose another audience, metric, host group, or experience to make a preset again. (TGT-29424) </p> </li> 
     </ul> </p> <p>For more information, see the Target Preset section in <a href="c_report-settings.xml#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Report Settings </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Profile scripts </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F382C8E7708846A08676E1534BC92878"> 
      <li id="li_70E89504525C4119B588C230DCE772E8"> <p>You can view profile script information pop-up cards similar to offer information cards. These profile script information cards let you view the list of activities that reference the selected profile script, along with other useful metadata. (TGT-28253) </p> <p>For more information, see the Viewing Profile Script Information Cards section in <a href="c_profile_parameters.xml#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profile Script Attributes </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_DFEB778393024E3EBBC482F31A5B39BC"> 
      <li id="li_4049E334A38F4F94842FF1E35F177FE9"> <p>Custom Audience creation now allows using the mbox parameter directly without having to mandatorily specify the mbox name. The mbox name is now optional. This change lets you use parameters from multiple mboxes or reference a parameter that has not yet been recorded on the edge. Alternately, you can also filter on mbox parameter with the mbox name filter. </p> <p>This same improvement has also been extended to Recommendations Criteria, Recommendations Promotions, and Template Testing rules. </p> </li> 
     </ul> </p> <p>For more information, see <a href="c_custom_parameters.xml#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local"> Custom Parameters </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7765B69E679D4C94B1E863E340DFDE15"> 
      <!--<li id="li_6B29B32C84DB4F30A79859DC3AA7E2E1"> <p>You can view a list of activities that reference a selected criteria on its Criteria card. The card lists active and inactive activities. (TGT-27672) </p> </li>--> 
      <li id="li_F2AF7E1AFBD6461990EF1D83D1989582"> <p>While selecting Recommendations criteria in the Form-Based Experience Composer, there is now a direct link to the selected Criteria card so you can quickly and easily edit the criteria. (TGT-28483) </p> <p>For more information, see <a href="t_form_experience_composer.xml#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </li> 
      <li id="li_517F0A174587416B8621D6F710C1AC48"> <p>Recommendations Criteria, Recommendations Promotions, and Template Testing rules creation now allow using the mbox parameter directly without having to mandatorily specify the mbox name. The mbox name is now optional. This change lets you use parameters from multiple mboxes or reference a parameter that has not yet been recorded on the edge. Alternately, you can also filter on mbox parameter with the mbox name filter. </p> <p>This same improvement has also been extended to Custom Audience creation. </p> <p>For more information, see <a href="../recs/c_recommendations-faq.xml#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Recommendations FAQ </a>. </p> </li> 
      <li id="li_AAB242830D1E47B78E58A980B717C736"> <p>Updated the UI for Recommendations Design cards. </p> </li> 
      <li id="li_1BE3178663E54F4CA8714FE3ACDBB97B"> <p>The Target Recommendations API documentation can be found on the <a href="https://www.adobe.io/apis/experiencecloud/target/docs/getting-started.html" format="html" scope="external"> Adobe I/0 Adobe Target website </a> (https://www.adobe.io/apis/experiencecloud/target/docs/getting-started.html). </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following enhancements, fixes, and changes: 


* Updated the UI for Step 2 of the Target three-step guided workflow used to create or edit an A/B Test, Experience Targeting (XT), or Recommendations activity. (TGT-18911) 



## Target Standard/Premium 18.4.1 (April 25, 2018) {#section_445DBC5402BA456BAF2D24AEA33A91C9}

This release includes the following features and enhancements: 


>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.





<table id="table_6D99C48B72D24728BF623608053931D3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Adobe Experience Manager (AEM) Experience Fragments </p> </td> 
   <td colname="col2"> <p>Using experience fragments created in AEM in Target activities lets you combine the ease-of-use and power of AEM with powerful Automated Intelligence (AI) and Machine Learning (ML) capabilities in Target to test and personalize experiences at scale.&amp;nbsp;&amp;nbsp; </p> <p>AEM brings together all of your content and assets in a central location to fuel your personalization strategy. AEM lets you easily create content for desktops, tablets, and mobile devices in one location without writing code. There’s no need to create pages for every device—AEM automatically adjusts each experience using your content. </p> <p> Target lets you deliver personalized experiences at scale based on a combination of rules-based and AI-driven machine learning approaches that incorporate behavioral, contextual, and offline variables.&amp;nbsp; With Target you can easily set up and run A/B and Multivariate activities to determine the best offers, content, and experiences. </p> <p>Experience fragments represent a huge step forward to link the content/experience creators and managers to the optimization and personalization professionals who are driving business outcomes using Target. </p> <p>For more information, see <a href="aem-experience-fragments.xml#topic_1E1E4EA01F074349B2CF8785387B5FE8" format="dita" scope="local"> AEM Experience Fragments </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reports </p> </td> 
   <td colname="col2"> 
    <ul id="ul_EAB90C510EA04D6A8AEFF23A77DB2337"> 
     <!--<li id="li_B8929C19276D42168A28A3775CDEDFB3"> <p>You can now save up to ten different presets of an individual activity's report after configuring it as desired (metrics, audiences, Advanced settings, and so forth). All Target users can display the various presets, but only the creator of the preset or a Target admin can edit or delete them. (TGT-21268) </p> </li>--> 
     <li id="li_47DA6EB92CC84FFDBFDC9CC9386AF654"> <p>You can now refresh a report to update the report's table and graph view without refreshing the entire page, its configuration, or its date range. (TGT-28125) </p> <p>For more information, see <a href="c_report-settings.xml#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Report Settings </a>. </p> </li> 
     <li id="li_AB2DE7A45D914FD7AEB0832187AF3844"> <p>The calendar in reports now contains pre-defined date ranges, such as Last 7 Days, Last 15 Days, and so forth. (TGT-29171) </p> <p>For more information, see <a href="c_report-settings.xml#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Report Settings </a>. </p> </li> 
     <li id="li_46DF9037E0ED4935B3BCDB35E8BED065"> <p>The table view column width was modified to reduce horizontal scrolling when multiple metrics are applied. (TGT-26575) </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>UI localization </p> </td> 
   <td colname="col2"> <p>The Target UI is now available in the following languages: </p> <p> 
     <ul id="ul_DB6C771FCFDF43F498F8754920A70BCD"> 
      <li id="li_A65D07DF66844AC8BEEC1D413F214191"> <p>Chinese Simplified </p> </li> 
      <li id="li_5986DD06AF5B4F76B3A02CFBF2DC3644"> <p>Chinese Traditional </p> </li> 
      <li id="li_341FDC1CEC2B4C4BBD45CB2A0A54F2A3"> <p>Korean </p> </li> 
      <li id="li_A4C31539B98E42348D5F1A18C63EAB6C"> <p>Italian </p> </li> 
      <li id="li_97E3E0A916B64601BBF601AAED581174"> <p>Portuguese </p> </li> 
     </ul> </p> <p>The <a href="https://marketing.adobe.com/resources/help/en_US/target/" format="https" scope="external"> Target Product Documentation </a> is currently being localized and will be posted in the above languages when ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>When creating a custom audience based on an mbox parameter, <span class="codeph"> mboxParameter </span> no longer prompts you for <span class="codeph"> mboxName </span>. mbox name is now optional. This change lets you use parameters from multiple mboxes or reference a parameter that has not yet been recorded on the edge. (TGT-25807) </p> <p> <p>Note:  This feature is visible in the Target UI but is currently disabled. This feature will be enabled soon (date to be communicated). </p> </p> 
    <!--<p>For more information, see <xref href="c_custom_parameters.xml#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local">Custom Parameters</xref>. </p>--> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following enhancements, fixes, and changes: 


* Transport Layer Security (TLS) is the most-widely deployed security protocol used today for web browsers and other applications that require data to be securely exchanged over a network. Adobe has security compliance standards that require the end-of-life of older protocols and is mandating the use of TLS 1.2 in order to have the most up-to-date and secure version in use. Starting with the Target 18.4.1 release (April 25, 2018), Adobe Target will take steps to move towards TLS 1.2 encryption and phase out support for TLS 1.0 encryption completely by September 12, 2018. It is important that you go through the specifics and plan out the changes for a smooth transition. For more information, see [ TLS (Transport Layer Security) Encryption Changes ](c_tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451). 

* UI for Recommendations Criteria Cards has been improved for better usability. (TGT-27829) 



## at.js (April 3, 2018) {#section_932DF1004F4648668FE4984BFAF2EC49}

This release includes the following features and enhancements: 



<table id="table_76576D9D931B4DA99900F2C03175938E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js version 1.3.0 is now available. For more information, see <a href="../ov2/c_target-configure-atjs.xml#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Download at.js </a> and <a href="../ov2/r_target-atjs-versions.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> <p> 
     <ul id="ul_349BEB37B6C94FF0801F121042037803"> 
      <li id="li_4C2F82F4DD394ED5A0BFF978B15FEDDF"> <p>The following new events are available to help in tracing, debugging, and customizing interaction with at.js: </p> <p> 
        <ul id="ul_EFF7E2FCEA0D42298779DDE13B54503F"> 
         <li id="li_6A2B06A522004EDE96D9A552571A7C30"> <p>LIBRARY_LOADED </p> </li> 
         <li id="li_61AA203A21DF4B7EAE075374A09C8FF0"> <p>REQUEST_START </p> </li> 
         <li id="li_DAF9CC1E86834C62B93419429B43A2CB"> <p>CONTENT_RENDERING_START </p> </li> 
         <li id="li_A52DC337115248A1BE5AF5B358BE5A9A"> <p>CONTENT_RENDERING_NO_OFFERS </p> </li> 
         <li id="li_7D71E48016B1446995493EBBF7D32447"> <p>CONTENT_RENDERING_REDIRECT </p> </li> 
        </ul> </p> <p>For more information, see <a href="../ov2/cmp_at.js_Functions.xml#reference_A828E4BA535F4E7692A075F3D70CF6CD" format="dita" scope="local"> at.js custom events </a>. </p> </li> 
      <li id="li_E2704294F8BA47FFAABE7572F67FB5C0"> <p>You can augment an at.js request with additional parameters that come from data providers. Data providers should be added to <span class="codeph"> window.targetGlobalSettings </span> under the <span class="codeph"> dataProviders key </span>. </p> <p>For more information, see "Data Providers" in <a href="../ov2/cmp_at.js_Functions.xml#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_02EAFE6DA0D44CF88980184FD14226A5"> <p>at.js requests now use GET, but it will switch to POST when the URL size exceeds 2048 characters. There is a new property named <span class="codeph"> urlSizeLimit </span> where you can increase the size limit if necessary. This change allows Target to align at.js to AppMeasurement, which uses the same technique. </p> </li> 
      <li id="li_43363A4F3A764394AA88D2595F93D8C0"> <p>Target now enforces that the <span class="codeph"> mbox </span> key in the <span class="codeph"> adobe.target.applyOffer(options) </span> function is used. This key has been required in the past, but Target now enforces its use to ensure that Target has proper validation and customers are using the function correctly. </p> <p>For more information, see <a href="../ov2/cmp_at.js_Functions.xml#reference_BBE83F513B5B4E03BBC3F50D90864245" format="dita" scope="local"> adobe.target.applyOffer(options) </a> . </p> </li> 
      <li id="li_7336D8D48A894291A378E0BB212B7F9B"> <p>at.js has improved event and click tracking functionality. at.js uses <span class="codeph"> navigator.sendBeacon() </span> to send event tracking data and will fallback to synchronous XHR when <span class="codeph"> navigator.sendBeacon() </span> is not supported. This fallback mostly affects Internet Explorer 10 and 11 and some versions of Safari. Safari will add support for <span class="codeph"> navigator.sendBeacon() </span> in the iOS 11.3 release. </p> </li> 
      <li id="li_28D7324137B14C75BF6F1EA0B2487C9B"> <p>at.js can now render offers even when a page is opened in background tabs. Some Target Customers encountered an issue when <span class="codeph"> requestAnimationFrame() </span> was disabled because of the browser throttling behavior for background tabs. </p> </li> 
      <li id="li_3278979E1C6C41DEA7E8025AEB337985"> <p>This release adds many performance improvements, including shorter callstacks when inspecting a Chrome CPU profile. </p> </li> 
      <li id="li_AAA9C0DCC3354DFA8907968C8E6427F6"> <p>at.js 1.3.0 no longer supports content delivery on Microsoft Internet Explorer 9. For a list of supported browsers, see <a href="../ov/r_supported_browsers.xml#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Supported Browsers </a>. Going forward, all requests are executed via <span class="codeph"> XMLHttpRequest </span> with CORS support with no JSONP requests. This change greatly improves security. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 18.3.1 (March 20, 2018) {#section_880706BE15544A03A2C951F267F4AEC5}

This release includes the following features and enhancements: 


>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.





<table id="table_AE38682151A948AEA21E35A353F18D76"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Popularity by Entity Attribute </p> </td> 
   <td colname="col2"> <p><b>New: March 22, 2018</b> </p> <p>You can now choose the Popularity by Entity attribute in the existing flow when a Custom attribute is selected as the key. </p> <p>After selecting the desired key (in this case, a custom profile attribute), for "Recommendation Logic," you can choose two new options: </p> <p> 
     <ul id="ul_7A6F2398ADE846EF8A7A3110C2736BF7"> 
      <li id="li_66BFF016564749B298B88F6B9638B64E"> <p>Most Viewed </p> </li> 
      <li id="li_937FE5C40ED8471391B282D1ACE8C133"> <p>Top Sellers </p> </li> 
     </ul> </p> <p>For more information, see the "Custom Attribute" row in <a href="../recs/t_create_new_algorithm.xml#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B" format="dita" scope="local"> Base the Recommendation on a Recommendation Key </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>While viewing an audience’s definitions pop-up card (for example, from the Audience Library), you can now see other activities that reference that audience, if applicable. This way you can avoid accidental impact to activities while editing audiences. </p> <p>Previously, when you tried to delete an audience that was referenced by activities, a warning displayed informing you that the audience cannot be deleted with at maximum of 10 activities referencing the audience. </p> <p>For more information, see <a href="c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> About Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reports </p> </td> 
   <td colname="col2"> <p>Improved the lift and bounds information in reports to be more comprehensive and useful, including a tooltip that explains how bounds are calculated. (TGT-28729) </p> <p>For more information, see <a href="average-lift-bounds-and-confidence-interval.xml#topic_AFFDC672A8A34D028B100EF6BE5D8129" format="dita" scope="local"> Average Lift, Lift Bounds, and Confidence Interval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization (AP) and Auto-Target activities </p> </td> 
   <td colname="col2"> <p>Additional guidance is available in the UI and in Help to help you allocate traffic percentages more effectively in Automated Personalization (AP) and Auto-Target activities. </p> <p>For more information, see <a href="c_auto-target-to-optimize.xml#concept_67779E5B7F67427A97D7EA2A6FB919B3/section_AB3656F71D2D4C67A55A24B38092958F" format="dita" scope="local"> Determining Traffic Allocation </a> and <a href="t_create_ap_activity.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creating an Automated Personalization Activity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Inclusion rules, collections, and exclusions for Custom Criteria </p> </td> 
   <td colname="col2"> <p>You can now perform real-time filtering on top of your own custom criteria output. For example, you can limit your recommended items to only those from a visitor's favorite category or brand. This gives you the power to combine off-line calculations with real-time filtering. </p> <p>With the addition of inclusion rules on Custom Criteria, this turns otherwise static recommendations into dynamic recommendations based a visitor's interests. </p> <p> 
     <ul id="ul_BDD55AB34F4A43C691D2399C16AA3D6C"> 
      <li id="li_133C33E0D02E4861A4C855BD8A492E69"> <p>Custom Criteria are now configurable, like other criteria in recommendations. </p> </li> 
      <li id="li_AC201F0917BF465C985E8947635F762E"> <p>You can use collections, exclusions, and inclusions (including the special rules for Price and Inventory) in the same way as any other criteria. Collections and exclusions were already supported. This release adds inclusions. </p> </li> 
     </ul> </p> <p>For more information, see <a href="../recs/c_algorithms.xml#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria </a>. </p> <p>(TGT-28488) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Inclusion rules, collections, and exclusions for Recently Viewed Criteria </p> </td> 
   <td colname="col2"> <p>Recently Viewed items can now be filtered so that only items with a particular attribute are displayed. For example, a multi-national company with multiple businesses might have a visitor view items across multiple digital properties. In this case, you can limit the recently viewed items to display only for the respective property where it was viewed. This prevents Recently Viewed items from displaying on another digital property's site. </p> <p> 
     <ul id="ul_A2D260F01CA047EEA72EF56BD0EE88FA"> 
      <li id="li_DB107DD357B741CCB2B7A4FDAD16F9D6"> <p>Recently Viewed Criteria are now configurable, like other criteria in recommendations. </p> </li> 
      <li id="li_85452C03F0924D4C8D854509F1293021"> <p>You can use collections, exclusions, and inclusions (including the special rules for Price and Inventory) in the same way as any other criteria. Collections and exclusions were already supported. This release adds inclusions. </p> </li> 
     </ul> </p> <p>For more information, see <a href="../recs/c_algorithms.xml#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria </a>. </p> <p>(TGT-22843) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target Extension for Adobe Launch </p> </td> 
   <td colname="col2"> <p>Launch is the next-generation of tag management capabilities from Adobe. Launch gives customers a simple way to deploy and manage all of the analytics, marketing, and advertising tags necessary to power relevant customer experiences. </p> <p>The Target extension lets you quickly and easily implement Target in your environment. </p> <p>For more information, see <a href="../ov2/cmp_implementing-target-using-adobe-launch.xml#topic_5234DDAEB0834333BD6BA1B05892FC25" format="dita" scope="local"> Implementing Target using Adobe Launch </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following enhancements, fixes, and changes: 


* When creating or editing A/B and Experience Targeting (XT) activities, Target retains information about the last opened experience, page, or experience version (via multiple audiences feature) and opens the appropriate page the next time you open the Target UI. (TGT-28225) 

* Security fixes have been made for compliance purposes. 



## Target Standard/Premium 18.2.1 (February 15, 2018) {#section_837CBBB7A89D45D99855A8C5F5E7BFFB}

This release includes the following features and enhancements: 



<table id="table_1C7A462AE8D4492FA5555F060031F665"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>The Adobe Marketing Cloud has been re-branded and is now called the Adobe Experience Cloud. </p> </td> 
   <td colname="col2"> <p>The Experience Cloud is Adobe's integrated family of digital marketing solutions and services. It's also an intuitive interface that lets you quickly access your cloud solutions and core services. </p> <p>Re-branding and UI Changes: Adobe Marketing Cloud has been re-branded and is now called the Adobe Experience Cloud. In addition, you will see UI changes in the Target interface and in the Solution Switcher. </p> <p>For more information about this change, see <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/solutions-core-services.html" format="html" scope="external"> About the new cloud names in Experience Cloud </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes some back-end enhancements, fixes, and changes. 

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
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js 1.2.3 adds support for JSON offers. JSON offers are supported only in activities created using the Form-based Experience Composer. Currently the only way to use JSON offers is via direct API calls. See <a href="c_create_json_offer.xml#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> Create JSON Offer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Other changes </p> </td> 
   <td colname="col2"> <p>Exclusion rules, catalogs, algorithm inclusion rules, and run-time filtering are now case in-sensitive. </p> </td> 
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
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_42D7C86043C94A7BBA5ED405B2902E3A"> 
      <li id="li_50F2A7D05AB244E18D263A476BD906B3"> <p>You can now create Time Frame audiences without start or end dates. This lets you use the same audience in multiple activities (without making a copy of the audience) while controlling the start and end dates at the activity level. See <a href="c_time-frame.xml#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. (TGT-25975) </p> </li> 
      <!--<li id="li_0A4BF407694F4B0C99A6F020916A193A"> <p>While viewing an audience’s definitions pop-up card from the Audience Library, you can now see other activities that reference that audience, if applicable. This way you can avoid accidental impact to other activities while editing audiences. Previously, when you tried to delete an audience that was referenced by other activities, a warning displayed informing you that the audience cannot be deleted with at max 10 activities referencing the audience. See <xref href="c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local">About Audiences</xref>. (TGT- 26275) </p> </li>--> 
      <li id="li_6F08D63BC4F040859D51C47C3521C5E1"> <p>Copy and Edit functionality is available for activity-only audiences when you hover over an audience on the Choose Audience &gt; Activity Only Audience page. Previously, this functionality existed only for Library audiences. See <a href="creating-activity-only-audience.xml#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Creating an Activity-Only Audience </a>. (TGT-27410) </p> </li> 
      <li id="li_A8CF45E6DC37401AA273F7D6CF617524"> <p>Activity-only audiences across activities can have the same name. Previously, duplicate names would result in the addition of time stamps—a duplicate audience named “Target on Weekday” would get saved as “Target on Weekday-1456732099201.” </p> <p>Library audiences continue to require unique names. (TGT-17967) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reports </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C595EEF916494342AD99FF0FDF999927"> 
      <li id="li_8C74478D3480406591DC876F69C19329"> <p>You can now view confidence intervals for continuous variables. (TGT-22085) </p> </li> 
      <li id="li_21B31F91685C46CAA47688FDE5735312"> <p>Target now displays lift bounds when statistically significant in reports.(TGT-27301, TGT-27794, and TGT-26387) </p> </li> 
     </ul> </p> <p>See <a href="c_report-settings.xml#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Report Settings </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_BD0C5B260E7E4F139FBC1FBA286C0B81"> 
      <li id="li_FCDBABE6C5034A3596F5BBF024245FB9"> <p>Target now supports creation of JSON offers in the Offer Library for use in the Form-Based Experience Composer. See <a href="c_create_json_offer.xml#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> Create JSON Offer </a>. (TGT-27064) </p> </li> 
      <li id="li_5500AE7DCF4146E88E4619382CE8E836"> <p>You can now view the activities that reference a code offer in each offer's definition pop-up card. This functionality does not apply to image offers. See <a href="c_manage_content.xml#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. (TGT- 26277) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_63613AD2D744442AA12CD23F4DAC75B4"> 
      <li id="li_4DD5CF06D93A4083BCB34A4FFA293C89"> <p>The UI now displays the status of uploading custom algorithm data for recommendations. See <a href="../recs/t_recommendations_csv.xml#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> Uploading Custom Criteria </a>. (TGT-23891) </p> </li> 
      <li id="li_14FCFDD0A0E84B47AF1488DB4DDF197B">The Value is Present and Value is Not Present operators are now available while creating algorithm inclusion rules. See <a href="../recs/c_use-dynamic-and-static-inclusion-rules.xml#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. (TGT-24110) </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Target Insider newsletter </p> </td> 
   <td colname="col2"> <p>The Adobe Target Insider is a monthly newsletter for members of the Adobe Target community. Learn about product updates and future plans, personalization and optimization tips and tricks, customer successes, upcoming events, information-filled white papers, popular blog posts, and more. Read the <a href="https://theblog.adobe.com/stay-optimized-adobe-target-insider-newsletter/" format="https" scope="external"> announcement letter </a> to learn more. </p> <p> <a href="https://www.adobe.com/subscription/adobe_target_newsletter.html" format="html" scope="external"> Subscribe to the newsletter </a> to help you deliver the exceptional customer experiences that drive business success. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following customer-facing enhancements, fixes, and changes: 


* You can now scroll the page while rearranging experiences on Step 2 of the three-step guided workflow while creating activities. (TGT-27652) 

* You can right-click an activity from the Activity List to open the activity in a new tab. For example, in Firefox, right-click the desired activity &amp;gt; Open Link in New Tab. (TGT-27409) 

* Made performance improvements to the Designs page (Recommendations &amp;gt; Designs). The speed to display and search for designs has been improved. (TGT-21792) 

* at.js is now the default implementation option to download. (TGT-24676) 

* URL validation now allows the use of double hyphens in the URL. Previously, a URL with double hyphens could not be loaded into the Visual Experience Composer (VEC). (TGT-28176) 

* Multiple UI localization fixes for supported languages. 


