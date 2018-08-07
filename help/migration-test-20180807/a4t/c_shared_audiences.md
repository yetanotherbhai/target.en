---
description: Audience data collected by Analytics is used for real-time targeting and personalization in Adobe Target and other Marketing Cloud solutions.
keywords: Marketing cloud audiences;Shared audiences
seo-description: Audience data collected by Analytics is used for real-time targeting and personalization in Adobe Target and other Marketing Cloud solutions.
seo-title: Real-Time Shared Audiences
solution: Target,Analytics,Marketing Cloud
title: Real-Time Shared Audiences
uuid: 46093e53-0bd3-4bbd-b812-943bceb2c7b9
index: y
internal: n
snippet: y
translate: y
---

# Real-Time Shared Audiences


>[!NOTE]
>
>Real-time shared audiences requires both Target and Analytics.


The Visitor ID service provides a single visitor ID for a single view across Marketing Cloud solutions. The service does not replace audience IDs in Target or Analytics, but adds an additional Marketing Cloud-level ID. This Marketing Cloud ID augments the data sets that are already in Target and Analytics, so existing data is not lost.
Share audiences from Analytics to the Marketing Cloud and select them in Target for use when targeting campaigns.
Use the [Marketing Cloud Audience Library](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html) to create and manage shared audiences. You can view intersections and unions of audiences and estimate the number of visitors you'll impact with your audiences. All of this can be done during the audience creation process. 
EDGE-accessible audiences are available in Target, Audience Manager, and Analytics.
**Key Benefits** 
Real-time shared audiences provide the following benefits:

* Common Marketing Cloud level ID
* Server-to-server integration, rather than page-level integration, for additional robustness
* Fewer tags
* Real-time and next-click targeting There is no need to wait for next page load. The information is available on the next click. This generates relevant personalized experiences more rapidly.

* Manage audiences for all solution in a single place, the shared audience library.
* No data variance
* Filter on any Analytics metrics and segments, which don't need to be defined at the beginning of the campaign
* Updated data collection infrastructure improves performance by using the nearest data center
**First-Time Visitors** 
It is recommended that you use Target to create segments for activities targeted at first-time visitors.
A first-time visitor does not yet have a Visitor ID. Sometimes, Target's call to the Marketing Cloud is not fast enough and is made without the Visitor ID. In this case, the Supplemental ID that is built in to the page is sent to both Analytics and Target, and is used for reporting.
However, the Supplemental ID can cause issues for audience sharing. The visitor is not recognized as belonging to a shared audience on the first click of the first visit. This includes audiences shared from the Audience Library, Analytics, and Audience Manager.
In Analytics, there is no data for that first-time visitor, so this is not an issue. In the Audience Library, raw analytics attributes are used, so there is no effect. However, certain technographic audience set up in the Audience Library, such the browser the visitor uses or the time of day, cannot be used on that visitor.
If that visitor is important to you, the audience should be built in Target, not in Analytics or the Audience Library.
