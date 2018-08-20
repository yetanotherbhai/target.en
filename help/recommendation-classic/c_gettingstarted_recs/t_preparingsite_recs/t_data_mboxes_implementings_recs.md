---
description: Display data mboxes send updated catalog data for recommendations, and display product recommendations.
seo-description: Display data mboxes send updated catalog data for recommendations, and display product recommendations.
seo-title: Implementing Display Data Mboxes
solution: Target
title: Implementing Display Data Mboxes
topic: Recommendations
uuid: b27b5dbc-cf27-4603-9c57-4a0590fe13d7
index: y
internal: n
snippet: y
translate: y
---

# Implementing Display Data Mboxes

Display data mboxes have two purposes: 


* Show recommendations, like any other mbox
* Send dynamic catalog data to the recommendations server


Sending updated catalog data ensures that the recommendations displayed on your site always include the most updated information about your products. Display data mboxes make an offline catalog import strategy unnecessary. 

The display data mbox sends the ` productId` or ` productPurchasedId` (referred to as ` entity.id` in the code) that is used in the algorithms. 


>[!NOTE]
>
>` entity.id` must match the ` productPurchasedId` sent to the order confirmation page and the ` productId` used in Adobe Analytics product reports). 



Each parameter can accept only one value. new values overwrite old values, except for the ` categoryId` parameter. The ` categoryId` parameter can accept a comma-delimited list of values for each category containing that product. There is a character limit of 250 for ` categoryId`. 

See [ Advanced Recommendations Options ](../../c_rec_mng_recs/c_Creating_a_Custom_Algorithm/r_Recommendation_Parameters.md#reference_93CA52A6B7D64CDFABAE37E27D1F0A9F) for more information on each of the attributes that can be passed. 

In general, the display information mbox might look like the following example. Change the details in bold to refer to your products. 


>[!NOTE]
>
>All entity parameter attributes are case sensitive.




```
<div class="mboxDefault"></div><script language="JavaScript1.2"> 
 
mboxCreate('productPage', 
 
'entity.id= 
<b>67833</b>', 
 
'entity.name= 
<b>GIANTS VS ROCKIES 5/12</b>', 
 
'entity.categoryId= 
<b>BASEBALL, GIANTS, SF BAY AREA</b>', 
 
'entity.pageURL= 
<b>../baseball/giants-tix/giantsvrockies5.12.2000-67833</b>', 
 
'entity.venue= 
<b>AT&amp;T PARK</b>', 
 
'entity.secondary= 
<b>ROCKIES</b>', 
 
'entity.thumbnailURL= 
<b>../baseball/giants-tix/giants-136px.gif</b>', 
 
'entity.message= 
<b>FAMILY SPECIAL</b>', 
 
'entity.value= 
<b>15.99</b>', 
 
'entity.inventory= 
<b>1</b>' 
 
); 
 
</script>
```



>[!NOTE]
>
>Relative URLs are preferred for ` pageURL` and ` thumbnailURL` rather than absolute URLs because recommendations receive data being sent from all environments on your site. Using relative URLs avoids hardcoded links to a staging or development server. 



The following table describes the available variables. 

<table id="table_2F24AB9862FE4D94BFD91F910F436BA9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Entity Attribute </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.id </span> </p> </td> 
   <td colname="col2"> <p>This required parameter identifies the product. This ID must be the same across all Adobe Marketing Cloud products that are used, including Analytics, for the various products to recognize the item and share data about it. </p> <p>You cannot use a comma in an entity ID, unless you escape it. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.id=67833' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.name </span> </p> </td> 
   <td colname="col2"> <p>Provides a name for the item. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.name=Giants&amp;nbsp;vs&amp;nbsp;Rockies&amp;nbsp;5/12' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.categoryId </span> </p> </td> 
   <td colname="col2"> <p> Category of the current page. This can include multiple categories, such as a cardigans sub-subsection (i.e. <span class="codeph"> womens </span>, <span class="codeph"> womens:sweaters </span>, <span class="codeph"> womens:sweaters:cardigans </span>). Multiple categories should be separated by commas. </p> <p> <span class="codeph"> categoryId </span>is limited to 250 characters. Multiple categories should be separated by commas. </p> <p> <p>Note:  To show a recommendation based on a category, only one <span class="codeph"> categoryId </span> can be passed into the mbox used to display that particular recommendation. </p> </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.categoryId=BASEBALL,&amp;nbsp;GIANTS,&amp;nbsp;SF&amp;nbsp;BAY&amp;nbsp;AREA', 
     </codeblock> </p> <p>For category-based Recommendations, a comma is used to separate category value. Any values separated by commas become categories. You can also define subcategories by using a different separator, such as a colon (:), to separate subcategories within the category value. </p> <p>For example, in the following code the Womens category is divided into several subcategories: </p> <p> 
     <codeblock>
       mboxCreate('mboxName', 
      &nbsp;&nbsp;'entity.id=343942-32', 
      &nbsp;&nbsp;'entity.categoryId= 
      &nbsp;&nbsp;&nbsp;&nbsp;Womens, 
      &nbsp;&nbsp;&nbsp;&nbsp;Womens:Outerwear, 
      &nbsp;&nbsp;&nbsp;&nbsp;Womens:Outerwear:Jackets, 
      &nbsp;&nbsp;&nbsp;&nbsp;Womens:Outerwear:Jackets:Parka, 
      &nbsp;&nbsp;&nbsp;&nbsp;Womens:Outerwear:Jackets:Caban’, 
      &nbsp;&nbsp;'entity.thumbnailUrl=...', 
      &nbsp;&nbsp;'entity.message=...', 
      ); 
       
     </codeblock> </p> <p> For the mbox delivery, the longest attribute name is used for the key. If there is a tie, the last attribute is used. In the example above, the category key is <span class="codeph"> Womens:Outerwear:Jackets:Caban </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.pageURL </span> </p> </td> 
   <td colname="col2"> <p>Defines the relative URL of the page where the item can be purchased. </p> <p>Example: </p> <p> 
     <codeblock> 
      'entity.pageURL=baseball/giants-tix/giantsvrockies5.12.2000-67833' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.thumbnailURL </span> </p> </td> 
   <td colname="col2"> <p>Defines the relative URL to the thumbnail image that displays with the item. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.thumbnailURL=baseball/giants-tix/giants-136px.gif' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.message </span> </p> </td> 
   <td colname="col2"> <p> Defines additional information to display with the product in the template, such as "on sale" or "clearance." </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.message=Family&amp;nbsp;special' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.inventory </span> </p> </td> 
   <td colname="col2"> <p>Displays the inventory level of the item. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.inventory=1' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.value </span> </p> </td> 
   <td colname="col2"> <p>Defines the price of the item. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.value=15.99' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity </span> <span class="varname"> &amp;lt;custom&amp;gt; </span> </p> </td> 
   <td colname="col2"> <p>Define up to 100 custom variables that provide additional information about the item. For example, a ticket vendor might create attributes for the venue where an event will take place or for a secondary performer, such as a visiting team in a sporting event or an opening act in a concert. </p> <p>Examples: </p> <p> 
     <codeblock>
       'entity.venue=AT&amp;amp;T&amp;nbsp;Park' 
     </codeblock> </p> <p> 
     <codeblock>
       'entity.secondary=Rockies' 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

If the mbox is on a product page, you can include both the product ID and category ID. The selected algorithm determines which displays. The product ID is used for affinity algorithms and the category ID is used for category algorithms. 










>[!MORE_LIKE_THIS]* [ Preparing Your Website for Recommendations ](t_preparingsite_recs.md#task_30B8C075A14B426F9042119553F750B8)* [ Downloading the mbox.js Library File ](t_mboxjs_dl_recs.md#task_6B577DD43FD346F7BC01962DAA822816)* [ Validating the mbox.js Download ](t_Validating_the_mboxjs_Download.md#task_FA78EB3B991C43F9ADE507A16522B770)* [ Referencing the mbox.js File on Your Web Pages ](t_mboxjs_referencing_recs.md#task_69315D69881442209EB5CC8A5644CF37)* [ Implementing an Order-Confirmation Details Mbox ](t_mbox_orderconfirm_implementing_recs.md#task_AC372C1B9DFC4F5FB9DB4BDC759343EA)* [ Placing Mboxes to Display Recommendations ](t_mbox_placing_recs.md#task_F3638B849C9B45F197DBE49791AE13A1)