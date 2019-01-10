---
description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
keywords: release notes
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
seo-title: Target release notes (prerelease)
solution: Target
title: Target release notes (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming [!DNL Adobe Target] releases.

**Last Updated: January 10, 2019**

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change. To view information about the current release, see [Target Release Notes](release-notes.md) in the [!DNL Target] documentation. Depending on the timing of releases, the information on these pages might differ.

<table id="table_1DAD8293D4A447D9932083FB9488EAA2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Announcements:</b> </p> <p> 
     <ul id="ul_A0205508929340CB89A766AA047E8363"> 
      <lI>Target and the Adobe Marketing Cloud will drop support for Microsoft Internet Explorer 11 starting in March 2019. This change affects Target authoring only; this change does not affect experience delivery. Please switch to Microsoft Edge or another supported browser. For more information, see <a href="/help/c-implementing-target/c-considerations-before-you-implement-target/r-supported-browsers.md" format="dita" scope="local"> Supported Browsers</a>.</li> </li> 
      <li id="li_262EDDD313B5423DA77D002B8AF747C6"> <p> Starting with the Target 18.4.1 release (April 25, 2018), [!DNL Target] will take steps to move towards TLS 1.2 encryption and phase out support for TLS 1.0 encryption by February 2019. Migrating to TLS 1.2 provides improved security. It is important that you go through the specifics and plan out the changes for a smooth transition. For more information, see <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> TLS (Transport Layer Security) Encryption Changes</a>. </p> </li>  
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## [!DNL at.js] version 1.6.4 (January 11, 2019)

[!DNL at.js] 1.6.4 is a maintenance release and addresses the following issue:

* Fixed a race condition manifesting in Microsoft Internet Explorer 11 that caused duplicate offers to be applied.



## [!DNL Target] Standard/Premium 19.1.1 (January 22, 2019) {#section_6BBA8B1EE9D241C28E12856A375E97F6}

This release includes the following features, changes and enhancements:

Note: The issue numbers in parentheses are for internal Adobe use.

<table id="table_EF529199D1C741F7BDBC9C41A37B7D26"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr>
 </thead>
 <tbody>  
  <tr> 
   <td colname="col1" class="premium"> <p>Enterprise Permissions support in Target APIs </p> <p>(Target Premium)</p></td> 
   <td colname="col2"> <p>Adobe Target APIs can now leverage the power of Enterprise Permissions just like the UI. Currently, Target APIs deal only with the default workspace if you are leveraging Enterprise Permissions features. However, now you can work with Target APIs (Activity, Offers, Audiences and Reporting) across all workspaces.</p><p>Note: This feature will be available starting January 31, 2019 after the Adobe I/O APIs are updated. Support for Automated Personalization (AP) activities will come in next release.</P> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: filter collections and exclusions by host group (environment) </p> <p>(Target Premium)</p></td> 
   <td colname="col2"> <p>You can now filter collections and exclusions by host group (environment).</P> <p>Previously, when you viewed the Collections or Exclusions list pages, the items for the default host group (set in Recommendations > Settings > Default Host Group) displayed. You can now filter the pages by host group to view only collections and exclusions for the selected host group.</p><p>Additionally, when you created or edified collections or exclusions, those items were created or edited in the default host group. You can now access the Environment filter to select the desired host group in which to create or edit the collection or exclusion.</p><p>The new Environment filter saves you time and effort because you must no longer navigate to the Settings page to change the default host group every time before viewing, creating, or editing collections and exclusions.</p><p>The new Environment filter is available from the following places in the Target UI:</p><ul><li>Collections list page (Recommendations > Collections)</li><li>Exclusions list page (Recommendations > Exclusions)</li><li>Create Collections dialog box</li><li>Create Exclusions dialog box</li><li>Update Collections dialog box</li><li>Update Exclusions dialog box</ul> <p>(TGT-20622)</P></td> 
  </tr> 
 </tbody> 
</table>

**Enhancement, Fixes, and Changes**

* You are now instructed to re-authenticate when your session expires while reviewing a report. After you log in again, you are directed back to the report. (TGT-32723)

## Product Documentation for [!DNL Target] Capabilities {#section_F03C61D438814538967B2BF901130BE4}

Use the following links to view product documentation for [!DNL Target] capabilities:

* [Adobe Target Learn &amp; Support](https://helpx.adobe.com/support/target.html) 
* [Recommendations Classic release notes](../assets/adobe-recommendations-classic.pdf) 
* [Search&Promote help](https://marketing.adobe.com/resources/help/en_US/snp/)

## Prerelease Information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
