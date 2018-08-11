---
description: Use settings to manage your Recommendations implementation.
keywords: Recommendations;settings;preferences;industry vertical;filter incompatible criteria;default host group;thumb base url;recommendation api token
seo-description: Use settings to manage your Recommendations implementation.
seo-title: Settings
solution: Target
title: Settings
title_outputclass: premium
topic: Premium
uuid: 25b9a2ed-b0a8-4aaa-a80a-eb8f58bce26c
badge: assets/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Settings

To access the [!UICONTROL  Recommendations Settings] options, open [!DNL  Target] in the [!DNL  Adobe Experience Cloud], then click ** [!UICONTROL  Recommendations] ** > ** [!UICONTROL  Settings] **. 

![](/migration-test-20180813/assets/recs settings.png) 

The following options are available: 



<table id="table_64B65F53C8904026BD4031E749AA3625"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Custom Global Mbox </p> </td> 
   <td colname="col2"> <p>(Optional) Specify the custom global mbox used to serve <span class="keyword"> Target</span> activities. By default, the global mbox used by <span class="keyword"> Target</span> is used for <span class="keyword"> Recommendations</span>. </p> <p> <p>Note: This option is set on the <span class="wintitle"> Target Setup</span> page. Open <span class="keyword"> Target</span>, then click <span class="uicontrol"> Setup</span>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Industry Vertical </p> </td> 
   <td colname="col2"> <p>The industry vertical is used to help categorize your recommendations criteria. This helps members of your team find criteria that make sense for a particular page, such as criteria that are best for the shopping cart page or for a media page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Filter Incompatible Criteria </p> </td> 
   <td colname="col2"> <p>Enable this option to show only those criteria where the selected page passes the required data. Not every criteria will run correctly on every page. The page or mbox needs to pass in<span class="codeph"> entity.id</span> or<span class="codeph"> entity.categoryId</span> for the current item/current category recommendations to be compatible. In general, it is best to show only compatible criteria. However, if you want incompatible criteria to be available for the activity, uncheck this option. </p> <p> It is recommended that you disable this option if using a tag management solution. </p> <p>For more information about this option, see <a href="c_recommendations-faq.xml#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Recommendations FAQ</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Default Host Group </p> </td> 
   <td colname="col2"> <p>Select your default host group. None means that your<span class="wintitle"> Default Host Group for Reporting</span> setting in <span class="keyword"> Target Classic</span> is used for your default host group. </p> <p>The host group provides the environment where the products are hosted. You can only preview from one given host group at a time. The numbers and update information that show in the Collection list all come from that host group. Likewise, the delivery depends on your host group. </p> <p>If you don't see your products, make sure that you are using the correct host group. For example, if you set up your recommendation to use a staging environment and you set your host group to Staging, you might need to re-create your collections in the staging environment for the products to show. </p> <p>To see which products are available in each environment, use Catalog Search with each environment. </p> <p>For more information about host groups, see <a href="../ov2/c_hosts.xml#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> Hosts</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Thumbnail Base URL </p> </td> 
   <td colname="col2"> <p>Setting a base URL for your product catalog makes it possible to use relative URLs when specifying thumbnails of your products when passing in your thumbnail URL. </p> <p>For example: </p> <p> <span class="codeph"> "entity.thumbnailURL=/Images/Homepage/product1.jpg"</span> </p> <p>sets a URL relative to the thumbnail base URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Recommendation API Token </p> </td> 
   <td colname="col2"> <p>Use this token in Recommendations API calls, such as the Download API. </p> </td> 
  </tr> 
 </tbody> 
</table>

