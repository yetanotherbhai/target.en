---
description: The at.js library is a new implementation library for Adobe Target designed for both typical web implementations and single-page applications.
keywords: Target;at.js;migrate to at.js;readiness;audit at.js;integrate at.js
seo-description: The at.js library is a new implementation library for Adobe Target designed for both typical web implementations and single-page applications.
seo-title: at.js Implementation
solution: Target
subtopic: Getting Started
title: at.js Implementation
topic: Standard
uuid: 83b11fdd-deeb-4f19-afe8-70bd9366a2e9
index: y
internal: n
snippet: y
translate: y
---

# at.js Implementation

## at.js Implementation {#concept_8AC8D169E02944B1A547A0CAD97EAC17}The 
<filepath>
  at.js 
</filepath> library is a new implementation library for 
<keyword>
  Adobe Target 
</keyword> designed for both typical web implementations and single-page applications.Among other benefits, [!DNL  at.js] improves page-load times for web implementations and provides better implementation options for single-page applications. 

[!DNL  at.js] replaces [!DNL  mbox.js] for [!DNL  Target] implementations. The [!DNL  at.js] library also includes the components that were included in [!DNL  target.js], so there is no longer a call to [!DNL  target.js]. 


>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 with FP-11577 (or later) supports at.js implementations with its Adobe Target Cloud Services integration. For more information, see[ Feature Packs ](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) and [ Integrating with Adobe Target ](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in the *Adobe Experience Manager 6.2 documentation*. 



To use [!DNL  at.js], replace the [!DNL  mbox.js] reference on pages where you want to implement it. You cannot use both [!DNL  mbox.js] and [!DNL  at.js] on a single page. However, you can use either on each page on your site. 

The [!DNL  at.js] library works for existing implementations using the ` mboxCreate()`, ` mboxDefine()`, and ` mboxUpdate()` functions and supports new functionality focused on single-page-app based implementations. 

You can use [!DNL  at.js] anywhere you currently use [!DNL  mbox.js]. 

The [!DNL  at.js] library offers several improvements over the [!DNL  mbox.js] library, including: 


* Completely asynchronous communication via cross domain AJAX 


  >[!IMPORTANT]
  >
  >Although [!DNL  at.js] communicates with the [!DNL  Target] servers asynchronously, the [!DNL  at.js] file itself must load synchronously in the ` &amp;lt;head&amp;gt;` section of your page. Ideally, it should be one of the first scripts loaded. Once loaded, [!DNL  at.js] executes mbox calls asynchronously through ` XMLHttpRequest`, and does not block page rendering. 


* No more blocking calls 

* No ` document.write()` used 

* No immediate execution of JavaScript in [!DNL  Target] responses 

* Better timeout and error handling 


    * Customizable [ timeout ](c_target-ats-functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF) per call 

    * No reloads on timeouts 



* Functions designed specifically for single-page apps/MVC frameworks 


>## How at.js Works {#concept_7B5951B4394D4478B01FE80D57735F8B}<keyword>
  Target 
</keyword> system diagram showing the flow of calls and information sent or collected for an auto-created global mbox using 
<filepath>
  at.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov/c_how_atjs_works.xml 
</draft-comment>In the Target implementation illustrated below, the following Marketing Cloud solutions are implemented: Analytics, Target, and Audience Management. In addition, the following Marketing Cloud core services are implemented: Dynamic Tag Management (Activation), Audiences, and Visitor ID Service. 

![](../graphics/target-flow.png) 



<table id="table_BF424454762C45C6ABED85FC49A7809E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Call </th> 
   <th colname="col2" class="entry"> Description </th> 
   <th colname="col3" class="entry"> Call </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <img href="../ov2/graphics/step1 red.png" id="image_93C806D5A60A4F03BA258780E99C9EA9" /> </td> 
   <td colname="col2"> <p>Call returns the <span class="keyword"> Marketing Cloud ID </span> (MCID) if the user is authenticated; another call syncs the customer ID. </p> </td> 
   <td colname="col3"> <img href="../ov2/graphics/step2 red.png" id="image_6FC6C3541AF34BA5B53843D573D726B7" /> </td> 
   <td colname="col4"> <p>The <span class="filepath"> at.js </span> library loads synchronously and hides the document body. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../ov2/graphics/step3 red.png" id="image_54CB02239B994478A20AC192EDF90DC4" /> </td> 
   <td colname="col2"> <p>A global mbox request is made including all configured parameters, MCID, SDID, and customer ID (optional). </p> </td> 
   <td colname="col3"> <img href="../ov2/graphics/step4 red.png" id="image_6AF7D59C1127417E9718A027AB304BD3" /> </td> 
   <td colname="col4"> <p>Profile scripts execute and then feed into the Profile Store. The Store requests qualified audiences from the Audience Library (for example, audiences shared from <span class="keyword"> Adobe Analytics </span>, <span class="keyword"> Audience Management </span>, etc.). </p> <p>Customer attributes are sent to the Profile Store in a batch process. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../ov2/graphics/step5 red.png" id="image_978B5A368D9A4929B9CD98CEAF261136" /> </td> 
   <td colname="col2"> <p>Based on the URL, mbox parameters, and profile data, <span class="keyword"> Target </span> decides which activities and experiences to return to the visitor. </p> </td> 
   <td colname="col3"> <img href="../ov2/graphics/step6 red.png" id="image_8CC1644F6C8A49DFA74678FC484ADCDD" /> </td> 
   <td colname="col4"> <p>Targeted content is sent back to page, optionally including profile values for additional personalization. </p> <p>The experience is revealed as quickly as possible without flicker of default content. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <img href="../ov2/graphics/step7 red.png" id="image_BA305C16960247A0B55D66CD3A664B02" /> </td> 
   <td colname="col2"> <p> <span class="keyword"> Analytics </span> data is sent to Data Collection servers. </p> </td> 
   <td colname="col3"> <img href="../ov2/graphics/step8 red.png" id="image_01FCF7749E2A42EA9C8AF0F46B219846" /> </td> 
   <td colname="col4"> <p> <span class="keyword"> Target </span> data is matched to <span class="keyword"> Analytics </span> data via the SDID and is processed into the <span class="keyword"> Analytics </span> reporting storage. </p> <p> <span class="keyword"> Analytics </span> data can then be viewed in both <span class="keyword"> Analytics </span> and <span class="keyword"> Target </span> via <span class="wintitle"> Analytics for Target </span> (A4T) reports. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Configure at.js {#concept_2FA0456607D04F82B0539C5BF5309812}Information to help you set several settings on the 
<codeph>
  at.js 
</codeph> Settings page. 
<draft-comment otherprops="merge">
  ov2/c_target-atjs-advanced-settings.xml 
</draft-comment>
>[!NOTE]
>
>You can override settings in the ` at.js` library, rather than configuring the settings in the Target Standard/Premium UI or by using REST APIs. For more information, see [ at.js Settings Override ](c_target-ats-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506). 



To open the [!UICONTROL  Settings] page: 


1. Click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] **. 

1. Select ** [!UICONTROL  at.js] ** > ** [!UICONTROL  Edit at.js Settings] **. 



## Content Delivery Settings {#section_118D290DFC444509AD8E4AE86C9D92C0}

Please consult with Client Care before changing these settings. These settings are required for most implementations. 



<table id="table_51A0B36B374A4F2FA36ADCFE05E4F28C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Autocreate global mbox </td> 
   <td colname="col2"> <p>Select whether to embed the global mbox call in the <span class="filepath"> at.js </span> file to automatically fire on each page load. </p> <p>Changing this setting affects both <span class="filepath"> at.js </span> and <span class="filepath"> mbox.js </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Global mbox name </td> 
   <td colname="col2"> <p>Select a name for the global mbox. By default, this name is <span class="codeph"> target-global-mbox </span>. </p> <p> Special characters, including ampersands (&amp;), can be used in mbox names with <span class="codeph"> at.js </span>. </p> <p>Changing this setting affects both <span class="filepath"> at.js </span> and <span class="filepath"> mbox.js </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Advanced Settings {#section_33B697B77BA64A01B5939D7EC75231F2}



<table id="table_AFA97284FD5B4495A0CBE7B9A1C0EBE2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Client Code </td> 
   <td colname="col2"> <p>The client code is a client-specific sequence of characters often required when using the <span class="keyword"> Target </span> APIs. </p> <p>This setting cannot be changed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IMS Organization ID </td> 
   <td colname="col2"> <p> This ID ties your implementation to your <span class="keyword"> Adobe Marketing Cloud </span> account. </p> <p>This setting cannot be changed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profile Lifetime </td> 
   <td colname="col2"> <p>This setting determines how long visitor profiles are stored. By default, profiles are stored for two weeks. </p> <p>To change the <span class="wintitle"> Profile Lifetime </span> setting, contact <a href="http://helpx.adobe.com/marketing-cloud/contact-support.html" format="http" scope="external"> Client Care </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> X-Domain </td> 
   <td colname="col2"> <p>Determines whether the browser sets cookies in your own domain (1st party cookies), Target's domain, or both. </p> <p>Changing this setting affects both <span class="filepath"> at.js </span> and <span class="filepath"> mbox.js </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Timeout </td> 
   <td colname="col2"> <p>If <span class="keyword"> Target </span> does not respond with content within the defined period, the server call times out and default content is displayed. Additional calls continue to be attempted during the visitor's session. The default is 15 seconds. </p> <p>Changing this setting affects both <span class="filepath"> at.js </span> and <span class="filepath"> mbox.js </span>. </p> <p>The <span class="filepath"> at.js </span> library uses the timeout setting in <span class="codeph"> XMLHttpRequest </span>. The timeout starts when the request is fired and stops when <span class="keyword"> Target </span> gets a response from the server. For more information, see <span class="codeph"> <a href="https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout" format="https" scope="external"> XMLHttpRequest.timeout </a> </span> on the Mozilla Developer Network. </p> <p>If the specified timeout occurs before receiving the response, default content is shown and the visitor might be counted as a participant in an activity because all data collection happens on the <span class="keyword"> Target </span> edge. If the request reaches the <span class="keyword"> Target </span> edge, the visitor is counted. </p> <p>Consider the following when configuring the timeout setting: </p> <p> 
     <ul id="ul_F9154E3EC6BF41ECA49216BF4373AF6C"> 
      <li id="li_C26553FD85B94850944F623CA94CD370"> <p>If the value is too low, users might see default content most of the time, although the visitor could be counted as a participant in the activity. </p> </li> 
      <li id="li_6BDF05026AA747D2A494BE5E5A199717"> <p>If the value is too high, visitors might see blank regions on your web page or blank pages if you use body hiding for extended periods of time. </p> </li> 
     </ul> </p> <p>To get a better understanding of mbox response times, look at the Network tab in your browser's Developer Tools. You can also use third-party web performance monitoring tools, such as Catchpoint. </p> <p> <p>Note:  The <a href="c_target-ats-functions.xml#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> visitorApiTimeout setting </a> ensures that <span class="keyword"> Target </span> doesn't wait for the Visitor API response for too long. This setting and the <span class="wintitle"> Timeout </span> setting for <span class="codeph"> at.js </span> described here do not affect each other. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Legacy Browser Support </td> 
   <td colname="col2"> <p> <p>Note:  The <span class="wintitle"> Legacy Browser Support </span> option is available in <span class="codeph"> at.js </span> version 0.9.3 and earlier. This option was removed in <span class="codeph"> at.js </span> version 0.9.4. For a list of browsers supported by <span class="codeph"> at.js </span>, see <a href="../ov/c_implementing_target.xml#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Supported Browsers </a>. </p> </p> <p> Legacy browsers are older browsers that do not fully support CORS (Cross Origin Resource Sharing). These browsers include: Internet Explorer browsers earlier than version 11 and Safari versions 6 and below. If Legacy Browser Support is disabled, Target does not deliver content or count visitors in reports on these browsers. If this option is enabled, it is recommended to do quality assurance across older browsers to ensure a good customer experience. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Code Settings {#section_D41C905D0F8149949F525C85F2CCFF7F}

Please consult with Client Care before changing these settings. These settings are required for most implementations. 



<table id="table_05B4524D0E204B6390FF6192A846ABA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Library Header </td> 
   <td colname="col2"> <p>Add any custom JavaScript to include at the top of the library. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Library Footer </td> 
   <td colname="col2"> <p>Add any custom JavaScript to include at the bottom of the library. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Download at.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}Instructions to download the 
<filepath>
  at.js 
</filepath> library using the Target interface or the Download API. 
<draft-comment otherprops="merge">
  ov2/c_target-configure-atjs.xml 
</draft-comment>
>[!IMPORTANT]
>
>The Target team maintains only two versions of [!DNL  at.js]—the current version and the second-latest version. Please upgrade [!DNL  at.js] as necessary to ensure that you are running a supported version. For more information about what's in each version, see [ at.js Version Details ](c_target-atjs-implementation.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A). 




>[!NOTE]
>
>If you are migrating your [!DNL  Target] implementation from using the mbox.js library to the at.js library, see [ Migrate to at.js from mbox.js ](c_target-atjs-implementation.md#task_DE55DCE9AC2F49728395665DE1B1E6EA). 



## Download at.js Using the Target Interface {#section_1F5EE401C2314338910FC57F9592894E}

To download [!DNL  at.js] from the [!DNL  Target] interface: 


1. Click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] **. 

1. Select ** [!UICONTROL  at.js] **. 

1. Click ** [!UICONTROL  Edit at.js Settings] **. 

   The Settings page shows your [!DNL  at.js] settings. Some of these settings are informational only. 

1. Change any settings as needed. 



<table id="table_03B0D41E2A574BB98B28A8D845BE3CDB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Auto create global mbox </td> 
   <td colname="col2"> <p>Use <span class="filepath"> at.js </span> to auto-deploy target-global-mbox for a single line of code implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Global mbox name </td> 
   <td colname="col2"> <p>Specify a name for the global mbox. The default is target-global-mbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Advanced Settings </td> 
   <td colname="col2"> <p>Refer to <a href="c_target-atjs-implementation.xml#concept_2FA0456607D04F82B0539C5BF5309812" format="dita" scope="local"> Configure at.js </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Code Settings </td> 
   <td colname="col2"> <p>(Optional) Specify custom code to include in the page header and footer. We recommend that you consult with Client Care before changing these settings. </p> </td> 
  </tr> 
 </tbody> 
</table>


1. Click ** [!UICONTROL  Code] ** and enter any custom header and footer JavaScript to execute at the top of the library, such as ` targetPageParams`. 

   If you used [!DNL  mbox.js] in the past, you might notice fewer fields. However, there are ways to do many of the same things in [!DNL  at.js] that you did in [!DNL  mbox.js]. For example, if you used mbox parameters in [!DNL  mbox.js], in [!DNL  at.js] you can use [ targetPageParamsAll ](c_target-ats-functions.md#reference_B235C9F6DA79449ABE3E23F914FEABAE). The [!DNL  mbox.js] Extra JavaScript field is replaced by the [!DNL  at.js] Header and Footer fields, which provide more control of the code. 

1. Click ** [!UICONTROL  Save] **. 

1. Return to the Implementation page and click ** [!UICONTROL  Download at.js] **. 



## Download at.js Using the Target Download API {#section_C0D9D2A9068144708D08526BA5CA10D0}

To download [!DNL  at.js] using the API. 


1. Get your client code. 

   Your client code is available at the top of the ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] ** > ** [!UICONTROL  Edit at.js Settings] ** page of the [!DNL  Target] interface. 

1. Get your admin number. 

   Load this URL: 


   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/< 
<span class="varname"> client&amp;nbsp;code </span>>
   ```


   Replace ` < * ` client code` *>` with the client code from Step 1. 

   The result of loading this URL should look similar to the following example: 


   ```
   { 
     "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1" 
   }
   ```


   In this example, "6" is the admin number. 

1. Download [!DNL  at.js]. 

   Load this URL with the following structure: 


   ```
   https://admin< 
<span class="varname"> admin&amp;nbsp;number </span>>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=< 
<span class="varname"> client&amp;nbsp;code </span>>&amp;version=<version number>
   ```



    * Replace ` < * ` admin number` *>` with your admin number. 

    * Replace ` < * ` client code` *>` with the client code from Step 1. 

    * Replace ` < * ` version number` *>` with the desired [ [!DNL  at.js] version number ](c_target-atjs-implementation.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) (for example, 0.9.4). 



   Loading this URL starts the download of your customized [!DNL  at.js] file. 


>## How at.js Manages Flicker {#concept_AA168574397D4474B993EEAB90865EBA}Information about how the Target at.js JavaScript library prevents flicker during page or app load. 
<draft-comment otherprops="merge">
  ov2/c_manage-flicker-with-atjs.xml 
</draft-comment>Flicker happens when default content momentarily displays to visitors before it is replaced by the activity content. Flicker is undesirable because it can be confusing to visitors. 

Target provides several ways to prevent flicker: 


* Using an Auto Created Global mbox 

* Using a Custom Global mbox with getOffer() and applyOffer() 

* Using a Regional mbox with mboxCreate() 



## Using an Auto Created Global mbox {#section_C502170D551C4F52AAFD8E82C41BB63A}

If you enable the [ Auto Create Global Mbox ](c_understanding-global-mbox.md#concept_76AC0EC995A048238F3220F53773DB13) setting when configuring ` at.js`, ` at.js` will set HTML BODY style opacity to 0. After a response from Target is received, ` at.js` resets HTML BODY opacity to 1. 

Opacity set to 0 keeps the page content hidden to prevent flicker, but the browser still executes the page load. 

## Using a Custom Global mbox with getOffer() and applyOffer() {#section_E42C06BB3B16456A920B3332BC6B1C28}

In almost all implementations, the auto created mbox should be used. In the rare instance that a [ custom global mbox ](c_understanding-global-mbox.md#task_8FE8D068DE924B3B96A784643015D830) is required, you can use a combination of [ ` getOffer()` ](c_target-ats-functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF) and [ ` applyOffer()` ](c_target-ats-functions.md#reference_BBE83F513B5B4E03BBC3F50D90864245). You must use your own flicker-handling code. The following sample pre-hides HTML BODY and then displays it after a response is received from Target: 


```
document.documentElement.style.opacity = "0"; 
  
adobe.target.getOffer({ 
    mbox: 'target-global-mbox', 
    success: function(offer) { 
        adobe.target.applyOffer({ 
            mbox: 'target-global-mbox', 
            offer: offer 
        }); 
  
        document.documentElement.style.opacity = "1"; 
    }, 
    error: function() { 
        document.documentElement.style.opacity = "1";         
    } 
});
```


Because both ` getOffer()` and ` applyOffer()` are low-level APIs, there is no built-in flicker control. You can pass a selector or HTML element as an option to ` applyOffer()`, in this case ` applyOffer()` will add the activity content to this particular element; however, you must make sure the element is properly pre-hidden before invoking ` getOffer()` and ` applyOffer()`. 

## Using a Regional mbox with mboxCreate() {#section_D4946235531544BF9B9B4A80CCF09226}

If you use a regional mbox implementation, you can use [ ` mboxCreate()` ](c_target-ats-functions.md#reference_E68805FE86C64792B2066DB17B253D74) with your page provisioned similar to the following sample code: 


```
<div class="mboxDefault"> 
Some default content 
</div> 
<script> 
mboxCreate('some-mbox'); 
</script> 

```


If your pages are properly provisioned, ` at.js` will manage flicker by appropriately switching the CSS "visibility" property of the element with the mboxDefault class. 
>## Create an Order Confirmation mbox - at.js {#task_E85D2F64FEB84201A594F2288FABF053}The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y." 
<draft-comment otherprops="merge">
  ov/t_create_orderconfirm-page-mbox-atjs.xml 
</draft-comment>
>[!NOTE]
>
>If users make purchases on your website, we recommend implementing an Order Confirmation mbox even if you use Analytics for Target (A4T) for your reporting.




>[!NOTE]
>
>If you are migrating to ` at.js` from ` mbox.js`, your [ existing Order Confirmation mbox ](c_target-atjs-implementation.md#task_E85D2F64FEB84201A594F2288FABF053) might work as is. If this is the case, you don't need to use the ` trackEvent()` technique explained below. 



>1. In your order details page, insert the mbox script following the model below.
>1. Replace the WORDS IN CAPITAL LETTERS with either dynamic or static values from your catalog.


>       >[!NOTE]
>       >
>       >Use comma delimiting to separate multiple product IDs.


>       **Tip: **You can also pass order information in any mbox (it does not need to be named ` orderConfirmPage`). You can also pass order information in multiple mboxes within the same campaign. 

>    
>       ```
>       <script type="text/javascript"> 
>       adobe.target.trackEvent({ 
>           "mbox": "orderConfirmPage", 
>           "params":{  
>               "orderId": "ORDER ID FROM YOUR ORDER PAGE",  
>               "orderTotal": "ORDER TOTAL FROM YOUR ORDER PAGE",  
>               "productPurchasedId": "PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3"  
>           } 
>       }); 
>       </script> 
>       ```

>## Single-Page Application Implementation {#reference_CF0B0D71987D487EA0BCDE128C80ABEB}There are many options for implementing Target in single-page applications with 
<filepath>
  at.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-single-page-application.xml 
</draft-comment>
>Use a combination of the following techniques for the best capabilities. We strongly recommend that you implement [!DNL  Target] using [!DNL  Adobe's Dynamic Tag Management], a free Core Service offering that can be used to quickly adapt your [!DNL  Target] implementation as needed. For more information, see the [ Dynamic Tag Management documentation ](https://marketing.adobe.com/resources/help/en_US/dtm/). 



><table id="table_A228B59A06454E9E80732400BD8242D3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Implementation </th> 
   <th colname="col2" class="entry"> Framework </th> 
   <!-- <entry colname="col3">Pros </entry> <entry colname="col4">Cons </entry> --> 
   <th colname="col5" class="entry"> DTM-Implementable? </th> 
   <th colname="col6" class="entry"> Recommended mbox Name </th> 
   <th colname="col7" class="entry"> Demo/Documentation </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p>ngRoute </p> </td> 
   <td colname="col2" morerows="1"> <p>Angular </p> </td> 
   <!-- <entry colname="col3"> <p> <ul id="ul_FB3B7021365B4536876A9ACC8495EA29"> <li id="li_21EE6E9161184724BBED3FD10411EF43"> Earliest possible firing of an mbox on the route change </li> <li id="li_2A456D69B54241C99F2AA2513046215A">Excellent flicker handling. Enforces sequencing of the mbox response and DOM updates, offering excellent capabilities for flicker-control when used with DOM-manipulation type offers. </li> </ul> </p> </entry> <entry colname="col4"> Might fire before you have updated your data layer </entry> --> 
   <td colname="col5" morerows="1"> <p>Yes </p> </td> 
   <td colname="col6" morerows="1"> <p>target-global-mbox </p> </td> 
   <td colname="col7"> <p> <a href="http://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/angular/route_change_demo.html" scope="external" format="html"> Demo </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col7"> <p> <a href="https://github.com/Adobe-Marketing-Cloud/target-spa-extensions/wiki/Angular-ngRoute" scope="external" format="http"> Documentation </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>Ui-router </p> </td> 
   <td colname="col2" morerows="1"> <p>Angular </p> </td> 
   <!-- <entry colname="col3"> <p> <ul id="ul_09E8114B138748ED9AC7971A87FFBF6C"> <li id="li_6DC9942B0E16473E88CC62F80ADFE236"> Earliest possible firing of an mbox on the route change </li> <li id="li_CAB6CCFE15104687800325F6C13C0685"> Excellent flicker handling. Enforces sequencing of the mbox response and DOM updates, offering excellent capabilities for flicker-control when used with DOM-manipulation type offers. </li> </ul> </p> </entry> <entry colname="col4">Might fire before you have updated your data layer </entry> --> 
   <td colname="col5" morerows="1"> <p>Yes </p> </td> 
   <td colname="col6" morerows="1"> <p>target-global-mbox </p> </td> 
   <td colname="col7"> <p> <a href="http://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/angular/state_change_demo.html" scope="external" format="html"> Demo </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col7"> <p> <a href="https://github.com/Adobe-Marketing-Cloud/target-spa-extensions/wiki/Angular-UIRouter" scope="external" format="http"> Documentation </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>Directive </p> </td> 
   <td colname="col2" morerows="1"> <p>Angular </p> </td> 
   <!-- <entry colname="col3"> Excellent flicker handling </entry> <entry colname="col4"> Requires use of the form-based composer </entry> --> 
   <td colname="col5" morerows="1"> <p>Yes </p> </td> 
   <td colname="col6" morerows="1"> <p>Custom per content </p> </td> 
   <td colname="col7"> <p> <a href="http://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/angular/directive_example.html#/view1" scope="external" format="html"> Demo </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col7"> <p> <a href="https://github.com/Adobe-Marketing-Cloud/target-spa-extensions/wiki/Angular-Directive" scope="external" format="http"> Documentation </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>Component </p> </td> 
   <td colname="col2" morerows="1"> <p>React </p> </td> 
   <td colname="col5" morerows="1"> <p>No </p> </td> 
   <td colname="col6" morerows="1"> <p>Custom per content </p> </td> 
   <td colname="col7"> <p> <a href="http://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/react/react_component_demo.html" scope="external" format="html"> Demo </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col7"> <p> <a href="https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions/wiki/React-Component" scope="external" format="https"> Documentation </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom event </p> </td> 
   <td colname="col2"> <p>All </p> </td> 
   <!-- <entry colname="col3"> <p> <ul id="ul_6761725AEDB1433F81432A87419B1FDC"> <li id="li_A99AB34FAE294E309F6457BC22962677"> Richest possible information for targeting and segmenting available passed with the mbox call </li> <li id="li_07AA645BEA7641498DA1C25438C87A74"> Works great with adding new content </li> </ul> </p> </entry> <entry colname="col4"> No guarantee of flicker-handling. No sequencing of DOM updates with mbox calls, which might result in flicker of default content. </entry> --> 
   <td colname="col5"> <p>Yes </p> </td> 
   <td colname="col6"> <p>target-global-mbox </p> </td> 
   <td colname="col7"> <p> 
     <!--Demo/--> <a href="https://github.com/Adobe-Marketing-Cloud/target-spa-extensions/wiki/Custom-Event" scope="external" format="http"> Documentation </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>hashchange </p> </td> 
   <td colname="col2" morerows="1"> <p>All </p> </td> 
   <!-- <entry colname="col3"> <p> <ul id="ul_D27476145B8841FEB4B020FDE87CE1D1"> <li id="li_A721ECBEA3E9435386C5CC240D47F249"> Easiest to implement </li> <li id="li_FAD0033B8F134252B34C173CC005A299">Works great with adding new content </li> </ul> </p> </entry> <entry colname="col4"> No guarantee of flicker-handling. No sequencing of DOM updates with mbox calls, which might result in flicker of default content. </entry> --> 
   <td colname="col5" morerows="1"> <p>Yes </p> </td> 
   <td colname="col6" morerows="1"> <p>target-global-mbox </p> </td> 
   <td colname="col7"> <p> <a href="http://adobe-marketing-cloud.github.io/target-atjs-extensions/examples/angular/hash_change_event.html" scope="external" format="html"> Demo </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col7"> <p> <a href="https://github.com/Adobe-Marketing-Cloud/target-spa-extensions/wiki/Hash-Change" scope="external" format="http"> Documentation </a> </p> </td> 
  </tr> 
 </tbody> 
</table>


>>[!NOTE]
>>
>>If you previously used[ ` mboxUpdate()` ](c_target-ats-functions.md#reference_61B2B9F351344CF5B0915D5AFD21C5FE) or TNT.createGlobalMbox() to fire the global mbox on view changes within your app, you need to migrate to using a combination of [ ` getOffer()` ](c_target-ats-functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF) and [ ` applyOffer()` ](c_target-ats-functions.md#reference_BBE83F513B5B4E03BBC3F50D90864245) for this purpose. 
>



>>[!NOTE]
>>
>>If you are using the Analytics for Target (A4T) implementation, ensure that you complete Step 8 in[ Analytics for Target Implementation ](a4t.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A). 
>

>## at.js Limitations {#concept_FA99E4D6EC274552BF45E01AFB76CCAE}There are some differences between 
<filepath>
  at.js 
</filepath> and 
<filepath>
  mbox.js 
</filepath>. This section lists some of the differences and limitations, to help you be successful with 
<filepath>
  at.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov2/c_target-atjs-limitations.xml 
</draft-comment>
## Known Visual Experience Composer Limitations {#section_4B63C97169DE4C93B22944E880FD3DF1}


* Insert Element and Rearrange options in the Visual Experience Composer should be avoided in single-page apps. Because the DOM is not cleared on page load events in single-page apps like it is with traditional websites, the Insert Element and Rearrange manipulations might be reapplied multiple times depending on how the visitor navigates the SPA. 



## Integrations and Plugins {#section_D92E31170176406AAC7B5005F03D3425}

Some functions within [!DNL  mbox.js] are not available in [!DNL  at.js]. Internal [ mbox.js objects and methods ](c_visitor_profile.md#section_8C78059D15D9452F95636A5640188537) (such as ` mbox`, ` mboxCurrent`, ` mboxFactoryDefault`, ` mboxFactories`, and others) are no longer supported by [!DNL  at.js] (example: ` mboxFactoryDefault`). This is by design, intended to discourage you from "hacking" [!DNL  at.js] to develop unsupported functionality that over the long term can cripple an implementation and make it impossible to upgrade. The only exposed methods are covered in the API pages of this documentation. Because of this: 


* Legacy, page-based [ integrations ](c_target-atjs-implementation.md#concept_C100BC4F073C4B57A608B309D0157B39) with other Adobe solutions might not work and should be upgraded to newer, server-side integrations.
* [ Custom plugins developed for mbox.js ](c_target-atjs-implementation.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) might not work unless updated for [!DNL  at.js]. Make sure you include any [ plugins ](c_target-atjs-implementation.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) as part of your testing. 



## Asynchronous Considerations {#section_B586360A3DD34E2995AE25A18E3FB953}

Because all mboxes are now asynchronous, they won't block page rendering or return in the order in which they fired. 


* Legacy page-based [!DNL  Target] to [!DNL  Analytics] integration will not work. This integration requires that the [!DNL  Target] call is made before the [!DNL  Analytics] call. 

* Beware of JavaScript dependencies between your offer and the page. You should not assume that the JavaScript in your offer is going to execute before the hardcoded JavaScript below the mbox. 

* Beware of JavaScript dependencies between multiple offers on the page. You can no longer assume that the offer delivered by the first mbox is going to execute before the offer delivered by your second mbox. 

* DOM Manipulation and Redirect offers should be delivered through the auto-created global mbox in [!DNL  at.js] and delivered in the ` &amp;lt;head&amp;gt;`. An ` mboxCreate()` function at the top of the ` &amp;lt;body&amp;gt;` will likely result in flicker of default content. 


>## at.js Integrations {#concept_C100BC4F073C4B57A608B309D0157B39}Information about common integrations with 
<keyword>
  Target 
</keyword> and their support status with 
<filepath>
  at.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov2/c_target-atjs-integrations.xml 
</draft-comment>If there are additional integrations you use or if you have a compelling need for an integration that is not supported, please contact your account representative or consultant. 

## Supported Integrations {#section_3B44A970D3FB42D1973701452C868B55}


<table id="table_3C9C2D0A88004D5D9708347B85DE5A7E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Integration </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Analytics for Target (A4T) </p> </td> 
   <td colname="col2"> 
    <!-- link to section in tnt--> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Profiles &amp;amp; Audiences (P&amp;amp;A) </p> </td> 
   <td colname="col2"> 
    <!--link to mcloud help Audiences--> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>VisitorId Service </p> </td> 
   <td colname="col2"> 
    <!-- link to mcloud help Marketing Cloud ID Service--> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Tag Management (DTM) </p> </td> 
   <td colname="col2"> 
    <!--link to dtm--> <p>Consider the following when using a DTM integration: </p> <p> 
     <ul id="ul_8B7BF60E14554C7B863E434180D409C7"> 
      <li id="li_EF8BC216C6A04FAA8E214ADC59CC7724">Library Management: Use the "Custom" hosting option. <p>"Automatic" management is not currently supported. </p> </li> 
      <li id="li_AB3B3ED75C634846914A8DE9B96FEB76">Global Mbox Parameters work </li> 
      <li id="li_E048B9DCDA8A4BD68600218F2D653963">Wrapping Mboxes in page-load rules now fire immediately instead of at the end of page load. </li> 
      <li id="li_8017C0CE60D64860AED299B134E5C465">JavaScript/Third Party Tags: Mbox creation and parameter passing methods can be used in the JavaScript/Third Party Tag sections of Page Load Rules, Event-based Rules, and Direct Call Rules. For example, many customers already trigger view change mboxes using the "pushState or hashChange" or "custom event" conditions in DTM's Event-based Rules. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Experience Manager (AEM) Cloud Service </p> </td> 
   <td colname="col2"> <p> The AEM Cloud Service enables access to Target capabilities from within the AEM workflow. </p> <p> <span class="keyword"> Adobe Experience Manager </span> 6.2 with FP-11577 (or later) now supports <span class="filepath"> at.js </span> implementations with its <span class="wintitle"> Adobe Target Cloud Services </span> integration. For more information, see <a href="https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html" format="html" scope="external"> Feature Packs </a> and <a href="https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html" format="html" scope="external"> Integrating with Adobe Target </a> in the <i>Adobe Experience Manager 6.2</i> documentation. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Unsupported Integrations {#section_8EFCAED418DC42E0B07F95924819EAC2}


<table id="table_4CF1738CF06B43A784EE783D3FAED3C8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Integration </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Legacy Target to SiteCatalyst Integration </p> </td> 
   <td colname="col2"> <p>This was the integration that sent campaign and recipe ids to <span class="keyword"> SiteCatalyst </span> via the page call so you could do reporting in the <span class="keyword"> SiteCatalyst </span> UI. This functionality is replaced by A4T. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Legacy Target to SiteCatalyst Integration </p> </td> 
   <td colname="col2"> <p>This was the integration that made mbox calls named "SiteCatalyst: Event" and "SiteCatalyst: Purchase" so you could build success metrics and user profiles based on evars and props. This functionality is replaced by A4T and P&amp;amp;A. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Legacy Audience Manager (AAM) to Target Integration </p> </td> 
   <td colname="col2"> <p>This was the integration that made a front-end API call to retrieve AAM segments and then sent them as mbox parameters on every mbox call on the page. It's possible to replicate this integration using the <span class="codeph"> adobe.target.registerExtension() </span> method in <span class="filepath"> at.js </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Third-Party Integrations {#section_EE599839CCAD49DD97640E5EDAD9082E}


<table id="table_8139E0696BAD436588224AEC2AEE0852"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Integration </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Other Tag Managers </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> at.js </span> should work with non-Adobe tag management platforms, but be careful using custom integration features that other vendors have developed. Their integrations might be dependent on internal <span class="filepath"> mbox.js </span> functions that no longer exist in <span class="filepath"> at.js </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Third-party data providers (e.g. Demandbase, Bluekai, weather APIs) </p> </td> 
   <td colname="col2"> <p>Many third-party data providers used to supplement Target's user profiling can be replicated using <a href="c_target-ats-functions.xml#reference_B3ACC004D45E460C8DD94C1476D2625C" format="dita" scope="local"> registerExtension() </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## at.js Plug-ins {#concept_F5D4C0A4DACF41409CC42FDD93B13FAF}Information about supported and not-supported 
<filepath>
  at.js 
</filepath> plug-ins. 
<draft-comment otherprops="merge">
  ov2/c_target-atjs-plugins.xml 
</draft-comment>Many people have built customized plugins and response plug-ins for [!DNL  mbox.js]. These custom plug-ins might not be supported by [!DNL  at.js] without being updated. 

If you are using a plug-in that is not listed here and you would like to know the status, please contact your account representative. 

Here is the current status of some of the plug-ins that are used by many customers when used with [!DNL  at.js]: 

<table id="table_51B92B09370E4A03B28ACE358CC12BCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Plugin </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> mboxTrack </td> 
   <td colname="col2"> <p>Not supported. </p> <p>This is replaced by the <a href="c_target-ats-functions.xml#reference_7E0F19368F9C4BC38F1E5DC5E717E487" format="dita" scope="local"> trackEvent </a> function. Update your plug-ins to apply the new function. </p> <p> See the <a href="c_target-atjs-implementation.xml#concept_C100BC4F073C4B57A608B309D0157B39" format="dita" scope="local"> integrations </a> page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Persistent Profile Backup Plugin </td> 
   <td colname="col2"> <p>Not supported. </p> <p> This plug-in was deprecated when the <span class="keyword"> Target </span> profile lifetime was extended from two weeks to 90 days. Check the expiration date of your mbox cookie to see the profile lifetime setting on your account. </p> <p>Contact ClientCare if you would like to extended the profile lifetime to 90 days. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ttMeta </td> 
   <td colname="col2"> <p>Supported. </p> <p> This plug-in should continue to work with <span class="filepath"> at.js </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Debugging at.js {#concept_CAE591DA8C404C22917584ECD4F7494F}Information about the status of traditional 
<keyword>
  Target 
</keyword> debugging techniques when used with 
<filepath>
  at.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov2/c_target-debugging-atjs.xml 
</draft-comment>Debugging options are slightly different for mbox calls using [!DNL  at.js]. 

The following video demonstrates tools for troubleshooting at.js: 



<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Tools for Troubleshooting Adobe Target </th> 
   <th colname="col3" class="entry"> 14:14 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/OXznmfKjxwU/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/OXznmfKjxwU/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Use native browser tools for inspecting mbox requests </li> 
      <li id="li_4610283D0A4649469C0D88FCE8F6D47A">Use the Marketing Cloud Debugger, mboxTrace, and ttMETA </li> 
      <li id="li_297A797915ED4278BC17340951024427">Understand the Target timeout </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


<table id="table_2A681D6FC38F4EF5882D981788804B8B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Debugging Technique </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Marketing Cloud Debugger </p> </td> 
   <td colname="col2"> <p>Not supported. </p> <p>All mbox calls with <span class="filepath"> at.js </span> use XHR requests, which are not exposed by MC debugger. Instead, use your browser's Developer Tools to inspect the Network requests, filtering to "mbox" to isolate mbox calls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>atList </p> </td> 
   <td colname="col2"> <p> Supported. <a href="http://dwright.businesscatalyst.com/bookmarklets.html" scope="external" format="http"></a> </p> <p> <a href="http://dwright.businesscatalyst.com/bookmarklets.html" scope="external" format="http"> atList </a> shows Mbox Names, Activity Names, Experience Names, Offer Names dev console as an alert or both (true/false configs are at the beginning of the bookmarklet). Requires ttMETA response plugin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> mboxHighlight </p> </td> 
   <td colname="col2"> <p> New version. </p> <p> <a href="http://dwright.businesscatalyst.com/bookmarklets.html" scope="external" format="http"> mboxHighlightJSON </a> outlines wrapping mboxes created with <span class="filepath"> at.js </span>. Use <a href="http://dwright.businesscatalyst.com/bookmarklets.html" scope="external" format="http"> atList </a> to expose activity details. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> mboxTrace=console </p> </td> 
   <td colname="col2"> <p>Supported, but in a different location. </p> <p>Instead of popping a new browser window or outputting to the console, you will need to inspect the Network request and look under Preview (Chrome) or Response (Firefox). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> mboxDisable=1 </p> <p>mboxDisable= </p> </td> 
   <td colname="col2"> <p>Disable or enable Target. </p> <p>If you are using <span class="filepath"> at.js </span> 0.9.6 or later you can disable Target by setting an <span class="codeph"> mboxDisable </span> cookie via the console. </p> <p>Use the following console statements to turn on/off Target (same behavior as <span class="codeph"> ?mboxDisable=1 </span>), but you don't have to keep adding this to the URL. Disabling persists until you remove the cookie or set the value to an empty string. </p> <p>document.cookie = "mboxDisable=1"; </p> <p>document.cookie = "mboxDisable="; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> mboxDebug=1 </p> <p>mboxDebug= </p> </td> 
   <td colname="col2"> <p>Disable or enable logging. </p> <p>If you are using <span class="filepath"> at.js </span> 0.9.6 or later you can disable logging by setting an <span class="codeph"> mboxDebug </span> cookie via the console. </p> <p>Use the following console statements to turn on/off Target console logging (same behavior as <span class="codeph"> ?mboxDebug=1 </span>), but you don't have to keep adding this to the URL. Console logging persists until you remove the cookie or set the value to an empty string. </p> <p>document.cookie = <span class="codeph"> "mboxDebug=1"; </span> </p> <p>document.cookie = <span class="codeph"> "mboxDebug="; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> mboxDebug=x-profile </p> </td> 
   <td colname="col2"> <p>Not Supported. </p> <p>Use <span class="codeph"> mboxTrace </span> to expose profile information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> mboxDebug=x-cookie </p> </td> 
   <td colname="col2"> <p>Not Supported. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> VEC Offer Debugging (_AT_Debug=console </p> </td> 
   <td colname="col2"> <p> Not supported. </p> <p> <span class="codeph"> mboxDebug=1 </span> will show the details of <span class="wintitle"> Visual Experience Composer </span> offer delivery. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## at.js Frequently Asked Questions {#concept_D6EFE8D84A06476DB5ABD494D7E8C769}Answers to frequently asked questions about 
<filepath>
  at.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov2/c_target-atjs-faq.xml 
</draft-comment>
## What are the advantages of using at.js versus mbox.js ? {#section_FE30D01A577C46ACB0F787B85F5E0F6B}

Although [!DNL  at.js] replaces [!DNL  mbox.js], [!DNL  mbox.js] will continue to be supported. However, for most people, [!DNL  at.js] provides advantages over [!DNL  mbox.js]. 

Among other benefits, [!DNL  at.js] improves page-load times for web implementations, improves security, and provides better implementation options for single-page applications. 

The following diagram illustrates page-load performance using ` mbox.js` versus ` at.js`. 

![](../graphics/atjs vesus mboxjs.png) 

As illustrated above, using ` mbox.js`, page content does not begin to load until after the [!DNL  Target] call is complete. Using ` at.js`, page content begins loading when the [!DNL  Target] call is initiated and does not wait until the call is complete. 

## Why does it seem like I see slower response times after upgrading from a previous version of at.js to version 1.0.0? {#section_DFBA5854FFD142B49AD87BFAA09896B0}

[!DNL  at.js] version 1.0.0 and later fires all the requests in parallel. Previous versions execute the requests sequentially, meaning the requests are put in a queue and Target waits for first request to complete before moving on to the next request. 

The way previous versions of [!DNL  at.js] execute requests is susceptible to the so-called "head of line blocking." In [!DNL  at.js] 1.0.0 and later, Target switched to parallel request execution. 

If you check the network tab waterfall for [!DNL  at.js] 0.9.1, for example, you'll see that next Target request doesn't start until the previous one has finished. This is not the case with [!DNL  at.js] 1.0.0 and later where all the request basically start at the same time. 

From a response-time perspective, mathematically, this can be summed like this 


<ul class="simplelist"> 
 <li> at.js 0.9.1: Response time of all Target requests = sum of requests response time </li> 
 <li> at.js 1.0.0 and later: Response time of all Target requests = maximum of requests response time </li> 
</ul>



As you can see, [!DNL  at.js] 1.0.0 will complete the requests faster. In addition, [!DNL  at.js] requests are asynchronous, so Target doesn't block page rendering. Even if requests take seconds to complete, you will still see the rendered page, only some portions of the page will be blanked out until Target gets a response from the Target edge. 

## What is the impact of at.js on page-load times? {#section_90B3B94FE0BF4B369577FCB97B67F089}

For more information, see [ Understanding the Target JavaScript Libraries ](c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB). 

## Can I load the Target library asynchronously? {#section_AB9A0CA30C5440C693413F1455841470}

The ` at.js` library should be loaded synchronously as best practice; however, you can load it asynchronously as an experimental option. 

The ` at.js` 1.0.0 release makes it possible to load the Target library asynchronously. 

To load ` at.js` asynchronously: 


* The recommended approach is via a tag manager such as Adobe Dynamic Tag Manager (DTM) or the new Adobe Launch. See the [ Adobe Dynamic Tag Manager documentation ](https://marketing.adobe.com/resources/help/en_US/dtm/) for more information. 

* You can also load ` at.js` asynchronously by adding the async attribute to the script tag that loads ` at.js`. You should use something like this: 


  ```
  &amp;lt;script&amp;nbsp;src="&amp;lt;URL&amp;nbsp;to&amp;nbsp;at.js&amp;gt;"&amp;nbsp;async&amp;gt;&amp;lt;/script&amp;gt;
  ```


* You can also load ` at.js` asynchronously using this code: 


  ```
  var script = document.createElement('script'); 
  script.async = true; 
  script.src = "<URL to at.js>"; 
  document.head.appendChild(script);
  ```




Loading ` at.js` asynchronously is a great way to avoid blocking the browser from rendering; however, this technique can lead to flicker on the web page. 

You can avoid flicker by using a pre-hiding snippet that will be visible after the relevant HTML elements are personalized by Target. We recommend using a tag manager such as Adobe DTM or the new Adobe Launch to add the pre-hiding snippet. The snippet must be added before loading ` at.js`. 

The pre-hiding code snippet is as follows: 


```
;(function(win, doc, style, timeout) { 
  var STYLE_ID = 'at-body-style'; 
 
  function getParent() { 
    return doc.getElementsByTagName('head')[0]; 
  } 
 
  function addStyle(parent, id, def) { 
    if (!parent) { 
      return; 
    } 
 
    var style = doc.createElement('style'); 
    style.id = id; 
    style.innerHTML = def; 
    parent.appendChild(style); 
  } 
 
  function removeStyle(parent, id) { 
    if (!parent) { 
      return; 
    } 
 
    var style = doc.getElementById(id); 
 
    if (!style) { 
      return; 
    } 
 
    parent.removeChild(style); 
  } 
 
  addStyle(getParent(), STYLE_ID, style); 
  setTimeout(function() { 
    removeStyle(getParent(), STYLE_ID); 
  }, timeout); 
}(window, document, "body {opacity: 0 !important}", 3000));
```


By default the snippet pre-hides the whole HTML BODY. In some cases, you may only want to pre-hide certain HTML elements and not the entire page. You can achieve that by customizing the style parameter. It can be replaced with something that pre-hides only particular regions of the page. 

For example, you have two regions identified by IDs container-1 and container-2, then the style can be replaced with the following: 


```
#container-1,&amp;nbsp;#container-2&amp;nbsp;{opacity:&amp;nbsp;0&amp;nbsp;!important}
```


Instead of default: 


```
body {opacity: 0 !important} 

```


## Is at.js compatible with the Adobe Experience Manager integration (AEM)? {#section_6177AE10542344239753764C6165FDDC}

[!DNL  Adobe Experience Manager] 6.2 with FP-11577 (or later) now supports [!DNL  at.js] implementations with its [!UICONTROL  Adobe Target Cloud Services] integration. For more information, see [ Feature Packs ](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) and [ Integrating with Adobe Target ](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in the *Adobe Experience Manager 6.2* documentation. 

## How can I prevent page-load flicker using at.js ? {#section_4D78AAAE73C24E578C974743A3C65919}

Target provides several ways to prevent page-load flicker. For more information, see [ Preventing Flicker with at.js ](c_target-atjs-implementation.md#concept_AA168574397D4474B993EEAB90865EBA). 

## What is the file size of at.js ? {#section_6A25C9A14C66441785A7635FEF5C4475}

The ` at.js` file is approximately 109 KB when downloaded. However, because most servers automatically compress files to make file sizes smaller, ` at.js` is approximately 34 KB when compressed (using GZIP or another method) on your server and loaded as users visit your website. The compression settings on the server where you installed ` at.js` determine its actual compressed size. 

## Why is at.js bigger than mbox.js ? {#section_AA1C43897E46448FA3E26EEC10ED7E51}

` at.js` implementations use a single library ( [!DNL  at.js]), while ` mbox.js` implementations actually use two libraries ( [!DNL  mbox.js] and [!DNL  target.js]). So a fairer comparison is ` at.js` versus ` mbox.js` *and* ` target.js`. Comparing the gzipped sizes of the two versions, ` at.js` version 1.2 is 34 KB and ` mbox.js` version 63 is 26.2 KB. `` 

` at.js` is larger because it does a lot more DOM parsing compared to ` mbox.js`. This is required because ` at.js` gets "raw" data in the JSON response and has to make sense of it. ` mbox.js` uses ` document.write()` and all the parsing is done by the browser. 

Despite the larger file size, our testing indicates that pages load faster with ` at.js` versus ` mbox.js`. Additionally, ` at.js` is superior from a security perspective because it doesn't load additional files dynamically or use ` document.write`. 

## Does at.js have jQuery in it? Can I remove this part of at.js because I already have jQuery on my website? {#section_E4604E46E7B34460B8DD6A78D9B476F9}

` at.js` currently uses parts of jQuery and thus you will see the MIT license notification at the top of ` at.js`. jQuery is not exposed and it doesn't interfere with the jQuery library you already have on your page, which might be a different version. Removal of the jQuery code within ` at.js` is not supported. 

## Does at.js support Safari and cross domain set to x-only? {#section_114EC271A6E045E1B2183B66F1B71285}

No, if cross domain is set to x-only and Safari has third-party cookies disabled, then both [!DNL  mbox.js] and ` at.js` will set a disabled cookie and no mbox requests will be executed for that particular client's domain. 

To support Safari visitors, a better X-Domain would be “disabled” (sets only a first-party cookie) or “enabled” (sets only a first-party cookie on Safari, while setting first- and third-party cookies on other browsers). 

## Can I run at.js and mbox.js side by side? {#section_4DCAF38DBAEB430CA486FAEFAE0E0A29}

Not on the same page. However, while implementing and testing [!DNL  at.js], you can run [!DNL  at.js] on some pages and [!DNL  mbox.js] on other pages until you've completely validated [!DNL  at.js]. 

## Can I use the Target Visual Experience Composer in my single-page applications? {#section_459C1BEABD4B4A1AADA6CF4EC7A70DFB}

The Visual Experience Composer (VEC) was designed for static web content and server-side-driven web applications. Depending on your SPA architecture, you may or may not be successful using the VEC. Each SPA framework and application is different and may have different results. Expect to need front-end developer support to create activities in single-page applications. 

Your SPA should load in the VEC so you can see if it will work for simple content changes in your application. If you have trouble loading your SPA in the VEC, open a Client Care ticket. You should also be able to use the "Browse&amp;amp;Navigate" feature to get to the right state of your application to begin making edits, as well as target the Activity URL to hash fragments and mbox parameters to deliver the activity content to the right mbox. 

The main challenges are timing: 


* VEC offer replaces content before the SPA has fully updated. The updated SPA content then replaces the VEC content.
* VEC offer looks for SPA content that is not yet on the page. After several tries the offer will give up. The SPA content then loads.
* SPA content loads and is visible before the VEC offer is returned and can replace it, resulting in flicker.


An implementation strategy that initiates mbox calls as close as possible to dynamic content can help. Please see the SPA Implementations page. 

## Can I use the Adobe Marketing Cloud Debugger with at.js implementations? {#section_FF3CF4C5FD2F4DB1BF1A6B39DA161637}

No, [!DNL  at.js] implementations are not compatible with the [!DNL  Marketing Cloud Debugger]. All mbox calls with [!DNL  at.js] use XHR requests, which are not exposed by the debugger. Instead, we recommend that you use mboxTrace for debugging purposes. You can also use your browser's Developer Tools to inspect the Network requests, filtering to "mbox" to isolate mbox calls. 

## Can I use special characters in mbox names with at.js ? {#section_8E31D2E8A27642098934D7DACFB2A600}

Special characters, including ampersands (&amp;), cannot be used in mbox names with ` at.js`. 

If you have migrated from [!DNL  mbox.js] to [!DNL  at.js] and you have mbox names that contain special characters, as a workaround, you can rename the affected mboxes. 

## Why are my mboxes not firing on my web pages? {#section_4BA5DA424B734324AAB51E4588FA50F5}

Target customers sometimes use cloud-based instances with [!DNL  Target] for testing or simple proof-of-concept purposes. These domains, and many others, are part of the [ Public Suffix List ](https://publicsuffix.org/list/public_suffix_list.dat). 

Modern browsers won't save cookies if you are using these domains unless you customize the ` cookieDomain` setting using targetGlobalSettings(). For more information, see [ Using Cloud-Based Instances with Target ](c_targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566). 

## Can IP addresses be used as the cookie domain when using at.js? {#section_8BEEC91A3410459D9E442840A3C88AF7}

Yes, if you are using [ at.js version 1.2 or later ](c_target-atjs-implementation.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A). We strongly recommend that you keep current with the latest version, however. 


>[!NOTE]
>
>The following examples are not necessary if you are using at.js version 1.2 or later.



Depending on how you use ` [ targetGlobalSettings ](c_target-ats-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506)`, you might need to make additional modifications to the code after downloading ` at.js`. For example, if you needed slightly different settings for your [!DNL  Target] implementations on various websites and were unable to define these settings dynamically using custom JavaScript, make these customizations manually after downloading the file and before uploading to the respective website. 

The following examples let you use the ` targetGlobalSettings()` at.js function to insert a code snippet to support IP addresses: 

This example is for a single IP address: 


```
if (window.location.hostname === '123.456.78.9') { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```


This example is for a range of IP addresses: 


```
if (/^123\.456\.78\..*/g.test(window.location.hostname)) { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```


## Why do I see warning messages, such as "actions with missing selectors"? {#section_C36BED5B16634361A1BA46FCB731489D}

These message are not related to [!DNL  at.js] functionality. The [!DNL  at.js] library tries to report anything that can't be found in the DOM. 

The following are possible root causes if you see this warning message: 


* The page structure that activity is running on has been changed. If you reopen the activity in the Visual Experience Composer (VEC), you should get a warning message. You should update the activity so that all the necessary elements can be found. 

* The underlying page is part of a Single Page Application (SPA) or the page contains elements that appear farther down the page and the [!DNL  at.js] "selector polling mechanism" cannot find those elements. Increasing the ` selectorsPollingTimeout` might help. For more information, see [ targetGlobalSettings() ](c_target-ats-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506). 

* Any click-tracking metric tries to add itself to every page, regardless of the URL on which the metric was set up. Although harmless, this situation makes many of these messages display. Recent versions of [!DNL  at.js] try to suppress these messages, but many customers are still on older versions of [!DNL  at.js] or on [!DNL  mbox.js]. 

  For best results, please download and use the latest version of [!DNL  at.js]. For more information, see [ at.js Version Details ](c_target-atjs-implementation.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) and [ Download at.js ](c_target-atjs-implementation.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2). 



## What is the domain tt.omtrdc.net that Target server calls go to? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL  tt.omtrdc.net] is the domain name for Adobe's EDGE network, used to receive all server calls for Target. 
>## at.js Version Details {#reference_DBB5EDB79EC44E558F9E08D4774A0F7A}Details about changes in each version of 
<filepath>
  at.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-versions.xml 
</draft-comment>
<a id="section_CEA633C86E7040669785F63F79468B1A"></a>


>[!IMPORTANT]
>
>The Target team maintains only two versions of [!DNL  at.js]—the current version and the second-latest version. Please upgrade [!DNL  at.js] as necessary to ensure that you are running a supported version. 



## at.js Version 1.2.3 {#section_CE4D14AF00D04F4C8A2F0513F5EA1A84}

[!DNL  at.js] version 1.2.3 is now available. 


* Adds support for JSON offers. JSON offers are supported only in activities created using the Form-based Experience Composer. Currently the only way to use JSON offers is via direct API calls. See [ Create JSON Offers ](c_manage_content.md#concept_63C7BEE1F0DB4A7596D997219B7C136D). 



## at.js Version 1.2.2 {#section_4E96D13F2DFE4F1F81A1089877D53649}

[!DNL  at.js] version 1.2.2 is now available. 


* Fixed an issue that returned a JavaScript error when the Target library loaded on a page using QUIRKS mode. (TNT-28312) 

* Fixed an issue that caused Target click tracking to break Analytics data collection calls. (TNT-28261) 

* Fixed an issue that caused ` getOffer() params` to fail when ` targetPageParams()` returns an empty string. (TNT-28359) 

* Fixed an issue with session ID generation when using x-only. (TNT-28361) 



## at.js Version 1.2.1 {#section_F757C8174BBA4F68AC5524ADC3D9C5E3}

[!DNL  at.js] version 1.2.1 is now available. 


* Fixed an issue when click tracking on a link with target="_blank" prevented Target from opening the link in a new tab. 



## at.js Version 1.2.0 {#section_1C3A18C595C34B25A14A440D213F3B9C}

[!DNL  at.js] version 1.2 is now available as a maintenance release that contains mostly bug fixes. 


* Fixed an issue that prevented default actions for click-tracking special cases. (TNT-28089) 

* Fixed an issue when click-tracking on a link with ` target="_blank"` that prevented Target from opening the link in a new tab. (TNT-28072) 

* IP addresses can be used as the cookie domain. (TNT-28002) 

* Fixed an issue that caused flicker in redirect offers with a global mbox or other regional mboxes. (TNT-27978) 

* Fixed an issue in Experience Targeting activity setup failing within the VEC when switching between Browse and Compose. (TNT-27942) 

* Fixed incorrect handling on flicker style classes for click-track elements. (TNT-27896) 

* Fixed an issue that caused global mbox parameters to become mixed up with all mbox parameters. (TNT-27846) 

* Made changes to ensure that Handlebars, Mustache, and other client-side templating libraries are properly handled by [!DNL  at.js]. (TNT-27831) 

* Made changes to ensure that ` sdidParamExpiry` is properly initialized and passed to the Visitor API. This is a regression that has been added to ` at.js 1.1.0`. Previous [!DNL  at.js] versions are not affected. This affects only clients using redirect offers and A4T. (TNT-27791) 

* Made changes to ensure that ` SCRIPT` is executed regardless of the type attribute being used. (TNT-27865) 



## at.js Version 1.1.0 {#section_8F494E1EA94E48A9B169F5CF9FE6DC56}

**Date: **August 2, 2017 

The following enhancements and fixes are included in [!DNL  at.js] version 1.1: 


* Added response token handling. For more information, see [ Response Tokens ](c_response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4). 

* Resolved issue so that ` document.currentScript polyfill` doesn't interfere with Angular 1.X. 

* Made changes to ensure that click tracking doesn't interfere with visibility property. Click tracking elements are marked with the ` at-element-click-tracking` CSS class instead of ` at-element-marker`. 



## at.js Version 1.0.0 {#section_37A3D23FC4AD42A68AA831B89E03E725}

**Date: **July 7, 2017 

The following enhancements and fixes are included at.js version 1.0: 


* Support for loading at.js asynchronously for faster page loads. 

* Support for pre-hiding page content when loading at.js asynchronously. 

* Better error messaging when content delivery is disabled. 

* Performance improvements when delivering multiple activities. 

* Support for YUI Compressor. 

* Bug/error reporting for custom events during activity delivery. 

* Fix for performance issues in Microsoft Internet Explorer 11. 

* Fix for ` getOffer()` function giving an error on some websites. 

* Load the Target library asynchronously. For more information, see [ at.js Frequently Asked Questions ](c_target-atjs-implementation.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769). 



## at.js Version 0.9.7 {#section_6C7B698BE21E40E495FD2850EFBF3E80}

**Date: **May 22, 2017 

The following enhancements and fixes are included in [!DNL  at.js] version 0.9.7: 


* Fixed an issue related to an asset key that was missing from ` insertAfter` and ` insertBefore` actions in the Visual Experience Composer (VEC). These issues were related to the migration from visual offers to offer templates.


## at.js Version 0.9.6 {#section_EEFA6413F2F947AD8C4A88128B90245D}

**Date: **April 13, 2017 

The following enhancements and fixes are included in [!DNL  at.js] version 0.9.6: 


* Redirect offer support for A4T. After you download and install [!DNL  at.js] version 0.9.6, you can use redirect offers in activities that use [!DNL  Adobe Analytics] as the Reporting Source for [!DNL  Target] (A4T). Besides [!DNL  at.js] version 0.9.6, there are other minimum requirements your implementation must meet in order to use redirect offers and A4T. For more information and additional important information you should know, see [ Redirect Offers - A4T FAQ ](c_a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905). 

* Prior to [!DNL  at.js] 0.9.6, when the Visitor API was present on the page and the ` visitorApiTimeout` setting was too aggressive, Target could run into a situation when no MCID data was sent in the [!DNL  Target] request. This could lead to issues like unstitched hits in [!DNL  Analytics] when using A4T. 

  This behavior has been changed in [!DNL  at.js] 0.9.6, even if the ` visitorApiTimeout` is set to say 1 ms, Target will try to collect SDID, tracking servers, and customer IDs data and send those in the Target request. 

* Added the ` selectorsPollingTimeout` setting. For more information, see [ targetGlobalSettings() ](c_target-ats-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506). 

* The format of the response from ` getOffer()` has been changed. For more information, see [ adobe.target.getOffer(options) ](c_target-ats-functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF). 

* Console logging has been added for unsupported ` &amp;lt;!DOCTYPE&amp;gt;` declarations. 

* Fixed an issue where [!DNL  Target Classic] plugins weren’t being applied correctly when multiple default offers were delivered to a single mbox. (TGT-22664) For more information, see [ Plug-Ins ](https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Using_Plug-Ins.html) in the Adobe Target Classic documentation. 

* Improved cookie-setting for two letter top-level-domains (TLDs) to ensure that the mbox cookie is set correctly for these domains (for example, [!DNL  test.no], [!DNL  autodrives.ca], and so forth). 

* The algorithm for extracting the top-level domain that should be used when saving cookies has changed in ` at.js` version 0.9.6. Because of this change, cookies cannot be saved to addresses that use IP. Most of the time, IP addresses are used for testing purposes, but as workarounds you can use DNS entries or adjust the hosts file on a local box. 

* Fixed move and rearrange actions handling when properties are string values instead of integers. 



## at.js Version 0.9.4 {#section_A15B12F12CD94F07B3F56613A79A815F}

**Date: **January 19, 2017 


* mbox names can now contain special characters, including ampersands ( &amp; ), to be consistent with naming requirements for mbox names using ` mbox.js`. 

  For a list of allowable special characters, see [ Configure at.js ](c_target-atjs-implementation.md#concept_2FA0456607D04F82B0539C5BF5309812). 

* Added ` secureOnly` setting that indicates whether ` at.js` should use HTTPS only or be allowed to switch between HTTP and HTTPS based on the page protocol. This is an advanced setting that defaults to False and can be overridden via ` targetGlobalSettings`. 

* The [!UICONTROL  Legacy Browser Support] option is available in ` at.js` version 0.9.3 and earlier. This option was removed in ` at.js` version 0.9.4. 



## at.js Version 0.9.3 {#section_DF13BC1D7C994AE7A36B81937A699DF4}

**Date: **October 10, 2016 


* Ensures mbox calls fire in Microsoft Internet Explorer 11 when legacy browsers are disabled in the ` at.js` settings. 

* Ensures that default content is rendered if a dynamic remote offer fails (for example, if the URL is incorrect and returns a 404 error). 

* Ensures that elements are revealed quickly when VEC click-tracking selectors can't be found in the DOM. 



## at.js Version 0.9.2 {#section_148549CBB4F046BAA8F79C79B64EC889}

**Date: **September 21, 2016 


* Added an ` optoutEnabled` setting to enable or disable the Device Graph opt-out. If this setting is set to ` true` and the visitor has opted out of tracking, the visitor's browser will not make any mbox calls. Device Graph is currently in Beta. This setting is set to ` false` by default, but must be set to ` true` if you are using Device Graph. A similar option is part of ` mbox.js` v61. 

* Added ` CustomEvent` support for the notification mechanism. Previously, the ` at.js` event notification mechanism could not be used via standard DOM APIs, such as ` document.addEventListener()`. Now you can use ` document.addEventListener()` to subscribe to ` at.js` events, such as request events and content rendering events. 

* Fixed an issue related to offers created in the Visual Experience Composer (VEC). Prior to this release, Target hid the selectors and un-hid them only when all selectors matched. In ` at.js` 0.9.2 Target un-hides the selectors as soon as they are matched. 



## at.js Version 0.9.1 {#section_DAFB99114D604CFB8416C1BC7DEEAEEE}

**Date: **July 14, 2016 


* Provides ` at.js` a timeout for the Visitor Id Service, which is independent of the service’s own timeout. 

* Corrects an issue in 0.9.0 that impacted implementations using ` at.js` on some pages and ` mbox.js` on other pages. 

* If you use Adobe Analytics as your activity's reporting source, you do not need to specify a tracking server during activity creation if you are using ` mbox.js` version 61 (or later) or ` at.js` version 0.9.1 (or later). The ` mbox.js` or ` at.js` library automatically sends tracking server values to [!DNL  Target]. During activity creation, you can leave the [!UICONTROL  Tracking Server] field empty on the [!UICONTROL  Goals &amp;amp; Settings] page. 



## at.js Version 0.9.0 {#section_2981CC9792F245389B39BB5B69F84C4E}

**Target Release:** 16.6.1 

**Date:** June 23, 2016 
* Fixes a whitescreen issue when using VEC offers. Anyone using [!DNL  at.js] should upgrade to this new version. 

* New ` [ registerExtension ](c_target-ats-functions.md#reference_B3ACC004D45E460C8DD94C1476D2625C)` API. 

  This new API gives developers access to certain jQuery modules used in [!DNL  at.js] to develop extensions (aka plugins) for the library. There are a few implications for this change. This impact only those users who are using these features: 

    * ` getSettings()` API has been removed, but the same functionality is available using ` registerExtension()`. 

    * ` getTracking()` API has been removed, but the same functionality is available using ` registerExtension()`.
    * Existing extensions (e.g. AngularJS extensions) must be updated to use the ` registerExtension()` approach. 


* New ` [ at.js notification ](c_target-ats-functions.md#reference_A828E4BA535F4E7692A075F3D70CF6CD)` API. 

  The goal of this notification system is to provide more insight into what [!DNL  at.js] is doing on the page and when there are issues. A common issue seen with the VEC is that an IT release changes the page, a VEC selector breaks, and the test stops delivering content correctly. A goal of this notification system is to make this delivery issue known to the page, so developers can access this information, pass it to a system like [!DNL  Adobe Analytics], and alerts can be sent to the business owners that their test broke. 

* New ` [ at.js Settings Override ](c_target-ats-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506) API method.` 

  You can override settings in the ` at.js` library, rather than configuring the settings in the [!DNL  Target Standard/Premium UI]or by using REST APIs. 



## at.js Version 0.8.0 {#section_E1C7B08EC0494388A022C28A8B8FE807}

**Date: **May 5, 2016. 

This is the first official release of the [!DNL  at.js] library. 

[!DNL  at.js] is a new implementation library for [!DNL  Target] designed for both typical web implementations and single-page applications. 

[!DNL  at.js] replaces [!DNL  mbox.js] for [!DNL  Adobe Target] implementations. 


>[!NOTE]
>
>Although [!DNL  at.js] replaces [!DNL  mbox.js], ` mbox.js` will continue to be supported. For most people, [!DNL  at.js] provides advantages over [!DNL  mbox.js]. This gives you time to test [!DNL  at.js] and to change the implementation on your pages. 



Among other benefits, [!DNL  at.js] improves page load times for web implementations, improves security, and provides better implementation options for single-page applications. 

[!DNL  at.js] contains the components that were included in [!DNL  target.js], so there is no longer a call to [!DNL  target.js]. 

When implementing [!DNL  at.js], be aware of the following: 


* Internet Explorer versions earlier than 8 are not supported.
* Asynchronous implementation means legacy integrations like the [!DNL  Test&amp;amp;Target] to [!DNL  SiteCatalyst] plugin may not work.
* [!DNL  Target] plugins that reference [!DNL  mbox.js] objects and methods are not supported.
* All calls to [!DNL  Target] are made via XMLHTTPRequest and content is returned via JSON.

>## Migrate to at.js from mbox.js {#task_DE55DCE9AC2F49728395665DE1B1E6EA}Migrating from 
<filepath>
  mbox.js 
</filepath> to 
<filepath>
  at.js 
</filepath> is a straightforward process. 
<draft-comment otherprops="merge">
  ov2/t_target-migrate-atjs.xml 
</draft-comment>Use the following steps to migrate from [!DNL  mbox.js] to [!DNL  at.js] and to check your migration: 

>1. Determine your organization's [ browser support ](c_implementing_target.md#reference_01B4BF99E7D545A7998773202A2F6100) requirements.
>1. Check your website's current [!DNL  mbox.js] implementation for capabilities that are not supported by [!DNL  at.js].

>       When auditing your implementation, look for the following: 

>       **What types of mboxes do you currently use?** 



>    <table id="table_B728D875E392457CB304D82CA85348BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Auto-created global mbox </p> </td> 
   <td colname="col2"> <p> The auto-created global mbox is created when the only line of <span class="keyword"> Target </span> code on your site is the <span class="filepath"> mbox.js </span> file. That file automatically generates an mbox call. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Global, empty <span class="codeph"> mboxCreate </span> </p> </td> 
   <td colname="col2"> <p>It is recommended that you switch to the auto-created global mbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wrapping <span class="codeph"> mboxCreate </span> </p> </td> 
   <td colname="col2"> <p>Migration should be simple, as long as your <span class="codeph"> mboxCreate() </span> is preceded by the <span class="codeph"> &amp;lt;div class="mboxDefault"&amp;gt;&amp;lt;/div&amp;gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxUpdate </p> </td> 
   <td colname="col2"> <p> Migration should be simple when <a href="c_target-ats-functions.xml#reference_61B2B9F351344CF5B0915D5AFD21C5FE" format="dita" scope="local"> <span class="codeph"> mboxUpdate() </span> </a> is used in conjunction with <span class="codeph"> mboxDefine() </span> or <a href="c_target-ats-functions.xml#reference_E68805FE86C64792B2066DB17B253D74" format="dita" scope="local"> <span class="codeph"> mboxCreate() </span> </a>. <span class="codeph"> mboxUpdate() </span> does not update the auto-created global mbox or an mbox originally created by <span class="codeph"> getOffer() </span>. In these circumstances, <a href="c_target-ats-functions.xml#reference_BBE83F513B5B4E03BBC3F50D90864245/section_D8D6A17B73DE4542937CDB687193A5CC" format="dita" scope="local"> a combination of <span class="codeph"> getOffer() </span> and <span class="codeph"> applyOffer() </span> </a> should be used to replace <span class="codeph"> mboxUpdate() </span> when migrating to at.js. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom clicktracking mboxes, including mboxTrack </p> </td> 
   <td colname="col2"> <p>We recommend that you update your code to use <a href="c_target-ats-functions.xml#reference_7E0F19368F9C4BC38F1E5DC5E717E487" format="dita" scope="local"> trackEvent() </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>       **Do you have any customizations to your [!DNL  mbox.js] file?** 

>    
>    * mboxParameters()
>    * mboxSupported()
>    * mboxCookieDomain()
>    * Extra Javascript
>    * Other locations


>       Most of the [ mbox.js objects and methods ](c_visitor_profile.md#section_8C78059D15D9452F95636A5640188537) (such as ` mbox`, ` mboxCurrent`, ` mboxFactoryDefault`, ` mboxFactories`, and others) are not supported. Alternate approaches might be possible to accomplish what you are trying to do. 

>       **Do you have [!DNL  mbox.js] on any of your web pages?** 

>       You cannot use both [!DNL  at.js] and [!DNL  mbox.js] on the same web page. However, you can use the two JavaScript libraries on two different pages of the same website. 

>       The mbox cookie is the main way Adobe stitches the visitor from page to page. As part of your QA process, you should confirm that the cookie is being preserved and read correctly as the visitor moves back and forth between pages with [!DNL  at.js] and those with [!DNL  mbox.js]. Make sure the same ` mboxPC` and ` mboxSession` values are passed in the mbox calls, regardless of which section of the site ( [!DNL  at.js] or [!DNL  mbox.js]) the visitor first lands on and which section originally sets the cookie. If you use 3rd-party cookies in your implementation, ensure that those values stay the same as you browse the site. 

>       **Do you integrate [!DNL  Target] with any other Adobe solutions?** 

>    
>    * Analytics (A4T)
>    * Analytics (legacy integration)
>    * AAM (backend)
>    * AAM (legacy frontend)
>    * AEM
>    * Data Workbench


>       Some of the legacy integrations are not supported by [!DNL  at.js]. For more information, see the [ Integrations ](c_target-atjs-implementation.md#concept_C100BC4F073C4B57A608B309D0157B39) page. 

>       **Do you integrate [!DNL  Target] with any 3rd-party tools?** 

>    
>    * Other Analytics tools
>    * Other DMPs
>    * Demandbase
>    * Click-tale
>    * Other


>       These integreations might need to be adjusted to work with [!DNL  at.js]. For more information, see the [ Integrations ](c_target-atjs-implementation.md#concept_C100BC4F073C4B57A608B309D0157B39) page. 

>       **Do you use a tag manager?** 

>    
>    * Dynamic Tag Management
>    * Ensighten
>    * Tealium
>    * Signal/BrightTag


>       For more information, see [ at.js Integrations ](c_target-atjs-implementation.md#concept_C100BC4F073C4B57A608B309D0157B39). 


>       >[!NOTE]
>       >
>       >If you are not currently using a tag manager to deploy [!DNL  Target], now might be a good time to consider it. Adobe's [ Dynamic Tag Management ](https://dtm.adobe.com) is free to [!DNL  Target] customers and is the recommended method to deploy [!DNL  Target]. For more information, see [ Best Practices for Implementing Adobe Target using Dynamic Tag Management ](https://marketing.adobe.com/resources/help/en_US/dtm/target/). 

>1. Verify that all current activities and integrations are working as expected.

>       Here are some things you can do while testing to confirm that [!DNL  at.js] is working as expected: 

>    
>    * Make sure all of your current activities work with the new JavaScript library. 

>    * Confirm that all [ integrations ](c_target-atjs-implementation.md#concept_C100BC4F073C4B57A608B309D0157B39) and [ plugins ](c_target-atjs-implementation.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) work as expected. 

>    * Make sure you are comfortable [ debugging ](c_target-atjs-implementation.md#concept_CAE591DA8C404C22917584ECD4F7494F) with the approaches available with [!DNL  at.js]. 


>## Deploy at.js to a Non-Production Environment {#reference_57C07770FA824DD6A63065CB0B0ECEB7}Information about how to safely deploy 
<filepath>
  at.js 
</filepath> to a non-production environment. 
<draft-comment otherprops="merge">
  ov2/r_target-test-atjs. 
</draft-comment>


><table id="table_D7E62869F2B040DD8E7DDF1A1F1BCC37"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Technique </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Deploy to DTM Staging </td> 
   <td colname="col2"> <p>If you use DTM, you can easily save <span class="filepath"> at.js </span> in your Adobe Target Tool configuration. </p> <p>After you have saved the library, use the DTM Switch tool to test it against your production code. This will also make it easy for your Adobe consultants to support you. </p> <p>For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/dtm/target/t_implementing-target-manually-js-hosted-dtm.html" format="html" scope="external"> Option 3: Implement Target Manually with the Target JavaScript Library Hosted by DTM </a> in the <i>Best Practices for Implementing Adobe Target using Dynamic Tag Management </i>guide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Use "Requestly" Chrome extension to map to another file </td> 
   <td colname="col2"> <p> <a href="https://chrome.google.com/webstore/detail/requestly/mdnleldcmiljblolnjhpnblkcekpdkpa?hl=en" scope="external" format="http"> Requestly </a> is a free Chrome extension that lets you redirect requests to an alternate URL. </p> <p>You deploy <span class="filepath"> at.js </span> to a URL, and then use Requestly to map your current <span class="filepath"> mbox.js </span> file URL to the new <span class="filepath"> at.js </span> URL. Then, any time your website tries to load <span class="filepath"> mbox.js </span>, it loads <span class="filepath"> at.js </span> instead. This approach also make it easier for Adobe to provide support. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Deploy to a development, staging, or QA environment </td> 
   <td colname="col2"> <p>If you host <span class="filepath"> mbox.js </span> in your codebase and are able to easily make updates to your code environments, deploy <span class="filepath"> at.js </span> to one of your lower environments. </p> <p>For better support from Adobe, deploy the file to an environment that Adobe can access. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Use Charles or Fiddler to map to a local file </td> 
   <td colname="col2"> <p> <a href="http://www.charlesproxy.com/" scope="external" format="http"> Charles Web Debugging Proxy </a> is an application available for Mac and Windows whose Map Local feature can be used to map the loading of your production <span class="filepath"> mbox.js </span> file to a local copy of <span class="filepath"> at.js </span>. A free trial version is available for download for Mac and Windows. </p> <p> <a href="http://www.telerik.com/fiddler" scope="external" format="http"> Fiddler </a> is a similar tool available as a free download for Windows. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Deploy to another tag manager environment </td> 
   <td colname="col2"> <p>If you are using another tag manager, it probably has a way to deploy <span class="filepath"> at.js </span> safely without impacting your production traffic. </p> </td> 
  </tr> 
 </tbody> 
</table>

