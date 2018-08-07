---
description: Use entity attributes to pass product or content information to Recommendations.
keywords: entity attributes;pass information to Recommendations;behavioral data;data counter;define relative URL;display inventory level;define price;define profit margin;custom attributes
seo-description: Use entity attributes to pass product or content information to Recommendations.
seo-title: Entity Attributes
solution: Target
title: Entity Attributes
topic: Premium
uuid: d2d10d41-0383-4947-851f-fb8d6e919f1c
index: y
internal: n
snippet: y
translate: y
---

# Entity Attributes


>The following table describes the available variables.

><table id="table_2F24AB9862FE4D94BFD91F910F436BA9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Entity Attribute </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.id </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>This required parameter identifies the product. This numeric ID must be the same across all Adobe Marketing Cloud products that are used, including Analytics, for the various products to recognize the item and share data about it.</p> <p>You cannot use a comma in an entity ID, unless you escape it.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.id=67833' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.name </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>The product name that is displayed on the Web site when the product is recommended.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.name=Giants vs Rockies 5/12' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.categoryId </span> </p> <p>Supports multi-value (comma-delimited list).</p> </td> 
   <td colname="col2"> <p> The product category used to organize products on your site. A product can have multiple categories, but only one category can be entered in this field, such as a cardigans sub-subsection (i.e. <span class="codeph"> womens </span>, <span class="codeph"> womens:sweaters </span>, <span class="codeph"> womens:sweaters:cardigans </span>). Multiple categories should be separated by commas. </p> <p> <span class="codeph"> categoryId </span>is limited to 250 characters. Multiple categories should be separated by commas. </p> <p> <p>Note:  To show a recommendation based on a category, only one <span class="codeph"> categoryId </span> can be passed into the mbox used to display that particular recommendation. </p> </p> <p>Example:</p> <p> 
     <codeblock>
       'entity.categoryId=BASEBALL, GIANTS, SF BAY AREA', 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.brand </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>Displays an item's brand name.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.brand=brandxyz' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.pageURL </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>Defines the relative URL of the page where the item can be purchased.</p> <p>Example:</p> <p> 
     <codeblock> 
      'entity.pageURL=baseball/giants-tix/giantsvrockies5.12.2000-67833' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.thumbnailURL </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>Defines the relative URL to the thumbnail image that displays with the item.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.thumbnailURL=baseball/giants-tix/giants-136px.gif' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.message </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>A message about the product that is displayed in the recommendation, such as "on sale" or "clearance." The message is typically more verbose than the product name. Use to define additional information to display with the product in the template</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.message=Family special' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.inventory </span> </p> <p>Single-value only. Requires an integer or long value.</p> </td> 
   <td colname="col2"> <p>Displays the inventory level of the item.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.inventory=1' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.value </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>Defines the price or value of the item.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.value=15.99' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.margin </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>The profit margin or other value of the item.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.margin=1.00' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity. </span> <span class="varname"> &lt;custom&gt; </span> </p> <p>Supports multi-value (JSON array).</p> </td> 
   <td colname="col2"> <p>Define up to 100 custom variables that provide additional information about the item. You can specify any unused attribute name for each custom attribute. For example, you might create a custom attribute called <span class="codeph"> entity.genre </span> to define a book or movie. Or, a ticket vendor might create attributes for an event venue for a secondary performer, such as a visiting team in a sporting event or an opening act in a concert. </p> <p><b>Restrictions</b>: </p> 
    <ul id="ul_F0F102908B0142669AF3B74636C828F1"> 
     <li id="li_9271366EC1C34315B01D5BD919F5432A">You cannot use predefined entity attribute names for custom entity attributes.</li> 
     <li id="li_C765DE30512C4E99927E9810EAA822CF">The attribute <span class="codeph"> entity.environment </span> is reserved by the system and cannot be used for custom entity attributes. Attempts to pass <span class="codeph"> entity.environment </span> using <span class="codeph"> targetPageParams </span>, feed, or API will be ignored. </li> 
    </ul> <p>Examples:</p> <p> 
     <codeblock>
       'entity.venue=AT&amp;T Park' 
     </codeblock> </p> <p> 
     <codeblock>
       'entity.secondary=Rockies' 
     </codeblock> </p> <p>Custom entity attributes support multiple values. A multi-value entity attribute can include up to 100 values. Each value can be up to 100 characters. Values that exceed 100 characters are ignored.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.secondary=["band1", "band2"]' 
     </codeblock> </p> <p> <p>Note:  Multi-value custom entity attributes require valid JSON arrays. For correct syntax information, see <a href="c_custom_entity_attributes.xml#concept_E5CF39BCAC8140309A73828706288322" format="dita" scope="local"> Custom Entity Attributes </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.event.detailsOnly </span> </p> <p>Single-value only.</p> </td> 
   <td colname="col2"> <p>Used to prevent an mbox call from incrementing behavioral data counters for an algorithm.</p> <p>Example:</p> <p> 
     <codeblock>
       'entity.event.detailsOnly=true' 
     </codeblock> </p> <p>In the examples below, the first mbox call will update the catalog and behavioral data. The second mbox call will update only the catalog.</p> <p> 
     <codeblock>
       mboxCreate('myMbox',&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'profile.geo.city&nbsp;=&nbsp;new&nbsp;york', 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'profile.geo.state&nbsp;=&nbsp;new&nbsp;york',&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.id&nbsp;=&nbsp;123', 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.inventory&nbsp;=&nbsp;4' 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;) 
     </codeblock> </p> <p> 
     <codeblock>
       mboxCreate('myMbox',&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'profile.geo.city&nbsp;=&nbsp;new&nbsp;york', 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'profile.geo.state&nbsp;=&nbsp;new&nbsp;york',&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.id&nbsp;=&nbsp;123', 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.inventory&nbsp;=&nbsp;4' 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.event.detailsOnly=true' 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;) 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

>Recommendations sends the ` productId` or ` productPurchasedId` (referred to as ` entity.id` in the code) that is used in the algorithms. 

>>[!NOTE]
>>
>>` entity.id` must match the ` productPurchasedId` sent to the order confirmation page and the ` productId` used in Adobe Analytics product reports). 
>

>Most predefined parameters accept only a single value, with new values overwriting old values. The ` categoryId` parameter can accept a comma-delimited list of values for each category containing that product. New ` categoryId` values are appended (250-character limit). Custom entity attributes can accept multiple values passed as valid JSON arrays (see [ Custom Entity Attributes ](c_custom_entity_attributes.md#concept_E5CF39BCAC8140309A73828706288322)). 
>In general, the display information mbox might look like the following example. Change the details in bold to refer to your products.

>>[!NOTE]
>>
>>All entity parameter attributes are case sensitive.
>

>
>```
><div class="mboxDefault"></div><script language="JavaScript1.2"> 
> 
>mboxCreate('productPage', 
> 
>'entity.id= 
<b>67833</b>', 
> 
>'entity.name= 
<b>GIANTS VS ROCKIES 5/12</b>', 
> 
>'entity.categoryId= 
<b>BASEBALL, GIANTS, SF BAY AREA</b>', 
> 
>'entity.pageURL= 
<b>../baseball/giants-tix/giantsvrockies5.12.2000-67833</b>', 
> 
>'entity.venue= 
<b>AT&amp;T PARK</b>', 
> 
>'entity.secondary= 
<b>ROCKIES</b>', 
> 
>'entity.thumbnailURL= 
<b>../baseball/giants-tix/giants-136px.gif</b>', 
> 
>'entity.message= 
<b>FAMILY SPECIAL</b>', 
> 
>'entity.value= 
<b>15.99</b>', 
> 
>'entity.inventory= 
<b>1</b>' 
> 
>); 
> 
></script>
>```


>>[!NOTE]
>>
>>Relative URLs are preferred for ` pageURL` and ` thumbnailURL` rather than absolute URLs because recommendations receive data being sent from all environments on your site. Using relative URLs avoids hardcoded links to a staging or development server. 
>

>If the mbox is on a product page, you can include both the product ID and category ID. The selected algorithm determines which displays. The product ID is used for affinity algorithms and the category ID is used for category algorithms.
>[!MORE_LIKE_THIS]* [ Custom Entity Attributes ](c_custom_entity_attributes.md#concept_E5CF39BCAC8140309A73828706288322)