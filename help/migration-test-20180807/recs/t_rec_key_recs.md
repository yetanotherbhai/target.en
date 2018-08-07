---
description: You can create multiple recommendation keys and test them against each other.
keywords: recommendation key;recommendation logic;recommendation page types
seo-description: You can create multiple recommendation keys and test them against each other.
seo-title: Base the Recommendation on a Recommendation Key
solution: Target
title: Base the Recommendation on a Recommendation Key
topic: Premium
uuid: ee0d9525-fdc9-45fc-b8d6-96694400ad8f
index: y
internal: n
snippet: y
translate: y
---

# Base the Recommendation on a Recommendation Key

Each criteria is defined in its own tab. Traffic is split evenly across your different criteria tests. In other words, if you have two criteria, traffic is divided equally between them. If you have two criteria and two designs, traffic is split evenly between the four combinations. You can also specify a percentage of site visitors who see the default content, for comparison. In that case, the specified percentage of visitors see the default content, and the rest are split between your criteria and design combinations.

>1. Create a new recommendation, or select an existing recommendation and click ** `Edit` **.
>1. To change the recommendation key, select the new key from the `Recommendation Key` drop-down list.

>       Because different logic maps to different recommendations keys, different recommendations lend themselves to placement on different types of pages:


>    <table id="table_D2F606E0723A4A47992CFCF5B5A110E2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Key</th> 
   <th colname="col2" class="entry">Description</th> 
   <th colname="col03" class="entry">Logic (Criteria)</th> 
   <th colname="col3" class="entry">Where on Your Site</th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p> <uicontrol>Current Page Activity</uicontrol> </p> </entry> <entry colname="col2"> <p>This set of recommendation types is defined by the visitor's activity on the current page. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol">Current Item</span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the item the visitor is currently viewing. Recommendations display other items that might interest visitors who are interested in the specified item.</p> <p>When this option is selected, the <span class="codeph">entity.id</span> value must be passed as a parameter in the display mbox. </p> </td> 
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
   <td colname="col1"> <p> <span class="uicontrol">Current Category</span> </p> </td> 
   <td colname="col2"> <p>The recommendation is determined by the product category that the visitor is currently viewing. Recommendations display items in the specified product category.</p> <p>When this option is selected, the <span class="codeph">entity.categoryId</span>value must be passed as a parameter to the display mbox. </p> </td> 
   <td colname="col03"> 
    <ul id="ul_6C0145C493DC4D999041824654A3FD0F"> 
     <li id="li_02B9BDAA806C469A8F1B433B205C761F"> <p>Top Sellers</p> </li> 
     <li id="li_3BAF37AC41B049968FBB34B2DF0F7BD9"> <p>Most Viewed</p> </li> 
    </ul> </td> 
   <td colname="col3"> <p>Single-category pages.</p> <p>Do NOT use on null search results pages.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol">Custom Attribute</span> </p> </td> 
   <td colname="col2"> <p>Recommendation is determined by an item that is stored in a visitor's profile, using either <span class="codeph">user.&lt;x&gt;</span> or <span class="codeph">profile.&lt;x&gt;</span> attributes. </p> <p>When this option is selected, the <span class="codeph">entity.id</span> value must be present in the profile attribute. </p> </td> 
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
   <td colname="col1"> <p> <span class="uicontrol">Last Purchased Item</span> </p> </td> 
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
   <td colname="col1"> <p> <span class="uicontrol">Last Viewed Item</span> </p> </td> 
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
   <td colname="col1"> <p> <span class="uicontrol">Most Viewed Item</span> </p> </td> 
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
   <td colname="col1"> <p> <span class="uicontrol">Favorite Category</span> </p> </td> 
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
   <td colname="col1"> <p> <span class="uicontrol">Popularity</span> </p> </td> 
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
   <td colname="col1"> <p> <span class="uicontrol">Recently Viewed Items</span> </p> </td> 
   <td colname="col2"> <p>Uses the visitor's history (spanning sessions) to present the last <i>x</i> items the visitor has viewed, based on the number of slots in the design. </p> <p> <p>Note: This key does not apply collection restrictions.</p> </p> </td> 
   <td colname="col03"> <p>None</p> </td> 
   <td colname="col3"> <p>General pages, such as home or landing pages and offsite ads.</p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Click ** `Save` **.
