---
description: This topic lists all possible parameters you can set when creating or editing a recommendation, and the algorithms where each parameter can be used.
seo-description: This topic lists all possible parameters you can set when creating or editing a recommendation, and the algorithms where each parameter can be used.
seo-title: Advanced Recommendations Options
solution: Target
title: Advanced Recommendations Options
topic: Recommendations
uuid: 88f1e2bf-3c82-4704-854f-1e92710a57bd
index: y
internal: n
snippet: y
translate: y
---

# Advanced Recommendations Options




><table id="table_C269C40F544F4C648B22D3DBE038B4E9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Description </th> 
   <th colname="col3" class="entry"> Algorithms </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Only recommend products with inventory greater than or equal to </p> </td> 
   <td colname="col2"> <p>Specify how many items must be in stock before a product is recommended. </p> <p>The product is not recommended unless there are at least the specified number in stock. This helps to prevent recommending products that are sold out or nearly sold out. You can also use this setting to try to reduce the inventory of products that are overstocked. </p> <p> <p>Note:  The .csv file follows the rules established in the algorithm setup, except for any information filtered at display time (price limit and inventory limit). </p> </p> </td> 
   <td colname="col3"> <p>Top Sellers </p> <p>Most Viewed </p> <p>Purchase Affinities </p> <p>View/Purchase Affinities </p> <p>Popularity </p> <p>Site Affinity </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Only recommend products within the price range </p> </td> 
   <td colname="col2"> <p>Specify the price range that products must fit into before they are recommended. </p> <p>This helps you target recommended products to buyers. If, for example, a customer usually purchases bargain products, lower-priced products are recommended. </p> <p> <p>Note:  The .csv file follows the rules established in the algorithm setup, except for any information filtered at display time (price limit and inventory limit). </p> </p> </td> 
   <td colname="col3"> <p>Top Sellers </p> <p>Most Viewed </p> <p>Purchase Affinities </p> <p>Popularity </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Strength of connection between recommended products and the referenced product </p> </td> 
   <td colname="col2"> <p>Specify the affinity between the recommended products and the source product. </p> <p>This helps you target your recommendations based on how often people act on the source product and the recommended product during the same Web session. The strength is calculated according to the number of times the recommended product has been viewed, added to the cart, or purchased in the same session as the source product. </p> <p>If you want to make recommendations without very much affinity data, select <span class="uicontrol"> Weak</span>. If you prefer to wait until there's a lot of data before the algorithm starts to make recommendations, select <span class="uicontrol"> Strong</span>. </p> </td> 
   <td colname="col3"> <p>Site Affinity </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Site Catalyst Report Suite </p> </td> 
   <td colname="col2"> <p>Specify the Adobe Analytics report suite used to track the data used with this recommendation. </p> </td> 
   <td colname="col3"> <p>Top Sellers </p> <p>Most Viewed </p> <p>Purchase Affinities </p> <p>Popularity </p> <p>Site Affinity </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SiteCatalyst Metric </p> </td> 
   <td colname="col2"> <p>Use any metric available on the product report in Adobe Analytics to drive your algorithm. You can choose algorithms that rank your products based on any metric, such as "add to carts," revenue, units sold, etc. </p> </td> 
   <td colname="col3"> <p>Popularity </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attribute Weighing </p> </td> 
   <td colname="col2"> <p>Use attribute weighting to "nudge" the algorithm. Marketers can influence the algorithm based on important description or metadata about the content catalog. Apply a higher weighting to these on-sale items so they show more often in the recommendation. Non-sale items are not completely excluded, but they display less often. Multiple weightings can be applied to the same algorithm, and the weightings can be tested on split traffic in the recommendation. </p> <p> 
     <table id="simpletable_A218459CE1344ED3935BEA1943771600"> 
      <tr class="strow">
       <td class="stentry"> 
        <ul class="simplelist"> 
         <li> High </li> 
         <li>&nbsp; </li> 
         <li>&nbsp; </li> 
         <li>&nbsp; </li> 
         <li> Low </li> 
        </ul></td>
       <td class="stentry"> 
        <ul class="simplelist"> 
         <li> 25% </li> 
         <li> 12% </li> 
         <li> 0 </li> 
         <li> -12% </li> 
         <li> -25% </li> 
        </ul></td> 
      </tr> 
     </table> </p> 
    <!--<p> <ul id="ul_8B9604BB058E44F2A48DFF0E5F6AE71A"> <li id="li_05DEDA4D9B3840958677F5E6BA289DF2"><b>Very High</b> changes the count by +10% </li> <li id="li_66609BE89A4A40488C25C668C86E7C46"><b>Very Low </b>changes the count by -10% </li> </ul> </p>--> </td> 
   <td colname="col3"> <p>Purchase Affinities </p> <p>View Affinities </p> <p>View/Purchase Affinities </p> <p>Top Sellers </p> <p>Most Viewed </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Include Only When </p> </td> 
   <td colname="col2"> <p>Show this recommendation only if one or more selected variables exactly matches the specified criteria. For example, you can set this option to specify that the recommendation shows only for a specific entityID. </p> </td> 
   <td colname="col3"> <p>Site Affinity </p> <p>Purchase Affinities </p> <p>View/Purchase Affinities </p> <p>View Affinities </p> <p>Popularity </p> <p>Top Sellers </p> <p>Most Viewed </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!MORE_LIKE_THIS]
>
>* [ Viewing a Recommendation in the Recommendations Manager ](c_Viewing_a_Recommendation_in_the_Recommendations_Manager.md#concept_20461D0A428B42F99270AF30293038AE)
>* [ Setting Up and Deleting a Recommendation ](c_Setting_Up_and_Deleting_a_Recommendation.md#concept_46FC867861EC477ABF287D49B84F0961)
>* [ Starting a Recommendation ](c_Starting_a_Recommendation.md#concept_FD5D757B0C174CE2B0D8C132303EE674)
>* [ Creating a Custom Algorithm ](c_Creating_a_Custom_Algorithm.md#concept_9D76531BEE5A4AC8BA2DD30B99CED51A)
>* [ Creating Catalogs ](t_Creating_Catalogs.md#task_CF595BC2426140E08F7948E43E3C8F81)
>* [ Searching Catalogs ](t_Searching_Catalogs.md#task_B5E7B5638BF0406E93AE18B2C6893AE2)
>* [ Troubleshooting Recommendations ](r_Troubleshooting_Recommendations.md#reference_14CE05395C164BE1AC5E5FA2F7E940E2)
