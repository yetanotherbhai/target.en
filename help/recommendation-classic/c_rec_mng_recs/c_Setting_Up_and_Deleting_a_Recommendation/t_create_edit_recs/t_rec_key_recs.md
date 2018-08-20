---
description: You can create multiple recommendation keys and test them against each other.
seo-description: You can create multiple recommendation keys and test them against each other.
seo-title: Basing the Recommendation on a Recommendation Key
solution: Target
title: Basing the Recommendation on a Recommendation Key
topic: Recommendations
uuid: 4594651d-4ed7-4115-97ea-36aa604142d7
index: y
internal: n
snippet: y
translate: y
---

# Basing the Recommendation on a Recommendation Key

Each algorithm is defined in its own tab. Traffic is split evenly across your different algorithm tests. In other words, if you have two algorithms, traffic is divided equally between them. if you have two algorithms and two templates, traffic is split evenly between the four combinations. You can also specify a percentage of site visitors who see the default content, for comparison. In that case, the specified percentage of visitors see the default content, and the rest are split between your algorithm and template combinations. 

>1. Create a new recommendation, or find the recommendation whose type to set and click **[!UICONTROL  Edit]**.
>1. To change the recommendation key, select the new key from the [!UICONTROL  Base the recommendation on:] dropdown list, then select any additional options.

>       The list contains the following options: 



>    <table id="table_D2F606E0723A4A47992CFCF5B5A110E2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Option </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Current Page Activity</span> </p> </td> 
   <td colname="col2"> <p>This set of recommendation types is defined by the visitor's activity on the current page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Current Item </span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the item the visitor is currently viewing. Recommendations are set up to display other items that might interest visitors who are interested in the specified item. </p> <p>When this option is selected, the <span class="codeph"> entity.id</span> value must be passed as a parameter in the display mbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Current Category</span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the product category that the visitor is currently viewing. Recommendations are set up to display items in the specified product category. </p> <p>When this option is selected, the <span class="codeph"> entity.categoryId </span>value must be passed as a parameter to the display mbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Custom Profile Attribute</span> </p> </td> 
   <td colname="col2"> <p>For users who use the recommendations and testing and targeting functions of Adobe Target. </p> <p>The recommendation is based on any profile attribute set up for testing. The value for the attribute must resolve to an<span class="codeph"> entity.id</span>. For example, you might want to keep track of an item someone abandoned in their cart. You could write a profile script that stores that <span class="codeph"> entity.id</span>, and then deliver recommendations based on that abandoned cart item the next time the visitor returns to the site. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Custom Algorithms</span> </p> </td> 
   <td colname="col2"> <p>This set of recommendation types lists any custom algorithms that have been defined. If there are no custom algorithms, this portion of the <span class="wintitle"> Recommendation Type</span> list is empty. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Past Behavior</span> </p> </td> 
   <td colname="col2"> <p>This set of recommendation types is defined by the past behavior of your site visitors. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Nth Last Purchased Entity</span> </p> </td> 
   <td colname="col2"> <p> <p>Note:  This key was formerly named "Last Purchased Item." </p> </p> <p>The recommendation is determined by a recent item that was purchased by each unique visitor. This is captured automatically, so no values need to be passed on the page. </p> <p>Choose from the following options to determine the item to key off of: </p> <p> 
     <ul id="ul_C3184D7E9E1344EA863A12326D6F1117"> 
      <li id="li_1425A9CA4ABA444798FBF2D34B1CEF47">Last </li> 
      <li id="li_8C1A4894741443E7B0322F19DAB00F6A">Second-to-Last </li> 
      <li id="li_58FF5A39C1404E77AE0BF61A84FCA643">Third-to-Last </li> 
      <li id="li_DF6E65A056094BBBBCCFC8E55011890B">Fourth-to-Last </li> 
      <li id="li_89BE67D54314452086AFD5789E64C73B">Fifth-to-Last </li> 
     </ul> </p> <p>After choosing the item, select one of the following: </p> <p id="p_F117F6CF2A264025A93D3C26316A002B"> 
     <ul id="ul_4C29600D88094B1D919316DF557BDDBE"> 
      <li id="li_262350D2DD1D43B591D5629053A01262">No Aggregate <p>Only produce recommendations from the specified key. </p> </li> 
      <li id="li_B07138A85B17413BBB966B40C64B9D0E">Aggregate <p>Your recommendations begin with the specified entity, then continue in chronologically reverse order of the visitor's behavior on your site until your template is filled. For example, if you key off the third most-viewed entity, Recommendations begins with that entity, followed by the fourth most-viewed entity, then the fifth, and so on until the template is filled. </p> </li> 
      <li id="li_6D8FF718233045AAACCB478B6E7A1EDE">All or Nothing <p>Creates a recommendation based on the first entity ID that fills the template. For example, if your recommendation contains eight items and you key off the last purchased entity, then Recommendations begins with that entity and works back through your history until it finds an entity ID containing at least eight items. If an entity ID contains fewer than eight items, it is skipped. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Nth Last Viewed Entity</span> </p> </td> 
   <td colname="col2"> <p> <p>Note:  This key was formerly named "Last Viewed Item." </p> </p> <p>The recommendation is determined by a recent item that was viewed by each unique visitor. This is captured automatically, so no values need to be passed on the page. </p> <p>Choose from the following options to determine the item to key off of: </p> <p> 
     <ul id="ul_6DEC967E8BEA4DF997ED37B18232F054"> 
      <li id="li_8EAF6C9878274BC0BE04456FF30A6F48">Last </li> 
      <li id="li_C0343C308E2E496D9F599332CAF51F0A">Second-to-Last </li> 
      <li id="li_BD38BF03EE494F6AA17412342FD01679">Third-to-Last </li> 
      <li id="li_B8261DB0A21147729CC3AA16957066EC">Fourth-to-Last </li> 
      <li id="li_638BBB0760224601A800A4DD69BAA6A9">Fifth-to-Last </li> 
     </ul> </p> <p> </p> <p>After choosing the item, select one of the following: </p> <p> 
     <ul id="ul_EA31573F5595497999DF51EF175DDE0E"> 
      <li id="li_C7356135D0BA4BA88DE9ED82A2342278">No Aggregate <p>Only produce recommendations from the specified key. </p> </li> 
      <li id="li_6A7DD0D361844050852F759C2F29D10F">Aggregate <p>Your recommendations begin with the specified entity, then continue in chronologically reverse order of the visitor's behavior on your site until your template is filled. For example, if you key off the third most-viewed entity, Recommendations begins with that entity, followed by the fourth most-viewed entity, then the fifth, and so on until the template is filled. </p> </li> 
      <li id="li_68231EA48D3044C4A2D26076DEC64566">All or Nothing <p>Creates a recommendation based on the first entity ID that fills the template. For example, if your recommendation contains eight items and you key off the last purchased entity, then Recommendations begins with that entity and works back through your history until it finds an entity ID containing at least eight items. If an entity ID contains fewer than eight items, it is skipped. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Nth Most Viewed Entity</span> </p> </td> 
   <td colname="col2"> <p> <p>Note:  This key was formerly named "Most Viewed Item." </p> </p> <p>The recommendation is determined by an item that has been viewed often, using the same method as used for Nth Most Favorite Category. </p> <p>This is determined by recency/frequency algorithm that works as follows: </p> <p> 
     <ul id="ul_568FB583582546C49479197AC416C4A1"> 
      <li id="li_472876E860A6430DB0F50BAD266BC7BC"> 10 pts for 1st product view </li> 
      <li id="li_08E2CE83C7174B69BAFBF992204F1E52"> 5 pts for every one after </li> 
      <li id="li_ADDB3EDABC5A4B159F7BF7B3C2DABAD8"> At end of session divide all values by 2 </li> 
     </ul> </p> <p>For example, viewing surfboardA then surfboardB in one session results in A: 10, B: 5. When the session ends, you will have A: 5, B: 2.5. If you view the same items in the next session, the values change to A: 15 B: 7.5. </p> <p>Choose from the following options to determine the item to key off of: </p> <p> 
     <ul id="ul_406BD16E7AE043AC922911E2F26AD63A"> 
      <li id="li_89D422AE73F04C9CA46A78B05A26CA38">Most </li> 
      <li id="li_7BA538780F074A97B7A332429F8D2F42">Second-Most </li> 
      <li id="li_7E739A46850649928433E59A2A43C48B">Third-Most </li> 
      <li id="li_A25B73639196444EB298F8C4714A8845">Fourth-Most </li> 
      <li id="li_A0F2F2F8737A4439A927E2B5A75FD00A">Fifth-Most </li> 
     </ul> </p> <p> </p> <p>After choosing the item, select one of the following: </p> <p> 
     <ul id="ul_077F89B5F4054C5C85A23E5B8F198245"> 
      <li id="li_23E9DE25740C4039AE37D91946FA2F29">No Aggregate <p>Only produce recommendations from the specified key. </p> </li> 
      <li id="li_B091AB20484C4E039A672A1A1D1676B6">Aggregate <p>Your recommendations begin with the specified entity, then continue in chronologically reverse order of the visitor's behavior on your site until your template is filled. For example, if you key off the third most-viewed entity, Recommendations begins with that entity, followed by the fourth most-viewed entity, then the fifth, and so on until the template is filled. </p> </li> 
      <li id="li_0147E9C8A9764F15A36F8B91790C4219">All or Nothing <p>Creates a recommendation based on the first entity ID that fills the template. For example, if your recommendation contains eight items and you key off the last purchased entity, then Recommendations begins with that entity and works back through your history until it finds an entity ID containing at least eight items. If an entity ID contains fewer than eight items, it is skipped. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Nth Most Favorite Category</span> </p> </td> 
   <td colname="col2"> <p> <p>Note:  This key was formerly named "Favorite Category." </p> </p> <p>The recommendation is determined by the category that has received the most activity, using the same method used for "most viewed item" except that categories are scored instead of products. </p> <p>Choose from the following options to determine the item to key off of: </p> <p> 
     <ul id="ul_B8A275AB57FD4EEC965C0A1E9E1796F0"> 
      <li id="li_B991D3EFCA7C471499614A0EEF0280F2">Most </li> 
      <li id="li_6F0C021D74C449C383191F0824F10AC8">Second-Most </li> 
      <li id="li_1D045C3B9E504292826A2B72570ADC5A">Third-Most </li> 
      <li id="li_8ABB2129203944359155FB294C7A0992">Fourth-Most </li> 
      <li id="li_275ED3E2F8124E69A8DD39B2BB77CC90">Fifth-Most </li> 
     </ul> </p> <p> </p> <p>After choosing the item, select one of the following: </p> <p> 
     <ul id="ul_2786305A6A3140ABBAA8A32D236D5F87"> 
      <li id="li_00CFF0CF72A64850B52B9936E0CD37E6">No Aggregate <p>Only produce recommendations from the specified key. </p> </li> 
      <li id="li_FB1EC83201CB4AB0BE4AECAC59708AF0">Aggregate <p>Your recommendations begin with the specified entity, then continue in chronologically reverse order of the visitor's behavior on your site until your template is filled. For example, if you key off the third most-viewed entity, Recommendations begins with that entity, followed by the fourth most-viewed entity, then the fifth, and so on until the template is filled. </p> </li> 
      <li id="li_3A9F858186AF44A3BD1F8CEAAD798DC0">All or Nothing <p>Creates a recommendation based on the first entity ID that fills the template. For example, if your recommendation contains eight items and you key off the last purchased entity, then Recommendations begins with that entity and works back through your history until it finds an entity ID containing at least eight items. If an entity ID contains fewer than eight items, it is skipped. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Popularity</span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the popularity of items on your site. Popularity includes top sellers and top viewed by mbox data and, if you use Adobe Analytics, all of the metrics available in the product report (previously called <i>optimize on any metric</i>). These recommendations rank the items based on the criteria you choose in the <span class="wintitle"> Algorithm</span> dropdown. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Site Search</span> </p> </td> 
   <td colname="col2"> <p>(Available only if you use the search capabilities of Adobe Target.) The recommendation is determined by the search results on a particular page. Those search results are used as input to the recommendation to determine complementary items. </p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Click **[!UICONTROL  Save]**.
>[!MORE_LIKE_THIS]* [ Adding a New Recommendation ](c_Creating_a_New_Recommendation.md#concept_9F20B4F0F53D4399B10BCBBC979E0B4C)* [ Targeting a Recommendation ](t_targeting_recs.md#task_3D93B8962F6341CB9A3ADE8E29BFECA5)* [ Choosing a Test Type ](t_choosetype_recs.md#task_301A771BFE7F45A3AA1E77024E574D1C)* [ Choosing a Catalog ](t_Choose_a_Catalog.md#task_047A4BA38078464782024764CA38EF0A)* [ Selecting an Algorithm ](t_algo_select_recs.md#task_2203616ABBE342B6ADAB08F278D794FA)* [ Choosing the Data Source ](t_data_source_recs.md#task_4EC990FBF374465EA6B7FCA8A5A12786)* [ Setting Data Details ](t_Setting_Data_Details.md#task_28DB20F968B1451481D8E51BAF947079)* [ Selecting a Template and Recommendation Area ](t_template_and_recommendation_area_recs.md#task_45CA0403F24944EF9FE6C4FC5D1A7836)* [ Defining Segments ](t_definesegments_recs.md#task_338EDF86E0A2412896C2854257E91D62)* [ Specifying How Many Users See Default Content ](t_how_many_users_see_default_conten_recst.md#task_5059665F6EE64FA39D2851671898F996)