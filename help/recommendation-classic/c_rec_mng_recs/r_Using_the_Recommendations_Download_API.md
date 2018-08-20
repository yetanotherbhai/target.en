---
description: Use the recommendations download API to download your recommendations in a .CSV file that can be viewed in a spreadsheet or text editor. The .CSV file lists all recommendations for each product key.
seo-description: Use the recommendations download API to download your recommendations in a .CSV file that can be viewed in a spreadsheet or text editor. The .CSV file lists all recommendations for each product key.
seo-title: Using the Recommendations Download API
solution: Target
title: Using the Recommendations Download API
topic: Recommendations
uuid: eb4b93cf-0ea2-4dd7-984c-441605a18f7b
index: y
internal: n
snippet: y
translate: y
---

# Using the Recommendations Download API


>Every time you download recommendations results, all of the data is refreshed, not just the data that changed between when you last ran the algorithm and when you downloaded the results. 

>The algorithm server updates the recommendations every two to six hours. Changes are reflected immediately in the results of the download API. 

>This API is always available except during regularly scheduled maintenance windows, which occur on Thursday nights at 8 PM Pacific Time or later. 

>**API Structure** 

>The download API uses a simple structure in a REST call. For example: 

>
>```
>https://recommendations.omniture.com/rest?action=downloadRecommendations
>&id=43&clientKey=24be79b2-d631-4207-a435-c6d5dd11059a
>&client=clientcodehere
>```


>Where: 

>**Id** is the recommendation ID visible in the app. Find the ID by looking at the URL on the recommendation's Edit page. Use the id=XXX value, not the groupId value. 

>**clientKey** is the API token that can be viewed and changed on the Settings page of the recommendations application. 

>**clientcode** is displayed under the client API token on the Settings page. 

>If you provide an invalid client key or recommendation ID, the error "Client key or recommendation id invalid" is returned. 
>[!MORE_LIKE_THIS]* [ Adobe Recommendations Home ](recs_home.md#topic_74F655D8648E4586BCCFD789E60D13CE)* [ Getting Started ](c_gettingstarted_recs.md#concept_CCF04F19782145099178353D37517D9E)* [ Managing Your Recommendations ](c_rec_mng_recs.md#concept_8BD886F4E0954B46B8EC0EA4626A00E1)* [ Managing Templates ](c_Managing_Templates.md#concept_C3A712A99D47406C855955161DB699A1)* [ Managing Recommendations Settings ](c_Managing_Recommendations_Settings.md#concept_70257C38F0A74F3E88B1E7ED278A8DB4)* [ Managing Mboxes ](c_Managing_Mboxes.md#concept_B2EE9F6FDDD74A5AAAE6D14C263BCDEB)* [ Deleting an Item From the System ](r_Deleting_an_Item_From_the_System.md#reference_9D644188516045E295DD69065118ED2D)* [ Deleting All Items From the System ](r_Deleting_All_Items_From_the_System.md#reference_A916F48DE01E41DA81F2C35AF2A5E58F)* [ Integrating Recommendations with Email ](r_Integrating_Recommendations_with_Email.md#reference_256B16C894864F24AF970E43DC174420)* [ Recommendations FAQ ](r_Recommendations_FAQ.md#reference_72906D385558428C8190721E2E437855)