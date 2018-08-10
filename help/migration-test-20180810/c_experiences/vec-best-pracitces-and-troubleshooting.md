---
description: Following best practices can help make your experiences work as expected. There are also other tips and limitations that you should be aware of when using the Visual Experience Composer (VEC). target/c_experience_composer_best_practices.xml
keywords: Recommendations
seo-description: Following best practices can help make your experiences work as expected. There are also other tips and limitations that you should be aware of when using the Visual Experience Composer (VEC). target/c_experience_composer_best_practices.xml
seo-title: Visual Experience Composer Best Practices and Limitations
solution: Target
title: Visual Experience Composer Best Practices and Limitations
topic: Premium
uuid: 785120fd-7212-4b05-94ea-26e60f710172
index: y
internal: n
snippet: y
translate: y
---

# Visual Experience Composer Best Practices and Limitations

## Visual Experience Composer Best Practices and Limitations {#concept_E284B3F704C04406B174D9050A2528A6}Following best practices can help make your experiences work as expected. There are also other tips and limitations that you should be aware of when using the Visual Experience Composer (VEC). 
<draft-comment otherprops="merge">
  target/c_experience_composer_best_practices.xml 
</draft-comment>By following these best practices, you are less likely to encounter unexpected problems with the experiences you design. 

## Best Practices {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}



<table id="table_E1E01D8E51F94B08888A01219AAA5E2C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Best Practice </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>For mbox.js version 57 and later, and for at.js, place the mbox.js or at.js reference at the top of the &amp;lt;head&amp;gt; section of your page. </p> </td> 
   <td colname="col2"> <p>If you also use the Visitor API Service, place the visitor API script above mbox.js or at.js. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>For versions of mbox.js before version 57, place the mbox.js code as low as possible in the &amp;lt;head&amp;gt; section of your page. </p> </td> 
   <td colname="col2"> <p>Place the mbox.js at the end of the &amp;lt;head&amp;gt; section, with no additional declarations after it. Otherwise, any script or link tags will be moved into the &amp;lt;body&amp;gt; section. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>You can enable the <span class="wintitle"> Enhanced Experience Composer </span> at the account level (enabled for all activities created in the account) or at the individual activity level. </p> </td> 
   <td colname="col2"> <p>To enable the <span class="wintitle"> Enhanced Experience Composer </span> at the account level, click <span class="uicontrol"> Setup </span> &gt; <span class="uicontrol"> Preferences </span>, then toggle the switch to the On position. </p> <p>To enable the <span class="wintitle"> Enhanced Experience Composer </span> at the activity level while creating an activity in the <span class="wintitle"> Visual Experience Composer </span>, click <span class="uicontrol"> Configure </span> &gt; <span class="uicontrol"> URL </span>, then toggle the switch to the On position. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> You can whitelist certain IP addresses if the Enhanced Visual Experience Composer won't load on secure pages on your site. </p> 
    <!--<p>This list is also included in Troubleshooting the VEC below. Keep them consistent if new IPs are added.</p>--> </td> 
   <td colname="col2"> Problems loading the Enhanced Visual Experience Composer can be resolved by whitelisting the following IP addresses. These IP addresses are for Adobe's server used for the Enhanced Experience Composer proxy. They are only required for activity editing. Visitors to your site do not need these IP addresses whitelisted. <p> 
     <table id="table_E8DFD24B9B684CF182CEAFCA13ADD9C4">  
     </table> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Use unique IDs for top-level elements and any other elements that could be good testing/targeting candidates. </p> </td> 
   <td colname="col2"> <p>Anything immediately inside the body element should have a unique ID. If new elements are injected into the body and code moves around, at least the parent elements have an easier way to be recognized. </p> <p>Adobe Target does not require IDs, but using IDs increases the reliability of experiences created with the experience composer. Target uses CSS selectors to modify your content when the experience is delivered. When you edit an experience, the Visual Experience Composer anchors the selector to the closest ancestor with a non-null id attribute to the HTML element being modified. It is, therefore, not advisable to use any mechanism, including JavaScript libraries, that sets or modifies HTML ID attributes. Although those IDs might be available to the Target experience composer for activity creation, if JavaScript modifies IDs, the ID that was used when the experience was created might not be available when the experience runs. If an ID is not available, the selector anchored to the ID fails. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Name CSS classes so they are easily identifiable. </p> </td> 
   <td colname="col2"> <p>When editing CSS classes in the Visual Experience Composer, it is helpful to make the classes easy to identify by using descriptive class names. This helps to ensure that you edit the right CSS classes, and your pages appear as expected. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Don't use the <span class="codeph"> !important </span> CSS property when hiding or removing elements. </p> </td> 
   <td colname="col2"> <p>If the <span class="codeph"> !important </span> CSS property is present, changes made by target.js during delivery will be overridden by the site's CSS rules. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Avoid using HTML tables for page layouts. </p> </td> 
   <td colname="col2"> <p>Target Standard and Premium uses JavaScript to format a page. It is difficult to modify table-based layouts with JavaScript. Also, table-based layouts might not display the same way in all browsers. For best results, use CSS to create page layouts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Minimize the use of iFrames. </p> </td> 
   <td colname="col2"> <p>It is a good practice to minimize the use of iFrames, to simplify page and test management. The visual experience composer can apply some actions within an iFrame, but some actions, such as resizing, do not work properly. It is difficult to manage and resize pages that use multiple iFrames. As a result, testing iFrame-heavy pages can create problems. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attempt to arrange all dynamic DOM modifications as soon after DOM ready as possible. </p> </td> 
   <td colname="col2"> <p>If your modifications fail to apply before the experience application by target.js, content delivery could be broken. This happens only when there is a DOM change in the hierarchy of a targeted element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Use only plain text or an image tag in your anchor elements. </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> &amp;lt;a&amp;gt;Anchor Text&amp;lt;/a&amp;gt; </span> </p> <p>OR </p> <p> <span class="codeph"> &amp;lt;a href=""&amp;gt; &amp;lt;img src=""&amp;gt; &amp;lt;/img&amp;gt; &amp;lt;/a&amp;gt; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Avoid block-level elements inside an inline element. </p> </td> 
   <td colname="col2"> <p>Block-level elements should not be used inside inline elements like anchor, span, and so on. Doing so causes inline elements to lose their height and width, so the overlay tool in Visual Experience Composer might not work as expected. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>When updating offers for classic mboxes, make sure that mbox is created as described at <a href="https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Creating_a_Single_Mbox.html" format="https" scope="external"> Create a Single Mbox </a> in the Target Classic help. </p> </td> 
   <td colname="col2"> <p>If you are considering placing an element or group of elements in an mbox, wrap them in a new div with class <span class="codeph"> mboxDefault </span>: </p> <p> 
     <codeblock>
       &lt;div&nbsp;class="mboxDefault"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;//Content&nbsp;goes&nbsp;here 
      &lt;/div&gt; 
      &lt;script&gt;&nbsp;mboxCreate('mboxName');&nbsp;&lt;/script&gt; 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Don't use the base tag in your website to resolve URLs and links. </p> </td> 
   <td colname="col2"> <p>The Visual Experience Composer manipulates the website behind the scenes, using a proxy server that updated the links. If you add a base tag, the URLs used by the proxy server are resolved again by the browser and appear broken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Using EDIT HTML to manipulate DOM structure can break selectors. </p> </td> 
   <td colname="col2"> <p>For example, if you have taken two actions: </p> <p> 
     <ul id="ul_8DE119C87A6B42BE8CF8097DEF6B32FA"> 
      <li id="li_92AE664EE93342268543D85B3A6DAB86">Added a class to Element 1 </li> 
      <li id="li_2895F928B6D7483D8306DF03AC2B20A7">Edited the HTML for Element 1 </li> 
     </ul> </p> <p>Each change creates a new element in the Visual Experience Composer. Because the second action modifies Element 1, if you delete Element 1, the second action no longer has anything to modify, so the change no longer works. </p> <p>In other words, if you add an element with text, then in a separate action you edit that element with different text, the code editor shows both actions as separate elements. When you edited the element, you created a new element that modifies the original one you created, containing the edited text. If you then delete the original element, the edited text won't be able to find the element that was edited, and will not display. The second element remains in the list of elements, but it does not affect the page because the element it changes no longer exists. </p> <p>See <a href="c_experiences.xml#concept_4EB7663E255F439B8D24079D23479337" format="dita" scope="local"> Element Selectors Used in the Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Use <span class="codeph"> &amp;lt;b&amp;gt; </span> and <span class="codeph"> &amp;lt;i&amp;gt; </span> tags when styling text elements with the rich-text editor. </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7815FC70CE414D9B99969C890DD13480"> 
      <li id="li_BC70FC033E5740C99F40240F1EE344F3"> For bold text, use &lt;b&gt; rather than <span class="codeph"> &amp;lt;strong&amp;gt; </span>. </li> 
      <li id="li_28736D8B774343448C2D30DBE44C4A19">For italic text, use &lt;i&gt; rather than <span class="codeph"> &amp;lt;em&amp;gt; </span>. </li> 
     </ul> </p> <p> <span class="codeph"> &amp;lt;strong&amp;gt; </span> and <span class="codeph"> &amp;lt;em&amp;gt; </span> tags might cause unexpected results. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Be careful when removing form fields. </p> </td> 
   <td colname="col2"> Certain form fields might be mandatory for submission. Removing those form fields could impact submissions. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Do not include <span class="codeph"> mboxCreate </span>inside scripts. </p> </td> 
   <td colname="col2"> <p>Because <span class="codeph"> mboxCreate </span> uses <span class="codeph"> document.write </span>, it is not recommended to include <span class="codeph"> mboxCreate </span> in scripts. Instead, use <span class="codeph"> mboxDefine </span> and <span class="codeph"> mboxUpdate </span> for the same purpose. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Don't update an html snippet using Target Standard if it requires JavaScript code for its initialization. </p> </td> 
   <td colname="col2"> <p>When an action (Edit HTML) is performed on page components (such Sliders, Carousels and so on), delivery might appear broken. The Visual Experience Composer performs the action after the page component has been instantiated by JavaScript. </p> <p>However, when the content of the page is delivered to visitors, the action is applied before instantiation of the component. Because of this, this component's functionality may or may not break at the time of delivery. Functionality depends on the nature of the script used on his page to define the component. </p> <p>If you test for delivery and it works the first time, it is not guaranteed that it will continue working. There may (or may not) be a race condition. </p> <p> 
     <ul id="ul_DFDC45F4AD8B4AFCB473D6D990BF0945"> 
      <li id="li_009ACBF2ABDF4766862E12A598630B99"> If there is a race condition, delivery will work intermittently. </li> 
      <li id="li_C34FC755E9F74E24B0D8517EEF43E792"> If there is no race condition, it will always work. </li> 
     </ul> </p> <p> Test your page multiple times to make sure delivery works as expected. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Don't use a base tag in your website to resolve URLs and links. </p> </td> 
   <td colname="col2"> <p>When you use the Enhanced Experience Composer, the website is manipulated behind the scenes by a proxy server that updates all link urls to make them work in the proxy. If you add a base tag, all these URLs are resolved by the browser so they appear broken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Important text on the site that might be used for targeting should be kept in HTML code within an element. </p> </td> 
   <td colname="col2"> <p>For example, you cannot target Shopping Cart text in the VEC if your code is like the following: </p> 
    <codeblock>
      &lt;a&nbsp;href="http://www.botanicchoice.com/shop.axd/Cart"&gt; 
     &nbsp;&nbsp;&nbsp;&lt;img&nbsp;alt="Shopping&nbsp;Cart"&nbsp;src="/images/ico-cart.gif"&gt;&lt;/img&gt; 
     &nbsp;&nbsp;&nbsp;Shopping&nbsp;Cart: 
     &nbsp;&nbsp;&nbsp;&lt;span&nbsp;id="HeaderCartQtyTotal"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0 
     &nbsp;&nbsp;&nbsp;&lt;/span&gt; 
     &nbsp;&nbsp;&nbsp;Items&nbsp;| 
     &nbsp;&nbsp;&nbsp;&lt;span&nbsp;id="HeaderCartPriceTotal"&gt;&lt;/span&gt; 
     &lt;/a&gt; 
      
    </codeblock> <p> In this example, the entire anchor element is selected in the VEC, which adversely affect other elements if targeting is performed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Don't use <span class="codeph"> <span class="varname"> top </span> </span> or <span class="codeph"> <span class="varname"> self </span> </span> variables in JavaScript code. </p> </td> 
   <td colname="col2"> <p>When the Enhanced Experience Composer is enabled, the value of the <span class="codeph"> <span class="varname"> top </span> </span> and <span class="varname"> self </span> variables are updated to disable iframe busting. Use an X-frame-options header to add iframe busting instead of custom JavaScript codes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Always test your website if parameters are added when loading the page. </p> </td> 
   <td colname="col2"> <p>For example, to open www.abc.com, the following url parameters are used: </p> <p> <span class="codeph"> www.abc.com?mboxEdit=1&amp;amp;mboxDisable=1 </span> </p> <p>These parameters enable editing in an iframe. </p> <p>Make sure your website loads as expected after adding parameters like these. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Make sure your page opens as expected in an iframe. </p> </td> 
   <td colname="col2"> <p>Turn OFF iframe busting techniques on your website and check whether it opens as expected within an iframe on a dummy page. For example: </p> <p> 
     <codeblock>
       &lt;!DOCTYPE&nbsp;html&gt; 
      &lt;html&gt; 
      &lt;head&gt; 
      &nbsp;&nbsp;&lt;meta&nbsp;charset="utf-8"&gt; 
      &nbsp;&nbsp;&lt;meta&nbsp;name="viewport"&nbsp;content="width=device-width"&gt; 
      &nbsp;&nbsp;&lt;title&gt;JS&nbsp;Bin&lt;/title&gt; 
      &lt;/head&gt; 
      &lt;body&gt; 
      &nbsp;&nbsp;&lt;iframe&nbsp;src="http://www.homedepot.com"&lt;/iframe&gt; 
      &lt;/body&gt; 
      &lt;/html&gt; 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Caveats {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

Consider the following caveats when using the Visual Experience Composer to design your activity. 



<table id="table_4DACCF112F914727826B265FE8B792EE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Caveat </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>The Move feature does not support z-index. </p> </td> 
   <td colname="col2"> <p>Because there is no z-index functionality, the moved element can't be moved on top of another element. See <a href="vec-best-pracitces-and-troubleshooting.xml#concept_E284B3F704C04406B174D9050A2528A6/section_F33C2EA27F2E417AA036BC199DD6C721" format="dita" scope="local"> Limitations </a> for more details. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rearranging elements affects click tracking. </p> </td> 
   <td colname="col2"> <p>If an element marked for click tracking is rearranged, the paths of the rearranged elements are changed. As a result, the element in the location where the original element was before it was rearranged is the one whose clicks are tracked. </p> <p> This occurs because both the code to deliver the activity content and the code to track clicks is included in one piece of code that is delivered to the page. If you browse to a different page and set up click tracking, then the activity content code and the click tracking code are delivered to that page. If the click-tracking page has a similar page structure to the page where the test is run, then the test content might also appear on the click-tracking page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inserting an element might not work in a &amp;lt;div&amp;gt; that is an mbox. </p> </td> 
   <td colname="col2"> <p>If an mbox contains an offer, inserting an element may appear as insertBefore and not insertAfter, if the mbox is implemented incorrectly. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>When editing both a parent and child element, edit the parent first. </p> </td> 
   <td colname="col2"> <p>If you swap an image action on an element, then edit the text or HTML on its parent element, delivery issues can occur. The best workflow is to edit the parent element before swapping the image on the child element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cannot select page element that includes an mbox as a child element. </p> </td> 
   <td colname="col2"> <p>For example, if your page contains: </p> <p> 
     <codeblock>
       &lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="mboxDefault"&nbsp;&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&lt;script&gt;mboxCreate('myMbox'); 
      &lt;/div&gt; 
     </codeblock> </p> <p> The outer div should not be selected in an experience because the mbox hardcoded in the page still makes a call to Target and receives a response. This response interferes with the response intended for the larger page element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxy IPs may be blocked in customers environment. </p> </td> 
   <td colname="col2"> <p>If you are using Enhanced Experienced Composer on a non-live site, such as a staging environment, you might see timeouts and access denied errors if your site blocks RIPs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>When adding multiple pages, both the experience rail and page rail are opened at the same time. This eventually decreases the width for the Visual Experience Composer to display the site for optimizations. As a result, reflowable sites might start to appear differently than expected in the reduced space. </p> </td> 
   <td colname="col2"> <p>The workaround is to collapse the experience rail and page rail by clicking the left chevron icons on top. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Limitations {#section_F33C2EA27F2E417AA036BC199DD6C721}



<table id="table_BFCC9711F6A94B56B3A9DDC42270B125"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Limitation </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Move feature </p> </td> 
   <td colname="col2"> <p>An element cannot be moved outside a container that is followed by a CSS property. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Only swap offers are available on mboxes. </p> </td> 
   <td colname="col2"> <p>Actions such as Edit Class and Rearrange are not allowed inside an mbox. Mbox content is served by mbox.js. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>You should not rearrange and move the same element. </p> </td> 
   <td colname="col2"> <p>If an element has been moved to another location, and you select the parent container and try to rearrange the child elements, the moved element is not affected and remains where it is. The rearrangement might not appear as desired. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Swap Image Action does not work on an Image in a carousel. </p> </td> 
   <td colname="col2"> <p>If, for example, your page contains a carousel with six images and you want to swap an image with the second image of the carousel, the Swap Image action won't work. </p> <p>The workaround is to select the parent container and use the Edit HTML action to edit the HTML of the carousel to update the image source of the desired image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Images cannot be resized in an mbox. </p> </td> 
   <td colname="col2"> <p>If you swap an image in an mbox element, then try to resize that image according to the mbox element size, the resizing is not permitted. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>After you swap an image, you cannot select the Edit action. </p> </td> 
   <td colname="col2"> <p>After you swap the image, you cannot edit the Scene7 URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>HTML elements with external source cannot be edited. </p> </td> 
   <td colname="col2"> <p>For example: Video, audio tags, embed, iFrames, frames. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Click tracking does not work for anchor elements that contain anything other than plain text or image tags. </p> </td> 
   <td colname="col2"> <p>For example, click tracking does not work if the element contains JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pages must accept URL parameters for the Visual Experience Composer to work. </p> </td> 
   <td colname="col2"> <p>Some sites strip any URL parameters for their pages. However, the Visual Experience Composer requires those parameters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>While using a script as part of html, any variables and functions that are accessed from outside should be declared under window namespace. </p> </td> 
   <td colname="col2"> <p>The script is executed within the scope of target.js after the page loads. Therefore, any variable or function that is declared locally is not accessible from outside the script block. </p> <p><b>Incorrect:</b> </p> <p> 
     <codeblock>
       &lt;script&gt; 
      &nbsp;&nbsp;var&nbsp;myVar&nbsp;=&nbsp;123; 
      &nbsp;&nbsp;function&nbsp;myFunc()&nbsp;{ 
      &nbsp;&nbsp;&nbsp;&nbsp;// 
      &nbsp;&nbsp;} 
      &lt;/script&gt; 
     </codeblock> </p> <p><b>Correct:</b> </p> <p> 
     <codeblock>
       &lt;script&gt; 
      &nbsp;&nbsp;window.myVar&nbsp;=&nbsp;123; 
      &nbsp;&nbsp;window.myFunc&nbsp;=&nbsp;function()&nbsp;{ 
      &nbsp;&nbsp;&nbsp;&nbsp;// 
      &nbsp;&nbsp;}; 
      &lt;/script&gt; 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inserting an image from the Content library (Scene7) and editing the HTML breaks the image url. </p> </td> 
   <td colname="col2"> <p> 
     <ol id="ol_7578ED0C7C7D4173BFC25D0FEFF0F8C7"> 
      <li id="li_969E12184B144BB8BDC310829B19D7B6">Add an anchor element inside the 'customHeaderMessage' div with some dummy text: <p> 
        <codeblock>
          &lt;a&nbsp;href="#"&gt; 
         &lt;span&gt;&nbsp;Dummy&nbsp;text&nbsp;&lt;/span&gt; 
         &lt;/a&gt; 
        </codeblock> </p> </li> 
      <li id="li_958BF70672364D6AAC5B5624E87C14FF">Select this div using the Insert Element action to insert a image as a sibling of this dummy text div. <p> After image insertion, it looks like : </p> <p> 
        <codeblock>
          &lt;a&nbsp;href="#"&gt;&nbsp; 
         &lt;span&gt;&nbsp;Dummy&nbsp;text&nbsp;&lt;/span&gt; 
         &lt;img&nbsp;src=""&gt;&nbsp;This&nbsp;is&nbsp;inserted&nbsp;Image.&nbsp;&lt;/img&gt; 
         &lt;/a&gt; 
        </codeblock> </p> </li> 
      <li id="li_D4CC0C23497049288B1803BD13593213">Remove the dummy text span. </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>The customCode action in the Visual Experience Composer does not work with Internet Explorer 8. </p> </td> 
   <td colname="col2"> <p>Due to IE8 limitations when handling script content, target.js does not support this in IE8. As a workaround, if the page contains jQuery and is exposed on the <span class="codeph"> window </span> object globally, target.js can use deliver the customCode action. Ensure that <span class="codeph"> window.jQuery </span> and <span class="codeph"> window.jQuery.fn.prepend </span> are defined. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Click tracking is supported only on the page on which experiences are created or on the redirected page. </p> </td> 
   <td colname="col2"> <p>Although Browse mode is available in Click Track VEC, it can't be used to add click tracking on a page. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Troubleshooting the Visual Experience Composer and Enhanced Experience Composer {#reference_77743144F10143A3A89D56E116D296E4}Display problems sometimes occur in the Visual Experience Composer (VEC) and the Enhanced Experience Composer (EEC) under certain conditions. 
<draft-comment otherprops="merge">
  target/r_troubleshoot_composer.xml 
</draft-comment>
<a id="section_557118B08DA04B0D933C2D6548682754"></a>

The VEC is one of the main features of Adobe Target. The VEC is an editor that enables marketers and designers to create and change content using a visual interface. Many design choices can be made without requiring direct editing of the code. Editing HTML and JavaScript is also possible using the editing options available in the composer. 

The EEC is an extension of the VEC that helps you edit an experience for an iframe-busting site or pages that do not yet include the Target implementation. If you have trouble opening your page in the VEC, try the EEC. 

For information about the VEC and the EEC, see [ Experiences ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

## When I try to edit a page, all I see is a spinner instead of my page. (VEC and EEC) {#section_313001039F79446DB28C70D932AF5F58}

This can happen if the URL contains a # character. To fix the issue, switch into Browse mode in the Visual Experience Composer, and then switch back to Compose mode. The spinner should go away and the page should load. 

## Content Security Policy (CSP) headers block the Target libraries on my website. (VEC and EEC) {#section_89A30C7A213D43BFA0822E66B482B803}

If your website's CSP headers block Target libraries, then loads the website but prevents editing, ensure that the Target libraries are not blocked. 

![](../graphics/cps headers.png) 

As a workaround, you can configure a Requestly rule to remove CSP headers, as shown below: 

![](../graphics/cps headers 2.png) 

You can configure a similar Requestly rule for any header that causes a resource to not load inside the VEC. 

## The VEC or EEC appears broken or does not initialize when re-editing a saved activity. (VEC and EEC) {#section_5AC3BA8F8FBB451EA814F298D0645E54}

If the website has changed outside of the Visual Experience Composer after the experience was defined, selectors on which actions were taken earlier cannot be found when the activity is opened for re-editing. The page appears broken, and no warning displays. 

## The VEC or EEC does not show my rotating banners and other content containing JavaScript. (VEC and EEC) {#section_8B5BE6EB050B42D6A14A054724C41330}

By default, the Visual Experience Composer blocks JavaScript elements. You can work with these elements if you disable JavaScript in the Visual Experience Composer settings. Depending on how the site is set up, some items might continue to display incorrectly or to remain unavailable. 

## My hosted target.js file fails to load on subsequent page reloads. (VEC and EEC) {#section_87F6418C2CD142A7B4D1E7037935F81F}

This issue happens when customers have an ` mbox.js` version earlier than 57 (i.e. version 56 or earlier). 

We recommend that all VEC users upgrade to the [ latest version of ` mbox.js` ](t_mbox_download.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A), or at least upgrade to version 57. You might also consider [ making the transition to ` at.js` ](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17). 

## When I change one element on the page, multiple elements change. (VEC and EEC) {#section_309188ACF34942989BE473F63C5710AF}

If the same DOM element ID is used on multiple elements on the page, changing one of those elements changes all elements with that ID. To prevent this from happening, an ID should be used only once on each page. This is a standard HTML best practice. For more information, see [ Page Modification Scenarios ](vec-best-pracitces-and-troubleshooting.md#concept_A458A95F65B4401588016683FB1694DB). 

## I can't edit experiences for an iFrame-busting site. (VEC and EEC) {#section_9FE266B964314F2EB75604B4D7047200}

This issue can be addressed by enabling the Enhanced Experience Composer. Click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Preferences] **, then select the check box that enables the Enhanced Experience Composer. The Enhanced Experience Composer uses an Adobe-managed proxy to load your page for editing. This allows editing on iFrame-busting sites and allows editing on sites and pages where you have not yet added Adobe Target code. The activities do not deliver to the site until the code has been added. Some sites may not load via the Enhanced Experience Composer, in which case you can uncheck this option to load the Visual Experience Composer via an iFrame. [] 


>[!NOTE]
>
>Your locally hosted pages or pages that are not accessible outside your network are not accessible to the Adobe proxy server and cannot be opened in the EEC. These pages might include staging URLs, User Acceptance Testing (UAT) URLs, or locally hosted pages.



## I want to set up tests on pages that don't have the mbox/target implementation done yet. (VEC and EEC) {#section_DE63BCCB5B124E10A71FA579B582A80A}

See "I can't edit experiences for an iFrame-bursting site" above. 

## Bold and italic text styles with Edit Text/HTML or Change text/HTML do not show on my page. Sometimes the text disappears after applying these style changes. (VEC and EEC) {#section_7A71D6DF41084C58B34C18701E8774E5}

If you use ** [!UICONTROL  Edit Text/HTML] ** in the Visual Experience Composer for A/B or Experience Targeting activities or ** [!UICONTROL  Change Text/HTML] ** for Automated Personalization or Multivariate Test activities to make text bold or italic, those styles might not be applied on the page or the text disappears from the page in the Visual Experience Composer. This is because the way the rich-text editor applies these styles might interfere with the website markup. 

If you see this issue: 


1. Click the ** [!UICONTROL  HTML] ** button in the rich-text editor to enter source editing mode.
1. Find the styles text elements. 
    * For bold text, change ` &amp;lt;strong&amp;gt;` elements to ` &amp;lt;b&amp;gt;`.
    * For italic text, change ` &amp;lt;em&amp;gt;` elements to ` &amp;lt;i&amp;gt;`.




## For Automated Personalization activities, image swapping appears broken in the VEC or EEC. (VEC and EEC) {#section_88AABFDFE6A3420299B0D508B12A3994}

Adding an image offer to a location takes the full dimension of the original image space in the VEC or EEC. On delivery, the image is not expanded and is shown as it is, so there is no impact on delivery. 

## When I open my website in the Visual Experience Composer, the Target libraries do not load. (VEC only) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

Target adds two parameters ( ` mboxEdit=1` and ` mboxDisable=1`) while opening the website in the Visual Experience Composer. 

If your website (specially Single Page Apps), trims our parameters or actually removes them while navigating from one page to another (without a page reload) the Target functionality breaks and the Target libraries do not load. 
To avoid this problem, ensure that you do not trim or remove these two parameters. 
## My page won't open in the EEC, or loads slowly. Activities or experiences load slowly in the VEC. (VEC only) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Several issues can affect page performance in the Target experience composers. Some common issues include: 


* You do not have an mbox on the page.
* Your site uses proxy blocking, which does not allow the page to be opened in either experience composer.
* Your site doesn't allow itself to be opened in an iFrame.


If issues occur in the Enhanced Experience Composer, try turning off the Enhanced Experience Composer and use the Visual Experience Composer instead. 

To disable the Enhanced Experience Composer, go to ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Preferences] ** and turn off the ** [!UICONTROL  Enable Enhanced Experience Composer] ** option. 

Some users see the following error message in the console: 

![](../graphics/error message.jpg) 

If neither the Visual Experience Composer nor the Enhanced Experience Composer works, use a browser extension like Requestly (Chrome or Firefox) or Modify Response Headers (Firefox) that can overwrite the X-Frames header options for your site and allow them to be loaded in iFrames, enabling the VEC. If you are unable to use browser extensions, use the Form Composer. 

**To use the Requestly extension on Chrome or Firefox: ** 


1. Turn off the Enhanced Experienced Composer. 

1. Install the Requestly browser extension on Chrome or Firefox. 

1. Open the extension and configure it using the following: 

1. Select ** [!UICONTROL  Modify headers] **. 

1. Enter the following: 

    * Rule name 

    * Modification rules 
    
        * Toggle ** [!UICONTROL  Add] ** to ** [!UICONTROL  Remove] **. 

        * Toggle ** [!UICONTROL  Request] ** to ** [!UICONTROL  Response] **. 

        * Enter "X-Frame-Options" as the header name. 

        * Repeat previous steps and enter "x-frame-options" as the header name. 


          >[!NOTE]
          >
          >Headers that are manipulated via Requestly are case sensitive.


        * Change ** [!UICONTROL  Equals] ** to ** [!UICONTROL  Contains] ** as the condition for the source URL and enter the URL of the activity that you are trying to load in the VEC. 

      ![](../graphics/chrome extension.png) 


1. Click ** [!UICONTROL  Save] **. 

   ![](graphics/requestly.png) 

   You should now be able to load the page quickly with the Visual Experience Composer. 



**To use the Modify Response Headers extension on Firefox: ** 


1. Install the Modify Response Headers on Firefox and restart the browser. 

1. From your Firefox extensions, select the Modify Response Headers extension. 

1. Click ** [!UICONTROL  Preferences] **. 

1. Select ** [!UICONTROL  Filter] ** from the Action drop down. 

1. In the Header Name field, enter: ** [!UICONTROL  X-Frame-Options] **. 

1. Repeat Steps 4 and 5 to add a filter with ** [!UICONTROL  x-frame-options] **. 

1. Click ** [!UICONTROL  Add] **. 

1. Click ** [!UICONTROL  Start] **. 



![](../graphics/firefox extension.png) 

After setting up an extension, open Target. Your pages should now load in the Visual Experience Composer, even if the Enhanced Experience Composer is disabled. 

## My page does not display in the VEC (VEC only) {#section_87B3BEA4B6174CFDA6C9A69A1A051FA1}


* The browser is not supported.
* The browser is blocking a non-secure page on a secure site. Click the icon to the left of the URL in the browser address bar and click ** [!UICONTROL  Disable protection on this page] ** 

* You entered an invalid URL.
* You have not entered a default URL in your account setup page.

## When launching a URL for a VEC activity, the console displays the following error message: "Uncaught ReferenceError:_AT is not defined." (VEC only) {#section_BB5B9B629AC4452496A82943EFF72B85}

This error occurs if you try to deliver Visual Experience Composer (VEC) campaigns and you have not updated ` mbox.js` downloaded from the Target user interface with the [!UICONTROL  Support Visual Experience Composer Activities] option enabled ( [!UICONTROL  Setup] > [!UICONTROL  Implementation] > [!UICONTROL  mbox.js] > [!UICONTROL  Edit mbox.js Settings]). 

Ensure that this setting is enabled, then download and update ` mbox.js` on your website. 

## The VEC appears broken when I use browse mode. (VEC only) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

While using browse mode, if you access a URL that does not have target.js or contains a frame-buster header, the Visual Experience Composer appears broken. Due to browser security concerns, Target cannot access the URL you navigated to. 

## The EEC won't load an internal QA URL that is not accessible on public IP. (EEC only) {#section_D29E96911D5C401889B5EACE267F13CF}

This can be resolved by whitelisting the following IP addresses. These IP addresses are for Adobe's server used for the Enhanced Experience Composer proxy. They are only required for activity editing. Visitors to your site do not need these IP addresses whitelisted. 



<table id="table_F4AD035AA688465AB46A845089442A26"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Region </th> 
   <th colname="col2" class="entry"> IP Addresses </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>United States </p> </td> 
   <td colname="col2"> <p>52.55.99.45 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe, Middle East, and Africa (EMEA) </p> </td> 
   <td colname="col2"> <p>52.51.238.221 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Asia-Pacific (APAC) </p> </td> 
   <td colname="col2"> <p>52.193.67.35 </p> </td> 
  </tr> 
 </tbody> 
</table>

You might see the following error message in Target: 

` Error: Your website domain (ISP) is blocking the Enhanced Experience Composer. You can whitelist the Enhanced Experience Composer's IP addresses or turn off Enhanced Experience Composer in [!UICONTROL  Configure] > [!UICONTROL  Page Delivery] menu.` 

![](../graphics/EEC_error.png) 

The following are reasons that you might see this error message and remedies to fix the situation: 


* **Issue: **Your website domain (ISP) is blocking the Enhanced Experience Composer. 

  **Remedy: **Whitelist the IP addresses listed above. 

* **Issue: **The IP addresses are whitelisted but your website does not support TLS version 1.0. Target currently uses the default configuration of 1.0. 

  **Solution: **See the following question (The Enhanced Visual Experience Composer won't load on secure pages on my site that use TLS 1.2). 



## The EEC won't load on secure pages on my site that use TLS 1.2. (EEC only) {#section_C5B31E3D32A844F68E5A8153BD17551F}

You might see the error message described above in "The Enhanced Visual Experience Composer won't load on secure pages on my site." if the above IP addresses are whitelisted but your website does not support TLS version 1.0. Target currently uses the default configuration of 1.0. 

To check the TLS version on your website using Firefox (other browsers have similar steps): 


1. Open the affected website in Firefox. 

1. Click the ** [!UICONTROL  Show Site Information] ** icon on the browser's address bar. 

   ![](../graphics/firefox more info.png) 

1. Click ** [!UICONTROL  Show Connection Details] ** > ** [!UICONTROL  More Information] **. 

   ![](../graphics/firefox more info 2.png) 

1. Examine the TLS version information under Technical Details: 

   ![](../graphics/firefox more info 3.png) 

1. To remedy this situation, reach out to [ Customer Care ](r_release_notes.md#reference_ACA3391A00EF467B87930A450050077C) for configuration with your TLS version and the domain. 



## I'm seeing timeouts or "access denied" errors when loading sites with proxy enabled. (EEC only) {#section_60CBB9022DC449F593606C0E6252302D}

Make sure proxy IPs are not blocked in your environment. 
>## Enabling Mixed Content in Your Browser {#concept_46D022D50280468C9EF6D5DF6EFC911C}Some browsers block the display of a page if secure content is mixed with insecure content. 
<draft-comment otherprops="merge">
  target/c_mixed_content.xml 
</draft-comment>If the Visual Experience Composer (VEC) tries to open a page containing mixed (secure and insecure) content, a message displays showing how to disable blocking in your browser so you can open an HTTP site or a site that has mixed calls (HTTPS and HTTP). 

![](../graphics/mixed content warning.gif) 

Previously, when mixed content was not allowed, you could still perform some actions in Step 1 of the three-step guided workflow when creating activities. Target now blocks actions in Step 1. When this message displays, you must enable mixed content before continuing. 

Your browser's security settings might block mixed content or insecure (HTTP) content being loaded into a secure (HTTPS) page or frame (such as the VEC). If you don't want to disable your browser's security settings, you need to have an HTTPS website. 

If you website is running on an insecure (HTTP) domain, you are required to allow the VEC to load active mixed content. 


>[!NOTE]
>
>Allowing mixed content affects the VEC only and not your live website.



For more information, see [ Mixed Content ](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) on the *Mozilla Developer Network* (MDN) website. 
>## Enabling Mixed Content in Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}By default, Firebox blocks pages that mix secure and insecure content. It is recommended that you permanently change this setting to use 
<keyword>
  Target 
</keyword>. 
<draft-comment otherprops="merge">
  target/t_mixed_content_firefox.xml 
</draft-comment>
>1. In Firefox, enter ` about:config` in the address bar.
>1. Acknowledge the warning message displayed by Firefox.
>1. In the search bar, type ` block_active`.
>1. Double-click ` ** [!UICONTROL  security.mixed_content.block_active_content] **` .

>## Enabling Mixed Content in Internet Explorer {#task_59E7D13C04DF486C92CD78D0C63DDDE8}By default, Internet Explorer blocks pages that mix secure and insecure content. It is recommended that you permanently change this setting to use Target Standard. 
<draft-comment otherprops="merge">
  target/t_mixed_content_ie.xml 
</draft-comment>
>1. In Internet Explorer, click the settings icon > ** [!UICONTROL  Internet Options] **.
>1. Open the [!UICONTROL  Security] tab.
>1. Select ** [!UICONTROL  Internet] **, then click ** [!UICONTROL  Custom Level] **.
>1. Select ** [!UICONTROL  Miscellaneous] **.
>1. Under [!UICONTROL  Miscellaneous], enable ** [!UICONTROL  Display Mixed Content] **.
>1. Click  ** [!UICONTROL  OK] ** > ** [!UICONTROL  Yes] ** > ** [!UICONTROL  Apply] ** .
>## Enabling Mixed Content in Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}If you're visiting a site via a secure connection, Google Chrome will verify that the content on the web page has been transmitted safely. 
<draft-comment otherprops="merge">
  target/t_mixed_content_chrome.xml 
</draft-comment>See [ This page has insecure content ](https://support.google.com/chrome/answer/1342714?hl=en) in Google Chrome Help. 
>## Page Modification Scenarios {#concept_A458A95F65B4401588016683FB1694DB}The scenarios in this topic show how changes made to your page affect Target's ability to display an experience. 
<draft-comment otherprops="merge">
  target/c_vec_scenarios.xml 
</draft-comment>The Target selector determines where to display an experience. If a page is modified outside of Target, the changes might affect the ability of Target to display the experience. 

When using the selector, the unique class is not equivalent to the ID. The selector always works with a unique class. If no class is assigned to the element, the selector calculates the number of previous siblings which have the same tag name. 


>[!NOTE]
>
>Although these scenarios use list items as examples, the concepts apply to any element.



## Scenario: Insert an element with a different class name before the selected element {#section_298F661F72384F6AB957D5885A99D822}

In this example, a new element is inserted as a sibling of the element in the Target selector. 

There is a possibility that first class present on the element might be added by JavaScript. In that case, delivery fails and the action is not applied. 

**Inserted element:** 


```
&amp;lt;li&amp;nbsp;class="kids-section"&amp;gt;Kids&amp;lt;/li&amp;gt;
```


**Selected:** 

` &amp;lt;li class="women-section"&amp;gt;Women&amp;lt;/li&amp;gt;` 

Selector: ` #wrap &amp;gt; ul.nav:eq(0) &amp;gt; li.women-section:eq(0)` 

**Result:** 

The selector works as expected because ` li.women-section:eq(0)` is not affected. 



<table id="table_F37367FB9CB343D497B5C58E8AA1B015"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Before </th> 
   <th colname="col2" class="entry"> After </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     &nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;&nbsp;Men&lt;/li&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     &lt;/div&gt; 
    </codeblock> </td> 
   <td colname="col2"> <p> 
     <codeblock>
       &lt;div&nbsp;id="wrap"&gt; 
      &nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
      <b>&amp;lt;li&amp;nbsp;class="kids-section"&amp;gt;Kids&amp;lt;/li&amp;gt;</b> 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;&nbsp;Men&lt;/li&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
      &lt;/div&gt; 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Scenario: Insert an element with the same class name as the selected element {#section_0969B88C2F154E648D9969C8C85EF55A}

In this scenario, an attempt is made to insert a list when an item in a list is selected. 

**Inserted element:** 


```
<ul class="nav"> 
   <li class="item"> Sale </li> 
   <li> class="item"> Offers </li> 
</ul>
```


**Selected** 

` &amp;lt;li class="women-section"&amp;gt;Women&amp;lt;/li&amp;gt;` 

Selector: ` #wrap &amp;gt; ul.nav:eq(0) &amp;gt; li.women-section:eq(0)` 

**Result:** 

The selector does not work, because ` ul.nav:eq(0)` provides a dynamically added element. The element won't be available and the action is not applied. When a similar list item with same class is added dynamically or manually after an activity has been created, a new element at the first position is created. This breaks the selector. 



|  Before  | After (Attempted)  |
|---|---|
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men-section"> Men</li> 
      <li class="women-section">Women</li> 
   </ul> 
</div>
```
| 
```
<div id="wrap"> 
    
<b><ul class="nav"> 
       <li class="item"> Sale</li> 
       <li> class="item"> Offers</li> 
    </ul></b> 
   <ul class="nav"> 
      <li class="men-section"> Men</li> 
      <li class="women-section">Women</li> 
   </ul> 
</div>
```
|


## Scenario: Insert an element after the selected element {#section_15B07B84BEE94ED39D85BBBE0733E170}

In this scenario, a list item is inserted after the selected element. 

**Inserted element:** 


```
<ul class="nav"> 
   <li class="men-section"> Men Clothes</li> 
   <li class="women-section"> Women Clothes</li> 
</ul>
```


**Selected:** 

` &amp;lt;li class="women-section"&amp;gt;Women Shoes&amp;lt;/li&amp;gt;` 

Selector: ` #wrap &amp;gt; ul.nav:eq(0) &amp;gt; li.women-section:eq(0)` 

**Result:** 

In this case, inserting a list after the list ending with the selected list item works as expected. The new element is added to the same position as the selected element relative to the parent element. 



|  Before  | After  |
|---|---|
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men">Men Shoes </li> 
      <li class="women">Women Shoes</li> 
   </ul> 
</div>
```
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men">Men Shoes </li> 
      <li class="women">Women Shoes</li> 
   </ul> 
    
<b><ul class="nav"> 
       <li class="men-section">Men Clothes</li> 
       <li class="women-section"> Women Clothes</li> 
    </ul></b> 
</div>
```
|


## Scenario: Remove the element immediately preceding another element {#section_F193674F04F84AA593EAA1137C880EBA}

In this scenario, the list item before the selected element is deleted. 

**Removed element:** 


```
&amp;lt;li&amp;nbsp;class="men-section"&amp;gt;&amp;nbsp;Men&amp;nbsp;&amp;lt;/li&amp;gt;
```


**Selected:** 

` &amp;lt;li class="women-section"&amp;gt;Women&amp;lt;/li&amp;gt;` 

Selector: ` #wrap &amp;gt; ul.nav:eq(0) &amp;gt; li.women-section:eq(0)` 

**Result:** 

The element is successfully removed because the class of the selected item is not altered. 



|  Before  | After  |
|---|---|
| 
```
<div id="wrap"> 
   <ul class="nav"> 
       
<b>&amp;lt;li&amp;nbsp;class="men-section"&amp;gt;Men&amp;lt;/li&amp;gt;</b> 
      <li class="women-section">Women</li> 
   </ul> 
</div>
```
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="women-section">Women</li> 
   </ul> 
</div>
```
|


## Scenario: Remove the element immediately following another element {#section_F83B51BE54924FB58679D512DAF1EBB2}

In this scenario, the list item after the selected element is deleted. 

**Removed element:** 


```
&amp;lt;li&amp;nbsp;class="kids-section"&amp;gt;Kids&amp;lt;/li&amp;gt;
```


**Selected:** 

` &amp;lt;li class="women-section"&amp;gt;Women&amp;lt;/li&amp;gt;` 

Selector: ` #wrap &amp;gt; ul.nav:eq(0) &amp;gt; li.women-section:eq(0)` 

**Result:** 

The element is successfully removed because the class of the selected item is not altered. The removed element includes a unique class within its parent subtree. 



|  Before  | After  |
|---|---|
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men-section">Men</li> 
      <li class="women-section">Women</li> 
       
<b>&amp;lt;li&amp;nbsp;class="kids-section"&amp;gt;Women&amp;lt;/li&amp;gt;</b> 
   </ul> 
</div>
```
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men-section">Men</li> 
      <li class="women-section">Women</li> 
   </ul> 
</div>
```
|


## Scenario: Remove the selected element {#section_1989CF1E2C344CC5963084ED83C18F9C}

In this scenario, the selected list item is deleted. 

**Removed element:** 


```
&amp;lt;li&amp;nbsp;class="women-shoes"&amp;gt;Women&amp;lt;/li&amp;gt;
```


**Selected:** 

` &amp;lt;li class="women-shoes"&amp;gt;Women&amp;lt;/li&amp;gt;` 

Selector: ` #wrap &amp;gt; ul.nav:eq(0) &amp;gt; li.women-section:eq(0)` 

**Result:** 

The element is successfully removed. 



|  Before  | After  |
|---|---|
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men-section">Men</li> 
      <li class="women-shoes">Women</li> 
   </ul> 
</div>
```
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men-section">Men</li> 
   </ul> 
</div>
```
|


## Scenario: Rename the class of the selected element {#section_79D244C588BA452DB8E433D82B7F63EA}

In this scenario, the class of the selected list item is changed. 

**Changed element:** 


```
&amp;lt;li&amp;nbsp;class="women-section"&amp;gt;Women&amp;lt;/li&amp;gt;
```


**Selected:** 

` &amp;lt;li class="women-section"&amp;gt;Women&amp;lt;/li&amp;gt;` 

Selector: ` #wrap &amp;gt; ul.nav:eq(0) &amp;gt; li.women-section:eq(0)` 

**Result:** 

The element class cannot be renamed because ` class` is not found. 



|  Before  | After (Attempted)  |
|---|---|
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men-section">Men</li> 
       
<b>&amp;lt;li&amp;nbsp;class="women-section"&amp;gt;Women&amp;lt;/li&amp;gt;</b> 
   </ul> 
</div>
```
| 
```
<div id="wrap"> 
   <ul class="nav"> 
      <li class="men-section">Men</li> 
       
<b>&amp;lt;li&amp;nbsp;class="women-shoes"&amp;gt;Women&amp;lt;/li&amp;gt;</b> 
   </ul> 
</div>
```
|

