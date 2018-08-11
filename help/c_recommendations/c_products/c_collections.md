---
description: A collection is a set of products or items that are eligible for a recommendation.
keywords: collection;Targeting
seo-description: A collection is a set of products or items that are eligible for a recommendation.
seo-title: Collections
solution: Target
title: Collections
title_outputclass: premium
topic: Premium
uuid: ee9ede09-834f-4468-a202-ba0b215bd06a
badge: assets/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Collections

## Collections {#concept_671BEFFB997D4F1282665BF3CAC00AC5}
>A collection is a set of products or items that are eligible for a recommendation.Commonly, a collection is a set of similar or related items, such as a single product collection. However, you can group whichever items into a category that makes sense to your business, such as products in a certain price range or color, or items that are likely to be interesting in a particular geographical area. 

Use collections to organize your products in logical buckets. For example, if some items are available in one region but not another, you might want to create a collection that excludes items that are unavailable in the visitor's region. You can also use collections to organize seasonal items, or any other organizational parameters that apply to your business. 

The backup recommendations generated for each criteria within the recommendation also uses this collection, so only items in the collection are included in the backup recommendation. With collections, you can be sure that only products that make sense to show in a location are displayed. 

Collections are rebuilt or updated every time each criteria runs. 

You can group your items into catalogs, then create separate recommendations for each collection. 

Inclusion criteria allow you to do similar things as a collection, but they must be set up every time you create an activity. Collections allow you to create a set of items one time, then use it whenever it is appropriate to do so without having to set it up again. 

When you are creating or editing a [!DNL  Recommendations] activity, the collection name appears next to the [!UICONTROL  Criteria] label on the activity diagram. 


>[!NOTE]
>
>Collections are not applied when using the [!UICONTROL  Recently Viewed Items] recommendation key. 


>## Create a Collection {#task_1256DFF6842141FCAADD9E1428EF7F08}
>Create a collection to organize the products you want to show in your recommendations. 
<draft-comment otherprops="merge">
  recs/t_create_collection.xml 
</draft-comment>
>1. Click ** [!UICONTROL  Recommendations] ** > ** [!UICONTROL  Collections] **.
>1. Click ** [!UICONTROL  Create Collection] **.

>       ![Step Result](../../assets/CreateCollection.png) 
>1. Type a ** [!UICONTROL  Name] ** for the collection.

>       You can also enter an optional ** [!UICONTROL  Description] **. 
>1. Set the rules used to build the collection.

>       For example, your collection might be built around a product ID or category, margin, or any other parameter in the list. 

>       You can add rules to use multiple parameters to define a collection. Multiple rules are joined with an AND. All specified rules must be matched for the collection to apply. 
>1. Click ** [!UICONTROL  Save] **.
