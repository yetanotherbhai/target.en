---
description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
keywords: Release notes;prerelease
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
seo-title: Target Release Notes
solution: Target
title: Target Release Notes
topic: Recommendations
uuid: 70a73ae3-e3b9-496d-b442-b82ffb7f65e2
index: y
internal: n
snippet: y
translate: y
---

# Target Release Notes


<a id="section_209FD0D5FA5B4EC2AEABB2CC7901612F"></a>



<table id="table_1DAD8293D4A447D9932083FB9488EAA2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Announcements:</b> </p> <p> 
     <ul id="ul_A0205508929340CB89A766AA047E8363"> 
      <li id="li_27A12387D508414BA5DFCD743432E735"> <p>Participate in the new <a href="c_target-customer-success-webinar-series.xml#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Target Basics Webinar Series </a>. Sign up now for the next session. </p> </li> 
      <li id="li_262EDDD313B5423DA77D002B8AF747C6"> <p> Starting with the Target 18.4.1 release (April 25, 2018), Adobe Target will take steps to move towards TLS 1.2 encryption and phase out support for TLS 1.0 encryption completely by September 12, 2018. It is important that you go through the specifics and plan out the changes for a smooth transition. For more information, see <a href="c_tls-transport-layer-security-encryption.xml#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> TLS (Transport Layer Security) Encryption Changes </a>. </p> </li> 
      <li id="li_CC766ADAE921431486E513373EBFF5AC"> <p> <a href="c_target-insider-newsletter.xml#concept_7600A06142034A3FA325EF7FA898DDE8" format="dita" scope="local"> Subscribe to the Adobe Target Insider Newsletter! </a> The Adobe Target Insider is a monthly newsletter for members of the Adobe Target community. Learn about product updates and future plans, personalization and optimization tips and tricks, customer successes, upcoming events, information-filled white papers, popular blog posts, and more. </p> </li> 
      <!--<li id="li_FA1435E6FB0C455187C3ECA7FE5D63C2"> <p>The Target Classic UI has been decommissioned. Target Classic APIs will be phased out at a later date. For information about switching to Target's modern APIs, see <xref href="https://marketing.adobe.com/resources/help/en_US/target/target/c_target-api-documentation.html#concept_3A31E26C8FAF49598152ACFE088BD4D2" format="html" scope="external"> Transitioning from Target Legacy APIs to Adobe I/O</xref>. </p> </li> <li id="li_1FDE64B48C2542D2923287179568840B"> <p>The Target Recommendations API documentation can be found on the <xref href="https://www.adobe.io/apis/experiencecloud/target/docs/getting-started.html" format="html" scope="external">Adobe I/0 Adobe Target website</xref>. </p> </li>--> 
      <li id="li_B0250D0AA36A4787A6738378699720B4"> <p> For information about Target Delivery APIs, Recommendations APIs, and NodeJS, see <a href="c_api-and-sdk-overview.xml#concept_5718EC1FF2ED4436935D0BCCD7AA29A6" format="dita" scope="local"> Target APIs and NodeJS SDK </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

This section contains the following information: 


* [ Adobe Target Named the Only Leader ](r_release_notes.md#section_42EF75B157DF4DD4BB71DF283F825F40) 

* [ Target Standard/Premium 18.7.1 (July 25, 2018) ](r_release_notes.md#section_3A2216543B064D6F82EC03E1F8AEC74D) 

* [ Release Notes for Other Adobe Target Capabilities ](r_release_notes.md#section_9EB425262A1947D18953F98CF3D4EE71) 

* [ Documentation Changes, Past Release Notes, and Experience Cloud Release Notes ](r_release_notes.md#section_1BC5F5208DA548E9B4344A0836E4B943) 

* [ Prerelease Information ](r_release_notes.md#section_5D588F0415A2435B851A4D0113ACA3A0) 



## Adobe Target Named the Only Leader {#section_42EF75B157DF4DD4BB71DF283F825F40}

Adobe was named the only Leader in The Forrester Wave: Experience Optimization Platforms, Q2 2018 report for its offering in this space, Adobe Target Premium. Adobe received the highest scores in the current offering, strategy, and market presence categories. We also received the highest scores in the online testing, behavioral targeting, and product vision criteria, and among the highest scores in the execution roadmap, performance, and partner ecosystem criteria. The report is based on a thorough evaluation of eight experience optimization platform providers across 24 criteria. Read more in the [ Adobe Blog ](https://theblog.adobe.com/adobe-named-leader-forrester-wave-experience-optimization-platforms/). 

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
   <td colname="col2"> <p>Edit and delete experiences right from the activity diagram. Now you can jump into the Visual Experience Composer (VEC) for a specific experience or delete an experience right from the diagram. </p> <p style="text-align: center;"> <img href="/migration-test-20180813/assets/experience edit.png" id="image_FA6E5F07B04A4B4BA02EA71EDB6908A7" /> </p> <p>See: </p> <p> 
     <ul id="ul_CB0C1146716F4C09BF924CF3DFA7DC1A"> 
      <li id="li_3767DD36F597481FB312CC577CD668F0"> <p>A/B activity: <a href="t_ab_add_experience.xml#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Add Experience </a> </p> </li> 
      <li id="li_E2990CA178C6446BA7206643A3164FEF"> <p>XT activity: <a href="t_xt_add_experience.xml#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Create Experience </a> </p> </li> 
     </ul> </p> <p>(TGT-30229) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>Compare one profile attribute to another profile attribute instead of to a static number. </p> <p>See <a href="c_creating-a-profile-attribute-comparison-audience.xml#concept_4C2124B79A5B4556A6C1D10C0F5E40A0" format="dita" scope="local"> Creating a Profile Attribute Comparison Audience </a>. </p> <p> (TGT-28406) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom Code </p> </td> 
   <td colname="col2"> <p>"Custom Code" is now available from the "Add Modifications" panel instead of having its own tab. You can also add more than one custom code and optionally name each custom code. (TGT-28504) </p> <p>See <a href="c_vec_code_editor.xml#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Modifications </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_371C18DFC6D24E94B3D4FFFD83FC8D3A"> 
      <li id="li_9D11939014E7479AB7FD8910852A5386"> <p>View a list of activities that reference a selected criteria on its Criteria card. The card lists active and inactive activities. (TGT-27672) </p> </li> 
      <li id="li_B97BF9305EB04F6D8B1F6178B2E0CB34"> <p>From the activity diagram, Criteria cards now show when results are ready to display. (TGT-27673) </p> <p>See <a href="../recs/c_algorithms.xml#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Templates </p> </td> 
   <td colname="col2"> <p>Adobe Target Experience Templates are pre-coded offer samples with configurable inputs to be used in Target to execute some common marketer use cases. These experience templates are provided free to developers and marketers as a starting point to execute some common external use cases in Adobe Target - either via the Visual Experience Composer or Form-Based Experience Composer. Customization might be required to integrate successfully with your webpage or platform architecture. </p> <p>See <a href="c_vec_code_editor.xml#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Modifications </a> and <a href="https://github.com/Adobe-Marketing-Cloud/target-experience-templates" format="https" scope="external"> Target-Experience-Templates </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target Basics Webinar Series </p> </td> 
   <td colname="col2"> <p>Participate in the new <a href="c_target-customer-success-webinar-series.xml#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Target Basics Webinar Series </a>, a Customer Success Webinar Series brought to you by the Community. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following enhancements, fixes, and changes: 


* Increased the Rich Text Editor modal's size for better usability. (TGT-24775) 

* The diagrams in the Target step (step 2 of the three-step guided workflow) for Automated Personalization (AP) and Multivariate Test (MVT) activities have been redesigned to be more consistent with the designs used for A/B, Experience Targeting (XT), and Recommendations activities. (TGT-30712) 

* The metric value for the Multivariate Test (MVT) Location Contribution report is now more consistent with the values for other metrics, which is rounded to two decimal places. (TGT-30921) 



## Release Notes for Other Adobe Target Capabilities {#section_9EB425262A1947D18953F98CF3D4EE71}

Use the following links to view release notes for Target capabilities other than Target Standard and Target Premium: 


* [ Recommendations Classic release notes ](https://marketing.adobe.com/resources/help/en_US/rec/r_whatsnew-recs.html)
* [ Search&amp;amp;Promote release notes ](https://marketing.adobe.com/resources/help/en_US/snp/c_searchpromote_release_notes.html)


## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes {#section_1BC5F5208DA548E9B4344A0836E4B943}

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
   <td colname="col2"> <p>View detailed information about updates to this guide that might not be included in these release notes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="c_past-release-notes.xml#concept_314253EBB7FF47AD8F7CF29B91964362" format="dita" scope="local"> Past Release Notes </a> </p> </td> 
   <td colname="col2"> <p>View information about new features and enhancements in previous releases of <span class="keyword"> Target Standard </span> and <span class="keyword"> Target Premium </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="http://wwwimages.adobe.com/content/dam/acom/en/marketing-cloud/testing-targeting/54658.en.target.capabilities.whats-new-fall-2016.pdf" format="pdf" scope="external"> What’s New in Adobe Target 2016 </a> (PDF) </p> </td> 
   <td colname="col2"> <p>Display a graphical review of features released in 2016. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/whatsnew/" format="https" scope="external"> Experience Cloud Release Notes </a> </p> </td> 
   <td colname="col2"> <p>View the latest release notes for the <span class="keyword"> Adobe Experience Cloud </span> solutions. </p> </td> 
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
   <td colname="col1"> <p>Adobe Priority Product Update list </p> </td> 
   <td colname="col2"> <p>To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update: </p> <p> <a href="https://www.adobe.com/subscription/priority-product-update.html" format="html" scope="external"> https://www.adobe.com/subscription/priority-product-update.html </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Current and upcoming release notes </p> </td> 
   <td colname="col2"> <p>For information about the current month's Target releases, including prerelease information, see the <a href="https://marketing.adobe.com/resources/help/en_US/target/rn/" format="https" scope="external"> Adobe Target Release Notes </a> page. </p> </td> 
  </tr> 
 </tbody> 
</table>

