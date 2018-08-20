---
description: This document lists the new features and bug fixes for recent releases.
keywords: recommendation classic release notes;recs classic release notes;recs release notes
seo-description: This document lists the new features and bug fixes for recent releases.
seo-title: Release Notes
solution: Target
title: Release Notes
topic: Recommendations
uuid: dad7b052-9afa-4a32-816e-1a7df7571e80
index: y
internal: n
snippet: y
translate: y
---

# Release Notes


<a id="section_29D78E4688D74BD3BC334B94527118A9"></a>

To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update: 

[ https://campaign.adobe.com/webApp/adbePriorityProductSubscribe ](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) 

## Adobe Recommendations Classic 17.8.1 (August 16, 2017) {#section_257662F0265944B2A6575A90EEF1B226}

This release includes the following feature update: 

<table id="table_C3782E920C4149DFB244D597E986E818"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="c_rec_mng_recs/c_Managing_Templates/c_Customizing_a_Template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59" format="dita" scope="local"> Customizing a Template </a> </p> </td> 
   <td colname="col2"> <p>The following variables are available as Velocity arrays. As such, they can be iterated over or referenced via index. </p> <p> 
     <ul id="ul_669416209BC34739A0CDFF94C29BF787"> 
      <li id="li_BF2AC07A641242729EEC2E9A393956F0"> <p> <span class="codeph"> entities </span> </p> </li> 
      <li id="li_35E9BCD4079C455E85A0C23CCEFDED42"> <p> <span class="codeph"> entityN.categoriesList </span> </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Recommendations Classic 16.10.1 (October 25, 2016) {#section_3D23B70434CE4B25BF5500818F249154}

This release does not include any new customer-facing features or enhancements. 

## Adobe Recommendations Classic 16.9.1 (September 20, 2016) {#section_58DBA8D322854153B204F6C6B4E843A7}

This release does not include any new customer-facing features or enhancements. 

## Adobe Recommendations Classic 16.8.1 (August 16, 2016) {#section_5CD15C25A8124176951F625A6AA8DF05}

This release does not include any new customer-facing features or enhancements. 

## Adobe Recommendations Classic 16.7.1 (July 20, 2016) {#section_B702337681FB488581C951FE35FE0523}

This release includes the following feature update: 

<table id="table_EEBD493F06A240D990FCF47C6FF5A019"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Multi-valued Recommendations attributes </p> </td> 
   <td colname="col2"> <p>All custom Recommendations attributes can now contain multiple entity values. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Recommendations Classic 16.6.1 (June 14, 2016) {#section_805BC85018A643118AB8480F358C3C11}

This release doesn't include any customer-facing enhancements. 

## Adobe Recommendations Classic 16.5.1 (May 18, 2016) {#section_2DEC936D28C54E529CF6294D9DCC3FBC}

This release includes the following enhancement: 



<table id="table_C9304491B4734A83976D5CD1A2DEF715"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Recommendations CSV download </td> 
   <td colname="col2"> <p>CSV downloads now have a line for all environments, including those that do not have entity recommendations (for example: 
     <systemoutput>
       # environment: 1724 
     </systemoutput>). </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Recommendations Classic 16.4.1 (April 14, 2016) {#section_73DEFBD0EFA542F8A01B22A94B439CF2}

This release includes the following enhancement: 

<table id="table_BD8BF52A2F2A4CB79B71E54393CACE38"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Inclusion rules can be enabled for backup recommendations. </td> 
   <td colname="col2"> <p>When backup recommendations are enabled, you can select an option to apply inclusion rules to backup recommendations. For more information, see <a href="c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/c_content_serve_settings.md#concept_828721CF007E430DAC6E9ABFCDFA5CA4" format="dita" scope="local"> Content Serve Settings </a>. </p> <p> Previously, inclusion rules were applied by default if backup recommendations were enabled. </p> </td> 
  </tr> 
 </tbody> 
</table>

This release includes the following change: 

<table id="table_A10FAC216FDA48D4B2D81A889D6273AC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Custom criteria support added to Honeybee API. </td> 
   <td colname="col2"> <p>The Honeybee API custom criteria replaces the <span class="filepath"> .xml </span> file format of the legacy custom algorithm with <span class="filepath"> .csv </span>, which is more compact and easier to generate, and supports a larger number of recommendations. </p> <p>For API documentation, see <a href="https://www.adobe.io/products/target/docs/reference/recommendations" format="https" scope="external"> https://www.adobe.io/products/target/docs/reference/recommendations </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recommendations Classic access enabled via Analytics Tools menu. </td> 
   <td colname="col2"> Access to Recommendations Classic can now be found in the <span class="uicontrol"> Tools </span> menu of the Analytics solution on <a href="https://my.omniture.com" format="https" scope="external"> https://my.omniture.com </a>. <p style="text-align: center;"> <img href="assets/Menu_Recommendations.png" scale="75" id="image_D7C47CB455C241E197862D25E6D1D481" /> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Recommendations Classic 16.3.1 (March 16, 2016) {#section_CE3FE39774A647A8B39E81E57878814B}

This release includes the following enhancements: 



|  Enhancement  | Description  |
|---|---|
|  Catalog search collection/exclusion enhancement  | It is now possible to create collections/exclusions using valueIsPresent and valueIsNotPresent operands in catalog search.  |

This release includes the following fixes: 


* Fixed issue that caused dynamic filtering to fail when attribute names include the underscore (_) character.


## Adobe Recommendations Classic 16.2.1 (February 18, 2016) {#section_D38B65833A3D4471A18D0187B6A97CBA}

This release includes the following enhancements: 



|  Enhancement  | Description  |
|---|---|
|  Download-only activities now run beyond 21 days.  | Download recommendations can now be activated so the algorithm will continue to run past 21 days.  |


## Adobe Recommendations Classic 16.1.1 (January 19, 2016) {#section_84DD11D085724BCDB1E23CCDD33BE91F}

This release includes the following enhancements: 



<table id="table_A979C7B600904FA99C25160A9ACB5566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Support for "&amp;amp;" character added in category values </td> 
   <td colname="col2"> The "&amp;amp;" character is now supported in category values. Previously, the "&amp;amp;" character caused recommendations to display incorrectly. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Custom algorithm limits increased </td> 
   <td colname="col2"> <p> You can now use post for the Custom algorithm API. </p> <p>For GET and POST custom algorithm upload the 1000 key limit has been removed. Depending on your data around 1000 entity keys can be used for Get and about 25K keys with POST . However, no single key can have more than 500 values. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Onsite links have been deprecated from the Recommendations Classic interface </td> 
   <td colname="col2"> <p>To manually specify a mbox for your recommendation, use the following workaround: </p> <p> On the Recommendations Edit page in your browser URL append <span class="codeph"> &amp;amp;mbox=NAME_OF_MBOX </span> and press <span class="uicontrol"> Enter </span>. </p> <p>This populates the mbox name in the mbox dropdown. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximum characters allowed in feed name increased </td> 
   <td colname="col2"> <p>Feed names can now contain 250 characters. The previous limit was 64. </p> </td> 
  </tr> 
 </tbody> 
</table>

This release includes the following enhancements: 



<table id="table_A5921AF48F074813A9F748044C9A7AE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Google Product XML feeds improvements </td> 
   <td colname="col2"> 
    <!--RECS-3567--> <p> Google Product XML feeds now support both RSS2 version and ATOM 1.0 version. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Recommendations Classic 15.7.1 (July 23, 2015) {#section_D062AD5AA91D4017977F75B0326D37E1}

There are currently no customer-facing features scheduled for release this month. 

This release includes the following fixes: 


* The limit on the number of custom algorithms that can be uploaded has been increased.
* Intermittent Recommendations mbox refresh and host group loading issues have been addressed.


## Recommendations Classic 15.2.2 (February 10, 2015) {#section_CB0EAB95716548FEA6D0471FD0559008}

This release includes the following enhancements: 



<table id="table_72F4B3A48F984348996877248902363B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Past-behavior algorithms now provide more than only the last-viewed items. </p> </td> 
   <td colname="col2"> <p>Some past-behavior algorithms have been renamed. Also, options have been added to past-behavior algorithms that allow you to key off of more than the last-viewed item. </p> <p> 
     <ul id="ul_D6E7F3E443134A939173F6AA3A428710"> 
      <li id="li_45205B2BD4A6443DA54E045FBF6A1218"> Last Purchased Item <p><b>Renamed:</b> nth last purchased entity </p> </li> 
      <li id="li_3B67EC2974FA48C9A886FE2A4A839F91">Last Viewed Item <p><b>Renamed:</b> nth last viewed entity </p> </li> 
      <li id="li_C9979FFA583346538653821F3F5C434C">Most Viewed item <p><b>Renamed:</b> nth most viewed entity </p> </li> 
      <li id="li_3903A218C05F4BBF991FADE0222C70BD"> Favorite Category <p><b>Renamed:</b> nth most favorite category </p> </li> 
     </ul> </p> <p>In addition, you can choose from three Cascading options when using these keys, to determine how your Recommendations template is filled based on the selected key. </p> <p>For more information, see <a href="c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_rec_key_recs.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B" format="dita" scope="local"> Basing the Recommendation on a Recommendation Key </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Improved recently viewed items. </p> </td> 
   <td colname="col2"> <p>Catalogs and exclusion rules are now applied to recently viewed items. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Feed enhancement. </p> </td> 
   <td colname="col2"> <p>RSS2.0 feeds are now supported. </p> </td> 
  </tr> 
 </tbody> 
</table>

This release includes the following fixes: 


* Fixed an issue where "Include Only When" filters were not applied to backup recommendations.


## Recommendations 15.1.1 {#section_096DCBA473334DF68BB243A9E5CD0CF0}

This release includes the following enhancements: 



<table id="table_D0DD38395B6C4CB4BD334A02C7487AA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Allow for past behavior algorithms to serve more than just the last viewed item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Improved exclusion rules </td> 
   <td colname="col2"> <p>Exclusion rules are now applied to recently viewed items. </p> </td> 
  </tr> 
 </tbody> 
</table>

This release includes the following fixes: 


* Fixed an issue that prevented navigating directly to product search result pages having more than 3 digits.
* Fixed a bug where the most viewed algorithm wasn't ranking products as expected.


## Recommendations 14.9.x {#section_5261669054654789AA96679AF4FA04BB}

This release includes the following enhancements: 

<table id="table_B4D41988B98C47AD894CCD7E73AC5E96"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Previously, if the number of recommended items was less than the number of "slots" defined in a template, the template was not transformed to html. This partial rendering behavior can now be set at the algorithm level. </p> <p>A checkbox has been added to the Content Serve Settings on the Recommendations Edit tab, as well as a modification to the existing Recommendation create/update API to enable the rendering of a partial template. </p> <p> If partial template rendering is not enabled, the old functionality will exist; if there aren't enough recommended entities to fill all the slots, the entire template will not be rendered. </p> <p> If partial template rendering is enabled, Recommendations renders the template whether or not enough recommendations exist to fill up all the slots in the template. You will have to build your templates to account for this. For example, you might create your template to include null checks. </p> <p>See <a href="c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/c_content_serve_settings.md#concept_828721CF007E430DAC6E9ABFCDFA5CA4" format="dita" scope="local"> Content Serve Settings </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Allow Backup recommendations to be disabled at the Algorithm level. </td> 
   <td colname="col2"> <p>Added the ability to disable the appending of backups to recommendations at the algorithm level, using a checkbox located in the Content Serve Settings on the Recommendations Edit tab. Previously, this was only available at the client level. </p> <p>The value of the new field is set based on the current value of the client-level setting. </p> <p>See <a href="c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/c_content_serve_settings.md#concept_828721CF007E430DAC6E9ABFCDFA5CA4" format="dita" scope="local"> Content Serve Settings </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Custom algorithm updates for partial template rendering and disabled backup recommendations need to be set via the custom algorithm API: 

` &amp;disableBackup=[true|false]&amp;allowPartialTemplate=[true|false]` 

## Recommendations 14.8 {#section_688D1739C49C4671ABD7D6C3038E6395}

This release includes the following enhancements: 

<table id="table_F51024224E474A179ACF728E4445645D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> Algorithm name and environment ID details are included when there is only one algorithm returned. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Backup recommendations are included for Report Suite data sourced Affinity algorithms. </td> 
   <td colname="col2"> <p>This enhancement fixes an issue that sometimes prevented backup recommendations from being served. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Recommendations 14.6 {#section_1FE4C29A60BB456FBBC5253A994D0743}

This release includes the following changes: 

* Adobe Analytics traffic classification at the product level is no longer supported.
* Recommendations now supports *` pageURL`* and *` thumbnailURL`* variations of *` pageUrl`* and *` thumbnailUrl`*. Additionally *` entity.categoryId`* is treated similarly to *` entity.category`* in that it supports multiple values.

## Recommendations 14.5 {#section_95863B5839F54B5A9C58569253E789C8}

This release adds support for Past Behavior-based recommendations. These recommendations work across sessions, and include recently viewed items. 

## Recommendations 14.1-TR-2.15.5 {#section_87672D183BF14B98B00BEA694CE0EAE9}

This release includes the following enhancement: 

|  Enhancement  | Description  |
|---|---|
|  Increase the number of data feeds shown to users on the **[!UICONTROL  Product]** > **[!UICONTROL  Feeds and Uploads]** page.  | Previously, Recommendations displayed the last five data feeds on the [!UICONTROL  Feeds and Uploads] page, although the entire history was stored. You can now use a URL parameter to configure how many days back are shown in the data feed history.  |

This release also includes the following fixes: 


* Fixed an issue where different versions of the Recommendations algorithms returned different information.
* Improved the report suite feeds using a new compression technique. This fixes an issue where report suite feeds sometimes failed due to an unexpected EOF error.


## Recommendations 2.15c {#section_3EFAFDA21850475A9E5EF71AA2F12A5A}

This release includes the following change: 

|  Feature  | Description  |
|---|---|
|  Scheduled .csv file upload for Recommendations  | Schedule uploads of .csv formatted product feeds from a FTP or HTTP location into Recommendations.  |


## July 2013 {#section_520AA9A624CA4972B9B0215D8F3683F2}

This release (2.15) includes the following changes: 



|  Feature  | Description  |
|---|---|
|  Recently Viewed Items algorithm  | Shows items that have been viewed recently. See [ Selecting an Algorithm ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_algo_select_recs.md#task_2203616ABBE342B6ADAB08F278D794FA)  |
|  Dynamically Exclude Entity recommendations  | Exclude certain items from being shown, such as items that are already in the cart. See [ Dynamically Excluding an Entity ](c_rec_mng_recs/c_Managing_Recommendations_Settings/c_dynamically_excluding_an_entity.md#concept_3CDCE863200A4EE191DA0668131C5858).  |
|  Support for host groups with custom algorithms  | A "host group name" attribute has been added to custom algorithms. If no host group name is specified, the default host group is used. See [ Uploading Custom Algorithm Data ](c_rec_mng_recs/c_Creating_a_Custom_Algorithm/r_Uploading_Custom_Algorithm_Data.md#reference_F905A439D6034D15AAE171CD69909742).  |
|  Support for multiple environments added to production back fill  | Previously, the default Production host group was hard-coded as the source for backfill. Now you can choose the source for the backfill. This setting must be set by Adobe Client Care. See [ Backfilling Environments with Production Data ](c_rec_mng_recs/c_backfilling_environments_with_production_data.md#concept_E479BA8C271842178D800577152B3231).  |

This release includes the following fix: 


*


## March 2013 {#section_3FA9CAD3C4CC4236A8530A8B011C9677}

This release of Recommendations (2.14) includes the following changes: 

[!DNL  Recommendations] is now an integral capability within [!DNL  Adobe] [!DNL  Target]. [!DNL  Adobe Target], part of the [!DNL  Adobe Marketing Cloud], is a solution that provides data-driven personalization for revenue impact by leveraging the integrated capabilities of [!DNL  Test&Target], [!DNL  Test&Target 1:1] (Automated Behavioral Targeting), Geo-targeting, Analytics-Powered Targeting, [!DNL  Recommendations] and [!DNL  Search&Promote]. Many of our upcoming upgrades within the tool will support new efficiencies in data/profile integration, extended algorithm options, and campaign creation / deployment within [!DNL  Recommendations]. Inherent benefits will include stronger collaboration with the other [!DNL  Adobe Target] capabilities, as well as across the [!DNL  Adobe Marketing Cloud]. 



<table id="table_EE462DB2F87E4E2B8CC314263A53B26B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Mbox selection via dropdown </td> 
   <td colname="col2"> All available mboxes are listed in a dropdown on the Recommendations edit page. Browsing your site to find the mbox is no longer required. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mbox Delivery Targeting </td> 
   <td colname="col2"> Recommendations can be limited to show only in mboxes when certain conditions are met. These can include matching particular URL values, mbox parameter values, or profile values. These rules are reevaluated on every mbox request. With this new ability, multiple recommendations can be set up on one mbox name but displayed in different circumstances. For example: one recommendation can display on women's product pages by targeting the mbox to URL contains <span class="codeph"> /women/ </span> and show on men's product pages when the URL contains <span class="codeph"> /mens/ </span>, even if the same mbox name is used across all product pages. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Improved support for multiple client environments (host group management) </td> 
   <td colname="col2"> <p>The following improvements have been made to support multiple host group environments: </p> <p> 
     <ul id="ul_4105EF4AA2A74CE4B4E04BB3C1A9CBD5"> 
      <li id="li_B5AE4AF436B24BD49B70A7CCE68450C4">Host groups can be selected for display in reports. <p>The report for the host group that is set as the default displays unless a different host group is selected. </p> </li> 
      <li id="li_9C02065130124DB98068A1AD1A67EBCF">The host group displays on the search details page. </li> 
      <li id="li_A69A77710FD24C38B88719CCC9FD49A8">Multiple host groups can be set when uploading a CSV file and when setting up a feed. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> The inclusion filter has been enhanced to include a "does not match" option. </td> 
   <td colname="col2"> Data can now be included when an attribute does not match the key's attribute. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multiple filter inclusion rules </td> 
   <td colname="col2"> Multiple "Include Only When" filters can be used. When more than one filter is used, the filters are combined with an AND. </td> 
  </tr> 
 </tbody> 
</table>


## September 2012 {#section_E3181F518FD1490495AEC404B1C1CA47}

This release of Recommendations includes the following changes: 

**Change to recommendation cards** 

If you are not testing against default content, the lower bar no longer appears on the recommendations card. See [ Recommendations Cards ](c_rec_mng_recs/c_Viewing_a_Recommendation_in_the_Recommendations_Manager/r_card_understanding_recs.md#reference_5F99F1159DD741CCB92963C9B32C28B0) 

**Changed algorithm data source** 

In past releases, only the Site Affinities algorithm used DataWarehouse data. In this release, View Affinities and View/Purchase Affinities also use DataWarehouse data. 

**Choice of control data when viewing recommendation results** 

You can now choose the control data you want to use when viewing the results of a recommendation. See . [ Viewing Complete Recommendation Results ](c_rec_mng_recs/c_Viewing_a_Recommendation_in_the_Recommendations_Manager/c_Testing_Recommendation_Results/t_Viewing_Complete_Recommendation_Results.md#task_19A3022F3E2044CCA535F3CEC594300E) 

**Improved product search** 

You can now search on all variables, including custom variables. You can also specify multiple search criteria to further narrow your results. See [ Searching Catalogs ](c_rec_mng_recs/c_Creating_a_Custom_Algorithm/t_Searching_Catalogs.md#task_B5E7B5638BF0406E93AE18B2C6893AE2). 

**Increased length limit of algorithm names** 

The length permitted for algorithm names has been increased to 255 characters. See [ Naming a Custom Algorithm ](c_rec_mng_recs/c_Creating_a_Custom_Algorithm/r_Naming_a_Custom_Algorithm.md#reference_EFEF6E3495F746948AEF178875B87CCB) 

## May 2012 {#section_5AD3A0EFBB794A0DBDD0D3A5DA5C0DCA}

This release of Recommendations includes the following changes: 

** ` keyType` attribute added to Custom Algorithm Name API** 

` keyType`is an optional parameter that allows users to specify their own key for custom algorithms. See [ Naming a Custom Algorithm ](c_rec_mng_recs/c_Creating_a_Custom_Algorithm/r_Naming_a_Custom_Algorithm.md#reference_EFEF6E3495F746948AEF178875B87CCB) for more information. 

**Changed Change Log to History and added functionality** 

The Change Log has been renamed History. In addition to the previous functionality, the History also shows the number of recommendations uploaded per algorithm so you can see that the algorithm has run and is ready with content. See [ Viewing the History ](c_rec_mng_recs/c_Viewing_a_Recommendation_in_the_Recommendations_Manager/t_Viewing_the_Change_Log.md#task_0B5CF07FDC30484F89A58E402ADFE493). 

**Changed Dynamic Attribute Filtering functionality** 


* Changed **[!UICONTROL  Dynamically Matches the Key]** to **[!UICONTROL  Matches]** to improve usability and clarity. 

* Changed **[!UICONTROL  Dynamically in the Range of the Key]** to **[!UICONTROL  Is Between]** to improve usability and clarity. Also removed the upper limit for the specified range. 



See [ Setting Data Details ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_Setting_Data_Details.md#task_28DB20F968B1451481D8E51BAF947079) for more information. 

## October 2011 {#section_56119F75B2404FAD9601636D8600A22E}

This release of Recommendations includes the following new features: 

**Dynamic Attribute Filtering** 

Dynamic filtering enables you to set up one recommendation that automatically applies for each item across the site. You can limit recommendations to items that match or share an attribute of the key item. For example, recommendations could be limited to items of the same brand as the current item, or could be limited to items from different categories. Or, you could set a rule to recommend items whose price is within 10% of the currently viewed item's price. See [ Setting Data Details ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_Setting_Data_Details.md#task_28DB20F968B1451481D8E51BAF947079). 

**Improved Algorithms** 

The existing affinity algorithms, "People who viewed this viewed that", "People who viewed this bought that", and "People who bought this bought that", will be upgraded to use enhanced collaborative filtering strategies that take into account a broader consideration set of similar visitors' behavior to drive more successful and relevant recommendations. See [ Selecting an Algorithm ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_algo_select_recs.md#task_2203616ABBE342B6ADAB08F278D794FA). 

To more accurately reflect the robust nature of these new algorithms, the names have been updated as follows: 


* "People who viewed this viewed that" is now "View Affinities"
* "People who viewed this bought that" is now "View/Purchase Affinities"
* "People who bought this bought that" is now "Purchase Affinities"


Any current recommendations that employ the existing affinity algorithms will be automatically updated to their matching upgraded algorithm with no disruption to the recommendation delivery. 

**Statistical Confidence in Reports** 

For each reported metric, you can view the statistical confidence level for the lift vs control. See [ Confidence Level and Confidence Interval ](c_rec_mng_recs/c_Viewing_a_Recommendation_in_the_Recommendations_Manager/c_Testing_Recommendation_Results/c_Confidence_Level_and_Confidence_Interval.md#concept_0D0002A1EBDF420E9C50E2A46F36629B). 

** Location Testing ** 

This new recommendation type enables you to determine the best location for a recommendation on a page. The same algorithm is delivered to each mbox location at different times. When the recommendation is showing in one mbox, the other mbox shows default content. This new recommendation enables you to determine which location is the best place for the selected recommendation. See [ Adding a Location Test Recommendation ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/c_Creating_a_New_Recommendation/t_Adding_a_Location_Test_Recommendation.md#task_3CB225C3A7EA44D2BB5D02631AF74EB5). 

## July 2011 {#section_AC6326C9CE734F94BDD515A19ACB3960}

This release of Recommendations includes the following new features: 

**Simplified Recommendation Creation** 

When you add a recommendation, you now begin by choosing a recommendation type. This simplifies the creation of each kind of recommendation. See [ Adding a New Recommendation ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/c_Creating_a_New_Recommendation/c_Creating_a_New_Recommendation.md#concept_9F20B4F0F53D4399B10BCBBC979E0B4C). 

**Test&amp;amp;Target Custom Profile Attributes** 

Users of both Recommendations and Test&amp;Target can base a recommendation on any Test&amp;Target profile attribute. See [ Basing the Recommendation on a Recommendation Key ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_rec_key_recs.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B). 

**Change Logs** 

The change log records the date and time any changes and activations occur, and who made them. See [ Viewing the History ](c_rec_mng_recs/c_Viewing_a_Recommendation_in_the_Recommendations_Manager/t_Viewing_the_Change_Log.md#task_0B5CF07FDC30484F89A58E402ADFE493). 

**Trended Graph Report** 

The Trended Graph report shows trends for the recommendation over a specified amount of time. See [ Viewing the Trended Graph Report ](c_rec_mng_recs/c_Viewing_a_Recommendation_in_the_Recommendations_Manager/c_Testing_Recommendation_Results/t_Viewing_the_Trended_Graph_Report.md#task_1D399DB0E0A14BF5A672E99C6695BAE7). 

## May 2011 {#section_0BDD45B01CC7404ABC596C99C8EB9F23}

This release of Recommendations includes the following new features: 

**Affinity Algorithms** 

These new algorithms take the same raw data as the old algorithms, but apply collaborative filtering strategies to gather different and better results. The affinity algorithms must be enabled by Client Services. See [ Selecting an Algorithm ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_algo_select_recs.md#task_2203616ABBE342B6ADAB08F278D794FA). 

**More Logical Operators** 

New logical operators give the marketer increased control over the items displayed in a recommendation. See [ Setting Data Details ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_Setting_Data_Details.md#task_28DB20F968B1451481D8E51BAF947079). 

**Improved Backup Recommendations** 

Backup recommendations now randomly select more items from the most popular items on your site or in your catalog. See [ Using a Backup Recommendation ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/c_backup_recs.md#concept_5D02FA607144416BB3514364E11E9395). 

**New Report Metrics** 

New report metrics give you a direct understanding of the influence Recommendations had on a customer's decision to purchase by tracking whether the recommendation was clicked before something was purchased. Any purchase after the recommendation was clicked counts. See [ Viewing Complete Recommendation Results ](c_rec_mng_recs/c_Viewing_a_Recommendation_in_the_Recommendations_Manager/c_Testing_Recommendation_Results/t_Viewing_Complete_Recommendation_Results.md#task_19A3022F3E2044CCA535F3CEC594300E). 

**Entity Feeds** 

Because Recommendations users already configure XML or txt feeds to send to Google either via URL or FTP, entity feeds accept that product data and use it to build out the Recommendations catalog. Tell Recommendations where that feed exists and Recommendations retrieves the data. 

Entity feeds enable more ways to get product or content information into Recommendations. Item details can be sent to Recommendations from SAINT product classifications or using the Google Product Search feed format. This allows you to bypass complex mbox implementation or augment your mbox data with information that is either unavailable on the page or unsafe to send directly from the page (like margin, COGS, and so on). See [ Using Entity Feeds ](c_rec_mng_recs/c_Managing_Recommendations_Settings/t_Using_Entity_Feeds.md#task_4034B221DC754633B1280893AE6B5F86). 

## February 2011 {#section_4340D601247B4C6489DB0E626B080524}

This release of Recommendations includes the following new features: 

**Catalog Item Viewer** 

After you create a product catalog, you can view and search it within Recommendations.&nbsp;You can search the catalog and see all the data that Recommendations has learned about your items including ID, price, inventory, categories, and so on, so you can be confident knowing what information will display in your Recommendations. &nbsp;You can also delete an item you no longer want in your catalog directly from this item viewer. See [ Searching Catalogs ](c_rec_mng_recs/c_Creating_a_Custom_Algorithm/t_Searching_Catalogs.md#task_B5E7B5638BF0406E93AE18B2C6893AE2). 

## November 2010 {#section_E7623F1927954AF3B09A7E5FAA0671DF}


* Catalogs The catalog is the set of products or items that are eligible for the recommendation. The backup recommendations generated for each algorithm within the recommendation also uses this catalog, so only items in the catalog are included in the backup recommendation. With catalogs, you can be sure that only products that make sense to show in a location are displayed. See [ Creating Catalogs ](c_rec_mng_recs/c_Creating_a_Custom_Algorithm/t_Creating_Catalogs.md#task_CF595BC2426140E08F7948E43E3C8F81). 

* Optimizing Recommendations The Optimizing recommendation type ensures the most effective recommendations are shown more often by automatically displaying the best performing recommendations. Optimizing recommendations allow marketers to use an automated approach to improving site performance. With an Optimizing recommendation, fewer visitors see underperforming experiences. Automatically and over time, more traffic is shown the best performing recommendations. When you create an Optimizing recommendation, you specify the optimizing metric used to determine performance, which can be the conversion rate, average order value, or revenue per visit. You also choose whether to include default content in the calculations. See [ Choosing a Test Type ](c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/t_choosetype_recs.md#task_301A771BFE7F45A3AA1E77024E574D1C). 


>[!MORE_LIKE_THIS] {class="- topic/related-links "}
>
>* [ Prerequisites and Integrations ](r_prereqs_recs.md#reference_D6E669D2EA0742279A3840D252079E1A)
>* [ Starting Recommendations ](t_recs_start_recs.md#task_BCD9A79509224A0DBD89C1B50E97B4D5)
>* [ Recommendations Functions ](r_recommendations_Settings_recs.md#reference_903C30236F0240ACBA453402B119D565)
