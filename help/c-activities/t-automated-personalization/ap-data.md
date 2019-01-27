---
description: Target automatically collects and uses a variety of data to build its personalization algorithms in Automated Personalization (AP) and Auto-Target (AT) activities. When a visitor enters the AP or AT activity, a snapshot of information is passed to a set of "training records" (the visitor data that the personalization algorithms will learn on).
seo-description: Target automatically collects and uses a variety of data to build its personalization algorithms in Automated Personalization (AP) and Auto-Target (AT) activities. When a visitor enters the AP or AT activity, a snapshot of information is passed to a set of "training records" (the visitor data that the personalization algorithms will learn on).
seo-title: Data collection for Target's personalization algorithms
solution: Target
title: Data collection for Target's personalization algorithms
title-outputclass: premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: premium
---

# ![PREMIUM](/help/assets/premium.png) Data collection for the Target personalization algorithms{#data-collection-for-the-target-personalization-algorithms}

Target automatically collects and uses a variety of data to build its personalization algorithms in Automated Personalization (AP) and Auto-Target (AT) activities. When a visitor enters the AP or AT activity, a snapshot of information is passed to a set of "training records" (the visitor data that the personalization algorithms will learn on).

To learn more about the Target personalization algorithms, see [Random Forest Algorithm](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

The following table shows the data collected by Automated Personalization by default, without the marketer having to do anything, as well as the naming convention used to indicate these attributes in [Personalization Insights Reports](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). You can augment the input data set at any time. To learn more about how to upload additional data, see [Uploading Data for the Target Personalization Algorithms](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Data Type | Description | Data Type Naming Convention | Example Attributes |
|--- |--- |--- |--- |
|URL Parameters|Target inspects the URL to extract the URL parameters.|`Custom - URL Parameter - [URL Parameter]`|Custom data|
|Referring URL Parameters|In general, the referring URL is the URL that referred to a particular page that initiated the mbox call.<br>Note that this variable can be impacted by the users' activity on your site as well as the technical implementation of your site.|`Custom - [Referring URL Parameter] - [Parameter value]`|Custom data|
|Environmental and Session data|Information about how and when the user is accessing the activity.|`Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]`|Visitor Profile - Start of Most Recent Visit<br>Visitor Profile -Total Visits<br>Visitor Profile - Average Time per Visit<br>Browser - Timezone<br>Browser - Day of Week<br>Browser - Language Setting<br>Browser - Type<br>Operating System - Version|
|Geography|Information on where the visitor is located.|`Geo - [geo attribute]`|City<br>Country<br>Region/State<br>Zip Code<br>Latitude<br>Longitude<br>ISP or Mobile Carrier|
|Device and Mobile Data|Device and mobile-specific information.|`Device - [device attribute]`<br>`Mobile - [mobile attribute]`|Mobile Device OS<br>Mobile Screen Size|

