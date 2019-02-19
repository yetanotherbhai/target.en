---
description: Upgrading from at.js 1.x to at.js 2.0.0
keywords: at.js releases;at.js versions;single page app; spa
seo-description: Detailed information about how to upgrade from Adobe Target at.js 1.x to at.js version 2.0.0
seo-title: Upgrade from Adobe Target at.js version 1.x to at.js version 2.0.0 
solution: Target
subtopic: Getting Started
title: Upgrading from at.js 1.x to at.js 2.0
uuid: 3586af55-db15-4e68-90a7-d552338ec5e8
---

# Upgrading from at.js 1.x to at.js 2.0.0 {#upgrading-from-atjs-1x-to-atjs-200}

The newest version of at.js provides rich feature sets that equip your business to execute personalization on next-generation, client-side technologies. This new version is focused on upgrading at.js to have harmonious interactions with single page applications (SPAs). 

Here are some benefits of using at.js 2.0.0 that are not available in previous versions:

* The ability to cache all offers on page-load to reduce multiple server calls to a single server call.
* Tremendously improve your end-users' experiences on your site because offers are shown immediately via the cache without any lag time that traditional server calls introduce.
* Simple one-line of code and one-time developer setup to enable your marketers to create and run A/B and XT activities via the VEC on your SPAs.

## at.js 2.0.0 system diagrams

The following diagrams help you understand the workflow of at.js 2.0.0 with Views and how this enhances the SPA integration. To get a better introduction of the concepts used in at.js 2.0.0, see [Single Page Application implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target flow with at.js 2.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

|Call|Details|
| --- | --- |
|1|Call returns the [!DNL Experience Cloud ID] if the user is authenticated; another call syncs the customer ID.|
|2|The at.js library loads synchronously and hides the document body.<br>at.js can also be loaded asynchronously with an option prehiding snippet implemented on the page.|
|3|A page load request is made including all configured parameters (MCID, SDID, and customer ID).|
|4|Profile scripts execute and then feed into the Profile Store. The Store requests qualified audiences from the Audience Library (for example, audiences shared from Adobe Analytics, Audience Management, etc.).<br>Customer attributes are sent to the Profile Store in a batch process.|
|5|Based on URL request parameters and profile data, [!DNL Target] decides which activities and experiences to return to the visitor for the current page and future views.|
|6|Targeted content is sent back to the page, optionally including profile values for additional personalization.<br>Targeted content on the current page is revealed as quickly as possible without flicker of default content.<br>Targeted content for views that are shown as a result to user actions in a SPA that is cached in the browser so it can be instantly applied without an additional server call when the views are triggered through `triggerView()`.|
|7|Analytics data is sent to Data Collection servers.|
|8|Targeted data is matched to Analytics data via the SDID and is processed into the Analytics reporting storage.<br>Analytics data can then be viewed in both Analytics and Target via Analytics for Target (A4T) reports.|

Now, wherever `triggerView()` is implemented on your SPA, the Views and actions are retrieved from cache and shown to the user without a server call. `triggerView()` also makes a notifications request to the [!DNL Target] backend in order to increment and record impression counts.

![Target flow at.js 2.0 triggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

|Call|Details|
| --- | --- |
|1|`triggerView()` is called in the SPA to render the View and apply actions to modify visual elements.|
|2|Targeted content for the view is read from the cache.|
|3|Targeted content is revealed as quickly as possible without flicker of default content.|
|4|Notification request is sent to the [!DNL Target] Profile Store to count the visitor in the activity and increment metrics.|
|5|Analytics data sent to Data Collection Servers.|
|6|Target data is matched to Analytics data via the SDID and is processed into the Analytics reporting storage. Analytics data can then be viewed in both Analytics and Target via A4T reports.|

## Deploy at.js 2.0.0 {#deploy-atjs-200}

1. Download at.js 2.0.0 using the Target UI.

   ![Implementation details dialog box](/help/c-experiences/assets/implement-atjs-2.png)

>[!NOTE]
>
>Installing at.js 2.0 via the [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) extension is not yet supported.

## Deprecated at.js functions

There are several functions that have been deprecated in at.js 2.0.0. 

>[!IMPORTANT]
>
>If these deprecated functions are still used on your site when at.js 2.0.0 is deployed, you will see console warnings. The recommended approach when upgrading is to test the deployment of at.js 2.0.0 in a staging environment and make sure to go through each and every warning that has been logged in the console and translate the deprecated functions to new functions introduced in at.js 2.0. 

You can find the deprecated functions and their counterpart below. For a complete list of functions, see [at.js functions](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-at.js-functions.md).

>[!NOTE]
>At.js 2.0.0 no longer automatically pre-hides `mboxDefault` marked elements. Customers will therefore have to accommodate for the pre-hide logic manually on the site or through a tag manager.

### mboxCreate(mbox,params)

**Description**: 

Executes a request and applies the offer to the closest DIV with the `mboxDefault` class name.

**Example**:

```
<div class="mboxDefault">
  default content to replace by offer
</div>
<script>
  mboxCreate('mboxName','param1=value1','param2=value2');
</script>
```

**at.js 2.0.0 equivalent**

An alternative to `mboxCreate(mbox, params)` is `getOffer()` and `applyOffer()`.

**Example**:

```
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  var el = document.currentScript.previousElementSibling;
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2"
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: el,
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      el.style.visibility = "visible";
    }
  });
</script> 
```

### mboxDefine() and mboxUpdate()

**Description**:

Creates an internal mapping between an element and an mbox name, but does not execute the request. Used in conjunction with `mboxUpdate()`, which executes the request and applies the offer to the element identified by the nodeId in `mboxDefine()`. Can also be used to update an mbox initiated by `mboxCreate`.

**Example**:

```
<div id="someId" class="mboxDefault"></div>
<script>
 mboxDefine('someId','mboxName','param1=value1','param2=value2');
 mboxUpdate('mboxName','param3=value3','param4=value4');
</script>
```

**AT.js 2.0.0 equivalent**:

An alternative to `mboxDefine()` and `mboxUpdate` is `getOffer()` and `applyOffer()`, with the selector option used in `applyOffer()`. This approach lets you map the offer to an element using any CSS selector, not just one with an ID.

**Example**:

```
<div id="someId" class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2",
      param3: "value3",
      param4: "value4" 
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: "#someId",
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      var el = document.getElementById("someId");
      el.style.visibility = "visible";
    }
  });
</script>
```

### adobe.target.registerExtension()

**Description**:

Provides a standard way to register a specific extension.

This is no longer supported and should not be used.

## Summary of deprecated, new, and supported at.js functions in 2.0

|Method|Supported?|New?|Deprecated?<br>(Default content will be shown)|
| --- | --- | --- | --- |
|`getOffer()`|Yes|||
|`getOffers()`||Yes||
|`applyOffer()`|Yes|||
|`applyOffers()`||Yes||
|`triggerView()`||Yes||
|`trackEvent()`|Yes|||
|`mboxCreate()`|||Yes|
|`mboxDefine()`<br>`mboxUpdate()`|||Yes|
|`targetGlobalSettings()`|Yes|||
|`Data Providers`|Yes|||
|`targetPageParams()`|Yes|||
|`targetPageParamsAll()`|Yes|||
|`registerExtension()`|||Yes|
|`At.js Custom Events`|Yes|||

## Limitations and callouts

Be aware of the following limitations and callouts:

**Conversion tracking**

Customers using `mboxCreate()` for conversion tracking must use `trackEvent()` or `getOffer()`.

**Offer delivery**

Customers who do not replace `mboxCreate()` with `getOffer()` or `applyOffer()` risk not having offers delivered.

**Can at.js 2.0.0 be used on some pages while at.js 1.*x* or mbox.js is on other pages?**

Yes, the visitor profile is preserved across pages using different versions and libraries. The cookie format is the same.

**Adobe Experience Cloud Debugger is not fully supported in at.js 2.0.0**

[!DNL Adobe Experience Cloud Debugger] [!UICONROL Summary Tab] features and [!UICONTROL Disable and Console Logging] tools are supported, but Network Requests and mboxTrace are not supported for at.js 2.0.0. 

This is because in at.js 2.0.0, a JSON payload is sent instead of key-value pairs. To inspect [!DNL Target] requests, filter the [!UICONTROL Network] tab of your browser’s Developer Tools to “delivery”, “`tt.omtrdc.net`,” or your client code. Trace data can still be inspected by using the query string parameter and authorization token. For more information, see [mboxTrace](/help/c-activities/c-troubleshooting-activities/content-trouble.md).

**New API use in at.js 2.0.0**

at.js 2.0.0 uses a new API, which we call the Delivery API. In order to debug whether at.js is calling the [!DNL Target] edge server correctly, you can filter the Network tab of your browser’s Developer Tools to “delivery”, “`tt.omtrdc.net`,” or your client code. You will also notice that [!DNL Target] sends a JSON payload instead of key-value pairs.

**Target Global Mbox is no longer used**

In at.js 2.0.0, you no longer see “`target-global-mbox`” visibly in the network calls. Instead, we have replaced the “`target-global-mbox`” syntax to “`execute > pageLoad`” in the JSON payload sent to the [!DNL Target] servers, as seen below:

```
{
  "id": {
    // ...
  },
  "context": {
    "channel": "web",
    // ...
  },
  "execute": {
    "pageLoad": {}
  }
}
```

Essentially the global mbox concept was introduced to let [!DNL Target] know whether to retrieve offers and content on page-load. Thus, we have made this more explicit in our newest version.

**Does the global mbox name in at.js matter anymore?**

Customers are able to specify a global mbox name via [!UICONTROL Target > Setup > Implementation > Edit at.js Settings]. This setting is used by the [!DNL Target] edge severs to translate execute > pageLoad to the global mbox name that appears in the [!DNL Target] UI. This allows customers to continue to use server-side APIs, the form-based composer, profile scripts, and create audiences using the global mbox name. We strongly recommend that you also make sure the same global mbox name is configured on the [!UICONTROL Setup > Preferences] page, as well, in case you still have pages using at.js 1.*x* or mbox.js, as shown in the following illustrations.

![Modify at.js dialog](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/modify-atjs.png)

and

![Custom Global mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/custom-global-mbox.png)

**Does the auto-create global mbox setting need to be turned on for at.js 2.0.0?**

In most cases, yes. This setting tells at.js 2.0.0 to fire a request to the [!DNL Target] edge servers upon page load. Because global mbox is translated to execute > pageLoad, and if you want to fire a request on page load, then this setting should be on.

**Will existing VEC activities continue to work, even though the target global mbox name is not specified from at.js 2.0.0?**

Yes, because execute > pageLoad is treated on the [!DNL Target] backend like `target-global-mbox`.

**If my form-based activities are targeted to the `target-global-mbox`, will those activities continue to work?**

Yes, because execute > pageLoad is treated on the [!DNL Target] edge servers like `target-global-mbox`.

**Supported and non-supported at.js 2.0.0 Settings**

|Setting|Supported?|
| --- | --- |
|X-Domain|No|
|Auto Create Global Mbox|Yes|
|Global Mbox Name|Yes|

**Cross-domain tracking is *not* supported**

Cross-domain tracking makes it possible to see sessions on two-related sites, but with different domains, as a single session. You could create a [!DNL Target] activity that spans `siteA.com` and `siteB.com` and the visitor would remain in the same experience when they crossed domains. This functionality ties into Target’s third-party and first-party cookie behavior.

In [!DNL Target], the third-party cookie is stored in `[CLIENTCODE].tt.omtrdc.net` and the first-party cookie is stored in `clientdomain.com`. The first request returns HTTP response headers that attempt to set third-party cookies named `mboxSession` and `mboxPC`, whereas a redirect request is sent back with an extra parameter (`mboxXDomainCheck=true`). If the browser accepts third-party cookies, the redirect request includes those cookies, and the offer is returned. This workflow is possible because we use the HTTP GET method.

However, in at.js 2.0.0, HTTP GET is no longer used and instead we use HTTP POST. HTTP POST is now used via at.js in order to send JSON payloads to [!DNL Target] edge servers. This means that the redirect request to check whether a browser supports third-party cookies now breaks. This is because HTTP GET requests are idempotent transactions, while HTTP POST is non-idempotent and mustn’t be arbitrarily repeated. Therefore, cross-domain tracking in at.js 2.0.0 is no longer supported.

**Auto Create Global Mbox is supported**

This setting tells at.js 2.0.0 to fire a request to the [!DNL Target] edge servers on page-load. Because the global mbox is translated to execute > pageLoad, and this is interpreted by the [!DNL Target] edge servers, customers should turn this on if they want to fire a request on page-load.

**Global Mbox Name is supported**

Customers are able to specify a global mbox name via [!UICONTROL Target > Setup > Implementation > Edit at.js Settings]. This setting is used by the [!DNL Target] edge severs to translate execute > pageLoad to the inputted global mbox name. This allows for customers to continue to use server-side APIs, the form-based composer, profile scripts, and create audiences that target the global mbox.

**Are the below at.js custom events applicable to `triggerView()` or is it only for `applyOffer()` or `applyOffers()`?**

* `adobe.target.event.CONTENT_RENDERING_FAILED`
* `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`
* `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`
* `adobe.target.event.CONTENT_RENDERING_REDIRECT`

Yes the at.js custom events are applicable to `triggerView()` as well.

**It says when I call `triggerView()` with `{“page” : “true”}`, it will send a notification to the [!DNL Target] backend and increase the impression. Does it also cause the profile scripts to execute?**

When a prefetch call is made to the [!DNL Target] backend, the profile scripts are executed. Thereafter, the impacted profile data will then be encrypted and passed back to the client side. After `triggerView()` with `{"page": "true"}` is invoked, a notification is sent along with the encrypted profile data. This is when the [!DNL Target] backend will then decrypt the profile data and store into the databases.

**Do we need to add pre-hiding code before calling `triggerView()` in order to manage flicker?**

No, you do not need to add pre-hiding code before calling `triggerView()`. at.js 2.0.0 manages the pre-hiding and flicker logic before the view is displayed and applied.

## at.js compatibility

The following tables explain at.js. 2.0.0 compatibility with different activity types, integrations, features, and at.js functions.

### Activity types

|Type|Supported?|
| --- | --- |
|A/B Test|Yes|
|Auto-Allocate|Yes|
|Auto-Target|Yes|
|Experience Targeting|Yes|
|Multivariate Test|Yes|
|Automated Personalization|Yes|
|Recommendations|Yes|

### Integrations

|Type|Supported?|
| --- | --- |
|Analytics for Target (A4T)|Yes|
|Audiences|Yes|
|Customer Attributes|Yes|
|AEM Experience Fragments|Yes|
|Adobe Launch extension|Not currently|
|Debugger|Currently no request capture or mboxTrace|
|Auditor|Rules have not yet been updated for at.js 2.0|
|Dynamic Tag Manager (DTM)|Yes|
|Opt-In| No |
| AEM Enhanced Personalization powered by Adobe Target | No|

### Features

|Feature|Supported?|
| --- | --- |
|X-Domain|No|
|Properties/Workspaces|Yes|
|QA links|Yes|
|Form-based Experience Composer|Yes|
|Visual Experience Composer (VEC)|Yes|
|Custom code|Yes|
|Response tokens|Yes|
|Click-tracking|Yes|
|Multi-activity delivery|Yes|
|targetGlobalSettings|Yes (but not x-domain)|
|at.js methods|Everything is supported except for<br>`mboxCreate()`<br>`mboxUpdate()`<br>`mboxDefine()`<br>which will display default content.|

### Query string parameters

|Parameter|Supported?|
| --- | --- |
|`?mboxDisable`|Yes|
|`?mboxDisable`|Yes|
|`?mboxTrace`|Yes|
|`?mboxSession`|No|
|`?mboxOverride.browserIp`|No|

## Training video: at.js 2.0.0 architectural diagram

at.js 2.0.0 enhances Adobe Target's support for SPAs and integrates with other Experience Cloud solutions. This video explains how everything comes together.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

See [Understanding how at.js 2.0.0 works](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) for more information.