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

**Last Updated: April 5, 2019**

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

## [!DNL Target] Standard/Premium 19.4.2 (April 29, 2019) {#release-19-4-2-prerelease}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

 Feature / Enhancement | Description |
| --- | --- |
|[!UICONTROL Mobile Visual Experience Composer]|The [!UICONTROL Visual Experience Composer] (VEC) for Native Mobile Apps lets you create activities and personalize content on native mobile apps in a do-it-yourself fashion without continuous development dependencies and app-release cycles.|
|[!UICONTROL Visual Experience Composer]|The [!UICONTROL Visual Experience Composer] (VEC) includes the following enhancements to make your work quicker and more efficient:<ul><li>You can edit the style of an element, including the background image, in the VEC. (TGT-15001)</li><li>[!DNL Target] supports HTML5 using configurations on v4.5.1 or higher. (TGT-33618)</li>|

**Enhancement, fixes, and changes**

* We improved the workflow when you delete assets using the VEC. Deleted assets are now removed from the [!UICONTROL Offers library] and from [!DNL Scene7] (if applicable). Deleted assets no longer display in search results. (TGT-31981)
* We improved the rendering of image offers in the Assets picker. Displaying and selecting image offers is now quicker and more efficient. (TGT-32897)
* We improved the handling of redirects to URLs when you cancel loading of a page within the VEC. (TGT-33815)
* Toolbar icons display appropriately after you cancel loading of a page within the VEC. If specific actions cannot be performed until after the page is fully loaded, the associated toolbar icons are disabled. (TGT-33811)
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
