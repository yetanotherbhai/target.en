---
description: Add promoted items and control their placement in your Recommendations designs. You can add static and dynamic promotions.
keywords: promotions;front promotions;back promotions;promotions type
seo-description: Add promoted items and control their placement in your Recommendations designs. You can add static and dynamic promotions.
seo-title: Adding Promotions
solution: Target
title: Adding Promotions
topic: Premium
uuid: 326ce67e-a3ec-4f56-9ecd-0cede0cdbc11
index: y
internal: n
snippet: y
translate: y
---

# Adding Promotions


>[!IMPORTANT]
>
>Static and dynamic exclusion rules are powerful features that can help you with your marketing efforts. For detailed information, examples, and use-case scenarios, see[Use Dynamic and Static Inclusion Rules](c_use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F). 


When you create a `Recommendations` activity, you have the option to include promoted items in your `Recommendations` design. Promotions use available slots in a design and take precedence over criteria results and backup recommendations. For example, if your design has six slots and you use two of them for promotions, four slots are available for items recommended based on criteria. 
You can promote specific items, dynamically promote items, promote items based on attributes, or promote collections.
![](graphics/add_promotion_toggles.png) 

>[!NOTE]
>
>Using promotions changes CSV structure and output. These changes could have an impact on any external processes that involve CSV, such as email.



>1. On the ** `Add Promotions` ** screen, click either the ** `Front Promotion` ** or ** `Back Promotion` ** toggle.

>       ![](graphics/add_promotion_front.png) 
>       You can insert promotions both before *and* after your criteria results. 
>1. Set the number of design slots to use for promoted items.

>       `Recommendations`1. Set a start date and end date for your promoted items.

>1. Select a ** `Promotion Type` **.

>    
>    * Select ** `List of items` ** and enter the `entity.id` values, separated by commas, of the specific items you want to promote. 
>      If your list includes more items than the number of slots you set for promotions, you can select the ** `Randomize item order` ** check box to vary the promoted items that are displayed in your design. 

>    * Select ** `Promote by attribute` ** and add rules to define the attributes of the items you want to promote. 
>      If you select Promote by Attribute, you can create dynamic matches. For more information, see [Use Dynamic and Static Inclusion Rules](c_use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F). 

>    * Select ** `Promote a collection` ** and choose the collection of items you want to promote. You can create new collections to use for promotions. See [Create a Collection](t_create_collection.md#task_1256DFF6842141FCAADD9E1428EF7F08) for more information. 

>1. Click ** `Save.` **.

>       Promotions are applied to all experiences in the activity.
