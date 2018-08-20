---
description: Several options help you narrow the items that display in your recommendations.
seo-description: Several options help you narrow the items that display in your recommendations.
seo-title: Setting Data Details
solution: Target
title: Setting Data Details
topic: Recommendations
uuid: 5ec4293f-fc88-4ebc-995b-1df58db0cbb9
index: y
internal: n
snippet: y
translate: y
---

# Setting Data Details

The data details are optional. However, setting these details gives you more control over the items that display in your recommendation. Each detail you configure further narrows the display criteria. For example, you can choose to display only women's shoes that have an inventory above 50 and a price between $25 and $45. You can also weight each attribute so those items that are more important to your business are most likely to display. 

>1. Specify the period for which data should be used when calculating recommendations.

>       This helps you target recommendations based on recent activity over a specified time period. Set the time period to provide enough data for a valid recommendation, but not so much data that the recommendation is out of date. 
>1. To access the data detail options, create or edit a recommendation, then click ` Show More` in the ` Data Details` section under ` Define Your Algorithm`.

>       The ` Data Details` section is not available until you choose an algorithm 
>1. Set the minimum inventory amount for the products you want to recommend.

>1. Set a price range for the products you want to recommend.

>1. Configure the recommendation to display items only when they meet certain criteria.

>       You can specify that items are included only when one of the following attributes meets or does not match one or more specified conditions: 

>    
>    * ID
>    * Category
>    * Name
>    * Message
>    * Margin
>    * Value
>    * Inventory
>    * Brand


>       You can set more than one value for each attribute. Separate each value with a comma. 


>       >[!NOTE]
>       >
>       >If you select **[!UICONTROL  Inventory]** but an Inventory value is not passed, that control on the recommendations setup page is ignored. In this case, use an "include only when" rule or a catalog to achieve your inventory control goal. 


>       In addition to the usual evaluators ( ` contains`, ` does not contain`, ` equals`, and so on), you can select one of the following options: 

>    
>    * ` Include Only When: Matches` The recommendation's attribute must match the key's attribute to display. 

>    * ` Include Only When: Does Not Match` The recommendation's attribute must not match the key's attribute to display. 

>    * ` Include Only When: Is Between` To display, a recommendation's attribute must fall within the range specified for the value, margin, or other numeric-based attribute. You might, for example, specify 50% and 200% if you want to display items that cost $25 to $100 when the user views a $50 item. This prevents the recommendation from displaying a $5000 dollar item when a $200 value item is being viewed, showing instead items that are more likely to interest the buyer. The lower limit is 0%. There is no upper limit. 



>       You can use multiple Include Only When filters to reduce the overhead of setting up many separate campaigns. Multiple filters are combined with an AND. 


>       >[!NOTE]
>       >
>       >This option limits the items that are displayed in the recommendation. It does not affect which pages the recommendation is displayed on. To limit where the recommendation displays, recommendation-level targeting is required.


>       Dynamic attribute filtering should be used sparingly. They are useful if, for example, your organization has rules that demand that one brand is not recommended while another brand is being shown. There is a cost to this feature. You could possibly lose a percentage of lift by restricting some items from not showing when they would normally be shown by the algorithm. 
>1. If desired, [ weight attributes](../../../c_rec_mng_recs/c_Creating_a_Custom_Algorithm/r_Recommendation_Parameters.md#reference_93CA52A6B7D64CDFABAE37E27D1F0A9F) so they are more or less likely to show.

>       Select an attribute, then enter one or more values for that attribute (separated by a comma), then use the slider to set the weight for that weighting. 

>       To add another weighting, click ` Add Weighting` and set the attribute, values, and weight. You can set as many weightings as you need. 
>1. Click ` Save`.

>[!MORE_LIKE_THIS] {class="- topic/related-links "}
>
>* [ Adding a New Recommendation ](c_Creating_a_New_Recommendation.md#concept_9F20B4F0F53D4399B10BCBBC979E0B4C)
>* [ Targeting a Recommendation ](t_targeting_recs.md#task_3D93B8962F6341CB9A3ADE8E29BFECA5)
>* [ Choosing a Test Type ](t_choosetype_recs.md#task_301A771BFE7F45A3AA1E77024E574D1C)
>* [ Choosing a Catalog ](t_Choose_a_Catalog.md#task_047A4BA38078464782024764CA38EF0A)
>* [ Basing the Recommendation on a Recommendation Key ](t_rec_key_recs.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B)
>* [ Selecting an Algorithm ](t_algo_select_recs.md#task_2203616ABBE342B6ADAB08F278D794FA)
>* [ Choosing the Data Source ](t_data_source_recs.md#task_4EC990FBF374465EA6B7FCA8A5A12786)
>* [ Selecting a Template and Recommendation Area ](t_template_and_recommendation_area_recs.md#task_45CA0403F24944EF9FE6C4FC5D1A7836)
>* [ Defining Segments ](t_definesegments_recs.md#task_338EDF86E0A2412896C2854257E91D62)
>* [ Specifying How Many Users See Default Content ](t_how_many_users_see_default_conten_recst.md#task_5059665F6EE64FA39D2851671898F996)
