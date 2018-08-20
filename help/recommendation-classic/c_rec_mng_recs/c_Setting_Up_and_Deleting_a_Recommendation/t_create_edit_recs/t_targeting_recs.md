---
description: Entry conditions help to determine who sees the recommendation when they visit your site.
seo-description: Entry conditions help to determine who sees the recommendation when they visit your site.
seo-title: Configuring Entry Conditions
solution: Target
title: Configuring Entry Conditions
topic: Recommendations
uuid: 11530ee3-2399-4612-a69a-765d44d02219
index: y
internal: n
snippet: y
translate: y
---

# Configuring Entry Conditions

To help you determine who sees your recommendation, configure entry conditions. Entry conditions are based on segments, as explained in [ Defining Segments](../../../c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_definesegments_recs.md#task_338EDF86E0A2412896C2854257E91D62). Entry conditions provide the first level of targeting for your recommendations. A visitor must meet the entry conditions before the recommendation is displayed. 

>1. Create a new recommendation, or locate the existing recommendation you want to target and click **[!UICONTROL  Edit]**.
>1. Under [!UICONTROL  Configuration], select the desired entry condition.

>       The available options are: 

>       **[!UICONTROL  Everyone:]** All visitors to your site. 

>       **[!UICONTROL  People who have purchased before:]** Any visitor who has bought an item from your site. 

>       **[!UICONTROL  People who have spent...:]** People who have spent more than or less than a specified amount. When you select this target, additional options appear that let you select whether the target amount is less than or more than a specified amount. 

>       **[!UICONTROL  First time visitor:]** People who have not visited your site before. Note that, if cookies have been deleted, a return visitor appears as a first time visitor. 

>       **[!UICONTROL  Returning visitor:]** People who have been to your site before. 

>       **[!UICONTROL  Custom profile attribute:]** (For Adobe targeting users only.) People who have a particular profile value as defined in Target. When you select this option, additional parameters appear. In the first box, type the name of an in-mbox profile parameter, or a script profile parameter. (More information about these parameters is available in the Target help.) Next, select a delimiter from the menu, then type the value that must be met for the recommendation to show. 

>       For in-mbox profile parameters, type `profile. *` attributeName`*` in the text box. For script profile parameters, type `user. *` attributeName`*`. `Replace *` attributeName`*` with the name of the attribute. 
>1. Set or change the remaining options for the recommendation as desired.
>1. Click **[!UICONTROL  Save]**.
>[!MORE_LIKE_THIS]* [ Adding a New Recommendation ](c_Creating_a_New_Recommendation.md#concept_9F20B4F0F53D4399B10BCBBC979E0B4C)* [ Choosing a Test Type ](t_choosetype_recs.md#task_301A771BFE7F45A3AA1E77024E574D1C)* [ Choosing a Catalog ](t_Choose_a_Catalog.md#task_047A4BA38078464782024764CA38EF0A)* [ Basing the Recommendation on a Recommendation Key ](t_rec_key_recs.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B)* [ Selecting an Algorithm ](t_algo_select_recs.md#task_2203616ABBE342B6ADAB08F278D794FA)* [ Choosing the Data Source ](t_data_source_recs.md#task_4EC990FBF374465EA6B7FCA8A5A12786)* [ Setting Data Details ](t_Setting_Data_Details.md#task_28DB20F968B1451481D8E51BAF947079)* [ Selecting a Template and Recommendation Area ](t_template_and_recommendation_area_recs.md#task_45CA0403F24944EF9FE6C4FC5D1A7836)* [ Defining Segments ](t_definesegments_recs.md#task_338EDF86E0A2412896C2854257E91D62)* [ Specifying How Many Users See Default Content ](t_how_many_users_see_default_conten_recst.md#task_5059665F6EE64FA39D2851671898F996)