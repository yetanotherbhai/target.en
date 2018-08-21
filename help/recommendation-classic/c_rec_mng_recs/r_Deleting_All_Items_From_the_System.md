---
description: You can use the Catalog Delete API to remove all items in your catalog.
seo-description: You can use the Catalog Delete API to remove all items in your catalog.
seo-title: Deleting All Items From the System
solution: Target
title: Deleting All Items From the System
topic: Recommendations
uuid: 3d6eea5f-34b9-4306-8d87-a29eb63d7c43
index: y
internal: n
snippet: y
translate: y
---

# Deleting All Items From the System


>The Catalog Delete API removes all entity.attributes for all items in your catalog. It does not remove behavioral data associated with product IDs. When you upload your catalog again, your algorithm data will be correctly associated if your product IDs have not changed. 


>>[!NOTE]
>>
>>There is no undo for this API.
>


>The syntax for the Catalog Delete API is: 

>
>```
>https://recommendations.omniture.com/rest?action=entity.deleteAll&client=clientCode 
>&clientToken=76bde9de-74f7-434b-ad1a-6d2d4c1b42d9
>```


>Where: 

>**recommendations.omniture.com** is the domain for the current recommendations environment you are using. 

>**clientCode** is your client code. 

>**76bde9de-74f7-434b-ad1a-6d2d4c1b42d9** is the client token that is obtained from the settings page. The token shown is a sample; yours will be different. 
>[!MORE_LIKE_THIS]
>
>* [ Adobe Recommendations Home ](recs_home.md#topic_74F655D8648E4586BCCFD789E60D13CE)
>* [ Getting Started ](c_gettingstarted_recs.md#concept_CCF04F19782145099178353D37517D9E)
>* [ Managing Your Recommendations ](c_rec_mng_recs.md#concept_8BD886F4E0954B46B8EC0EA4626A00E1)
>* [ Managing Templates ](c_Managing_Templates.md#concept_C3A712A99D47406C855955161DB699A1)
>* [ Managing Recommendations Settings ](c_Managing_Recommendations_Settings.md#concept_70257C38F0A74F3E88B1E7ED278A8DB4)
>* [ Managing Mboxes ](c_Managing_Mboxes.md#concept_B2EE9F6FDDD74A5AAAE6D14C263BCDEB)
>* [ Using the Recommendations Download API ](r_Using_the_Recommendations_Download_API.md#reference_09DA9D1AB3884CEC9144C7BDD07AB30A)
>* [ Deleting an Item From the System ](r_Deleting_an_Item_From_the_System.md#reference_9D644188516045E295DD69065118ED2D)
>* [ Integrating Recommendations with Email ](r_Integrating_Recommendations_with_Email.md#reference_256B16C894864F24AF970E43DC174420)
>* [ Recommendations FAQ ](r_Recommendations_FAQ.md#reference_72906D385558428C8190721E2E437855)
