---
description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
keywords: Release notes;prerelease
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
seo-title: Target release notes (current)
solution: Target
title: Target release notes (current)
topic: Recommendations
uuid: cc2671a9-f935-4893-9b49-a759d0cceeb0
index: y
internal: n
snippet: y
---

# Target release notes (current)

These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.

<a id="section_209FD0D5FA5B4EC2AEABB2CC7901612F"></a>

<table id="table_1DAD8293D4A447D9932083FB9488EAA2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Announcements:</b> </p> <p> 
     <ul id="ul_A0205508929340CB89A766AA047E8363"> 
      <li id="li_27A12387D508414BA5DFCD743432E735"> <p>Participate in the new <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Target Basics Webinar Series</a>. Sign up now for the next session. </p> </li> 
      <li id="li_262EDDD313B5423DA77D002B8AF747C6"> <p> Starting with the Target 18.4.1 release (April 25, 2018), Adobe Target will take steps to move towards TLS 1.2 encryption and phase out support for TLS 1.0 encryption by February 2019. Migrating to TLS 1.2 will provide improved security. It is important that you go through the specifics and plan out the changes for a smooth transition. For more information, see <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> TLS (Transport Layer Security) Encryption Changes</a>. </p> </li> 
      <li id="li_CC766ADAE921431486E513373EBFF5AC"> <p><a href="../cmp-resources-and-contact-information.md#concept_7600A06142034A3FA325EF7FA898DDE8" format="dita" scope="local"> Subscribe to the Adobe Target Insider Newsletter!</a> The Adobe Target Insider is a monthly newsletter for members of the Adobe Target community. Learn about product updates and future plans, personalization and optimization tips and tricks, customer successes, upcoming events, information-filled white papers, popular blog posts, and more. </p> </li> 
      <li id="li_B0250D0AA36A4787A6738378699720B4"> <p> For information about Target Delivery APIs, Recommendations APIs, and NodeJS, see <a href="../c-implementing-target/c-api-and-sdk-overview/c-api-and-sdk-overview.md#concept_5718EC1FF2ED4436935D0BCCD7AA29A6" format="dita" scope="local"> Target APIs and NodeJS SDK</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Target Standard/Premium 18.10.1 (October 24, 2018) {#section_66A0030993D54565BE30E56AC9CAC1DA}

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
   <td colname="col1"> <p>Experiences </p> </td> 
   <td colname="col2"> <p>You can now copy an experience in an Experience Targeting (XT) activity so you can make minor changes to it without having to re-create the experience from scratch. This capability was already available for A/B Tests. (TGT-31504) </p> <p>See <a href="../c-activities/t-experience-target/t-xt-create/t-xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Create Experience</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Offers in Automated Personalization (AP) activities </p> </td> 
   <td colname="col2"> <p>In the September 2018 release, we added an enhancement that lets you filter offers by reporting groups. You can now filter for Unassigned Offers so you can assign a reporting group to an offer that is not currently assigned to any reporting group. (TGT-31882) </p> <p>See <a href="../c-activities/t-automated-personalization/t-create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Create an Automated Personalization activity</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting source for activities </p> </td> 
   <td colname="col2"> <p>In <span class="wintitle"> Setup</span> &gt; <span class="wintitle"> Preferences</span>, you can select the reporting source for your activities, either <span class="keyword"> Target</span> or <span class="keyword"> Adobe Analytics</span>. You can also choose to select your reporting source per activity. </p> <p>Starting with this release, there are some important workflow considerations you should be aware of when you choose the reporting source in <span class="wintitle"> Preferences</span> or per activity. </p> <p>For more information, see "Experience Cloud Solution used for reporting" in <a href="../administrating-target/r-target-account-preferences/r-target-account-preferences.md#reference_0CF97B1C2214412ABBC8222EA8A36D7E" format="dita" scope="local"> Preferences</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* Improved the handling of audiences referenced in Target activities that have been deleted in Adobe Audience Manager (AAM). (TGT-23338)

    * If an audience was deleted in AAM, a warning icon in both the [!UICONTROL Audience] list and the audience picker displays. A tool-tip in the UI also indicates that the audience was deleted in AAM. 
    * If you attempt to combine multiple audiences with a deleted audience, or if you attempt to save an activity that references a deleted audience, a warning message displays.

  See [About audiences](../c-target/c-audiences/c-audiences.md#concept_65BE870D290E412D8BBF557EEA67C271). 

* Fixed an issue that prevented users in certain situations from being able to create an activity when Adobe Analytics was selected as the reporting source on the [!UICONTROL Setup] page. Users saw a "Please select a report suite" message even though they were not given the option of selecting the report suite. (TGT-31968)

## Platform (October 19, 2018) {#section_484A56774E004282B98FFFF851E4E670}

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr>
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>at.js 1.6.2 </p> </td> 
   <td colname="col2"> <p>This is a maintenance release and addresses the following issue: </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>Fixed an issue that on some customer sites lead to an infinite "async" loop. </p> </li> 
     </ul> </p> <p> <p>Important:  In addition, at.js Version 1.6.2 also contains all of the enhancements and fixes included in at.js Version 1.6.1 and 1.6.0. These versions are no longer available for download. We recommend that you upgrade to version 1.6.2 if using 1.6.1 or 1.6.0 </p> </p> <p>For more information, see <a href="../c-implementing-target/c-implementing-target-for-client-side-web/r-target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Release Notes for Other Adobe Target Capabilities {#section_9EB425262A1947D18953F98CF3D4EE71}

Use the following links to view release notes for Target capabilities other than Target Standard and Target Premium:

* [Recommendations Classic release notes](https://marketing.adobe.com/resources/help/en_US/rec/r_whatsnew-recs.html) 
* [Search&Promote release notes](https://marketing.adobe.com/resources/help/en_US/snp/c_searchpromote_release_notes.html)

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
   <td colname="col1"> <p> <a href="../r-release-notes/r-doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C" format="dita" scope="local"> Documentation Changes</a> </p> </td> 
   <td colname="col2"> <p>View detailed information about updates to this guide that might not be included in these release notes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../r-release-notes/release-notes-for-previous-releases.md#topic_607D0324907E472EA3682033A27B5F07" format="dita" scope="local"> Release notes for previous releases</a> </p> </td> 
   <td colname="col2"> <p>View information about new features and enhancements in previous releases of <span class="keyword"> Target Standard</span> and <span class="keyword"> Target Premium</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="http://wwwimages.adobe.com/content/dam/acom/en/marketing-cloud/testing-targeting/54658.en.target.capabilities.whats-new-fall-2016.pdf" format="pdf" scope="external"> What’s New in Adobe Target 2016</a> (PDF) </p> </td> 
   <td colname="col2"> <p>Display a graphical review of features released in 2016. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/whatsnew/" format="https" scope="external"> Experience Cloud Release Notes</a> </p> </td> 
   <td colname="col2"> <p>View the latest release notes for the<span class="keyword"> Adobe Experience Cloud</span> solutions. </p> </td> 
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
   <td colname="col2"> <p>To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update: </p> <p> <a href="https://www.adobe.com/subscription/priority-product-update.html" format="html" scope="external"> https://www.adobe.com/subscription/priority-product-update.html</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Current and upcoming release notes </p> </td> 
   <td colname="col2"> <p>For information about the current month's Target releases, including prerelease information, see the <a href="https://marketing.adobe.com/resources/help/en_US/target/rn/" format="https" scope="external"> Target Release Notes - Prerelease</a> page. </p> </td> 
  </tr> 
 </tbody> 
</table>

