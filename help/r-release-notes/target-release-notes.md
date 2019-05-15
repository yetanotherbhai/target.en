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

**Last Updated: May 15, 2019**

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change. To view information about the current release, see [Target Release Notes](release-notes.md) in the [!DNL Target] documentation. Depending on the timing of releases, the information on these pages might differ.

## [!DNL Target] Standard/Premium 19.5.1 (May 21, 2019) {#release-19-5-1-prerelease}

This release includes the following features, changes, and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

### Feature updates

|Feature / Enhancement | Description |
| --- | --- |
|Single Page App Visual Experience Composer (SPA VEC)|The SPA VEC includes the following enhancements to make your work quicker and more efficient:<ul><li>Clicking an action in the SPA highlights the element on the site where this action will be applied. Each VEC action created under a View has four corresponding icons: Information, Edit, Move, and Delete. New "Move" functionality in this release lets you move the action to a Page Load Event or any other View that already exists in the modifications panel.</li><li>You can now cancel the loading of a website in the VEC to unblock editing of an activity. This enhancement is useful, for example, if you want to make a small edit to the activity, review its settings, or add custom code and you don't want to wait for the site to load. (TGT-33872)</li><li>You can perform many actions before the page loads in the VEC, or even if the page fails to load altogether (for example, custom code is no longer operational). Actions that cannot be edited before the site loads are disabled in the Target UI. (TGT-33851 & TGT-34149)</li></ul>|
|Automated Personalization (AP) & Auto-Target activities<br>![Premium badge](/help/assets/premium.png)|You can select an experience to be used as control while creating an AP or Auto-Target activity. This feauture lets you route the entire control traffic to a specific experience, based on the traffic allocation percentage configured in the activity. You can then evaluate the performance of the personalized deliveries against the control experience. (TGT-26572)|
|Recommendations<br>![Premium badge](/help/assets/premium.png)|You can use the Recommend Previously Purchased Items toggle while creating Recently Viewed Items logic. (TGT-34030)|

### Enhancement, fixes, and changes

* Toolbar icons display appropriately after you cancel loading of a page within the VEC. If specific actions cannot be performed until after the page is fully loaded, the associated toolbar icons are disabled. (TGT-33811)
* You can now list and navigate more easily through offer folders in the Asset picker instead of navigating through a flat folder hierarchy. (TGT-33725)

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
