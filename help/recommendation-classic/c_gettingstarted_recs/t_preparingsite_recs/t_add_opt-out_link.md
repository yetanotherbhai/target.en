---
description: You can add an opt-out link to your sites to enable visitors to opt-out of all recommendations counting and content delivery.
seo-description: You can add an opt-out link to your sites to enable visitors to opt-out of all recommendations counting and content delivery.
seo-title: Adding an Opt-Out Link
solution: Target
title: Adding an Opt-Out Link
topic: Recommendations
uuid: 8589db7c-e9de-468c-ba23-b73f9296743b
index: y
internal: n
snippet: y
translate: y
---

# Adding an Opt-Out Link


>1. Add the following link to your site:

>       ` <a href="http://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>` 
>1. Replace the ` clientcode` text with your client code, and add the text or image to be linked to the opt-out URL.
>Any visitor who clicks this link is not included in any mbox requests called from their browsing sessions until they delete their cookies, or for two years, whichever comes first. This works by setting a cookie for the visitor called ` disableClient` in the ` clientcode.tt.omtrdc.net` domain. 

>Even if you use a first-party cookie implementation, the provided opt-out is set via a 3rd-party cookie. If the client is using a first-party cookie only, Adobe checks whether an opt-out cookie is set. 

>>[!MORE_LIKE_THIS] {class="- topic/related-links "}
>>
>>* [ Preparing Your Website for Recommendations ](t_preparingsite_recs.md#task_30B8C075A14B426F9042119553F750B8)
>>* [ Downloading the mbox.js Library File ](t_mboxjs_dl_recs.md#task_6B577DD43FD346F7BC01962DAA822816)
>>* [ Validating the mbox.js Download ](t_Validating_the_mboxjs_Download.md#task_FA78EB3B991C43F9ADE507A16522B770)
>>* [ Referencing the mbox.js File on Your Web Pages ](t_mboxjs_referencing_recs.md#task_69315D69881442209EB5CC8A5644CF37)
>>* [ Implementing Display Data Mboxes ](t_data_mboxes_implementings_recs.md#task_83C1EA8433C249E1AC4BBEF591AC4FC3)
>>* [ Implementing an Order-Confirmation Details Mbox ](t_mbox_orderconfirm_implementing_recs.md#task_AC372C1B9DFC4F5FB9DB4BDC759343EA)
>>* [ Placing Mboxes to Display Recommendations ](t_mbox_placing_recs.md)
