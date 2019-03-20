---
description: You can display profile values and campaign information directly in an HTML or Flash Offer.
keywords: dynamic data;assets;data;offers
seo-description: You can display profile values and campaign information directly in an HTML or Flash Offer.
seo-title: Pass dynamic data into offers
solution: Target
title: Pass dynamic data into offers
topic: Premium
uuid: 1910a7f5-e4bd-413a-9875-e0b005407f50
---

# Pass dynamic data into offers{#pass-dynamic-data-into-offers}

You can display profile values and campaign information directly in an HTML or Flash Offer.

 **Business Case**

A visitor arrives on your landing page with `keyword=world` `cup`. You display the term *World cup* in the offer.

**Technical Advantages**

Because it is stored in the user profile, you can repeat this message on his next visits. Just one offer or campaign can manage these custom messages for all your visitors. As the visitor's intent changes your website content automatically reflects those changes.

**Example**

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");` 

* HTML Offer code: `Get your ${profile.keyword} information here!` 
* User sees: Get your World Cup information here!

The following values can be "token replaced":

| Values | Examples |
|--- |--- |
|In-mbox profile parameters|`${profile.age}`|
|Script profile parameters|`${user.lifetimeSpend}`|
|Mbox parameters|`${mbox.favoriteColor}`|
|Campaign information|`${campaign.name}`, `${campaign.recipe.name}`, `${campaign.id}`, `${campaign.recipe.id}`, and `${campaign.recipe.trafficType}`|
|Unique visitor id|`${user. pcId}`|
|Unique session id|`${user.sessionId}`|
|Visitor's first session (true or false)|`${user.isFirstSession}`|

**Tip:** This information can be useful for debugging.

**Implementation**

For profile parameters passed into an mbox, use the syntax: `${profile.parameter}` For profile parameters created in a script, use the syntax:

`${user.parameter}`

These variables are replaced with the value on the server side, so no quotes or other JavaScript is required for the proper display.

Default values can also be specified for values you wish to expose to offers. The syntax is like this:

`${user.testAttribute default="All Items!"}`

When `testAttribute` doesn’t exist or is blank, "All Items!" will be written out. If an empty attribute value is valid, and you want to write it out instead of showing the default, you can use:

`${user.testAttribute default="All Items!" show_blank="true"}`

You can also escape and unescape values to be displayed. If your value has an apostrophe for example, you would want to escape the value so it does not break the JavaScript on the page. (Offers are written in JavaScript, so a single apostrophe can be confused for a quote.) For example:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`

>[!NOTE]
>
>Please work with your representative to use this feature.

