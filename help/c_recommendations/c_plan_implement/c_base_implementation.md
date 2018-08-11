---
description: The base implementation requires that you pass parameters to your page that determine which products or services appear in your recommendations.
keywords: multipage activity
seo-description: The base implementation requires that you pass parameters to your page that determine which products or services appear in your recommendations.
seo-title: Base Implementation
solution: Target
title: Base Implementation
title_outputclass: premium
topic: Premium
uuid: 06578914-9047-43fe-b312-7245bcd8e349
badge: assets/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Base Implementation

Before you begin setting up a [!DNL  Recommendations] activity, you should understand how product data is provided to [!DNL  Recommendations], and decide which method works best for your needs. 

There are two methods to provide information about products and services to [!DNL  Recommendations]: 



<table id="table_FCC3159B51BF43FA92F3658EDF7C7E1F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Method </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Pass parameters directly to the page </p> </td> 
   <td colname="col2"> <p>This method works well for items that change frequently. However, because it requires that changes be made directly to the page, in many organizations, this method requires the involvement of IT and the people who implement the pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pass parameters through a Google or CSV feed </p> </td> 
   <td colname="col2"> <p>This method works well for collections that do not change frequently. It is usually not necessary to change your mbox implementation or other page code to provide product information through a feed. However, the product list remains static, so quick changes are more difficult. For more information, see <a href="c_feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> Feeds </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

These methods can be used separately or together, as in the following examples. 

This page contains the following sections: 


<ul class="simplelist"> 
 <li> <a href="c_base_implementation.xml#concept_D1154A3FB0FB4467A29AD2BDD21C82D5/section_DF6BAE4BF11548BD9C44D0A426BCF5A7" format="dita" scope="local"> Example One: Combine Page and Feeds </a> </li> 
 <li> <a href="c_base_implementation.xml#concept_D1154A3FB0FB4467A29AD2BDD21C82D5/section_D5A4F69457604CA7AACFD7BFF79B58A9" format="dita" scope="local"> Example Two: Pass All Parameters on the Product (or Content) Details Page </a> </li> 
 <li> <a href="c_base_implementation.xml#concept_D1154A3FB0FB4467A29AD2BDD21C82D5/section_6E8A73376F30468BB549F337C4C220B1" format="dita" scope="local"> Sample Code </a> </li> 
</ul>



## Example One: Combine Page and Feeds {#section_DF6BAE4BF11548BD9C44D0A426BCF5A7}

One common [!DNL  Recommendations] implementation option uses both page parameters and feeds. 

This method might be preferred by a retailer who has a relatively set product catalog, but who might want to emphasize specific seasonal items or items that are on sale. Most customers might provide their information primarily through the feed, with only occasional adjustments on the page. 

Use a feed to provide information that will remain static. Whether using a CSV file or Google feed, use the following parameters: 


* Required parameters 
    * ` entity.id`

* Helpful parameters 
    * ` entity.cust1`
    * ` entity.cust2`
    * ` entity.cust3`
    * All other attributes



Once the feed is set up and passed to [!DNL  Recommendations], pass parameters on the page for items that are frequently changing. 


* Required parameters 
    * ` entity.id`
    * ` entity.categoryId`

* Helpful parameters 
    * ` entity.inventory`
    * ` entity.value`



Priority is given to whichever set of data runs most recently. If you pass the feed first and then update the page parameters, changes that are made in the page parameters will be shown, replacing item information passed in the feed. 

## Example Two: Pass All Parameters on the Product (or Content) Details Page {#section_D5A4F69457604CA7AACFD7BFF79B58A9}

If you pass all parameters on the page, you can quickly make updates by updating the page. In some organizations, this requires the involvement of IT or your Web Design team. 

This example might be especially useful for a media company, with content that constantly changes. 


* Required parameters 
    * ` entity.id`
    * ` entity.categoryId`
    * All other attributes



## Sample Code {#section_6E8A73376F30468BB549F337C4C220B1}

For example, you can use the following code in the header section of your product or content pages: 


```
function targetPageParams() { 
   return { 
      "entity": { 
         "id": " 
<i>32323</i>", 
         "categoryId": " 
<i>My&amp;nbsp;Category</i>", 
         "value": 105.56, 
         "inventory": 329 
      } 
   } 
}
```


For more examples of the code you might use on different types of pages, see [ Implementation According to Page Type ](r_implementation_page_type.md#reference_DE38BB07BD3C4511B176CDAB45E126FC). 
