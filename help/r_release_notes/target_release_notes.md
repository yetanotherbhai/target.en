---
description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
keywords: release notes
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
seo-title: Target Release Notes - Prerelease
solution: Target
title: Target Release Notes - Prerelease
topic: Standard
uuid: 1e97b4d2-55a4-43d6-9012-2bc25ae526ec
index: y
internal: n
snippet: y
translate: y
---

# Target Release Notes - Prerelease


<a id="section_209FD0D5FA5B4EC2AEABB2CC7901612F"></a>

**Last Updated: August 13, 2018** 


>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change. To view information about the current release, see[ Target Release Notes ](https://marketing.adobe.com/resources/help/en_US/target/target/r_release_notes.html) in the Target documentation. Depending on the timing of releases, the information on these pages might differ. 





<table id="table_1DAD8293D4A447D9932083FB9488EAA2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Announcements:</b> </p> <p> 
     <ul id="ul_A0205508929340CB89A766AA047E8363"> 
      <li id="li_248ACD8F14F74ECEB34E18DB16CFD1C5"> <p> Starting with the Target 18.4.1 release (April 25, 2018), Adobe Target will take steps to move towards TLS 1.2 encryption and phase out support for TLS 1.0 encryption completely by September 12, 2018. It is important that you go through the specifics and plan out the changes for a smooth transition. For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_tls-transport-layer-security-encryption.html" format="html" scope="external"> TLS (Transport Layer Security) Encryption Changes </a> . </p> </li> 
      <li id="li_CC766ADAE921431486E513373EBFF5AC"> <p> <a href="https://www.adobe.com/subscription/adobe_target_newsletter.html" format="html" scope="external"> Subscribe to the Adobe Target Insider Newsletter! </a> The Adobe Target Insider is a monthly newsletter for members of the Adobe Target community. Learn about product updates and future plans, personalization and optimization tips and tricks, customer successes, upcoming events, information-filled white papers, popular blog posts, and more. Read the <a href="https://theblog.adobe.com/stay-optimized-adobe-target-insider-newsletter/" format="https" scope="external"> announcement letter </a> to learn more. </p> </li> 
      <li id="li_B0250D0AA36A4787A6738378699720B4"> <p> For information about Target Delivery APIs, Recommendations APIs, and NodeJS, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_api-and-sdk-overview.html" format="html" scope="external"> Target APIs and NodeJS SDK </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

This section contains the following information: 


* [ Forrester Wave Report: Target Named the Only Leader ](../r_release_notes/target_release_notes.md#section_42EF75B157DF4DD4BB71DF283F825F40)
* [ at.js 1.6.0 (August 13, 2018) ](../r_release_notes/target_release_notes.md#section_4198E76F2DF6412F932674B463BA8B74)
* [ Target Standard/Premium 18.8.1 (August 21, 2018) ](../r_release_notes/target_release_notes.md#section_66A0030993D54565BE30E56AC9CAC1DA)
* [ Target Standard/Premium 18.7.1 (July 25, 2018) ](../r_release_notes/target_release_notes.md#section_3A2216543B064D6F82EC03E1F8AEC74D)
* [ Product Documentation for Target Capabilities ](../r_release_notes/target_release_notes.md#section_F03C61D438814538967B2BF901130BE4)
* [ Prerelease Information ](../r_release_notes/target_release_notes.md#section_7B9D4AAFC6A74388B9D7DEF0658D8B63)


## Forrester Wave Report: Target Named the Only Leader {#section_42EF75B157DF4DD4BB71DF283F825F40}

Adobe was named the only Leader in The Forrester Wave: Experience Optimization Platforms, Q2 2018 report for its offering in this space, Adobe Target Premium. Adobe received the highest scores in the current offering, strategy, and market presence categories. We also received the highest scores in the online testing, behavioral targeting, and product vision criteria, and among the highest scores in the execution roadmap, performance, and partner ecosystem criteria. The report is based on a thorough evaluation of eight experience optimization platform providers across 24 criteria. Read more in the [ Adobe Blog ](https://theblog.adobe.com/adobe-named-leader-forrester-wave-experience-optimization-platforms/). 

## at.js 1.6.0 (August 13, 2018) {#section_4198E76F2DF6412F932674B463BA8B74}

This release is a maintenance release and includes the following enhancements: 


* Redirect offers are now automatically supported in the Analytics for Target (A4T) integration. The client-side workaround has been removed. (TNT-30247) 

* Client-side edge routing is now enabled by default. (TNT-30261) 

* Fixed an issue with Visual Experience Composer (VEC) action rendering when there are dependencies between actions. (TNT-30248) 




>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.



## Target Standard/Premium 18.8.1 (August 21, 2018) {#section_66A0030993D54565BE30E56AC9CAC1DA}

This release includes the following features and enhancements: 


>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.





<table id="table_4785030753B24AA1A973E1DF790B83DD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Personalization Insights reports </p> </td> 
   <td colname="col2"> <p>Access specialized reports for your Automated Personalization (AP) and Auto-Target (AT) activities: </p> <p> 
     <ul id="ul_54652C5AE0984657BB9A0E46673CB2F1"> 
      <li id="li_0807959BA7D94114BE47A43D3454CAB4"> <p><b>Automated Segments:</b> See how different automated segments defined by Target's personalization models respond to offers/experiences in your activity. </p> </li> 
      <li id="li_48210B1E4EB24288B96CDECAF1CEE34A"> <p><b>Model Attribute Ranking:</b> See the top attributes that influenced Target's personalization models and the relative importance of each attribute. </p> </li> 
     </ul> </p> <p> <p>Note:  This feature will be available August 30, 2018. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_406B95728467496CA6CC5892F88B69FE"> 
      <li id="li_6D717868FB204A3A95832E709773B424"> <p>You can dock the Modifications panel vertically along the side of the Target UI or horizontally at the bottom. </p> </li> 
      <li id="li_27FEBEE245E64ADF9ADF561C6CBBDE8F"> <p>You can edit offers more efficiently, thanks to a larger edit window. (TGT-31052) </p> </li> 
      <li id="li_27750AFBCB3E4CB8B0B53592B2447E59"> <p>We have grouped various VEC actions to make your job quicker and more efficient. (TGT-30472) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tips and Tricks </p> </td> 
   <td colname="col2"> <p>Get the most out of Adobe Target by learning more about various features and see why you should give them a try. Tips and Tricks provides links to videos, use-cases, blogs, documentation, and much more. Become a Target Power User! </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following enhancements, fixes, and changes: 


* We have added several improvements to make Target even more secure than it was before. (TGT-31090, TGT-31089, TGT-31143) 



## Target Standard/Premium 18.7.1 (July 25, 2018) {#section_3A2216543B064D6F82EC03E1F8AEC74D}

This release includes the following features and enhancements: 


>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.





<table id="table_7E3513EABA4948DC92EADCCE0234A9FF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>A/B and Experience Targeting (XT) activities </p> </td> 
   <td colname="col2"> <p>Edit and delete experiences right from the activity diagram. Now you can jump into the Visual Experience Composer (VEC) for a specific experience or delete an experience right from the diagram. </p> <p style="text-align: center;"> <img href="assets/experience_edit.png" id="image_FA6E5F07B04A4B4BA02EA71EDB6908A7" /> </p> <p>For more information, see: </p> <p> 
     <ul id="ul_CB0C1146716F4C09BF924CF3DFA7DC1A"> 
      <li id="li_3767DD36F597481FB312CC577CD668F0">A/B activity: <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_ab_add_experience.html" format="html" scope="external"> Add Experience </a> </li> 
      <li id="li_E2990CA178C6446BA7206643A3164FEF">XT activity: <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_xt_add_experience.html" format="html" scope="external"> Create Experience </a> </li> 
     </ul> </p> <p>(TGT-30229) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>You can create an audience that is defined to compare two profile attributes for your audience library or in an activity-only audience. (TGT-28406) </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_creating-a-profile-attribute-comparison-audience.html" format="html" scope="external"> Creating a Profile Attribute Comparison Audience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom Code </p> </td> 
   <td colname="col2"> <p>"Custom Code" is now available from the "Add Modifications" section instead of having its own tab. You can also add more than one custom code and optionally name each custom code. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_vec_code_editor.html" format="html" scope="external"> Modifications </a>. </p> <p>(TGT-28504) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_371C18DFC6D24E94B3D4FFFD83FC8D3A"> 
      <li id="li_9D11939014E7479AB7FD8910852A5386"> <p>You can view a list of activities that reference a selected criteria on its Criteria card. The card lists active and inactive activities. (TGT-27672) </p> </li> 
      <li id="li_B97BF9305EB04F6D8B1F6178B2E0CB34"> <p>From the activity diagram, Criteria cards now indicate when results are ready to display. (TGT-27673) </p> </li> 
     </ul> </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_algorithms.html" format="html" scope="external"> Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Templates </p> </td> 
   <td colname="col2"> <p>Adobe Target Experience Templates are pre-coded offer samples with configurable inputs to be used in Target to execute some common marketer use cases. These experience templates are provided free to developers and marketers as a starting point to execute some common external use cases in Adobe Target - either via the Visual Experience Composer or Form-Based Experience Composer. Customization might be required to integrate successfully with your webpage or platform architecture. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_vec_code_editor.html" format="html" scope="external"> Modifications </a> and <a href="https://github.com/Adobe-Marketing-Cloud/target-experience-templates" format="https" scope="external"> Target-Experience-Templates </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target Basics Webinar Series </p> </td> 
   <td colname="col2"> <p>Participate in the new <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_target-customer-success-webinar-series.html#concept_11902FAC95C64479AABE020557A7EEE4" format="html" scope="external"> Target Basics Webinar Series </a>, a Customer Success Webinar Series brought to you by the Community. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following enhancements, fixes, and changes: 


* Increased the Rich Text Editor modal's size for better usability. (TGT-24775) 

* The diagrams in the Target step (step 2 of the three-step guided workflow) for Automated Personalization (AP) and Multivariate Test (MVT) activities have been redesigned to be more consistent with the designs used for A/B, Experience Targeting (XT), and Recommendations activities. (TGT-30712) 

* The metric value for the Multivariate Test (MVT) Location Contribution report is now more consistent with the values for other metrics, which is rounded to two decimal places. (TGT-30921) 



## Product Documentation for Target Capabilities {#section_F03C61D438814538967B2BF901130BE4}

Use the following links to view product documentation for Target capabilities: 


* [ Target Standard/Premium help ](https://marketing.adobe.com/resources/help/en_US/target/)
* [ Recommendations Classic help ](https://marketing.adobe.com/resources/help/en_US/rec/)
* [ Search&amp;amp;Promote help ](https://marketing.adobe.com/resources/help/en_US/snp/)


## Prerelease Information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update: 

[ https://www.adobe.com/subscription/priority-product-update.html ](https://www.adobe.com/subscription/priority-product-update.html) 
