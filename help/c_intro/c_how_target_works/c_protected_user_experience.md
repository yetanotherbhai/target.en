---
description: Adobe ensures that the availability and performance of the targeting infrastructure is as reliable as possible. However, a communication breakdown between an end-user’s browser and Adobe’s servers can cause an interruption in content delivery.
keywords: Overview and Reference
seo-description: Adobe ensures that the availability and performance of the targeting infrastructure is as reliable as possible. However, a communication breakdown between an end-user’s browser and Adobe’s servers can cause an interruption in content delivery.
seo-title: Protected User Experience
solution: Target
subtopic: Getting Started
title: Protected User Experience
topic: Standard
uuid: 2f529365-228c-4e03-b441-911893772c0f
index: y
internal: n
snippet: y
translate: y
---

# Protected User Experience

To safeguard against service interruptions and connectivity issues, all locations are set up to include default content (defined by the client), which is surfaced if the user’s browser cannot connect to [!DNL  Target]. 

No changes are made to the page if the user’s browser cannot connect within a defined timeout period (by default,15 seconds). If this timeout threshold is reached, a setting is changed in the cookie so the user sees default content for all other locations immediately. This state lasts for a half hour, after which the user’s browser again attempts to contact Adobe’s servers for content requests. 

Adobe protects the user experience by optimizing and safeguarding performance. 


* Adobe ensures performance benchmarks based on industry standards, which are guaranteed by the Adobe Service Level Agreement.
* The Edge Network ensures timely data delivery.
* Adobe employs a multi-tiered approach to securing its applications to provide the highest level of availability and reliability for customers.
* [!DNL  Target] Consulting offers implementation assistance and ongoing product support.

