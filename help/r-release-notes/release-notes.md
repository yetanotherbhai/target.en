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

## at.js version 2.1.0 (Date to be Announced)

We are thrilled to announce the following exciting features in at.js 2.1.0:

>[!NOTE]
>
>The exact date of the release of at.js 2.1.0 will be announced shortly, but we wanted to give you a sneak preview.

|Feature / Enhancement|Description|
| --- | --- |
|Adobe Opt-in Support|Adobe Opt-In is a way to simplify Adobe solutions integrations with consent management platforms.<br>For more information about Adobe Opt-in, see [Privacy and General Data Protection Regulation (GDPR)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md).|
|Industry Standard CSP Compliant|at.js no longer uses eval() to execute JavaScript.|
|Client Side Analytics Logging|Give customers full control on how they want to send analytics data to Adobe Analytics, whether on the client-side or server-side.<br>For more information, see [Client-side Analytics logging](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *Before you implement*.|
|Send Notifications|Allow developers to send notifications when an experience is rendered by their code instead of using `applyOffer()` or `applyOffers()`.<br>For more information, see [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md).|
|Reduced file size|The size of at.js is reduced by ~24%, which improves page load performance and reduces the time to download at.js on the page.|

## Mobile App Visual Experience Composer (May 14, 2019) {mobile-vec}

|Feature / Enhancement | Description |
| --- | --- |
|Mobile App Visual Experience Composer (VEC)|The Mobile App VEC lets you create activities and personalize content on native mobile apps in a do-it-yourself fashion without continuous development dependencies and app-release cycles.<br>For more information, see:<ul><li>[Mobile App Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android - set up the mobile app](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS - set up the mobile app](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Set up click tracking in the Mobile VEC](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li></ul>|

## [!DNL Target] Standard/Premium 19.4.2 (April 30, 2019) {#release-19-4-2}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

### Feature updates

|Feature / Enhancement | Description |
| --- | --- |
|[!UICONTROL Visual Experience Composer]|The [!UICONTROL Visual Experience Composer] (VEC) includes the following enhancements to make your work quicker and more efficient:<ul><li>The DOM path feature is now available when setting up click tracking.<br>For more information, see [click tracking](/help/c-activities/r-success-metrics/click-tracking.md#considerations).</li><li>Use the Styles panel to view or edit the value of existing styles for the selected element. You can also add additional styling.<br>To access the Styles panel, click a page element from within the VEC, then click [!UICONTROL Edit] > [!UICONTROL Styles].<br>The Styles panel displays on the right side of the VEC. The panel contains a list of styles that lets you edit or add to the selected element. A real-time CSS Editor lets you view changes and add styles if you are comfortable using Cascading Style Sheets (CSS) or if you receive code from your developer.<br>For more information, see [Styles](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) in *Visual Experience Composer Options*.</li><li>The Rich Text Editor now supports nested HTML5 elements.<br>HTML5 specifications allow new combinations of tags for nesting. The previous version of the rich text editor did not support new nesting of tags as allowed by the HTML5 specification. As a result, any nested elements selected in the VEC were not handled properly, which led to unwanted HTML changes. (TGT-33618)<br>For more information, see [Edit Text/HTML](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) in *Visual Experience Composer options*.</li>|

### Enhancement, fixes, and changes

* We improved the workflow when you delete assets using the VEC. Deleted assets are now removed from the [!UICONTROL Offers library] and from [!DNL Scene7] (if applicable). Deleted assets no longer display in search results. (TGT-31981)
* You can now delete asset folders even if they contain images (non-empty folders). (TGT-33265)

  Previously, you could not delete a non-empty folder from the Target image offers library ([!UICONTROL Offers] > [!UICONTROL Image Offers]). You would get a “Folder is not empty!" notification when trying to delete the folder from the UI.  With this feature, we are adding the capability to let you perform the folder deletion to remove an entire folder containing any number of assets and sub-folders inside. This feature is available in the Target UI as well in the Adobe Experience Cloud Assets UI.

  * Non-empty folders in the Image Offer library can be deleted. If all images within the folder are not referenced in any activity, the entire folder and its contents are deleted. If some images within the folder are referenced in any activity, all unreferenced images are deleted, but referenced images and folders containing those images are retained.
  * Rendering of image offers in the Image Asset picker is made faster and more efficient. 
  
  For more information, see [Work with content in the library](/help/c-experiences/c-manage-content/assets-working.md). (TGT-32897) 

* We improved the rendering of image offers in the Assets picker. Displaying and selecting image offers is now quicker and more efficient. (TGT-32897)
* We improved the handling of redirects to URLs when you cancel loading of a page within the VEC. (TGT-33815)
* After you select a [!UICONTROL Recommendations] collection from the Collections picker, you must now click the [!UICONTROL Save] button. This workflow is consistent with other workflows within [!DNL Target]. (TGT-33205)
* Fixed an issue that caused a small set of Insights reports to return 0% conversion rates instead of the actual conversion rates. (TNT-32125)

## [!DNL Target] Standard/Premium 19.4.1 (April 15, 2019) {#release-19-4-1}

This release is a maintenance release and includes the following change:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

* Updated the [!DNL Adobe Experience Cloud] UI to reflect branding and product changes. (TGT-33546, TGT-33272, and TGT-33331)

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