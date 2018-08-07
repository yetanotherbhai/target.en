---
description: Following best practices can help make your experiences work as expected. There are also other tips and limitations that you should be aware of.
keywords: Recommendations
seo-description: Following best practices can help make your experiences work as expected. There are also other tips and limitations that you should be aware of.
seo-title: Visual Experience Composer Best Practices and Limitations
solution: Target
title: Visual Experience Composer Best Practices and Limitations
topic: Premium
uuid: 973c572a-4c30-422a-9d2c-5bf6db68e1b1
index: y
internal: n
snippet: y
translate: y
---

# Visual Experience Composer Best Practices and Limitations

By following these best practices, you are less likely to encounter unexpected problems with the experiences you design.

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
   <td colname="col1"> For mbox.js version 57 and later, and for at.js, place the mbox.js or at.js reference at the top of the &lt;head&gt; section of your page. </td> 
   <td colname="col2"> If you also use the Visitor API Service, place the visitor API script above mbox.js or at.js. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> For versions of mbox.js before version 57, place the mbox.js code as low as possible in the &lt;head&gt; section of your page. </td> 
   <td colname="col2"> Place the mbox.js at the end of the &lt;head&gt; section, with no additional declarations after it. Otherwise, any script or link tags will be moved into the &lt;body&gt; section. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Use unique IDs for top-level elements and any other elements that could be good testing/targeting candidates. </td> 
   <td colname="col2"> <p>Anything immediately inside the body element should have a unique ID. If new elements are injected into the body and code moves around, at least the parent elements have an easier way to be recognized.</p> <p>Adobe Target does not require IDs, but using IDs increases the reliability of experiences created with the experience composer. Target uses CSS selectors to modify your content when the experience is delivered. When you edit an experience, the Visual Experience Composer anchors the selector to the closest ancestor with a non-null id attribute to the HTML element being modified. It is, therefore, not advisable to use any mechanism, including JavaScript libraries, that sets or modifies HTML ID attributes. Although those IDs might be available to the Target experience composer for activity creation, if JavaScript modifies IDs, the ID that was used when the experience was created might not be available when the experience runs. If an ID is not available, the selector anchored to the ID fails.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Name CSS classes so they are easily identifiable. </td> 
   <td colname="col2"> When editing CSS classes in the Visual Experience Composer, it is helpful to make the classes easy to identify by using descriptive class names. This helps to ensure that you edit the right CSS classes, and your pages appear as expected. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Don't use the <span class="codeph"> !important </span> CSS property when hiding or removing elements. </td> 
   <td colname="col2"> If the <span class="codeph"> !important </span> CSS property is present, changes made by target.js during delivery will be overridden by the site's CSS rules. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Avoid using HTML tables for page layouts. </td> 
   <td colname="col2"> Target Standard and Premium uses JavaScript to format a page. It is difficult to modify table-based layouts with JavaScript. Also, table-based layouts might not display the same way in all browsers. For best results, use CSS to create page layouts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Minimize the use of iFrames. </td> 
   <td colname="col2"> It is a good practice to minimize the use of iFrames, to simplify page and test management. The visual experience composer can apply some actions within an iFrame, but some actions, such as resizing, do not work properly. It is difficult to manage and resize pages that use multiple iFrames. As a result, testing iFrame-heavy pages can create problems. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Attempt to arrange all dynamic DOM modifications as soon after DOM ready as possible. </td> 
   <td colname="col2"> If your modifications fail to apply before the experience application by target.js, content delivery could be broken. This happens only when there is a DOM change in the hierarchy of a targeted element. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Use only plain text or an image tag in your anchor elements. </td> 
   <td colname="col2"> <p> <span class="codeph"> &lt;a&gt;Anchor Text&lt;/a&gt; </span> </p> <p>OR</p> <p> <span class="codeph"> &lt;a href=""&gt; &lt;img src=""&gt; &lt;/img&gt; &lt;/a&gt; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Avoid block-level elements inside an inline element. </td> 
   <td colname="col2"> Block-level elements should not be used inside inline elements like anchor, span, and so on. Doing so causes inline elements to lose their height and width, so the overlay tool in Visual Experience Composer might not work as expected. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> When updating offers for classic mboxes, make sure that mbox is created as described at <a href="https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Creating_a_Single_Mbox.html" format="https" scope="external"> Create a Single Mbox </a> in the Target Classic help. </td> 
   <td colname="col2"> If you are considering placing an element or group of elements in an mbox, wrap them in a new div with class <span class="codeph"> mboxDefault </span>: <p> 
     <codeblock>
       &lt;div&nbsp;class="mboxDefault"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;//Content&nbsp;goes&nbsp;here 
      &lt;/div&gt; 
      &lt;script&gt;&nbsp;mboxCreate('mboxName');&nbsp;&lt;/script&gt; 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Don't use the base tag in your website to resolve URLs and links. </td> 
   <td colname="col2"> The Visual Experience Composer manipulates the website behind the scenes, using a proxy server that updated the links. If you add a base tag, the URLs used by the proxy server are resolved again by the browser and appear broken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Using EDIT HTML to manipulate DOM structure can break selectors. </td> 
   <td colname="col2"> <p>For example, if you have taken two actions:</p> <p> 
     <ul id="ul_8DE119C87A6B42BE8CF8097DEF6B32FA"> 
      <li id="li_92AE664EE93342268543D85B3A6DAB86">Added a class to Element 1</li> 
      <li id="li_2895F928B6D7483D8306DF03AC2B20A7">Edited the HTML for Element 1</li> 
     </ul> </p> <p>Each change creates a new element in the Visual Experience Composer. Because the second action modifies Element 1, if you delete Element 1, the second action no longer has anything to modify, so the change no longer works.</p> <p>In other words, if you add an element with text, then in a separate action you edit that element with different text, the code editor shows both actions as separate elements. When you edited the element, you created a new element that modifies the original one you created, containing the edited text. If you then delete the original element, the edited text won't be able to find the element that was edited, and will not display. The second element remains in the list of elements, but it does not affect the page because the element it changes no longer exists.</p> <p>See <a href="c_vec_selectors.xml#concept_4EB7663E255F439B8D24079D23479337" format="dita" scope="local"> Element Selectors Used in the Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Use <span class="codeph"> &lt;b&gt; </span> and <span class="codeph"> &lt;i&gt; </span> tags when styling text elements with the rich-text editor. </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7815FC70CE414D9B99969C890DD13480"> 
      <li id="li_BC70FC033E5740C99F40240F1EE344F3"> For bold text, use &lt;b&gt; rather than <span class="codeph"> &lt;strong&gt; </span>. </li> 
      <li id="li_28736D8B774343448C2D30DBE44C4A19">For italic text, use &lt;i&gt; rather than <span class="codeph"> &lt;em&gt; </span>. </li> 
     </ul> </p> <p> <span class="codeph"> &lt;strong&gt; </span> and <span class="codeph"> &lt;em&gt; </span> tags might cause unexpected results. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Be careful when removing form fields. </td> 
   <td colname="col2"> Certain form fields might be mandatory for submission. Removing those form fields could impact submissions. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Do not include <span class="codeph"> mboxCreate </span>inside scripts. </p> </td> 
   <td colname="col2"> <p>Because <span class="codeph"> mboxCreate </span> uses <span class="codeph"> document.write </span>, it is not recommended to include <span class="codeph"> mboxCreate </span> in scripts. Instead, use <span class="codeph"> mboxDefine </span> and <span class="codeph"> mboxUpdate </span> for the same purpose. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Don't update an html snippet using Target Standard if it requires JavaScript code for its initialization. </td> 
   <td colname="col2"> Updated html, for example for sliders or carousels which when delivered appears broken as JS code is not invoked which initializes it or is invoked before we change such html snippet using target.js </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Don't use a base tag in your website to resolve urls and links. </td> 
   <td colname="col2"> When you use the Enhanced Experience Composer, the website is manipulated behind the scenes by a proxy server that updates all link urls to make them work in the proxy. If you add a base tag, all these urls are resolved by the browser so they appear broken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Important text on the site that might be used for targeting should be kept in HTML code within an element. </td> 
   <td colname="col2"> <p>For example, you cannot target Shopping Cart text in the VEC if your code is like the following:</p> <p> 
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
       
     </codeblock> In this example, the entire anchor element is selected in the VEC, which adversely affect other elements if targeting is performed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Don't use <span class="codeph"> <span class="varname"> top </span> </span> or <span class="codeph"> <span class="varname"> self </span> </span> variables in JavaScript code. </td> 
   <td colname="col2"> <p>When the Enhanced Experience Composer is enabled, the value of the <span class="codeph"> <span class="varname"> top </span> </span> and <span class="varname"> self </span> variables are updated to disable iframe busting. Use an X-frame-options header toadd iframe busting instead of custom JavaScript codes.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Always test your website if parameters are added when loading the page. </td> 
   <td colname="col2"> <p>For example, to open www.abc.com, the following url parameters are used:</p> <p> <span class="codeph"> www.abc.com?mboxEdit=1&amp;mboxDisable=1 </span></p> <p>These parameters enable editing in an iframe.</p> <p>Make sure your website loads as expectedafter adding parameters like these.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Make sure your page opens as expected in an iframe. </td> 
   <td colname="col2"> <p>Turn OFF iframe busting techniques on your website and check whether itopens as expected within an iframe on a dummy page. For example:</p> <p> 
     <codeblock></codeblock></p> </td> 
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
   <td colname="col1"> The Move feature does not support z-index. </td> 
   <td colname="col2"> Because there is no z-index functionality, the moved element can't be moved on top of another element. See <a href="c_experience_composer_best_practices.xml#concept_E284B3F704C04406B174D9050A2528A6/section_F33C2EA27F2E417AA036BC199DD6C721" format="dita" scope="local"> Limitations </a> for more details. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rearranging elements affects click tracking. </td> 
   <td colname="col2"> <p>If an element marked for click tracking is rearranged, the paths of the rearranged elements are changed. As a result, the element in the location where the original element was before it was rearranged is the one whose clicks are tracked.</p> <p>This occurs because both the code to deliver the activity content and the code to track clicks is included in one piece of code that is delivered to the page. If you browse to a different page and set up click tracking, then the activity content code and the click tracking code are delivered to that page. If the click-tracking page has a similar page structure to the page where the test is run, then the test content might also appear on the click-tracking page.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>When editing both a parent and child element, edit the parent first.</p> </td> 
   <td colname="col2"> <p>If you swap an image action on an element, then edit the text or HTML on its parent element, delivery issues can occur. The best workflow is to edit the parent element before swapping the image on the child element.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Cannot select page element that includes an mbox as a child element. </td> 
   <td colname="col2"> <p>For example, if your page contains:</p> <p> 
     <codeblock>
       &lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="mboxDefault"&nbsp;&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&lt;script&gt;mboxCreate('myMbox'); 
      &lt;/div&gt; 
     </codeblock> </p> <p>The outer div should not be selected in an experience because the mbox hardcoded in the page still makes a call to Target and receives a response. This response interferes with the response intended for the larger page element.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxy IPs may be blocked in customers environment </td> 
   <td colname="col2"> If you are using Enhanced Experienced Composer on a non-live site, such as a staging environment, you might see timeouts and access denied errors if your site blocks RIPs. </td> 
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
   <td colname="col1"> Move feature </td> 
   <td colname="col2"> An element cannot be moved outside a container that is followed by a CSS property. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Only swap offers are available on mboxes. </td> 
   <td colname="col2"> Actions such as Edit Class and Rearrange are not allowed inside an mbox. Mbox content is served by mbox.js. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> You should not rearrange and move the same element. </td> 
   <td colname="col2"> <p>If an element has been moved to another location, and you select the parent container and try to rearrange the child elements, the moved element is not affected and remains where it is. The rearrangement might not appear as desired.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Images cannot be resized in an mbox. </td> 
   <td colname="col2"> <p>If you swap an image in an mbox element, then try to resize that image according to the mbox element size, the resizing is not permitted.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> After you swap an image, you cannot select the Edit action. </td> 
   <td colname="col2"> After you swap the image, you cannot edit the Scene7 URL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> HTML elements with external source cannot be edited. </td> 
   <td colname="col2"> For example: Video, audio tags, embed, iFrames, frames. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Click tracking does not work for anchor elements that contain anything other than plain text or image tags. </td> 
   <td colname="col2"> For example, click tracking does not work if the element contains JavaScript. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pages must accept URL parameters for the Visual Experience Composer to work. </td> 
   <td colname="col2"> Some sites strip any URL parameters for their pages. However, the Visual Experience Composer requires those parameters. </td> 
  </tr> 
 </tbody> 
</table>

