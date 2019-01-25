---
description: There are many options for implementing Target in single-page applications with at.js.
keywords: single page application implementation;implement single page application;spa;ngroute;ui router;Component;directive;custom event;hashchange
seo-description: There are many options for implementing Target in single-page applications with at.js.
seo-title: Single Page Application implementation
solution: Target
title: Single Page Application implementation
topic: standard
uuid: 5887ec53-e5b1-40f9-b469-33685f5c6cd6
---

# Single Page Application implementation{#single-page-application-implementation}

There are many options for implementing Target in single-page applications with at.js.

 Use a combination of the following techniques for the best capabilities. We strongly recommend that you implement [!DNL Target] using [!DNL Adobe Launch], a free Core Service offering that can be used to quickly adapt your [!DNL Target] implementation as needed. For more information, see [Implementing Target using Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25).

| Implementation | Framework | DTM-Implementable? | Recommended mbox Name | Demo/Documentation |
|--- |--- |--- |--- |--- |
|ngRoute|Angular|Yes|target-global-mbox|[Demo](https://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/angular/route_change_demo.html#/view1)<br>[Documentation](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions/wiki/Angular-ngRoute)|
|Ui-router|Angular|Yes|target-global-mbox|[Demo](https://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/angular/state_change_demo.html#/view1)<br>[Documentation](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions/wiki/Angular-UIRouter)|
|Directive|Angular|Yes|Custom per content|[Demo](https://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/angular/directive_example.html#/view1)<br>[Documentation](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions/wiki/Angular-Directive)|
|Component|React|No|Custom per content|[Demo](https://adobe-marketing-cloud[.github.io/target-atjs-extensions/examples/react/react_component_demo.html#/view1?_k=zopyz4)<br>[Documentation](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions/wiki/React-Component)|](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions/wiki/React-Component)
|Custom event|All|Yes|target-global-mbox|[Documentation](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions/wiki/Custom-Event)|
|hashchange|All|Yes|target-global-mbox|[Demo](https://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/angular/hash_change_event.html)<br>[Documentation](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions/wiki/Hash-Change)|

>[!NOTE]
>
>If you previously used [ `mboxUpdate()`](../../../c-implementing-target/c-implementing-target-for-client-side-web/cmp-at.js-functions.md#reference_61B2B9F351344CF5B0915D5AFD21C5FE) or TNT.createGlobalMbox() to fire the global mbox on view changes within your app, you need to migrate to using a [combination of `getOffer()` and `applyOffer()`](../../../c-implementing-target/c-implementing-target-for-client-side-web/cmp-at.js-functions.md#reference_BBE83F513B5B4E03BBC3F50D90864245) for this purpose.

>[!NOTE]
>
>If you are using the Analytics for Target (A4T) implementation, ensure that you complete Step 8 in [Analytics for Target Implementation](../../../c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A).