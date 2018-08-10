---
description: null
seo-description: null
seo-title: 2014 Releases
title: 2014 Releases
uuid: f6b08827-f7a3-4a04-88a0-5fd4c3bf9318
index: y
internal: n
snippet: y
translate: y
---

# 2014 Releases


## Adobe Target 14.10.2 (November 6, 2014) {#section_E7036B45DF974FB7B81E67261357A01B}

This minor release is focused mainly on server stability. There are no new features as part of this patch. 

## Adobe Target 14.10.1 (October 30, 2014) {#section_D557CB331A004155B91CFE5B197076F3}

This release includes the following features and enhancements: 



|  Feature  | Description  |
|---|---|
|  Redirect offers  | Redirect an experience to a different URL so you can test one page against another page. See [ Create a Redirect Offer ](t_redirect_offer.md#task_9578678D42784F5EB9638F8AC8C911FA).  |
|  Apply targeting on success metrics  | Choose a saved audience to apply on a success metric. With this feature you can limit what actions count for a particular success event. An example might be limiting conversions to when the order is more than $0, or only counting success when a user views a particular page in the same session as entering the activity.  |
|  Automated Personalization: Select and report against RPV/AOV metrics  | You can now select the RPV and AOV metrics in the Automated Personalization experience creation flow. For more information about creating n Automated Personalization activity, see [ Automated Personalization ](t_automated_personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).  |
|  Improved permission controls  | Only users with sufficient permissions can edit audiences.  |

This release includes the following enhancements: 


*
*


## Adobe Target 14.9.1 (September 19, 2014) {#section_681F27FBFDFF46FE8A1A8E24A50A26F4}

This release includes the following features and enhancements: 

|  Feature/Enhancement  | Description  |
|---|---|
|   | Added the ability to edit and inject custom JavaScript in the experience editor when you choose ** [!UICONTROL  Edit HTML] ** from the actions menu.  |
|   | Audiences are automatically imported in the background when a user opens the audience list and the imported audiences are more than 10 minutes old.  |
|  Increased size of HTML offers than can be synced to [!DNL  Target Classic]  | Increased the former 64KB limit to 256KB.  |

This release includes the following fixes: 


*
*
*
*


## Adobe Target 14.8.1 (August 21, 2014) {#section_02D0DFA7A8D145B2B3FEFF83591243E1}

This release includes the following new features and enhancements: 

|  Feature/Enhancement  | Description  |
|---|---|
|  Enhanced syncing of HTML offers with [!DNL  Target Classic] by increasing the character limit  | Raised the character limit of an HTML offer created under Content to align with the 256 KB limit of HTML offers synced to [!DNL  Target Classic].  |
|   | The Experience Editor displays a message when DOM structure changes on the page breaks the selectors.  |

**Fixes** 

*
* Fixed a problem where selected links were not marked as selected when users clicked ** [!UICONTROL  Select Link] ** on the [!UICONTROL  Goals and Settings] page.
* Fixed an error that prevented a new activity from appearing in the [!UICONTROL  Activity List] after being activated on the [!UICONTROL  Overview] page.
*
*
*
*
* Fixed a click-track conversion error that negated ` target="_blank" functions.`
*

## Adobe Target 14.6.1 (June 25, 2014) {#section_A520F01EEE0A4C2CBB3F2A37E6DD6F83}

This release includes the following new features: 


>[!NOTE]
>
>Some features in this release are available only as part of the [!DNL  Target Premium] solution. 



<table id="table_A2A978B157D54E17BD7366ADC04C8FC9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="keyword"> Automated Personalization (Target Premium) </span> </td> 
   <td colname="col2"> <p> <span class="keyword"> Automated Personalization </span> provides advanced machine learning algorithms to drive personalized experiences and improved conversion rates for digital experiences. </p> <p> <p>Note:  <span class="keyword"> Automated Personalization </span> is available as part of the <span class="keyword"> Target Premium </span> solution. It is not included with <span class="keyword"> Target Standard </span> without a <span class="keyword"> Target Premium </span> license. If you have a <span class="keyword"> Target Standard </span> or <span class="keyword"> Target Premium </span> license, use the <span class="keyword"> Target </span> card in the Adobe Marketing Cloud. </p> </p> <p>Implement one file on your site and to enable the ability to point and click on any content and then visually create and select additional content options for that area. Then, the modeling system automatically determines which piece of content to deliver to each individual based on all behavioral data the system has about the visitor. This ability provides a personalized experience for each visitor. The marketer does not need to run a test, then analyze the results, then deliver a winner before realizing the lift found from optimization. </p> <p> <span class="keyword"> Automated Personalization </span> provides: </p> 
    <ul id="ul_9EF654B10FFA46169EE2E033683BA82E"> 
     <li id="li_8D201BF8F37B4B2489D039A0340E065E">Two machine-learning algorithms: 
      <ul id="ul_E1DF69071C9047EEA692B5EF01176E4B"> 
       <li id="li_1F4ED87AB6D044C1BE04D0360F42D56F"> <span class="keyword"> Random Forest </span> </li> 
       <li id="li_BE6388BA88684501B741713CECF5AE91"> <span class="keyword"> Residual Variance Model </span> </li> 
      </ul> </li> 
     <li id="li_36E18493A95B4C96BFA3133CDFD8826A">Single line of code implementation with WYSIWYG content editing </li> 
     <li id="li_79B1878FA64A40E88A973C57C39FC5FF">Primary goal for the activity currently uses the Conversion metric. Revenue and engagement are available as additional metrics. </li> 
     <li id="li_FE94A79767EF4534BD02B2AFD7E27E1B">Connection to the <span class="keyword"> Master Marketing Profile </span> for seamless collection of advance visitor behavioral data <p>For information about using the <span class="keyword"> Master Marketing Profile </span> with <span class="keyword"> Target </span>, see <a href="https://marketing.adobe.com/resources/help/en_US/target/mmp/c_mmp.html" format="http" scope="external"> Master Marketing Profile and Real-Time Audiences </a> in the <span class="keyword"> Adobe Target </span> Integration guide. </p> </li> 
    </ul> <p>See <a href="t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multiple activities on one page </td> 
   <td colname="col2"> <p>Content from multiple Target Standard activities can be delivered on one page from one <span class="keyword"> Target </span> server call. </p> <p> <p>Note:  This does not affect the Target Classic priorities evaluation. </p> </p> <p>To learn more about the Target priorities decision process, refer to the <a href="https://marketing.adobe.com/resources/help/en_US/target/target/c_priority.html" format="http" scope="external"> Target Standard help </a>. </p> <p>For information about how Target determines which experience to show when multiple activities target the same location on a page, see <a href="c_activities.xml#concept_1780C11FEA57440499F0047DD6900E0F" format="dita" scope="local"> Priority </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes** 

* Fixed an issue where some shared audiences that have been deleted still show in the [!UICONTROL  Audiences] list.
* Fixed an error where an unexpected [!UICONTROL  Save] dialog box appeared in Internet Explorer 10.
*
*
* Fixed an issue that prevented the metrics lists in [!DNL  Target] and [!DNL  Analytics] from matching.
* Fixed an issue that allowed users to specify their global mbox to be an mbox that is used to deliver HTML content by [!DNL  Target Standard]. Using the global mbox in that way negatively affects content delivery and [!DNL  Target Classic]'s ability to deliver multiple campaigns to a single page in a single request.
*

## Adobe Target Standard 14.5 (May 28, 2014) {#section_530EAB9376414D4989CA0740361DDCC2}

This release includes the following bug fixes: 

*

## Adobe Target Standard 1.7 (April 28, 2014) {#section_2C2B9B6299ED4F48A3B983AB015F381A}

[ Target Standard 1.7 Release Webinar ](https://my.adobeconnect.com/p1oabaz3cxi/) 

This release includes the following new features

<table id="table_11CD9EE0C9534FF19C9154784C4BFCF0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Adobe Analytics-enhanced reporting for Adobe Target </td> 
   <td colname="col2"> Adobe Analytics customers can select <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/" format="http" scope="external"> Analytics as the default reporting source </a> during the <a href="t_test_ab.xml#task_FE48F7B077C44A5BA015B087428412EF" format="dita" scope="local"> test set-up process </a>. Selecting all success metrics or audiences you want to use to filter your results is no longer required. Within reporting, you can select any success metric or audience segment defined in Analytics and retroactively apply it to your reporting for extensive filtering and drill-down analysis of your optimization results. <p> <p>Note:  To request access to this feature, visit <a href="http://www.adobe.com/go/audiences" format="http" scope="external"> http://www.adobe.com/go/audiences </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Master marketing profile real-time audiences </td> 
   <td colname="col2"> Leverage the <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/" format="http" scope="external"> master marketing profile </a> that unifies visitor IDs and data into a single, actionable profile for use across solutions. A checkbox during the segment creation process in Adobe Analytics allows the segment to be available within the Adobe Target's custom audience library. A segment created in Analytics or Audience Manager can be used to target visitors in Target. <p> <p>Note:  To request access to this feature, visit <a href="http://www.adobe.com/go/audiences" format="http" scope="external"> http://www.adobe.com/go/audiences </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Experience targeting activity type </td> 
   <td colname="col2"> <a href="t_experience_target.xml#task_A53DF336CB9F4D7BB87EF2106099EFC4" format="dita" scope="local"> Target different experiences to different audiences in one activity </a>. <p> <p>Note:  This provides similar functionality to the Landing Page campaign in Target Advanced. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multi-page testing </td> 
   <td colname="col2"> <p> <a href="c_experiences.xml#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Choose to run a test or targeted activity across a set of webpages </a>. You can now deliver tests to every product page, or modify your global nav on every page of the site. Use a simple rule builder to specify what the group of pages should be. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Bug Fixes** 

This release includes the following bug fixes: 


* Fixed an issue that prevented ` target.js` from being compressed by Edge.
*
*
*


**Known Issues** 

This release includes the following known issues. This issue will be fixed in an upcoming update. 


*
*
*
*


## Adobe Target Standard 1.6 (March 17, 2014) {#section_DB1319CDD8944F6FB749E525EB551017}

This release includes the following new features

|  Feature  | Description  |
|---|---|
|   | Target Standard has been localized in French, German, Japanese, and Spanish  |
|   | Target Standard has been improved to make it easier to implement for existing Target Advanced users. The new implementation uses your existing global mboxes to run Adobe Standard activities.  |

**Bug Fixes** 

This release includes the following bug fixes: 


*


**Known Issues** 

This release includes the following known issues. This issue will be fixed in an upcoming update. 


*
*
*
*
*
*
*
*


## Adobe Target Standard 1.5 (February 25, 2014) {#section_5E9E3DDBCB82494AA62A21AC9282063F}

This release includes the following new features

<table id="table_67115780726F48859DC8E46E34567DC3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity collisions </td> 
   <td colname="col2"> <p> Target Standard now provides a list of activity collisions. An activity collision occurs when multiple activities are set up to deliver content to the same page. If an activity collision occurs, you may not see the expected content on your page because you've entered a different activity. </p> <p> All activities on the same URL are listed, regardless of any audience targeting in each activity. </p> <p> If your activity contains collisions, a <span class="wintitle"> Collisions </span> tab is available the on the activity overview page. Open this tab for a list of activities that are colliding. Click an activity in the list to view the overview page for that activity. </p> <p>See <a href="c_experiences.xml#concept_0BC6B929592744DFA7DA01FF4F91052E" format="dita" scope="local"> Activity Collisions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New targeting options: Profile, User </td> 
   <td colname="col2"> You can now target profile and user parameters. See <a href="c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Audiences </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Insert elements </td> 
   <td colname="col2"> <p>You can now add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test. </p> <p>See <a href="c_experiences.xml#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This release includes the following known issues. This issue will be fixed in an upcoming update. 


*
*
*
*


## Adobe Target Standard 1.4 (January 20, 2014) {#section_CD27AEE32B4F40BDAB422711B96739A5}

This release includes the following new features and enhancements: 

<table id="table_9E303FF0CD954795A29369A6D4166DB5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Estimate revenue lift </td> 
   <td colname="col2"> <p>Target can estimate the revenue lift you would attain if all users view the winning experience. </p> <p>This estimate calculates the amount of lift achieved by the winning experience and your total number of visitors over the life of the test, and shows the lift you might achieve if every visitor sees the winning experience, if the trends continue as they have during the test. </p> <p> The accuracy of the estimate depends on a number of factors, including projected figures if current trends continue. These values are estimates based on past performance and should not be used for financial guidance. Future results may vary. </p> <p>See <a href="c_estimating_lift_in_revenue.xml#concept_32F875D8F91349CE86AF391F65BEAEEE" format="dita" scope="local"> Estimating Lift in Revenue </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Undo/Redo </td> 
   <td colname="col2"> <p>You can undo changes you make to your activities during an editing session. You can also redo undone changes. </p> <p>See <a href="c_experiences.xml#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Move element </td> 
   <td colname="col2"> <p>You can move elements on your page. Unlike Rearrange Elements, Move does not shift other elements to make room for the element being moved. Use your arrow keys to fine tune the move. </p> <p>See <a href="c_experiences.xml#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Resize element </td> 
   <td colname="col2"> <p>You can resize an element on your page. When you select Resize, a handle appears in a corner of the element that lets you drag that corner to resize. </p> <p>See <a href="c_experiences.xml#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target a location when setting up an audience </td> 
   <td colname="col2"> <p>When creating an audience, you can select a location (mbox) and specify parameters for that location. </p> <p>See <a href="c_audiences.xml#task_1D507519D3AD4390B507F188BD294DC1" format="dita" scope="local"> Creating a New Audience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Preview links (Enhancement) </td> 
   <td colname="col2"> <p>Preview links work as expected. </p> </td> 
  </tr> 
 </tbody> 
</table>

This release includes the following fixes: 


* Fixed issues that prevented preview links from displaying as expected.


This release includes the following known issues. These issues will be fixed in an upcoming update. 


*
*
*
*


## Adobe Target Standard 1.3 (November 19, 2013) {#section_D633ACA56FA941648219EB3748D814EC}

This release includes the following new features and enhancements: 

|  Feature  | Description  |
|---|---|
|  Geo-targeting  | Target on Country, State, City, Zip code, or DMA.  |
|  Use the Visual Experience Composer to rearrange elements.  | You can rearrange child elements inside their parent element using the Visual Experience Composer.  |
|  Preview experiences directly on your site.  | Once you save an activity, you can preview it directly on your site, even if the activity is not live. This allows you to see how it will appear, without serving it through an iFrame. You can copy links to each test experience to view those experiences in your browser or to send them to your team members for them to view. People who view these pages will not be counted in the reports.  |

This release includes the following fixes: 


*
*


This release includes the following known issues. These issues will be fixed in an upcoming update. 


*
*
*
* Users cannot select the ** [!UICONTROL  Remove] ** action for content that is wrapped in an mbox.


## Adobe Target Standard 1.2 (Oct. 31, 2013) {#section_420B5E910D7341AA8DB059C8E1071D53}

There are four known issues with this release. These issues will be fixed in an upcoming update. 


*
*
*
*


This release includes the following fixes and enhancements: 


*
* Fixed an issue where [!DNL  target.js] moves other scripts out of the ` &amp;lt;head&amp;gt;` section of a page.
*
*
*
*
*
*
* Fixed an issue where an [!DNL  mbox.js] file downloaded from Target Standard is named [!DNL  mboxEditor.at.js].
*


## Adobe Target Standard 1.1 (Oct. 18, 2013) {#section_79FA6A61D2284D41A34F00014A342F07}

This release includes the following feature: 



|  Feature  | Description  |
|---|---|
|  [!DNL  mbox.js] download from within Target Standard  | The [!DNL  mbox.js] file can now be downloaded directly from ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] ** in the Target Standard interface. Previously, the file had to be downloaded from within Target Advanced or be supplied by your account representative or consultant.  |

This release includes the following fixes and enhancements: 


*
*
*
*
*
*
*
*
*
*
*
*
*
*
*


## Adobe Target Standard 1.0 {#section_ED95CF049DD347E4A36FA46406F2823F}

This is the first release of Target Standard. 
