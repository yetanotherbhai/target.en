---
description: Details about changes in each version of at.js.
keywords: at.js releases;at.js versions
seo-description: Details about changes in each version of at.js.
seo-title: at.js Version Details
solution: Target
subtopic: Getting Started
title: at.js Version Details
uuid: 5962fedc-2c79-4a7b-8eec-387aba85a54f
index: y
internal: n
snippet: y
translate: y
---

# at.js Version Details


<a id="section_CEA633C86E7040669785F63F79468B1A"></a>


>[!IMPORTANT]
>
>The Target team maintains only two versions of `at.js`—the current version and the second-latest version. Please upgrade `at.js` as necessary to ensure that you are running a supported version. 



<a id="section_61864A88D38B46C1825958FC4CD89EEA"></a>

This section contains information about the following `at.js` versions: 

* [at.js Version 1.2.1](r_target-atjs-versions.md#section_F757C8174BBA4F68AC5524ADC3D9C5E3)
* [at.js Version 1.2.0](r_target-atjs-versions.md#section_1C3A18C595C34B25A14A440D213F3B9C)
* [at.js Version 1.1.0](r_target-atjs-versions.md#section_8F494E1EA94E48A9B169F5CF9FE6DC56)
* [at.js Version 1.0.0](r_target-atjs-versions.md#section_37A3D23FC4AD42A68AA831B89E03E725)
* [at.js Version 0.9.7](r_target-atjs-versions.md#section_6C7B698BE21E40E495FD2850EFBF3E80)
* [at.js Version 0.9.6](r_target-atjs-versions.md#section_EEFA6413F2F947AD8C4A88128B90245D)
* [at.js Version 0.9.4](r_target-atjs-versions.md#section_A15B12F12CD94F07B3F56613A79A815F)
* [at.js Version 0.9.3](r_target-atjs-versions.md#section_DF13BC1D7C994AE7A36B81937A699DF4)
* [at.js Version 0.9.2](r_target-atjs-versions.md#section_148549CBB4F046BAA8F79C79B64EC889)
* [at.js Version 0.9.1](r_target-atjs-versions.md#section_DAFB99114D604CFB8416C1BC7DEEAEEE)
* [at.js Version 0.9.0](r_target-atjs-versions.md#section_2981CC9792F245389B39BB5B69F84C4E)
* [at.js Version 0.8.0](r_target-atjs-versions.md#section_E1C7B08EC0494388A022C28A8B8FE807)


## at.js Version 1.2.1 {#section_F757C8174BBA4F68AC5524ADC3D9C5E3}

`at.js` version 1.2.1 is now available. 

* Fixed an issue when click tracking on a link with target="_blank" prevented Target from opening the link in a new tab.



## at.js Version 1.2.0 {#section_1C3A18C595C34B25A14A440D213F3B9C}

`at.js` version 1.2 is now available as a maintenance release that contains mostly bug fixes. 

* Fixed an issue that prevented default actions for click-tracking special cases. (TNT-28089)

* Fixed an issue when click-tracking on a link with `target="_blank"` that prevented Target from opening the link in a new tab. (TNT-28072) 

* IP addresses can be used as the cookie domain. (TNT-28002)

* Fixed an issue that caused flicker in redirect offers with a global mbox or other regional mboxes. (TNT-27978)

* Fixed an issue in Experience Targeting activity setup failing within the VEC when switching between Browse and Compose. (TNT-27942)

* Fixed incorrect handling on flicker style classes for click-track elements. (TNT-27896)

* Fixed an issue that caused global mbox parameters to become mixed up with all mbox parameters. (TNT-27846)

* Made changes to ensure that Handlebars, Mustache, and other client-side templating libraries are properly handled by `at.js`. (TNT-27831) 

* Made changes to ensure that `sdidParamExpiry` is properly initialized and passed to the Visitor API. This is a regression that has been added to `at.js 1.1.0`. Previous `at.js` versions are not affected. This affects only clients using redirect offers and A4T. (TNT-27791) 

* Made changes to ensure that `SCRIPT` is executed regardless of the type attribute being used. (TNT-27865) 



## at.js Version 1.1.0 {#section_8F494E1EA94E48A9B169F5CF9FE6DC56}

**Date:**August 2, 2017 
The following enhancements and fixes are included in `at.js` version 1.1: 

* Added response token handling. For more information, see [Response Tokens](c_response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4). 

* Resolved issue so that `document.currentScript polyfill` doesn't interfere with Angular 1.X. 

* Made changes to ensure that click tracking doesn't interfere with visibility property. Click tracking elements are marked with the `at-element-click-tracking` CSS class instead of `at-element-marker`. 



## at.js Version 1.0.0 {#section_37A3D23FC4AD42A68AA831B89E03E725}

**Date:**July 7, 2017 
The following enhancements and fixes are included at.js version 1.0:

* Support for loading at.js asynchronously for faster page loads.

* Support for pre-hiding page content when loading at.js asynchronously.

* Better error messaging when content delivery is disabled.

* Performance improvements when delivering multiple activities.

* Support for YUI Compressor.

* Bug/error reporting for custom events during activity delivery.

* Fix for performance issues in Microsoft Internet Explorer 11.

* Fix for `getOffer()` function giving an error on some websites. 

* Load the Target library asynchronously. For more information, see [at.js Frequently Asked Questions](c_target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769). 



## at.js Version 0.9.7 {#section_6C7B698BE21E40E495FD2850EFBF3E80}

**Date:**May 22, 2017 
The following enhancements and fixes are included in `at.js` version 0.9.7: 

* Fixed an issue related to an asset key that was missing from `insertAfter` and `insertBefore` actions in the Visual Experience Composer (VEC). These issues were related to the migration from visual offers to offer templates.


## at.js Version 0.9.6 {#section_EEFA6413F2F947AD8C4A88128B90245D}

**Date:**April 13, 2017 
The following enhancements and fixes are included in `at.js` version 0.9.6: 

* Redirect offer support for A4T. After you download and install `at.js` version 0.9.6, you can use redirect offers in activities that use `Adobe Analytics` as the Reporting Source for `Target` (A4T). Besides `at.js` version 0.9.6, there are other minimum requirements your implementation must meet in order to use redirect offers and A4T. For more information and additional important information you should know, see [Redirect Offers - A4T FAQ](c_a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905). 

* Prior to `at.js` 0.9.6, when the Visitor API was present on the page and the `visitorApiTimeout` setting was too aggressive, Target could run into a situation when no MCID data was sent in the `Target` request. This could lead to issues like unstitched hits in `Analytics` when using A4T. 
  This behavior has been changed in `at.js` 0.9.6, even if the `visitorApiTimeout` is set to say 1 ms, Target will try to collect SDID, tracking servers, and customer IDs data and send those in the Target request. 

* Added the `selectorsPollingTimeout` setting. For more information, see [targetGlobalSettings()](c_atjs-settings-override.md#concept_8DACBC47ABDE4279BB102B42609FE506). 

* The format of the response from `getOffer()` has been changed. For more information, see [adobe.target.getOffer(options)](r_target-atjs-getoffer.md#reference_C81525D1598A4A1199740DCAB81A7FDF). 

* Console logging has been added for unsupported `<!DOCTYPE>` declarations. 

* Fixed an issue where `Target Classic` plugins weren’t being applied correctly when multiple default offers were delivered to a single mbox. (TGT-22664) For more information, see [Plug-Ins](https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Using_Plug-Ins.html) in the Adobe Target Classic documentation. 

* Improved cookie-setting for two letter top-level-domains (TLDs) to ensure that the mbox cookie is set correctly for these domains (for example, `test.no`, `autodrives.ca`, and so forth). 

* The algorithm for extracting the top-level domain that should be used when saving cookies has changed in `at.js` version 0.9.6. Because of this change, cookies cannot be saved to addresses that use IP. Most of the time, IP addresses are used for testing purposes, but as workarounds you can use DNS entries or adjust the hosts file on a local box. 

* Fixed move and rearrange actions handling when properties are string values instead of integers.



## at.js Version 0.9.4 {#section_A15B12F12CD94F07B3F56613A79A815F}

**Date:**January 19, 2017 

* mbox names can now contain special characters, including ampersands ( &amp; ), to be consistent with naming requirements for mbox names using `mbox.js`. 
  For a list of allowable special characters, see [Configure at.js](c_target-atjs-advanced-settings.md#concept_2FA0456607D04F82B0539C5BF5309812). 

* Added `secureOnly` setting that indicates whether `at.js` should use HTTPS only or be allowed to switch between HTTP and HTTPS based on the page protocol. This is an advanced setting that defaults to False and can be overridden via `targetGlobalSettings`. 

* The `Legacy Browser Support` option is available in `at.js` version 0.9.3 and earlier. This option was removed in `at.js` version 0.9.4. 



## at.js Version 0.9.3 {#section_DF13BC1D7C994AE7A36B81937A699DF4}

**Date:**October 10, 2016 

* Ensures mbox calls fire in Microsoft Internet Explorer 11 when legacy browsers are disabled in the `at.js` settings. 

* Ensures that default content is rendered if a dynamic remote offer fails (for example, if the URL is incorrect and returns a 404 error).

* Ensures that elements are revealed quickly when VEC click-tracking selectors can't be found in the DOM.



## at.js Version 0.9.2 {#section_148549CBB4F046BAA8F79C79B64EC889}

**Date:**September 21, 2016 

* Added an `optoutEnabled` setting to enable or disable the Device Graph opt-out. If this setting is set to `true` and the visitor has opted out of tracking, the visitor's browser will not make any mbox calls. Device Graph is currently in Beta. This setting is set to `false` by default, but must be set to `true` if you are using Device Graph. A similar option is part of `mbox.js` v61. 

* Added `CustomEvent` support for the notification mechanism. Previously, the `at.js` event notification mechanism could not be used via standard DOM APIs, such as `document.addEventListener()`. Now you can use `document.addEventListener()` to subscribe to `at.js` events, such as request events and content rendering events. 

* Fixed an issue related to offers created in the Visual Experience Composer (VEC). Prior to this release, Target hid the selectors and un-hid them only when all selectors matched. In `at.js` 0.9.2 Target un-hides the selectors as soon as they are matched. 



## at.js Version 0.9.1 {#section_DAFB99114D604CFB8416C1BC7DEEAEEE}

**Date:**July 14, 2016 

* Provides `at.js` a timeout for the Visitor Id Service, which is independent of the service’s own timeout. 

* Corrects an issue in 0.9.0 that impacted implementations using `at.js` on some pages and `mbox.js` on other pages. 

* If you use Adobe Analytics as your activity's reporting source, you do not need to specify a tracking server during activity creation if you are using `mbox.js` version 61 (or later) or `at.js` version 0.9.1 (or later). The `mbox.js` or `at.js` library automatically sends tracking server values to `Target`. During activity creation, you can leave the `Tracking Server` field empty on the `Goals &amp; Settings` page. 



## at.js Version 0.9.0 {#section_2981CC9792F245389B39BB5B69F84C4E}

**Target Release:** 16.6.1 
**Date:** June 23, 2016 
* Fixes a whitescreen issue when using VEC offers. Anyone using `at.js` should upgrade to this new version. 

* New `[registerExtension](r_target-atjs-registerextension.md#reference_B3ACC004D45E460C8DD94C1476D2625C)` API. 
  This new API gives developers access to certain jQuery modules used in `at.js` to develop extensions (aka plugins) for the library. There are a few implications for this change. This impact only those users who are using these features: 

    * `getSettings()` API has been removed, but the same functionality is available using `registerExtension()`. 

    * `getTracking()` API has been removed, but the same functionality is available using `registerExtension()`.
    * Existing extensions (e.g. AngularJS extensions) must be updated to use the `registerExtension()` approach. 


* New `[at.js notification](r_target-atjs-notification.md#reference_A828E4BA535F4E7692A075F3D70CF6CD)` API. 
  The goal of this notification system is to provide more insight into what `at.js` is doing on the page and when there are issues. A common issue seen with the VEC is that an IT release changes the page, a VEC selector breaks, and the test stops delivering content correctly. A goal of this notification system is to make this delivery issue known to the page, so developers can access this information, pass it to a system like `Adobe Analytics`, and alerts can be sent to the business owners that their test broke. 

* New `[at.js Settings Override](c_atjs-settings-override.md#concept_8DACBC47ABDE4279BB102B42609FE506) API method.` 
  You can override settings in the `at.js` library, rather than configuring the settings in the `Target Standard/Premium UI`or by using REST APIs. 



## at.js Version 0.8.0 {#section_E1C7B08EC0494388A022C28A8B8FE807}

**Date:**May 5, 2016. 
This is the first official release of the `at.js` library. 
`at.js` is a new implementation library for `Target` designed for both typical web implementations and single-page applications. 
`at.js` replaces `mbox.js` for `Adobe Target` implementations. 

>[!NOTE]
>
>Although `at.js` replaces `mbox.js`, `mbox.js` will continue to be supported. For most people, `at.js` provides advantages over `mbox.js`. This gives you time to test `at.js` and to change the implementation on your pages. 


Among other benefits, `at.js` improves page load times for web implementations, improves security, and provides better implementation options for single-page applications. 
`at.js` contains the components that were included in `target.js`, so there is no longer a call to `target.js`. 
When implementing `at.js`, be aware of the following: 

* Internet Explorer versions earlier than 8 are not supported.
* Asynchronous implementation means legacy integrations like the `Test&amp;Target` to `SiteCatalyst` plugin may not work.
* `Target` plugins that reference `mbox.js` objects and methods are not supported.
* All calls to `Target` are made via XMLHTTPRequest and content is returned via JSON.

