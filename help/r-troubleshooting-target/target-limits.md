---
description: Information about the character limits and other limits (offer size, audiences, profiles, values, parameters, etc.) that affect activities and other elements in Adobe Target.
keywords: character limit;mbox parameters;batch delivery api;profile parameters;limits;built in profiles;maximum;limit;constraint;character;best practice;orderid;orderTotal;mbox3rdPartyID;category;categoryID
seo-description: Information about the character limits and other limits (offer size, audiences, profiles, values, parameters, etc.) that affect activities and other elements in Adobe Target.
seo-title: Limits
solution: Target
title: Limits
topic: Standard
uuid: 603fb800-a26c-43ec-b2d9-ef7a8ed8721e
---

# Limits{#limits}

Information about the character limits and other limits (offer size, audiences, profiles, values, parameters, etc.) that affect activities and other elements in Adobe Target.

 The limits listed below are recommended limits. When these limits are approached or exceeded, performance can slow. Slow interface load times can also be caused by a very complex activity, such as many audiences, targets, and experiences all in one activity. 
 
 Highly complex activities should be reviewed with Adobe Consulting and tested in a limited environment before being released to production.

| Feature | Limit | Comments |
|--- |--- |--- |
|Audience Names|256 characters|Values longer than 256 characters are truncated.|
|Customer Attribute Name|128 characters||
|Mbox Name|250 characters||
|Mbox Request URLs|2,083 characters|Due to URL length restrictions in Internet Explorer.|
|Activity Names|250 characters||
|Experience Names|20 characters||
|Offer Names|250 characters||
|Offer Size|256 KB for HTML offers  64 KB for visual offers from the UI  512 KB from the API|If using a global mbox, the limit is for the whole set of content returned for the page. Limiting offer size improves page load times. If the limit is exceeded, the following message appears:<br>"The content for the experience is too large to deliver. Please modify the experience to affect less page code."|
|Reusable Audiences/Account|75 audiences|Recommended limit. JavaScript timeouts occur in the interface if you have too many.|
|In-Mbox Profile Names|128 characters||
|In-Mbox Profiles in an mbox request|50 profiles|All profiles after 50 are ignored.|
|In-Mbox Profile Attribute Value|256 characters|Values longer than this get truncated.|
|Script Profile Names|50 characters||
|Script Profile Value|256 characters (Recommended)|The recommended size is 256 characters for the return value of script profiles. This value is stored in the user profile, along with other profile attributes and information about visited experiences. If the profile gets larger than 64K, it is truncated by removing the oldest attributes until the profile is below 64K again.|
|Script Profile input box in the Target UI|1,300 characters||
|Target Names|50 characters||
|Target input box in the Target UI|2,000 characters|Recommended limit. Depends on the size of the encoded string, which could be much longer than the raw string. If the string is too large, it fails before it gets to Adobe Target.|
|Target Conditions|1,000 values|Recommended limit. This refers to the number of line-separated values in the targeting text area. For example, entering 1,000 zip codes into a zip code target.|
|productPurchasedId parameter|47 characters per comma-separated value|Anything longer is clipped by the system.|
|orderId parameter|120 characters|Recommended limit.|
|orderTotal parameter|120 characters|Recommended limit.|
|mbox3rdPartyId parameter|60 characters||
|categoryId parameter|250 characters||
|entityID parameter|1,000 characters||
|MBox Parameters|<ul><li>mbox Parameters: 500 parameters per mbox</li><li>Profile Parameters: 500</li><li>profile parameters per mbox</li><li>Other Parameters (URL, referring URL, etc.): 50 per mbox for each other parameter type</li></ul>|For parameters that get logged in the Target database, the limits in the column to the left are for standard mbox requests. These limits apply unless the request is shortened due to web browser limitations.<br>If you are using the [Batch Delivery API](https://developers.adobetarget.com/api/#server-side-batch-delivery) in the Mobile Services SDK, the limit of 50 mbox parameters, 50 profile parameters, and 50 for other parameter types are limitations of the API itself. It is not possible to send a request containing more that these numbers using the Batch Delivery API. If a request contains more than these limits, the API will return the following error message:<br>"The number of mboxParameters cannot exceed 100."|