---
description: The Content settings determine how recommendations display in your design.
keywords: content settings;content;partial design rendering;backup recommendations;apply inclusion rules
seo-description: The Content settings determine how recommendations display in your design.
seo-title: Content Settings
solution: Target
title: Content Settings
topic: Premium
uuid: bc156062-f125-4a00-84f5-86b97ec7b94d
index: y
internal: n
snippet: y
translate: y
---

# Content Settings

It is possible for `Recommendations` criteria to return fewer recommendations than your design calls for. For example, your design may have five available "slots," but the criteria returns only three recommended items. The `Content` settings control how recommendations are presented when this happens. 
Content rules determine what happens if the number of recommended items does not fill your design. For example, if your design has space for five items, but your criteria causes only three items to be recommended, you can leave the remaining space empty, or you can use backup recommendations to fill the extra space.
Select the appropriate toggles:

* `Enable Partial Design Rendering` 

* `Show Backup Recommendations` 

* `Apply Inclusion Rules to Backup Recommendations` 

* `Recommend Previously Purchased Items` 
  This setting is based on the `productPurchasedId`. It is useful if you sell items that people typically purchase only once, such as kayaks. If you sell items that people come back to purchase again, such as shampoo or other personal items, you should disable this option. 


If you enable ** `Show Backup Recommendations` **, the option to apply your [inclusion rules](t_data_details.md#task_28DB20F968B1451481D8E51BAF947079) to backup recommendations is enabled by default. 
![](../target/graphics/Recs_ContentControls.png) 


<table id="table_C0B893ECCEB4472B848808750C7ADDED"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Partial Design Rendering</th> 
   <th colname="col2" class="entry">Backup Recommendations</th> 
   <th colname="col3" class="entry">Result</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Disabled</td> 
   <td colname="col2">Disabled</td> 
   <td colname="col3"> <p>If fewer recommendations are returned than the design calls for, the recommendations design is replaced by default content and no recommendations are displayed.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Enabled</td> 
   <td colname="col2">Disabled</td> 
   <td colname="col3"> <p>The design is rendered, but may include blank space if fewer recommendations are returned than the design calls for.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Enabled</td> 
   <td colname="col2">Enabled</td> 
   <td colname="col3"> <p>Backup recommendations will fill available design "slots," fully rendering the design.</p> <p>If applying inclusion rules to backup recommendations restricts the number of qualifying backup recommendations to the point that the design cannot be filled, the design is partially rendered.</p> <p>If the criteria does not return any recommendations, and inclusion rules restrict backup recommendations to zero, the design is replaced with default content.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Disabled</td> 
   <td colname="col2">Enabled</td> 
   <td colname="col3"> <p>Backup recommendations will fill available design "slots," fully rendering the design.</p> <p>If applying inclusion rules to backup recommendations restricts the number of qualifying backup recommendations to the point that the design cannot be filled, the design is replaced by default content and no recommendations are displayed.</p> </td> 
  </tr> 
 </tbody> 
</table>

