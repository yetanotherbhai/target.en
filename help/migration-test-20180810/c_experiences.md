---
description: An experience determines which content displays when the visitor meets the audience criteria for an activity.
keywords: Experience Targeting;Landing Page Test
seo-description: An experience determines which content displays when the visitor meets the audience criteria for an activity.
seo-title: Experiences
solution: Target
title: Experiences
topic: Standard
uuid: f81c614e-9dae-4237-bf32-d1fe60472419
index: y
internal: n
snippet: y
translate: y
---

# Experiences

## Experiences {#concept_A2E10F6AFB3D4AEAB6951EE14688848D}An experience determines which content displays when the visitor meets the audience criteria for an activity.An activity typically contains more than one experience. For example, visitors from the Salt Lake City area might see an offer for a $30 discount on ski boots, while visitors from San Diego see an offer for a discount on wet suits. Or, you might test a page with different special offers for returning visitors. Each of these offers is presented in a separate experience. 

## Visual Experience Composer and Enhanced Experience Composer {#section_34265986611B4AB8A0E4D6ACC25EF91D}

The Visual Experience Composer is one of the main features of Adobe Target. The Visual Experience Composer is an editor that enables marketers and designers to create and change content using a visual interface. Many design choices can be made without requiring direct editing of the code. Editing HTML and JavaScript is also possible using the editing options available in the composer. 

The videos below provide information about using the Visual Experience Composer. 

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
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


<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Visual Experience Composer (2 of 2) </th> 
   <th colname="col3" class="entry"> 7:29 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/qwUKEp8en_k/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/qwUKEp8en_k/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F">Rename and duplicate an experience </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Create a redirect experience </li> 
      <li id="li_79866ECECA2D4ACB9AE991B2922ADA84">Target an activity to a single URL or a group of URLs </li> 
      <li id="li_67ED273861FC493785AC049CC0B37E6A">Create a multi-page activity </li> 
      <li id="li_F4646D966373499DA6A32ED62411DF57">Preview and build experience for responsive websites </li> 
      <li id="li_4CA9280B227C4ACBB3EDDC23AB8ECCC3">Use overlays to highlight types of elements </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

On the Target ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Preferences] ** tab, you can enter the Default Visual Experience Composer URL. 

![](../graphics/pref-default-url.png) 

This URL determines where you start when you open the Visual Experience Composer. If you do not enter a default, then you start with a blank page when you open the editor, and specify a URL at that time. 


>[!NOTE]
>
>Certain browsers, such as Firefox, might block a page from displaying in the Visual Experience Composer if the page contains mixed content (for example, a non-secure page in a secure site). If your page does not display, click the icon to the left of the URL in the browser address bar and click ** [!UICONTROL  Disable protection on this page] **. This issue does not affect the display of your pages to site visitors. 



Content inside an iframe on the page can't be modified in Visual Experience Composer. To edit content within an iframe, ensure that the iframe document is Target-enabled, then load that iframe URL in the Visual Experience Composer. 

You can use the drop-down menus across the top of the page to view your page as it would appear to different audiences or with different experiences. You can provide a name for each experience in the second drop-down list. For example, if you are testing the location of the Home link in your nav bar, you might name an experience where the Home link appears first something like, "Home link" to make it easier to identify the experiences in the list. 


>[!NOTE]
>
>Changes to the structure of a page that affect the locations used in an activity created on that page could cause issues with experience editing. If a location has been changed outside the Visual Experience Editor, Target might not be able to find the location where the content was changed.



As you move your mouse around the page, a context-sensitive box follows the cursor, highlighting the elements on the page. 

![](../graphics/vec_highlight.png) 

Click the Overlays icon to change the way the highlight displays. For example, you can choose to highlight only images or mboxes or links, and you can change the color of the highlight. You can also specify a highlight color and type of fill used to highlight different element types. 

Click on a highlighted element for a menu of options available for that element type For example, you can click on an image and select ** [!UICONTROL  Edit Image] ** to change the image, or click on a button and change the HTML. You can use the buttons at the top left of the page to toggle the overlays on and off. 

You can also click ** [!UICONTROL  Browse] **, then navigate to a page that is available from the primary page, such as a shipping page or shopping cart, and test changes on that page. You can also access page elements that are available when you hover, such as flyout menus and mini-carts. When you are finished browsing to the page, click ** [!UICONTROL  Compose] ** to edit the experience. For example, you might want to change the design of a shopping cart drop-down or a carousel of images. This functionality is currently available for A/B tests, A/B tests with Analytics, and experience targeting. 


>[!NOTE]
>
>If a hover state depends on JavaScript, make sure ** [!UICONTROL  Disable JavaScript] ** is not selected. JavaScript must be enabled to edit JavaScript elements. 



For information about the options available in the Visual Experience Composer, see [ Visual Experience Composer Options ](c_experiences.md#reference_3BD1BEEAFA584A749ED2D08F14732E81). 

## Form-Based Experience Composer {#section_3643394BD424463C8768F2907DEBCC22}

The Form-Based Experience Composer enables Target Standard A/B tests, Experience Targeting and Recommendations activities to be delivered in emails, mobile apps, kiosks, and other places that don't work with a Visual Experience Composer. 

This video provides a demo of the form-based composer: 

<table id="table_47FED9E4494B4ABB9BBD4D082534BC45"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Form-Based Experience Composer </th> 
   <th colname="col3" class="entry"> 4:35 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/R9hcD9D1VPY/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/R9hcD9D1VPY/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_3B9FF13D85254CBF84E539960B764CF0"> 
      <li id="li_317BEB0C637349818D3C1784803C0FE9">Create an activity using the Form-Based Experience Composer </li> 
      <li id="li_996E0C8D914E42DE90F6552B3C1161B9">Understand when to use Form-Based Experience Composer vs. the Visual Experience Composer </li> 
      <li id="li_B5B119535AD3488CAAAD8EEF45AD3418">Use refinements to target a location </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

See [ Form-Based Experience Composer ](t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) for more information. 
>## Visual Experience Composer Options {#reference_3BD1BEEAFA584A749ED2D08F14732E81}When you click on a page element, a menu shows the options that are available for that element type. 
<draft-comment otherprops="merge">
  target/r_viztarget_options.xml 
</draft-comment>
>The following options are available. 


>>[!NOTE]
>>
>>The available options depend on the activity type you are editing.
>




><table id="table_B146BECBBF554EEA8BA6F72C09CCE73F"> 
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

>## Include the Same Experience on Similar Pages {#task_2539D51A18044F82B0D9895636546781}If you use a page template to provide structure to your pages, or if your pages contain similar elements, this feature makes it possible to test variations in similarly structured page elements. 
<draft-comment otherprops="merge">
  target/t_temtest.xml 
</draft-comment>To work correctly, this feature must be used on pages that have a very similar structure. or contain template elements that are structured the same on all pages. 


>[!IMPORTANT]
>
>Using this feature to change elements across dissimilar pages will likely cause unexpected results.



For example, you might use this feature to do one of the following: 

* Test a global navigation bar by rearranging or removing elements
* Remove an item from all product pages that use a particular page template
* Add a banner to all product pages
* Change the layout of article template
You can specify pages that include the change elements, or apply the change across your site. 

>1. Create an activity as described in [ Activities ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).
>1. To specify the pages where the experience will appear, in the Visual Experience Composer click the gear icon, then select ** [!UICONTROL  URL] **.

>1. Click ** [!UICONTROL  Add Rule] **, then specify the criteria for the pages you want to add the experience to.

>    
>    1. Specify the page range. The page range can be one of the following: >    
>        * URL
>        * Domain
>        * Path
>        * Hash (#) Fragment (Target the part of a URL that follows the # symbol.)
>        * Query
>        * Mbox parameter


>    1. Choose an operator. The operator specifies how the items after the operator relate to the page range. Available operators are: 

>    
>        * Contains
>        * Does not contain
>        * Is
>        * Is not


>    1. Type the strings that define where the experience is added, such as the domain or the strings contained in the page name. For example, if you select ** [!UICONTROL  Domain] ** and ** [!UICONTROL  Is] **, type the domain where you want the experience added to all pages. 

>       You can include multiple items. 


>       >[!IMPORTANT]
>       >
>       >Multiple items use ` OR` logic, meaning that any single item in the list makes the condition true. 



>1. If desired, enter additional criteria by clicking ** [!UICONTROL  Add Criteria] **and repeating the procedure in the previous step.

>## Multipage Activity {#concept_277E096063E14813AC5D8EDFA1D2ED48}A multipage activity enables you to create a story over multiple pages, with a design that is specific to each page. 
<draft-comment otherprops="merge">
  target/c_multipage_activity.xml 
</draft-comment>For example, you might want to test an offer for free shipping with purchases above a certain amount. You might want that offer to appear on your landing page, a category page, and certain product pages, but you want it to be a different size and in a different location on each page type. You could display a prominent offer on your home page, then reinforce that offer with smaller offers on other relevant pages. 

You can also use a multipage activity to define different layouts for your desktop and non-responsive mobile sites. If the site has a separate mobile site like [!DNL  m.mysite.com] instead of [!DNL  www.mysite.com], you should instead create a [ multipage activity ](c_experiences.md#concept_277E096063E14813AC5D8EDFA1D2ED48), add [!DNL  m.mysite.com] as separate pages, and then apply mobile editing to make appropriate changes on the desktop version and mobile version in the same experience. For responsive mobile sites, use [ mobile experience editing ](c_mobile_viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5). 


>[!NOTE]
>
>Multipage activities are designed for activities where the same offer has a different appearance on multiple pages. If the offer appears the same on all pages, a[ template test ](c_experiences.md#task_2539D51A18044F82B0D9895636546781) is more efficient. 



You can specify template rules for each page in the multipage test. For example, you can run a multipage test across the home page and all category pages by applying template rules to the category page in the multipage test. See [ Include the Same Experience on Similar Pages ](c_experiences.md#task_2539D51A18044F82B0D9895636546781). 

To add pages to a test: 

1. Click the ** [!UICONTROL  Configure] ** gear icon.
1. Click ** [!UICONTROL  Add Additional Pages] **. A navigation bar appears on the left of the screen. 

   ![](../graphics/multipage_nav.png) 

1. Use that navigational bar to specify your pages and to set the default page. Click ** [!UICONTROL  Add Page] ** to add an additional page. 

   Click the  ![](../graphics/action menu.png) to display an action menu: 

   ![](../graphics/multipage_menu.png) 

   Use this menu to rename the pages, perform a redirect test from within the multipage activity or delete the page. 

1. Use the Visual Experience Composer to design the way the offer looks on each page.
>## Activity Collisions {#concept_0BC6B929592744DFA7DA01FF4F91052E}The Collisions tab on the Activity Overview page lists activity collisions on your site. 
<draft-comment otherprops="merge">
  target/c_activity_collisions.xml 
</draft-comment>An activity collision occurs when multiple activities are set up to deliver content to the same page. If an activity collision occurs, you may not see the expected content on your page. 

If your activity contains potential collisions, the [!UICONTROL  Collisions] tab is available the on the activity overview page. All activities on the same URL are listed, regardless of any audience targeting in each activity. Open this tab for a list of activities that might be colliding. Click an activity in the list to view the overview page for that activity. If the collision alters the expected experience, edit the activity. 

The Collisions list helps you: 


* Identify whether a test is already running on a page before you set up a new activity
* Troubleshoot an activity if the expected content does not appear


The Collisions list shows every Target Standard scenario where the mbox is used and that uses the same URL. For each potential collision, the list shows the Activity URL, the mbox name where the collision might occur, and any activities that match bot of those criteria. If there are multiple mboxes, they are each listed. 

The list shows the status and priority of each potential collision, along with other information. You can use the status and priority to help you determine the likelihood of a collision occurring. For example, if there is a potential collision between two activities and one is inactive, there will be no actual collision unless the inactive activity is activated. If the potential collision is between two live activities with the same priority and the same audience, a collision will occur. You can change the priority or status to prevent the collision. 

If the audiences are different, there is still a potential collision because it's possible a particular visitor could belong to multiple audiences. 
>## Element Selectors Used in the Visual Experience Composer {#concept_4EB7663E255F439B8D24079D23479337}An element selector is a CSS expression which can identify one or more elements. 
<draft-comment otherprops="merge">
  target/c_vec_selectors.xml 
</draft-comment>You can find basic information about CSS selectors in the [ Selectors ](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) document on the Mozilla Developer Network (MDN). 

You can set whether to use element classed or element IDs in your account preferences. Click ** [!UICONTROL  Setup &amp;gt; Preferences] **, then choose your preferred CSS selectors. 

![](../graphics/css_selectors.png) 


>[!NOTE]
>
>Element Classes are available as selectors in A/B Test, Automated Personalization, and Multivariate Test activities.



For information about when to use CSS selectors and when to use unique IDs, see [ Visual Experience Composer Best Practices and Limitations ](vec-best-pracitces-and-troubleshooting.md#concept_E284B3F704C04406B174D9050A2528A6). 

## How Adobe Target Generates a Selector for an Element {#section_D89D954BCBFB486CA081BE183776A475}

Target uses a simple algorithm to create a selector. Here is very brief explanation of the generation logic: 


1. If an element has an id, for example ` id="container"`, then the selector for the element is ` #container`. For Example: 


   ```
   <div class="wrapper"> 
     <div id="container"> <!-- Selector is computed for this element --> 
       <ul class="navigation"> 
         <li class="item active"> Home </li> 
         <li class="item"> Men </li> 
         <li class="item"> Women </li> 
         <li class="item"> Kids </li> 
       </ul> 
     </div> 
   </div> 
   
   ```


1. If an element contains a class attribute, Target attempts to leverage the first class of any classes present on the element. Target attempts to parse the parent element until it finds the ` &amp;lt;HTML&amp;gt;` element or an element with an id. Whenever an element contains an id and the selector is computed on its descendant child, this element's id contributes to the selector. 

   For example: 


   ```
   <div class="wrapper"> 
     <div id="container"> <!-- id is present here. It contributes to selector --> 
       <ul class="navigation"> 
         <li class="item active"> Home </li> <!-- Selector is computed for this element --> 
         <li class="item"> Men </li> 
         <li class="item"> Women </li> 
         <li class="item"> Kids </li> 
       </ul> 
     </div> 
   </div>
   ```


   In this example: 

   Selector: ` #container` > ` ul.navigation:eq(0)` > ` li.item:eq(0)` (" &gt; " indicates the immediate child.) 

   ` eq` tells the index there's an element that has "tagName=UL" and the first class is ` navigation`. Therefore, ` index` is 0. See the [ Selectors ](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) article in MDN for more information. 

1. If an element does not contain a class, Target uses ` tagName` for the element and traverses up the parent element until either the ` &amp;lt;HTML&amp;gt;` element or an element with an id is found. For example: 


   ```
   <div class="wrapper"> 
     <div id="container"> <!-- id is present here. It contributes to selector --> 
       <ul class="navigation"> 
         <li> Home </li> 
         <li> Men </li> 
         <li class="active"> Women </li> 
         <li> Kids </li><!-- Selector is computed for this element --> 
       </ul> 
     </div> 
   </div>
   ```


   Selector: ` #container` > ` ul.navigation(0)` > ` li:nth-of-type(4)` 

   You can learn more about [ nth-of-type on the CSS Tricks web page ](https://css-tricks.com/almanac/selectors/n/nth-of-type/). 



In the above process: 


* You can use any CSS selector as long as it uniquely identifies an element in the DOM.
* The approach above is the one used by Target. Target does not mandate that you use this approach. You can add any selector as long as point #1 is true.
* You can use any attribute in the selector. This document only uses class name as an example.

