---
description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
keywords: Release notes;prerelease
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
seo-title: Target release notes (current)
solution: Target
title: Target release notes (current)
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
---

# Target release notes (current){#target-release-notes-current}

These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.

## Announcements

Be aware of the following important announcements:

* We’re looking for the best experience makers. Which means we’re looking for you. The person behind those experiences. The brains. The rock star. The experience maker who worked hard to make something magical happen. Enter your work so we can showcase our amazing customers and partners who've created the world's best experiences. We'll showcase your work at both our North America and EMEA Summit events. For more information, see [2019 Adobe Experience Maker Awards](https://www.adobeexperienceawards.com/). The submission deadline is February 14, 2019.

* [!DNL Target] and the [!DNL Adobe Marketing Cloud] will drop support for Microsoft Internet Explorer 11 starting in March 2019. This change affects [!DNL Target] authoring only; this change does not affect experience delivery. Please switch to Microsoft Edge or another browser. For more information, see [Supported browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).
* Starting with the [!DNL Target] 18.4.1 release (April 25, 2018), [!DNL Target] had taken steps to move towards TLS 1.2 encryption. The final date to completely phase out support for TLS 1.0 encryption is **February 20, 2019**. With this change, [!DNL Adobe] will no longer collect data from end users with older devices or web browsers that do not support TLS 1.1 or later. We do not expect this to have a significant impact to customer data or reporting. Migrating to TLS 1.2 provides improved security. It is important that you go through the specifics and plan out the changes for a smooth transition. For more information, see [TLS (Transport Layer Security) Encryption Changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).

## Platform Changes (January 16 and 17, 2019)

| Feature / Enhancement | Description |
| --- | --- |
|Profile scripts<br>January 17, 2019|For performance reasons, Target requires a return value that is no longer than 256 characters.<br>For a String return value, if the size of the return value exceeds 2048 characters, the script is disabled by the system.<br>For an array return value, if the size of the concatenated values of the array exceeds 2048 characters, the script is disabled by the system.<br>For more information about the character limits and other limits (offer size, audiences, profiles, values, parameters, etc.) that affect activities and other elements in Target, see [Limits](/help/r-troubleshooting-target/target-limits.md).|
|at.js<br>January 16, 2019|at.js 1.6.4 is a maintenance release and addresses the following issues:<ul><li>Fixed a race condition manifesting in Microsoft Internet Explorer 11 that caused duplicate offers to be applied. (TNT-31374)</li><li>Fixed an issue that affected click tracking when there is a default offer with a click-token and html offers. (TNT-31493)</li><li>Extended the mboxEdgeCluster cookie with each Target request. This is used only when mboxEdgeOverride is enabled. (TNT-31485)</li></ul>

## [!DNL Target] Standard/Premium 19.1.1 (January 22, 2019) {#section_6BBA8B1EE9D241C28E12856A375E97F6}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal Adobe use.)

| Feature / Enhancement | Description |
| --- | --- |
| ![Target Premium badge](/help/assets/premium.png)<br/>[!UICONTROL Enterprise Permissions] support in [!DNL Target] APIs | [!DNL Adobe Target] APIs can now leverage the power of [!UICONTROL Enterprise Permissions] just like the [!DNL Target] UI. Currently, [!DNL Target] APIs deal only with the default workspace if you are leveraging [!UICONTROL Enterprise Permissions] features. However, you can now work with [!DNL Target] APIs (Activity, Offers, Audiences, and Reporting) across all workspaces. Resources (activities, audiences, and offers) created using these upgraded APIs will show up in respective workspaces in the [!DNL Target Standard/Premium] interface as well.<br/>**Note:** This feature will be available starting January 31, 2019 after the [!DNL Adobe] I/O APIs are updated. Support for [!UICONTROL Automated Personalization] (AP) activities will come in next release. |
| ![Target Premium badge](/help/assets/premium.png)<br/>[!UICONTROL Recommendations]: filter collections and exclusions by environment (host group) | You can now preview the contents of [!UICONTROL Recommendations] collections and exclusions for a selected environment (host group).<br/>Previously, when you viewed a collection or exclusion, the displayed items contained were results for the default host group (specified in [!UICONTROL Recommendations > Settings > Default Host Group]).<br/>Now, when creating or updating a collection or exclusion, you can use the [!UICONTROL Environment] selector to choose the environment to preview results for. The new [!UICONTROL Environment] filter saves you time and effort because you no longer need to navigate to the [!UICONTROL Settings] page to select the appropriate default host group before creating or editing collections and exclusions.<br/>**Note:** After changing the selected environment, you must click [!UICONTROL Search] to update the returned results.<br/>The new [!UICONTROL Environment] filter is available from the following places in the [!DNL Target] UI:<ul><li>[!UICONTROL Catalog Search] ([!UICONTROL Recommendations > Catalog Search])</li><li>[!UICONTROL Create Collection] dialog box ([!UICONTROL Recommendations > Collections > Create New])</li><li>[!UICONTROL Update Collection] dialog box ([!UICONTROL Recommendations > Collections > Edit])</li><li>[!UICONTROL Create Exclusion] dialog box ([!UICONTROL Recommendations > Exclusions > Create New])</li><li>[!UICONTROL Update Exclusion] dialog box ([!UICONTROL Recommendations > Exclusions > Edit])</li></ul><br>For more information, see the following topics:<uL><li>[Collections](/help/c-recommendations/c-products/collections.md)</li><li>[Exclusions](/help/c-recommendations/c-products/exclusions.md)</li><li>[Catalog Search](/help/c-recommendations/c-products/catalog-search.md)</li><li>[Settings](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84)</li><li>[Recommendations: filter collections and exclusions by environment (host group)](/help/administrating-target/hosts.md)</li></ul>(TGT-20622)</ul>|

**Enhancement, fixes, and changes**

* You are now instructed to re-authenticate when your session expires while reviewing a report. After you log in again, you are directed back to the report. (TGT-32723)

## Release Notes for Other Adobe Target Capabilities {#section_9EB425262A1947D18953F98CF3D4EE71}

Use the following links to view release notes for Target capabilities other than Target Standard and Target Premium:

* [Recommendations Classic release notes](../assets/adobe-recommendations-classic.pdf) 
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
   <td colname="col1"> <p> <a href="../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C" format="dita" scope="local"> Documentation Changes</a> </p> </td> 
   <td colname="col2"> <p>View detailed information about updates to this guide that might not be included in these release notes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../r-release-notes/release-notes-for-previous-releases.md" format="dita" scope="local"> Release notes for previous releases</a> </p> </td> 
   <td colname="col2"> <p>View information about new features and enhancements in previous releases of <span class="keyword"> Target Standard</span> and <span class="keyword"> Target Premium</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://wwwimages.adobe.com/content/dam/acom/en/marketing-cloud/testing-targeting/54658.en.target.capabilities.whats-new-fall-2016.pdf" format="pdf" scope="external"> What’s New in Adobe Target 2016</a> (PDF) </p> </td> 
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
