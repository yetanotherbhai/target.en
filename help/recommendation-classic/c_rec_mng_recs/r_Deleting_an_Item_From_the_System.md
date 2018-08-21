---
description: You can use the Catalog Item Delete API to remove a single item from your Recommendations system.
seo-description: You can use the Catalog Item Delete API to remove a single item from your Recommendations system.
seo-title: Deleting an Item From the System
solution: Target
title: Deleting an Item From the System
topic: Recommendations
uuid: b782f643-6314-491f-8555-8c022ac96264
index: y
internal: n
snippet: y
translate: y
---

# Deleting an Item From the System


>This API deletes all information about an individual entity. Once the cache is updated after a few hours, the entity no longer shows in any recommendations. These entities will be eligible to be "relearned" through a ` productPage` mbox request or a CSV product upload. 


>>[!NOTE]
>>
>>There is no undo for this API.
>


>The syntax for the Catalog Item Delete API is: 

>
>```
>https://recommendations.omniture.com/rest?action=entity.delete&amp;client=clientCode&amp;clientToken=76bde9de-74f7-434b-ad1a-6d2d4c1b42d9&amp;entityIds=Entity_ID
>```


>Where: 

>**recommendations.omniture.com** is the domain for the current recommendations environment you are using. 

>**clientCode** is your client code. 

>**76bde9de-74f7-434b-ad1a-6d2d4c1b42d9** is the client token that is displayed on the settings page. The token shown is a sample; yours will be different. 

>**Entity_ID** is the ID of the item you want to delete. You can delete multiple items by including multiple ` entityId` values separated by comma. 
>[!MORE_LIKE_THIS]
>
>* [ Adobe Recommendations Home ](recs_home.md#topic_74F655D8648E4586BCCFD789E60D13CE)
>* [ Getting Started ](c_gettingstarted_recs.md#concept_CCF04F19782145099178353D37517D9E)
>* [ Managing Your Recommendations ](c_rec_mng_recs.md#concept_8BD886F4E0954B46B8EC0EA4626A00E1)
>* [ Managing Templates ](c_Managing_Templates.md#concept_C3A712A99D47406C855955161DB699A1)
>* [ Managing Recommendations Settings ](c_Managing_Recommendations_Settings.md#concept_70257C38F0A74F3E88B1E7ED278A8DB4)
>* [ Managing Mboxes ](c_Managing_Mboxes.md#concept_B2EE9F6FDDD74A5AAAE6D14C263BCDEB)
>* [ Using the Recommendations Download API ](r_Using_the_Recommendations_Download_API.md#reference_09DA9D1AB3884CEC9144C7BDD07AB30A)
>* [ Deleting All Items From the System ](r_Deleting_All_Items_From_the_System.md#reference_A916F48DE01E41DA81F2C35AF2A5E58F)
>* [ Integrating Recommendations with Email ](r_Integrating_Recommendations_with_Email.md#reference_256B16C894864F24AF970E43DC174420)
>* [ Recommendations FAQ ](r_Recommendations_FAQ.md#reference_72906D385558428C8190721E2E437855)
