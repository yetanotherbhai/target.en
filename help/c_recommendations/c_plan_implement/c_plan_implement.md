---
description: What you need to know before creating a Recommendations activity.
keywords: implementing recommendations;javascript library;mbox.js;at.js;prerequisites
seo-description: What you need to know before creating a Recommendations activity.
seo-title: Planning and Implementation
solution: Target
title: Planning and Implementation
title_outputclass: premium
topic: Standard
uuid: aef7f97b-6057-4b03-9108-05572ed7a0db
badge: premium
index: y
internal: n
snippet: y
translate: y
---

# Planning and Implementation

[!DNL  Recommendations] requires that you set up the following hierarchy of information: 



<table id="table_53E0DEF7F0204F9F9C8C8928D55B049E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Step </th> 
   <th colname="col2" class="entry"> Information </th> 
   <th colname="col3" class="entry"> Details </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p style="text-align: center;"><img href="assets/step1_red.png" id="image_079D053A075F427B85266AA9BACE95B8" /> </p> </td> 
   <td colname="col2"> <p>JavaScript library </p> </td> 
   <td colname="col3"> <p> Each page requires a reference to <span class="filepath"> at.js</span> version 0.9.1 (or later) or <span class="filepath"> mbox.js</span> version 55 (or later). This implementation step is required on all pages where a <span class="keyword"> Target</span> activity will be used, and can include keys such as a product or category ID. </p> <p>For information about<span class="filepath"> at.js</span>, see <a href="../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17" format="dita" scope="local"> at.js Implementation</a>. </p> <p>For more information about <span class="filepath"> mbox.js</span>, see <a href="../../c_seting_up_target/c_implementing_target/t_mbox_download/t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420" format="dita" scope="local"> Mbox.js Implementation</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p style="text-align: center;"><img href="assets/step2_red.png" id="image_8600F0A878A547F590F14959DE95D0D2" /> </p> </td> 
   <td colname="col2"> <p>Keys </p> </td> 
   <td colname="col3"> <p>The key determines the type of product or content that displays in your recommendations. For example, the key might be a product category. See <a href="../../c_recommendations/c_algorithms/t_create_new_algorithm.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B" format="dita" scope="local"> Base the Recommendation on a Recommendation Key</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p style="text-align: center;"><img href="assets/step3_red.png" id="image_9A3BE89D45F84FE09B8F8E7751470F83" /> </p> </td> 
   <td colname="col2"> <p>Attributes </p> </td> 
   <td colname="col3"> <p>Attributes provide more specific information about the products you want to display. For example, you might want to show products within a certain price range, or items that meet an inventory threshold. Attributes can be provided in the mbox or through a <a href="../../c_recommendations/c_products/c_feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> feed</a>. </p> <p>See <a href="../../c_recommendations/c_algorithms/t_create_new_algorithm.md#task_28DB20F968B1451481D8E51BAF947079" format="dita" scope="local"> Inclusion Rules</a> and <a href="../../c_recommendations/c_products/r_entity_attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F" format="dita" scope="local"> Entity Attributes</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p style="text-align: center;"><img href="assets/step4_red.png" id="image_933D0A2340CF423B8970DF4336F9C0C4" /> </p> </td> 
   <td colname="col2"> <p>Exclusions </p> </td> 
   <td colname="col3"> <p>Exclusions determine which specific items do not appear in your recommendations. </p> <p>See <a href="../../c_recommendations/c_products/c_feeds.md#task_DD6D2F889E234F8C82B1604A3B315D81" format="dita" scope="local"> Exclusions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p style="text-align: center;"><img href="assets/step5_red.png" id="image_5E83430D145948BDBB2C17D0F6C2B9A5" /> </p> </td> 
   <td colname="col2"> <p>Purchase deals </p> </td> 
   <td colname="col3"> <p>Purchase details provide information about purchased items and the order when the purchase has been completed. </p> </td> 
  </tr> 
 </tbody> 
</table>

