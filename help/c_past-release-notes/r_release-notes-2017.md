---
description: null
seo-description: null
seo-title: 2017 Releases
title: 2017 Releases
uuid: e06b3e56-0d74-4ef0-b740-aaa832570bd8
index: y
internal: n
snippet: y
translate: y
---

# 2017 Releases


## Target Platform (November 8, 2017) {#section_3A2216543B064D6F82EC03E1F8AEC74D}

This release includes the following features and enhancements: 



<table id="table_872FE2BE61CC4A5CA369D9A6C730686E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" morerows="1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js version 1.2.2 is now available. For more information, see <a href="../ov2/c_target-configure-atjs.xml#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Download at.js </a>. </p> <p> 
     <ul id="ul_3C4C9385A0F3489AA2137A2C88AE93CF"> 
      <li id="li_E658799D930547E6901ACFBF7C541F1F"> <p>Fixed an issue that returned a JavaScript error when the Target library loaded on a page using QUIRKS mode. (TNT-28312) </p> </li> 
      <li id="li_050620115ED84CBDA736D94E9AAC6550"> <p>Fixed an issue that caused Target click tracking to break Analytics data collection calls. (TNT-28261) </p> </li> 
      <li id="li_97BC1B7295364ACDAD3FB07005ED592F"> <p>Fixed an issue that caused <span class="codeph"> getOffer() params </span> to fail when <span class="codeph"> targetPageParams() </span> returns an empty string. (TNT-28359) </p> </li> 
      <li id="li_B542D4A4E37141BA8BE79D416E1B58DB"> <p>Fixed an issue with session ID generation when using x-only. (TNT-28361) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>The default timeout for at.js is changed from 15 seconds to 5 seconds. </p> <p>If your current setting was 15 seconds, it will be updated to the new default of 5 seconds. If you previously changed it to something different, your setting will not be affected. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mbox.js </p> </td> 
   <td colname="col2"> <p>The default timeout for mbox.js changed from 15 seconds to 5 seconds. </p> <p>If your current setting was 15 seconds, it will be updated to the new default of 5 seconds. If you previously changed it to something different, your setting will not be affected. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.11.1 (November 8, 2017) {#section_324A9B1DA0B14F5999FEE41F15B13A44}

This release includes the following features and enhancements (issue numbers in parentheses are for internal Adobe use): 



<table id="table_6ADDF3552AD04666B76F2D3F457BB042"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Offers </p> </td> 
   <td colname="col2"> <p> If a user has the "Editor" permission, that user cannot edit an offer referenced to a live or scheduled activity. </p> <p> <p>Note:  For Target Premium customers using <a href="https://marketing.adobe.com/resources/help/en_US/target/target/property_channel.html" format="html" scope="external"> Enterprise User Permissions </a>, if a user selects the All Workspaces option, Target uses the highest permission of the user across workspaces. If the highest permission is "Editor," Target restricts editing as mentioned above </p>. </p> <p>These restrictions apply to all offers, not just offers created in Target. (TGT-27276) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Response tokens </p> </td> 
   <td colname="col2"> <p>Added the following built-in parameters: </p> <p> 
     <ul id="ul_17AD5B9788514E9DB14ED435A4224BFE"> 
      <li id="li_334F10A5B7934215B4D37278901BAF96"> <p>profile.tntId </p> </li> 
      <li id="li_AA9B4611035344549CC933FFC499289F"> <p>profile.marketingCloudVisitorId </p> </li> 
      <li id="li_DD751027371D4293BF9DB872278BD1B3"> <p>profile.thirdPartyId </p> </li> 
      <li id="li_B6D983A1B68D49AAA40CB401437676F1"> <p>profile.categoryAffinity </p> </li> 
      <li id="li_F5E86BFD14CA4C198F36F3F9987750F9"> <p>profile.categoryAffinities </p> </li> 
     </ul> </p> <p>For more information, see <a href="c_response-tokens.xml#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Response Tokens </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.10.1 (October 25, 2017) {#section_EF74751744024C209A02F45322642D37}

This release includes the following features and enhancements (issue numbers in parentheses are for internal Adobe use): 



<table id="table_307DF0CD143048BC9E419444C556B8FB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6E91AEC68A6E45D8B2907C77E752FEC6"> 
      <li id="li_A5778B528358433DB31D700D8F9BCB79"> <p>You can create activity-only audiences from within the three-step guided workflow when creating an activity. This audience can be used in other places within the same activity, but is not stored in the Audiences Library for use in other activities. (TGT-25474) </p> <p style="text-align: center;"> <img href="../assets/adhoc audience.png" id="image_32C7C8B72F51425595A2E266AEFA17E9" /> </p> <p>For more information, see <a href="creating-activity-only-audience.xml#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Creating an Activity-Only Audience </a>. </p> </li> 
      <li id="li_691812682A5B42C0941324F2BC7D5740"> <p>For all activities, you can choose a success metric that qualifies the user for the audience. In the past, Target qualified users for an audience when they entered the activity, whereas now you can choose when to evaluate the audience by choosing a success metric. (TGT-15805) </p> <p style="text-align: center;"> <img href="../assets/success metric.png" id="image_0CEC6015A2C4429790A063FE54CC1A35" /> </p> </li> 
     </ul> </p> <p>For more information, see <a href="c_apply-reporting-audience-success-metric.xml#concept_5F11149ACCA84FE79C7B9F766B6B0595" format="dita" scope="local"> Apply a Reporting Audience to a Success Metric </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Auto-Target </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6F89BD36373E47C4B3A6F8584D431D82"> 
      <li id="li_5F7B590AF8F24066ADD270E9F75CB12F"> <p>Auto-Target activities now support segment-level reporting. (TGT-22777) </p> <p>For more information, see <a href="c_auto-target-to-optimize.xml#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </li> 
      <li id="li_35042E7D6BB04265B42F08A23A774E92"> <p>You can change the Control percentage for Auto-Target activities. (TGT-26467) </p> <p style="text-align: center;"> <img href="../assets/auto-target-control-small.png" id="image_81F6F61DB61240C289FB71362851AA53" /> </p> <p>For more information, see <a href="c_auto-target-to-optimize.xml#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_667DDEDDC5284C8393F8BCA5CD9EF12A"> 
      <li id="li_E00DB93297EC4100B46E42D867757DAA"> <p>You can now view offer definition details on a pop-up card in the Offers Library without opening the offer. (TGT-26377) </p> <p style="text-align: center;"> <img href="../assets/offer-card.png" id="image_1980AE8E9BED424085CC482C773C20EC" /> </p> <p>For more information, see <a href="c_manage_content.xml#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. </p> </li> 
      <li id="li_F71AC4FDAC0E4BEE81D39490E82686C0"> <p>You can copy and edit offers and folders in the Offer selector while creating an activity. (TGT-26936) </p> <p style="text-align: center;"> <img href="../assets/offer-picker.png" id="image_1077A6C7A8DD40FB9370CB55BD7260E5" /> </p> <p>For more information, see <a href="c_manage_content.xml#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Form-based Experience Composer </p> </td> 
   <td colname="col2"> <p>In the Form-based Experience Composer, Refinements have been replaced with full audience functionality. Refinements for existing activities have been migrated to activity-only audiences. (TGT-13646) </p> <p>For more information, see <a href="t_form_experience_composer.xml#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Response Tokens </p> </td> 
   <td colname="col2"> <p>You can now create response tokens from Target without waiting for them to be created in or imported to Target. Previously, in the Response Token UI, you could see only the tokens created via API. Changes to the feature also help you avoid response tokens duplicates. (TGT-26534) </p> <p>For more information, see <a href="c_response-tokens.xml#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Response Tokens </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following customer-facing enhancements, fixes, and changes: 


* You can delete imported audiences (Target Classic, Experience Cloud, etc.) from the Audience Library. Target warns you if you try to delete an audience used for an active activity. (TGT-25171) 

* Audiences imported from Target Classic are now labeled as Adobe Target Classic in the Audience Library. In the past, the UI did not differentiate between Target Standard/Premium and Target Classic. (TGT-27093) 

* Collections now apply to all criteria (including recently viewed items). (TGT-26646) 

* You can filter by Workspace in the Audience Library and Offer Library (applies to Target Premium users with Enterprise User Permissions). (TGT-26813) 

* Made improvements in the Reports UI for better scrolling in tables and placements of filter drop-down lists. (TGT-23713 &amp;amp; TGT-26819) 



## Target Platform Changes (October 13, 2017) {#section_6C298C5C3D01415CB4B658EB2166096C}



<table id="table_8457FAE3508F454F9DFDEF093FBD7E40"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>October 13, 2017</b> </p> <p> <span class="filepath"> at.js </span> version 1.2.1 is now available. For more information, see <a href="../ov2/r_target-atjs-versions.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> <p> 
     <ul id="ul_14D6BB3B51974789BBFC036A45B7A56B"> 
      <li id="li_AE9826C8FC4A4DF4BE61BB72C2946C93"> <p>Fixed an issue when click tracking on a link with target="_blank" prevented Target from opening the link in a new tab. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.9.1 (September 25, 2017 &amp; October 12, 2017) {#section_ECC5DD8B6ED443788B46F53E25FC896E}

This release includes the following features and enhancements (issue numbers in parentheses are for internal Adobe use): 



<table id="table_0A8817F64F434875A485FD671C6988AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p> Mobile Experience Preview </p> </td> 
   <td colname="col2"> <p><b>Updated: October 12, 2017</b> </p> <p> You can now select multiple mobile app activities from the UI and preview them on your device. This feature will allow you to enroll yourself into multiple experiences for previewing and QA without relying on special test builds and simulators. </p> <p>This feature requires that you download and install the appropriate 4.14 (or later) version of the Adobe Mobile SDK. </p> <p>For more information, see <a href="target-mobile-preview.xml#concept_5FBF12C2FDFC42429FE4F5CFBD78E19D" format="dita" scope="local"> Target Mobile Preview </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mobile Batch and Prefetch Delivery </p> </td> 
   <td colname="col2"> <p><b>Updated: October 12, 2017</b> </p> <p> Content for multiple mboxes can be pre-fetched in a single call and cached locally on the device without worrying how, when, and if the end user will see the content. </p> <p>This feature requires that you download and install the appropriate 4.14 (or later) version of the Adobe Mobile SDK. </p> <p>For more information, see <a href="c_prefetch-offer-content.xml#concept_A355D9D55E1C429AA31FA4055A1DDFAF" format="dita" scope="local"> Prefetch Offer Content </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activities </p> </td> 
   <td colname="col2"> <p>The following enhancements have been made in the activity-creation workflow: </p> <p> 
     <ul id="ul_2D251AC11FC54E86AE84DEFFB6FDF43C"> 
      <li id="li_AB8F12B3CF654120BD16EAE570517741"> <p>While editing an activity, you can make the desired changes on the currently displayed step, click the drop-down on the split button, then select <span class="wintitle"> Next </span> to advance to the next step, click <span class="wintitle"> Save and Close </span> to save your changes and display the activity's <span class="wintitle"> Overview </span> page, or click <span class="wintitle"> Save </span> to save your changes and remain on that step. </p> <p style="text-align: center;"> <img href="../assets/edit split button 2.png" id="image_ABC7EE42F5D341EC88AACC54CA98DA2F" /> </p> <p>For more information, see <a href="c_edit-activity.xml#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Edit an Activity or Save as Draft </a>. </p> </li> 
      <li id="li_4C71E2570ECF4BBAB08443D89230CE82"> <p>While editing an activity, you can open the desired workflow step, make your changes (for example experience percentages, audiences, and so forth), then save or close the activity without having to advance through the three-step guided workflow. </p> <p style="text-align: center;"> <img href="../assets/edit activity.png" id="image_0B9A2EF729C34A1D9FA84B8B7B17A3C1" /> </p> <p>For more information, see <a href="c_edit-activity.xml#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Edit an Activity or Save as Draft </a>. </p> </li> 
      <li id="li_43C15B13E4F7475E9376A98222AA0253"> <p>When you are creating a new activity that has not yet been saved, or you are editing an activity that was previously saved in draft form, the <span class="wintitle"> Save Draft </span> options display in the split button. </p> <p style="text-align: center;"> <img href="../assets/save draft.png" id="image_3975786947CE4E39B900AA81D838B9B3" /> </p> <p>For more information, see <a href="c_edit-activity.xml#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Edit an Activity or Save as Draft </a>. </p> </li> 
      <li id="li_36EF9AD13B2D40ADB99343C9F758D5FD"> <p>You can now edit or copy an audience by hovering over the desired audience in the <span class="wintitle"> Choose Audience </span> dialog box while choosing targeting in step 2 of the three-step guided workflow. </p> <p style="text-align: center;"> <img href="../assets/audience picker hover.png" id="image_6DC33A0856A346948E517F0BA4C9039F" /> </p> </li> 
     </ul> </p> <p>For more information, see <a href="c_ab_audience.xml#concept_A268236C1224451DB7844BF67F41A087" format="dita" scope="local"> Select Audience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting </p> </td> 
   <td colname="col2"> <p>The following new features and enhancements are available for reporting: </p> <p> 
     <ul id="ul_2D1AF91D1B4E478FBFFA0B83EE30075E"> 
      <li id="li_98E67A4DA8BF4CFF90C279FAC12F4C54"> <p>You can choose the counting methodology for graphs in reports. Note that this is not supported in Auto-Target and Automated Personalization (AP) activities. </p> <p>For more information, see the "Counting Methodology" row in <a href="c_report-settings.xml#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Report Settings </a>. </p> </li> 
      <li id="li_5803CE90DB764C9E983702CB6C1AFEE3"> <p>You can view multiple metrics in a single report for Auto-Target A/B activities. (TGT-23464) </p> <p>For more information, see <a href="c_view-multiple-metrics.xml#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> View Multiple Metrics in a Report </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>You can now view the definitions of audiences imported from Target Classic or created via API. (TGT-22630) </p> <p style="text-align: center;"> <img href="../assets/imported mobile audience rn.png" id="image_6ED9EA63FD7D440286DBAFDBD696BA64" /> </p> <p>For more information, see "Viewing Audience Definitions" in <a href="c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> About Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Code Editor </p> </td> 
   <td colname="col2"> <p>The Form-based Experience Composer and the HTML offers editor now use the same code editor that the Visual Experience Composer (VEC) uses in custom code. (TGT-25808) </p> <p>This enhancement gives you the following features when using the code editor in the Form-based Experience Composer and when creating HTML offers: </p> <p> 
     <ul id="ul_CBB17806FBF34774A8160A61204ED014"> 
      <li id="li_22665F583F1742E280D5BC7EC4203007"> <p>Line numbers are now visible for better usability. </p> </li> 
      <li id="li_B0D863CDAD2E46A4B133BB86886EB527"> <p>Syntax highlighting helps you avoid incorrect syntax for HTML offers. </p> </li> 
     </ul> </p> <p>For more information, see <a href="c_vec_code_editor.xml#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geo Targeting </p> </td> 
   <td colname="col2"> <p>You can now use latitude and longitude in geo-targeting. (TGT-12129) </p> <p>For more information, see <a href="c_geo.xml#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Node.JS SDK </p> </td> 
   <td colname="col2"> <p>You can install the node.js SDK from <a href="https://www.npmjs.com/package/@adobe/target-node-client" format="https" scope="external"> npm @adobe/target-node-client </a> to easily implement and run server-side tests on your node.js applications. The VisitorID service is enabled in the node SDK to connect all your Adobe data and you can use choose to use Adobe Analytics as your reporting source (A4T). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following customer-facing enhancements, fixes, and changes (issue numbers in parentheses are for internal Adobe use): 


* Users with Approver permissions can now generate and enable profile API authentication tokens. (TGT-24074) 

  For more information, see [ Profile API Settings ](c_profile-api-settings.md#concept_5C4ABA5FA64E4D6CAE9C5902572F2794). 

* When creating an activity in the Visual Experience Composer and the user reloads the page, the activity URL and associated properties are retained in the UI. The need to reload can occur if the activity uses mixed content (secure and insecure content) or there are permission issues. (TGT-28230) 

* Improved the messaging when an activity uses mixed content (secure and insecure content). The message provides information to help users perform the necessary steps needed to open an HTTP site or a site that has mixed calls (HTTPS and HTTP). (TGT-26271) 

  For more information, see [ Enabling Mixed Content in Your Browser ](c_mixed_content.md#concept_46D022D50280468C9EF6D5DF6EFC911C). 

* Improved the workflow when a user's Target session times out while configuring options on the Setup, Audiences, and Recommendations pages. When the user clicks Save, the session-expired message displays, but after logging back in, a dialog informs the user of a successful login and the UI remains on the same page in Target with no data loss. (TGT-25557) 



## Target Platform Changes (September 27, 2017) {#section_AC32516DFBA64AD2AC9A74171D452778}



<table id="table_701D8D53D1DF4F28ADAC6EC221B0208A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>September 27, 2017</b> </p> <p> <span class="filepath"> at.js </span> version 1.2.0 is now available as a maintenance release that contains mostly bug fixes. For more information, see <a href="../ov2/r_target-atjs-versions.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> <p> 
     <ul id="ul_D11024549C3643C7A756988087498D24"> 
      <li id="li_E1B3994125B64F6AB20B29FE8BCD8459"> <p>Fixed an issue that prevented default actions for click-tracking special cases. (TNT-28089) </p> </li> 
      <li id="li_53806C902AA04B31B59AA87A1E707348"> <p>Fixed an issue when click-tracking on a link with <span class="codeph"> target="_blank" </span> that prevented Target from opening the link in a new tab. (TNT-28072) </p> </li> 
      <li id="li_94F5794330D14C71BA07B3F17D0705FD"> <p> IP addresses can be used as the cookie domain. (TNT-28002) </p> </li> 
      <li id="li_7D2A11B17672419583F9632CDA00D28F"> <p>Fixed an issue that caused flicker in redirect offers with a global mbox or other regional mboxes. (TNT-27978) </p> </li> 
      <li id="li_BA27A749A7A242478080F3D8E04148FC"> <p> Fixed an issue in Experience Targeting activity setup failing within the VEC when switching between Browse and Compose. (TNT-27942) </p> </li> 
      <li id="li_FA11ABA5B9CD435080426805C5359A51"> <p> Fixed incorrect handling on flicker style classes for click-track elements. (TNT-27896) </p> </li> 
      <li id="li_E2DFBAE52FCA4996BA083868CBFCCD10"> <p>Fixed an issue that caused global mbox parameters to become mixed up with all mbox parameters. (TNT-27846) </p> </li> 
      <li id="li_B3153BBD66AA4D51AE81EF6C903CF78D"> <p>Made changes to ensure that Handlebars, Mustache, and other client-side templating libraries are properly handled by <span class="filepath"> at.js </span>. (TNT-27831) </p> </li> 
      <li id="li_B859939C1B5A4DF78CF8ADF236B88306"> <p>Made changes to ensure that <span class="codeph"> sdidParamExpiry </span> is properly initialized and passed to the Visitor API. This is a regression that has been added to <span class="codeph"> at.js 1.1.0 </span>. Previous <span class="filepath"> at.js </span> versions are not affected. This affects only clients using redirect offers and A4T. (TNT-27791) </p> </li> 
      <li id="li_24A748DFB7824AE6AC7331B7EA940BFF"> <p>Made changes to ensure that <span class="codeph"> SCRIPT </span> is executed regardless of the type attribute being used. (TNT-27865) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting (XT) </p> </td> 
   <td colname="col2"> <p><b>September 21, 2017</b> </p> <p>With the release on September 21, Target will change the way users are placed into experiences in Experience Targeting (XT) activities (Landing Page campaigns in Target Classic). For all new and existing activities in both Target Standard/Premium and Target Classic, users must meet the experience targeting rules on every impression to continue to see the experience's content and to be counted in reports. Previously, if the user no longer qualified for any experience, the user would continue to see the content from, and be counted in reports for, the last experience they did qualify for. </p> <p>This change will happen automatically as part of the release for all existing activities and for any new activities created post-release. If the previous method (prior to September 21) is desired, you can create audiences using profile scripts so a user only must meet a condition once to continue to fall into that audience in the future. Then, use those audiences for each experience in the activity. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.8.1 (August 22, 2017) {#section_71A554D072F04B18B359C1626529E5D8}



<table id="table_AAC16F89060D4CC09762A370B86C0885"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Enterprise User Permissions for Target Premium </p> </td> 
   <td colname="col2"> <p>Create separate workspaces in Target and then assign users different roles and permissions for individual digital properties. </p> <p>For more information, see <a href="property_channel.xml#concept_E396B16FA2024ADBA27BC056138F9838" format="dita" scope="local"> Enterprise User Permissions </a>. </p> <p>See <a href="known-issues-resolved_issues.xml#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Known Issues and Resolved Issues </a> for more information about the rollout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>QA Mode </p> </td> 
   <td colname="col2"> <p>Perform easy activity QA with preview links that never change, optional audience targeting, and QA reporting that stays segmented from live activity data. </p> <p>For more information, see <a href="c_activity-qa.xml#concept_9329EF33DE7D41CA9815C8115DBC4E40" format="dita" scope="local"> Activity QA </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 

This [!DNL  Target] release includes the following customer-facing enhancements, fixes, and changes: (issue numbers in parentheses are for internal Adobe use): 


* We've added more places where you can view audience definition details on a pop-up card in the Target UI without opening the audience. Note that this functionality applies only to audiences created in [!DNL  Target Standard/Premium. (TGT-25772)] 

* You can now view definitions of adhoc audiences inside activity creation/overview. (TGT-25570) 

* The following variables are now available as [ Velocity ](c_customizing_a_template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59) arrays: ` entiites` and ` entityN.categoriesList`. 



## Target Platform Changes (August 3, 2017) {#section_FA5BF6808EA74F3A9E8E941530879208}



<table id="table_1B43199F1AE64E69AE65313B23741444"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>August 3, 2017</b> </p> <p> <span class="filepath"> at.js </span> version 1.1 is now available. For more information, see <a href="../ov2/c_target-configure-atjs.xml#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Download at.js </a>. </p> <p>The following enhancements and fixes are included in <span class="filepath"> at.js </span> version 1.1: </p> <p> 
     <ul id="ul_B7408267413347888938E2E7D48ABDBD"> 
      <li id="li_4DDF6DCFE6014C6795B6A9C9DFB54C21"> <p>Added response token handling. For more information, see <a href="c_response-tokens.xml#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Response Tokens </a>. </p> </li> 
      <li id="li_741CD22B7D074FBA90180B2E36FACE0D"> <p>Resolved issue so that <span class="codeph"> document.currentScript polyfill </span> doesn't interfere with Angular 1.X. </p> </li> 
      <li id="li_EF1B3D3DCC7F4D2490D2BFE660EC661C"> <p>Made changes to ensure that click tracking doesn't interfere with visibility property. Click tracking elements are marked with the <span class="codeph"> at-element-click-tracking </span> CSS class instead of <span class="codeph"> at-element-marker </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js </span> </p> </td> 
   <td colname="col2"> <p><b>July 18, 2017</b> </p> <p> <span class="filepath"> mbox.js </span> version 63 is now available. For more information, see <a href="../ov/t_target-download-config-mbox.xml#task_4EAE26BB84FD4E1D858F411AEDF4B420" format="dita" scope="local"> Download mbox.js </a>. </p> <p>The following enhancements and fixes are included in <span class="filepath"> mbox.js </span> version 63: </p> <p> 
     <ul id="ul_F876FABA804A459D84387102DC38B7DC"> 
      <li id="li_E840AFDFAD394F5E9CDF52FABCA27EF7">Fixes an issue with SDID generation when using <span class="codeph"> mboxDefine() </span> and <span class="codeph"> mboxUpdate() </span>. This affects only clients that have Visitor API on the page. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.7.3 (August 3, 2017) {#section_D90CB766679442C7A0642E5D79657674}



<table id="table_C81EA97B251547169BC9681E5DDB4B8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Response Tokens </p> </td> 
   <td colname="col2"> <p>Response tokens let you automatically output eligible variables (e.g., profile attributes) in the Target responses that deliver activities (i.e. display mboxes). Response tokens can be used for debugging purposes or for integration with 3rd-party providers (such as Clicktale). </p> <p>Response tokens are similar to <span class="keyword"> Adobe Target Classic </span> server plug-ins and provide feature parity between the two solutions. </p> <p> <p>Note:  Response tokens are available with <span class="filepath"> at.js </span> 1.1 or later. Response tokens are not supported with <span class="codeph"> mbox.js </span>. </p> </p> <p>For more information, see <a href="c_response-tokens.xml#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Response Tokens </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.7.2 (July 27, 2017) {#section_6980EC04D3CF4A00919953B9B10BC472}



<table id="table_DB51BD66756F4EBD875ED008B2C7C5D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Auto-Target </p> </td> 
   <td colname="col2"> <p>Auto-Target in now available to all Target Premium customers. </p> <p>Auto-Target uses advanced machine learning to identify multiple high performing marketer-defined experiences, and serves the most tailored experience to each visitor based on their individual customer profile and the behavior of previous visitors with similar profiles, in order to personalize content and drive conversions. </p> <p>While creating an A/B activity using the three-step guided workflow, you can choose to allocate traffic using the <span class="wintitle"> Auto-Target For Personalized Experiences </span> option: </p> <p style="text-align: center;"> <img href="../assets/auto-target-ui-small.png" id="image_DB7899CAD51D411EAB858CE132BECAA5" /> </p> <p>For more information, see <a href="c_auto-target-to-optimize.xml#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.7.1 (July 20, 2017) {#section_BB75DE30174F4ADD963451909FB81D74}



<table id="table_BCE36E0D56804E7B8861858DCF2F380E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>You can now view audience definition details on a pop-up card in various places in the Target UI without opening the audience. Note that this functionality applies only to audiences created in <span class="keyword"> Target Standard/Premium. </span> </p> <p style="text-align: center;"> <img href="../assets/audience details.png" id="image_AD0F411715DA43ACB4A913B1E54C13DC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Success metrics </p> </td> 
   <td colname="col2"> <p>Previously, Target allowed dependency on a single metric and that metric had to be reached before its count incremented. You can now provide dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increment. </p> <p>Multiple-metric dependency functionality is not supported for the following: </p> <p> 
     <ul id="ul_EC856F910B704D648065EA7DA13EE5B0"> 
      <li id="li_1A82414FE50B414CAA1A0A88E80BCC1B"> <p>Recommendations activities. This functionality is supported for all other activity types. </p> </li> 
      <li id="li_2D6CF42264D445FCB6C400ED321DE952"> <p>If you use Analytics as your reporting source (A4T). </p> </li> 
      <li id="li_E3A983A70BB04AE8B25A7CEC1F5FE1D9"> <p>The “Viewed a Page” metric type. </p> </li> 
      <li id="li_9AAF6BB275F7489BA691676E308172D5"> <p>The “Clicked an Element” metric type for Visual Experience Composer (VEC) activities. </p> </li> 
     </ul> </p> <p>For more information, see the following topics: </p> <p> 
     <ul id="ul_4B0EFFDD257C42579E19569DCBE15BE3"> 
      <li id="li_2402575F27F547968BD536C460BF81B5"> <p>A/B: <a href="r_ab_goals_and_settings.xml#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </p> </li> 
      <li id="li_FB5E7CBC0154406C989F5A5C6CAA0C8F"> <p>Automated Personalization (AP): <a href="t_create_ap_activity.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creating an Automated Personalization Activity </a> </p> </li> 
      <li id="li_57C36A7945A24A52BCBD62CA0F15B668"> <p>Experience Targeting (XT): <a href="r_xt_goals_and_settings.xml#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </p> </li> 
      <li id="li_06674A3152A547268A1AE5EE818EF1A5"> <p>Multivariate (MVT): <a href="../mvt/r_goals_and_settings.xml#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting (Auto-Allocate A/B Tests) </p> </td> 
   <td colname="col2"> <p>The ability to view multiple metrics is now available for Auto-Allocate A/B activities.</p> <p>For more information, see <a href="c_view-multiple-metrics.xml#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> View Multiple Metrics in a Report </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>Audience site page types and comparison operators now match types and comparison operators in Target Classic. </p> <p>You can now create site pages audiences using you own "user-defined query parameter" or "user-defined header."</p> <p>For more information, see <a href="c_site_pages.xml#concept_6425D5304568490899E8340CC94798A9" format="dita" scope="local"> Site Pages </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activities </p> </td> 
   <td colname="col2"> <p>The Activity list now lets you filter on Auto Allocate and Auto Target activity types. </p> <p>For more information, see <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Criteria &amp;amp; Promotions </p> </td> 
   <td colname="col2"> <p>You can now handle empty values when filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching. </p> <p>For more information, see <a href="../recs/c_use-dynamic-and-static-inclusion-rules.xml#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This [!DNL  Target] release includes the following customer-facing enhancements and fixes: (issue numbers in parentheses are for internal Adobe use): 


* Improved the workflow when a user's [!DNL  Target] session times out while creating or editing an activity or offer. When the user clicks [!UICONTROL  Save], the session-expired message displays, but after logging back in, a dialog informs the user of a successful login and the UI remains on the same page in [!DNL  Target] with no data loss. 

  If a user performs intermittent action on a [!DNL  Target] page and experiences a session timeout, the user is directed to re-log in and is then directed to the last page worked on in the [!DNL  Target] UI. 

* Fixed an issue that caused custom code changes to be lost if the user browses away (changes experiences, switches page, switches audience, clicks Next, etc.) and forgets to save changes. The user is now prompted to save the changes. (TGT-23766) 

* When an activity is archived, "Archived the activity" displays instead of "Updating the activity." (KB-1517) 

* The drop-down picker in the following locations within the Target UI has been replaced with auto-complete functionality to improve speed and performance: (TGT-22939) 


    * Activity Page &gt; *activity* &gt; Step3 &gt; Report Suite picker 

    * Audiences &amp;gt; Create Audience &amp;gt; Visitor Profile 

    * Recommendations &amp;gt; Feed Creation &amp;gt; When source type &amp;gt; Analytics &amp;gt; Report Suite picker 



* Improved error messaging when a site has "X-Frame-options" set to SAMEORIGIN and the site cannot be loaded in the Visual Experience Composer (VEC). The message prompts the user to switch to the Enhanced Experience Composer in Setup &amp;gt; Preferences. (TGT-17356) 

* Reports in Target Standard/Premium now display in your account's time zone rather than the Target server time zone (US EST). (TGT-24868) 

* If activities created in [!DNL  Target] are updated from outside of [!DNL  Target] (for example, via Adobe I/O), the following activity attributes are imported back into [!DNL  Target]: 

  ` thirdpartyId` 

  ` startDate` 

  ` endDate` 

  ` status` 

  ` priority` 

  ` marketingCloudMetadata(remoteModifiedBy)` 

  This import job will run when the activities page is opened, with a maximum delay of ten minutes. (KB-1526) 



## Target Platform Changes (July 18, 2017) {#section_08A2B80060FE4833B1BDD12D1AF5E3D6}



<table id="table_17607030DA7948819F73FA9F2B22AB5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js </span> </p> </td> 
   <td colname="col2"> <p><b>July 18, 2017</b> </p> <p> <span class="filepath"> mbox.js </span> version 63 is now available. For more information, see <a href="../ov/t_target-download-config-mbox.xml#task_4EAE26BB84FD4E1D858F411AEDF4B420" format="dita" scope="local"> Download mbox.js </a>. </p> <p>The following enhancements and fixes are included in <span class="filepath"> mbox.js </span> version 63: </p> <p> 
     <ul id="ul_6C88DB6332A94858B278F7F846E2F8EB"> 
      <li id="li_597D15CAD9DA44008FEC01E6BB3CB9A7">Fixes an issue with SDID generation when using <span class="codeph"> mboxDefine() </span> and <span class="codeph"> mboxUpdate() </span>. This affects only clients that have Visitor API on the page. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>July 7, 2017</b> </p> <p> <span class="filepath"> at.js </span> version 1.0 is now available. For more information, see <a href="../ov2/c_target-configure-atjs.xml#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Download at.js </a>. </p> <p>The following enhancements and fixes are included in <span class="filepath"> at.js </span> version 1.0: </p> <p> 
     <ul id="ul_4407D3923CE34CD8AD7120A2580A34DF"> 
      <li id="li_34C8D0572A0340DF99294DD33E352D2C"> <p>Support for loading at.js asynchronously for faster page loads. </p> </li> 
      <li id="li_BC944624B3104418854140484E682D69"> <p>Support for pre-hiding page content when loading at.js asynchronously. </p> </li> 
      <li id="li_F9D0AD095A2A425CB78772DDE8FCCF97"> <p>Better error messaging when content delivery is disabled. </p> </li> 
      <li id="li_4B32468665A34FC0AF66C1CD15DE7AFC"> <p>Performance improvements when delivering multiple activities. </p> </li> 
      <li id="li_48EAD25A4077411E954CCCDB95058924"> <p>Support for YUI Compressor. </p> </li> 
      <li id="li_3598B4223C0A478D956A7EC618BFBCD6"> <p>Bug/error reporting for custom events during activity delivery. </p> </li> 
      <li id="li_28A5DDF1A9D64D66BF8BD0E89E5BD69B"> <p>Fix for performance issues in Microsoft Internet Explorer 11. </p> </li> 
      <li id="li_BB1C11A76FB14341AB7699F2C7753377"> <p>Fix for <span class="codeph"> getOffer() </span> function giving an error on some websites. </p> </li> 
      <li id="li_4C7F3DE9A0A346C38E9EDCE21C83843D"> <p>Load the Target library asynchronously. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.6.2 (June 22, 2017) {#section_F0372B07B56E454CB048CE79FF56E9CD}



<table id="table_8C4DB1B83B874E4C85CE9FF352E7B857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization (AP) activities </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F5BB1074DD4140C798CB55D68DEEF824"> 
      <li id="li_9596AABA14C64DEEB2E70E8ADED8AA74">Automated Personalization activities can be created using the form-based composer. </li> 
      <li id="li_315F5FF590404670A677FEA6E4E0DF5D">New confidence numbers for Automated Personalization </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Criteria and Promotions </p> </td> 
   <td colname="col2"> <p> You can now create dynamic criteria and promotions based on profile attribute matching and parameter matching. </p> <p style="text-align: center;"> <img href="../assets/inclusion rules.png" id="image_D136F75A5C2B428390FE231559AEC2D3" /> </p> <p> <p>Note:  If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>VEC Code Editor improvements </p> </td> 
   <td colname="col2"> <p> If the page format changes and actions cannot be applied, an alert now appears next to each failing action. Previously, a general error notified the user that the page structure had changed. Now, the code editor highlights each failed action. </p> </td> 
  </tr> 
 </tbody> 
</table>

This [!DNL  Target] release includes the following customer-facing enhancements and fixes: 


* Improved performance on host groups and recommendations entity search pages.
* More descriptive error messages throughout Target, especially when related to sync failures.
* Fixed an issue that caused the count on activity diagram to sometimes be incorrect in UI when auto-dedupe is applied after creating exclusion groups.
* Fixed an issue where the manual inclusions might not be correctly reflected in UI when an existing activity with Exclusion Group is edited.


## Target Standard/Premium 17.6.1 (June 8, 2017) {#section_1D05FE23CE3744DDB5D28E933341F575}



<table id="table_47117524922A472AA977C652B581B356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting (XT) activities </p> </td> 
   <td colname="col2"> <p>Drag-and-drop functionality lets you arrange audiences and experiences in the desired order while creating or editing XT activities. Visitors will be evaluated for experiences in order, from top to bottom. </p> <p style="text-align: center;"> <img href="../assets/move exp.jpg" id="image_0AA2EE2B5B00462C8E125A30F145E654" /> </p> <p>For more information, see <a href="t_xt_add_experience.xml#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Create Experience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting: A/B, XT, and Recommendations </p> </td> 
   <td colname="col2"> <p>Reports for A/B, XT, and Recommendations activities include visual representations that let you visually see the confidence interval and lift so that you can more accurately determine a winner. You can mouse over the representations to see the actual numbers. This feature is not available for activities that use Analytics as the reporting source (A4T). </p> <p style="text-align: center;"> <img href="../assets/whisker.JPG" id="image_DFD8EED61D52497280066D55AD473479" /> </p> <p>For more information, see <a href="c_report-settings.xml#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Report Settings </a>. </p> </td> 
  </tr> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top-priority activity's content is returned. </p> <p>For more information, see <xref href="c_priority.xml#concept_1780C11FEA57440499F0047DD6900E0F" format="dita" scope="local">Priority</xref>. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization (AP) activities </p> </td> 
   <td colname="col2"> <p>You can create Exclusion Groups in AP activities to ensure that experiences with the designated offers are automatically excluded. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Criteria and Promotions </p> </td> 
   <td colname="col2"> <p><b>(Scheduled to be released June 22, 2017)</b> You can now create dynamic criteria and promotions based on profile attribute matching and parameter matching. </p> <p style="text-align: center;"> <img href="../assets/inclusion rules.png" id="image_694305D969AF43F7822012F69614250C" /> </p> <p>For more information, see <a href="../recs/c_use-dynamic-and-static-inclusion-rules.xml#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. </p> <p> <p>Note:  If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Naming activities </p> </td> 
   <td colname="col2"> <p>You are now prompted to name the activity before saving. You cannot save an activity without a name. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New location for Target Forum </p> </td> 
   <td colname="col2"> <p> The Target Forum has moved to the new <a href="https://forums.adobe.com/community/experience-cloud/marketing-cloud/target" format="https" scope="external"> Adobe Community Platform </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This [!DNL  Target] release includes the following customer-facing enhancements and fixes: (issue numbers in parentheses are for internal Adobe use): 


* Fixed an XSS security issue with [!DNL  mbox.js]. This fix is a server-side fix that does not require an [!DNL  mbox.js] update. 



## Target Standard/Premium 17.4.1 (April 27, 2017) {#section_24E6889AF1E0405497F6F77A407A9A46}

This release includes the following features and enhancements: 



<table id="table_9554D0094421417C88548BDC97B710F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Reporting </td> 
   <td colname="col2"> <p><b>View Multiple Goals/Metrics: </b>You can now view multiple metrics in A/B and Experience Targeting (XT) activities, with the exception of <a href="automated_traffic_allocation.xml#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Auto-Allocate </a> and <a href="c_auto-target-to-optimize.xml#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Target </a> A/B activities. </p> <p>For more information, see <a href="c_view-multiple-metrics.xml#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> View Multiple Metrics in a Report </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This [!DNL  Target] release focuses on back-end fixes and includes the following customer-facing enhancements and fixes: (issue numbers in parentheses are for internal Adobe use): 


* Fixed an issue that caused the "Increment Count, Release User &amp;amp; Allow Reentry" setting in Advanced Settings for activities to not function correctly. (TNT-26556) 

* Fixed an issue that prevented Customer Attribute data from being removed from Target after being updated with NULL in the Experience Cloud user interface. (TNT-26462) 



## Target Platform Changes (April 13, 2017) {#section_B59C26405EB7482AA80820D6D39B9C44}



<table id="table_6167ECB7B44F40DCADF299F46F1F795C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> at.js </span> version 0.9.6 is now available. For more information, see <a href="../ov2/c_target-configure-atjs.xml#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Download at.js </a>. </p> <p>The following enhancements and fixes are included in <span class="filepath"> at.js </span> version 0.9.6: </p> <p> 
     <ul id="ul_108DF85393614C69988E299485D338FD"> 
      <li id="li_4117C900982240B5AFFCFE1B2716A443"> <p>Redirect offer support for A4T. After you download and install <span class="filepath"> at.js </span> version 0.9.6, you can use redirect offers in activities that use <span class="keyword"> Adobe Analytics </span> as the Reporting Source for <span class="keyword"> Target </span> (A4T). Besides <span class="filepath"> at.js </span> version 0.9.6, there are other minimum requirements your implementation must meet in order to use redirect offers and A4T. For more information and additional important information you should know, see <a href="../a4t/c_a4t-faq-redirect-offers.xml#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Redirect Offers - A4T FAQ </a>. </p> </li> 
      <li id="li_DA5321D72E81496DB7C49D589E1A59C4"> <p>Prior to <span class="filepath"> at.js </span> 0.9.6, when the Visitor API was present on the page and the <span class="codeph"> visitorApiTimeout </span> setting was too aggressive, Target could run into a situation when no MCID data was sent in the <span class="keyword"> Target </span> request. This could lead to issues like unstitched hits in <span class="keyword"> Analytics </span> when using A4T. </p> <p>This behavior has been changed in <span class="filepath"> at.js </span> 0.9.6, even if the <span class="codeph"> visitorApiTimeout </span> is set to say 1 ms, Target will try to collect SDID, tracking servers, and customer IDs data and send those in the Target request. </p> </li> 
      <li id="li_B11CE11D9A594CB1ABB85BD0D93C4A15"> <p>Added the <span class="codeph"> selectorsPollingTimeout </span> setting. For more information, see <a href="../ov2/cmp_at.js_Functions.xml#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_D6F862099A374FE394F4DA3520A1BBF0"> <p>The format of the response from <span class="codeph"> getOffer() </span> has been changed. For more information, see <a href="../ov2/cmp_at.js_Functions.xml#reference_C81525D1598A4A1199740DCAB81A7FDF" format="dita" scope="local"> adobe.target.getOffer(options) </a>. </p> </li> 
      <li id="li_80166567ED8945ECB37FEEE2C5F06ACE"> <p>Console logging has been added for unsupported <span class="codeph"> &amp;lt;!DOCTYPE&amp;gt; </span> declarations. </p> </li> 
      <li id="li_02904EBAE8D3400092B762F0B28B0C86"> <p>Fixed an issue where <span class="keyword"> Target Classic </span> plugins weren’t being applied correctly when multiple default offers were delivered to a single mbox. (TGT-22664) For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Using_Plug-Ins.html" format="html" scope="external"> Plug-Ins </a> in the Adobe Target Classic documentation. </p> </li> 
      <li id="li_7016022D9DDE4529B77984F195825AB7"> <p>Improved cookie-setting for two letter top-level-domains (TLDs) to ensure that the mbox cookie is set correctly for these domains (for example, <span class="filepath"> test.no </span>, <span class="filepath"> autodrives.ca </span>, and so forth). </p> </li> 
      <li id="li_3B1F618DEC744056B5BB172C4DBB359A"> <p>The algorithm for extracting the top-level domain that should be used when saving cookies has changed in <span class="codeph"> at.js </span> version 0.9.6. Because of this change, cookies cannot be saved to addresses that use IP. Most of the time, IP addresses are used for testing purposes, but as workarounds you can use DNS entries or adjust the hosts file on a local box. </p> </li> 
      <li id="li_A52181499E63402DB4E16E33E36A9400"> <p>Fixed move and rearrange actions handling when properties are string values instead of integers. </p> </li> 
     </ul> </p> <p>For information about this and previous versions of <span class="filepath"> at.js </span>, see <a href="../ov2/r_target-atjs-versions.xml#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.3.1 (March 30, 2017 - Updated April 13, 2017) {#section_5C13660A8AA34F35A9CBEFEEC88738D0}

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
   <td colname="col1"> <p>Analytics for Target (A4T) </p> <p>Redirect Offers </p> </td> 
   <td colname="col2"> <p><b>Updated April 13, 2017.</b> </p> <p>You can now use redirect offers in activities that use <span class="keyword"> Analytics </span> as the reporting source. </p> <p>Your implementation must meet the following minimum requirements: </p> <p conref="../reuse/RedirectWithA4TReqs.xml#ditacomponent_1F888AE8E57E447CBA11C5F0407E2DB0/p_A816444144144867B5266CA4D5F69F4A"> </p> <p>These libraries must be included on both the page with the redirect offer and the page to which the visitor is redirected. As a part of this change, new URL parameters will automatically be added to your redirect URLs if the Visitor Id service is implemented on your site, regardless of whether or not you are using Analytics as the reporting source for that activity. </p> <p>For more information, see <a href="../a4t/c_a4t-faq-redirect-offers.xml#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Redirect Offers - A4T FAQ </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>The following enhancements have been made to audience targeting: </p> <p> 
     <ul id="ul_C920198404654C97A33190A29ACA6990"> 
      <li id="li_DB52EF909C9640649981940460CDF2B5"> <p><b>Week and Day Parting: </b>You can set <span class="wintitle"> Week and Day Parting </span> options to create recurring patterns for audience targeting. </p> <p>For more information, see <a href="c_time-frame.xml#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. </p> </li> 
      <li id="li_2541A6EF2D604CE098012A16909C237E"> <p><b> Exclusions in Combined Audiences: </b>You can now add exclusion rules and exclude audiences when combining multiple audiences. </p> <p>For more information, see <a href="c_combining-multiple-audiences.xml#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Combining Multiple Audiences </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p><b>Dynamic Promotions: </b>Target Recommendations now supports dynamic matches for promotions. </p> <p>For more information, see <a href="../recs/c_use-dynamic-and-static-inclusion-rules.xml#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


>[!NOTE]
>
>The ability to view multiple metrics in a report, included in the Target 17.3.1 release (March 30, 2017) has been removed due to unexpected behavior. This feature will be available again in an upcoming release.



This [!DNL  Target] release includes the following enhancements and fixes: : 


* The [!DNL  Target] user interface has been updated to support redirect offers in activities that use [!UICONTROL  Analytics for Target] (A4T) as the reporting source. This functionality will require [!DNL  at.js] 0.9.6, which will be available soon. 

* The [!DNL  Target] user interface was updated in some places: 

    * In reports and activities, some options ( [!UICONTROL  Edit], [!UICONTROL  Share to Feed], [!UICONTROL  View Experience URLs], etc.) are now accessed by clicking the [!UICONTROL  More Options] icon (  ![](../assets/icon_more_options.png) ). 

    * In the [!UICONTROL  Offers] library, offers now display in a list rather as cards. Other minor UI changes were made throughout the [!UICONTROL  Offers] library UI. 


* Significantly improved performance on the [!UICONTROL  Activity] and [!UICONTROL  Audience] lists. Also, load times for search results return significantly faster. 

* "Views" is now "Visits" in the [!UICONTROL  Offer Level Report] for [!UICONTROL  Automated Personalization] reports. 

* [!DNL  Target] now supports switching of environments (host groups) for [!UICONTROL  Automated Personalization] activities. 

* [!UICONTROL  Automated Personalization] activities now support host groups. 



## Target Standard/Premium 17.2.1 (February 21, 2017) {#section_FC6412353DE64E848FFD5E8EFF72C7C7}


>[!NOTE]
>
>[!DNL  Adobe Experience Manager] 6.2 with FP-11577 (or later) now supports [!DNL  at.js] implementations with its [!UICONTROL  Adobe Target Cloud Services] integration. For more information, see [ Feature Packs ](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) and [ Integrating with Adobe Target ](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in the *Adobe Experience Manager 6.2* documentation. 



This [!DNL  Target] release focuses on usability and performance improvements and includes the following enhancements and fixes (issue numbers in parentheses are for internal Adobe use): 


* Added additional items to the Help menu that can be accessed from the top right corner of the [!DNL  Target] user interface. New options include: "Blogs" and "Videos." The "Adobe Experience Cloud Status" option is now "Adobe Target Standard/Premium Status." (TGT-22629) 

* When deleting an audience, [!DNL  Target] displays a list of activities that reference that audience. Users can click each activity in the list to display its [!UICONTROL  Overview] page. (TGT-17997) 

* Improved ` user.activeCampaigns` to return the campaign ID for all campaigns/activities that the user is in, even if he or she has not interacted with the campaign/activity in the current session. (TNT-26237) 

* The [!UICONTROL  Create Activity] button on the [!UICONTROL  Activities] page is now active before all activity names are loaded in the list. This improvement lets users create new activities faster, especially when the account has many configured activities. (TGT-21470) 

* Made enhancements to the Enhanced Experience Composer (EEC) to improve loading time for websites running HTTPS accessed via proxy. Target no longer fetches static resources via proxy. (TGT-21793) 

* Made performance improvements on the [!UICONTROL  Goals &amp;amp; Settings] page, especially load time when many metrics are defined for an activity. (TGT-21654) 

* Added a tool tip on the [!UICONTROL  Goals &amp;amp; Settings] page of all activities using [!UICONTROL  Analytics for Target] (A4T) reporting informing users that a tracking server is not required if the activity's pages have ` at.js` (version 0.9.1 or later) or ` mbox.js` (version 61 or later) loaded. (TGT-22607) 

* Metric names now display on the [!UICONTROL  Goals &amp;amp; Settings] page without users needing to expand each metric to view the entire metric name. This improvement lets users edit metrics quicker and more efficiently. (TGT-21276) 

* You can now apply [!DNL  Recommendations] inclusion rules to custom criteria (uploaded via CSV), just like any other criteria. (TGT-21896) 

* Improved the user interface and usability of the [!UICONTROL  Offers] page, especially when creating or managing folders and creating offers. (TGT-22509 and TGT-22187) 

* Improved the user experience in the [!UICONTROL  Visual Experience Composer] (VEC) when selecting items to hide. 
  (TGT-22224)
* Improved the user experience when creating activities using the [!UICONTROL  Form-Based Experience Composer]. When choosing an mbox location, the validation border remains highlighted after clicking [!UICONTROL  Next]. (TGT-22221) 

* Enhanced the downloaded reports to differentiate between active and deleted offers. The following text is appended to deleted offers: [Deleted]. (TGT-22449) 

* Fixed an issue that prevented older assets from displaying in the infinitely scrollable asset list in the Experience Cloud Assets core service user interface. (TGT-19733) 

* Fixed an issue where the extreme order setting was not honored in downloaded CSV reports. (TGT-21871) 

* Fixed an issue where extreme orders were not marked correctly in the downloaded [!UICONTROL  Order Details]CSV report. (TGT-22500) 

* Fixed an issue that caused the incorrect order time to display in the downloaded [!UICONTROL  Campaign Audit] CSV report, even though the report displayed the correct order date. (TNT-26469) 

* Fixed an issue that prevented the [!UICONTROL  Disable JavaScript] option from working correctly on multi-page activities. (TGT-15130) 

* If you use the Form-Based Experience Composer with an mbox other than the auto-created global mbox ( ` target-global-mbox`), and then choose an engagement metric as a success metric, the metric increments only on pages that have the mbox used in the activity. As an example, if your mbox is ` homepage_mbox`, the [!UICONTROL  Pages Per Visit] metric is the number of hits to the ` homepage_mbox` during that visit. 

  If this is not what you want, you can add another location to the activity and assign the global mbox to that location and give it default content. This workaround connects the global mbox to the activity and allows Target to count the metric for reporting. 



## Target Platform Changes (January 18, 2017) {#section_EA41802B2B24426FBA88D25E17DBE360}



<table id="table_3A2CD47252894F119B0E60BF6A9285B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> version 0.9.4 </p> </td> 
   <td colname="col2"> <p>January 18, 2017 </p> <p> <span class="codeph"> at.js </span> version 0.9.4 contains the following changes: </p> <p> 
     <ul id="ul_8F149C28E2D946B9888B4D2F45167C3C"> 
      <li id="li_93E866BBFE374E93BCDB65BCFAC33B62"> <p> mbox names can now contain special characters, including ampersands ( &amp; ), to be consistent with naming requirements for mbox names using <span class="codeph"> mbox.js </span>. (TNT-26144) </p> <p>For more information, see <a href="../ov2/c_target-atjs-advanced-settings.xml#concept_2FA0456607D04F82B0539C5BF5309812" format="dita" scope="local"> Configure at.js </a>. </p> </li> 
      <li id="li_99309046030B4D93B59113C01A8789DA"> <p>Added <span class="codeph"> secureOnly </span> setting that indicates whether <span class="codeph"> at.js </span> should use HTTPS only or be allowed to switch between HTTP and HTTPS based on the page protocol. This is an advanced setting that defaults to False and can be overridden via <span class="codeph"> targetGlobalSettings </span>. (TNT-26183) </p> <p>For more information, see <a href="../ov2/cmp_at.js_Functions.xml#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_D84D578C43A24D4896795999F841CEB8"> <p>The <span class="wintitle"> Legacy Browser Support </span> option is available in <span class="codeph"> at.js </span> version 0.9.3 and earlier. This option was removed in <span class="codeph"> at.js </span> version 0.9.4. </p> <p>For more information, see <a href="../ov2/c_target-atjs-advanced-settings.xml#concept_2FA0456607D04F82B0539C5BF5309812" format="dita" scope="local"> Configure at.js </a>. </p> </li> 
     </ul> </p> <p>For detailed information about the changes in each version of <span class="codeph"> at.js </span>, see <a href="https://marketing.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-versions.html" format="html" scope="external"> at.js Version Details </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.js </span> version 62 </p> </td> 
   <td colname="col2"> <p>January 18, 2017 </p> <p> <span class="codeph"> mbox.js </span> version 62 contains the following enhancement and fixes: </p> <p> 
     <ul id="ul_1D4351AEB0D74FE4B09196113A4672C1"> 
      <li id="li_653D9C605A0B447AB1FFEE5D22D3AD05"> <p>Fixed flicker issues in redirect activities when viewed in Google Chrome browsers. (TNT-24928) </p> </li> 
      <li id="li_2196D7CD9B144C0A96AE8B8D13976C69"> <p>Added <span class="codeph"> secureOnly </span> setting that indicates whether <span class="codeph"> mbox.js </span> should use HTTPS only or be allowed to switch between HTTP and HTTPS based on the page protocol. This is an advanced setting that defaults to False. (TNT-26183) </p> <p>For more information, see <a href="../ov/r_advanced_mboxjs_settings.xml#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C" format="dita" scope="local"> Configure mbox.js </a>. </p> </li> 
     </ul> </p> <p>For detailed information about the changes in each version of <span class="codeph"> mbox.js </span>, see <a href="https://marketing.adobe.com/resources/help/en_US/target/ov/r_mboxjs_change_log.html" format="html" scope="external"> mbox.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.1.1 (January 19, 2017) {#section_88AFA2F54CF24DF7822CFEBB07DFABE2}

This release includes the following features and enhancements: 



<table id="table_4F7D4A71F5DF4E8782C7DBEEEF24AD04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p>Content/Offers </p> </td> 
   <td colname="col2"> <p>The following enhancements are now available for offers: </p> <p> 
     <ul id="ul_7D8E81443E0F48B6A0C1D1DF6F27D292"> 
      <li id="li_EA529EF4EBC2416E9D3B9E7251E7AAAB"> <p>The Content page has been renamed to Offers. In addition, there are now two tabs along the right side to separate code offers from image offers. </p> <p>If you had code and images in the same folder before this release, Target will split them into two duplicate folders. </p> </li> 
      <li id="li_9574FA6BDCFB4BAB938273BF7F4B21C8"> <p>Offers created via Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services (AMS), and APIs are now visible in the Target Standard/Premium user interface. Offers created in Target Classic are editable in Target Standard/Premium. (TGT-15738) </p> <p> Offers updated in the last two years using these methods will be visible in Target Standard/Premium (i.e. January 2015 and beyond). </p> </li> 
      <li id="li_CAD67C9EBB564525ABD2269D918275F8"> <p>You can now filter offers by source and type. </p> </li> 
     </ul> </p> <p>For more information, see <a href="c_manage_content.xml#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>The following enhancement has been made to geo-location targeting: </p> <p> 
     <ul id="ul_DD8B50F980B8447A8C37EA96530D8949"> 
      <li id="li_348E04AB29B14E6F83E3A7E7BF7D75B8"> <p>You can now use <span class="codeph"> profile.geolocation </span> values directly as tokens in offers, plugins, and so forth. (TNT-25967) </p> </li> 
     </ul> </p> <p>For more information, see <a href="c_geo.xml#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="2"> <p>Reporting </p> <p> <p>Note:  These enhancements do not apply to Analytics for Target (A4T) reports. </p> </p> </td> 
   <td colname="col2"> <p>The following reporting enhancements are now available for Target reports. </p> <p> 
     <ul id="ul_ACFCA821B120419EA252EF5031309D52"> 
      <li id="li_0B634602BB044AEDB26DAF78189AB833"> <p>The user interface for reports has been redesigned. </p> </li> 
      <li id="li_309435D10AE84E8795C4CCC1F36747F7"> <p>Target reports now have an option to reset reporting data to remove old data. (TGT-5933) </p> </li> 
      <li id="li_9D30BFCC4CD6461B9DDCD5797A5E2B3A"> <p>The counting methodology options for reporting includes Visitors (the default), Visits, and Activity Impressions. (TGT-10002) </p> </li> 
     </ul> </p> <p>For more information, see <a href="c_report-settings.xml#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Report Settings </a> and <a href="c_counting_methodology.xml#concept_EC19BC897D66411BABAF2FA27BCE89AA" format="dita" scope="local"> Counting Methodology </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>The following reporting enhancements are now available for downloadable CSV reports: </p> <p> 
     <ul id="ul_18B0636A41B94F9F903ABFE3E13285DA"> 
      <li id="li_2422075AA0A34F868809C5D580FC5D4B"> <p>The offer-level CSV report now has additional details about each offer. (TGT-18995) </p> </li> 
      <li id="li_659D126E846348D4BE4544962F41539F"> <p>Downloaded offer-level CSV files now always include data from control and targeted segments for <span class="wintitle"> Automated Personalization </span> reports. (TGT-22000) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2" class="premium"> <p>The following reporting enhancements are now available for Automated Personalization (AP) reports. </p> <p> 
     <ul id="ul_5743684487CD4905BA998C298FD423D7"> 
      <li id="li_EB48BA21E00C4878B4408D24DD23BA9C"> <p>Improved reporting load time for Automated Personalization activities. </p> </li> 
      <li id="li_B8ECCE250A674B83A66705AD5C45B9C3"> <p>The confidence interval for continuous variables (Revenue and Engagement metric types) is now displayed in Automated Personalization (AP) summary reports. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activities </p> </td> 
   <td colname="col2"> <p>The following enhancements are now available for Target activities: </p> <p> 
     <ul id="ul_436556860E6C4AEEB35411A02E78A199"> 
      <li id="li_5CC3B995D0AF4B658B3D6C3F6895AA41"> <p>Activities created in <span class="keyword"> Adobe Mobile Services </span> now display within the <span class="keyword"> Target Standard/Premium </span> user interface. (TGT-10806) </p> <p>For more information, see <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </li> 
      <li id="li_684F9FC5CF414F4A892E6495352B5939"> <p>When creating multivariate tests, you can now exclude more than 10 percent of experiences from the test, provided you acknowledge the warning that you must then use offline reporting for analysis. (TGT-21719) </p> <p>For more information, see <a href="../mvt/t_preview_experiences.xml#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> Preview Experiences for a Multivariate Test </a>. </p> </li> 
      <li id="li_B2FC7414C76848B39AD6EA20EE483F06"> <p>The Campaign ID is now visible on each activity's Overview page. This is useful for API and troubleshooting operations. (TGT-20928) </p> </li> 
      <li id="li_5A9880AFE5FB46168D92255AA088B854"> <p>The design for the Collisions and Change Log pages have been improved. </p> </li> 
      <li id="li_1489EA6C30C94B2AB394189E5FAFF6F6"> <p>The maximum allowed length of anonymous offer names in Automated Personalization (AP) activities has been increased from 30 to 250 characters. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>The following enhancements are now available for audiences: </p> <p> 
     <ul id="ul_F1D1F97266134D4ABE627CF2DCE2C6D4"> 
      <li id="li_99A611FCC1254D229D79B8FD075B952A"> <p> <span class="wintitle"> Device Marketing Name </span> is now available as a built-in option from the drop-down list when creating audiences targeting mobile devices. </p> <p>This change lets you easily pick a device model name rather than searching for the appropriate device model number. For example, the Galaxy S7's marketing device name is "Samsung Galaxy S7 Edge," while the device model is "SM-G9350." (TGT-18393) </p> <p>For more information, see <a href="c_mobile.xml#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobile </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p>The following enhancements have been made to Recommendations: </p> <p> 
     <ul id="ul_9D3644890C0C472D8B485DE9A52898B3"> 
      <li id="li_1E5662348F6E4ABDB2B74FE3326F2FD3"> <p>The Backup Algorithm result line is now included in Top Viewed and Top Bought CSV downloads. The backup Recommendation starts with "*," </p> </li> 
      <li id="li_91DFD809378D4C20918F8F875747CE07"> <p>Additional statuses let you know the progress of your Recommendation feeds. </p> <p>For more information, see <a href="../recs/c_feeds.xml#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> Feeds </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhanced Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>Updated the IP addresses for the Enhanced Visual Experience Composer (VEC). </p> <p>If you whitelist IP addresses used for the VEC, add the new IP addresses. </p> <p>For more information, see <a href="r_troubleshoot_composer.xml#reference_77743144F10143A3A89D56E116D296E4" format="dita" scope="local"> Troubleshooting the Visual Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

