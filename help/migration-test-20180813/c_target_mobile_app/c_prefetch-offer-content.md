---
description: The Adobe Target prefetch feature uses the iOS and Android Mobile SDKs to fetch offer content as few times as possible by caching the server responses.
keywords: offer;prefetch;iOS;android
seo-description: The Adobe Target prefetch feature uses the iOS and Android Mobile SDKs to fetch offer content as few times as possible by caching the server responses.
seo-title: Prefetch Offer Content
solution: Target
title: Prefetch Offer Content
topic: Advanced,Standard,Classic
uuid: 637f8d05-edcb-457e-862f-da1d11b86a8f
index: y
internal: n
snippet: y
translate: y
---

# Prefetch Offer Content

This process reduces the load time, prevents multiple network calls, and allows Adobe Target to be notified which mbox was visited by the mobile app user. All content will be retrieved and cached during the prefetch call, and this content will be retrieved from the cache for all future calls that contain cached content for the specified mbox name. 

Prefetch content does not persist across launches. The prefetch content is cached as long as the application lives or until the ` clearPrefetchCache()` method is called. 

For more information, including prefetch methods, public classes, and code samples, see: 


* **iOS: **[ Prefetch Offer Content in iOS](https://marketing.adobe.com/resources/help/en_US/mobile/ios/c_mob_target-prefetch_ios.html) in the* iOS SDK 4.x for Experience Cloud Solutions* guide. 

* **Android: **[ Prefetch Offer Content in Android](https://marketing.adobe.com/resources/help/en_US/mobile/android/c_mob_target-prefetch_android.html) in the *Android SDK 4.x for Experience Cloud Solutions* guide. 


