---
description: The Visual Experience Composer (VEC) for Single Page Apps (SPAs) enables marketers to create tests and personalize content on SPAs in a do-it-yourself fashion without continuous development dependencies. The VEC can be used to create activities on most popular frameworks, such as React and Angular.
keywords: spa vec;react;angular;react.js;spa visual experience composer;spa experience composer options;single page apps;single-page-app;spa;mobile experience options;target view
seo-description: The Visual Experience Composer (VEC) for Single Page Apps (SPAs) enables marketers to create tests and personalize content on SPAs in a do-it-yourself fashion without continuous development dependencies. The VEC can be used to create activities on most popular frameworks, such as React and Angular.
seo-title: Single Page App (SPA) Visual Experience Composer
solution: Target
title: Single Page App (SPA) Visual Experience Composer
topic: Standard
uuid: 4dcd6d9c-b2e3-4759-a2e0-3696c572faba
---

# Single Page App (SPA) Visual Experience Composer{#single-page-app-spa-visual-experience-composer}

In [!DNL Adobe Target], the [!UICONTROL Visual Experience Composer] (VEC) gives marketers a do-it-yourself capability to create activities and personalize experiences that can be dynamically delivered on traditional Multi Page Applications via Adobe Target's global mbox. However, this relies on retrieving offers on page load or subsequent server calls, which introduce latency as shown in the diagram below. This approach does not work well with SPAs as it degrades user experience and application performance.

![Traditional lifecycle vs. SPA lifecycle](/help/c-experiences/assets/trad-vs-spa.png)

With the newest release, we now introduce the Visual Experience Composer (VEC) for Single Page Apps (SPAs). The Visual Experience Composer (VEC) for Single Page Apps (SPAs) enables marketers to create tests and personalize content on SPAs in a do-it-yourself fashion without continuous development dependencies. The VEC can be used to create [A/B Test](/help/c-activities/t-test-ab/test-ab.md) and [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md) (XT) activities on popular frameworks, such as React and Angular.

## Adobe Target Views and Single Page Applications

The Adobe Target VEC for SPAs takes advantage of a new concept called Views: a logical group of visual elements that together make up an SPA experience. A SPA can, therefore, be considered as transitioning through views, instead of URLs, based on user interactions. A View can typically represent a whole site, or grouped visual elements within a site.

To explain further about what Views are, let’s navigate this fake online e-commerce site implemented in React called AShop and explore some example Views.

**Home Site**: `http://www.adobeshop.com/home`

![home site](/help/c-experiences/assets/home.png)

When we navigate to the home site of the AShop, we can immediately see a hero image that promotes an Easter sale as well as the newest products that AShop is selling on its site. In this case, a View can be defined as the entire home site. We can name this View as home just like the path name in `www.adobshop.com/home`. This is handy to note as we will expand on this more in the Implementing Adobe Target Views section below.

**Product Site**: `http://www.adobeshop.com/products`

![product site](/help/c-experiences/assets/product-site.png)

As we become more interested in the products that AShop is selling, we decide to click the Products link. Similar to the home site, the entirety of the products site can be defined as a View. We can name this View as products just like the path name in `www.adobshop.com/products`.

![product site 2](/help/c-experiences/assets/product-site-2.png)

In the beginning of this section, we defined Views as the whole site or even a group of visual elements on the site. As shown above, the four products shown on the site can also be grouped and considered as a View. If we wanted to name this View, we can name it to be Products.

![product site 3](/help/c-experiences/assets/product-site-3.png)

We decide to click on the Load More button to explore more products on the site. The website URL does not change in this case. But a View here can represent only the second row of products shown above. The View name can be called PRODUCTS-PAGE-2.

**Checkout**: `http://www.adobeshop.com/checkout`

![check-out page](/help/c-experiences/assets/checkout.png)

Because we liked some products shown in AShop, we decided to buy a couple. Now, on the checkout site we are given some options to choose normal delivery or express delivery. Because a View can be any group of visual elements on a site, we can name this View Delivery Preferences. 

Furthermore, the Views concept can be extended much further than this. If AShop wants to personalize content on the site depending on which delivery preference is selected, a View can be created for each delivery preference. In this case, when we select Normal Delivery, the View can be named Normal Delivery. If Express Delivery is selected, the View can be named Express Delivery. 

Now, AShop may want to run an A/B Test to see whether changing the color from blue to red when Express Delivery is selected can boost conversions as opposed to keeping the button color blue for both delivery options. 

## Implementing Adobe Target Views

Now that we have covered what Adobe Target Views are, we can leverage this concept in Target to empower marketers to run A/B and XT tests on Single Page Applications via the Visual Experience Composer. This will require a one-time developer setup. Let’s go through the steps to set this up.

1. Install at.js 2.0.

   First, we need to install at.js 2.0. The newest version of at.js 2.0 was developed with Single Page Applications in mind. Previous versions of at.js and mbox.js do not support Adobe Target Views and the VEC for SPA.

   ![Implementations Details dialog box](/help/c-experiences/assets/implement-atjs-2.png)

   Download the at.js 2.0 via the Adobe Target UI located in [!UICONTROL Setup > Implementation]. at.js 2.0 can also be deployed via Adobe Launch. However, the Adobe Target Extensions are not up to date and supported.

1. Implement at.js 2.0’s newest function, `triggerView()` on your sites.

   After defining the Views of your SPA where you want to run an A/B or XT test, implement at.js 2.0’s `triggerView()` function with the Views passed in as a parameter. This allows marketers to use the VEC to design and run the A/B and XT tests for those Views defined. If the `triggerView()` function is not defined for those Views, the VEC will not detect the Views and thus marketers cannot use the VEC to design and run A/B and XT tests.

   adobe.target.triggerView(viewName, options)

   |Parameter|Type|Required?|Validation|Description|
   | --- | --- | --- | --- | --- |
   |viewName|String|Yes|1. No trailing spaces<br>2. Cannot be empty<br>3. View name should be unique for all pages.<br>4. Warning: View name should not start or end with '`/`'. This is because the customer would generally extract view name from URL path and for us "home" and "`/home`" are different.<br>5. Warning: Same view should not be consecutively triggered multiple times with the  `{page: true}` option.|Pass in any name as a string type that you want to represent your View. This View name displays in the [!UICONTROL Modifications] panel of the VEC for marketers to create actions and run their A/B and XT activities.|
   |options|Object|No|||
   |options > page|Boolean|No||**TRUE**: Default value of page is true. When `page=true`, notifications will be sent to the Edge servers for incrementing impression count.<br>**FALSE**: When `page=false`, notifications will not be sent for incrementing impression count. This should be used when you want to only re-render a component on a page with an offer.|

   Now let’s go through some example use cases on how to invoke the `triggerView()` function in React for our hypothetical AShop e-commerce SPA:

   **Home Site**: `http://www.adobeshop.com/home`

   ![home-react-1](/help/c-experiences/assets/react1.png)

   ![home-react-2](/help/c-experiences/assets/react2.png)

   ![home-react-3](/help/c-experiences/assets/react3.png)

   As AShop marketers, if we want to run A/B tests on the whole home site, then we might want to name the view as home that can be extracted from the URL:

   `[Insert Code Here]`

   **Products Site**: `http://www.adobeshop.com/products`

   Now, let’s look at an example that is a little bit more complicated. Let’s say as AShop marketers, we would like to personalize the second row of the products by changing the price label color to red after a user clicked on the Load More button.

   ![react products](/help/c-experiences/assets/react4.png)

   `[Insert Code Here]`

   **Checkout**: `http://www.adobeshop.com/checkout`

   ![react checkout](/Checkout: http://www.adobeshop.com/checkout)

   ![react checkout](/help/c-experiences/assets/react6.png)

   If AShop wants to personalize content on the site depending on which delivery preference is selected, a View can be created for each delivery preference. In this case, when we select Normal Delivery, the View can be named as Normal Delivery. If Express Delivery is selected, the View can be named as Express Delivery. 

   Now, AShop might want to run an A/B test to see whether changing the color from blue to red when Express Delivery is selected can boost conversions as opposed to keeping the button color blue for both delivery options.  

   `[INSERT CODE HERE]`

1. Launch A/B or XT activities via the VEC.

   When `adobe.target.triggerView()` is implemented on your SPA with view names passed in as parameters, the VEC will be able to detect these views and allow users to create actions and modifications for their A/B or XT activities.

   Now, there are two major improvements to the [!UICONTROL Modification] panel and Actions for the VEC that allow the VEC to work well with SPA.

   **Modifications Panel**

   The [!UICONTROL Modifications] panel, as shown below, captures the actions created for a particular view. Notice that all actions for a View are grouped under that View.

   **Actions** 

   Clicking an action highlights the element on the site where this action will be applied. Each VEC action created under a view has four icons as shown below: Information, Edit, Move to "Page Load" and Delete.

   ![Modifications panel](/help/c-experiences/assets/modifications.png)

   The following table describes each action:

   |Page|Description|
   | --- | --- |
   |Information|Displays the details of the action.|
   |Edit|Allows you to edit the properties of the action directly.|
   |Move to “Page Load”|Moves the action to page-load event. These actions are typically applied to static HTML of the SPA that are used across pages such as the header and footer.|
   |Delete|Deletes the action.|

   **Example 1**

   Let’s refer to the example above where we created a Home view. Our goal is two-fold for this view:

   1. Change the Add to Cart and the Like button to a lighter blue color. This should be in a “Page Load” since we are changing components of the header.
   1. Change the label Latest Products for 2019 to Hottest Products for 2019 with the text color changed to purple.

   In order to execute the two goals above, in the VEC, click [!UICONTROL Compose] and apply those changes on the Home view.

   ![Example 1](/help/c-experiences/assets/example1.png)

   **Example 2**

   Let’s refer to the example above where we created a PRODUCTS-PAGE-2 view. Our goal is to change the Price to Sale Price with the label color as red.

   1. Click [!UICONTROL Browse], then click the [!UICONTROL Products] link at the header. 
   1. Click [!UICONTROL Load More] once to get to the second row of products. 
   1. Click [!UICONTROL Compose].
   1. Apply actions to change the text label to Sale Price and the color to red.

   ![Example 2](/help/c-experiences/assets/example2.png)

   **Example 3**

   Lastly, as mentioned before, Views can be defined at a granular level. Views can be a state or even an option from a radio button. Previously we have created Views as CHECKOUT-EXPRESS and CHECKOUT-NORMAL. Our goal is to change the button color to red for the CHECKOUT-EXPRESS view.

   1. Click [!UICONTROL Browse].
   1. Add couple of products to the cart.
   1. Click the cart icon at the top right corner.
   1. Click Checkout your Order.
   1. Click on the Express Delivery radio button.
   1. Click [!UICONTROL Compose].
   1. Change the Pay to Complete the Order button color to red.

   ![Example 3](/help/c-experiences/assets/example3.png)

   >[!NOTE]
   >
   >The CHECKOUT-EXPRESS view will not show up in the modification panel until you click the Express Delivery radio button. This is because the `triggerView()` function is triggered when the Express Delivery radio button is selected and this is only when VEC knows that there is a View to show in the modification panel.

## Deep dive into at.js and SPAs

**How can I retrieve views for the latest audience data hydrated by actions after the initial page load on my SPA?**

The typical workflow of at.js 2.0 is when your site loads, all of your views and actions are cached so that subsequent user actions on your site won’t trigger server calls to retrieve offers. If you would like to retrieve views depending on the most up-to-date profile data that might have been updated depending on subsequent user actions, you can call `getOffers()` and `applyOffers()` with the latest audience user or profile data passed.

For example, consider that you are a telecom company and you have a SPA that uses at.js 2.0. As a business, you want to achieve the following objectives:

* For a logged out or anonymous user, show the latest company promotion such as showing a “First month free” hero offer on `http://www.telecom.com/home`.
* For a logged in user, show an upgrade promotional offer for users whose contracts are coming up such as “You are eligible for a free phone!” on `http://www.telecom.com/loggedIn/home`.

Now, your developers name views and call `triggerView()` in the following manner:

* For `http://www.telecom.com/home` the view name is Logged Out Home
  * `triggerView(“Logged Out Home”)` is invoked.
* For `http://www.telecom.com/loggedIn/home` the view name is Logged In Home.
  * `triggerView(“Logged In Home”)` is invoked on route change.

Your marketers then run the following A/B activities through the VEC:

* A/B activity with the “First Month Free” offer for audiences with the parameter “`loggedIn= false`” to be shown in `http://www.telecom.com/home` where the view name is Logged Out Home.
* A/B activity with the “You are eligible for a free phone!” offer for audiences with the parameter “`loggedIn=true`” to be shown in `http://www.telecom.com/loggedIn/home` where the view name is Logged In Hero Offer.

Now, lets consider this user flow:

1. An anonymous logged-out user lands on your page.
1. Because you are using at.js 2.0, you pass in the parameter “`loggedIn = false`” on page load to retrieve all views present in active activities that qualify for when the audience has parameter “`loggedIn = false`”. 
1. at.js 2.0 then retrieves the Logged Out Home view and action to show the “First Month Free” offer and stores it in cache.
1. When `triggerView(“Logged Out Home”)` is invoked, the “First Month Free” offer is retrieved from cache and the offer is shown without a server call.
1. The user now clicks “Log in” and provides his or her credentials. 
1. Because your website is a SPA, you do not conduct a full page load and instead route your user to `http://www.telecom.com/loggedIn/home`.

Now, here is the problem. The user logs in and we encounter `triggerView(“Logged In Home”)` because we placed this code on route change. This tells at.js 2.0 to retrieve the view and actions from cache, but the only view that exists in cache is Logged Out Home. 

So, how can we then retrieve our Logged In View and show the “You are eligible for a free phone!” offer? And since all subsequent actions on your site will be from a logged in user perspective, how can you make sure all subsequent actions result in personalized offers for logged in users?

You can use the new `getOffers()` and `applyOffers()` supported in at.js 2.0:

```
adobe.target.getOffers({
  request: {
  prefetch: {
    "views": [
      {
        "parameters": {
          "loggedIn": true
        },
      }
    ]
  },
});
```

Pass the response of `getOffers()` to `applyOffers()` and now all views and actions associated with “loggedIn = true” will update the at.js cache. 

In other words, at.js 2.0 supports a way to retrieve views, actions, and offers with the most up-to-date audience data in an on-demand fashion.

**Does at.js 2.0 support A4T for Single Page Applications?**

Yes, at.js 2.0 supports A4T for SPA via the `triggerView()` function given that you have implemented Adobe Analytics and the Experience Cloud Visitor ID Service. See the diagram below with step-by-step descriptions.

![Target Flow](/help/c-experiences/assets/atjs-spa-flow.png)

|Call|Description|
| --- | --- |
|1|`triggerView()` is called in the SPA to render a view and apply actions to modify visual elements associated to the view.|
|2|Targeted content for the view is read from the cache.|
|3|Targeted content is revealed as quickly as possible without flicker of default content.|
|4|Notification request is sent to the Target Profile Store to count the visitor in the activity and increment metrics.|
|5|Analytics data sent to Data Collection Servers.|
|6|Target data is matched to Analytics data via the SDID and is processed into the Analytics reporting storage. Analytics data can then be viewed in both Analytics and Target via A4T reports.|

>[!NOTE]
>If you don’t want to send notifications to Adobe Analytics for impression counting every time a view is triggered, pass in `{page: false}` to the `triggerView()` function so that impression counting is not inflated when a view is triggered multiple times for a component that re-renders constantly. For example:
>
>`adobe.target.triggerView(“PRODUCTS-PAGE-2”, {page:false})`

## Supported activities

|Activity Type|Supported?|
| --- | --- |
|A/B Test|Yes|
|Auto-Allocate|Yes|
|Experience Targeting|Yes|
|Multivariate Test|No|
|Auto-Target|No|
|Automated Personalization|No|
|Recommendations|No|

## Supported integrations

|Integration|Supported?|
| --- | --- |
|Analytics for Target (A4T)|Yes|
|Experience Cloud Audiences|Yes|
|Customer Attributes|Yes|
|AEM Experience Fragments|Yes|

## Supported features

|Feature|Supported?|
| --- | --- |
|Workspaces and Properties|Yes|
|QA Links|Yes|
|Form-based Experience Composer|No|
|Custom Code|Yes|
|VEC options|All|
|Click-tracking|Yes|
|Multi-Activity Delivery|Yes|
