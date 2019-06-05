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

**Last Updated: May 28, 2019**

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change. To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same or it might differ, depending on the timing of releases.

## Target Standard/Premium 19.6.1 (June 25, 2019) {#tgt-19-6-1}

|Feature / Enhancement|Description|
| --- | --- |
|Visual Experience Composer (VEC)|When you click a page element in the VEC, a menu shows the options that are available for that element type. <ul><li>You can now use the [!DNL Styles > Background] option to change the background image and color for the selected element. (TGT-15001)</li><li>When you click an image then click [!DNL Replace With], two new options display: [!DNL HTML] and [Experience Fragment](/help/c-experiences/c-manage-content/aem-experience-fragments.md).<br> Replacing an image with HTML gives you full control of the element without needing to select the parent element to access the HTML option.<br>Experience fragments let you quickly insert elements created in Adobe Experience Manager (AEM) in Target activiites. (TGT-34097)</li><li>We have improved the process for configuring click tracking within the VEC and the Single Page Application VEC.<br>While selecting elements to use in click tracking, the names of all available elements display in the Modifications panel on the right side, making it quick and easy to select the desired elements.<br>The [!DNL Goals & Settings] page of the three-part guided activity workflow displays a number representing the number of elements selected for click tracking. You can hover over this number to see the names of all selected elements. (TGT-33878) </li></ul>|
|Single Page App (SPA) Visual Experience Composer (VEC)|<ul><li>A new guided workflow helps you understand how page-delivery-rule settings should be configured to execute and run an activity successfully for your Single Page App. (TGT-33718)</li><li>You can now define a modification using the SPA VEC and then clone that modification for use in other views in your Single Page App. (TGT-33882)</li></ul>|
|Mobile Visual Experience Composer (VEC)|<ul><li>You can now author activities for multiple versions of your mobile app. This saves you time and effort when the versions are very similar and you don't need to significantly change the app's UI. (TGT-34231)</li></ul>|
|![Premium badge](/help/assets/premium.png)<br>Automated Personalization (AP) and Auto-Target activities: experience as control|<ul><li>You can select an experience to be used as control while creating an AP or Auto-Target activity. This feauture lets you route the entire control traffic to a specific experience, based on the traffic allocation percentage configured in the activity. You can then evaluate the performance of the personalized deliveries against the control experience. (TGT-32801 & TGT-26572)</li></ul>|

### Enhancement, fixes, and changes

* The `<BODY>` tag now displays in the DOM path that displays at the bottom of the VEC when you click an element on the page, letting you perform actions on the `<BODY>` tag. (TGT-33736)

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
