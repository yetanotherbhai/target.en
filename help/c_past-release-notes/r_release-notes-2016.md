---
description: null
seo-description: null
seo-title: 2016 Releases
title: 2016 Releases
uuid: 97623128-9684-4420-ab8b-e6b1574437f9
index: y
internal: n
snippet: y
translate: y
---

# 2016 Releases


## Target Standard/Premium 16.10.2 (November 8, 2016) {#section_2FDEFB3D56CC4BD7BC04DBEECFF6E942}

**Fixes** 

This release includes the following fixes: 


* Fixed an issue in [!DNL  Recommendations] where feeds could not be created for any non-default environments (host groups). 

* Made several improvements to reduce activity syncing errors. 

* You can no longer create redirect offers for activities using [!DNL  Analytics for Target] (A4T). 



## Target Standard/Premium 16.10.1 (October 25, 2016) {#section_F76F7329FCAC452FB88F8BE0BA727044}

This release includes the following features and enhancements: 



<table id="table_F8C01B2A9F07443490DB3025AC3AAC2A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Auto-Allocate: Winner Badge </td> 
   <td colname="col2"> <p>We've now made it easier to determine a winner in an Auto-Allocate A/B activity. </p> <p>Many marketers make the mistake of prematurely declaring a winning experience before the results indicate the clear winner. </p> <p>When using the <span class="wintitle"> Automated Traffic Allocation </span> feature, <span class="keyword"> Target </span> displays a badge at the top of the activity's page indicating "No Winner Yet" until the activity reaches the minimum number of conversions with sufficient confidence. When a clear winner is declared, <span class="keyword"> Target </span> displays "Winner: Experience X." </p> <p>For more information, see <a href="automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a> and <a href="c_determine-winner.md#concept_5741A89ED7224E1285A3BC34B2CCD0F9" format="dita" scope="local"> Determine a Winner </a>. </p> <p> <p>Note:  Auto-Allocate A/B activities are no longer supported in Analytics for Target (A4T) going forward. With this release, any active Auto-Allocate A/B activities with A4T enabled will be switched to <span class="wintitle"> Manual </span> mode (equal traffic allocation). </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target mobile devices by carrier </td> 
   <td colname="col2"> <p>Create an audience to target mobile devices based on mobile carrier (Verizon, Sprint, AT&amp;T, T-Mobile, etc.). The <span class="wintitle"> Mobile Carrier </span> option is under the <span class="wintitle"> Geo </span> settings. </p> <p>For more information, see <a href="c_geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Generate mboxTrace authentication token from Target UI </td> 
   <td colname="col2"> <p>Enable advanced <span class="keyword"> Target </span> debugging tools by creating a temporary authentication token. </p> <p>Click <span class="uicontrol"> Generate Authentication Token </span> on the <span class="wintitle"> Implementation Details </span> page ( <span class="uicontrol"> Setup </span> &gt; <span class="uicontrol"> Implementation </span>). You can then add the resulting parameter to your web page URLs for troubleshooting purposes. </p> <p>For more information, see "Retrieve the Authorization Token to Use With Debugging Tools" in <a href="c_content_trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Troubleshooting Content Delivery </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Criteria set sequencing </td> 
   <td colname="col2"> <p>Use sets of up to five pre-created criteria in a single experience for greater control over the recommendations presented to visitors. </p> <p>For more information, see <a href="../recs/t_create_criteria_sequence.md#task_8A9CB465F28D44899F69F38AD27352FE" format="dita" scope="local"> Creating Criteria Sequences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Insert external promotions </td> 
   <td colname="col2"> <p>Add promoted items and control their placement in your Recommendations designs. </p> <p>For more information, see <a href="../recs/t_adding_promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> Adding Promotions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="firstlook"> <p><b>First Look</b> </p> Auto-targeting in A/B activities </td> 
   <td colname="col2"> <p> <p>Note:  This "First Look" offering is enabled for a few customers in this release for testing and feedback. </p> </p> <p>Automatically target experiences in A/B tests to serve the right experience to the right visitor. </p> <p>For more information, see <a href="c_auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Platform Changes (October 10, 2016) {#section_0761AED70C3E44EA9D8546107B162CC1}



<table id="table_E3E52A4362724D05A8472DB5F51A2429"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> version 0.9.3 </p> </td> 
   <td colname="col2"> <p>October 10, 2016 </p> <p> <span class="codeph"> at.js </span> version 0.9.3 is available. </p> <p> 
     <ul id="ul_E4D300700390433E9EF8D5C9D3AA7669"> 
      <li id="li_E916EB3A77ED4CFF90CF6B4D30F188B1"> <p>Ensures mbox calls fire in Microsoft Internet Explorer 11 when legacy browsers are disabled in the <span class="codeph"> at.js </span> settings. </p> </li> 
      <li id="li_1130509832CE429DB6DE636404CC54E1"> <p>Ensures that default content is rendered if a dynamic remote offer fails (for example, if the URL is incorrect and returns a 404 error). </p> </li> 
      <li id="li_21B5225D894B43CB863A775C937F66F4"> <p>Ensures that elements are revealed quickly when VEC click-tracking selectors can't be found in the DOM. </p> </li> 
     </ul> </p> <p>For more information, see <a href="../ov2/r_target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 16.9.1 (September 22, 2016) {#section_3CD20678B6254DE1A9BD41FDD2255DDD}

This release includes the following features and enhancements: 



<table id="table_FED049F97C054CA895E0AEA3F2B180BF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Combine audiences </td> 
   <td colname="col2"> <p>Combine multiple audiences (including <span class="keyword"> Adobe Experience Cloud </span> audiences and <span class="keyword"> Target </span> audiences) on the fly during the activity-creation workflow. </p> <p>For example, you can target all loyalty customers by including a specific <span class="keyword"> Audience Manager </span> segment for loyalty status and combine it with a <span class="keyword"> Target </span> segment made up of people who signed up for your loyalty program during the current session, instead of creating a third, permanent audience. </p> <p>For more information, see <a href="c_combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Combining Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target visitors during a specific time period </td> 
   <td colname="col2"> <p>Add start and end dates to target an audience. </p> <p>For example, using the new combined, ad-hoc audiences mentioned above, you can target low-spenders with specific content during the three days leading up to Black Friday and other content after Black Friday. </p> <p>For more information, see <a href="c_time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Save smart collections </td> 
   <td colname="col2"> <p>Search functionality on the <span class="wintitle"> Content </span> page now includes saved folders, called smart collections, to save time when performing similar searches. </p> <p>For more information, see <a href="c_filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> Search Content and Create Smart Collections </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Add a link to an image. The link can be a click-through link, destination link, or a landing link. </p> <p>For more information, see <a href="t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements** 

This release includes the following enhancements: 



|  Enhancement  | Description  |
|---|---|
|  Visual Experience Composer (VEC)  | Improved error messaging.  |

**Known Issues** 


* The [!UICONTROL  Render Using JavaScript] option is currently not supported if it is used along with custom code in the Visual Experience Composer.


## Target Platform Changes (September 2016) {#section_1955146045A247D393DB824669A2A916}



<table id="table_8FDAEED5D84C4C718AB863BD6C383F20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> version 0.9.2 </p> </td> 
   <td colname="col2"> <p>September 21, 2016 </p> <p> <span class="codeph"> at.js </span> version 0.9.2 is available. </p> <p> 
     <ul id="ul_0778A9049C9D48A7B6CB4B79A95F0F4C"> 
      <li id="li_689FF306179F4EC3B391DEE3C53F4B1D"> <p>Added an <span class="codeph"> optoutEnabled </span> setting to enable or disable the Device Graph opt-out. If this setting is set to <span class="codeph"> true </span> and the visitor has opted out of tracking, the visitor's browser will not make any mbox calls. Device Graph is currently in Beta. This setting is set to <span class="codeph"> false </span> by default, but must be set to <span class="codeph"> true </span> if you are using Device Graph. A similar option is part of <span class="codeph"> mbox.js </span> v61. </p> </li> 
      <li id="li_663462C0680049F89CA8FE1853F31807"> <p>Added <span class="codeph"> CustomEvent </span> support for the notification mechanism. Previously, the <span class="codeph"> at.js </span> event notification mechanism could not be used via standard DOM APIs, such as <span class="codeph"> document.addEventListener() </span>. Now you can use <span class="codeph"> document.addEventListener() </span> to subscribe to <span class="codeph"> at.js </span> events, such as request events and content rendering events. </p> </li> 
      <li id="li_3FB2914F8D2F4AFFAA9B4622E8CA1EFF"> <p>Fixed an issue related to offers created in the Visual Experience Composer (VEC). Prior to this release, Target hid the selectors and un-hid them only when all selectors matched. In <span class="codeph"> at.js </span> 0.9.2 Target un-hides the selectors as soon as they are matched. </p> </li> 
     </ul> </p> <p>For more information, see <a href="../ov2/r_target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 16.9.1 (September 22, 2016) {#section_60ADF842E4A0424E8D2A81FB8B813A7A}

This release includes the following features and enhancements: 



<table id="table_896218AECE4C4EC691B76E79CC7DC356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Combine audiences </td> 
   <td colname="col2"> <p>Combine multiple audiences (including <span class="keyword"> Adobe Experience Cloud </span> audiences and <span class="keyword"> Target </span> audiences) on the fly during the activity-creation workflow. </p> <p>For example, you can target all loyalty customers by including a specific <span class="keyword"> Audience Manager </span> segment for loyalty status and combine it with a <span class="keyword"> Target </span> segment made up of people who signed up for your loyalty program during the current session, instead of creating a third, permanent audience. </p> <p>For more information, see <a href="c_combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Combining Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target visitors during a specific time period </td> 
   <td colname="col2"> <p>Add start and end dates to target an audience. </p> <p>For example, using the new combined, ad-hoc audiences mentioned above, you can target low-spenders with specific content during the three days leading up to Black Friday and other content after Black Friday. </p> <p>For more information, see <a href="c_time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Save smart collections </td> 
   <td colname="col2"> <p>Search functionality on the <span class="wintitle"> Content </span> page now includes saved folders, called smart collections, to save time when performing similar searches. </p> <p>For more information, see <a href="c_filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> Search Content and Create Smart Collections </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Add a link to an image. The link can be a click-through link, destination link, or a landing link. </p> <p>For more information, see <a href="t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements** 

This release includes the following enhancements: 



|  Enhancement  | Description  |
|---|---|
|  Visual Experience Composer (VEC)  | Improved error messaging.  |

**Known Issues** 


* The [!UICONTROL  Render Using JavaScript] option is currently not supported if it is used along with custom code in the Visual Experience Composer.


## Target Platform Changes (August 2016) {#section_8D8BA8C628E747338C84564EC34CE0FD}



<table id="table_0035B0D7ECD444C68B1B6CB0F150C55E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js </span> version 61 </p> </td> 
   <td colname="col2"> <p>August 23, 2016 </p> <p> <span class="filepath"> mbox.js </span> version 61 includes the following changes in the August release: </p> <p> 
     <ul id="ul_DC4E5AB3B48A4D2D9B08B6CDA5DFE8FB"> 
      <li id="li_B52F3AE60D324C2A8FAD03C1495F26D7"> <p> <span class="filepath"> mbox.js </span> version 61 is now the default download in the <span class="keyword"> Target Standard/Premium </span> and <span class="keyword"> Target Classic </span> user interfaces. </p> </li> 
      <li id="li_41C2D2E552BF4F8E8A4375AF368F7728"> <p>Added an <span class="codeph"> optoutEnabled </span> setting to support future Adobe Experience Cloud opt-out functionality. The default value is false. If this property is enabled, all requests execute asynchronously against the <span class="filepath"> /ajax </span> endpoint, just like version 60. </p> </li> 
     </ul> </p> <p>For more information about all the changes in <span class="filepath"> mbox.js </span> version 61, see <a href="../ov/r_mboxjs_change_log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> mbox.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Target Standard/Premium 16.8.1 (August 23, 2016) {#section_A8854D4EDF014AEBB81F49EB104D4A20}

The Adobe Target Standard/Premium 16.8.1 (August 23, 2016) release includes the following features and enhancements: 



<table id="table_AE048CB9EA1C4C7BBC2E9D90D26F7395"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Hosts and environment (host group) management </p> </td> 
   <td colname="col2"> <p>Organize your sites and pre-production environments for easy management and separated reporting. </p> <p>Hosts are bundled into environments for ease of management. The preset environments include Production, Staging, and Development. You can also add new environments. </p> <p>This feature achieves feature parity with <span class="keyword"> Target Classic </span>. </p> <p>For more information, see <a href="../ov2/c_hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> Hosts </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Category Affinity </p> </td> 
   <td colname="col2"> <p>The category affinity feature automatically captures the categories a user visits and calculates the user's affinity for the category so it can be targeted and segmented on. This helps to ensure that content is targeted to visitors who are most likely to act on that information. </p> <p>This feature achieves feature parity with <span class="keyword"> Target Classic </span>. </p> <p>For more information, see <a href="c_category_affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local"> Category Affinity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enable/Disable Enhanced Experience Composer at the activity level </p> </td> 
   <td colname="col2"> <p>Enable/disable the <span class="wintitle"> Enhanced Experience Composer </span> at the account level (applies to all activities created in the account) or at the individual activity level. </p> <p>Previously, you could enable/disable the Enhanced Experience Composer only at the account level. </p> <p>For more information, see <a href="c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Offer performance report </p> </td> 
   <td colname="col2"> <p>Download an offer performance report with all Automated Personalization activity success metrics. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements** 

This release includes the following enhancements: 



<table id="table_E2E4BE72BD79413A821C6A6D1A3AB0F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Code Editor UI redesign </p> </td> 
   <td colname="col2"> <p>The code editor UI has been updated to be more intuitive and easier to use. </p> <p>For more information, see <a href="../target/c_vec_code_editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

The following known issues have been reported: 


* Some of the UI text for the [!UICONTROL  Category Affinity] feature displays in English only. Text in other languages will be available in the September [!DNL  Target] release.


## Target Platform Changes (July 2016) {#section_09C18773707B4059852A41C764F817E4}



<table id="table_33B60910EAE24BAFA778F280F72FB683"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> version 0.9.1 </p> </td> 
   <td colname="col2"> <p>July 14, 2016 </p> <p> <span class="filepath"> at.js </span> version 0.9.1 is now available. </p> <p>For more information, see <a href="../ov2/r_target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js </span> version 61 </p> </td> 
   <td colname="col2"> <p>July 28, 2016 </p> <p> <span class="codeph"> mbox.js </span> version 61 is now available for download. Version 61 is not currently the default download. </p> <p>For more information, see <a href="../ov/r_mboxjs_change_log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> mbox.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Target Standard/Premium 16.7.1 (July 21, 2016) {#section_DB583EF9A30247A488EE319583911F22}

The Adobe Target Standard/Premium 16.7.1 (July 21, 2016) release includes the following features and enhancements: 



<table id="table_EBA34BD2F5C745DD9EC5231AD79F6C00"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Priority settings for activities </td> 
   <td colname="col2"> <p>You can now set activity priority levels from 0-999 to allow for finer control over which activity displays if multiple activities are assigned to the same location with the same audience. </p> <p>This option must be enabled in <span class="wintitle"> Setup </span> &gt; <span class="wintitle"> Preferences </span> . </p> <p>The Fine-grained priorities option applies to A/B Test, Automated Personalization, Experience Targeting, and Multivariate Test activities. </p> <p>For more information, see the following topics: </p> <p> 
     <ul id="ul_FD92CD06CF25480887AC171274262E18"> 
      <li id="li_D321FAED82944D2685DA69EB310D80BE"><b>A/B Test: </b> <a href="../target/r_ab_goals_and_settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_12ECDFD71DB94E22A85AB13B487E8503"><b>Automated Personalization: </b> <a href="../target/t_automated_personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a> </li> 
      <li id="li_84B893C214994246AB36E28E84C51460"><b>Experience Targeting: </b> <a href="../target/r_xt_goals_and_settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_26533B659C0E49D6A6D3B3FEBE9CA930"><b>Multivariate Test: </b> <a href="../mvt/r_goals_and_settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_FBACF2B73B2E491BBB85618153AC4568"><b>Activities: </b> <a href="t_activity_settings.md#task_C6B2FF8374724933BE79A83549B9CD02" format="dita" scope="local"> Activity Settings </a> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Multi-valued Recommendations attributes </td> 
   <td colname="col2"> <p>All custom <span class="keyword"> Recommendations </span> attributes can now contain multiple entity values. </p> <p>For more information, see <a href="../recs/c_custom_entity_attributes.md#concept_E5CF39BCAC8140309A73828706288322" format="dita" scope="local"> Custom Entity Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dynamic/remote offer support </td> 
   <td colname="col2"> <p>Dynamic content can be part of any form-based activity in <span class="keyword"> Target Standard/Premium </span>. Dynamic content is stored outside of <span class="keyword"> Target </span>. </p> <p>For more information, see <a href="../target/c_about-remote-offers.md#concept_657016A0E6174C22B89036E9C8A0170F" format="dita" scope="local"> Create Remote Offers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Copy audiences and profile scripts </td> 
   <td colname="col2"> <p>You can now copy an existing audience that you can then edit to create a similar audience. </p> <p>For more information, see <a href="../target/t_create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creating an Audience </a>. </p> <p>You can also copy existing profile scripts. </p> <p>For more information, see <a href="c_profile_parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profile Script Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Use classes to determine element selectors </td> 
   <td colname="col2"> <p>Element selectors can now be based on classes or IDs in Automated Personalization and Multivariate Test activities. In previous versions, this option was only available for A/B Test activities. </p> <p>For more information, see <a href="../target/c_vec_selectors.md#concept_4EB7663E255F439B8D24079D23479337" format="dita" scope="local"> Element Selectors Used in the Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Content similarity </td> 
   <td colname="col2"> <p> Use Content Similarity rules to make recommendations based on item or media attributes. </p> </td> 
  </tr> 
 </tbody> 
</table>



<table id="table_699755B33F8F48ECABB6FC7E78289A79"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Reporting improvements </p> </td> 
   <td colname="col2"> <p>Success metric report downloads now show metric and segment names instead of IDs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Evaluate mbox entry condition on each request in Automated Personalization activities </td> 
   <td colname="col2"> <p>In Automated Personalization activities, entry criteria (URL targeting, template rules, audience target) are evaluated for each request for more accurate offer delivery. </p> <p>For more information, see <a href="t_automated_personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Target Standard/Premium 16.6.1 (June 16, 2016) {#section_C1E9F43111BF4160AF31482CD53E00BD}

There is no customer-facing release planned for June. 

**Fixes** 

This release includes the following fixes: 


* Fixed an issue where some customers saw a white screen when trying to edit their page inside the Visual Experience Composer.


**Known Issues** 

The following known issues have been reported: 


* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages.
* Issue with experience preview URLs for experiences with a redirect. As a workaround, in the Experience Composer, click ** [!UICONTROL  Configure] **, choose ** [!UICONTROL  Multiple Audiences] **, and add ** [!UICONTROL  All visitors] ** as the only audience. Continue to save your activity. This does not change the delivery of your activity, but allows preview to work. This will be fixed in the July release of Adobe Target.
* The documentation shows the expected behavior for the Redirect URL checkbox. However, due to a bug, the check box does not show as selected by default. This defect will be fixed soon. To check this option in an existing activity with a redirect offer, use the following workaround: 


    1. Open the Redirect to URL popup.
    1. Change the URL to a dummy URL and save.
    1. Change the dummy URL again to your campaign's expected redirect URL.
    1. Check the "Include Current Query Parameters" option, and save.


  If you check the option while creating a new redirect offer, you can expect your query parameters to be included in the redirection. 

  For older activities, if this option is checked in the experience composer of your activity, it means your redirection will include the query parameters. If it is not checked, current query parameters will not be included in redirection. 



## Adobe Target Standard/Premium 16.5.1 (May 19, 2016) {#section_406CE09317994F55A26C2FDB77C77FEA}

The Adobe Target Standard/Premium 16.5.1 (May 19, 2016) release includes the following features and enhancements: 



<table id="table_DDC5356FD6B8443EAA6EB81C03ADF73A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1">Export/Download Summary reports for Automated Personalization and Recommendations Premium </entry> <entry colname="col2"> <p>The ability to download data in a .csv format for quick import into Excel or other data analysis programs has been added to Automated Personalization and Recommendations Premium. </p> <p>This feature was previously only available for A/B, Experience Targeting, and Multivariate activities. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> Experience Versions </td> 
   <td colname="col2"> <p>Versions targeted to different audiences can now be set up within experiences in A/B activities. </p> <p>See <a href="t_target-experience-to-multiple-audiences.md#task_0138112E283A4A5B9F8AB9AAF2FBC2FF" format="dita" scope="local"> Target an Experience to Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QA/Preview URLs </td> 
   <td colname="col2"> <p>Preview URLs are now available for the form-based experience composer. </p> <p>See <a href="t_experience_preview.md#task_586C6655A6FD4AF08F5678FC3F481EFC" format="dita" scope="local"> View Experience URLs </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1" outputclass="premium">Personalized Recommendations </entry> <entry colname="col2"> <p>Visitor profile attributes can be added to collaborative filtering to return recommendations that are more highly personalized to each visitor. </p> <p>See <xref href="../recs/t_create_new_algorithm.xml#task_8A9CB465F28D44899F69F38AD27352FE" format="dita" scope="local">Creating Criteria</xref>. </p> </entry> </row> --> 
  <!-- <row> <entry colname="col1" outputclass="premium">Content similarity weighting </entry> <entry colname="col2"> <p> Select specific attributes to consider/prioritize in calculating content similarity </p> <p>See <xref href="../recs/c_content_similarity.xml#concept_5402DAFA279C4E46A9A449526889A0CB" format="dita" scope="local">Content Similarity</xref>. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations custom algorithms </td> 
   <td colname="col2"> <p>Custom algorithm mappings can be uploaded in a CSV file. It is no longer required to use the XML-based API. </p> <p>See <a href="../recs/t_recommendations_csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> Uploading Custom Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Analytics for Target: Analytics tracking server </td> 
   <td colname="col2"> <p>To ensure proper reporting tracking, you must specify a tracking server when you create or edit activities that use Analytics for Target (A4T). Existing activities will continue to run using current settings. </p> <p>See <a href="../a4t/t_analytics_tracking_server.md#task_72077BA7E93C4A65A715A18F32228823" format="dita" scope="local"> Using an Analytics Tracking Server </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New Instructional Videos </td> 
   <td colname="col2"> <p>The following instructional videos have been added to help: </p> <p> 
     <ul id="ul_47BAE946E764404497B7D81EE4C5D076"> 
      <li id="li_E16E50F94D3748E2985FB78F75140626">Using DTM to pass parameters to the global mbox </li> 
      <li id="li_A8CCDE3EFF25430580E6C372000CF964">Using DTM to deploy Target </li> 
      <li id="li_8897F7B5930B448D87274CEDFCC75AE4">Setting up a multivariate test </li> 
      <li id="li_2573DF52CE974ED0AF9EA433C97BC4C0">Creating an A/B activity </li> 
      <li id="li_52F28040D54D43E787B763E6AA998614">Understanding activity types </li> 
      <li id="li_577C8DDEB4CE429CA3C14BE5655F6E11">Configuring activity settings </li> 
      <li id="li_2F7FCA657FD04E02ADD6E6964A8EA1F0">Targeting an activity </li> 
      <li id="li_A08B8AFF48764D1B9EA706977F72AA66">Creating audiences </li> 
      <li id="li_493CDC3BEA5F4EA0821B971579177E03">Using audiences </li> 
      <li id="li_19045C86E1524649B56F82416934EF13">Using the Content Library </li> 
      <li id="li_8E89F3691A6F4400A2DFDFE5186DFA83">Using profile scripts </li> 
      <li id="li_2EBB2B61BFA24F5FB858C0551AB20F70">Setting account preferences </li> 
      <li id="li_E1886818C7BF4F36B07EC293F1A45911">Understanding Visual Experience Composer modes </li> 
      <li id="li_F74D2BA5ACD04595B658955A489602E5">Configuring and implementing mbox.js </li> 
      <li id="li_A87B876298344B2987BDC5FFD5580EC0">Creating and managing Target users </li> 
      <li id="li_F90E1083444E4DBAA8C406AC293C0FD6">Setting success metrics </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> User Interface improvements </td> 
   <td colname="col2"> <p>User interface improvements have been made to the Visual Experience Composer and Recommendations search. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations CSV download </td> 
   <td colname="col2"> <p>CSV downloads now have a line for all environments, including those that do not have entity recommendations (for example: 
     <systemoutput>
       # environment: 1724 
     </systemoutput>). </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
 </tbody> 
</table>

**Enhancements** 

Improvement made to improve the A4T provisioning process. 

**Known Issues** 

The following known issues have been reported: 


* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages.
* Issue with experience preview URLs for experiences with a redirect. As a workaround, in the Experience Composer, click ** [!UICONTROL  Configure] **, choose ** [!UICONTROL  Multiple Audiences] **, and add ** [!UICONTROL  All visitors] ** as the only audience. Continue to save your activity. This does not change the delivery of your activity, but allows preview to work. This will be fixed in the July release of Adobe Target.


## New Target Implementation Library, at.js 0.8.0 (May 5, 2016) {#section_6A44C277E82D409AB6DCD0901F43794A}

at.js is a new implementation library for Target designed for both typical Web implementations and single-page applications. 

at.js replaces mbox.js for Adobe Target implementations. 


>[!NOTE]
>
>Although at.js replaces mbox.js, mbox.js will continue to be supported. For most people, at.js provides advantages over mbox.js. This gives you time to test at.js and to change the implementation on your pages.



Among other benefits, at.js improves page load times for Web implementations, improves security, and provides better implementation options for single-page applications. 

at.js contains the components that were included in target.js, so there is no longer a call to target.js. 

When implementing at.js, be aware of the following: 


* Visual Experience Composer redirects do not work.
* Internet Explorer versions earlier than 8 are not supported.
* Asynchronous implementation means legacy integrations like the Test&amp;amp;Target to SiteCatalyst plugin may not work.
* Target plugins that reference mbox.js objects and methods are not supported.
* All calls to Target are made via XMLHTTPRequest and content is returned via JSON.


## Target Platform Changes {#section_8295A808A4CE405C9DA2893E7935238E}


* [ Mbox.js version 60 ](r_mboxjs_change_log.md#section_3BDAB885FA13444A8D35940A4BFF5825) is now the default download.
* Mbox.js versions earlier than 50 are no longer actively tested. If your implementation is not yet updated, ensure additional QA is performed on all Target content delivery and reporting collection.
* Flash campaigns and other Flash-related items have been removed from Target.
* Internet Explorer 10 is no longer supported in the Target interface.
* Support for content delivery in Internet Explorer 8, 9, and 10 is expected to end in an upcoming release. Active testing will be discontinued in a future release for these browsers, following the end of active support for these browsers by Microsoft. Target will continue to deliver content to these browsers, but you should test content delivery and data collection for reports. 



## Adobe Target Standard/Premium 16.4.1 Fix (May 5, 2016) {#section_70552F61E83140C7B4D2A245198B630E}


* at.js v 0.8.0 is now available for download from the Target interface.
* Target APIs changed. ` applyOffer` now requires ` mbox param [0]`. 
  ```
  adobe.target.applyOffer({ 
      "mbox": "target-global-mbox", 
   "params": {"test": "true"}, 
      "selector": ".banner-text", 
      "offer": offer 
  });
  ```




## Adobe Target Standard/Premium 16.4.1 (April 21, 2016) {#section_C968860FAB81485BA12BD588F4ECA401}

This release includes the following features and enhancements: 



<table id="table_162CC5A0DB324B38A8A4252A18976686"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1">Export/Download Summary reports for Automated Personalization and Recommendations Premium </entry> <entry colname="col2"> <p>The ability to download data in a .csv format for quick import into Excel or other data analysis programs has been added to Automated Personalization and Recommendations Premium. </p> <p>This feature was previously only available for A/B, Experience Targeting, and Multivariate activities. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> at.js </td> 
   <td colname="col2"> See <a href="r_release-notes-2016.md#reference_607661929B504CCFAB3791B13C0DCDBE/section_6A44C277E82D409AB6DCD0901F43794A" format="dita" scope="local"> New Target Implementation Library, at.js 0.8.0 (May 5, 2016) </a>, above. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Experience Cloud Notifications </td> 
   <td colname="col2"> <p>Notifications from Target are visible in all Adobe Experience Cloud solutions. Notifications are automatically sent when an activity is activated or deactivated. These notifications are available to all users with access to Target Standard/Premium. </p> <p>Notifications are also visible in Target Standard/Premium. </p> <p>See <a href="c_notifications.md#concept_557351F8BB7D40F39A65951A77B79D62" format="dita" scope="local"> Notifications </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> User Interface Improvements </td> 
   <td colname="col2"> <p>The user interface has been changed significantly in this release. Among the most noticeable changes are: </p> <p> 
     <ul id="ul_28F382C60ADE43F5A3A4BD0CD5A5CE52"> 
      <li id="li_C47240826E5844D6843314F453F042FC">Navigation has moved from the left to the top </li> 
      <li id="li_3BB03504E98C40CC85583DCD9A4CEA06">Improved dialog boxes </li> 
      <li id="li_AE71506DF1E748A788C40E1F09951732">Improved activity creation flow </li> 
     </ul> </p> <p>The way Experience Cloud solutions, including Target, are selected has also changed. To access Experience Cloud solutions and services, click the menu icon: </p> <p style="text-align: center;"> <img href="../assets/menu-shell-400.png" id="image_6E9323E0EBEA41B1A7319D6BCC43E769" width="400" height="140" /> </p> <p>For more information about accessing Target and making Target your default page after logging in to the Experience Cloud, see <a href="t_target-access-from-mac.md#task_5467C72DAFCB4BB583762CAAFC00A5CF" format="dita" scope="local"> Access Target from the Adobe Experience Cloud </a>. </p> <p>For more information about the user interface improvements, see <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/marketing-cloud-interface.html" format="https" scope="external"> What's New in the Adobe Experience Cloud - Spring 2016 </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Content similarity weighting (First Look) </entry> <entry colname="col2"> <p> Select specific attributes to consider/prioritize in calculating content similarity </p> <p><xref href="https://jira.corp.adobe.com/browse/TGT-15269">https://jira.corp.adobe.com/browse/TGT-15269</xref></p> <p><xref href="https://jira.corp.adobe.com/browse/TGT-15649">https://jira.corp.adobe.com/browse/TGT-15649</xref></p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> Inclusion rules can be disabled for backup recommendations </td> 
   <td colname="col2"> <p>When backup recommendations are enabled, you can choose not to apply inclusion rules to your backup recommendations. . </p> <p>For more information, see <a href="../recs/t_create_new_algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96" format="dita" scope="local"> Content Settings </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: New debugging capabilities in text area via <span class="codeph"> mboxTrace </span> </td> 
   <td colname="col2"> <p>Adding <span class="codeph"> &amp;amp;mboxTrace </span> to a URL replaces recommendations on that page with debugging details, including information about served recommendations, criteria, design, exclusions, inclusions, backup recommendations served, and more. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations API: Upload a CSV for the Custom Criteria </td> 
   <td colname="col2"> <p>You can upload a CSV for the Custom Criteria via API. </p> <p>This ability will be added to the Target Premium user interface in an upcoming release. </p> <p> <a href="https://www.adobe.io/products/target/docs/reference/recommendations" format="https" scope="external"> API documentation </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations API: New Design APIs </td> 
   <td colname="col2"> <p>New Design APIs make it possible to manage your Recommendations designs via API. </p> <p> <a href="https://www.adobe.io/products/target/docs/reference/recommendations" format="https" scope="external"> API documentation </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Dependent Success Metrics </td> 
   <td colname="col2"> Automated Personalization now supports the ability to limit a success metric to only count if a previous success metric has already been met. <p>For more information, see <a href="r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Reports Summary View Download </td> 
   <td colname="col2"> The download option now allows users to download summary view (i.e. comparing Control and Automated traffic) as broken down by all available success metrics. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Customer attributes can be used as tokens in offers </td> 
   <td colname="col2"> <p>Previously, customer attributes could be referenced in profile scripts, formatted as <span class="codeph"> crs.get('&lt; <span class="varname"> Datasource Name </span>&gt;.&lt; <span class="varname"> Attribute name </span>&gt;') </span>. </p> <p>Now, the attributes are available as tokens in profile scripts and directly in offers without first requiring a profile script. The token should be in the form: <span class="codeph"> $crs. <span class="varname"> datasourceName </span>. <span class="varname"> attributeName </span> </span>. </p> <p>See <a href="r_variables_profiles_parameters_methods.md#reference_F5D9EF735F1044C38E208F3A178903B2/section_62B4821EB6564FF4A14159A837AD4EDB" format="dita" scope="local"> CRS Tokens </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Custom Code enhancement </td> 
   <td colname="col2"> Custom code can now execute the JavaScript code in the <span class="codeph"> &amp;lt;head&amp;gt; </span> tag. Execution of code no longer waits for the <span class="codeph"> &amp;lt;body&amp;gt; </span> tag to be present in DOM. Earlier, the selector was only the first element in the <span class="codeph"> &amp;lt;body&amp;gt; </span> tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New Instructional Videos </td> 
   <td colname="col2"> Instructional videos have been added to help. Currently, you can view videos about the <a href="c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Visual Experience Composer and Form-Based Experience Composer </a>. More videos will be added in the coming weeks. </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* The issue introduced by Chrome version 48 that caused the Visual Experience Composer to function incorrectly in Chrome has been fixed. To benefit from this fix, update to Chrome version 50.


**Known Issues** 

The following known issues have been reported: 


* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages.


## Adobe Target Standard/Premium 16.3.1 (March 15, 2016) {#section_A5A9B03A5CCD4213AD656BE722B5FF67}

This release includes the following features and enhancements: 



<table id="table_F2A89DF1EAB443B4B4C7E0BC6118384B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1">Export/Download Summary reports for Automated Personalization and Recommendations Premium </entry> <entry colname="col2"> <p>The ability to download data in a .csv format for quick import into Excel or other data analysis programs has been added to Automated Personalization and Recommendations Premium. </p> <p>This feature was previously only available for A/B, Experience Targeting, and Multivariate activities. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>First Look: </p> <p>New Target implementation library, at.js </p> </td> 
   <td colname="col2"> <p> <p>Note:  This "First Look" offering is available via API download. It will be available via the Target interface in an upcoming release. In the meantime, you can download the at.js library, test it in your environment, and deploy it in your production Target implementation. </p> </p> <p> at.js is a new implementation library for Target designed for both typical Web implementations and single-page applications. </p> <p> at.js replaces mbox.js for Adobe Target implementations. </p> <p> <p>Note:  Although at.js replaces mbox.js, mbox.js will continue to be supported, although, for most people, at.js provides advantages over mbox.js. This gives you time to test at.js and to change the implementation on your pages. </p> </p> <p>Among other benefits, at.js improves page load times for Web implementations, improves security, and provides better implementation options for single-page applications. </p> <p>at.js contains the components that were included in target.js, so there is no longer a call to target.js. </p> <p>When implementing at.js, be aware of the following: </p> <p> 
     <ul id="ul_8C50C669AA7B4464A5FDECFCFD8662ED"> 
      <li id="li_6065B208480D46178055B40A2654E0C6">Visual Experience Composer redirects do not work. </li> 
      <li id="li_A2FABD3C21994511A45DED84283E526E">Internet Explorer versions earlier than 8 are not supported. </li> 
      <li id="li_04499B391F784B89B09A1D6329B1C790">Asynchronous implementation means legacy integrations like the Test&amp;amp;Target to SiteCatalyst plugin may not work. </li> 
      <li id="li_D3C00EF206154038A54F53CA40B34DC3"> Target plugins that reference mbox.js objects and methods are not supported. </li> 
     </ul> </p> <p>See <a href="../ov2/c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17" format="dita" scope="local"> at.js Implementation </a> for documentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dependent Success Metrics </td> 
   <td colname="col2"> <p>This features provides the option per success metric to count someone as reaching the success metric only if they've previously reached a different success metric. </p> <p> For example, a test might change the hero image on the homepage. The marketer might only want to count conversions for people who clicked the hero image. So, the marketer can set a success metric for "clicked on homepage hero" and then another metric for purchasing. Then, the marketer can add a rule on the "purchasing" metric to ensure visitors have first reached the "clicked on homepage hero" success metric. </p> <p> <p>Note:  If audience targeting on a location in a success metric is set, this feature is not supported for that metric. </p> </p> <p> Dependent Success Metrics are only supported in AB, XT, and MVT activities. Automated Personalization and Recommendations support will be available later. </p> <p>For more information, see <a href="r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Auto-Allocate usability improvements </td> 
   <td colname="col2"> <p>After the model for an Auto-Allocate activity is ready, the following operations from the UI are not allowed: </p> <p> 
     <ul id="ul_52B790B2B0D746769A3471E09CE1A122"> 
      <li id="li_B9F0FFF019CE4CB697F5D0B60061DC27">Switching the "Traffic Allocation" mode to "Manual" </li> 
      <li id="li_C271B0BE4C5C4B06BB21703239E7B061">Changing the reporting source from "Adobe Target" to "Analytics" and vice-versa </li> 
      <li id="li_E023DDA7ED9142B58D54F42904ADC994">Changing the goal metric type </li> 
      <li id="li_619F4765CEEC48E0A45E1821C282A082">Changing options in the "Advanced Settings" panel </li> 
     </ul> </p> <p>Refer to <a href="automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a> for documentation about Auto-Allocate. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
 </tbody> 
</table>

**Known Issues** 

The following known issues have been reported: 


* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages.
* Some interface issues might occur in Internet Explorer 10, including screen flicker and possible slowness.
* The Chrome version 48 update introduced an issue that causes the Visual Experience Composer to function incorrectly in Chrome. Google is working on a solution. For information, refer to [ https://code.google.com/p/chromium/issues/detail?id=582603 ](https://code.google.com/p/chromium/issues/detail?id=582603). To work around this issue: 
    * Use Firefox or Internet Explorer.
    * Enable the Enhanced Experience Composer, which can be configured from within the ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Preferences] ** tab.




## Adobe Target Standard/Premium 16.2.1 (February 18, 2016) {#section_47E5CEE2EED24CB3B71D7457673F3200}

This release includes the following features and enhancements: 



|  Feature  | Description  |
|---|---|
|  Activity entry targeting by percentage.  | You can now limit entries into [ A/B ](t_test_create_ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) and [ multivariate ](t_create_multivariate_test.md#task_BF870FA60A8245AB8F0B775BE32EA710) activities to a percentage of visitors or audience members. For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience.  |
|  Support for Revenue, Orders, and Engagement in Auto-Allocate  | You can now choose Revenue (RPV), Orders, and Engagement metrics as goals for A/B activities with Auto-Allocation selected. Previously, only conversion metrics were supported. See [ Automated Traffic Allocation ](automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).  |
|  Filter by source  | You can now filter the Activities list by the source where the activity was created. Choice are Adobe Target and Adobe Experience Manager. See [ Activities ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).  |
|  Automated Personalization performance enhancements  | Automated Personalization has been redesigned to perform better with a large number of offer/location combinations.  |

**Known Issues** 

The following known issues have been reported: 


* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages.
* Some interface issues might occur in Internet Explorer 10, including screen flicker and possible slowness.
* The Chrome version 48 update introduced an issue that causes the Visual Experience Composer to function incorrectly in Chrome. Google is working on a solution. For information, refer to [ https://code.google.com/p/chromium/issues/detail?id=582603 ](https://code.google.com/p/chromium/issues/detail?id=582603). To work around this issue: 
    * Use Firefox or Internet Explorer.
    * Enable the Enhanced Experience Composer, which can be configured from within the ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Preferences] ** tab.




## Adobe Target Standard/Premium 16.1.1 (January 28, 2016) {#section_8BF7705B452C449F961AEFC568A0778C}

This release includes the following features and enhancements: 



<table id="table_8525ECC9B6D0435ABEF8C27F747B7A0C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1">Export/Download Summary reports for Automated Personalization and Recommendations Premium </entry> <entry colname="col2"> <p>The ability to download data in a .csv format for quick import into Excel or other data analysis programs has been added to Automated Personalization and Recommendations Premium. </p> <p>This feature was previously only available for A/B, Experience Targeting, and Multivariate activities. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> User interface improvements. </td> 
   <td colname="col2"> <p>The Activities list and Audience list design have been improved, as has the search/sort functionality. Additional user interface changes will be included in upcoming releases. </p> <p>See <a href="c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> "Super" audiences </td> 
   <td colname="col2"> <p>Use nested AND/OR logic when configuring audiences. </p> <p>See <a href="t_create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creating an Audience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Select host groups in reports </td> 
   <td colname="col2"> <p>Host groups are available in reports. </p> <p> <p>Note:  This option is not available for Automated Personalization. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Support for Internet Explorer 11 </td> 
   <td colname="col2"> <p>Internet Explorer 11 is now supported in the Target interface. </p> <p>See <a href="../ov/r_supported_browsers.md#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Supported Browsers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> View Confidence Interval in Target reports for continuous variables </td> 
   <td colname="col2"> <p>Display the Confidence Interval Range for the revenue metric type (RPV, AOV, Sales, Orders), and for engagement metrics. </p> <p>For example, if RPV = 200.00 and CI Range = 50.00 , then this should be displayed for RPV: 200.00 +/- 50.00 </p> <p>This change applies to A/B, Experience Targeting, and Multivariate tests. </p> <p>See <a href="c_confidence_level_and_confidence_interval.md#concept_0D0002A1EBDF420E9C50E2A46F36629B" format="dita" scope="local"> Confidence Level and Confidence Interval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Visual Experience Composer URL rules enhancement </td> 
   <td colname="col2"> <p>Previously, the URL template rules in the Visual Experience Composer formed an OR condition with the Page URL. Now you can choose AND or OR when specifying multiple URLs. OR is the default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: </p> <p>Change in global mbox delivery coding </p> </td> 
   <td colname="col2"> <p>When creating a design, it is now the default to wrap an HTML design in a <span class="codeph"> &amp;lt;div&amp;gt; </span> element. </p> <p>For information about creating a design, see <a href="../recs/t_create_design.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> Create a Design </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Life Time Value (LTV) machine learning reinforcement technique </p> </td> 
   <td colname="col2"> <p>This new algorithm focuses on long-term conversion across many sessions instead of focusing on improving conversion just in this session. This technique is suitable for sites with many returning visitors because it optimizes on overall revenue for the entire interaction with the visitor. </p> <p>See <a href="../target/t_automated_personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhancement: Allow targeting on hash (#) fragments </p> </td> 
   <td colname="col2"> <p>You can now target on the part of a URL that follows a hash (#). </p> <p>See <a href="t_temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Include the Same Experience on Similar Pages </a> and other relevant topics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Download success metrics report </p> </td> 
   <td colname="col2"> <p> Download a single csv file with all success metric listed, instead of a report that only had the final activity goal. </p> <p>See <a href="c_reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6" format="dita" scope="local"> Reports </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* Fixed an issue that caused all AEM-based activities as Experience Targeting (XT) activities. AEM now uses the correct activity types for A/B and XT activities.
* Removed an option to use non-conversion metrics as a goal in new Auto Allocated activities. This restriction will be lifted in an upcoming release.
*
* Fixed an issue that wrapped a non-HTML Recommendations template in a ` &amp;lt;div&amp;gt;` element when used in a form-based workflow.
*
*
*


**Known Issues** 

The following known issues have been reported: 


*
* Some interface issues might occur in Internet Explorer 10, including screen flicker and possible slowness.
* The Chrome version 48 update introduced an issue that causes the Visual Experience Composer to function incorrectly in Chrome. Google is working on a solution. For information, refer to [ https://code.google.com/p/chromium/issues/detail?id=582603 ](https://code.google.com/p/chromium/issues/detail?id=582603). To work around this issue: 
    * Use Firefox or Internet Explorer.
    * Enable the Enhanced Experience Composer, which can be configured from within the ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Preferences] ** tab.



