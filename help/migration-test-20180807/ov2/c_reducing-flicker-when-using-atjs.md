---
description: Information about the advantages of using at.js versus mbox.js and information to help you reduce page flicker by using a combination of page-loader images and the Target Timeout setting.
keywords: at.js;flicker;loader;page loader;page loader image;at.js versus mbox.js;at.js advantages
seo-description: Information about the advantages of using at.js versus mbox.js and information to help you reduce page flicker by using a combination of page-loader images and the Target Timeout setting.
seo-title: Reducing Flicker When Using at.js
solution: Target
subtopic: Getting Started
title: Reducing Flicker When Using at.js
uuid: 77b71b10-a243-4263-bf2f-2b873d78af1c
index: y
internal: n
snippet: y
translate: y
---

# Reducing Flicker When Using at.js

Although ` at.js` replaces ` mbox.js`, ` mbox.js` will continue to be supported. For most people, ` at.js` provides advantages over ` mbox.js`. 
Among other benefits, ` at.js` improves page-load times for web implementations, improves security, and provides better implementation options for single-page applications. 
The following diagram illustrates page-load performance using ` mbox.js` versus ` at.js`. 

>[!NOTE]
>
>The diagram is a visualization of the sequence of events during page load. This data is*NOT* representative of expected performance. 


![](../graphics/atjs vesus mboxjs.png) 
As illustrated above, using ` mbox.js`, page content does not begin to load until after the ` Target` call is complete. Using ` at.js`, page content begins loading when the ` Target` call is initiated and does not wait until the call is complete. 
You should see improved page-load performance when using ` at.js`, but some pages might experience flicker when changing elements at the top of the page. 
The best way to reduce flicker during page load is to configure the [ Timeout setting ](c_target-atjs-advanced-settings.md#concept_2FA0456607D04F82B0539C5BF5309812) appropriately and use a page-loader image that displays during page rendering. 
You should use a loader rather than hiding default content until the ` Target` call is complete. Hiding default content with a loader until the call is complete avoids a poor user experience for pages with significant changes, as illustrated in the following diagram. 

>[!NOTE]
>
>The diagram is a visualization of the sequence of events during page load. This data is*NOT* representative of expected performance. 


![](../graphics/loader1.png) 
The loader screen appearance, coverage area, and deployment logic are fully customizable. The following illustrations show different coverage areas for the loader screen. You should configure the coverage area to best suit your needs.
The first illustration shows a loader image that covers approximately half of the page:
![](../graphics/loader2.png) 
Target activities that change visible areas on the page might result in flicker. For example, in the above illustration, changing the text from "Your current bill" to "This month's statement" might be visible to visitors. To avoid this situation, you can enlarge the loader coverage area, as in the following illustration:
![](../graphics/loader3.png) 
Target seamlessly manipulates on-page content. When the page loads, visitors see the fully rendered activity experience.
As previously mentioned, the use of a page-loader image and the ` Target` [ Timeout setting ](c_target-atjs-advanced-settings.md#concept_2FA0456607D04F82B0539C5BF5309812) should be used in combination to reduce flicker. Consider the following points when configuring the Timeout setting: 

* The optimal Timeout setting varies by visitor. Target server response times depend on the visitor's connection speed.

* Too short of a Timeout setting causes:

    * Visitors on slower connections will not qualify for ` Target` activities. 

    * Increased activity duration will be required to reach statistical significance.



* Too long of a Timeout setting causes:

    * Visitors exposed to the loader for too long might navigate away from your page.




The maximum Timeout setting should account for the worst case scenario on slow connections (for example, mobile users on 3G). Adobe recommends a two-second Timeout setting; however, your business needs might dictate a different setting. The best way to find the optimal setting is to run a monitoring activity to measure ` Target` server response time dispersion. 
