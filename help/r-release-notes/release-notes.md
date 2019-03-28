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

## [!DNL Target] Standard/Premium 19.3.1 (March 29, 2019) {#release-19-3-1-current}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

| Feature / Enhancement | Description |
| --- | --- |
|Visual Experience Composer|The Visual Experience Composer (VEC) includes the following enhancements to make your work quicker and more efficient:<ul><li>You can now cancel the loading of a website in the VEC to unblock editing of an activity. This enhancement is useful, for example, if you want to make a small edit to the activity, review its settings, or add custom code and you don't want to wait for the site to load. (TGT-31288)<br>See [Cancel loading of a page within the VEC](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#cancel-loading).</li><li>You can perform many actions before the page loads in the VEC, or even if the page fails to load altogether (for example, custom code is no longer operational). Actions that cannot be edited before the site loads are disabled in the Target UI. (TGT-31288, TGT-31611, and TGT-32602)<br>See [Edit a page while the page is loading or after the page fails to load](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#loading).</li><li>The VEC displays the DOM path so you can easily select the proper element while creating or editing experiences. (TGT-13422)<br>See [Navigate elements using the DOM path](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path).</li></ul>|

**Enhancement, fixes, and changes**

* You are now instructed to re-authenticate when your session expires while reviewing a report. After you log in again, you are directed back to the report. (TGT-32723)

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