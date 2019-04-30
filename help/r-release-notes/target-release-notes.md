---
description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
keywords: release notes
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Adobe Target releases
seo-title: Target release notes (prerelease)
solution: Target
title: Target release notes (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

These release notes provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.

**Last Updated: April 30, 2019**

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change. To view information about the current release, see [Target Release Notes](release-notes.md) in the [!DNL Target] documentation. Depending on the timing of releases, the information on these pages might differ.

## Announcements

Be aware of the following important announcements:

* On February 20, 2019, the Adobe Target infrastructure was upgraded in the EMEA, Japan, and APAC regions to no longer collect data from end users with older devices or web browsers that do not support TLS 1.1 or later. This same upgrade is planned for the North America region for **April 1, 2019**. Migrating to TLS 1.2 provides improved security. It is important that you go through the specifics and plan out the changes with your IT team for a smooth transition. For more information, see [TLS (Transport Layer Security) encryption changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target] and the [!DNL Adobe Marketing Cloud] will drop support for Microsoft Internet Explorer 11 starting in March 2019. This change affects [!DNL Target] authoring only; this change does not affect experience delivery. Please switch to Microsoft Edge or another browser. For more information, see [Supported browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## [!DNL Target] Standard/Premium 19.4.1 (April 15, 2019) {#release-19-4-1-prerelease}

This release is a maintenance release and includes the following change:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

* Updated the [!DNL Adobe Experience Cloud] UI to reflect branding and product changes. (TGT-33546, TGT-33272, and TGT-33331)

## [!DNL Target] Standard/Premium 19.4.2 (April 30, 2019) {#release-19-4-2-prerelease}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

|Feature / Enhancement | Description |
| --- | --- |
|[!UICONTROL Visual Experience Composer]|The [!UICONTROL Visual Experience Composer] (VEC) includes the following enhancements to make your work quicker and more efficient:<ul><li>The DOM path feature is now available when setting up [click tracking](/help/c-activities/r-success-metrics/click-tracking.md). For more information, see [Navigate elements using the DOM path](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Visual Experience Composer options*.</li><li>You can edit the style of an element, including the background image, in the VEC. For more information, see [Styles](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) in *Visual Experience Composer Options*. (TGT-15001)</li><li>The Rich Text Editor now supports nested HTML5 elements.<br>HTML5 specifications allow new combinations of tags for nesting. The previous version of the rich text editor did not support new nesting of tags as allowed by the HTML5 specification. As a result, any nested elements selected in the VEC were not handled properly, which led to unwanted HTML changes. (TGT-33618)<br>For more information, see [Edit Text/HTML](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) in *Visual Experience Composer options*.</li>|

**Enhancement, fixes, and changes**

* We improved the workflow when you delete assets using the VEC. Deleted assets are now removed from the [!UICONTROL Offers library] and from [!DNL Scene7] (if applicable). Deleted assets no longer display in search results. (TGT-31981)
* You can now delete asset folders even if they contain images (non-empty folders). (TGT-33265)

  Previously, you could not delete a non-empty folder from the Target image offers library. You would get a “Folder is not empty!" notification when trying to delete the folder from the UI.  With this feature, we are adding the capability to let you perform the folder deletion to remove an entire folder containing any number of assets and sub-folders inside. This feature is available in the Target UI as well in the Adobe Experience Cloud Assets UI.

  Consider the following:

  * When deleting a folder, some stale references can take time to delete from the database. You might see some folders displayed in the UI that take several minutes to delete (approximately 10 minutes for 2,000 assets). The deletion process is being performed behind the scenes. Check back later to verify the deletion.
  * If the request takes too long, it might get timed out in the browser. This can lead to showing an error notification in the UI. For now, ignore the error message and visit the asset folder after a while (same as above).
  * If there are blank folders remaining that contain assets, try deleting the folder again after a while (same as above).

* We improved the rendering of image offers in the Assets picker. Displaying and selecting image offers is now quicker and more efficient. (TGT-32897)
* We improved the handling of redirects to URLs when you cancel loading of a page within the VEC. (TGT-33815)
* After you select a [!UICONTROL Recommendations] collection from the Collections picker, you must now click the [!UICONTROL Save] button. This workflow is consistent with other workflows within [!DNL Target]. (TGT-33205)
* Fixed an issue that caused a small set of Insights reports to return 0% conversion rates instead of the actual conversion rates. (TNT-32125)

## Product documentation for [!DNL Target] capabilities {#section_F03C61D438814538967B2BF901130BE4}

Use the following links to view product documentation for [!DNL Target] capabilities:

* [Adobe Target Learn &amp; Support](https://helpx.adobe.com/support/target.html) 
* [Recommendations Classic release notes](../assets/adobe-recommendations-classic.pdf) 
* [Search&Promote help](https://marketing.adobe.com/resources/help/en_US/snp/)

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
