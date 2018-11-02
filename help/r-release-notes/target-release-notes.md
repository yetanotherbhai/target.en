---
description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
keywords: release notes
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
seo-title: Target release notes (prerelease)
solution: Target
title: Target release notes (prerelease)
topic: Standard
uuid: e9401a4e-b66f-46e7-bd69-97e12ca9644b
index: y
internal: n
snippet: y
---

# Target release notes (prerelease)

These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.

<a id="section_209FD0D5FA5B4EC2AEABB2CC7901612F"></a>

**Last Updated: October 31, 2018**

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change. To view information about the current release, see [Target Release Notes](https://marketing.adobe.com/resources/help/en_US/target/target/r_release_notes.html) in the Target documentation. Depending on the timing of releases, the information on these pages might differ.

<table id="table_1DAD8293D4A447D9932083FB9488EAA2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Announcements:</b> </p> <p> 
     <ul id="ul_A0205508929340CB89A766AA047E8363"> 
      <li id="li_248ACD8F14F74ECEB34E18DB16CFD1C5"> <p> Starting with the Target 18.4.1 release (April 25, 2018), Adobe Target will take steps to move towards TLS 1.2 encryption and phase out support for TLS 1.0 encryption. Migrating to TLS 1.2 will provide improved security. It is important that you go through the specifics and plan out the changes for a smooth transition. For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_tls-transport-layer-security-encryption.html" format="html" scope="external"> TLS (Transport Layer Security) Encryption Changes</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Target Standard/Premium 18.11.1 (November 12, 2018) {#section_6BBA8B1EE9D241C28E12856A375E97F6}

This Target release includes back-end enhancements, fixes, and changes.

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
   <td colname="col2"> <p>You can now copy an experience in an Experience Targeting (XT) activity so you can make minor changes to it without having to re-create the experience from scratch. This capability was already available for A/B Tests. (TGT-31504) </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_xt_add_experience.html" format="html" scope="external"> Create experience</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Offers in Automated Personalization (AP) activities </p> </td> 
   <td colname="col2"> <p>In the September 2018 release, we added an enhancement that lets you filter offers by reporting groups. You can now filter for Unassigned Offers so you can assign a reporting group to an offer that is not currently assigned to any reporting group. (TGT-31882) </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_create_ap_activity.html" format="html" scope="external"> Create an Automated Personalization activity</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting source for activities </p> </td> 
   <td colname="col2"> <p>In <span class="wintitle"> Setup</span> &gt; <span class="wintitle"> Preferences</span>, you can select the reporting source for your activities, either <span class="keyword"> Target</span> or <span class="keyword"> Adobe Analytics</span>. You can also choose to select your reporting source per activity. </p> <p>Starting with this release, there are some important workflow considerations you should be aware of when you choose the reporting source in <span class="wintitle"> Preferences</span> or per activity. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/ov/r_target-account-preferences.html" format="html" scope="external"> Preferences</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* Improved the handling of audiences referenced in Target activities that have been deleted in Adobe Audience Manager (AAM). (TGT-23338)

    * If an audience was deleted in AAM, a warning icon in both the [!UICONTROL Audience] list and the audience picker displays. A tool-tip in the UI also indicates that the audience was deleted in AAM. 
    * If you attempt to combine multiple audiences with a deleted audience, or if you attempt to save an activity that references a deleted audience, a warning message displays.

  See [About audiences](https://marketing.adobe.com/resources/help/en_US/target/target/c_audiences.html). 

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
     </ul> </p> <p> <p>Important:  In addition, at.js Version 1.6.2 also contains all of the enhancements and fixes included in at.js Version 1.6.1 and 1.6.0. These versions are no longer available for download. We recommend that you upgrade to version 1.6.2 if using 1.6.1 or 1.6.0. </p> </p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-versions.html" format="html" scope="external"> at.js Version Details</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Product Documentation for Target Capabilities {#section_F03C61D438814538967B2BF901130BE4}

Use the following links to view product documentation for Target capabilities:

* [Target Standard/Premium help](https://marketing.adobe.com/resources/help/en_US/target/) 
* [Recommendations Classic help](https://marketing.adobe.com/resources/help/en_US/rec/) 
* [Search&Promote help](https://marketing.adobe.com/resources/help/en_US/snp/)

## Prerelease Information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
