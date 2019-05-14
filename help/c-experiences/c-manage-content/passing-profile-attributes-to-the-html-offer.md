---
description: You can display profile values and activity information directly in an HTML or JSON Offer.
keywords: dynamic data;assets;data;offers;personalized offers;personal offers;token replace
seo-description: You can display profile values and activity information directly in an HTML or JSON Offer.
seo-title: Pass dynamic data into offers
solution: Target
title: Pass dynamic data into offers
topic: Premium
uuid: 1910a7f5-e4bd-413a-9875-e0b005407f50
---

# Pass dynamic data into offers{#pass-dynamic-data-into-offers}

You can dyanimcally display visitor information that is stored in the Target profile. Similarly, Activity information (such as the name of the Activity or the name of the Experience) can also be used to create a single offer that dynamically returns personalized content based on the visitors interests, past behavior, and overall profile.

 **Business Cases**

* Promote a discounted offer to "refill" or "replenish" the last product purchased. Instead of creating a separate offer for every item in your catalog, you can create an offer with dynamic text that reads the "last product purchased" from the profile and displays a link in the offer.
* A visitor arrives on your landing page with `keyword=world` `cup`. You display the term *World cup* in the offer.
* Personlize a recommendations label with info such as (1) the last item added to a visitor's cart (Nike Air Max 1000s), (2) the visitor's color preference (black) and (3) the visitor's favorite non-shoe category (hoodies). Example: "Accessorize your 'Nike Air Max 1000s' with these cool 'black' 'hoodies'! 


**Technical Advantages**

Because user-specific preferences, behaviors, status, etc. can stored in the user's profile, you can repeat this message on his or her next visits. Dyanmic offers enable greater scale by allowing you to setup a single offer within an Activity that displays personalized messages for all your visitors. As the visitor's intent changes, your website content automatically reflects those changes.

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
|Unique visitor id|`${user.pcId}`|
|Unique session id|`${user.sessionId}`|
|Visitor's first session (true or false)|`${user.isFirstSession}`|
|Past behavior| `{$user.endpoint.lastPurchasedEntity}`, `{$user.endpoint.lastViewedEntity}`, `{$user.endpoint.mostViewedEntity}`, `{$user.endpoint.categoryAffinity}` 

**Tip:** This information can also be useful for debugging.
Log information in the console for debugging purposes, such as `${campaign.name}`, `${campaign.id}`, `${campaign.recipe.name}`, `${campaign.recipe.id}`, `${offer.name}`, `${offer.id}`, `${campaign.name}`

For Recommendations Designs, see additional examples here: [https://docs.adobe.com/content/help/en/target/using/recommendations/recommendations-design/design-overview.html](https://docs.adobe.com/content/help/en/target/using/recommendations/recommendations-design/design-overview.html)

**Implementation**

For profile parameters passed into an mbox, use the syntax: `${profile.parameter}` For profile parameters created in a profile script, use the syntax:

`${user.parameter}`

When using dyanamic attributes in a Recommendations Design, you must insert a backslash ('\') before the dollar sign ('$') in order for the dynamic value to render properly: `\${user.endpoint.lastViewedEntity}`

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
>Please work with your consulting representative for advanced uses of this feature.

