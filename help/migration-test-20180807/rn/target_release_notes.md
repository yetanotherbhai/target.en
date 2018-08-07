---
description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
keywords: release notes
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for the latest or upcoming Target releases.
seo-title: Target Releases  Current
solution: Target
title: Target Releases  Current
topic: Standard
uuid: 855ad82e-7029-4053-bcd1-93f4f6251d4b
index: y
internal: n
snippet: y
translate: y
---

# Target Releases: Current


<a id="section_209FD0D5FA5B4EC2AEABB2CC7901612F"></a>

**Last Updated: November 8, 2017** 

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change.




<table id="table_1DAD8293D4A447D9932083FB9488EAA2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>On November 14, 2017, Target Classic will be decommissioned. For everything you need to know about making the move from Target Classic to the new Adobe Target Standard/Premium, see <a href="https://marketing.adobe.com/resources/help/en_US/target/ov/c_target-transition-classic-to-standard.html" format="html" scope="external">Transitioning from Target Classic to Target Standard Premium</a>. For information about Target Classic APIs, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_target-api-documentation.html" format="html" scope="external">Transitioning from Target Legacy APIs to Adobe I/O</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This section contains the following information:

* [Target Platform (November 8, 2017)](target_release_notes.md#section_3A2216543B064D6F82EC03E1F8AEC74D)
* [Target Standard/Premium 17.11.1 (November 8, 2017)](target_release_notes.md#section_324A9B1DA0B14F5999FEE41F15B13A44)
* [Target Standard/Premium 17.10.1 (October 26, 2017)](target_release_notes.md#section_ECC5DD8B6ED443788B46F53E25FC896E)
* [Target Platform Changes (September 27, 2017 &amp; October 13, 2017)](target_release_notes.md#section_B59C26405EB7482AA80820D6D39B9C44)
* [Product Documentation for Target Capabilities](target_release_notes.md#section_4CA76C0E8612402FAE0922103F05ACE8)
* [Prerelease Information](target_release_notes.md#section_7B9D4AAFC6A74388B9D7DEF0658D8B63)


## Target Platform (November 8, 2017) {#section_3A2216543B064D6F82EC03E1F8AEC74D}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parenthesis are for internal Adobe use.




<table id="table_872FE2BE61CC4A5CA369D9A6C730686E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Feature</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1" morerows="1"> <p>at.js</p> </td> 
   <td colname="col2"> <p>at.js version 1.2.2 is now available. For more information, see <a href="../ov2/c_target-configure-atjs.xml#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local">Download at.js</a>. </p> <p> 
     <ul id="ul_3C4C9385A0F3489AA2137A2C88AE93CF"> 
      <li id="li_E658799D930547E6901ACFBF7C541F1F"> <p>Fixed an issue that returned a JavaScript error when the Target library loaded on a page using QUIRKS mode. (TNT-28312)</p> </li> 
      <li id="li_050620115ED84CBDA736D94E9AAC6550"> <p>Fixed an issue that caused Target click tracking to break Analytics data collection calls. (TNT-28261)</p> </li> 
      <li id="li_97BC1B7295364ACDAD3FB07005ED592F"> <p>Fixed an issue that caused <span class="codeph">getOffer() params</span> to fail when<span class="codeph">targetPageParams()</span> returns an empty string. (TNT-28359) </p> </li> 
      <li id="li_B542D4A4E37141BA8BE79D416E1B58DB"> <p>Fixed an issue with session ID generation when using x-only. (TNT-28361)</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>The default timeout for at.js is changed from 15 seconds to 5 seconds.</p> <p>If your current setting was 15 seconds, it will be updated to the new default of 5 seconds. If you previously changed it to something different, your setting will not be affected.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mbox.js</p> </td> 
   <td colname="col2"> <p>The default timeout for mbox.js changed from 15 seconds to 5 seconds.</p> <p>If your current setting was 15 seconds, it will be updated to the new default of 5 seconds. If you previously changed it to something different, your setting will not be affected.</p> </td> 
  </tr> 
 </tbody> 
</table>


## at.js Version 1.2.2 {#section_4E96D13F2DFE4F1F81A1089877D53649}

`at.js` version 1.2.2 is now available. 

* Fixed an issue that returned a JavaScript error when the Target library loaded on a page using QUIRKS mode. (TNT-28312)

* Fixed an issue that caused Target click tracking to break Analytics data collection calls. (TNT-28261)

* Fixed an issue that caused `getOffer() params` to fail when `targetPageParams()` returns an empty string. (TNT-28359) 

* Fixed an issue with session ID generation when using x-only. (TNT-28361)



## Target Standard/Premium 17.11.1 (November 8, 2017) {#section_324A9B1DA0B14F5999FEE41F15B13A44}

This release includes the following features and enhancements (issue numbers in parentheses are for internal Adobe use):


<table id="table_6ADDF3552AD04666B76F2D3F457BB042"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Feature</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Offers</p> </td> 
   <td colname="col2"> <p>If a user has the "Editor" permission, that user cannot edit an offer referenced to a live or scheduled activity.</p> <p> <p>Note: For Target Premium customers using <a href="https://marketing.adobe.com/resources/help/en_US/target/target/property_channel.html" format="html" scope="external">Enterprise User Permissions</a>, if a user selects the All Workspaces option, Target uses the highest permission of the user across workspaces. If the highest permission is "Editor," Target restricts editing as mentioned above </p>. </p> <p>These restrictions apply to all offers, not just offers created in Target. (TGT-27276)</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Response tokens</p> </td> 
   <td colname="col2"> <p>Added the following built-in parameters:</p> <p> 
     <ul id="ul_17AD5B9788514E9DB14ED435A4224BFE"> 
      <li id="li_334F10A5B7934215B4D37278901BAF96"> <p>profile.tntId</p> </li> 
      <li id="li_AA9B4611035344549CC933FFC499289F"> <p>profile.marketingCloudVisitorId</p> </li> 
      <li id="li_DD751027371D4293BF9DB872278BD1B3"> <p>profile.thirdPartyId</p> </li> 
      <li id="li_B6D983A1B68D49AAA40CB401437676F1"> <p>profile.categoryAffinity</p> </li> 
      <li id="li_F5E86BFD14CA4C198F36F3F9987750F9"> <p>profile.categoryAffinities</p> </li> 
     </ul> </p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_response-tokens.html" format="html" scope="external">Response Tokens</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target Standard/Premium 17.10.1 (October 25, 2017) {#section_ECC5DD8B6ED443788B46F53E25FC896E}

This release includes the following features and enhancements (issue numbers in parentheses are for internal Adobe use):


<table id="table_0A8817F64F434875A485FD671C6988AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Feature</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <!-- <row> <entry colname="col1"> <p>Form-Based Activities </p> </entry> <entry colname="col2"> <p>This release includes a new priority model for activities that use the Form-Based Experience Composer with only a global mbox. Before this release, content from multiple activities was returned to the page and overwrote content from other returned activities. Now, only the top priority activity's content is returned. </p> </entry> </row> --> 
  <tr> 
   <td colname="col1"> <p>Audiences</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6E91AEC68A6E45D8B2907C77E752FEC6"> 
      <li id="li_A5778B528358433DB31D700D8F9BCB79"> <p>You can create activity-only audiences from within the three-step guided workflow when creating an activity. This audience can be used in other places within the same activity, but is not stored in the Audiences Library for use in other activities. (TGT-25474)</p> <p style="text-align: center;"><img href="graphics/adhoc audience.png" id="image_32C7C8B72F51425595A2E266AEFA17E9" /> </p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/creating-activity-only-audience.html" format="html" scope="external">Creating an Activity-Only Audience</a>. </p> </li> 
      <li id="li_691812682A5B42C0941324F2BC7D5740"> <p>For all activities, you can choose a success metric that qualifies the user for the audience. In the past, Target qualified users for an audience when they entered the activity, whereas now you can choose when to evaluate the audience by choosing a success metric. (TGT-15805)</p> <p style="text-align: center;"><img href="graphics/success metric.png" id="image_0CEC6015A2C4429790A063FE54CC1A35" /> </p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_apply-reporting-audience-success-metric.html" format="html" scope="external">Apply a Reporting Audience to a Success Metric</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Auto-Target</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6F89BD36373E47C4B3A6F8584D431D82"> 
      <li id="li_5F7B590AF8F24066ADD270E9F75CB12F"> <p>Auto-Target activities now support segment-level reporting. (TGT-22777)</p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_auto-target-to-optimize.html" format="html" scope="external">Auto-Target For Personalized Experiences</a>. </p> </li> 
      <li id="li_35042E7D6BB04265B42F08A23A774E92"> <p>You can change the Control percentage for Auto-Target activities. (TGT-26467)</p> <p style="text-align: center;"><img href="graphics/auto-target-control-small.png" id="image_3F1F0FF6C55742BABE28CA6850BD015A" /> </p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_auto-target-to-optimize.html" format="html" scope="external">Auto-Target For Personalized Experiences</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_667DDEDDC5284C8393F8BCA5CD9EF12A"> 
      <li id="li_E00DB93297EC4100B46E42D867757DAA"> <p>You can now view offer definition details on a pop-up card in the Offers Library without opening the offer. (TGT-26377)</p> <p style="text-align: center;"><img href="graphics/offer-card.png" id="image_1980AE8E9BED424085CC482C773C20EC" /> </p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_manage_content.html" format="html" scope="external">Offers</a>. </p> </li> 
      <li id="li_F71AC4FDAC0E4BEE81D39490E82686C0"> <p>You can copy and edit offers and folders in the Offer selector while creating an activity. (TGT-26936)</p> <p style="text-align: center;"><img href="graphics/offer-picker.png" id="image_3AE34B8A75A843A6A6A72954A35DA83F" /> </p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_manage_content.html" format="html" scope="external">Offers</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Form-based Experience Composer</p> </td> 
   <td colname="col2"> <p>In the Form-based Experience Composer, Refinements have been replaced with full audience functionality. Refinements for existing activities have been migrated to activity-only audiences. (TGT-13646)</p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/r_release_notes.html" format="html" scope="external">Form-Based Experience Composer</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Response Tokens</p> </td> 
   <td colname="col2"> <p>You can now create response tokens from Target without waiting for them to be created in or imported to Target. Previously, in the Response Token UI, you could see only the tokens created via API. Changes to the feature also help you avoid response tokens duplicates. (TGT-26534)</p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_response-tokens.html" format="html" scope="external">Response Tokens</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes** 
This `Target` release includes the following customer-facing enhancements, fixes, and changes: 

* You can delete imported audiences (Target Classic, Marketing Cloud, etc.) from the Audience Library. Target warns you if you try to delete an audience used for an active activity. (TGT-25171)

* Audiences imported from Target Classic are now labeled as Adobe Target Classic in the Audience Library. In the past, the UI did not differentiate between Target Standard/Premium and Target Classic. (TGT-27093)

* Collections now apply to all criteria (including recently viewed items). (TGT-26646)

* You can filter by Workspace in the Audience Library and Offer Library (applies to Target Premium users with Enterprise User Permissions). (TGT-26813)

* Made improvements in the Reports UI for better scrolling in tables and placements of filter drop-down lists. (TGT-23713 &amp; TGT-26819)



## Target Platform Changes (September 27, 2017 & October 13, 2017) {#section_B59C26405EB7482AA80820D6D39B9C44}



<table id="table_6167ECB7B44F40DCADF299F46F1F795C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Change</th> 
   <th colname="col2" class="entry">Details</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="filepath">at.js</span> </p> </td> 
   <td colname="col2"> <p><b>October 13, 2017</b> </p> <p> <span class="filepath">at.js</span> version 1.2.1 is now available. For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/ov2/c_target-configure-atjs.html" format="html" scope="external">Download at.js</a>. </p> <p> 
     <ul id="ul_14D6BB3B51974789BBFC036A45B7A56B"> 
      <li id="li_AE9826C8FC4A4DF4BE61BB72C2946C93"> <p>Fixed an issue when click tracking on a link with target="_blank" prevented Target from opening the link in a new tab.</p> </li> 
     </ul> </p> <p><b>September 27, 2017</b> </p> <p> <span class="filepath">at.js</span> version 1.2.0 is now available as a maintenance release that contains mostly bug fixes. For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/target/ov2/c_target-configure-atjs.html" format="html" scope="external">Download at.js</a>. </p> <p> 
     <ul id="ul_D11024549C3643C7A756988087498D24"> 
      <li id="li_E1B3994125B64F6AB20B29FE8BCD8459"> <p>Fixed an issue that prevented default actions for click-tracking special cases. (TNT-28089)</p> </li> 
      <li id="li_53806C902AA04B31B59AA87A1E707348"> <p>Fixed an issue when click-tracking on a link with <span class="codeph">target="_blank"</span> that prevented Target from opening the link in a new tab. (TNT-28072) </p> </li> 
      <li id="li_94F5794330D14C71BA07B3F17D0705FD"> <p>IP addresses can be used as the cookie domain. (TNT-28002)</p> </li> 
      <li id="li_7D2A11B17672419583F9632CDA00D28F"> <p>Fixed an issue that caused flicker in redirect offers with a global mbox or other regional mboxes. (TNT-27978)</p> </li> 
      <li id="li_BA27A749A7A242478080F3D8E04148FC"> <p>Fixed an issue in Experience Targeting activity setup failing within the VEC when switching between Browse and Compose. (TNT-27942)</p> </li> 
      <li id="li_FA11ABA5B9CD435080426805C5359A51"> <p>Fixed incorrect handling on flicker style classes for click-track elements. (TNT-27896)</p> </li> 
      <li id="li_E2DFBAE52FCA4996BA083868CBFCCD10"> <p>Fixed an issue that caused global mbox parameters to become mixed up with all mbox parameters. (TNT-27846)</p> </li> 
      <li id="li_B3153BBD66AA4D51AE81EF6C903CF78D"> <p>Made changes to ensure that Handlebars, Mustache, and other client-side templating libraries are properly handled by <span class="filepath">at.js</span>. (TNT-27831) </p> </li> 
      <li id="li_B859939C1B5A4DF78CF8ADF236B88306"> <p>Made changes to ensure that <span class="codeph">sdidParamExpiry</span> is properly initialized and passed to the Visitor API. This is a regression that has been added to <span class="codeph">at.js 1.1.0</span>. Previous <span class="filepath">at.js</span> versions are not affected. This affects only clients using redirect offers and A4T. (TNT-27791) </p> </li> 
      <li id="li_24A748DFB7824AE6AC7331B7EA940BFF"> <p>Made changes to ensure that <span class="codeph">SCRIPT</span> is executed regardless of the type attribute being used. (TNT-27865) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting (XT)</p> </td> 
   <td colname="col2"> <p><b>September 21, 2017</b> </p> <p>With the release on September 21, Target will change the way users are placed into experiences in Experience Targeting (XT) activities (Landing Page campaigns in Target Classic). For all new and existing activities in both Target Standard/Premium and Target Classic, users must meet the experience targeting rules on every impression to continue to see the experience's content and to be counted in reports. Previously, if the user no longer qualified for any experience, the user would continue to see the content from, and be counted in reports for, the last experience they did qualify for.</p> <p>This change will happen automatically as part of the release for all existing activities and for any new activities created post-release. If the previous method (prior to September 21) is desired, you can create audiences using profile scripts so a user only must meet a condition once to continue to fall into that audience in the future. Then, use those audiences for each experience in the activity.</p> </td> 
  </tr> 
 </tbody> 
</table>


## Product Documentation for Target Capabilities {#section_4CA76C0E8612402FAE0922103F05ACE8}

Use the following links to view product documentation for Target capabilities:

* [Target Standard/Premium help](https://marketing.adobe.com/resources/help/en_US/target/)
* [Target Classic help](https://marketing.adobe.com/resources/help/en_US/tnt/help/)
* [Recommendations Classic help](https://marketing.adobe.com/resources/help/en_US/rec/)
* [Search&amp;Promote help](https://marketing.adobe.com/resources/help/en_US/snp/)


## Prerelease Information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements, sign up for the Adobe Priority Product Update:
[https://campaign.adobe.com/webApp/adbePriorityProductSubscribe](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) 
