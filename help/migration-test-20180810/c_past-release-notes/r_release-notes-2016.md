---
description: null
seo-description: null
seo-title: 2016 Releases
title: 2016 Releases
uuid: f5f297ab-d2a9-4e0a-bfd8-8565fdfd537a
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
   <td colname="col2"> <p>We've now made it easier to determine a winner in an Auto-Allocate A/B activity. </p> <p>Many marketers make the mistake of prematurely declaring a winning experience before the results indicate the clear winner. </p> <p>When using the <span class="wintitle"> Automated Traffic Allocation </span> feature, <span class="keyword"> Target </span> displays a badge at the top of the activity's page indicating "No Winner Yet" until the activity reaches the minimum number of conversions with sufficient confidence. When a clear winner is declared, <span class="keyword"> Target </span> displays "Winner: Experience X." </p> <p>For more information, see <a href="automated_traffic_allocation.xml#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a> and <a href="automated_traffic_allocation.xml#concept_5741A89ED7224E1285A3BC34B2CCD0F9" format="dita" scope="local"> Determine a Winner </a>. </p> <p> <p>Note:  Auto-Allocate A/B activities are no longer supported in Analytics for Target (A4T) going forward. With this release, any active Auto-Allocate A/B activities with A4T enabled will be switched to <span class="wintitle"> Manual </span> mode (equal traffic allocation). </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target mobile devices by carrier </td> 
   <td colname="col2"> <p>Create an audience to target mobile devices based on mobile carrier (Verizon, Sprint, AT&amp;T, T-Mobile, etc.). The <span class="wintitle"> Mobile Carrier </span> option is under the <span class="wintitle"> Geo </span> settings. </p> <p>For more information, see <a href="c_target_rules.xml#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Generate mboxTrace authentication token from Target UI </td> 
   <td colname="col2"> <p>Enable advanced <span class="keyword"> Target </span> debugging tools by creating a temporary authentication token. </p> <p>Click <span class="uicontrol"> Generate Authentication Token </span> on the <span class="wintitle"> Implementation Details </span> page ( <span class="uicontrol"> Setup </span> &gt; <span class="uicontrol"> Implementation </span>). You can then add the resulting parameter to your web page URLs for troubleshooting purposes. </p> <p>For more information, see "Retrieve the Authorization Token to Use With Debugging Tools" in <a href="c_manage_content.xml#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Troubleshooting Content Delivery </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Criteria set sequencing </td> 
   <td colname="col2"> <p>Use sets of up to five pre-created criteria in a single experience for greater control over the recommendations presented to visitors. </p> <p>For more information, see <a href="../recs/c_algorithms.xml#task_8A9CB465F28D44899F69F38AD27352FE" format="dita" scope="local"> Creating Criteria Sequences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Insert external promotions </td> 
   <td colname="col2"> <p>Add promoted items and control their placement in your Recommendations designs. </p> <p>For more information, see <a href="../recs/t_create_recs_activity.xml#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> Adding Promotions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="firstlook"> <p><b>First Look</b> </p> Auto-targeting in A/B activities </td> 
   <td colname="col2"> <p> <p>Note:  This "First Look" offering is enabled for a few customers in this release for testing and feedback. </p> </p> <p>Automatically target experiences in A/B tests to serve the right experience to the right visitor. </p> <p>For more information, see <a href="c_auto-target-to-optimize.xml#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </td> 
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
     </ul> </p> <p>For more information, see <a href="../ov2/c_target-atjs-implementation.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
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
   <td colname="col2"> <p>Combine multiple audiences (including <span class="keyword"> Adobe Marketing Cloud </span> audiences and <span class="keyword"> Target </span> audiences) on the fly during the activity-creation workflow. </p> <p>For example, you can target all loyalty customers by including a specific <span class="keyword"> Audience Manager </span> segment for loyalty status and combine it with a <span class="keyword"> Target </span> segment made up of people who signed up for your loyalty program during the current session, instead of creating a third, permanent audience. </p> <p>For more information, see <a href="c_audiences.xml#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Combining Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target visitors during a specific time period </td> 
   <td colname="col2"> <p>Add start and end dates to target an audience. </p> <p>For example, using the new combined, ad-hoc audiences mentioned above, you can target low-spenders with specific content during the three days leading up to Black Friday and other content after Black Friday. </p> <p>For more information, see <a href="c_target_rules.xml#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Save smart collections </td> 
   <td colname="col2"> <p>Search functionality on the <span class="wintitle"> Content </span> page now includes saved folders, called smart collections, to save time when performing similar searches. </p> <p>For more information, see <a href="c_manage_content.xml#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> Search Content and Create Smart Collections </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Add a link to an image. The link can be a click-through link, destination link, or a landing link. </p> <p>For more information, see <a href="t_form_experience_composer.xml#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
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
     </ul> </p> <p>For more information, see <a href="../ov2/c_target-atjs-implementation.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
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
   <td colname="col2"> <p>Combine multiple audiences (including <span class="keyword"> Adobe Marketing Cloud </span> audiences and <span class="keyword"> Target </span> audiences) on the fly during the activity-creation workflow. </p> <p>For example, you can target all loyalty customers by including a specific <span class="keyword"> Audience Manager </span> segment for loyalty status and combine it with a <span class="keyword"> Target </span> segment made up of people who signed up for your loyalty program during the current session, instead of creating a third, permanent audience. </p> <p>For more information, see <a href="c_audiences.xml#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Combining Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target visitors during a specific time period </td> 
   <td colname="col2"> <p>Add start and end dates to target an audience. </p> <p>For example, using the new combined, ad-hoc audiences mentioned above, you can target low-spenders with specific content during the three days leading up to Black Friday and other content after Black Friday. </p> <p>For more information, see <a href="c_target_rules.xml#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Save smart collections </td> 
   <td colname="col2"> <p>Search functionality on the <span class="wintitle"> Content </span> page now includes saved folders, called smart collections, to save time when performing similar searches. </p> <p>For more information, see <a href="c_manage_content.xml#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> Search Content and Create Smart Collections </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Add a link to an image. The link can be a click-through link, destination link, or a landing link. </p> <p>For more information, see <a href="t_form_experience_composer.xml#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
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
      <li id="li_41C2D2E552BF4F8E8A4375AF368F7728"> <p>Added an <span class="codeph"> optoutEnabled </span> setting to support future Adobe Marketing Cloud opt-out functionality. The default value is false. If this property is enabled, all requests execute asynchronously against the <span class="filepath"> /ajax </span> endpoint, just like version 60. </p> </li> 
     </ul> </p> <p>For more information about all the changes in <span class="filepath"> mbox.js </span> version 61, see <a href="../ov/t_mbox_download.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> mbox.js Version Details </a>. </p> </td> 
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
   <td colname="col2"> <p>Organize your sites and pre-production environments for easy management and separated reporting. </p> <p>Hosts are bundled into environments for ease of management. The preset environments include Production, Staging, and Development. You can also add new environments. </p> <p>This feature achieves feature parity with <span class="keyword"> Target Classic </span>. </p> <p>For more information, see <a href="../ov2/c_hosts.xml#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> Hosts </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Category Affinity </p> </td> 
   <td colname="col2"> <p>The category affinity feature automatically captures the categories a user visits and calculates the user's affinity for the category so it can be targeted and segmented on. This helps to ensure that content is targeted to visitors who are most likely to act on that information. </p> <p>This feature achieves feature parity with <span class="keyword"> Target Classic </span>. </p> <p>For more information, see <a href="c_target_rules.xml#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local"> Category Affinity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enable/Disable Enhanced Experience Composer at the activity level </p> </td> 
   <td colname="col2"> <p>Enable/disable the <span class="wintitle"> Enhanced Experience Composer </span> at the account level (applies to all activities created in the account) or at the individual activity level. </p> <p>Previously, you could enable/disable the Enhanced Experience Composer only at the account level. </p> <p>For more information, see <a href="c_experiences.xml#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a>. </p> </td> 
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
   <td colname="col2"> <p>The code editor UI has been updated to be more intuitive and easier to use. </p> <p>For more information, see <a href="../target/c_vec_code_editor.xml#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a>. </p> </td> 
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
   <td colname="col2"> <p>July 14, 2016 </p> <p> <span class="filepath"> at.js </span> version 0.9.1 is now available. </p> <p>For more information, see <a href="../ov2/c_target-atjs-implementation.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js </span> version 61 </p> </td> 
   <td colname="col2"> <p>July 28, 2016 </p> <p> <span class="codeph"> mbox.js </span> version 61 is now available for download. Version 61 is not currently the default download. </p> <p>For more information, see <a href="../ov/t_mbox_download.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> mbox.js Version Details </a>. </p> </td> 
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
      <li id="li_D321FAED82944D2685DA69EB310D80BE"><b>A/B Test: </b> <a href="../target/t_test_ab.xml#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_12ECDFD71DB94E22A85AB13B487E8503"><b>Automated Personalization: </b> <a href="../target/t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a> </li> 
      <li id="li_84B893C214994246AB36E28E84C51460"><b>Experience Targeting: </b> <a href="../target/t_experience_target.xml#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_26533B659C0E49D6A6D3B3FEBE9CA930"><b>Multivariate Test: </b> <a href="../mvt/c_multivariate_testing.xml#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_FBACF2B73B2E491BBB85618153AC4568"><b>Activities: </b> <a href="c_activities.xml#task_C6B2FF8374724933BE79A83549B9CD02" format="dita" scope="local"> Activity Settings </a> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Multi-valued Recommendations attributes </td> 
   <td colname="col2"> <p>All custom <span class="keyword"> Recommendations </span> attributes can now contain multiple entity values. </p> <p>For more information, see <a href="../recs/c_products.xml#concept_E5CF39BCAC8140309A73828706288322" format="dita" scope="local"> Custom Entity Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dynamic/remote offer support </td> 
   <td colname="col2"> <p>Dynamic content can be part of any form-based activity in <span class="keyword"> Target Standard/Premium </span>. Dynamic content is stored outside of <span class="keyword"> Target </span>. </p> <p>For more information, see <a href="../target/c_manage_content.xml#concept_657016A0E6174C22B89036E9C8A0170F" format="dita" scope="local"> Create Remote Offers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Copy audiences and profile scripts </td> 
   <td colname="col2"> <p>You can now copy an existing audience that you can then edit to create a similar audience. </p> <p>For more information, see <a href="../target/c_audiences.xml#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creating an Audience </a>. </p> <p>You can also copy existing profile scripts. </p> <p>For more information, see <a href="c_target_rules.xml#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profile Script Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Use classes to determine element selectors </td> 
   <td colname="col2"> <p>Element selectors can now be based on classes or IDs in Automated Personalization and Multivariate Test activities. In previous versions, this option was only available for A/B Test activities. </p> <p>For more information, see <a href="../target/c_experiences.xml#concept_4EB7663E255F439B8D24079D23479337" format="dita" scope="local"> Element Selectors Used in the Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Exclude duplicate offers in Automated Personalization activities </td> 
   <td colname="col2"> <p>Users can select an option to prevent offers from offer library from being duplicated when used in different locations in Automated Personalization activities. </p> <p>For more information, see <a href="../target/t_automated_personalization.xml#concept_EF78A3B7CF4A42A0B336A007A576D7A6" format="dita" scope="local"> Exclude Duplicate Offers </a>. </p> </td> 
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
   <td colname="col2"> <p>In Automated Personalization activities, entry criteria (URL targeting, template rules, audience target) are evaluated for each request for more accurate offer delivery. </p> <p>For more information, see <a href="t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
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
   <td colname="col2"> <p>Versions targeted to different audiences can now be set up within experiences in A/B activities. </p> <p>See <a href="t_test_ab.xml#task_0138112E283A4A5B9F8AB9AAF2FBC2FF" format="dita" scope="local"> Target an Experience to Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QA/Preview URLs </td> 
   <td colname="col2"> <p>Preview URLs are now available for the form-based experience composer. </p> <p>See <a href="t_automated_personalization.xml#task_586C6655A6FD4AF08F5678FC3F481EFC" format="dita" scope="local"> View Experience URLs </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1" outputclass="premium">Personalized Recommendations </entry> <entry colname="col2"> <p>Visitor profile attributes can be added to collaborative filtering to return recommendations that are more highly personalized to each visitor. </p> <p>See <xref href="../recs/t_create_new_algorithm.xml#task_8A9CB465F28D44899F69F38AD27352FE" format="dita" scope="local">Creating Criteria</xref>. </p> </entry> </row> --> 
  <!-- <row> <entry colname="col1" outputclass="premium">Content similarity weighting </entry> <entry colname="col2"> <p> Select specific attributes to consider/prioritize in calculating content similarity </p> <p>See <xref href="../recs/c_content_similarity.xml#concept_5402DAFA279C4E46A9A449526889A0CB" format="dita" scope="local">Content Similarity</xref>. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations custom algorithms </td> 
   <td colname="col2"> <p>Custom algorithm mappings can be uploaded in a CSV file. It is no longer required to use the XML-based API. </p> <p>See <a href="../recs/c_algorithms.xml#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> Uploading Custom Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Analytics for Target: Analytics tracking server </td> 
   <td colname="col2"> <p>To ensure proper reporting tracking, you must specify a tracking server when you create or edit activities that use Analytics for Target (A4T). Existing activities will continue to run using current settings. </p> <p>See <a href="../a4t/a4t.xml#task_72077BA7E93C4A65A715A18F32228823" format="dita" scope="local"> Using an Analytics Tracking Server </a>. </p> </td> 
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


* [ Mbox.js version 60 ](t_mbox_download.md#section_3BDAB885FA13444A8D35940A4BFF5825) is now the default download.
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
   <td colname="col2"> See <a href="r_release-notes-2016.xml#reference_607661929B504CCFAB3791B13C0DCDBE/section_6A44C277E82D409AB6DCD0901F43794A" format="dita" scope="local"> New Target Implementation Library, at.js 0.8.0 (May 5, 2016) </a>, above. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Marketing Cloud Notifications </td> 
   <td colname="col2"> <p>Notifications from Target are visible in all Adobe Marketing Cloud solutions. Notifications are automatically sent when an activity is activated or deactivated. These notifications are available to all users with access to Target Standard/Premium. </p> <p>Notifications are also visible in Target Standard/Premium. </p> <p>See <a href="c_notifications.xml#concept_557351F8BB7D40F39A65951A77B79D62" format="dita" scope="local"> Notifications </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> User Interface Improvements </td> 
   <td colname="col2"> <p>The user interface has been changed significantly in this release. Among the most noticeable changes are: </p> <p> 
     <ul id="ul_28F382C60ADE43F5A3A4BD0CD5A5CE52"> 
      <li id="li_C47240826E5844D6843314F453F042FC">Navigation has moved from the left to the top </li> 
      <li id="li_3BB03504E98C40CC85583DCD9A4CEA06">Improved dialog boxes </li> 
      <li id="li_AE71506DF1E748A788C40E1F09951732">Improved activity creation flow </li> 
     </ul> </p> <p>The way Marketing Cloud solutions, including Target, are selected has also changed. To access Marketing Cloud solutions and services, click the menu icon: </p> <p style="text-align: center;"> <img href="../graphics/menu-shell-400.png" id="image_6E9323E0EBEA41B1A7319D6BCC43E769" width="400" height="140" /> </p> <p>For more information about accessing Target and making Target your default page after logging in to the Marketing Cloud, see <a href="../ov/c_getting_started.xml#task_5467C72DAFCB4BB583762CAAFC00A5CF" format="dita" scope="local"> Access Target from the Adobe Marketing Cloud </a>. </p> <p>For more information about the user interface improvements, see <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/marketing-cloud-interface.html" format="https" scope="external"> What's New in the Adobe Marketing Cloud - Spring 2016 </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Content similarity weighting (First Look) </entry> <entry colname="col2"> <p> Select specific attributes to consider/prioritize in calculating content similarity </p> <p><xref href="https://jira.corp.adobe.com/browse/TGT-15269">https://jira.corp.adobe.com/browse/TGT-15269</xref></p> <p><xref href="https://jira.corp.adobe.com/browse/TGT-15649">https://jira.corp.adobe.com/browse/TGT-15649</xref></p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> Inclusion rules can be disabled for backup recommendations </td> 
   <td colname="col2"> <p>When backup recommendations are enabled, you can choose not to apply inclusion rules to your backup recommendations. . </p> <p>For more information, see <a href="../recs/c_algorithms.xml#concept_BC16005C7A1E4F1A87E33D16221F4A96" format="dita" scope="local"> Content Settings </a>. </p> </td> 
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
   <td colname="col2"> Automated Personalization now supports the ability to limit a success metric to only count if a previous success metric has already been met. <p>For more information, see <a href="r_success_metrics.xml#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Reports Summary View Download </td> 
   <td colname="col2"> The download option now allows users to download summary view (i.e. comparing Control and Automated traffic) as broken down by all available success metrics. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Customer attributes can be used as tokens in offers </td> 
   <td colname="col2"> <p>Previously, customer attributes could be referenced in profile scripts, formatted as <span class="codeph"> crs.get('&lt; <span class="varname"> Datasource Name </span>&gt;.&lt; <span class="varname"> Attribute name </span>&gt;') </span>. </p> <p>Now, the attributes are available as tokens in profile scripts and directly in offers without first requiring a profile script. The token should be in the form: <span class="codeph"> $crs. <span class="varname"> datasourceName </span>. <span class="varname"> attributeName </span> </span>. </p> <p>See <a href="c_target_rules.xml#reference_F5D9EF735F1044C38E208F3A178903B2/section_62B4821EB6564FF4A14159A837AD4EDB" format="dita" scope="local"> CRS Tokens </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Custom Code enhancement </td> 
   <td colname="col2"> Custom code can now execute the JavaScript code in the <span class="codeph"> &amp;lt;head&amp;gt; </span> tag. Execution of code no longer waits for the <span class="codeph"> &amp;lt;body&amp;gt; </span> tag to be present in DOM. Earlier, the selector was only the first element in the <span class="codeph"> &amp;lt;body&amp;gt; </span> tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New Instructional Videos </td> 
   <td colname="col2"> Instructional videos have been added to help. Currently, you can view videos about the <a href="c_experiences.xml#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Visual Experience Composer and Form-Based Experience Composer </a>. More videos will be added in the coming weeks. </td> 
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
     </ul> </p> <p>See <a href="../ov2/c_target-atjs-implementation.xml#concept_8AC8D169E02944B1A547A0CAD97EAC17" format="dita" scope="local"> at.js Implementation </a> for documentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dependent Success Metrics </td> 
   <td colname="col2"> <p>This features provides the option per success metric to count someone as reaching the success metric only if they've previously reached a different success metric. </p> <p> For example, a test might change the hero image on the homepage. The marketer might only want to count conversions for people who clicked the hero image. So, the marketer can set a success metric for "clicked on homepage hero" and then another metric for purchasing. Then, the marketer can add a rule on the "purchasing" metric to ensure visitors have first reached the "clicked on homepage hero" success metric. </p> <p> <p>Note:  If audience targeting on a location in a success metric is set, this feature is not supported for that metric. </p> </p> <p> Dependent Success Metrics are only supported in AB, XT, and MVT activities. Automated Personalization and Recommendations support will be available later. </p> <p>For more information, see <a href="r_success_metrics.xml#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Auto-Allocate usability improvements </td> 
   <td colname="col2"> <p>After the model for an Auto-Allocate activity is ready, the following operations from the UI are not allowed: </p> <p> 
     <ul id="ul_52B790B2B0D746769A3471E09CE1A122"> 
      <li id="li_B9F0FFF019CE4CB697F5D0B60061DC27">Switching the "Traffic Allocation" mode to "Manual" </li> 
      <li id="li_C271B0BE4C5C4B06BB21703239E7B061">Changing the reporting source from "Adobe Target" to "Analytics" and vice-versa </li> 
      <li id="li_E023DDA7ED9142B58D54F42904ADC994">Changing the goal metric type </li> 
      <li id="li_619F4765CEEC48E0A45E1821C282A082">Changing options in the "Advanced Settings" panel </li> 
     </ul> </p> <p>Refer to <a href="automated_traffic_allocation.xml#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a> for documentation about Auto-Allocate. </p> </td> 
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
|  Activity entry targeting by percentage.  | You can now limit entries into [ A/B ](t_test_ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) and [ multivariate ](c_multivariate_testing.md#task_BF870FA60A8245AB8F0B775BE32EA710) activities to a percentage of visitors or audience members. For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience.  |
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
   <td colname="col2"> <p>The Activities list and Audience list design have been improved, as has the search/sort functionality. Additional user interface changes will be included in upcoming releases. </p> <p>See <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> "Super" audiences </td> 
   <td colname="col2"> <p>Use nested AND/OR logic when configuring audiences. </p> <p>See <a href="c_audiences.xml#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creating an Audience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Select host groups in reports </td> 
   <td colname="col2"> <p>Host groups are available in reports. </p> <p> <p>Note:  This option is not available for Automated Personalization. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Support for Internet Explorer 11 </td> 
   <td colname="col2"> <p>Internet Explorer 11 is now supported in the Target interface. </p> <p>See <a href="../ov/c_implementing_target.xml#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Supported Browsers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> View Confidence Interval in Target reports for continuous variables </td> 
   <td colname="col2"> <p>Display the Confidence Interval Range for the revenue metric type (RPV, AOV, Sales, Orders), and for engagement metrics. </p> <p>For example, if RPV = 200.00 and CI Range = 50.00 , then this should be displayed for RPV: 200.00 +/- 50.00 </p> <p>This change applies to A/B, Experience Targeting, and Multivariate tests. </p> <p>See <a href="c_reports.xml#concept_0D0002A1EBDF420E9C50E2A46F36629B" format="dita" scope="local"> Confidence Level and Confidence Interval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Visual Experience Composer URL rules enhancement </td> 
   <td colname="col2"> <p>Previously, the URL template rules in the Visual Experience Composer formed an OR condition with the Page URL. Now you can choose AND or OR when specifying multiple URLs. OR is the default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: </p> <p>Change in global mbox delivery coding </p> </td> 
   <td colname="col2"> <p>When creating a design, it is now the default to wrap an HTML design in a <span class="codeph"> &amp;lt;div&amp;gt; </span> element. </p> <p>For information about creating a design, see <a href="../recs/c_design-overview.xml#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> Create a Design </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Life Time Value (LTV) machine learning reinforcement technique </p> </td> 
   <td colname="col2"> <p>This new algorithm focuses on long-term conversion across many sessions instead of focusing on improving conversion just in this session. This technique is suitable for sites with many returning visitors because it optimizes on overall revenue for the entire interaction with the visitor. </p> <p>See <a href="../target/t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhancement: Allow targeting on hash (#) fragments </p> </td> 
   <td colname="col2"> <p>You can now target on the part of a URL that follows a hash (#). </p> <p>See <a href="c_experiences.xml#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Include the Same Experience on Similar Pages </a> and other relevant topics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Download success metrics report </p> </td> 
   <td colname="col2"> <p> Download a single csv file with all success metric listed, instead of a report that only had the final activity goal. </p> <p>See <a href="c_reports.xml#concept_B5077F5503AA4C98901AA99EDCE6CDE6" format="dita" scope="local"> Reports </a>. </p> </td> 
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




## Adobe Target Standard/Premium 15.10.1 (November 2, 2015) {#section_B5135D75FA0D42A1A3C2711CA3A1B812}

This release includes the following features and enhancements: 



<table id="table_EE13D9B959DA4FB0AD6BC03FBF78AEF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1">Export/Download Summary reports for Automated Personalization and Recommendations Premium </entry> <entry colname="col2"> <p>The ability to download data in a .csv format for quick import into Excel or other data analysis programs has been added to Automated Personalization and Recommendations Premium. </p> <p>This feature was previously only available for A/B, Experience Targeting, and Multivariate activities. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Auto-Allocate in A/B Tests </p> </td> 
   <td colname="col2"> <p> You now have the option to automatically allocate traffic to increase overall campaign lift and discover winning experiences faster. This algorithm increases the overall campaign performance while maintaining the integrity of an A/B test. </p> <p>The algorithm relies on measured performance (e.g. conversion rate) and confidence intervals to produce a traffic distribution that is changed up to twice per hour. </p> <p>Key Benefits </p> <p> 
     <ul id="ul_A41C74C0C7C844F3A923CD6EA5D5D952"> 
      <li id="li_86D3C6A4993F4DC0907BF42986E6CCD1">Preserves the integrity of an A/B test by ensuring that visitors remain in the same experience, like they do in a manual A/B test </li> 
      <li id="li_B849EB2709F84831A1B7A4F312EAFA7E">Finds a statistically significant winner faster than a manual A/B test </li> 
      <li id="li_3F258C6DEB7245E2924115C5628BC3C6">Provides higher average campaign lift than a manual A/B test </li> 
      <li id="li_C9E82388B93E4A298000984B69CBAEDE">Allows you to toggle to a manual test at any time </li> 
     </ul> </p> <p>See <a href="automated_traffic_allocation.xml#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Customer Attributes </p> </td> 
   <td colname="col2"> <p> Upload 1st party data, called Customer Attributes, using the Marketing Cloud core service and choose attributes to share to Target. This functionality launched in March for Analytics and now integrates directly with Target. </p> <p> For example, you might use customer data such as membership status (gold, silver, etc.), purchase history, favorite destination, local store, and so on in your CRM or eCommerce/POS system. Now you can upload that data to Marketing Cloud. After the user authenticates on your site, Target can match that data to their web behavior. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/attributes.html" format="https" scope="external"> Customer Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Multiple companies are available when selecting Analytics as the reporting source for Target. </p> </td> 
   <td colname="col2"> <p>When selecting Analytics as the reporting source for Target, you select an Analytics report suite to receive Target activity data. To do this, first choose from any of the Analytics companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to Adobe Target will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the Adobe Marketing Cloud to try again. If the report suite is still missing from the list, please contact Customer Care. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/c_integrating_target_with_analytics.html" format="https" scope="external"> Integrating Target with Analytics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New Built-in Options for Audience Creation </p> </td> 
   <td colname="col2"> <p>There are new built-in audience options: </p> <p> 
     <ul id="ul_16E7B53E324B4FB79E1B1E97A1CE65AC"> 
      <li id="li_60B55A81119E48FE83639B9740A2FD21">Target visitors based on which language they use on their browser. This is more accurate than geo-based language targeting. </li> 
      <li id="li_84CAAE7E02CA48FA9C7C00C0415046B6">Target visitors based on browser version, not just which browser is being used. </li> 
      <li id="li_AAF8170CAF4C45BB965D1A9A4E9204D5">You can now Target multiple browsers rather than only one. </li> 
     </ul> </p> <p>See <a href="c_target_rules.xml#concept_221D8EEF53CC45AEACEB17CF336A3658" format="dita" scope="local"> Browser Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p class="Premium">Exclude Past Purchases </p> </td> 
   <td colname="col2"> <p>Target now automatically excludes previously purchased items from a visitor's recommendations. This option can be disabled for any criteria. </p> <p>All out-of-the-box criteria now have this option enabled, including those used in activities that were running prior to this release. If you do not want to exclude past purchases, you should edit those activities. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_data_details.html" format="https" scope="external"> Inclusion Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p> Attribute Weighing </p> </td> 
   <td colname="col2"> <p> Recommendations ranking rules have changed for criteria. This change affects existing Recommendations. </p> <p> Use attribute weighting to "nudge" the algorithm. Marketers can influence the algorithm based on important description or metadata about the content catalog. Apply a higher weighting to these on-sale items so they show more often in the recommendation. Non-sale items are not completely excluded, but they display less often. Multiple weightings can be applied to the same algorithm, and the weightings can be tested on split traffic in the recommendation. </p> <p>These new weights have automatically been applied to all activities. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_attribute_weighting.html" format="https" scope="external"> Attribute Weighting </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Set the Time for Feed Processing </p> </td> 
   <td colname="col2"> <p>Specify the time when you want a feed to update. </p> <p>See <a href="../recs/c_products.xml#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Create Feed </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Use the Feed List to Set a Feed to Never Run </p> </td> 
   <td colname="col2"> <p>From the feed list, set a feed to never run if you do not want to update that feed. </p> <p>See <a href="../recs/c_products.xml#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Create Feed </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Set a New Criteria Type Based on Content Similarity </p> </td> 
   <td colname="col2"> <p>An item-based criteria that can be used for the following: </p> <p> 
     <ul id="ul_86BDF2DE0FCE4665A2985D0C56E50A53"> 
      <li id="li_D83669F9019B431891E072C973B317D7">Current items with similar attributes </li> 
      <li id="li_4E45848423F2450999C699C64E0EE9E2">Last purchased item with similar attributes </li> 
      <li id="li_901D4AAF7BE244FCB9277DC7EDD91E32">Custom attributes that match a specified entity.id and use items with similar attributes </li> 
      <li id="li_49D52B0182F346E982C11A0C2DA50B4F">Last viewed item with similar attributes </li> 
      <li id="li_2DBAF32476AC435EB57D08D96CB55683">Most viewed item with similar attributes </li> 
     </ul> </p> <p>See <a href="../recs/c_algorithms.xml#task_28DB20F968B1451481D8E51BAF947079" format="dita" scope="local"> Inclusion Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New Activity List Filters </td> 
   <td colname="col2"> <p>Several filters have been added to help you show the activities you are most interested in seeing in the Activities list. </p> <p>See <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Enhancement: Industry-Relevant Criteria Configuration </p> </td> 
   <td colname="col2"> <p>Irrelevant options during setup have been eliminated. In the past, some setup options for some industry verticals, such as Media, were not always relevant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>New Out-of-the-Box Criteria </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_47E67312A04E414EB797F9AE2A1F7599"> 
      <li id="li_5EDF9006145B4498B2EAD95D642057C5">More Videos Like This </li> 
      <li id="li_6A8DAACE7CD741D0BB766EBCB52BCD88">More Articles Like This </li> 
      <li id="li_1B44AB35B045416B8D8B72C428750822">More Content Like This </li> 
      <li id="li_FEC84CCF3DF3444DAB39F4764DE897B0">More Slideshows Like This </li> 
      <li id="li_5E874ACB5B004CACBDB4F8FF217BC593">More Products Like This </li> 
     </ul> </p> <p>See <a href="../recs/c_algorithms.xml#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Improved reporting details shown when using Analytics as your reporting source. </td> 
   <td colname="col2"> <p>The details shown by default in an Analytics report when using A4T now match the details shown in the Target report. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* Fixed an issue in the Global Experience Composer that prevented dragging a corner to resize a custom viewport.


**Known Issues** 

The following known issues have been reported: 


*


## Adobe Target Standard/Premium 15.9.1 (September 30, 2015) {#section_A54204291A99476688E8C0BD8255F93C}

This release includes the following features and enhancements: 



<table id="table_907A952F54084C2A9C61F10E2B7A7BFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Mobile Web Experience Composer </td> 
   <td colname="col2"> <p> View your site as it looks on various mobile devices and different screen sizes. Set responsive site breakpoints once and use them across your activities to make sure your optimization activities look great on all the devices your visitors use. </p> <p>See <a href="c_mobile_viewports.xml#concept_8E45527C4ABC41D59AA3553BEDC76FA5" format="dita" scope="local"> Mobile Viewports for Responsive Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Location targeting on form-based activity creation </td> 
   <td colname="col2"> <p> Apply targeting to your mbox locations to limit where your activity displays. </p> <p>See <a href="t_form_experience_composer.xml#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Export/Download Summary reports for Automated Personalization and Recommendations Premium </entry> <entry colname="col2"> <p>The ability to download data in a .csv format for quick import into Excel or other data analysis programs has been added to Automated Personalization and Recommendations Premium. </p> <p>This feature was previously only available for A/B, Experience Targeting, and Multivariate activities. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> Background color selection in Visual Experience Composer for MVT and Automated Personalization activities </td> 
   <td colname="col2"> <p>A color picker enables you to set background colors when editing Automated Personalization and Multivariate Test activities. </p> <p>This feature was previously only available for A/B and Experience Targeting activities. </p> <p>See <a href="c_experiences.xml#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rich Text and HTML editing in Visual Experience Composer for MVT and Automated Personalization activities </td> 
   <td colname="col2"> <p> Text and HTML formatting in a word processor-like window when editing Automated Personalization and Multivariate Test activities. </p> <p> This feature was previously only available for A/B and Experience Targeting activities. </p> <p>These actions provide rich-text editing capabilities by adding HTML tags or applying styles. These modifications by the rich-text editor for any action can be seen in its source view. Users can press the HTML button in the rich-text editor to see the source view. The styles added by the rich-text editor can interfere with customer websites' styles. In this case, users can go to the source view and edit the modifications to align them with their websites' styles. </p> <p>See <a href="c_experiences.xml#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p class="Premium">Form-based recommendations </p> </td> 
   <td colname="col2"> <p> Create recommendations activities for non-site locations including emails, consoles, kiosks, etc. </p> <p>See <a href="t_form_experience_composer.xml#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p> Display information about the key in the design </p> </td> 
   <td colname="col2"> <p>Show the key item in your Recommendations design. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_customizing_a_template.html" format="https" scope="external"> Customizing a Design </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Automated Personalization </p> <p>Conversion-based report </p> </td> 
   <td colname="col2"> <p> If the optimization goal is a conversion metric, then the Offer Detail report now shows the impact of the top predictive variables in lift and incremental conversions. This report was only revenue-based before, so this ability ensures that activities with no revenue data still produce relevant and actionable insights. </p> <p>See <a href="c_reports.xml#concept_C02BAFC922114A44846998FD956E345A" format="dita" scope="local"> Automated Personalization Reports </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adobe Campaign e-mail integration with Target Standard </td> 
   <td colname="col2"> <p> Previously, it was required to use Target Classic to set up a targeted e-mail campaign using Adobe Campaign. With the release of two new features in Target Standard (form-based activity creation and redirect offers) it is now possible to use Target Standard to set up a targeted e-mail campaign with Adobe Campaign. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/c_campaign_and_target.html" format="https" scope="external"> Integrating Target with Adobe Campaign </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Redirect Offers in Form-Based activity creation </td> 
   <td colname="col2"> <p> Support for the redirect offers functionality of Target Classic added in Target Standard form-based activity creation flow. </p> <p>See <a href="t_form_experience_composer.xml#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Experience URLs in activities no longer use on-site cookie </td> 
   <td colname="col2"> <p> The preview experience URLs available per activity are now more reliable. Easily copy the URLs and share with other team members, even if they don't use Adobe Target. </p> <p> <p>Note:  Updated experience URLs only work on activities created after July 30, 2015. Older activities continue to use the cookie-based preview functionality. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Reporting enhancement for Analytics as the reporting source for Target </p> </td> 
   <td colname="col2"> <p> Click to view the full Analytics report directly from the activity report page. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/c_reporting.html" format="https" scope="external"> Reporting </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Activity List performance improvements </td> 
   <td colname="col2"> <p>Greatly improved the load time for activities in the list. Searching and filtering are much faster, particularly when there are a lot of activities in the list. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* Fixed an issue that prevented Target report suites from showing up in the Target report suite selector, after being enabled for Analytics for Target.
*


**Known Issues** 

The following known issues have been reported: 


*


## Adobe Target Standard/Premium 15.8.1 (August 20, 2015) {#section_1C26CB72316A404DB655EBE655F5B8C1}

The goal of this release is to provide feature parity with Target Classic. The most commonly used features of Target Classic are now available in Target Standard. 

This release includes the following features and enhancements: 



<table id="table_DF5B434D639345B4ACE2467B8966A908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Create and edit profile scripts </td> 
   <td colname="col2"> <p>Profile scripts run profile attribute "catchers" on each mbox request. When an mbox request is received, Target runs any relevant profile scripts, determines which activity should run, and displays content that is appropriate to that activity and that experience, then tracks the success of the activity. This enables you to track information about the visit, such as the visitor's location, time of day, number of times that visitor has been to the site, if they've purchased before and so on. This information is then added to the visitor's profile so you can better track that visitor's activity on your site. </p> <p>See <a href="c_target_rules.xml#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profile Attributes </a>. 
     <!--(Copy help from Classic)--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Confidence interval for binary metrics </td> 
   <td colname="col2"> <p>Updated reports using Target-based data show the confidence interval of the lift, compared to the control. </p> <p>See <a href="c_reports.xml#concept_0D0002A1EBDF420E9C50E2A46F36629B" format="dita" scope="local"> Confidence Level and Confidence Interval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Download export activity report data </td> 
   <td colname="col2"> <p>Download data in a .csv format for quick import into Excel or other data analysis programs. This feature works for A/B, Experience Targeting, and Multivariate activities. </p> <p>See <a href="c_reports.xml#concept_B5077F5503AA4C98901AA99EDCE6CDE6/section_3099BC87DCAE46A2B075E1FF5B6552A6" format="dita" scope="local"> Downloading Reports </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rich text and HTML editing in Visual Experience Composer </td> 
   <td colname="col2"> <p>Text formatting options are available when editing text and HTML for A/B and Experience Targeting activities in the Visual Experience Composer. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML. </p> <p>See <a href="c_experiences.xml#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Background color selection in Visual Experience Composer </td> 
   <td colname="col2"> <p>A color picker enables you to set background colors when editing A/B and Experience Targeting activities in the Visual Experience Composer. This option is not available if a background image is set. </p> <p>See <a href="c_experiences.xml#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Archive activity </td> 
   <td colname="col2"> <p>Send an activity to the archive. You can approve an archived activity to make it active again. Activities in the archive do not display by default in the Activities list. </p> <p>See <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization </p> <p>Offer-level targeting </p> </td> 
   <td colname="col2"> <p>Allows marketers to apply targeting rules to offers in Automated Personalization. Makes it possible to exclude specific offers from being shown to a specified group of people. </p> <p>See <a href="t_automated_personalization.xml#task_F207ED7A41B84FD39BB6FCBFABF4B23E" format="dita" scope="local"> Target AP Offers </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1"> <p>Automated Personalization </p> <p>Conversion-based Offer Detail report </p> </entry> <entry colname="col2">Reporting improvement. This new functionality allows the Offer Detail report to report using lift and incremental conversions, metrics that are aligned with the optimization goal. Previously, the Offer Detail report in Automated Personalization always reported on revenue even though the optimization goal was a click-based conversion rate, whether or not the activity had revenue being passed in. This required marketers to specify "estimated revenue per conversion" in the Goals and Metrics page for the report to be meaningful. </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Show number of activities using design </p> </td> 
   <td colname="col2"> <p>The design library shows how many live and inactive activities are using each design. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_create_recs_activity.html" format="https" scope="external"> Creating a Recommendations Activity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Customized dynamic title displays in design </p> </td> 
   <td colname="col2"> <p>Choose a title to display when using a particular design. This title does not have to match the title displayed to visitors on the page. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_create_new_algorithm.html" format="https" scope="external"> Create a New Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>API Token </p> </td> 
   <td colname="col2"> <p>You can set your Client API token from Recommendations Premium. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_setup.html" format="https" scope="external"> Settings </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1" outputclass="premium"> <p>Recommendations Premium </p> <p>Key item's attributes can show in design </p> </entry> <entry colname="col2">The key item, the item your recommendations are based on, such as the item the visitor is currently viewing or the item in the cart, is dynamically shown in the recommendations. In cases where there is no key, a random displays in that template location. </entry> </row> --> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> When entering a URL for an activity or a new page within an activity, a menu shows the most recent and most frequently used URLs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>You can now target multiple mobile devices without requiring a profile script.</p> <p>See <a href="c_target_rules.xml#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobile </a>. 
     <!--<p> <ul id="ul_1F4F703828A845FF82D9797A2B36D801"> <li id="li_E69E5AEAD1914EB29AB0A4234057A481">Browser language </li> <li id="li_81D2E07A84A34E7BBCB2F8DF5C7AEE22">Browser version </li><li id="li_ADB0B297EF0941FC86441C2D5932C13A">Multiple mobile devices </li> </ul> </p>--> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Target Standard/Premium 15.7.1 (July 30, 2015) {#section_9C888BFD04A94DD58616D3F67D209CCC}

This release includes the following features and enhancements: 



<table id="table_46FF5AF77D824ADC941B1E472234F05C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity change log </td> 
   <td colname="col2"> <p>The change log lists changes made to an activity. The action and the user are listed with a timestamp for each change. </p> <p>See <a href="c_activities.xml#task_D6F224E8CE8346699187D21CD9A2B4AB" format="dita" scope="local"> Activity Change Log </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multipage activity </td> 
   <td colname="col2"> <p>A multipage activity enables you to create a story over multiple pages, with a design that is specific to each page. </p> <p>For example, you might want to test an offer for free shipping with purchases above a certain amount. You might want that offer to appear on your landing page, a category page, and certain product pages, but you want it to be a different size and in a different location on each page type. You could display a prominent offer on your home page, then reinforce that offer with smaller offers on other relevant pages. </p> <p>You can also use a multipage activity to define different layouts for your desktop and non-responsive mobile sites. </p> <p>See <a href="c_experiences.xml#concept_277E096063E14813AC5D8EDFA1D2ED48" format="dita" scope="local"> Multipage Activity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based activity creation </td> 
   <td colname="col2"> <p>Create an activity without using the Visual Experience Composer. Instead, choose locations and offers through a form. With this, Target Standard activities can be delivered in emails, mobile apps, kiosks, and other places that don't work with a Visual Experience Composer. </p> <p>See <a href="t_form_experience_composer.xml#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New mbox.js </p> </td> 
   <td colname="col2"> <p> Version 58 of mbox.js ensures the Marketing Cloud Visitor ID service is ready before the Target calls are made. This ensures that audience data shared through the Profiles and Audiences core service are available on the same hit. However, flicker can occur on the page while Target waits for the service to return, so full QA is important before upgrading. This mbox.js version is only available via API. </p> <p>See the <a href="https://marketing.adobe.com/resources/help/en_US/target/ov/r_mboxjs_change_log.html" format="https" scope="external"> mbox.js change log </a> for information about each version of mbox.js. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Configurable success metrics </td> 
   <td colname="col2"> <p> Fine-grained options let you determine how to count success metrics. Options include counting the metric per impression or once per visitor, and choosing whether to keep the user in the activity or removing them. This is equivalent to the "advanced options" for success metrics available in Target Classic. </p> <p>See <a href="r_success_metrics.xml#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Experience Targeting experience limit removed. </td> 
   <td colname="col2"> The previous limit of ten experiences in Experience Targeting has been removed. </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Enhanced click tracking configuration <TGT-9897> </entry> <entry colname="col2"> You can now browse to a different page to set up click tracking for A/B and Experience Targeting activities. </entry> </row> --> 
  <tr> 
   <td colname="col1"> Mbox.js management and editing options </td> 
   <td colname="col2"> <p>All mbox.js configuration and editing is now available within Target Standard. You no longer need to make modifications in Target Classic. </p> <p>See <a href="https://marketing-beta.adobe.com/resources/help/target/ov/r_advanced_mboxjs_settings.html" format="https" scope="external"> Advanced mbox.js Settings </a>. 
     <!--Beta link--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Real-time profile syncing for 3rdPartyId data </td> 
   <td colname="col2"> When a site visitor logs in mid-session and gets a 3rdpartyId, all previously-loaded profile attributes tied to the 3rdPartyId are now immediately available. See <a href="c_target_rules.xml#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Visitor Profile </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations Premium: Facet Name Search </td> 
   <td colname="col2"> You can now search for a facet name. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Automated Personalization: Post-goal metric tracking </td> 
   <td colname="col2"> <p> Previously, Target restarted an experience when the visitor hit the modeling goal. Now, users can be kept in the activity for tracking purposes after reaching the modeling goal. </p> <p> For example, often an Automated Personalization activity is used to improve click-rates, and that is set as the modeling goal. However, it's important to see how increased click-rates lead to final conversion, so tracking through the final conversion is essential. </p> See <a href="t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


*
*
*
*


**Known Issues** 

The following known issues have been reported: 


*


## Adobe Target Standard/Premium 15.6.1 (June 25, 2015) {#section_43FEA310830E4E8E853FAB56B12B1301}

This release includes the following features and enhancements: 



<table id="table_C0B37E1730014ADA8C36310093F5C43A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Configurable success metrics </p> </entry> <entry colname="col2"> <p>Includes advanced options for success metrics, such as <varname>count once</varname>, <varname>restart new experience</varname>, and so on. The default for new activities is now <varname>count once</varname>, replacing the former default of <varname>always convert</varname>. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer compatibility improvements </p> </td> 
   <td colname="col2"> <p> A new account-wide setting to make it easier for Target to generate the right CSS selectors. For example, it can be specified if Target should use classes or IDs. This improves compatibility with AEM. This setting can be overridden per activity </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/ov/t_account_preferences.html" format="https" scope="external"> Account Preferences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting support for Analytics as a reporting source </p> </td> 
   <td colname="col2"> <p>You can now use Analytics as a reporting source for Experience Targeting activities. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/r_xt_goals_and_settings.html" format="https" scope="external"> Goals and Settings </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1"> <p>New mbox.js </p> </entry> <entry colname="col2"> <p>Version 58 of mbox.js adds asynchronous loading. This enables the Visitor ID service to load before the first call is made to Target. This ensures that audience sharing is available on the first hit, which is important if you use the profiles and audiences core service. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: Visual indication of model status </p> </td> 
   <td colname="col2"> <p> Once a predictive model passes the required quality criteria and is deemed valid, it is considered ready and is used to calculate a personalized score for offer decisioning. A clock icon changes to a check mark when the model is ready and Target is able to begin delivering personalized content. Since lift is expected only after the models are ready, the visual indication allows you to set the right expectation. Use the traffic estimator in the Visual Experience Composer to get a guideline of when the models will be ready. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_ap_traffic_estimator.html" format="https" scope="external"> Estimate the Traffic Required for Success </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium Recommendations: Browse and Navigate in the Visual Experience Composer </p> </td> 
   <td colname="col2"> <p> Allows you to open the visual experience composer on one page, and then follow links and form submissions to reach other pages on your site, such as a shopping cart. Once on the page you want to test, flip the Visual Experience Composer back to "Compose" mode and create your experiences. For example, you can change a message on the Shipping page, then test it against the default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium Recommendations: Faceted Catalog Search </p> </td> 
   <td colname="col2"> <p> Provides a more robust way to search your catalog. Also makes it easier to narrow down the search results to very specific set of products. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p> You will now see Target Classic campaigns within the Target Standard Activities list. If you want to filter out Target Classic campaigns and only view Target Standard you can use the "Source" search filter option. For example, to view only Adobe Target Standard activities select the source filter and type "Adobe Target" as the source. The ability to view activities created in Recommendations Classic or Adobe Mobile Services will be added in a future release. </p> <p>You can activate and deactivate activities created in other solutions using the Target user interface. For all other changes you will be need to edit the activities in the source solution. </p> <p> For activities created in other solutions, audience information is not visible on the Overview page. View the audience information in the solution where the activity was created. </p> <p>See <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


*
*
*
*
*
*
*


## Adobe Target Standard/Premium 15.5.1_Hotfix (May 28, 2015) {#section_D751F55A3812417FAA72BD6872AE3C2A}

This hotfix release includes the following fixes: 


*
*
*


## Adobe Target Standard/Premium 15.5.1 (May 21, 2015) {#section_FF0F959908784AF0906EFB9E8324F207}

This release includes the following features and enhancements: 



<table id="table_3985F758176F4884A94AFDFB78B24209"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Custom code entry and editing in Visual Experience Composer </p> </td> 
   <td colname="col2"> <p>Enables you to see, edit, and add new actions using a code editor within the Visual Experience Composer. </p> <p>See <a href="c_vec_code_editor.xml#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Add JavaScript and CSS to the top of your page </p> </td> 
   <td colname="col2"> <p> Add JavaScript code to your page(s) right below the <span class="codeph"> &amp;lt;body&amp;gt; </span> tag, without requiring the selection of an element on your page. </p> <p>See <a href="c_vec_code_editor.xml#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New Audience Creation Options </p> </td> 
   <td colname="col2"> <p>You can now target by the following (located in the Geo section when creating an audience): </p> <p> 
     <ul id="ul_FE1E3605FB8042E9B5E80C0DB0C6C2AD"> 
      <li id="li_6D112A4DB2344B4E9F1B84E943A43DD8">ISP </li> 
      <li id="li_5C95F3F55D194D81905F8138FB546288">Network domain </li> 
      <li id="li_63E3606516BC4FFC8C91E49297542464">Connection speed (options are: broadband, dialup, mobile, t1, t3, satellite) </li> 
     </ul> </p> <p>See <a href="c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium New Features </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6DC206CB52E34498BC762FCCF77807AA"> 
      <li id="li_B26568D642974F17B4B2D6E42CFDC5B9"> <p>New Preview mode to view designs with JavaScript </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_create_recs_activity.html" format="https" scope="external"> Create a Recommendations Activity </a>. </p> </li> 
      <li id="li_B8D1ADE874D244F198CBD3387ED3E310"> <p>Catalog Search now supports free search for English language </p> </li> 
      <li id="li_EB8D595EA8A84B37A3262F76543E1B05"> <p>Account-level support for inputting a static, base url to prepend to all relative <span class="codeph"> entity.thumbnailUrl </span> values </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_setup.html" format="https" scope="external"> Setup </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Recommendations Premium Enhancements </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_1CF5F2D0CDE84DDC9C445B5CD878EEAA"> 
      <li id="li_EB225752776449C6B21C2B2514B508C5"> <p>Improvements to design preview in VEC </p> </li> 
      <li id="li_2CD8267EF166421DBB6EFBF704625848"> <p>Layout improvements on out-of-the-box designs </p> </li> 
      <li id="li_D737754C200844638B536A3BE02E9C5F"> Collection shown in targeting diagram <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_collections.html" format="https" scope="external"> Collections </a>. </p> </li> 
     </ul> </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_recommendations.html" format="https" scope="external"> Recommendations </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Recommendations Classic functionality now supported in Recommendations Premium </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E0D6A9C12B514DE3B3EA753BB4D56662"> 
      <li id="li_2A728C8938834162A0C0C1C926AC5DD9"> Partial template rendering <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_content_settings.html" format="https" scope="external"> Content Settings </a>. </p> </li> 
      <li id="li_B1DFC829D19B4570AB5A7F937C7EF2CC"> Specify backup rules per criteria </li> 
      <li id="li_F8C9690CEC974E37B72A85C2FACFAA6D"> Support FTPS for product feeds <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/t_feeds_create.html" format="https" scope="external"> Create Feed </a>. </p> </li> 
      <li id="li_3C0FA493C87345E4BE994936DF0D0162"> Custom algorithms now appear automatically as criteria <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_algorithms.html" format="https" scope="external"> Criteria </a>. </p> </li> 
      <li id="li_5B074C9FB3CB46EBA6EB4D8B1098480E"> Hourly automatic reindexing of product catalogs for customers without feeds <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_catalog_search.html" format="https" scope="external"> Catalog Search </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: QA links added </p> </td> 
   <td colname="col2"> <p> You can now preview how your experiences will look when delivered. View and share links to your AP experiences on your site to get a "true preview" of the experiences outside of Target's Visual Experience Composer. </p> <p>See <a href="t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics-powered MVT: Preview experience from Performance report </p> </td> 
   <td colname="col2"> <p>When using Analytics as the reporting source for multivariate tests, you can preview your MVT activities from the Performance report. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> A/B tests and Experience Targeting: three-step activity creation flow </p> </td> 
   <td colname="col2"> <p> <a href="t_test_ab.xml#task_68C8079BF9FF4625A3BD6680D554BB72" format="dita" scope="local"> Create A/B </a>and <a href="t_experience_target.xml#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local"> Experience Targeting </a> activity in three steps instead of four. This change makes the process of creating these activities more like the workflow of other activities types, such as Automated Personalization and Multivariate Tests. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics as a reporting source is available with most activity types. </p> </td> 
   <td colname="col2"> <p> The A/B with Analytics activity type no longer exists. The option of using Analytics as your reporting source is now available on the Goal &amp;amp; Settings page for all activity types except Automated Personalization and Experience Targeting. As a result, there is no longer a separate activity type called A/B Test with Analytics Data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p> You will now see Target Classic campaigns within the Target Standard Activities list. If you want to filter out Target Classic campaigns and only view Target Standard you can use the "Source" search filter option. For example, to view only Adobe Target Standard activities select the source filter and type "Adobe Target" as the source. The ability to view activities created in Recommendations Classic or Adobe Mobile Services will be added in a future release. </p> <p>See <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Export Order Audit Report </p> </td> 
   <td colname="col2"> <p> Ability to export/download Order Audit Report added to Target reports. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beta: A4T lift and confidence </p> </td> 
   <td colname="col2"> <p> Lift and confidence now available for Analytics' standard metrics and custom events. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


*
*
*
*


## Adobe Target Standard/Premium15.3.1 (March 26, 2015) {#section_591371851693496C820175753F588E73}

This release includes the following features and enhancements: 



<table id="table_5A2F2058ACFB455E9F69484CA0C8D3DE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer improvements </p> </td> 
   <td colname="col2"> <p>Content that only appears on hover, such as flyout menus and mini-carts, is now selectable for editing in the Visual Experience Composer. </p> <p>See <a href="c_experiences.xml#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Traffic Estimator </p> </td> 
   <td colname="col2"> <p>The Traffic Estimator, formerly available only in the Multivariate Test activity type, is now available for Automated Personalization activities. </p> <p>See <a href="t_automated_personalization.xml#task_71AA6922AFD447EA8C5E610A78ABA714" format="dita" scope="local"> Estimate the Traffic Required for Success </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Visual Preview </p> </td> 
   <td colname="col2"> <p>Visually preview every content combination inside the Visual Experience Composer. </p> <p>See <a href="t_automated_personalization.xml#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> Preview Experiences for an Automated Personalization Test </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: Improved content viewing </p> </td> 
   <td colname="col2"> <p>You can now see every item that qualifies for a collection or exclusion when viewing or editing the collection. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_recommendations.html" format="https" scope="external"> Recommendations </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: Improved search results </p> </td> 
   <td colname="col2"> <p>The total number of items that meet each search string is displayed. </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/recs/c_recommendations.html" format="https" scope="external"> Recommendations </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Upload Customer Attributes in Adobe Analytics </p> </td> 
   <td colname="col2"> <p>Analytics users who capture enterprise customer data in a customer relationship management (CRM) database can upload that data into the Marketing Cloud. </p> <p>Once the data is in the Marketing Cloud, you can, for example, create an audience segment in Analytics that includes customer attributes in the segment definition, and then share that audience with Target. </p> <p> <p>Note:  Target is not yet able to consume raw customer attributes directly. </p> </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/attributes.html" format="https" scope="external"> Customer Attributes </a> in the Marketing Cloud Product Documentation.. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* For Analytics for Target based activities, the Lift and Confidence columns are now hidden for Analytics metrics where the calculations cannot be performed.
* Fixed an issue where the short format of the ` charset` metatag was not recognized in the Enhanced Experience Composer


**Known Issues** 


*
* mbox.js version 56 moved the "extra JavaScript" section so it is executed before global mbox. All settings in v56+ are name spaced. If there are functions declared in "extra JavaScript," they must be prefixed with window. See [ mbox.js Change Log ](https://marketing.adobe.com/resources/help/en_US/target/ov/r_mboxjs_change_log.html). 



## Adobe Target 15.2.1 (February 19, 2015) {#section_9AA19B060D814E08A673FB752E21D0C3}

This release includes the following features and enhancements: 



<table id="table_1558E5A5BAB64CC281C193F5A49E2ECE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p class="premium">New activity type: Recommendations </p> </td> 
   <td colname="col2"> <p>Recommendations activities automatically display products or content that might interest your customers based on previous user activity. Recommendations help direct customers to relevant items they might otherwise not know about. </p> <p>Recommendations is available as part of the Target Premium solution. It is not included with Target Standard without a Target Premium license. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mbox.js v56 </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4D4AEAC314964ECFA6C3A2669233060F"> 
      <li id="li_F71CE15AD70E4A6E9216521E8AE2B102"> Changes for Premium Recommendations to support passing parameters into global mbox </li> 
      <li id="li_11F777D04DE04B848F681997C6458C8B"> Adds a 5 second timeout to the target.js load call. In the rare case that the file doesn't load, the page will render and no Target Standard activities will display. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


*


## Adobe Target 15.1.1 (January 22, 2015) {#section_FC6412353DE64E848FFD5E8EFF72C7C7}

This release includes the following features and enhancements: 



<table id="table_4BA8DA701BC64427957355E144570EFE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> New activity type: Multivariate test </td> 
   <td colname="col2"> <p> A full-factorial multivariate test compares all possible combinations of offers in your content areas to help you determine the best possible combination of content. Multivariate tests also show which content in which areas most contributes to activity success. A common use of multivariate tests is to optimize an entire page after you've used an A/B test to determine an optimal layout. With the multivariate test, you can optimize the individual assets on the page (such as the main image, headlines, or promotional content). </p> <p>See <a href="https://marketing.adobe.com/resources/help/en_US/target/mvt/c_multivariate_testing.html" format="https" scope="external"> Multivariate Test </a> for more information. </p> <p>For an introductory video, see <a href="https://my.adobeconnect.com/p2k6u8iiu6l/" format="https" scope="external"> https://my.adobeconnect.com/p2k6u8iiu6l/ </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browse to pages and in-page elements in the Visual Experience Composer </td> 
   <td colname="col2"> <p> Allows you to open the visual experience composer on one page, and then follow links and form submissions to reach other pages on your site, such as a shopping cart. Once on the page you want to test, flip the Visual Experience Composer back to "Compose" mode and create your experiences. For example, you can change a message on the Shipping page, then test it against the default. </p> <p> The Browse mode also lets you interact with a page to get to the right state, such as going through an image carousel, open a mini-cart, or close a pop-up. Once the page is in the state you need, flip to "Compose" mode and create your test. </p> <p> Currently works with A/B tests, experience targeting, and A/B tests with Analytics. </p> <p>See <a href="c_experiences.xml#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobile device targeting </td> 
   <td colname="col2"> You can select mobile device options when creating an audience. <p>See <a href="c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Audiences </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Click tracking (Automated Personalization) </td> 
   <td colname="col2"> <p>You can now track clicks in Automated Personalization. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mboxTrace debugging utility </td> 
   <td colname="col2"> <p> Examine details about your Target page implementation and activity/experience delivery status for improved troubleshooting. </p> <p>See <a href="c_manage_content.xml#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Troubleshooting Content Delivery </a> for more information. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

This release includes the following fixes: 


* Fixed an issue where scrolling did not work properly in IE10.

