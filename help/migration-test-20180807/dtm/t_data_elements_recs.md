---
description: Data elements are the building blocks for rules. Data elements let you create a data dictionary (or data map) for any object that is contained on your site. They can be JavaScript objects, cookie values, and query strings. You use data elements to build a data layer that can be used for Analytics and other data collection tools.
keywords: Dynamic tag management
seo-description: Data elements are the building blocks for rules. Data elements let you create a data dictionary (or data map) for any object that is contained on your site. They can be JavaScript objects, cookie values, and query strings. You use data elements to build a data layer that can be used for Analytics and other data collection tools.
seo-title: Create Data Elements
solution: Target
title: Create Data Elements
uuid: cfb5a428-50ba-4708-9aff-08b2f3744135
index: y
internal: n
snippet: y
translate: y
---

# Create Data Elements

Log in to DTM and create a new data element:

>1. In the web property, click ** `Rules` ** > ** `Data Elements` ** > ** `Create New Data Element` **.
>1. Complete the following fields and options:


>    <table id="table_493AF51524524EAB91324DBFBDFCA655"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Option</th> 
   <th colname="col2" class="entry">Value</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Name</td> 
   <td colname="col2">Order ID</td> 
  </tr> 
  <tr> 
   <td colname="col1">Type</td> 
   <td colname="col2">JS Object</td> 
  </tr> 
  <tr> 
   <td colname="col1">Parameter/Path Name</td> 
   <td colname="col2">OrderDetails.orderId</td> 
  </tr> 
  <tr> 
   <td colname="col1">Default value</td> 
   <td colname="col2">Leave blank</td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Remember this Value For</p> </td> 
   <td colname="col2">Page View</td> 
  </tr> 
 </tbody> 
</table>

>1. Create separate Data Elements for each of the entities you would like to capture.

>    
>    * `entity.id=<product Id>` (required)
>    * `entity.name=<product name>`
>    * `entity.categoryId=<category>`
>    * `entity.pageURL=<landing URL>`
>    * `entity.thumbnailURL=<thumbnail URL>`
>    * `entity.value=<price>`
>    * `entity.inventory=<inventory amount>`
