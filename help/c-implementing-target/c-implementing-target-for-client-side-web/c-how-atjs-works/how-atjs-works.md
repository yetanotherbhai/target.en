---
description: Target system diagram showing the flow of calls and information sent or collected for an auto-created global mbox using at.js.
keywords: system diagram;flicker;Target Standard;at.js;implementation
seo-description: Target system diagram showing the flow of calls and information sent or collected for an auto-created global mbox using at.js.
seo-title: How at.js works
solution: Target
title: How at.js works
topic: Standard
uuid: 8ed04881-3dd9-496f-9c9c-feb9c740ed80
---

# How at.js works{#how-at-js-works}

Target system diagram showing the flow of calls and information sent or collected for an auto-created global mbox using at.js.

In the Target implementation illustrated below, the following Experience Cloud solutions are implemented: Analytics, Target, and Audience Management. In addition, the following Experience Cloud core services are implemented: Dynamic Tag Management (Activation), Audiences, and Visitor ID Service.

![](assets/target-flow.png)

| Call | Description | Call | Description |
|--- |--- |--- |--- |
|![Step 1](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/assets/step1_red.png)|Call returns the [!DNL Experience Cloud ID] (MCID) if the user is authenticated; another call syncs the customer ID.|![Step 2](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/assets/step2_red.png)|The at.js library loads synchronously and hides the document body.|
|![Step 3](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/assets/step3_red.png)|A global mbox request is made including all configured parameters, MCID, SDID, and customer ID (optional).|![Step 4](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/assets/step4_red.png)|Profile scripts execute and then feed into the Profile Store. The Store requests qualified audiences from the [!UICONTROL Audience Library] (for example, audiences shared from [!DNL Adobe Analytics], [!DNL Audience Manager], etc.).<br>Customer attributes are sent to the [!DNL Profile Store] in a batch process.|
|![Step 5](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/assets/step5_red.png)|Based on the URL, mbox parameters, and profile data, [!DNL Target] decides which activities and experiences to return to the visitor.|![Step 6](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/assets/step6_red.png)|Targeted content is sent back to page, optionally including profile values for additional personalization.<br>The experience is revealed as quickly as possible without flicker of default content.|
|![Step 7](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/assets/step7_red.png)|[!DNL Analytics] data is sent to Data Collection servers.|![Step 8](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/assets/step8_red.png)|[!DNL Target] data is matched to [!DNL Analytics] data via the SDID and is processed into the [!DNL Analytics]  reporting storage.<br>[!DNL Analytics] data can then be viewed in both [!DNL Analytics] and  [!DNL Target] via [!DNL Analytics for Target] (A4T) reports.|