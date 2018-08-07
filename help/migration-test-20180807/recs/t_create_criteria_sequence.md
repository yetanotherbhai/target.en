---
description: Use sequences of up to five criteria to exercise greater control of the items that appear in your Recommendations activities.
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria
seo-description: Use sequences of up to five criteria to exercise greater control of the items that appear in your Recommendations activities.
seo-title: Creating Criteria Sequences
solution: Target
title: Creating Criteria Sequences
topic: Premium
uuid: e8ed3c9e-e151-43bf-ab55-6cab545f2ef8
index: y
internal: n
snippet: y
translate: y
---

# Creating Criteria Sequences


>[!NOTE]
>
>Criteria sequences cannot be used with `Recommendations` activities created before the October 2016 Release of `Target Premium`. 


To create a criteria sequence, you must first create the criteria you want to include in the sequence. See [Creating Criteria](t_create_new_algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) for more information. 
By using a criteria sequence, you can provide additional targeted recommendations, instead of using more generic backup recommendations, when a criteria doesn't return enough results to fill your design. Typically, a criteria sequence will proceed from more specific targeting, which may return fewer results, to more general targeting, which usually returns more results.
For example, a product page criteria sequence might follow this order:

1. Based on current item, from same brand

1. Based on current item, from all brands

1. Based on content similarity

1. Based on top sellers

1. Based on most-viewed items across the site


A home page criteria sequence might follow this order:

1. Based on visitor's last purchase

1. Based on visitor's favorite item

1. Based on visitor's favorite category

1. Based on top sellers

1. Based on most-viewed across site


There are multiple ways to reach the `Create Criteria Sequence` screen. Some screen options vary depending on how you reach the screen. 

* When you are creating a `Recommendations` activity, click ** `Create New` ** > ** `Create Criteria Sequence` ** on the `Select Criteria` screen. You will have the option to save your new criteria sequence for use with other `Recommendations` activities. 

* When you are editing a `Recommendations` activity, click in a `Recommendations Location` box on your page, and select ** `Change Criteria` **. On the `Select Criteria` screen, click ** `Create New` ** > ** `Create Criteria Sequence` **. You will have the option to save your new criteria for use with other `Recommendations` activities. 

* On the ** `Recommendations` ** > ** `Criteria` ** library screen, click ** `Create Criteria` ** > ** `Create Criteria Sequence` **. Criteria you create here are automatically made available for all `Recommendations` activities. 



>1. Click ** `Create Criteria` ** or ** `Create New` **.

>       ![](graphics/button_CreateCriteria.png) 
>1. Select ** `Create Criteria Sequence` **.

>       ![](graphics/CreateCriteriaSequence.png) 
>1. Type a ** `Name` ** for the sequence.

>       This is the "internal" name used to describe the criteria sequence. Visitors to your site will not see this name.
>1. Type a public-facing ** `Generic Display Title` ** to appear on the page if multiple criteria in the sequence are used to fill the `Recommendations` design.

>       For example, you might want to replace "Customers who viewed this also viewed..." with "Recommended for You" if the design might include items based on more than one `Recommendations` key. 
>1. Type a short ** `Description` ** of the criteria sequence.

>       The description should help you identify the criteria sequence, and might include information about its purpose.
>1. Select an ** `Industry Vertical` **.

>       Your default industry vertical appears automatically.
>1. Select a ** `Page Type` **.

>       You can select multiple page types.
>       Together, the industry vertical and page types are used to categorize your saved criteria sequence, making it easier to reuse sequences for other `Recommendations` activities. 
>1. Set your ** `Content` ** rules.

>       When you create a criteria sequence, backup recommendation and partial design rendering settings are ignored for the individual criteria the make up the sequence. To use backup recommendations and partial design rendering you must enable them for the sequence. Select the appropriate toggles. If you choose to allow backup recommendations, you can also choose whether to apply inclusion rules to the backups.
>1. Set the sequence order.

>    
>    1. Click ** `Add Criteria` **. 

>    1. On the Add Criteria screen, select a criteria.

>    1. Click ** `Add` **. 

>       You can add up to five criteria to a sequence.
>1. Click ** `Save` **.

>       ![](graphics/CriteriaSequenceCard.png) 
>       For more information about recommendation logic options, see [Criteria](c_algorithms.md#concept_4BD01DC437F543C0A13621C93A302750). 
