---
description: Several steps are required when implementing Adobe Analytics as the reporting source for Target (A4T).
keywords: A4T;Adobe Analytics;Analytics-based activity;Analytics report suite;report suite;Analytics Target integration;configure report suite
seo-description: Several steps are required when implementing Adobe Analytics as the reporting source for Target (A4T).
seo-title: Analytics for Target implementation
solution: Target
title: Analytics for Target implementation
topic: Premium
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
---

# Analytics for Target implementation{#analytics-for-target-implementation}

Several steps are required when implementing Adobe Analytics as the reporting source for Target (A4T).

## Implementation Steps {#section_73961BAD5BB4430A95E073DE5C026277}

The following table describes the steps required to deploy this integration to your site. 

## Step 1: Request provisioning for Analytics and Target

After you implement Analytics as the reporting source for Target, you must be provisioned for Analytics and Target. [Use this form to request to be provisioned](http://www.adobe.com/go/audiences).

## Step 2: Set up user permissions

User account requirements must be met before you can create an Adobe Analytics-based activity in Adobe Target. See [User permission requirements](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Step 3: Implement the Experience Cloud Visitor ID service

The visitor ID service lets you identify users across Experience Cloud solutions. You must implement or migrate to the required version of the Experience Cloud Visitor ID. For more information, see "Implementation Requirements" in [Before you implement](/help/c-integrating-target-with-mac/a4t/before-implement.md).

See [Implement the Experience Cloud ID Service for Target](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-target.html) in the Experience Cloud Visitor ID Service documentation.

## Step 4: Update AppMeasurement for JavaScript or s_code

You must implement or migrate to the required version of appMeasurement.js. For more information, see "Implementation Requirements" in [Before you implement](/help/c-integrating-target-with-mac/a4t/before-implement.md).

For new implementations, see [Analytics JavaScript Implementation](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html).

For a migration, see [Migrating to AppMeasurement for JavaScript](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=appmeasure_mjs_migrate).

## Step 5: Download and update at.js or mbox.js

You must implement or migrate to the required version of at.js or mbox.js using your production account. No modifications are required on the code.

For more information, see "Implementation Requirements" in [Before you implement](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Step 6: Host at.js or mbox.js

If you previously deployed at.js or mbox.js, you can replace your existing file with the updated version. For more information, see "Implementation Requirements" in [Before you implement](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Otherwise, this file can be hosted along with the Visitor ID service and AppMeasurement for JavaScript files. These files must be hosted on a web server that is accessible to all pages on your site. You need the path to these files in the next step.

## Step 7: Reference at.js or mbox.js on all site pages

Include at.js or mbox.js below VisitorAPI.js by adding the following line of code in the <head> tag on each page:

For at.js:

```
<script language="JavaScript" type="text/javascript" 
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

For mbox.js:

```
<script language="JavaScript" type="text/javascript" 
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/mbox.js"></script>
```

It is essential that VisitorAPI.js is loaded before at.js or mbox.js, so if you are updating an existing at.js or mbox.js file, make sure that you verify the load order.

## Step 8: Validate the implementation

Load your pages after you have updated the JavaScript libraries to confirm that the mboxMCSDID parameter values in Target calls match the sdid parameter value in the Analytics page-view call.

This is especially important to confirm in Single Page Applications (SPAs) where the order of calls is not always predictable.

**Note:** The matching of these values is required in order for A4T to function correctly.

## Step 9: (Optional) Remove previous integration code

We recommend that you remove the previous integration to simplify your implementation and eliminate the need to sort out discrepancies between the systems. You can remove any code you might have deployed for a previous SC to T&T integration, including `mboxLoadSCPlugin`.

## Step 10: Enable the options for using Analytics as the reporting source for Target

In Target, click [!UICONTROL Setup > Preferences] and choose either [!UICONTROL Select per activity] or [!UICONTROL Adobe Analytics] to enable the options.

* Select per activity lets you choose between Target and Analytics when creating each activity.
* Adobe Analytics sets Analytics as the reporting source for all activities that you create.

