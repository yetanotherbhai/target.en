---
description: Criteria control the content of your Recommendations activities. Create criteria to show the recommendations that are most appropriate for your activity.
keywords: creating criteria;algorithms;criteria;recommendations criteria
seo-description: Criteria control the content of your Recommendations activities. Create criteria to show the recommendations that are most appropriate for your activity.
seo-title: Creating Criteria
solution: Target
title: Creating Criteria
topic: Premium
uuid: cb8c4558-1450-4894-b8a0-0e5365880a26
index: y
internal: n
snippet: y
translate: y
---

# Creating Criteria

There are multiple ways to reach the `Create New Criteria` screen. Some screen options vary depending on how you reach the screen. 

* When you are creating a `Recommendations` activity, click ** `Create New` ** on the `Select Criteria` screen. You will have the option to save your new criteria for use with other `Recommendations` activities. 

* When you are editing a `Recommendations` activity, click in a `Recommendations Location` box on your page, and select ** `Change Criteria` **. On the `Select Criteria` screen, click ** `Create New` **. You will have the option to save your new criteria for use with other `Recommendations` activities. 

* On the ** `Recommendations` ** > ** `Criteria` ** library screen, click ** `Create Criteria` **. Criteria you create here are automatically made available for all `Recommendations` activities. 



>1. Click ** `Create Criteria` ** or ** `Create New` **.

>       ![](graphics/button_CreateCriteria.png) 
>1. Select ** `Create Criteria` **.

>       ![](graphics/CreateNewCriteria_full.png) 
>1. Type a ** `Criteria Name` **.

>       This is the "internal" name used to describe the criteria. For example, you might want to call your criteria "Highest margin products," but you don't want that title to display publicly. See the next step to set the public-facing title.
>1. Type a public-facing ** `Display Title` ** to appear on the page for any Recommendations that use this criteria.

>       For example, you might want to display "People who viewed this viewed that" or "Similar products" when you use this criteria to show recommendations.
>1. Type a short ** `Description` ** of the criteria.

>       The description should help you identify the criteria, and might include information about the purpose of the criteria.
>1. Select an ** `Industry Vertical` **.

>       Other criteria options will change based on the industry vertical you select.
>1. Select a ** `Page Type` **.

>       You can select multiple page types.
>       Together, the industry vertical and page types are used to categorize your saved criteria, making it easier to reuse criteria for other `Recommendations` activities. 
>1. Select a ** `Recommendation Key` **.

>       For more information about basing criteria on a key, see [Base the Recommendation on a Recommendation Key](t_rec_key_recs.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B). 
>1. Select the ** `Recommendation Logic` **.

>       For more information about recommendation logic options, see [Criteria](c_algorithms.md#concept_4BD01DC437F543C0A13621C93A302750). 

>       >[!NOTE]
>       >
>       >If you select ** `Items` **/ ** `Media with Similar Attributes` **, you will have the option to set [content similarity rules](c_content_similarity.md#concept_5402DAFA279C4E46A9A449526889A0CB). 
>1. Set the ** `Data Range` ** to determine the time range of available historical user behavior data to use when determining which recommendations to show.

>       If your site has a lot of traffic and behaviors change frequently, choose a shorter data window. A shorter window enables `Recommendations` to be more responsive to changes in the market and in your business. For example, a shorter window means that `Recommendations` will detect changes in visitor behavior as your visitors begin seasonal shopping, such as back-to-school shopping or Christmas, and will recommend items appropriate to those shopping seasons. 
>       If you don't have a lot of data, or visitor behavior does not change frequently, you might select a longer window. However, for many sites, a shorter window results in better recommendations.
>       The available data ranges are:
>    
>    * Two days
>    * One week
>    * Two weeks
>    * One month
>    * Two months

>1. Select the desired ** `Behavioral Data Source` **: `mboxes` or `Analytics`.

>       If you chose `Analytics`, select the desired report suite. 
>1. Set your ** `Content` ** rules.

>       Content rules determine what happens if the number of recommended items does not fill your design. For example, if your design has space for five items, but your criteria causes only three items to be recommended, you can leave the remaining space empty, or you can use backup recommendations to fill the extra space.
>       Select the appropriate toggles:
>    
>    * `Enable Partial Design Rendering` 

>    * `Show Backup Recommendations` 

>    * `Recommend Previously Purchased Items` 
>      This setting is based on the `productPurchasedId`. It is useful if you sell items that people typically purchase only once, such as kayaks. If you sell items that people come back to purchase again, such as shampoo or other personal items, you should disable this option. 


>1. Set your ** `Inclusion Rules` **.

>       Inclusion rules determine which items will be included in your recommendations. The options available depend on your industry vertical.
>       For more details, see [Inclusion Rules](t_data_details.md#task_28DB20F968B1451481D8E51BAF947079). 
>1. Configure ** `Attribute Weighting` **.

>       You can add multiple rules to "nudge" the algorithm based on important description or metadata about the content catalog. For example, you can apply a higher weighting to on-sale items so they appear more often in the recommendation.
>       See [Attribute Weighting](t_attribute_weighting.md#task_2AEDA0DB15B74770B76F6982B24C2E42). 
>1. When finished, click ** `Save` **.

>       If you are creating a new `Recommendations` activity or editing an existing one, the ** `Save criteria for later` ** check box is selected by default. If you do not want to use the criteria in other activities, clear the check box before saving. 
