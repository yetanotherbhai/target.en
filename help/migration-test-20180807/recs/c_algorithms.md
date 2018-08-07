---
description: Criteria are rules that determine which products to recommend based on a predetermined set of visitor behaviors.
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
seo-description: Criteria are rules that determine which products to recommend based on a predetermined set of visitor behaviors.
seo-title: Criteria
solution: Target
title: Criteria
topic: Premium
uuid: aa72ddbf-7ec6-4e33-becc-6bd21c4f4337
index: y
internal: n
snippet: y
translate: y
---

# Criteria

## Criteria {#concept_4BD01DC437F543C0A13621C93A302750}Criteria are rules that determine which products to recommend based on a predetermined set of visitor behaviors.Criteria determine which action will result in which recommendation. You can test multiple recommendation types against each other by adding multiple criteria.
You select an industry vertical based on the goals of your recommendations activity:


<table id="table_B99C2269E3EA4D5AA710C03A6BBBB008"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Industry Vertical </th> 
   <th colname="col2" class="entry"> Goal </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Retail/Ecommerce</p> </td> 
   <td colname="col2"> <p>Conversion resulting in purchase</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lead Generation/B2B/Financial Services</p> </td> 
   <td colname="col2"> <p>Conversion with no purchase</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Media/Publishing</p> </td> 
   <td colname="col2"> <p>Engagement</p> </td> 
  </tr> 
 </tbody> 
</table>

The recommendation key you select determines the criteria type. There are several criteria types, which are represented as criteria cards when you set up a ` Recommendations` activity. 


<table id="table_C82741028256468E9FE0B789A4C22F33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Criteria Type </th> 
   <th colname="col2" class="entry"> Keys </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Current Page Activity</p> </td> 
   <td colname="col2"> <p>Recommend items based on what users do on the current page. For example, visitors who view a particular article might want to see other articles from the same category.</p> <p> 
     <ul id="ul_84C06C98520B4CF98FF296D051EA360D"> 
      <li id="li_1D0F6D833598441385EE674ABE27EC9C"> <p>Current Item</p> </li> 
      <li id="li_28971A6C56F5470982BF2ECB0FF0140F"> <p>Current Category</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom</p> </td> 
   <td colname="col2"> <p>Recommend items based on custom attributes.</p> <p> 
     <ul id="ul_E34FB629F7984A0C9637FB7E3A5DCC0F"> 
      <li id="li_2824DCFCA5D74DFAACF22057872C0420"> <p>Custom Attribute</p> </li> 
     </ul> </p> <p>When you base recommendations on custom attributes, you must select the custom attribute and then select the recommendation type.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Past Behavior</p> </td> 
   <td colname="col2"> <p>Recommend items based on how visitors have responded to an item in the past. For example, people who have purchased a particular brand have been more likely to purchase another item from that brand.</p> <p> 
     <ul id="ul_2ED7631E9E7149EDA36D7A0F93BCF1C4"> 
      <li id="li_B3EB50778A2E4F55A61D95E3834BEE91"> <p>Last Purchased Item</p> </li> 
      <li id="li_CD2D62C14F71463E8D4BED64F1CF7846"> <p>Last Viewed Item</p> </li> 
      <li id="li_4D06DB888F0A43DD961172CAB82F6ACF"> <p>Most Viewed Item</p> </li> 
      <li id="li_5AA64DC791694E628177B622EA5344F9"> <p>Favorite Category</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Popularity</p> </td> 
   <td colname="col2"> <p>Recommend the most popular items, such as the most popular videos in a related category or the products that have been viewed most often on your site.</p> <p> 
     <ul id="ul_97F9B3D46473459CAD91046FE6F0966B"> 
      <li id="li_1AB63F10D22F43FDBADE6853F432227E"> <p>Popularity</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Recently Viewed Items</p> </td> 
   <td colname="col2"> <p>Recommend the items a visitor has viewed most recently, such as the items a visitor looked at the last time he or she visited your site, or the articles that are trending most highly right now.</p> <p>This criteria type is not limited by collections.</p> <p> 
     <ul id="ul_9017DDFB12AA4826BF139D5D24610574"> 
      <li id="li_B0A11E8C999C402EA7333481E9F04C1C"> <p>Recently Viewed Items</p> </li> 
     </ul> </p> <p> <p>Note:  You cannot use the Recently Viewed Items criteria for backup recommendations. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

` Target Recommendations` uses sophisticated algorithms to determine when a visitor's actions qualify for the criteria set in your activity. The recommendation key determines the recommendations logic options that are available. 


<table id="table_23DE3F3FFE374F4F812684BD6259930A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Criteria </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Items/Media with Similar Attributes</p> </td> 
   <td colname="col2"> <p>Recommends items or media similar to items or media based on current page activity or past visitor behavior.</p> <p> <p>Note:  If you select <span class="uicontrol"> Items </span>/ <span class="uicontrol"> Media with Similar Attributes </span>, you will have the option to set <a href="c_algorithms.xml#concept_5402DAFA279C4E46A9A449526889A0CB" format="dita" scope="local"> content similarity rules </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="- topic/p ">People Who Viewed This, Viewed That</p> </td> 
   <td colname="col2"> <p class="- topic/p ">Recommends items that are most often viewed in the same session that the specified item is viewed.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="- topic/p ">People Who Viewed This, Bought That</p> </td> 
   <td colname="col2"> <p class="- topic/p ">Recommends items that are most often purchased in the same session that the specified item is viewed. This criteria returns other products people purchased after viewing this one, the specified product is not included in the results set.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="- topic/p ">People Who Bought This, Bought That</p> </td> 
   <td colname="col2"> <p class="- topic/p ">Recommends items that are most often purchased by customers at the same time as the specified item.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Site Affinity</p> </td> 
   <td colname="col2"> <p>Recommends items based on the certainty of a relationship between items. You can configure this criteria to determine how much data is required before a recommendation is presented using the <span class="wintitle"> Inclusion Rules </span> slider. For example, if you select <span class="wintitle"> very strong </span>, the products with the strongest certainty of a match are recommended. </p> <p>For example, if you set a very strong affinity and your design includes five items, three of which meet the strength of connection threshold, the two items that do not meet the minimum strength requirements are not displayed in your recommendations and are replaced by your defined backup items. The items with the strongest affinity display first.</p> <p>Some customers with diverse product collections and diverse site behaviors might get the best results if they set a weak site affinity.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="- topic/p ">Top Sellers</p> </td> 
   <td colname="col2"> <p class="- topic/p ">The items that are included in the most completed orders. Multiple units of the same item in a single order are counted as one order.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="- topic/p ">Most Viewed</p> </td> 
   <td colname="col2"> <p class="- topic/p ">The items or media that are viewed most often.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Recently Viewed Items/Media</p> </td> 
   <td colname="col2"> <p> Items that have been viewed recently by the visitor. When using this criteria, you should update the <span class="keyword"> Target </span> design to handle cases where blank recommendations would show when there are not enough previously viewed items to display. </p> </td> 
  </tr> 
 </tbody> 
</table>


>[!NOTE] {class="- topic/note "}
>
>If you are running a recommendation and change its criteria, you will lose your reporting data.


You can also use additional known information about a visitor to enhance your recommendations.
All one-day criteria run twice daily. All one-week and longer criteria run once daily. Site Affinity criteria run once daily. Backup criteria run twice daily.
>## Select Criteria {#task_2203616ABBE342B6ADAB08F278D794FA}Select the criteria to use in your 
<keyword>
  Recommendations 
</keyword> activity. 
<draft-comment otherprops="merge">
  recs/t_algo_select_recs.xml 
</draft-comment>You can test multiple recommendation types against each other by adding more than one criteria.
If you select multiple criteria, traffic is split evenly between the selected criteria. For example, if you have selected two criteria and your activity is designed to display default content to 20% of activity entrants, then 40% of activity entrants will see the recommendations controlled by each criteria. There is no option to change the percentages for each criteria.

* To search for an existing criteria (for example, if many criteria cards display), type in the search field until the desired criteria appears, then select the criteria and click ** ` Done` **. 
  Some criteria are supplied with ` Recommendations`. You and your team can also create your own custom criteria. 

* To create a new criteria, click ** ` Create New` **, then fill in the information for the new criteria. For information about creating new criteria, see [ Create a New Criteria ](c_algorithms.md#task_8A9CB465F28D44899F69F38AD27352FE). 


>1. [ Create a new recommendation ](t_create_recs_activity.md#task_6874328773C64C44A73F0A130AD3F96F), or find the recommendation whose criteria you want to set and click ` Edit`.
>1. Select an industry type and a page type.

>    
>    * **Industry Type:**The industry type is used to help categorize ` Recommendations` criteria. To change your default industry vertical, click ** ` Settings` ** and select your desired default ** ` Industry Vertical` ** setting. 

>    * **Page Type:**The page type helps you categorize your recommendations. There are also built-in criteria that can be chosen for each page type. 

>    * **Compatible:**Show only those criteria where the selected page passes the required data. Not every criteria will run correctly on every page. The page or mbox needs to pass in ` entity.id` or ` entity.categoryId` for the current item/current category criteria to be displayed. In general, it is best to show only compatible criteria. However, if you want incompatible criteria to be available for the activity, clear the ** ` Compatible` ** check box. This option can be disabled or enabled in your ` Target` ` Preferences`. 


>1. Click ` Add`.
>## Creating Criteria {#task_8A9CB465F28D44899F69F38AD27352FE}Criteria control the content of your 
<keyword>
  Recommendations 
</keyword> activities. Create criteria to show the recommendations that are most appropriate for your activity. 
<draft-comment otherprops="merge">
  recs/t_create_new_algorithm.xml 
</draft-comment>There are multiple ways to reach the ` Create New Criteria` screen. Some screen options vary depending on how you reach the screen. 

* When you are creating a ` Recommendations` activity, click ** ` Create New` ** on the ` Select Criteria` screen. You will have the option to save your new criteria for use with other ` Recommendations` activities. 

* When you are editing a ` Recommendations` activity, click in a ` Recommendations Location` box on your page, and select ** ` Change Criteria` **. On the ` Select Criteria` screen, click ** ` Create New` **. You will have the option to save your new criteria for use with other ` Recommendations` activities. 

* On the ** ` Recommendations` ** > ** ` Criteria` ** library screen, click ** ` Create Criteria` **. Criteria you create here are automatically made available for all ` Recommendations` activities. 



>1. Click ** ` Create Criteria` ** or ** ` Create New` **.

>       ![](graphics/button_CreateCriteria.png) 
>1. Select ** ` Create Criteria` **.

>       ![](graphics/CreateNewCriteria_full.png) 
>1. Type a ** ` Criteria Name` **.

>       This is the "internal" name used to describe the criteria. For example, you might want to call your criteria "Highest margin products," but you don't want that title to display publicly. See the next step to set the public-facing title.
>1. Type a public-facing ** ` Display Title` ** to appear on the page for any Recommendations that use this criteria.

>       For example, you might want to display "People who viewed this viewed that" or "Similar products" when you use this criteria to show recommendations.
>1. Type a short ** ` Description` ** of the criteria.

>       The description should help you identify the criteria, and might include information about the purpose of the criteria.
>1. Select an ** ` Industry Vertical` **.

>       Other criteria options will change based on the industry vertical you select.
>1. Select a ** ` Page Type` **.

>       You can select multiple page types.
>       Together, the industry vertical and page types are used to categorize your saved criteria, making it easier to reuse criteria for other ` Recommendations` activities. 
>1. Select a ** ` Recommendation Key` **.

>       For more information about basing criteria on a key, see [ Base the Recommendation on a Recommendation Key ](c_algorithms.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B). 
>1. Select the ** ` Recommendation Logic` **.

>       For more information about recommendation logic options, see [ Criteria ](c_algorithms.md#concept_4BD01DC437F543C0A13621C93A302750). 

>       >[!NOTE]
>       >
>       >If you select ** ` Items` **/ ** ` Media with Similar Attributes` **, you will have the option to set [ content similarity rules ](c_algorithms.md#concept_5402DAFA279C4E46A9A449526889A0CB). 
>1. Set the ** ` Data Range` ** to determine the time range of available historical user behavior data to use when determining which recommendations to show.

>       If your site has a lot of traffic and behaviors change frequently, choose a shorter data window. A shorter window enables ` Recommendations` to be more responsive to changes in the market and in your business. For example, a shorter window means that ` Recommendations` will detect changes in visitor behavior as your visitors begin seasonal shopping, such as back-to-school shopping or Christmas, and will recommend items appropriate to those shopping seasons. 
>       If you don't have a lot of data, or visitor behavior does not change frequently, you might select a longer window. However, for many sites, a shorter window results in better recommendations.
>       The available data ranges are:
>    
>    * Two days
>    * One week
>    * Two weeks
>    * One month
>    * Two months

>1. Select the desired ** ` Behavioral Data Source` **: ` mboxes` or ` Analytics`.

>       If you chose ` Analytics`, select the desired report suite. 
>1. Set your ** ` Content` ** rules.

>       Content rules determine what happens if the number of recommended items does not fill your design. For example, if your design has space for five items, but your criteria causes only three items to be recommended, you can leave the remaining space empty, or you can use backup recommendations to fill the extra space.
>       Select the appropriate toggles:
>    
>    * ` Enable Partial Design Rendering` 

>    * ` Show Backup Recommendations` 

>    * ` Recommend Previously Purchased Items` 
>      This setting is based on the ` productPurchasedId`. It is useful if you sell items that people typically purchase only once, such as kayaks. If you sell items that people come back to purchase again, such as shampoo or other personal items, you should disable this option. 


>1. Set your ** ` Inclusion Rules` **.

>       Inclusion rules determine which items will be included in your recommendations. The options available depend on your industry vertical.
>       For more details, see [ Inclusion Rules ](c_algorithms.md#task_28DB20F968B1451481D8E51BAF947079). 
>1. Configure ** ` Attribute Weighting` **.

>       You can add multiple rules to "nudge" the algorithm based on important description or metadata about the content catalog. For example, you can apply a higher weighting to on-sale items so they appear more often in the recommendation.
>       See [ Attribute Weighting ](c_algorithms.md#task_2AEDA0DB15B74770B76F6982B24C2E42). 
>1. When finished, click ** ` Save` **.

>       If you are creating a new ` Recommendations` activity or editing an existing one, the ** ` Save criteria for later` ** check box is selected by default. If you do not want to use the criteria in other activities, clear the check box before saving. 
>## Base the Recommendation on a Recommendation Key {#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B}Recommendations based on keys utilize visitor behavior context to show relevant results. 
<draft-comment otherprops="merge">
  recs/t_rec_key_recs.xml 
</draft-comment>
There are two types of Recommendations:

* **Popularity:**Lists items according to Most Viewed, Top Sold, and Top Metric. The key is empty for popularity criteria. 

* **Key-based:**Comprises the rest of the criteria. Recommendations offers a diverse set of choices with regard to the key type. The options range from "current item" to "profile parameters," which allow you to programmatically set the key of the values to recommend. You can test multiple criteria against each other by basing each criteria on a different key. 


Each criteria is defined in its own tab. Traffic is split evenly across your different criteria tests. In other words, if you have two criteria, traffic is divided equally between them. If you have two criteria and two designs, traffic is split evenly between the four combinations. You can also specify a percentage of site visitors who see the default content, for comparison. In that case, the specified percentage of visitors see the default content, and the rest are split between your criteria and design combinations.

>1. Create a new recommendation, or select an existing recommendation and click ** ` Edit` **.
>1. To change the recommendation key, select the new key from the ` Recommendation Key` drop-down list.

>       Because different logic maps to different recommendations keys, different recommendations lend themselves to placement on different types of pages:


>    <table id="table_D2F606E0723A4A47992CFCF5B5A110E2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Key </th> 
   <th colname="col2" class="entry"> Description </th> 
   <th colname="col03" class="entry"> Logic (Criteria) </th> 
   <th colname="col3" class="entry"> Where on Your Site </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p> <uicontrol>Current Page Activity</uicontrol> </p> </entry> <entry colname="col2"> <p>This set of recommendation types is defined by the visitor's activity on the current page. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Current Item </span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the item the visitor is currently viewing. Recommendations display other items that might interest visitors who are interested in the specified item.</p> <p>When this option is selected, the <span class="codeph"> entity.id </span> value must be passed as a parameter in the display mbox. </p> </td> 
   <td colname="col03"> 
    <ul id="ul_DCDC1D7C1A184087A7880FE3A49CC812"> 
     <li id="li_C8D237612E6B4F0DB732801302587FCD"> <p>Items with similar attributes</p> </li> 
     <li id="li_D1DBE13F53344D2A8ABF455BA883DD08"> <p>People Who Viewed This, Viewed That</p> </li> 
     <li id="li_B39E09076D6746B6BF7BC12320A72871"> <p>People Who Viewed This, Bought That</p> </li> 
     <li id="li_F31C7BF0AE024D8A8097D79D5ABA94F8"> <p>People Who Bought This, Bought That</p> </li> 
     <li id="li_01C45368713E4F3AA26A752F61C6DF05"> <p>Overall behavior</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>Single-item pages, such as product pages.</p> <p>Do NOT use on null search results pages.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Current Category </span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the product category that the visitor is currently viewing. Recommendations display items in the specified product category.</p> <p>When this option is selected, the <span class="codeph"> entity.categoryId </span>value must be passed as a parameter to the display mbox. </p> </td> 
   <td colname="col03"> 
    <ul id="ul_6C0145C493DC4D999041824654A3FD0F"> 
     <li id="li_02B9BDAA806C469A8F1B433B205C761F"> <p>Top Sellers</p> </li> 
     <li id="li_3BAF37AC41B049968FBB34B2DF0F7BD9"> <p>Most Viewed</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>Single-category pages.</p> <p>Do NOT use on null search results pages.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Custom Attribute </span> </p> </td> 
   <td colname="col2"> <p>Recommendation is determined by an item that is stored in a visitor's profile, using either <span class="codeph"> user.&lt;x&gt; </span> or <span class="codeph"> profile.&lt;x&gt; </span> attributes. </p> <p>When this option is selected, the <span class="codeph"> entity.id </span> value must be present in the profile attribute. </p> </td> 
   <td colname="col03"> 
    <ul id="ul_362033C0345E40ED888618762B436B45"> 
     <li id="li_7313061B878D402999FA53C2E5384ACF"> <p>Items with similar attributes</p> </li> 
     <li id="li_2DA5B5EF217F4C56B212E19EE54BDC82"> <p>People Who Viewed This, Viewed That</p> </li> 
     <li id="li_C7BEB965C72544E1BA538FBDF696662F"> <p>People Who Viewed This, Bought That</p> </li> 
     <li id="li_DA421BF2FD314265A72DECE9E025AE86"> <p>People Who Bought This, Bought That</p> </li> 
     <li id="li_4B3B75420FEA481290DC73EDF754F445"> <p>Overall behavior</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>Can be used on any pages.</p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1"> <p> <uicontrol>Custom Profile Attribute</uicontrol> </p> </entry> <entry colname="col2"> <p>For users who use the recommendations and testing and targeting functions of Adobe Target. </p> <p>The recommendation is based on any profile attribute set up for testing. The value for the attribute must resolve to an<codeph> entity.id</codeph>. For example, you might want to keep track of an item someone abandoned in their cart. You could write a profile script that stores that <codeph>entity.id</codeph>, and then deliver recommendations based on that abandoned cart item the next time the visitor returns to the site. </p> </entry> </row> --> 
  <!-- <row> <entry colname="col1"> <p> <uicontrol>Custom Algorithms</uicontrol> </p> </entry> <entry colname="col2"> <p>This set of recommendation types lists any custom algorithms that have been defined. If there are no custom algorithms, this portion of the <wintitle>Recommendation Type</wintitle> list is empty. </p> </entry> </row> --> 
  <!-- <row> <entry colname="col1"> <p> <uicontrol>Past Behavior</uicontrol> </p> </entry> <entry colname="col2"> <p>This set of recommendation types is defined by the past behavior of your site visitors. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Last Purchased Item </span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the last item that was purchased by each unique visitor. This is captured automatically, so no values need to be passed on the page.</p> </td> 
   <td colname="col03"> 
    <ul id="ul_FE8FD3BB489842739CE545B5F2D6642F"> 
     <li id="li_DE45A9AA40AF4D1B9D88E435B60133F2"> <p>Items with similar attributes</p> </li> 
     <li id="li_E789CABB29654586903B151231F39B12"> <p>People Who Viewed This, Viewed That</p> </li> 
     <li id="li_B75E693A26FC434E9EDAA700063E9664"> <p>People Who Viewed This, Bought That</p> </li> 
     <li id="li_5233971798A041A8B32DD8ECA70EF757"> <p>People Who Bought This, Bought That</p> </li> 
     <li id="li_C6760972E028448685373AECF39B311D"> <p>Overall behavior</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>Home page, My Account page, offsite ads.</p> <p>Do NOT use on product pages or pages relevant to purchases.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Last Viewed Item </span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the last item that was viewed by each unique visitor. This is captured automatically, so no values need to be passed on the page.</p> </td> 
   <td colname="col03"> 
    <ul id="ul_59FAA3B61E124E7EACB323328118C5EE"> 
     <li id="li_27C265D3AF6844989EFACF528EB3D05D"> <p>Items with similar attributes</p> </li> 
     <li id="li_8522D197C43744D8B7D7F40BCEA3D514"> <p>People Who Viewed This, Viewed That</p> </li> 
     <li id="li_24BD56FC2B5842598AF08B78EE670EFE"> <p>People Who Viewed This, Bought That</p> </li> 
     <li id="li_ECC258DCD41B48878917E444C9D58B20"> <p>People Who Bought This, Bought That</p> </li> 
     <li id="li_0D6E97DE926D409E9D8DB6E905497A09"> <p>Overall behavior</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>Home page, My Account page, offsite ads.</p> <p>Do NOT use on product pages or pages relevant to purchases.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Most Viewed Item </span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the item that has been viewed most often, using the same method as used for favorite category.</p> <p>This is determined by recency/frequency criteria that works as follows:</p> <p> 
     <ul id="ul_E61195D2C502460CAA77E9A73103EA33"> 
      <li id="li_5BCA28971F084F8C8CFF8C218E71048B"> <p>10 points for first product view</p> </li> 
      <li id="li_F9C6F3319D6E4279AFF3F583A7D8BA67"> <p>5 points for every subsequent view</p> </li> 
      <li id="li_35AAF05DF8E64A8F93B9236F80CDB5C1"> <p>At end of session divide all values by 2</p> </li> 
     </ul> </p> <p>For example, viewing surfboardA then surfboardB in one session results in A: 10, B: 5. When the session ends, you will have A: 5, B: 2.5. If you view the same items in the next session, the values change to A: 15 B: 7.5.</p> </td> 
   <td colname="col03"> 
    <ul id="ul_AAB6FE5593FE4538AFDD1C8823ACCA6E"> 
     <li id="li_4FA53D2E00124FF6B997BFB9E08C86D2"> <p>Items with similar attributes</p> </li> 
     <li id="li_C8ACAB71752C4E6EBD1263E21CA8B4F1"> <p>People Who Viewed This, Viewed That</p> </li> 
     <li id="li_EEE10C05CCAF4EC2B6D44AF41DE97452"> <p>People Who Viewed This, Bought That</p> </li> 
     <li id="li_48BE7837CB9A4B329400D5B9624A3A96"> <p>People Who Bought This, Bought That</p> </li> 
     <li id="li_3C790AA66A8C4515A48625C23E1AC337"> <p>Overall behavior</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>General pages, such as home or landing pages and offsite ads.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Favorite Category </span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the category that has received the most activity, using the same method used for "most viewed item" except that categories are scored instead of products.</p> <p>This is determined by recency/frequency criteria that works as follows:</p> <p> 
     <ul id="ul_568FB583582546C49479197AC416C4A1"> 
      <li id="li_472876E860A6430DB0F50BAD266BC7BC"> <p>10 points for first category view</p> </li> 
      <li id="li_08E2CE83C7174B69BAFBF992204F1E52"> <p>5 points for every subsequent view</p> </li> 
     </ul> </p> <p>Categories visited for the first time are given 10 points. 5 points are given for subsequent visits to the same category. With each visit, non-current categories that have been viewed before are decremented by 1.</p> <p>For example, viewing categoryA then categoryB in one session results in A: 9, B: 10. If you view the same items in the next session, the values change to A: 20 B: 9.</p> </td> 
   <td colname="col03"> 
    <ul id="ul_7C53E286352F419FAFF9FC6F6A000050"> 
     <li id="li_6069417BFB2E4C1FAD7C6548A5FE8919"> <p>Top Sellers</p> </li> 
     <li id="li_466F4985D78042248311BCF770F5C74C"> <p>Most Viewed</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>General pages, such as home or landing pages and offsite ads.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Popularity </span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the popularity of items on your site. Popularity includes top sellers and top viewed by mbox data and, if you use Adobe Analytics, all of the metrics available in the product report. Items are ranked based on the Recommendation Logic you select.</p> </td> 
   <td colname="col03"> 
    <ul id="ul_098AAF8E66894BE58DE0C391CD9F7BE0"> 
     <li id="li_B15E7309E01A44D885334431FFDBDACB"> <p>Top Sellers</p> </li> 
     <li id="li_E05621811A3546699268BAD42646BBD1"> <p>Most Viewed</p> </li> 
     <li id="li_53A03302700D44D98C0D6C87BC907492"> <p>Product report metrics (if you are using Adobe Analytics)</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>General pages, such as home or landing pages and offsite ads.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Recently Viewed Items </span> </p> </td> 
   <td colname="col2"> <p>Uses the visitor's history (spanning sessions) to present the last <i>x</i> items the visitor has viewed, based on the number of slots in the design. </p> <p> <p>Note:  This key does not apply collection restrictions. </p> </p> </td> 
   <td colname="col03"> <p>None</p> </td> 
   <td colname="col3"> <p>General pages, such as home or landing pages and offsite ads.</p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Click ** ` Save` **.
>## Inclusion Rules {#task_28DB20F968B1451481D8E51BAF947079}Use inclusion rules to help you narrow the items that display in your recommendations. Inclusion rules can be used when creating recommendations criteria or promotions. 
<draft-comment otherprops="merge">
  recs/t_data_details.xml 
</draft-comment>Inclusion rules are optional; however, setting these details gives you more control over the items that appear in your recommendations. Each detail you configure further narrows the display criteria.
For example, you can choose to display only women's shoes that have an inventory of more than 50 and a price between $25 and $45. You can also weight each attribute so those items that are more important to your business are most likely to appear.
As another example, you can choose to display job openings to visitors who visit your site only from certain cities and who have the required college degrees.
Inclusion rule options vary by industry vertical. By default, inclusion rules are applied to backup recommendations.

>[!NOTE]
>
>You should use inclusion rules cautiously. They are useful if, for example, your organization has rules that demand that one brand is not recommended while another brand is being shown. However, there is an opportunity cost to this feature. You could possibly lose a percentage of lift by restricting some items from not showing when they would normally be shown by the activity criteria.


The inclusion rules are joined with an AND. All rules must be met to include an item in a recommendation.
To create a simple inclusion rule, as mentioned previously, to display only women's shoes that have an inventory of more than 50 and a price between $25 and $45, perform the following steps:

>1. Set a price range for the products you want to recommend.
>1. Set the minimum inventory amount for the products you want to recommend.
>1. Configure the recommendation to display items only when they meet certain criteria.

>       ![](../target/graphics/Recs_InclusionRules.png) 
>       You can specify that items are included only when one of the attributes in the list meets or does not match one or more specified conditions.
>       The available evaluators depend on the value you choose in the first drop-down. You can list multiple items. These items are evaluated with OR.
>       Multiple rules are combined with an AND.

>       >[!NOTE]
>       >
>       >This option limits the items that are displayed in the recommendation. It does not affect which pages the recommendation is displayed on. To limit where the recommendation displays, select the pages in the experience composer.

>## Attribute Weighting {#task_2AEDA0DB15B74770B76F6982B24C2E42}Use attribute weighting to "nudge" the algorithm so certain items are more likely to be shown. Marketers can influence the algorithm based on important description or metadata about the content catalog. 
<draft-comment otherprops="merge">
  recs/t_attribute_weighting.xml 
</draft-comment>Apply a higher weighting to these on-sale items so they show more often in the recommendation. Non-sale items are not completely excluded, but they appear less often. Multiple weighted attributes can be applied to the same algorithm, and the weighted attributes can be tested on split traffic in the recommendation.
>1. Choose a value.

>       The value determines the type of item that is more likely to display, based on one of several available criteria.
>1. Choose an evaluator.
>1. Type the keyword to complete the rule attributes.

>       For example, the complete rule might be "Category contains shoes."
>       ![](../target/graphics/Recs_AttributeWeighting.png) 
>       If you drag the Attribute Weighting slider all the way to the right, the ` Force to Top` option displays: 
>       ![](../target/graphics/force to top.png) 
>       If the attribute is present, Recommendations automatically forces that value to the front of the recommendation. The Number of Slots box sets how many values you can force to the front of the recommendation.
>1. Select the weight to assign to the rule.

>       Options range from 0 to 100 in increments of 25.
>1. Add additional rules if desired.
>## Content Settings {#concept_BC16005C7A1E4F1A87E33D16221F4A96}The 
<wintitle>
  Content 
</wintitle> settings determine how recommendations display in your design. 
<draft-comment otherprops="merge">
  recs/c_content_settings.xml 
</draft-comment>It is possible for ` Recommendations` criteria to return fewer recommendations than your design calls for. For example, your design may have five available "slots," but the criteria returns only three recommended items. The ` Content` settings control how recommendations are presented when this happens. 
The Enable Partial Design Rendering setting determines what happens if the number of recommended items does not fill your design. For example, if your design has space for five items, but your criteria causes only three items to be recommended, you can leave the remaining space empty, or you can use backup recommendations to fill the extra space. If this setting is enabled, you need to use the velocity code to hide unfilled slots.
Select the appropriate toggles:

* ` Enable Partial Design Rendering` 

* ` Show Backup Recommendations` 

* ` Apply Inclusion Rules to Backup Recommendations` 

* ` Recommend Previously Purchased Items` 
  This setting is based on the ` productPurchasedId`. It is useful if you sell items that people typically purchase only once, such as kayaks. If you sell items that people come back to purchase again, such as shampoo or other personal items, you should disable this option. 


If you enable ** ` Show Backup Recommendations` **, the option to apply your [ inclusion rules ](c_algorithms.md#task_28DB20F968B1451481D8E51BAF947079) to backup recommendations is enabled by default. 
![](../target/graphics/Recs_ContentControls.png) 


<table id="table_C0B893ECCEB4472B848808750C7ADDED"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Partial Design Rendering </th> 
   <th colname="col2" class="entry"> Backup Recommendations </th> 
   <th colname="col3" class="entry"> Result </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Disabled </td> 
   <td colname="col2"> Disabled </td> 
   <td colname="col3"> <p>If fewer recommendations are returned than the design calls for, the recommendations design is replaced by default content and no recommendations are displayed.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enabled </td> 
   <td colname="col2"> Disabled </td> 
   <td colname="col3"> <p>The design is rendered, but may include blank space if fewer recommendations are returned than the design calls for.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enabled </td> 
   <td colname="col2"> Enabled </td> 
   <td colname="col3"> <p>Backup recommendations will fill available design "slots," fully rendering the design.</p> <p>If applying inclusion rules to backup recommendations restricts the number of qualifying backup recommendations to the point that the design cannot be filled, the design is partially rendered.</p> <p>If the criteria does not return any recommendations, and inclusion rules restrict backup recommendations to zero, the design is replaced with default content.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Disabled </td> 
   <td colname="col2"> Enabled </td> 
   <td colname="col3"> <p>Backup recommendations will fill available design "slots," fully rendering the design.</p> <p>If applying inclusion rules to backup recommendations restricts the number of qualifying backup recommendations to the point that the design cannot be filled, the design is replaced by default content and no recommendations are displayed.</p> </td> 
  </tr> 
 </tbody> 
</table>

>## Content Similarity {#concept_5402DAFA279C4E46A9A449526889A0CB}Use 
<wintitle>
  Content Similarity 
</wintitle> rules to make recommendations based on item or media attributes. 
<draft-comment otherprops="merge">
  recs/c_content_similarity.xml 
</draft-comment>Content similarity compares item attribute keywords and makes recommendations based on how many keywords different items have in common. Recommendations based on content similarity do not require past data to deliver strong results.
Using content similarity to generate recommendations is especially effective for new items, which are not likely to show up in recommendations using *People Who Viewed This, Viewed That* and other logic based on past behavior. You can also use content similarity to generate useful recommendations for new visitors, who have no past purchases or other historical data. 
When you select ** ` Items` **/ ** ` Media with Similar Attributes` **, you have the option to create rules to increase or decrease the importance of specific item attributes in determining recommendations. For items such as books, you might want to boost the importance of attributes like *genre*, *author*, *series*, and so on, to recommend similar books. 
![](graphics/ContentSimilarity.png) 
Because content similarity uses keywords to compare items, some attributes, such as *message* or *description*, can introduce "noise" into the comparison. You can create rules to ignore these attributes. 
By default, all attributes are set to *Baseline*. You do not need to create a rule unless you want to change this setting. 
>## Creating Criteria Sequences {#task_78D0E107652E4FECA0A44F3D6728C229}Use sequences of up to five criteria to exercise greater control of the items that appear in your 
<wintitle>
  Recommendations 
</wintitle> activities. 
<draft-comment otherprops="merge">
  recs/t_create_criteria_sequence.xml 
</draft-comment>
>[!NOTE]
>
>Criteria sequences cannot be used with ` Recommendations` activities created before the October 2016 Release of ` Target Premium`. 


To create a criteria sequence, you must first create the criteria you want to include in the sequence. See [ Creating Criteria ](c_algorithms.md#task_8A9CB465F28D44899F69F38AD27352FE) for more information. 
By using a criteria sequence, you can provide additional targeted recommendations, instead of using more generic backup recommendations, when a criteria doesn't return enough results to fill your design. Typically, a criteria sequence will proceed from more specific targeting, which may return fewer results, to more general targeting, which usually returns more results.
For example, a product page criteria sequence might follow this order:

1. Based on current item, from same brand

1. Based on current item, from all brands

1. Based on content similarity

1. Based on top sellers

1. Based on most-viewed items across the site


A home page criteria sequence might follow this order:

1. Based on visitor's last purchase

1. Based on visitor's favorite item

1. Based on visitor's favorite category

1. Based on top sellers

1. Based on most-viewed across site


There are multiple ways to reach the ` Create Criteria Sequence` screen. Some screen options vary depending on how you reach the screen. 

* When you are creating a ` Recommendations` activity, click ** ` Create New` ** > ** ` Create Criteria Sequence` ** on the ` Select Criteria` screen. You will have the option to save your new criteria sequence for use with other ` Recommendations` activities. 

* When you are editing a ` Recommendations` activity, click in a ` Recommendations Location` box on your page, and select ** ` Change Criteria` **. On the ` Select Criteria` screen, click ** ` Create New` ** > ** ` Create Criteria Sequence` **. You will have the option to save your new criteria for use with other ` Recommendations` activities. 

* On the ** ` Recommendations` ** > ** ` Criteria` ** library screen, click ** ` Create Criteria` ** > ** ` Create Criteria Sequence` **. Criteria you create here are automatically made available for all ` Recommendations` activities. 



>1. Click ** ` Create Criteria` ** or ** ` Create New` **.

>       ![](graphics/button_CreateCriteria.png) 
>1. Select ** ` Create Criteria Sequence` **.

>       ![](graphics/CreateCriteriaSequence.png) 
>1. Type a ** ` Name` ** for the sequence.

>       This is the "internal" name used to describe the criteria sequence. Visitors to your site will not see this name.
>1. Type a public-facing ** ` Generic Display Title` ** to appear on the page if multiple criteria in the sequence are used to fill the ` Recommendations` design.

>       For example, you might want to replace "Customers who viewed this also viewed..." with "Recommended for You" if the design might include items based on more than one ` Recommendations` key. 
>1. Type a short ** ` Description` ** of the criteria sequence.

>       The description should help you identify the criteria sequence, and might include information about its purpose.
>1. Select an ** ` Industry Vertical` **.

>       Your default industry vertical appears automatically.
>1. Select a ** ` Page Type` **.

>       You can select multiple page types.
>       Together, the industry vertical and page types are used to categorize your saved criteria sequence, making it easier to reuse sequences for other ` Recommendations` activities. 
>1. Set your ** ` Content` ** rules.

>       When you create a criteria sequence, backup recommendation and partial design rendering settings are ignored for the individual criteria the make up the sequence. To use backup recommendations and partial design rendering you must enable them for the sequence. Select the appropriate toggles. If you choose to allow backup recommendations, you can also choose whether to apply inclusion rules to the backups.
>1. Set the sequence order.

>    
>    1. Click ** ` Add Criteria` **. 

>    1. On the Add Criteria screen, select a criteria.

>    1. Click ** ` Add` **. 

>       You can add up to five criteria to a sequence.
>1. Click ** ` Save` **.

>       ![](graphics/CriteriaSequenceCard.png) 
>       For more information about recommendation logic options, see [ Criteria ](c_algorithms.md#concept_4BD01DC437F543C0A13621C93A302750). 
>## Uploading Custom Criteria {#task_1BBA49883E794670A09F0ABE1B3F4288}Upload a CSV file to customize your recommendations. 
<draft-comment otherprops="merge">
  recs/t_recommendations_csv.xml 
</draft-comment>There are multiple ways to reach the ` Create New Criteria` screen. Some screen options vary depending on how you reach the screen. 

* When you are creating a ` Recommendations` activity, click ** ` Create New` ** on the ` Select Criteria` screen. You will have the option to save your new criteria for use with other ` Recommendations` activities. 

* When you are editing a ` Recommendations` activity, click in a ` Recommendations Location` box on your page, and select ** ` Change Criteria` **. On the ` Select Criteria` screen, click ** ` Create New` **. You will have the option to save your new criteria for use with other ` Recommendations` activities. 

* On the ** ` Recommendations` ** > ** ` Criteria` ** library screen, click ** ` Create Criteria` **. Criteria you create here are automatically made available for all ` Recommendations` activities. 


>1. Click ** ` Create Criteria` **.

>       ![](graphics/button_CreateCriteria.png) 
>1. Select ** ` Upload Custom Criteria` **.

>       ![](graphics/CreateNewCriteria_csv.png) 
>1. Type a ** ` Criteria Name` **.

>       This is the "internal" name used to describe the criteria. 
>1. Type a public-facing ** ` Display Title` ** to appear on the page for any recommendations that use this criteria.

>       For example, you might want to display "People who viewed this viewed that" or "Similar products" when you use this criteria to show recommendations.
>1. Type a short ** ` Description` ** of the criteria.

>       The description should help you identify the criteria, and might include information about the purpose of the criteria.
>1. Select an ** ` Industry Vertical` **.

>1. Select a ** ` Page Type` **.

>       You can select multiple page types.
>       Together, the industry vertical and page types are used to categorize your saved criteria, making it easier to reuse criteria for other ` Recommendations` activities. 
>1. Select a ** ` Recommendation Key` **.

>       For more information about basing criteria on a key, see [ Base the Recommendation on a Recommendation Key ](c_algorithms.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B). 
>1. Set your ** ` Content` ** rules.

>       Content rules determine what happens if the number of recommended items does not fill your design. For example, if your design has space for five items, but your criteria causes only three items to be recommended, you can leave the remaining space empty, or you can use backup recommendations to fill the extra space. Select the appropriate toggles. See [ Content Settings ](c_algorithms.md#concept_BC16005C7A1E4F1A87E33D16221F4A96). 
>1. Set your ** ` Inclusion Rules` **.

>       [ Inclusion Rules ](c_algorithms.md#task_28DB20F968B1451481D8E51BAF947079)1. Select the ** ` Location` ** of your CSV file.

>       The CSV file must be formatted correctly to upload successfully. Click ** ` Download the CSV template` ** to get a correctly formatted CSV file. 
>       You have two location options:
>    
>    * **FTP:**To upload your CSV file from an FTP server, select ** ` FTP` **, then enter the required information. You have the option to use SSL, which uses the FTPS protocol to transfer your CSV file securely. 

>    * **URL:**To upload your CSV file from a URL, select ** ` URL` **, then and enter a feed URL. 


>1. Click ** ` Save` **.


>       >[!NOTE]
>       >
>       >Custom criteria entities (rows) can contain up to 500 recommended items (columns).

