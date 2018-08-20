---
description: Exclusions let you specify that a product or item never be included in your recommendations if they meet specific criteria. Multiple global exclusions are combined using "Or" logic.
seo-description: Exclusions let you specify that a product or item never be included in your recommendations if they meet specific criteria. Multiple global exclusions are combined using "Or" logic.
seo-title: Creating Global Exclusions
solution: Target
title: Creating Global Exclusions
topic: Recommendations
uuid: 4be9a980-b7ed-46ed-926a-bf981b48e2c4
index: y
internal: n
snippet: y
translate: y
---

# Creating Global Exclusions


>1. From the recommendations menu, select **[!UICONTROL  Settings]**.
>1. Click **[!UICONTROL  Exclusions]**, then click **[!UICONTROL  Add exclusion rule]**.
>1. Specify an entity parameter.

>       The possible parameters are: 



>    <table id="table_E2D07D0D266D4965BD4336D2A0FD062A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Parameter </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>category </p> </td> 
   <td colname="col2"> <p> The product category used to organize products on your site. A product can have multiple categories, but only one category can be entered in this field. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entityid </p> </td> 
   <td colname="col2"> <p> The number used to identify the product. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p> The product name that is displayed on the Web site when the product is recommended. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>thumbnailUrl </p> </td> 
   <td colname="col2"> <p> The absolute URL that points to the thumbnail image of the product that is displayed in the recommendation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageUrl </p> </td> 
   <td colname="col2"> <p> The URL of the product page displayed in the recommendation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>message </p> </td> 
   <td colname="col2"> <p> A message about the product that is displayed in the recommendation. The message is typically more verbose than the product name. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p> The price or value of the product. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>margin </p> </td> 
   <td colname="col2"> <p> The profit margin or other value of the item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>inventory </p> </td> 
   <td colname="col2"> <p> The current amount of the product in inventory. </p> <p> <p>Note:  If you don't pass a value for the inventory parameter, the inventory control on the setup page is ignored. If you choose to use a custom parameter for inventory, use an "include only when" rule or a catalog to achieve your inventory control goal. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom attributes </p> </td> 
   <td colname="col2"> <p> You can include up to 100 custom attributes that provide additional information about your products. You can specify any unused attribute name for each custom attribute. For example, you might create a custom attribute called brand that specifies the brand name of the product. </p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Specify the string that must be matched for the exclusion to be used.
>1. Click **[!UICONTROL  Save]**.
>[!MORE_LIKE_THIS]
>
>* [ Uploading Entities to Recommendations ](c_Uploading_Entities_to_Recommendations.md#concept_23D55B1FAEBE425A8A0F9796A0E21AE1)
>* [ Using Entity Feeds ](t_Using_Entity_Feeds.md#task_4034B221DC754633B1280893AE6B5F86)
