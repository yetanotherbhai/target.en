---
description: Experience Targeting (XT) delivers content to a specific audience based on a set of marketer-defined rules and criteria.
keywords: experience targeting;xt;metrics;set metrics;goal metric;activity settings;success metric;conversion;revenue;engagement
seo-description: Experience Targeting (XT) delivers content to a specific audience based on a set of marketer-defined rules and criteria.
seo-title: Experience Targeting
solution: Target,standard
subtopic: Multivariate Test
title: Experience Targeting
topic: Standard
uuid: 222ca81b-73f6-4eff-95f5-43d73972baa7
index: y
internal: n
snippet: y
translate: y
---

# Experience Targeting

## Experience Targeting {#task_A53DF336CB9F4D7BB87EF2106099EFC4}Experience Targeting (XT) delivers content to a specific audience based on a set of marketer-defined rules and criteria.Experience Targeting, including [ geotargeting ](c_target_rules.md#concept_5B4D99DE685348FB877929EE0F942670), is valuable for defining rules that target a specific experience or content to a particular audience. Several rules can be defined in an activity to deliver different content variations to different audiences. 

When visitors view your site, Experience Targeting (XT) evaluates them to determine whether they meet the criteria you set. If they meet the criteria, they enter the activity and the experience designed for qualifying audiences is displayed. You can create experiences for multiple audiences within a single activity. 

This video explains the activity types available in Target Standard/Premium. Experience Targeting is discussed beginning at 5:15. 



<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Types </th> 
   <th colname="col3" class="entry"> 9:03 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/vtHg1pPFJp8/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/vtHg1pPFJp8/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F">Describe the types of activities included in Adobe Target </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Select the appropriate activity type to achieve your goals </li> 
      <li id="li_6C4D1871E45D40118D7D9D4DF81547B5">Describe the three-step guided workflow that applies to all activity types </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Create an Experience Targeting Activity {#task_D6B3429AC31549E1A70EDF04B3DDC765}Use the Visual Experience Composer to create an Experience Targeting activity on a Target-enabled page and to modify portions of the page within Target. 
<draft-comment otherprops="merge">
  target/t_xt_create.xml 
</draft-comment>
>1. From the [!UICONTROL  Activities] list, click ** [!UICONTROL  Create Activity] ** > ** [!UICONTROL  Experience Targeting] **.

>       ![](../graphics/xt_select.png) 


>       >[!NOTE]
>       >
>       >The available activity types depend on your Target account. Some activity types might not appear in your list.


>       For information about the activity types, see [ Activities ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). 
>1. Enter your [ activity URL ](t_experience_target.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), then click ** [!UICONTROL  Next] **.

>       ![](../graphics/form_url.png) 

>       If your account is configured with a default URL, that URL appears by default. You can change from the default to another URL. 

>       For troubleshooting information about the VEC, should you have problems, see [ Troubleshooting the Visual Experience Composer ](vec-best-pracitces-and-troubleshooting.md#reference_77743144F10143A3A89D56E116D296E4). 

>       If you prefer to use the form-based Experience Composer, select that option. See [ Form-Based Experience Composer ](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html). 

>       The Visual Experience Composer opens, showing the page specified in the URL. 
>1. Type a name for the activity in the space provided.

>       ![](../graphics/xt_name.png) 

>       The following characters are not allowed in an activity name: 

>       |  Character  | Description  |
>       |---|---|
>       |  /  | Forward slash  |
>       |  ?  | Question mark  |
>       |  #  | Number sign  |
>       |  :  | Colon  |

>1. [ Create any new experiences ](t_experience_target.md#task_454646F2895242D3B92DC395A0CE1A00) by changing the elements on the page.

>       The Experience Composer (see [ Experiences ](c_experiences.md#concept_1D011219034B492BB03C08B3BB80E3F0)) opens the page that is specified in your [ Account Preferences ](https://marketing.adobe.com/resources/help/en_US/target/target/t_account_preferences.html). To display a different page, click the Globe icon and enter the URL in the Select URL box in the Experience Composer and click ** [!UICONTROL  Continue] **. If you entered a URL for a site that does not include the Target Standard JavaScript code, you cannot select page elements. 

>       By default, the Visual Experience Composer does not allow changes to elements containing JavaScript, such as rotating banners. You can select to disable JavaScript if you want to be able to alter those elements using the Visual Experience Composer. 


>       >[!NOTE]
>       >
>       >If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.


>       As you hover the elements on your page, the elements are highlighted. Any highlighted element can be altered using the Experience Composer. 

>       If you created an mbox on the page using Target Classic (formerly Test&amp;amp;Target), that mbox appears as an element that shows the mbox name, and can be modified like any other element. 


>       >[!NOTE]
>       >
>       >If you deliver an image from a source other than your main page (such as an image hosted on akamai.net and delivered on dell.com), then that image does not display in the thumbnail of the page shown in the flow diagram.

>1. Click ** [!UICONTROL  Next] **.

>       The flow diagram opens. 

>       ![](../graphics/xt_diagram.png) 

>       The flow diagram leads you through the steps of choosing the audience for the activity and setting up experiences. 
>1. Mouse over the audience, click the ** [!UICONTROL  Edit] ** icon (  ![](../graphics/icon_more_options.png) ) that displays, click ** [!UICONTROL  Change Audience] **, then select the audience for the first experience in your activity.

>       ![](../graphics/xt_change_audience.png) 

>       The audience library appears. The audience library contains audiences that have previously been defined, including some common audiences that are pre-built as a part of Target. You can either select an audience from the library, or [ create a new audience ](c_audiences.md#concept_65BE870D290E412D8BBF557EEA67C271). To show the same experience to all entrants, choose All Visitors. 


>       >[!NOTE]
>       >
>       >In addition to selecting an existing audience, you can combine multiple audiences to create ad hoc combined audiences rather than creating a new audience. For more information, see[ Combining Multiple Audiences ](c_audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5). 


>       When creating an audience, you can select a location (mbox) and specify parameters for that location. Under Custom Parameters, select the mbox, then specify the desired parameters. 


>       >[!NOTE]
>       >
>       >Audiences are automatically imported in the background when you open the audience list and the imported audiences are more than 10 minutes old.


>       You can click the [!UICONTROL  Edit] icon (  ![](../graphics/icon_more_options.png) ) that displays, then click [!UICONTROL  Remove Audience] to remove an existing audience. 
>1. Click ** [!UICONTROL  Add Experience Targeting] **.


>       >[!NOTE]
>       >
>       >If you are targeting an experience to an audience, you must select the audience before you can add an experience. A message appears to remind you to choose your audience.

>1. (Optional) Click ** [!UICONTROL  Add] ** and set up additional targeted experiences.

>       ![](../graphics/xt_add_xt.png) 

>       Click ** [!UICONTROL  Continue] ** when you are finished with this step. 
>1. Specify the [ goals and settings ](t_experience_target.md#reference_B25389FD6F3A4989801E740364B089CC) for the activity.

>       ![](../graphics/xt_settings.png) 
>1. Click ** [!UICONTROL  Save &amp;amp; Close] **.
>## Activity URL {#concept_D28549AAA0A14E3BB5F05F32BE8ABC90}The Activity URL determines the page that is used in the test, and that opens when the test is designed. 
<draft-comment otherprops="merge">
  target/c_xt_activity_url.xml 
</draft-comment>When prompted during activity creation, enter the activity URL. Type the complete URL (including http://), then click ** [!UICONTROL  Create Activity] **. 


>[!NOTE]
>
>[!DNL  Target] does not differentiate between URL protocols ( [!DNL  https] and [!DNL  http]). As a result, [!DNL  https://adobe.com] and [!DNL  http://adobe.com] both match. 



By default, the Visual Experience Composer opens the page that is specified in your [ Account Preferences ](https://marketing.adobe.com/resources/help/en_US/target/target/t_account_preferences.html). You can specify a different page during activity creation. 

To display a different page after the Visual Experience Composer opens, click ** [!UICONTROL  Configure] **, select ** [!UICONTROL  URL] **, and enter the URL in the Activity URL box. 

![](../graphics/url-config.png) 

Click ** [!UICONTROL  Add Template Rule] ** to add more pages or sections to the activity. 

Additional rules can be based on any of the following: 


* URL
* Domain
* Path
* Hash (#) Fragment
* Query
* mbox Parameter


Additional rules can be joined to the Activity URL with AND or OR. All rules you add are evaluated against each other with AND. 

Click ** [!UICONTROL  Save] ** when you have finished. 

<a id="section_373CAB401E6A43EFA4D82E000581A4D3"></a>


>[!NOTE]
>
>If you entered a URL for a site that does not include the Target Standard JavaScript code, you cannot select page elements.



By default, the [!UICONTROL  Visual Experience Composer] does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off ** [!UICONTROL  Render using JavaScript] ** if you want to be able to alter those elements using the [!UICONTROL  Visual Experience Composer]. 


>[!NOTE]
>
>If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.


>## Create Experience {#task_454646F2895242D3B92DC395A0CE1A00}The Experience Composer provides a visual interface for editing the experiences on your page. 
<draft-comment otherprops="merge">
  target/t_xt_add_experience.xml 
</draft-comment>For additional detail about experiences, see [ Experiences ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

>1. Click ** [!UICONTROL  Add Experience] **.


>       >[!NOTE]
>       >
>       >If you are targeting an experience to an audience, you must select the audience before you can add an experience. A message appears to remind you to choose your audience.

>1. When prompted, enter the activity URL. Type the complete URL (including ` http://`), then click ** [!UICONTROL  Continue] **.

>       The Experience Composer (see [ Experiences ](c_experiences.md#concept_1D011219034B492BB03C08B3BB80E3F0)) opens the page that is specified in your [ Account Preferences ](https://marketing.adobe.com/resources/help/en_US/target/target/t_account_preferences.html). To display a different page, click the Globe icon and enter the URL in the Select URL box in the Experience Composer and click ** [!UICONTROL  Continue] **. If you entered a URL for a site that does not include the Target Standard JavaScript code, you cannot select page elements. 

>       By default, the Visual Experience Composer does not allow changes to elements containing JavaScript, such as rotating banners. You can select to disable JavaScript if you want to be able to alter those elements using the Visual Experience Composer. 


>       >[!NOTE]
>       >
>       >If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.

>1. Select the elements you want to change and make the desired changes.

>       As you hover the elements on your page, the elements are highlighted. Any highlighted element can be altered using the Experience Composer. 

>       The video below provides information about using the Visual Experience Composer options. 



>    <table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Visual Experience Composer (1 of 2) </th> 
   <th colname="col3" class="entry"> 7:17 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/2KUDgu6Mscg/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/2KUDgu6Mscg/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Change the content of a page </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Change the layout of a page </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>       If you created an mbox on the page using Target Classic (formerly Test&amp;amp;Target), that mbox appears as an element that shows the mbox name, and can be modified like any other element. 

>       The following actions can be performed on an element on the displayed page to change the experience: 



>    <table id="table_B146BECBBF554EEA8BA6F72C09CCE73F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Option </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Edit Text/HTML </td> 
   <td colname="col2"> <p>Change the HTML code for the element, such as the text for a text area, button, or link. </p> <p>In addition to HTML code, you can edit and inject custom JavaScript. </p> <p>Several rich text formatting options are available when editing text and HTML for A/B and Experience Targeting activities. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Edit Background Color </p> </td> 
   <td colname="col2"> <p>Use the color picker to select or configure a background color. You can select a color swatch, and adjust it using RGB values or color hex codes. The red x in the color picker makes the background transparent. </p> <p> <p>Note:  This option is not available for an element where a background image is set. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Insert Element </td> 
   <td colname="col2"> <p>Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test. </p> <p>Select an element on the page, then click <span class="uicontrol"> Insert Element </span> and choose whether you want to insert an image, HTML, or text. The inserted element appears after the selected element. </p> <p>The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected. </p> <p> <p>Note:  Inserting an image requires that Adobe Scene7 Publishing System is enabled so you have access to the image library. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Edit Link </td> 
   <td colname="col2"> <p>Change the URL in the link. </p> <p>Use <span class="uicontrol"> Edit Link </span> to update the selector to point to the same image element. However, linking to a different image element is not supported. To link to a different image element, delete the original action from the code editor and use the <span class="wintitle"> Visual Experience Composer </span> to apply the action on the other image element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Edit CSS Class </td> 
   <td colname="col2"> <p>Specify the predefined CSS class used for the element. If more than one element is selected, separate multiple CSS classes with a space. </p> <p>Available for A/B, Automated Personalization, and Multivariate test activities. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Swap Offer </td> 
   <td colname="col2"> <p>Select a different offer from the Content Library. </p> <p> <p>Note:  HTML Offers are stored on Target servers. </p> </p> <p>An HTML offer can be up to 256KB in size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Swap Image </td> 
   <td colname="col2"> <p>Select a different image from the Content Library. The images available for swapping include the images uploaded to the Marketing Cloud assets folder or uploaded in the Content Library in Target. </p> <p>During initial activity creation, the URL displayed is not the URL used for delivery. Upon activity synching, that URL is updated to a production Scene7 URL. </p> <p>For example, the initial URL might look like the following example: </p> <p> 
     <codeblock>
       https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867 
     </codeblock> </p> <p>After activity syncing, the delivery URL might look like the following example: </p> <p> 
     <codeblock>
       http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&amp;amp;fit=constrain&amp;amp;hei=173&amp;amp;wid=300 
     </codeblock> </p> <p> <p>Note:  Swapping images requires an Adobe Scene7 Publishing System account. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Remove Item </td> 
   <td colname="col2"> <p>Remove the element. The white space behind the image is removed and the space where the element was is collapsed. </p> <p> <p>Note:  Items within a "classic" mbox (an mbox created within a <span class="keyword"> Target Classic </span> campaign) cannot be removed using this option. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hide Item </td> 
   <td colname="col2"> <p>Hide the element. The white space remains, but the content is removed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rearrange </td> 
   <td colname="col2"> <p>Drag the element to another location inside the same parent element or <span class="filepath"> &amp;lt;div&amp;gt; </span>. Other elements shift location to make space for the rearranged element. </p> <p> <p>Note:  Click tracking does not work on rearranged items. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Move </td> 
   <td colname="col2"> <p>Move elements on your page. Unlike the <span class="wintitle"> Rearrange </span> option, <span class="wintitle"> Move </span> does not shift other elements to make room for the element being moved. Use the arrow keys to fine tune the move. (Planned enhancement: support for making sure moved elements are not hidden behind other elements.) </p> <p>In some cases, such as when a CSS restriction requires an element to remain inside its parent element, you cannot move the element outside its parent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Resize </td> 
   <td colname="col2"> <p>Resize an element on your page. When you select <span class="uicontrol"> Resize </span>, a handle appears in the bottom right corner of the element that lets you drag that corner to resize. Hold the Shift key to retain the same aspect ratio. </p> <p> <p>Note:  Inline elements cannot be resized. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Expand Selection </td> 
   <td colname="col2"> <p>Select the parent element in addition to the originally selected element. When you select any parent element, all children of that element are automatically selected. You can expand the selection multiple times. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Navigate to this Link </td> 
   <td colname="col2"> <p>Open the destination of the link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Undo/Redo </td> 
   <td colname="col2"> <p>Undo changes you make to your activities during an editing session. You can also redo changes that have been previously undone. </p> </td> 
  </tr> 
 </tbody> 
</table>


>       >[!NOTE]
>       >
>       >If you deliver an image from a source other than your main page (such as an image hosted on akamai.net and delivered on dell.com), then that image does not display in the thumbnail of the page shown in the flow diagram.

>1. Click the Check Mark button when you are finished designing the experience.

>       The activity diagram displays: 

>       ![](../graphics/xt_diagram.png) 

>       If an experience includes cross-domain content, the thumbnail might not display accurately and is replaced by an icon. 
>1. Create additional experiences, as desired.


>       >[!NOTE]
>       >
>       >You can drag and drop audience/experience pairs while creating or editing XT activities to arrange the pairs in the desired order. Visitors will be evaluated for experiences in order, from top to bottom.


>       ![](../graphics/move experiences.jpg) 

>       Experience Targeting assumes that order matters. If a visitor falls into the first audience/experience pair, the first experience is delivered. 

>       For example, suppose you were not aware that order matters while creating an XT activity. You later realize during testing that visitors that you think should qualify for experiences B or C are instead qualifying for experience A. This could be because the audiences are not mutually exclusive and are not in the proper order (for example, experience A = United States, experience B = San Francisco, and experience C = California). In this scenario, all users from the United States qualify for experience A, even if they are located in San Francisco or elsewhere in California. You can reorder the audience/experience pairs from most restrictive to least restrictive (San Francisco &amp;gt; California &amp;gt; United States) without re-creating the entire activity. 
>1. Click ** [!UICONTROL  Continue] ** when you are finished with this step.
>## Switching Experiences in Experience Targeting {#concept_01D067B9063E4256BED997CE8532310D}Information about the how visitors can switch between experiences in an Experience Targeting (XT) activity as their profiles evolve. 
<draft-comment otherprops="merge">
  target/c_xt-switching-experiences.xml 
</draft-comment>
<table id="table_4877125D1060461CBE8042261839BDEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>September 21, 2017</b> </p> <p>With the release on September 21, Target will change the way users are placed into experiences in Experience Targeting (XT) activities (Landing Page campaigns in Target Classic). For all new and existing activities in both Target Standard/Premium and Target Classic, users must meet the experience targeting rules on every impression to continue to see the experience's content and to be counted in reports. Previously, if the user no longer qualified for any experience, the user would continue to see the content from, and be counted in reports for, the last experience they did qualify for. </p> <p>This change will happen automatically as part of the release for all existing activities and for any new activities created post-release. If the previous method (prior to September 21) is desired, you can create audiences using profile scripts so a user only must meet a condition once to continue to fall into that audience in the future. Then, use those audiences for each experience in the activity. </p> </td> 
  </tr> 
 </tbody> 
</table>

With Experience Targeting, you can control which experience visitors see as their profiles evolve. The following list presents just a few scenarios in which visitors' profiles can evolve and you might want to present different content: 



<table id="table_4809FC45A27743128026C5E3074955EC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Scenario </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Geographic Location </p> </td> 
   <td colname="col2"> <p>As visitors travel for business or pleasure, they might view your website or mobile app from different geographic locations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Customer Status </p> </td> 
   <td colname="col2"> <p>Visitors might be considered prospects before creating an account or purchasing a product. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Category Affinity </p> </td> 
   <td colname="col2"> <p>The <a href="../ov/c_visitor_profile.xml#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local"> category affinity </a> feature in <span class="keyword"> Target </span> automatically captures the categories users visit and then calculates the users' affinity for the category for targeting purposes. For example, visitors who viewed several articles on your website about a particular subject could be presented with content related to that subject. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Day of Week </p> </td> 
   <td colname="col2"> <p>As the weekend approaches, you might want to show visitors content about movies, dining, or other forms of entertainment. </p> </td> 
  </tr> 
 </tbody> 
</table>

To leverage these capabilities in [!DNL  Target], it is important to understand the following information as you work with XT activities: 


* **Priority is controlled by the order of experiences, top to bottom.** If a visitor qualifies for more than two audiences, he or she receives content from the higher priority experience. 

* **Visitors will switch between experiences in an XT activity if they start qualifying for the audience of a higher-priority experience. ** 

  For example, in the following activity setup, a visitor accessed your website from the United States and then traveled to Germany and visited your website a second time. During the first visit, this visitor qualified for Experience A (United States). After viewing your website from Germany, this visitor switched to Experience B (Germany). 

  ![](graphics/xt_priority us germany.png) 

* **Visitors will also switch between experiences if they stop qualifying for their current audience but start qualifying for a lower-priority experience.** 

* **If visitors stop qualifying for their current experience, and do not qualify for another experience, they will see default content.** 

  For example, in the following activity setup, a visitor accessed your website from the United States and then traveled to France and visited your website a second time. During the first visit, this visitor qualified for Experience A (United States). After viewing your website from France, this visitor will remain in the original experience. 

  ![](graphics/xt_priority us germany.png) 

* **An experience targeted to "All Visitors" can be used as the last experience in the experience targeting activity to "catch" any visitors that have not fallen into any other experience. If an experience targeted to "All Visitors" is not the last in the order, other targeted experiences listed lower than this experience will still be evaluated.** 

  For example, in the following activity setup, a visitor accessed your website from the United States and then traveled to Germany and visited your website a second time. During the first visit, this visitor qualified for Experience A (United States). After viewing your website from Germany, this visitor will remain in Experience A (United States). 

  ![](graphics/xt_priority us all visitors.png) 

  If this is undesirable, you can create a new audience that is explicitly defined as the inverse of your targeted audience, as shown in the following example: 

  ![](graphics/xt_priority us not us.png) 

* **With a single-experience XT activity, visitors will remain in an experience even if they cease to qualify for the audience that put them in that experience.** 

  If this is undesirable, you could create another experience targeted to the inverse audience (for example, "Not United States" as opposed to "United States"). As another option, you could create an A/B activity targeted to your desired audience with 100% traffic allocation, as shown below: 

  ![](graphics/xt_priority one experience.png) 

* **The priority of experiences is defined by their order (top down) as they display in the Target UI. ** 

  This is important to keep in mind in scenarios where a visitor might qualify for more than one of your audiences. For example, if you have two experiences: one targeted to "United States" and one targeted to "New York," a visitor located in New York would qualify for both audiences. Therefore, you must ensure that the "New York" experience is defined before the "United States" experience in the Target UI. This ensures that the more targeted "New York" experience has the higher priority, as shown in the following example: 

  ![](graphics/xt_priority ny us.png) 


>## Goals and Settings {#reference_B25389FD6F3A4989801E740364B089CC}The Goals and Settings page is where you enter information about the goals of the test. 
<draft-comment otherprops="merge">
  target/r_xt_goals_and_settings.xml 
</draft-comment>
<a id="section_9B98C5E38DC244D0829B9B06CA627EA9"></a>


* Activity Settings
* Reporting Settings
* Other Metadata


The available settings depend on whether you use Target or Analytics as the data source. 

![](graphics/ab_settings.png) 

## Activity Settings {#section_DCBDC354261F420EBD4B43EA34947BAC}



<table id="table_464BE186EE1F463DA99D16FC482A4AFA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Settings </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Objective </td> 
   <td colname="col2"> <p>Type an optional objective. The objective can be any information that helps you and your team members identify the campaign. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Priority </td> 
   <td colname="col2"> <p>Depending on your settings, the UI and options for <span class="wintitle"> Priority </span> vary. You can use the legacy settings of Low, Medium, or High, or you can enable fine-grained priorities from 0 to 999. </p> <p>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays. </p> <p>If this option is not enabled in <span class="wintitle"> Setup </span> (the default), specify a priority: Low, Medium, or High. </p> <p> To enable fine-grained priorities, click <span class="wintitle"> Setup </span>, then toggle the <span class="wintitle"> Enable Fine-Grained Priorities </span> option to the "On" position. </p> <p>If this option is enabled, specify a value between 0 and 999: </p> <p> 
     <ul id="ul_FCA07A04D6F248759429BC46BA57CCE5"> 
      <li id="li_88F440506D22467295C71F2B14470AD7">0 = Low </li> 
      <li id="li_AEC7893759464944A6501FA742A2B0FE">999 = High </li> 
     </ul> </p> <p>For activities created in previous versions of <span class="keyword"> Target Standard/Premium </span>, Low priority is converted to 0, Medium is converted to 5, and High is converted to 10. You can adjust these values as necessary. </p> <p> <p>Note:  Before you can disable this option after using fine-grained priories, all priorities must be set back to 0, 5, and 10. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Duration </td> 
   <td colname="col2"> <p>The activity can start when approved, or you can set a specific date and time. Likewise, the activity can either end when it is deactivated or you can set a date and time. The time picker uses a 24-hour clock, with 00:00 being midnight. The time zone is set to the time zone configured in your browser. To use a different time zone, set your browser to another time zone and restart the browser. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Reporting Settings {#section_13119392051044FBA6387D9B3B1C43CF}



<table id="table_178993EC689C4C538F3EC7E3FC205592"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Settings </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Reporting Solution </td> 
   <td colname="col2"> <p>Specify whether data is collected from Adobe Target or from Adobe Analytics. See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/a4t.html" format="https" scope="external"> Adobe Analytics as the Reporting Source for Target </a> to learn about the differences between the reporting solutions and the advantages of each. </p> <p>When selecting Analytics as the reporting source for Target, you select an Analytics report suite to receive Target activity data. To do this, first choose from any of the Analytics companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to Adobe Target will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the Adobe Marketing Cloud to try again. If the report suite is still missing from the list, please contact Customer Care. </p> <p>Analytics for Target requires a tracking server to report results correctly. A default tracking server will appear in the Tracking Server field. If you use more than one tracking server, you should check to ensure you include the correct tracking server in this field. See <a href="../a4t/a4t.xml#task_72077BA7E93C4A65A715A18F32228823" format="dita" scope="local"> Using an Analytics Tracking Server </a> for more information. </p> <p>If a reporting solution is specified in your account settings, the specified solution is used and this setting is not visible. </p> <p> <p>Note:  You cannot change your reporting source after the activity goes live in order to keep reports consistent. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Goal </td> 
   <td colname="col2"> <p>Select the action taken by a visitor to achieve the goal. For example, choose a Conversion metric, then set the parameters that determine when success is achieved. </p> <p>For more information about setting metrics, see <a href="t_test_ab.xml#task_A04AB66007C1467DA1C21A519A5C7BEB" format="dita" scope="local"> Set Metrics </a>. </p> <p> <p>Note:  If the reporting solution is set to Analytics, the only available goal metric is Conversion. Analytics metrics cannot be selected as a goal. </p> </p> <p>When you select your success metric, a selector displays. Use this selector to choose the specifics for the success metric. </p> <p>If enabled, the Estimated Value of the Conversion field (not available for the Page Score metrics) provides a value for your goal, but not for other metrics. This value enables Target to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. For all revenue metrics (Revenue per Visitor, Average Order Value, Total Sales, and Orders), the estimate uses Revenue per Visitor. The data type is currency. </p> <p> After reaching the activity goal, a visitor continues to see the activity content, unless that visitor qualifies for a higher priority activity. If the visitor reaches the goal again, it is counted as another conversion. Note that this is different than the default behavior in Target Classic, which counts visitors as new if they see the test again. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Additional Metrics </td> 
   <td colname="col2"> <p>Create additional success metrics. </p> <p>This setting is not available if the reporting solution is set to Analytics. In this case, the metrics defined for the Analytics report suite are applied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Audiences for Reporting </td> 
   <td colname="col2"> <p>By default, reports show results for all qualified visitors. You can add report audiences to show only information about specific audiences. </p> <p>This setting is not available if you choose Analytics as your reporting solution. The audience defined for the Analytics report suite are applied. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Advanced Settings {#section_E2FE441AFB324E498793ABB025ED9974}

Advanced settings are available for Experience Targeting goal metrics. 

![](graphics/Menu_AdvancedSettings.png) 


>[!NOTE]
>
>If you use Adobe Analytics as your reporting source, settings are managed by the Analytics server. The advanced settings option will not be available.





<table id="table_5706360D23704F16AA18597D4C8F3438"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Which success metric must be reached before incrementing this metric? </td> 
   <td colname="col2"> <p>Use this option to only count someone as reaching the success metric if they’ve previously reached a different success metric. For example a test conversion might only be valid if the visitor clicks on the offer, or reaches a particular page before converting. </p> <p>You can provided dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increase. </p> <p>You must define both (or multiple) success metrics before you can make one dependent on another. </p> <p>The <span class="wintitle"> Add Dependency </span> option allows the success metric to increment if another success metric has been reached or has not been reached. </p> <p>To add a dependency: </p> <p> 
     <ol id="ol_7CE86C31CD5541039A3265E14D0C3630"> 
      <li id="li_3E374D8B28B443FA9FE8AF2B02814A82"> <p>After adding additional metrics, click <span class="uicontrol"> Advanced Settings </span>. </p> </li> 
      <li id="li_F65C369C8F354A6CBD447ED26D9F79E4"> <p>Click the <span class="uicontrol"> Add Dependency </span> option: </p> <p style="text-align: center;"> <img href="../graphics/add dependency.png" id="image_D3C6E4862509435E86A1F61B88F342CA" /> </p> </li> 
      <li id="li_9A6F187B4C294A9C8B5C834C76B32767"> <p>Drag and drop the desired metrics from the left pane into the right pane, then click <span class="uicontrol"> Reached </span> to toggle the setting between <span class="uicontrol"> Reached </span> and <span class="uicontrol"> Not Reached </span>. </p> <p style="text-align: center;"> <img href="../graphics/add dependency reached.png" id="image_CA136FD10D754BD1B26C621DF2A4858D" /> </p> </li> 
     </ol> </p> <p>You can edit or remove dependencies after adding them. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> What will happen after a user encounters this goal metric? </td> 
   <td colname="col2"> <p>There are three options for what happens after a visitor reaches the goal metric: </p> 
    <ul id="ul_2347FFB59E804DB382C3440BE684000E"> 
     <li id="li_5A8C13D4D43C436786D9FBE24C701CE1">Select <span class="uicontrol"> Increment Count &amp;amp; Keep User in Activity </span> to specify how the count is incremented. </li> 
     <li id="li_04D4A04310354FB4A7F23023E1FE0DE0">Select <span class="uicontrol"> Increment Count, Release User &amp;amp; Allow Reentry </span> to specify the experience the user sees if they reenter the activity. </li> 
     <li id="li_32FEAFA4C6BC469998C9181792B29BEE">Select <span class="uicontrol"> Increment Count, Release User &amp;amp; Bar from Reentry </span> to specify what the user sees instead of the activity content. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

See [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924) for more information about advanced settings. 

## Other Metadata {#section_2E8917BEFB954480A4206B9E9E917F80}



<table id="table_41D61740D4C246D695CE8B785B1785CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Settings </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Notes </td> 
   <td colname="col2"> <p>Type any information about your activity that is useful to keep on hand for yourself or other team members. The Notes pane is resizable. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Set Metrics {#task_A04AB66007C1467DA1C21A519A5C7BEB}Use metrics in an Experience Targeting (XT) activity to determine when a visit is successful. 
<draft-comment otherprops="merge">
  target/t_xt_set_metrics.xml 
</draft-comment>For detailed information about success metrics, see [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924). 

>1. Specify the goal of the activity.
>1. Select a [ success metric ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924)

>       ![](../graphics/ab_metrics.png) 

>       The [!UICONTROL  Select Metrics] page lists the success metrics you can choose for your activity. The success metrics are divided into the following categories: 

>    
>    * Conversion
>    * Revenue
>    * Engagement


>       You can use any of the pre-built success metrics, or create a custom success metric. You can also mark a success metric as a primary metric. Reports and Marketing Cloud cards default to show the primary metric, if one is set. 
>1. Specify the settings for your metrics.

>       The available settings depend on the success metric you are using. 

>       If enabled, the [!UICONTROL  Estimated Value of the Conversion]field (not available for the Page Score metrics) provides a value for your goal. This value enables Target to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. The data type is currency. This field is progressively shown after the user indicates the action taken to satisfy the goal. See [ Estimating Lift in Revenue ](c_estimating_lift_in_revenue.md#concept_32F875D8F91349CE86AF391F65BEAEEE) for more information. 

>       The correct configuration of success metrics is critical for making sure you get the data you expect. 

>       For more information, see [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924). 
>1. (Optional) Add additional metrics.
>1. Click ** [!UICONTROL  Continue] ** when you are finished setting your metrics.
