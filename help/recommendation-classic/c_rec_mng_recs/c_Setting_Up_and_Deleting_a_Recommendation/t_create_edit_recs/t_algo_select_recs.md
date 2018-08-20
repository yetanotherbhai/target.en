---
description: The algorithm determines which action will result in which recommendation. You can test multiple recommendation types against each other by adding more than one algorithm.
seo-description: The algorithm determines which action will result in which recommendation. You can test multiple recommendation types against each other by adding more than one algorithm.
seo-title: Selecting an Algorithm
solution: Target
title: Selecting an Algorithm
topic: Recommendations
uuid: 8d1ec815-ab7e-4f1b-b477-74719c8a7226
index: y
internal: n
snippet: y
translate: y
---

# Selecting an Algorithm


>[!NOTE] {class="- topic/note "}
>
>If you are running a recommendation and change its algorithm, you will lose your settings data. A warning message reminds you that this will occur.



All one-day and two-day algorithms run twice daily. All one-week and longer algorithms run once daily. Site Affinity algorithms run once daily. Backup algorithms run twice daily. 

If the number of recommended items is less than the number of "slots" defined in a template, the ability to partially render the template can be set at the algorithm level using a checkbox located in the Content Serve Settings on the Recommendations Edit tab. If partial template rendering is not enabled and there aren't enough recommended entities to fill all the slots, the entire template is not rendered. If partial template rendering is enabled, Recommendations renders the template whether or not enough recommendations exist to fill up all the slots in the template. You should build your templates to account for this behavior. For example, you might create your template to include null checks. 

Considering each key and the algorithms that map to it, different recommendations lend themselves to placement on different pages: 



<table id="table_ABCB3110D36B4CC9A491BE907C897494"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Key </th> 
   <th colname="col2" class="entry"> Algorithms </th> 
   <th colname="col3" class="entry"> Where on Your Site </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Current category </td> 
   <td colname="col2"> 
    <ul id="ul_E1A9DBA085AB4B3E90F895C17FE3629F"> 
     <li id="li_AFDFF31C8CA1443EA760CABC7C5756F7">Top Sellers </li> 
     <li id="li_BD2020B6758D45919C696CE9D4D8A6BE">Most Viewed </li> 
    </ul> </td> 
   <td colname="col3"> Single-category pages, such as category pages, NOT null search results pages </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Popularity </td> 
   <td colname="col2"> 
    <ul id="ul_5F2157A10A5F41DAB4E06321709976E9"> 
     <li id="li_9EEC741226EF45069A8A7974BAC410DC">Top Sellers </li> 
     <li id="li_E18C30D746204CEB86F483C3AAC801B2">Most Viewed </li> 
     <li id="li_F06E4D30F97644E3973C628FD9B4ECA6">Highest/Best ____ </li> 
    </ul> </td> 
   <td colname="col3"> General pages, such as home or landing pages and offsite ads. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Current item </td> 
   <td colname="col2"> 
    <ul id="ul_64EC295BD75643D992E9D2AB948C1559"> 
     <li id="li_C8585D6E5CB6441CBC86210C469740F7">Purchase Affinities </li> 
     <li id="li_46E0ECAC6F254135A0ECF3E2A1B988BA">View Affinities </li> 
     <li id="li_D1ABAA181FFC4C4EB615A3D4EE12E98E">View/Purchase Affinities </li> 
     <li id="li_3F05B71AC5074B429E9B52A785D12667">Site Affinity </li> 
    </ul> </td> 
   <td colname="col3"> Single-item pages, such as product pages, NOT null search results pages </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Custom profile attribute </td> 
   <td colname="col2"> 
    <ul id="ul_738624312A7A4A68A1BA6F58DEBD26E1"> 
     <li id="li_BFEBEC685AF04638A9C4E9ADC19C29E8">Purchase Affinities </li> 
     <li id="li_391B6B974AFB4A2AB54C443CE870EEF6">View Affinities </li> 
     <li id="li_2AE3C9902E764487AF2CB79C003F031B">View/Purchase Affinities </li> 
     <li id="li_9E965A77ECEC4EA4B4FF3A5BA825207C">Site Affinity </li> 
    </ul> </td> 
   <td colname="col3"> Varies. Home pages, landing pages, cart pages, etc. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nth Last Purchased Entity </td> 
   <td colname="col2"> 
    <ul id="ul_2F1BE1DCA5C24D4285CD6BF534922274"> 
     <li id="li_D98E7EE89F3B4E77B0E0E14AF1888677">Purchase Affinities </li> 
     <li id="li_FC3BE82A74794BDD99FB933E72777E7A">View Affinities </li> 
     <li id="li_DA81E7EC8F774A359B4692094EC59A09">View/Purchase Affinities </li> 
     <li id="li_892177CBE932408992429E7C0BCEFD4B">Site Affinity </li> 
    </ul> </td> 
   <td colname="col3"> NOT product page, pages relevant to purchases. For example, Home page, My Account page, offsite ads. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nth Last Viewed Entity </td> 
   <td colname="col2"> 
    <ul id="ul_8C565547CC4A43939A88B660C0E91A19"> 
     <li id="li_BB762ADD2F7C4AE5956724487AFA37FD">Purchase Affinities </li> 
     <li id="li_B3BFD77E78D8401EAD588BAF7E7BC15F">View Affinities </li> 
     <li id="li_0FA1EC246E42409C889BB3B6AA0E9D50">View/Purchase Affinities </li> 
     <li id="li_91C20AE4D5F247BABB4FF0A9FB96D8F6">Site Affinity </li> 
    </ul> </td> 
   <td colname="col3"> NOT product page. Pages relevant to purchases. For example, Home page, My Account page, offsite ads. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nth Most Favorite Category </td> 
   <td colname="col2"> 
    <ul id="ul_E9B9E84EBE48486B8D9233A581469E5B"> 
     <li id="li_C3E8C57C2C1949F6AB1A2E2C03921DBA">Top Sellers </li> 
     <li id="li_A4F31AFE33C3427A8CD732D8D9C7A96C">Most Viewed </li> 
    </ul> </td> 
   <td colname="col3"> General pages, such as home or landing pages and offsite ads. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nth Most Viewed Entity </td> 
   <td colname="col2"> 
    <ul id="ul_FDF1779FD6C24489A5877D6E23963AFF"> 
     <li id="li_B2182B19DABD494BA394CA3485965CC0">Purchase Affinities </li> 
     <li id="li_15CA1F1852B1481AAEE37AE0877B5F25">View Affinities </li> 
     <li id="li_1F313D3AFC9C4C00803302EF77348D0D">View/Purchase Affinities </li> 
     <li id="li_00153898D3824E198CE3C036DDCB89B3">Site Affinity </li> 
    </ul> </td> 
   <td colname="col3"> Varies. Home pages, landing pages, offsite ads, etc. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Custom Algorithms </td> 
   <td colname="col2"> Custom </td> 
   <td colname="col3"> Varies. Item-based algorithms on product pages, category-based algorithms on category pages. </td> 
  </tr> 
 </tbody> 
</table>


>1. Create a new recommendation, or find the recommendation whose algorithm you want to set and click ` Edit`.
>1. Select an algorithm from the ` Choose Algorithm` dropdown list.

>       The following algorithms are available: 


>       >[!NOTE] {class="- topic/note "}
>       >
>       >The affinities algorithms must be enabled by Client Services.


>       ` Purchase Affinities:` Items that are most often purchased by someone who purchased the current item. 

>       ` View Affinities:` The items that are most often viewed in the same session that the specified item is viewed. 

>       ` View/Purchase Affinities:` The items that are most often purchased in the same session that the specified item is viewed. This algorithm returns other products people purchased after viewing this one, the specified product is not included in the results set. 

>       ` Site Affinity:`This tuning parameter determines which products are best to recommend with other products based on the following criteria: 

>    
>    * Product page views
>    * Cart adds
>    * Cart removes
>    * Purchases
>    * Site activity


>       You can configure this recommendation algorithm to determine how much data is required before a recommendation is presented. The site affinity recommendation is based on the certainty of a relationship between two products. For example, if you select ` Strong`, then the products with the strongest certainty of a match are recommended. 

>       For example, you set a strong affinity and your template includes five items, three of which meet the strength of connection threshold. The two items that do not meet the minimum strength requirements do not display in your recommendations and are replaced by your defined backup items. The items with the strongest affinity display first. 

>       Some customers with diverse product catalogs and diverse site behaviors might get the best results if they set a weak site affinity. 

>       Adobe Search&amp;Promote Recommendation: If you use the Adobe Target site search and merchandising capabilities, this *people who searched for this bought that* recommendation displays in a promo area on the Site Search page. The placement of the mbox is determined with your site search consulting team. 

>       Advanced users can create custom algorithm types, as explained in [ Creating a Custom Algorithm](../../../c_rec_mng_recs/c_Creating_a_Custom_Algorithm/c_Creating_a_Custom_Algorithm.md#concept_9D76531BEE5A4AC8BA2DD30B99CED51A). 

>       ` Popularity By Metric:` Choose any metric from the products report in Adobe Analytics to show the top products by revenue, orders, cart adds, ratings, etc. 

>       ` Top Sellers:` The items that are included in the most completed orders. Multiples of the same item in a single order are counted as one order. 

>       ` Most Viewed:` The items that are viewed most often. 

>       **[!UICONTROL  Recently Viewed Items:]** Items that have been viewed recently by the visitor. When using this algorithm, you should update the Target template to handle cases where blank recommendations would show when there are not enough previously viewed items to display. 
>1. Click ` Save`.
>[!MORE_LIKE_THIS] {class="- topic/related-links "}
>
>* [ Adding a New Recommendation ](c_Creating_a_New_Recommendation.md#concept_9F20B4F0F53D4399B10BCBBC979E0B4C)
>* [ Targeting a Recommendation ](t_targeting_recs.md#task_3D93B8962F6341CB9A3ADE8E29BFECA5)
>* [ Choosing a Test Type ](t_choosetype_recs.md#task_301A771BFE7F45A3AA1E77024E574D1C)
>* [ Choosing a Catalog ](t_Choose_a_Catalog.md#task_047A4BA38078464782024764CA38EF0A)
>* [ Basing the Recommendation on a Recommendation Key ](t_rec_key_recs.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B)
>* [ Choosing the Data Source ](t_data_source_recs.md#task_4EC990FBF374465EA6B7FCA8A5A12786)
>* [ Setting Data Details ](t_Setting_Data_Details.md#task_28DB20F968B1451481D8E51BAF947079)
>* [ Selecting a Template and Recommendation Area ](t_template_and_recommendation_area_recs.md#task_45CA0403F24944EF9FE6C4FC5D1A7836)
>* [ Defining Segments ](t_definesegments_recs.md#task_338EDF86E0A2412896C2854257E91D62)
>* [ Specifying How Many Users See Default Content ](t_how_many_users_see_default_conten_recst.md#task_5059665F6EE64FA39D2851671898F996)
