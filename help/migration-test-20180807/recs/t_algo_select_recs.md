---
description: Select the criteria to use in your Recommendations activity.
keywords: recommendations;recommendations activity;criteria
seo-description: Select the criteria to use in your Recommendations activity.
seo-title: Select Criteria
solution: Target
title: Select Criteria
topic: Premium
uuid: 4eedc1c6-e4c7-47d8-8ec3-a530e7bad575
index: y
internal: n
snippet: y
translate: y
---

# Select Criteria

You can test multiple recommendation types against each other by adding more than one criteria.
If you select multiple criteria, traffic is split evenly between the selected criteria. For example, if you have selected two criteria and your activity is designed to display default content to 20% of activity entrants, then 40% of activity entrants will see the recommendations controlled by each criteria. There is no option to change the percentages for each criteria.

* To search for an existing criteria (for example, if many criteria cards display), type in the search field until the desired criteria appears, then select the criteria and click ** `Done` **. 
  Some criteria are supplied with `Recommendations`. You and your team can also create your own custom criteria. 

* To create a new criteria, click ** `Create New` **, then fill in the information for the new criteria. For information about creating new criteria, see [Create a New Criteria](t_create_new_algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE). 


>1. [Create a new recommendation](t_create_recs_activity.md#task_6874328773C64C44A73F0A130AD3F96F), or find the recommendation whose criteria you want to set and click `Edit`.
>1. Select an industry type and a page type.

>    
>    * **Industry Type:**The industry type is used to help categorize `Recommendations` criteria. To change your default industry vertical, click ** `Settings` ** and select your desired default ** `Industry Vertical` ** setting. 

>    * **Page Type:**The page type helps you categorize your recommendations. There are also built-in criteria that can be chosen for each page type. 

>    * **Compatible:**Show only those criteria where the selected page passes the required data. Not every criteria will run correctly on every page. The page or mbox needs to pass in `entity.id` or `entity.categoryId` for the current item/current category recommendations to be compatible. In general, it is best to show only compatible criteria. However, if you want incompatible criteria to be available for the activity, clear the ** `Compatible` ** check box. This option can be disabled or enabled in your `Target` `Preferences`. 


>1. Click `Add`.
