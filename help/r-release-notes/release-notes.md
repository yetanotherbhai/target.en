---
description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
keywords: Release notes;prerelease
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for each Adobe Target Standard and Target Premium release.
seo-title: Target release notes (current)
solution: Target
title: Target release notes (current)
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
---

# Target release notes (current){#target-release-notes-current}

These release notes provide information about features, enhancements, and fixes for each Target Standard and Target Premium release.

## Announcements

Be aware of the following important announcements:

* On February 20, 2019, the Adobe Target infrastructure was upgraded in the EMEA, Japan, and APAC regions to no longer collect data from end users with older devices or web browsers that do not support TLS 1.1 or later. This same upgrade is planned for the North America region for **April 1, 2019**. Migrating to TLS 1.2 provides improved security. It is important that you go through the specifics and plan out the changes with your IT team for a smooth transition. For more information, see [TLS (Transport Layer Security) encryption changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target] and the [!DNL Adobe Marketing Cloud] will drop support for Microsoft Internet Explorer 11 starting in March 2019. This change affects [!DNL Target] authoring only; this change does not affect experience delivery. Please switch to Microsoft Edge or another browser. For more information, see [Supported browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).
* The [Adobe Target product documentation](https://docs.adobe.com/content/help/en/target/using/target-home.html) has moved to a new domain: `docs.adobe.com`. The documentation can be found at the following URL: `https://docs.adobe.com/content/help/en/target/using/target-home.html`. Please update your bookmarks accordingly.

## at.js version 2.0.1 (March 19, 2019) {#atjs201}

This is a maintenance release and includes the following enhancements and fixes:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

* Fixed a race condition in the DOM polling code that caused JavaScript exceptions for certain customers. (TNT-31869)
* Notifications that views were rendered have been decoupled from click-tracking event handlers. Initially, Target did not send notifications if click-event handlers belonging to a rendered view could not be attached. Target now sends a view notification even when click elements are not found. (TNT-31969)
* Fixed an issue that caused the request-succeeded event redirect flag to always be set to true. (TNT-31907)
* Fixed an issue that caused the VEC rearrange action to be logged as success, even when elements were missing. (TNT-31924)
* Fixed an issue that caused notifications for certain customers to not contain the Enterprise Permissions property token. (TNT-31999)

>[!NOTE]
>
>If you require Adobe Opt-in support for the General Data Protection Regulation (GDPR), you should implement at.js 1.7.1. Opt-in support is not currently supported in at.js 2.*x*.

## at.js version 1.7.1 (March 19, 2019) {#atjs171}

This is a maintenance release and includes the following fix:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

* Fixed a race condition in the DOM polling code that caused JavaScript exceptions for certain customers. (TNT-31869)

## [!DNL Target] Standard/Premium 19.2.1 (February 19, 2019) {#release-19-2-1}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

| Feature / Enhancement | Description |
| --- | --- |
|Single Page App Visual Experience Composer|The Visual Experience Composer (VEC) for Single Page Apps (SPAs) lets marketers create tests and personalize content on SPAs in a do-it-yourself fashion without continuous development dependencies. The VEC can be used to create activities on most popular frameworks, such as React and Angular. (TGT-27916)<br>For more information, see [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md) and [Single Page Application integration](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).<br>In addition to the above article, there are many topics related to SPAs and at.js that address this feature and how to implement it. For more information see [Documentation changes](/help/r-release-notes/doc-change.md).|
|Visual Experience Composer|The Visual Experience Composer (VEC) includes the following enhancements to make your work quicker and more efficient:<ul><li>You can now use the Insert Before and Insert After options in the VEC while inserting [AEM experience fragments](/help/c-experiences/c-manage-content/aem-experience-fragments.md). See [Visual Experience Composer options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md). (TGT-32385)</li><li>The [!DNL Adobe Target] VEC Helper browser extension for Google Chrome lets you load websites reliably within the VEC to rapidly author and QA web experiences. See [Visual Experience Composer helper extension](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). (TGT-32746)</li></ul>|
|![Premium badge](/help/assets/premium.png)<br>Recommendations in [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] activities|You can now include recommendations inside [!UICONTROL A/B Test] (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) and [!UICONTROL Experience Targeting] (XT) activities. This opens up entirely new capabilities, such as:<ul><li>Test and target recommendations and non-recommendations content within the same activity.</li><li>Easily experiment with placement of recommendations on the page, including the order of multiple recommendations.</li><li>Automatically push traffic to the best-performing recommendations experience using [!UICONTROL Auto-Allocate].</li><li>Dynamically assign visitors to tailored recommendations experiences based on their individual profiles using [!UICONTROL Auto-Target].</li></ul>To get started, create an [!UICONTROL A/B Test] or [!UICONTROL Experience Targeting] activity using the VEC and use the [!UICONTROL Insert Before], [!UICONTROL Insert After], or [!UICONTROL Replace With] action to add recommendations to an experience. (RECS-6166)<br>For more information, see [Recommendations as an offer](/help/c-recommendations/recommendations-as-an-offer.md).|
|![Premium badge](/help/assets/premium.png)<br>Enterprise Permissions support in Target APIs|[Adobe Target Admin APIs](http://developers.adobetarget.com/api/#admin-apis) will now take full advantage of the same Enterprise Permissions capabilities found in the Target UI. Starting **Feb 21, 2019**, system administrators can programmatically access report data as well as create and manage activities, offers, and audiences within any workspace. These actions were previously limited to the default workspace only. Support for Automated Personalization (AP) activities will come in a future release.<br>**Note:** There is a [known issue](/help/r-release-notes/known-issues-resolved-issues.md#api) regarding this functionality.|

**Enhancement, fixes, and changes**

* To improve security, [!DNL Target] now prevents accessing Amazon Web Services (AWS) metadata endpoints while loading the VEC. (TGT-33129)

## Release Notes for Other Adobe Target Capabilities {#section_9EB425262A1947D18953F98CF3D4EE71}

Use the following links to view release notes for Target capabilities other than Target Standard and Target Premium:

* [Recommendations Classic release notes](../assets/adobe-recommendations-classic.pdf) 
* [Search&Promote release notes](https://marketing.adobe.com/resources/help/en_US/snp/c_searchpromote_release_notes.html)

## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes {#section_1BC5F5208DA548E9B4344A0836E4B943}

In addition to the notes for each release, the following resources provide additional information:

### Documentation changes

For more information, see [Documentation Changes](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)

View detailed information about updates to this guide that might not be included in these release notes.

### Release notes for previous releases

For more information, see [Release notes for previous releases](../r-release-notes/release-notes-for-previous-releases.md)

View information about new features and enhancements in previous releases of Target Standard and Target Premium.

### Adobe Experience Cloud release notes

For more information, see [Experience Cloud Release Notes](https://marketing.adobe.com/resources/help/en_US/whatsnew/)

View the latest release notes for the Adobe Experience Cloud solutions.

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

### Adobe Priority Product Update list

To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)

### Current and upcoming release notes

For information about the current month's Target releases, including prerelease information, see the [Target Release Notes - Prerelease](/help/r-release-notes/target-release-notes.md) page.