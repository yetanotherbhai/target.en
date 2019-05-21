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

## [!DNL Target] Standard/Premium 19.5.1 (May 21, 2019) {#tgt-19-5-1}

This release includes the following features, changes, and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

### Feature updates

|Feature / Enhancement | Description |
| --- | --- |
|Single Page App Visual Experience Composer (SPA VEC)|The SPA VEC includes the following enhancements to make your work quicker and more efficient:<ul><li>Clicking an action in the SPA highlights the element on the site where this action will be applied. Each VEC action created under a View has four corresponding icons: Information, Edit, Move, and Delete. New "Move" functionality in this release lets you move the action to a Page Load Event or any other View that already exists in the modifications panel. (TGT-33746)</li><li>You can perform many actions before the page loads in the VEC, or even if the page fails to load altogether (for example, custom code is no longer operational). Actions that cannot be edited before the site loads are disabled in the Target UI. (TGT-33851 & TGT-34149)</li></ul>For more information, see [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md).|

### Enhancement, fixes, and changes

* Toolbar icons display appropriately after you cancel loading of a page within the VEC. If specific actions cannot be performed until after the page is fully loaded, the associated toolbar icons are disabled. (TGT-33811)

## Mobile App Visual Experience Composer (May 14, 2019) {mobile-vec}

|Feature / Enhancement | Description |
| --- | --- |
|Mobile App Visual Experience Composer (VEC)|The Mobile App VEC lets you create activities and personalize content on native mobile apps in a do-it-yourself fashion without continuous development dependencies and app-release cycles.<br>For more information, see:<ul><li>[Mobile App Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android - set up the mobile app](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS - set up the mobile app](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Set up click tracking in the Mobile VEC](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li></ul>|

## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes {#section_1BC5F5208DA548E9B4344A0836E4B943}

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|Documentation changes|View detailed information about updates to this guide that might not be included in these release notes.<br>For more information, see [Documentation Changes](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C).|
|Release notes for previous releases|View information about new features and enhancements in previous releases of Target Standard and Target Premium.<br>For more information, see [Release notes for previous releases](../r-release-notes/release-notes-for-previous-releases.md).|
|Adobe Experience Cloud release notes|View the latest release notes for the Adobe Experience Cloud solutions.<br>For more information, see [Experience Cloud Release Notes](https://marketing.adobe.com/resources/help/en_US/whatsnew/).|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|Adobe Priority Product Update list|To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)|
|Upcoming release notes|For information about the current month's Target releases, including prerelease information, see the [Target Release Notes - Prerelease](/help/r-release-notes/target-release-notes.md) page.|