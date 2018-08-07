---
description: Frequently asked questions to help you transition from Target Classic to Target Standard/Premium.
keywords: transition;migration;migrate from target classic to target standard
seo-description: Frequently asked questions to help you transition from Target Classic to Target Standard/Premium.
seo-title: Transition FAQ
solution: Target
title: Transition FAQ
uuid: 7d0d1aa3-2efa-4214-837b-95aa834a4d2e
index: y
internal: n
snippet: y
translate: y
---

# Transition FAQ

This section contains the following information:

* [ What are key dates/milestones of the Target Classic (Test&amp;Target) user interface that I should be aware of? ](c_transition-faq.md#section_C66AAD6CD46749FDA3B49BD6D5095EBB) 

* [ What happens if there is a campaign still running when... ](c_transition-faq.md#section_9C40A72D2BA04277AE5C42BAF1D39C90) 

* [ Can I still work with campaigns, audiences, and offers created in Target Classic in the new Target Standard/Premium UI? ](c_transition-faq.md#section_807EEABC65774A6E86D87DB8D0D0C86D) 

* [ What about if I am a Recommendations Classic customer? Will the current transition effort also apply to this user interface? ](c_transition-faq.md#section_8F2E5F8923824CD990D78A4255D61678) 

* [ What are the requirements for taking full advantage of the... ](c_transition-faq.md#section_D8A09BF3EAE84FE6AB5738C122BFF3EA) 

* [ What happens to existing activities created with the AEM 6... ](c_transition-faq.md#section_E064ACAF9D044157B6A4BEC904872E8F) 

* [ Who should I reach out to for assistance with setting... ](c_transition-faq.md#section_1C79914C333C482BA041E9B7764C4056) 

* [ Where do I find more resources on transition and potential... ](c_transition-faq.md#section_563CB23D8A50407790E16AC7C684C6EC) 



## What are key dates/milestones of the decommissioning of the Target Classic (Test&Target) user interface that I should be aware of? {#section_C66AAD6CD46749FDA3B49BD6D5095EBB}

We have been reaching out to existing Target Classic customers with plenty of time to transition before any milestones of the Target Classic user interface are reached. We have provided access to the new Adobe Target user interface to all customers contracted on legacy offerings, so that they can begin to adopt the new solution architecture for all of their needs. They can naturally transition their activities into the new UI over time. As stated, the new Adobe Target UI is backward-compatible in terms of implementation and can be accessed on any contracted offering immediately.
Although users will migrate to the new Adobe Target Premium or Adobe Target Standard offerings during the renewal process, below are key milestone dates to keep in mind regarding access to and usage of the Target Classic user interface.
Adobe Target Classic (Test&amp;Target) will be decommissioned in November 2017.

* **September 14, 2017 (Phase 1):**No new campaigns can be created in Target Classic; existing campaigns can still be edited. 

* **October 17, 2017 (Phase 2):**Read/Only status for all users; no new campaigns and no editing of existing campaigns in Target Classic. 
  APIs that are linked to your Target Classic account will be decommissioned. These API calls are based on a username and password-based authentication and use the hostname ` testandtarget.omniture.com`. If your API calls contain a user name and password in the request URL, you must transition to Adobe I/O APIs. 

* **November 14, 2017 (Phase 3):**Decommissioning of Target Classic; no access to UI. 
  The remaining APIs will be decommissioned.


We made the initial announcement to all users of the Target Classic user interface of these plans in September 2016.

## What happens if there is a campaign still running when Target Classic is deprecated? {#section_9C40A72D2BA04277AE5C42BAF1D39C90}

Your campaigns will still deliver as always. You can view them in the new interface and deactivate them after the end-of-life date for Target Classic. We'd recommend that you move them over to Target Standard/Premium beforehand, but nothing will actually stop working if you don't. You won't be able to view the campaign details or modify the campaign though. You'll just be able to change the state and view reports.

## Can I still work with campaigns, audiences, and offers created in Target Classic in the new Target Standard/Premium UI? {#section_807EEABC65774A6E86D87DB8D0D0C86D}


* Campaigns created in Target Classic display in Target Standard/Premium and can be activated, deactivated, and archived with the new UI. You cannot delete Campaigns created in Target Classic using Target Standard/Premium.

* Audiences created in Target Classic display in Target Standard/Premium and can be deleted with the new UI.

* Offers created in Target Classic can be fully edited with the new UI.



## What about if I am a Recommendations Classic customer? Will the current transition effort also apply to this user interface? {#section_8F2E5F8923824CD990D78A4255D61678}

Reach our to your Adobe account team to see our new innovations in Recommendations with Adobe Target Premium. The new Recommendations includes a new visual guided workflow; industry- and page-specific best practices and governance; Adobe Analytics-enhanced segmentation and reporting; and new personalized recommendations algorithms. There are videos and documentation here to get you started: [ Adobe Target Transition Hub ](https://docs.adobe.com/content/AdobeTarget/transition-hub.html). 

## What are the requirements for taking full advantage of the unified Adobe Marketing Cloud profile, Analytics integration, and other core services of Adobe Experience Cloud? {#section_D8A09BF3EAE84FE6AB5738C122BFF3EA}

Visit the [ Adobe Target Transition Hub ](https://docs.adobe.com/content/AdobeTarget/transition-hub.html) for more detailed information on the requirements and steps you should take to enable these services. Two options include: 

* (Recommended) [ at.js ](https://marketing.adobe.com/resources/help/en_US/target/ov2/c_target-atjs-implementation.html#) Version 1.0.0 or later. at.js is the new Target library, designed for greater efficiency and security, and also optimized for single-page applications. 

* [ mbox.js ](https://marketing.adobe.com/resources/help/en_US/target/ov/t_mbox_download.html#) version 53 or later. (Version 58 or later is recommended). 


Your organization also needs to be both an Adobe Analytics Standard or Premium customer, as well as being an existing Adobe Target Standard or Premium customer. The Visitor ID service needs to be implemented on your site, and then a provisioning request needs to be made for the server-to-server integration to be enabled in the back-end. Provisioning, under normal circumstances, takes less than a week.
For more information on implementation, see [ Understanding the Target JavaScript Libraries ](c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB). 

## What happens to existing activities created with the AEM 6.1-6.3 / Target integration after the end-of-life date for the Target Classic user interface? {#section_E064ACAF9D044157B6A4BEC904872E8F}

While the Adobe Experience Manager (AEM) 6.1-6.3 integration with Target does use a Target Classic API user behind the scenes, this is managed separately from the Target UI transition and will not be affected by the end-of-life plans. If you would like to set up an new integration with AEM and Target you will need to send a request to Adobe’s provisioning team, who can set up this integration for you.

## Who should I reach out to for assistance with setting up a transition plan or any technical assistance required? {#section_1C79914C333C482BA041E9B7764C4056}

You can reach out to your Account team, a Customer Success Manager, or your Consultant for any specific or custom questions relative to your account and implementation that you have concerning your transition. ClientCare is also available 24X7 for any immediate technical issues that arise.

## Where do I find more resources on transition and potential next steps and requirements, as well as guidance? {#section_563CB23D8A50407790E16AC7C684C6EC}

Adobe Target Product Marketing, Product Management, Consulting, and Training teams have made major investments in developing resources to assist with your transition plan with more detailed information on any subject related to the transition, as well as knowledge sharing on how to quickly get up to speed and get the most value from the new Adobe Target interface.
These can all be found on the [ Adobe Target Transition Hub ](https://docs.adobe.com/content/AdobeTarget/transition-hub.html). Be sure to check the hub regularly for updates on upcoming webinars/trainings/labs and knowledge-sharing events. We will send reminders on the key milestone dates as they approach, and how you can build momentum on your transition efforts. 
