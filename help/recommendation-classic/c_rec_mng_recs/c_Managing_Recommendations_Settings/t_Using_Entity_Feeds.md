---
description: Entity feeds enable more ways to get product or content information into your recommendations. Item details can be sent from SAINT product classifications or using the Google Product Search feed format.
seo-description: Entity feeds enable more ways to get product or content information into your recommendations. Item details can be sent from SAINT product classifications or using the Google Product Search feed format.
seo-title: Using Entity Feeds
solution: Target
title: Using Entity Feeds
topic: Recommendations
uuid: 8ca1f5f8-ce76-4f8d-9d05-44095baa080e
index: y
internal: n
snippet: y
translate: y
---

# Using Entity Feeds

This allows you to bypass complex mbox implementation or augment your mbox data with information that is either unavailable on the page or unsafe to send directly from the page (like margin, COGS, etc.). 

You can select which columns from your SAINT product classifications file or Google Product Search file you want to send to the recommendations server. These pieces of data about each item can then be used in template display and for controlling recommendations. 

If data is collected by both an entity feed and an mbox, the most recent data wins. Usually, the most recent data comes from an mbox, because it is viewed more often. In the rare event that entity feed data and mbox data hit at the same time, the mbox data is used. 

**Google** 


>[!IMPORTANT]
>
>The Google Product Search feed type uses the Google format. This is different from the Adobe proprietary csv upload format.




>[!NOTE]
>
>It is not required to use Google data. Recommendations just uses the same format as Google. You can use this method to upload any data you have, and use the available scheduling features. However, you must retain the predefined attribute names defined by Google when you set up the file.



Most retailers upload products to Google, so when a visitor uses Google product search their products will show up. [!DNL  Recommendations] follows Google's specification exactly for entity feeds. Entity feeds can be sent to [!DNL  Recommendations] via XML, .txt, or .tsv and can use the attributes defined by Google here: [ http://support.google.com/merchants/bin/answer.py?hl=en&amp;amp;answer=188494&amp;amp;topic=2473824&amp;amp;ctx=topic#US ](http://support.google.com/merchants/bin/answer.py?hl=en&answer=188494&topic=2473824&ctx=topic#US). The results are searchable when a visitor goes here: [ http://www.google.com/prdhp ](http://www.google.com/prdhp). 


>[!NOTE]
>
>The POST method must be allowed on the server that is hosting the Google feed content.



Because Recommendations users already configure XML or .txt feeds to send to Google either via URL or FTP, entity feeds accept that product data and use it to build out the recommendations catalog. Specify where that feed exists and the recommendations server retrieves the data. 

If you use Google Product Search for the entity feed upload, you still need to have a product page mbox on the page if you want to show recommendations there or track product views for algorithm delivery based on views. 

The feed runs at the time you save and activate it. It runs at the time you save the feed, then every day an hour later. 

**SAINT** 

The SAINT Product classification is the only classification available for recommendations. For more information about this classification file, see the [ SAINT Classifications User Guide ](https://marketing.adobe.com/resources/help/en_US/sc/saint/oms_sc_saint.pdf). It's possible that not all the information you need for recommendations will be available in your current SAINT implementation, so follow this user guide if you want to add to your classifications file. 

**Adding Entity Feeds** 

To add entity feeds to recommendations, follow these steps: 

>1. Click ` Products`, then click the ` Feeds &amp; Uploads` tab.
>1. Click ` Add Entity Feed`.

>       The ` Edit Feed form` opens. 
>1. Enter a name for the feed, then select ` SiteCatalyst SAINT`from the ` Feed Type` dropdown.

>       If you are a retailer who uses Google Product Search, you can select ` Google Product Search` to map your recommendation entities to the parameters you already send to Google. In this case the following steps are essentially the same, except you also select a file location type (URL or FTP) and specify the URL or FTP information. 
>1. Select a report suite, then select ` Product` from the ` Classification` dropdown.

>1. Select a feed field.

>       The feed field is the classification field you want to map to recommendations. The value in this field for each product will be passed to the recommendations. 
>1. Select the recommendation entity attribute you want to map to the selected classification field.

>       Select ` New Custom Attribute` to add a new recommendation entity attribute if an applicable one is not already listed. 
>1. Click ` Add Mapping` to create additional mappings.

>       It is not necessary to map all of your entity attributes. Create a mapping only for those attributes you need to map. 


>       >[!NOTE] {class="- topic/note "}
>       >
>       >You must map a value from SAINT or Google Product Search to the "id" attribute in recommendations. This is how it is known which product recommendations to assign these new values to.

>1. If you want to specify how frequently the feeds are updated, click the ` Schedule` tab, then select the desired upload frequency.

>       Selecting ` never` is the same as pausing the feed from running. 
>1. Click ` Save`.

>       After you click ` Save`, the status displays under the [!UICONTROL  Schedule] tab. Open an entity feed by clicking ` Edit` to see your status updates. 
>[!MORE_LIKE_THIS] {class="- topic/related-links "}* [ Creating Global Exclusions ](t_Creating_Global_Exclusions.md#task_ABDA6F68D8BD47988A67A06396121318)* [ Uploading Entities to Recommendations ](c_Uploading_Entities_to_Recommendations.md#concept_23D55B1FAEBE425A8A0F9796A0E21AE1)