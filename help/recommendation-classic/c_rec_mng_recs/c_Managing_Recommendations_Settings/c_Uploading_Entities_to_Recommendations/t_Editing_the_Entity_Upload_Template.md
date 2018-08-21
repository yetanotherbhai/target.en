---
description: After you have downloaded the entity upload template, you can edit it.
seo-description: After you have downloaded the entity upload template, you can edit it.
seo-title: Editing the Entity Upload Template
solution: Target
title: Editing the Entity Upload Template
topic: Recommendations
uuid: 7e2c6003-8221-40ed-9bf1-6fed1ca823b9
index: y
internal: n
snippet: y
translate: y
---

# Editing the Entity Upload Template


>1. Open the upload template file in Excel or a text editor.
>1. Make the desired changes.

>       For example, you could fill out this file with ` productId` and inventory information, and leave the other fields blank. 

>       Entity upload data uses the form ` entity.attribute`. For example, if you sell athletic shoes, the entity is the Air Jordan Show and an attribute could be the $120 price for that shoe. 

>       Unless otherwise noted, there is a 100-character limit for entity attribute parameters. In some cases, more than 100 characters might be possible, but only 100 characters are supported. You can have up to 80 entity attributes per product. 

>       The possible parameters are: 



>    <table id="table_C3639611BB9E405EA485ECFE77557511"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>entity.id </p> </td> 
   <td colname="col2"> <p>The number used to identify the product. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entity.name </p> </td> 
   <td colname="col2"> <p>The product name that is displayed on the Web site when the product is recommended. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entity.categoryId </p> </td> 
   <td colname="col2"> <p>The product category used to organize products on your site. A product can have multiple categories, but only one category can be entered in this field. There is a 250-character limit for <span class="codeph"> categoryId</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entity.message </p> </td> 
   <td colname="col2"> <p>A message about the product that is displayed in the recommendation. The message is typically more verbose than the product name. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entity.thumbnailURL </p> </td> 
   <td colname="col2"> <p>The absolute URL that points to the thumbnail image of the product that is displayed in the recommendation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entity.value </p> </td> 
   <td colname="col2"> <p>The price or value of the product. Do not include the currency sign, for example the dollar sign ( $ ). The currency sign is not supported. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entity.pageURL </p> </td> 
   <td colname="col2"> <p>The URL of the product page displayed in the recommendation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entity.inventory </p> </td> 
   <td colname="col2"> <p>The current amount of the product in inventory. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>entity.margin </p> </td> 
   <td colname="col2"> <p>The profit margin or other value of the item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom attributes </p> </td> 
   <td colname="col2"> <p>You can include up to 100 custom attributes that provide additional information about your products. You can specify any unused attribute name for each custom attribute. For example, you might create a custom attribute called <span class="codeph"> entity.brand</span> that specifies the brand name of the product. </p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Save the file.
>[!MORE_LIKE_THIS]
>
>* [ Downloading the Entity Upload Template ](t_Downloading_the_Entity_Upload_Template.md#task_9889EEB9FCA64C8683255DD040939DCA)
>* [ Uploading the Entity Information to Recommendations ](t_Uploading_the_Entity_Information_to_Recommendations.md#task_F2A90148A36F4D0B99B7FAC612061925)
