---
description: Display problems sometimes occur in the Visual Experience Composer (VEC) and the Enhanced Experience Composer (EEC) under certain conditions.
keywords: Recommendations
seo-description: Display problems sometimes occur in the Visual Experience Composer (VEC) and the Enhanced Experience Composer (EEC) under certain conditions.
seo-title: Troubleshooting the Visual Experience Composer and Enhanced Experience Composer
solution: Target
title: Troubleshooting the Visual Experience Composer and Enhanced Experience Composer
topic: Premium
uuid: 91703dee-d6a4-4ae4-b622-65081e2b0e01
index: y
internal: n
snippet: y
translate: y
---

# Troubleshooting the Visual Experience Composer and Enhanced Experience Composer

## Troubleshooting the Visual Experience Composer and Enhanced Experience Composer {#reference_77743144F10143A3A89D56E116D296E4}Display problems sometimes occur in the Visual Experience Composer (VEC) and the Enhanced Experience Composer (EEC) under certain conditions.
<a id="section_557118B08DA04B0D933C2D6548682754"></a>

The VEC is one of the main features of Adobe Target. The VEC is an editor that enables marketers and designers to create and change content using a visual interface. Many design choices can be made without requiring direct editing of the code. Editing HTML and JavaScript is also possible using the editing options available in the composer.
The EEC is an extension of the VEC that helps you edit an experience for an iframe-busting site or pages that do not yet include the Target implementation. If you have trouble opening your page in the VEC, try the EEC.
For information about the VEC and the EEC, see [Experiences](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

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

This issue happens when customers have an `mbox.js` version earlier than 57 (i.e. version 56 or earlier). 
We recommend that all VEC users upgrade to the[ latest version of `mbox.js`](r_mboxjs_change_log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A), or at least upgrade to version 57. You might also consider [making the transition to `at.js`](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17). 

## When I change one element on the page, multiple elements change. (VEC and EEC) {#section_309188ACF34942989BE473F63C5710AF}

If the same DOM element ID is used on multiple elements on the page, changing one of those elements changes all elements with that ID. To prevent this from happening, an ID should be used only once on each page. This is a standard HTML best practice. For more information, see [Page Modification Scenarios](c_vec_scenarios.md#concept_A458A95F65B4401588016683FB1694DB). 

* **I can't edit experiences for an iFrame-busting site.**
* **I want to set up tests on pages that don't have the mbox/target implementation done yet.**

Both of these issues can be addressed by enabling the Enhanced Experience Composer. Click ** `Setup` ** > ** `Preferences` **, then select the check box that enables the Enhanced Experience Composer. The Enhanced Experience Composer uses an Adobe-managed proxy to load your page for editing. This allows editing on iFrame-busting sites and allows editing on sites and pages where you have not yet added Adobe Target code. The activities do not deliver to the site until the code has been added. Some sites may not load via the Enhanced Experience Composer, in which case you can uncheck this option to load the Visual Experience Composer via an iFrame. 

## Bold and italic text styles with Edit Text/HTML or Change text/HTML do not show on my page. Sometimes the text disappears after applying these style changes. (VEC and EEC) {#section_7A71D6DF41084C58B34C18701E8774E5}

If you use ** `Edit Text/HTML` ** in the Visual Experience Composer for A/B or Experience Targeting activities or ** `Change Text/HTML` ** for Automated Personalization or Multivariate Test activities to make text bold or italic, those styles might not be applied on the page or the text disappears from the page in the Visual Experience Composer. This is because the way the rich-text editor applies these styles might interfere with the website markup. 
If you see this issue:

1. Click the ** `HTML` ** button in the rich-text editor to enter source editing mode.
1. Find the styles text elements. 
    * For bold text, change `<strong>` elements to `<b>`.
    * For italic text, change `<em>` elements to `<i>`.




## For Automated Personalization activities, image swapping appears broken in the VEC or EEC. (VEC and EEC) {#section_88AABFDFE6A3420299B0D508B12A3994}

Adding an image offer to a location takes the full dimension of the original image space in the VEC or EEC. On delivery, the image is not expanded and is shown as it is, so there is no impact on delivery.

## When I open my website in the Visual Experience Composer, the Target libraries do not load. (VEC only) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

Target adds two parameters ( `mboxEdit=1` and `mboxDisable=1`) while opening the website in the Visual Experience Composer. 
If your website (specially Single Page Apps), trims our parameters or actually removes them while navigating from one page to another (without a page reload) the Target functionality breaks and the Target libraries do not load.
To avoid this problem, ensure that you do not trim or remove these two parameters. 
## My page won't open in the EEC, or loads slowly. Activities or experiences load slowly in the VEC. (VEC only) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Several issues can affect page performance in the Target experience composers. Some common issues include:

* You do not have an mbox on the page.
* Your site uses proxy blocking, which does not allow the page to be opened in either experience composer.
* Your site doesn't allow itself to be opened in an iFrame.

If issues occur in the Enhanced Experience Composer, try turning off the Enhanced Experience Composer and use the Visual Experience Composer instead.
To disable the Enhanced Experience Composer, go to ** `Setup` ** > ** `Preferences` ** and turn off the ** `Enable Enhanced Experience Composer` ** option. 
Some users see the following error message in the console:
![](../graphics/error message.jpg) 
If neither the Visual Experience Composer nor the Enhanced Experience Composer works, use a browser extension like Requestly (Chrome or Firefox) or Modify Response Headers (Firefox) that can overwrite the X-Frames header options for your site and allow them to be loaded in iFrames, enabling the VEC. If you are unable to use browser extensions, use the Form Composer.
**To use the Requestly extension on Chrome or Firefox:** 

1. Turn off the Enhanced Experienced Composer.

1. Install the Requestly browser extension on Chrome or Firefox.

1. Open the extension and configure it using the following:

1. Select ** `Modify headers` **. 

1. Enter the following:

    * Rule name

    * Modification rules
    
        * Toggle ** `Add` ** to ** `Remove` **. 

        * Toggle ** `Request` ** to ** `Response` **. 

        * Enter "X-Frame-Options" as the header name.

        * Repeat previous steps and enter "x-frame-options" as the header name.

          >[!NOTE]
          >
          >Headers that are manipulated via Requestly are case sensitive.


        * Change ** `Equals` ** to ** `Contains` ** as the condition for the source URL and enter the URL of the activity that you are trying to load in the VEC. 

      ![](../graphics/chrome extension.png) 


1. Click ** `Save` **. 
   ![](graphics/requestly.png) 
   You should now be able to load the page quickly with the Visual Experience Composer.


**To use the Modify Response Headers extension on Firefox:** 

1. Install the Modify Response Headers on Firefox and restart the browser.

1. From your Firefox extensions, select the Modify Response Headers extension.

1. Click ** `Preferences` **. 

1. Select ** `Filter` ** from the Action drop down. 

1. In the Header Name field, enter: ** `X-Frame-Options` **. 

1. Repeat Steps 4 and 5 to add a filter with ** `x-frame-options` **. 

1. Click ** `Add` **. 

1. Click ** `Start` **. 


![](../graphics/firefox extension.png) 
After setting up an extension, open Target. Your pages should now load in the Visual Experience Composer, even if the Enhanced Experience Composer is disabled.

## My page does not display in the VEC (VEC only) {#section_87B3BEA4B6174CFDA6C9A69A1A051FA1}


* The browser is not supported.
* The browser is blocking a non-secure page on a secure site. Click the icon to the left of the URL in the browser address bar and click ** `Disable protection on this page` ** 

* You entered an invalid URL.
* You have not entered a default URL in your account setup page.

## When launching a URL for a VEC activity, the console displays the following error message: "Uncaught ReferenceError:_AT is not defined." (VEC only) {#section_BB5B9B629AC4452496A82943EFF72B85}

This error occurs if you try to deliver Visual Experience Composer (VEC) campaigns and you have not updated `mbox.js` downloaded from the Target user interface with the `Support Visual Experience Composer Activities` option enabled ( `Setup` > `Implementation` > `mbox.js` > `Edit mbox.js Settings`). 
Ensure that this setting is enabled, then download and update `mbox.js` on your website. 

## The VEC appears broken when I use browse mode. (VEC only) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

While using browse mode, if you access a URL that does not have target.js or contains a frame-buster header, the Visual Experience Composer appears broken. Due to browser security concerns, Target cannot access the URL you navigated to.

## The EEC won't load an internal QA URL that is not accessible on public IP. (EEC only) {#section_D29E96911D5C401889B5EACE267F13CF}

This can be resolved by whitelisting the following IP addresses. These IP addresses are for Adobe's server used for the Enhanced Experience Composer proxy. They are only required for activity editing. Visitors to your site do not need these IP addresses whitelisted.


<table id="table_E8DFD24B9B684CF182CEAFCA13ADD9C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Region</th> 
   <th colname="col2" class="entry">IP Addresses</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>United States</p> </td> 
   <td colname="col2"> <p> 
     <ul class="simplelist"> 
      <li>52.55.99.45</li> 
      <li>54.80.158.92</li> 
      <li>54.204.197.253</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe, Middle East, and Africa (EMEA)</p> </td> 
   <td colname="col2"> <p> 
     <ul class="simplelist"> 
      <li> </li> 
      <li>52.51.238.221</li> 
      <li>52.210.199.44</li> 
      <li>54.72.56.50</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Asia-Pacific (APAC)</p> </td> 
   <td colname="col2"> <p> 
     <ul class="simplelist"> 
      <li>52.193.67.35</li> 
      <li>54.199.198.109</li> 
      <li>54.199.241.57</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

You might see the following error message in Target:
`Error: Your website domain (ISP) is blocking the Enhanced Experience Composer. You can whitelist the Enhanced Experience Composer's IP addresses or turn off Enhanced Experience Composer in `Configure` > `Page Delivery` menu.` 
![](../graphics/EEC_error.png) 
The following are reasons that you might see this error message and remedies to fix the situation:

* **Issue:**Your website domain (ISP) is blocking the Enhanced Experience Composer. 
  **Remedy:**Whitelist the IP addresses listed above. 

* **Issue:**The IP addresses are whitelisted but your website does not support TLS version 1.0. Target currently uses the default configuration of 1.0. 
  **Solution:**See the following question (The Enhanced Visual Experience Composer won't load on secure pages on my site that use TLS 1.2). 



## The EEC won't load on secure pages on my site that use TLS 1.2. (EEC only) {#section_C5B31E3D32A844F68E5A8153BD17551F}

You might see the error message described above in "The Enhanced Visual Experience Composer won't load on secure pages on my site." if the above IP addresses are whitelisted but your website does not support TLS version 1.0. Target currently uses the default configuration of 1.0.
To check the TLS version on your website using Firefox (other browsers have similar steps):

1. Open the affected website in Firefox.

1. Click the ** `Show Site Information` ** icon on the browser's address bar. 
   ![](../graphics/firefox more info.png) 

1. Click ** `Show Connection Details` ** > ** `More Information` **. 
   ![](../graphics/firefox more info 2.png) 

1. Examine the TLS version information under Technical Details:
   ![](../graphics/firefox more info 3.png) 
   To remedy this situation, reach out to[Customer Care](r_problem.md#reference_ACA3391A00EF467B87930A450050077C) for configuration with your TLS version and the domain.


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


For more information, see [Mixed Content](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) on the *Mozilla Developer Network* (MDN) website. 
>## Enabling Mixed Content in Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}By default, Firebox blocks pages that mix secure and insecure content. It is recommended that you permanently change this setting to use 
<keyword>
 Target
</keyword>. 
<draft-comment otherprops="merge">
 target/t_mixed_content_firefox.xml
</draft-comment>
>1. In Firefox, enter `about:config` in the address bar.
>1. Acknowledge the warning message displayed by Firefox.
>1. In the search bar, type `block_active`.
>1. Double-click ` ** `security.mixed_content.block_active_content` **` .

>## Enabling Mixed Content in Internet Explorer {#task_59E7D13C04DF486C92CD78D0C63DDDE8}By default, Internet Explorer blocks pages that mix secure and insecure content. It is recommended that you permanently change this setting to use Target Standard. 
<draft-comment otherprops="merge">
 target/t_mixed_content_ie.xml
</draft-comment>
>1. In Internet Explorer, click the settings icon > ** `Internet Options` **.
>1. Open the `Security` tab.
>1. Select ** `Internet` **, then click ** `Custom Level` **.
>1. Select ** `Miscellaneous` **.
>1. Under `Miscellaneous`, enable ** `Display Mixed Content` **.
>1. Click ** `OK` ** > ** `Yes` ** > ** `Apply` **.
>## Enabling Mixed Content in Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}If you're visiting a site via a secure connection, Google Chrome will verify that the content on the web page has been transmitted safely. 
<draft-comment otherprops="merge">
 target/t_mixed_content_chrome.xml
</draft-comment>See [This page has insecure content](https://support.google.com/chrome/answer/1342714?hl=en) in Google Chrome Help. 
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
<li class="kids-section">Kids</li>
```

**Selected:** 
`<li class="women-section">Women</li>` 
Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)` 
**Result:** 
The selector works as expected because `li.women-section:eq(0)` is not affected. 


<table id="table_F37367FB9CB343D497B5C58E8AA1B015"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Before</th> 
   <th colname="col2" class="entry">After</th> 
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
      <b>&lt;li class="kids-section"&gt;Kids&lt;/li&gt;</b>
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
`<li class="women-section">Women</li>` 
Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)` 
**Result:** 
The selector does not work, because `ul.nav:eq(0)` provides a dynamically added element. The element won't be available and the action is not applied. When a similar list item with same class is added dynamically or manually after an activity has been created, a new element at the first position is created. This breaks the selector. 


| Before |After (Attempted) |
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
`<li class="women-section">Women Shoes</li>` 
Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)` 
**Result:** 
In this case, inserting a list after the list ending with the selected list item works as expected. The new element is added to the same position as the selected element relative to the parent element.


| Before |After |
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
<li class="men-section"> Men </li>
```

**Selected:** 
`<li class="women-section">Women</li>` 
Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)` 
**Result:** 
The element is successfully removed because the class of the selected item is not altered.


| Before |After |
|---|---|
| 
```
<div id="wrap">
   <ul class="nav">
      
<b><li class="men-section">Men</li></b>
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
<li class="kids-section">Kids</li>
```

**Selected:** 
`<li class="women-section">Women</li>` 
Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)` 
**Result:** 
The element is successfully removed because the class of the selected item is not altered. The removed element includes a unique class within its parent subtree.


| Before |After |
|---|---|
| 
```
<div id="wrap">
   <ul class="nav">
      <li class="men-section">Men</li>
      <li class="women-section">Women</li>
      
<b><li class="kids-section">Women</li></b>
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
<li class="women-shoes">Women</li>
```

**Selected:** 
`<li class="women-shoes">Women</li>` 
Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)` 
**Result:** 
The element is successfully removed.


| Before |After |
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
<li class="women-section">Women</li>
```

**Selected:** 
`<li class="women-section">Women</li>` 
Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)` 
**Result:** 
The element class cannot be renamed because `class` is not found. 


| Before |After (Attempted) |
|---|---|
| 
```
<div id="wrap">
   <ul class="nav">
      <li class="men-section">Men</li>
      
<b><li class="women-section">Women</li></b>
   </ul>
</div>
```
| 
```
<div id="wrap">
   <ul class="nav">
      <li class="men-section">Men</li>
      
<b><li class="women-shoes">Women</li></b>
   </ul>
</div>
```
|

