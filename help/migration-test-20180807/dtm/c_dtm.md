---
description: This section describes how to implement Target Standard with Digital Tag Management .
keywords: Dynamic tag management
seo-description: This section describes how to implement Target Standard with Digital Tag Management .
seo-title: Implementing Target Standard with Digital Tag Management
solution: Target
title: Implementing Target Standard with Digital Tag Management
uuid: 2a257966-b6b9-4922-869e-41706616ad1f
index: y
internal: n
snippet: y
translate: y
---

# Implementing Target Standard with Digital Tag Management

To ensure synchronous delivery of `mbox.js`, enable both the `target.js` and Autocreate Global plugins. Then paste your mbox.js in the sequential JavaScript page load rule in DTM and set the condition to execute in the head. If the global mbox does not execute, check the load condition, and make sure that the mbox auto create is enabled. The autocreate global mbox routine deploys differently depending on the page. 

>[!NOTE]
>
>The sequential JavaScript deployment method is not required if the client uses the DTMbox (async) method.


