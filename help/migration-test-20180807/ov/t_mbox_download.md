---
description: To use Target Standard or Target Premium, add one line of code to call mbox.js.
keywords: mbox.js changes;mbox.js versions
seo-description: To use Target Standard or Target Premium, add one line of code to call mbox.js.
seo-title: mbox.js Implementation
solution: Target
subtopic: Getting Started
title: mbox.js Implementation
topic: Standard
uuid: 11115518-23b7-46fa-8d4b-ab12ce0e203d
index: y
internal: n
snippet: y
translate: y
---

# mbox.js Implementation

## mbox.js Implementation {#task_4EAE26BB84FD4E1D858F411AEDF4B420}To use 
<keyword>
  Target Standard 
</keyword> or 
<keyword>
  Target Premium 
</keyword>, add one line of code to call 
<filepath>
  mbox.js 
</filepath>.You can use either of two library references: ` mbox.js` or ` at.js`. [ Understanding the Target JavaScript Libraries ](c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB) explains the differences between the two libraries. 

>[!NOTE]
>
>The mbox.js library is still supported, but there will be no feature updates. All customers should migrate to at.js. For more information, see[ Migrate to at.js from mbox.js ](c_target-atjs-implementation.md#task_DE55DCE9AC2F49728395665DE1B1E6EA). 


The single reference to ` mbox.js` on each page provides the libraries needed for all of your activities. ` mbox.js` calls ` Target` from every page that references the ` mbox.js` file. This enables ` Target` to do the following: 

* Deliver Target activities
* Track clicks
* Track most success metrics


>[!TIP]
>
>To simplify implementation, you could reference ` mbox.js` in your global header. 


This video explains how to implement ` mbox.js`. 


<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> mbox.js Implementation Overview </th> 
   <th colname="col3" class="entry"> 8:52 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/f-A1zET6AwE/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/f-A1zET6AwE/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F">Select the correct settings for your <span class="filepath"> mbox.js </span> file </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Implement <span class="keyword"> Target </span> by adding the <span class="filepath"> mbox.js </span> file to the &lt;head&gt; of your site </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

You do not need to maintain different activity-specific versions of the file.

>1. Reference ` mbox.js` in the ` <head>` section of each page on your site.

>       ` <script src="/ * ` directory` */ * ` scripts` */mbox.js"></script>` 
>       Where ` * ` directory` */ * ` scripts` *` is the directory where you saved your ` mbox.js` file after downloading it. 
>## What mbox.js Does {#concept_EF761F5DB94241E7BE65A0AF3B9B46A3}Information to help your technical staff understand the 
<filepath>
  mbox.js 
</filepath> implementation and how it might affect your site. 
<draft-comment otherprops="merge">
  ov/c_mbox_technical.xml 
</draft-comment>Target Standard requires ` mbox.js` version 58 or later. For instructions on how to download and update ` mbox.js`, see [ mbox.js Implementation ](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420). 
For Target Standard, ` mbox.js` calls another JavaScript file, ` target.js`. ` Target.js` is hosted by Adobe and is automatically updated by Adobe. There is nothing you need to do to update ` target.js`, and there are no client-specific customizations. 
` Target.js` creates an mbox called ` target-global-mbox` in the ` <head>` section of your page. 
` Target.js` is called from ` mbox.js` by a line of JavaScript code added to the ` Extra JavaScript` field in ` mbox.js`. The only way to disable ` target.js` is not to include this line of code, thus also disabling ` Target`. 
` Target.js` has two functions in ` Target`: 

* DOM manipulation
* Enables visual elements of the ` Visual Experience Composer`


## DOM Manipulation {#section_169F8D4C077948DCB4F891ABBB03FF63}

` Target.js` controls the DOM manipulation library used by Standard. To display the content of a website, ` target.js` references ` sizzle.js` (version1.10.8-pre). ` Sizzle.js` enables the HTML element selectors. Other than ` sizzle.js`, only native JavaScript is used. No jquery is required. 
In addition, the following snippet is used for polling the DOM:
` https://github.com/dperini/ContentLoaded` 
## Target.js and the Visual Experience Composer {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

When you use the ` Visual Experience Composer` to set up an experience for an activity, your web page is opened in an iFrame. When the iFrame is loaded, Standard sends an HTML5 ` postMessage` API call. ` Target.js` detects any ` postMessage` calls and includes the following JavaScript libraries on the website: 

* For thumbnail generation: ` http://html2canvas.hertzen.com/`
* For cross-domain query: ` Admin.js`, ` CDQ.base.js`, ` CDQ.host.js`, ` admin.css`, used to send messages across the iFrames. These scripts allow Adobe to send data between the pages.


## Considerations for Angular Sites and Single-Page Applications {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

If you are implementing Target in an Angular site or in any Single-Page Application (SPA), you should use the ` at.js` library instead of ` mbox.js`. 
For more information, see [ at.js Implementation ](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17). 
>## Configure mbox.js {#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C}Information to help you set several settings on the 
<codeph>
  mbox.js 
</codeph> Settings page. 
<draft-comment otherprops="merge">
  ov/r_advanced_mboxjs_settings.xml 
</draft-comment>
>The default settings of the ` mbox.js` function library serve the needs of most ` Target` customers. 
>If needed, consult your account representative to change the ` mbox.js` settings. 


><table id="table_279063834235446A858D3CCFDA1F68A6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Client</p> </td> 
   <td colname="col2"> <p>The client code for your account.</p> <p>When viewing <span class="uicontrol"> Setup </span> &gt; <span class="uicontrol"> Implementation </span> &gt; <span class="uicontrol"> Edit Mbox.js Settings </span>, the Client at the top is the client code for your account. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Timeout</p> </td> 
   <td colname="col2"> <p>The Target request timeout.</p> <p>When viewing Setup &gt; Implementation &gt; Edit Mbox.js Settings, the Timeout after Compression Level is your Target request timeout. By default this value is set to 15 seconds, but we recommend setting it to a value between 2 seconds and 5 seconds.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XDomain</p> </td> 
   <td colname="col2"> <p>Determines whether the browser sets cookies in your own domain (1st party cookies), Target's domain, or both.</p> <p>Changing this setting affects both mbox.js and at.js.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Compression Level</p> </td> 
   <td colname="col2"> <p>Determines how compressed the <span class="filepath"> mbox.js </span> library file is. Increasing the compression level decreases the page-load time. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxParameters() function body</p> </td> 
   <td colname="col2"> <p>Returns extra parameters to pass to each mbox call.</p> <p>For example:</p> <p> <span class="codeph"> return "test=123"; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxSupported() function body</p> </td> 
   <td colname="col2"> <p>Returns false to exclude specific users.</p> <p>For example:</p> <p> <span class="codeph"> return !navigator.userAgent.indexOf('Safari') != -1; </span> </p> <p>The following browsers can be accepted or excluded:</p> <p> 
     <ul id="ul_571938793D6340558C9EA1996B503847"> 
      <li id="li_CCE7658BDB3F46E69B90534380D45EAF">IE 5.0 or greater (Windows)</li> 
      <li id="li_FBA2D7ABCDF84166A79EB74D3498E881">Netscape 5.0 or greater (Mac, Windows, Linux)</li> 
      <li id="li_E3594D180230474DAC872926DB1253CE">Safari 1.2.4 or greater (Mac)</li> 
      <li id="li_70D8B310F60B4271997F07BDC8316032">Mozilla Firefox 1.0 or greater (Mac, Windows, Linux)</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxCookieDomain() function body</p> </td> 
   <td colname="col2"> <p>Returns a string describing the domain to set first-party cookies.</p> <p>For example:</p> <p> <span class="codeph"> return "YOUR-DOMAIN"; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Extra JavaScript</p> </td> 
   <td colname="col2"> <p>Includes any additional JavaScript you want to execute on each page.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SiteCatalyst plug-in</p> </td> 
   <td colname="col2"> <p>Enables the <span class="keyword"> Analytics Target </span> plug-in. </p> <p>If enabled, the <span class="keyword"> Analytics </span> plug-in generates plug-in code in <span class="filepath"> mbox.js </span>. This sends <span class="keyword"> Analytics </span> tag information to <span class="keyword"> Target </span> servers as an mbox request on every page tagged with <span class="keyword"> Analytics </span>. </p> <p>Note that the <span class="keyword"> Analytics </span> plug-in must still be referenced on the page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>secureOnly</p> </td> 
   <td colname="col2"> <p>Indicates whether mbox.js should use HTTPS only or be allowed to switch between HTTP and HTTPS based on the page protocol. This is an advanced setting that defaults to False.</p> </td> 
  </tr> 
 </tbody> 
</table>

>## Download mbox.js {#task_8A48124A05F6442AA5C6A16BE2A4EE04}<keyword>
  Target Standard 
</keyword> and 
<keyword>
  Premium 
</keyword> use a modified version of the Adobe Target 
<filepath>
  mbox.js 
</filepath> file. 
<draft-comment otherprops="merge">
  ov/t_target-download-config-mbox.xml 
</draft-comment>This video explains how to implement ` mbox.js`. 


<table id="table_A3691A56EB814C8FB6C7D6840B8143AF"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> mbox.js Implementation Overview </th> 
   <th colname="col3" class="entry"> 8:52 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/f-A1zET6AwE/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/f-A1zET6AwE/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_18D0CEDD79FA4DB5B947064BAAA328CF"> 
      <li id="li_71FCC5919CFA47C0AEF75D6B2B5E9A35">Select the correct settings for your <span class="filepath"> mbox.js </span> file </li> 
      <li id="li_4667BA429D734F48A79B8B2FDEB194A0">Implement <span class="keyword"> Target </span> by adding the <span class="filepath"> mbox.js </span> file to the <span class="codeph"> &lt;head&gt; </span> of your site </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

To use the ` Adobe Target` ` Visual Experience Editor`, you must include an additional line of JavaScript as part of your ` mbox.js` file. 

>1. Click ** ` Setup` ** > ** ` Implementation` ** in ` Target Standard`.
>1. Click ** ` Download mbox.js` ** and follow the prompts to save the file.
>1. (Conditional) If you use ` mbox.js` version 60 or later, you can configure the library to automatically hide page content by default until mboxes load to reduce flicker on responsive sites.
>   For more information, see "Suppress page-load flicker" in [ Configure mbox.js ](t_mbox_download.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C). 
>
>1. Create the ` mbox.js` reference on the website.

>       Beginning with ` mbox.js` version 57, the ` mbox.js` reference can be placed anywhere within the ` <head>` section of the page. 

>       >[!IMPORTANT]
>       >
>       >If you use a version of ` mbox.js` prior to version 57, the reference must be the last item in the ` <head>` section of your pages. If the reference is not the last item, serious display or performance issues could result. See [ What mbox.js Does ](t_mbox_download.md#concept_EF761F5DB94241E7BE65A0AF3B9B46A3) for more information. 

>1. Upload the saved ` mbox.js` file to the location in your hosting environment that you specified in the code.
>## Target Page Methods by mbox.js Library Version {#concept_A95A4758A1E7405D947E9B4BCB5D62F0}The way 
<keyword>
  Target 
</keyword> makes and responds to calls from your page depends on the version of the 
<keyword>
  Target 
</keyword> library you are using, whether the 
<keyword>
  Marketing Cloud Visitor ID 
</keyword> implementation is present, and whether the visitor ID exists. 
<draft-comment otherprops="merge">
  target/c_call-Responses-library-version.xml 
</draft-comment>
>[!NOTE]
>
>If you use ` at.js`, all calls are made using JSON. This page provides details about ` mbox.js` library versions. The behaviors described in the scenarios below do not apply to ` at.js`. 


This section provides information about how each version of the ` Target` library responds to the ` Target` call from your page in each of the scenarios discussed below: 
There are several types or endpoints, depending on your implementation and library version. You should be familiar with each type to understand how ` Target` responds to calls in each scenario. 


<table id="table_9B6FA7E1F7E5470889FDA9D7C6F66CA9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type/Endpoint </th> 
   <th colname="col2" class="entry"> Call Method </th> 
   <th colname="col3" class="entry"> Response Content </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> autocreate global mbox - synchronous </td> 
   <td colname="col2"> document.write to make call </td> 
   <td colname="col3"> JavaScript without document.write() </td> 
  </tr> 
  <tr> 
   <td colname="col1"> autocreate global mbox - asynchronous </td> 
   <td colname="col2"> createElement() to append call to body </td> 
   <td colname="col3"> JavaScript without document.write() </td> 
  </tr> 
  <tr> 
   <td colname="col1"> standard </td> 
   <td colname="col2"> <p>document.write to make call</p> </td> 
   <td colname="col3"> JavaScript with document.write() </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ajax </td> 
   <td colname="col2"> <p>createElement() to append call to body</p> </td> 
   <td colname="col3"> JavaScript without document.write() </td> 
  </tr> 
  <tr> 
   <td colname="col1"> json </td> 
   <td colname="col2"> XMLHTTPrequest() to make call </td> 
   <td colname="col3"> returns JSON response </td> 
  </tr> 
 </tbody> 
</table>


>[!IMPORTANT]
>
>For any type but standard, all custom code and offers should be written to support an ajax environment. For example, if you use a JavaScript that includes ` document.write()`, the script will not work as expected. 



## No Visitor ID Implementation {#section_C6F7213FDE4D48E8BBCB1A9A26310FEE}

If you are using ` Target Standard` or ` Premium` with ` mbox.js`, and you have enabled ` Create Global Mbox` for your account,  the **autocreate global mbox synchronous** type of call and response is made, regardless of ` mbox.js` version. 
If you write your own custom code rather than using the ` Visual Experience Composer` actions, make sure your code is appropriate for an ajax environment. For example, if you use a JavaScript that includes ` document.write()`, the script will not work as expected. 

>[!NOTE]
>
>Multiple ajax mbox calls with the same mbox name but different parameters will not work on the same page. Only the first call will be made.


If you use "auto-create global mbox" but also have ` mboxCreate` calls on your page, for example, if you are implementing ` Target Standard` or ` Premium` on a page that previously used in a legacy implementation, the global mbox calls are made using the**autocreate global mbox - standard** endpoint and the ` mboxCreate` calls are made using the **standard** endpoint. The **standard** endpoint uses ` document.write()` to make the call and to respond. This blocks the page load, including content delivered in the ajax response, until all information is downloaded. 
If you use only mboxCreate, for example on pages created using ` Target Classic`, the page works as it always has. 


|  Creation Method  | mbox.js v57  | mbox.js v58  | mbox.js v59  | mbox.js v60  |
|---|---|---|---|---|
|  autocreate global mbox  | autocreate global mbox - synchronous  | autocreate global mbox - synchronous  | autocreate global mbox - synchronous  | autocreate global mbox - synchronous  |
|  mboxCreate  | standard  | standard  | standard  | standard  |


## Visitor ID Implementation Present, but No Visitor ID Set {#section_29888A119C7A4753AD287FC845AA63F4}

If no visitor ID has been set, there is no ` Marketing Cloud` visitor cookie for the user. The page calls out to the Visitor ID service to get the visitor ID. Target waits for the response with the ID making the call to ` Target`. 

>[!NOTE]
>
>` Mbox.js` v58  is strongly recommended to ensure that the visitor ID returns before the Target call is made. 


If you are using ` mbox.js` version 57 in this scenario, everything works as it does if there is no visitor ID implementation, as described in the previous scenario. Beginning with ` mbox.js` version 58, the ` Marketing Cloud Visitor ID` service returns with a visitor ID before ` Target` calls are made. This ensures that audience data shared through the Profiles and Audiences core service are available for the first ` Target` call in the visitor's session. To avoid flickering of default content before test content returns, ` Target` hides the ` <BODY>` until the visitor ID service returns. In version 58, ` display:none` is used to hide the page. This creates some problems with responsive sites, so beginning with version 59, ` opacity:0` is used to hide the content. 


|  Creation Method  | mbox.js v57  | mbox.js v58  | mbox.js v59  | mbox.js v60  |
|---|---|---|---|---|
|  autocreate global mbox  | autocreate global mbox - synchronous  | autocreate global mbox - asynchronous  | autocreate global mbox - asynchronous  | autocreate global mbox - asynchronous  |
|  mboxCreate  | standard  | ajax  | ajax  | ajax  |


## Visitor ID Implementation Present, and Visitor ID Exists {#section_9CD4AE4C8186425D886398BC3CE6C46D}

If the visitor ID cookie exists, ` Target` does not need to make a call to the Visitor ID service. In this case, there is no need to wait for the Visitor ID service before displaying content. For versions 57 to 59, the **autocreate global mbox - synchronous** type is used, so the page waits for the call to ` Target` to return before continuing to load. This ensures no flicker of default content is seen. For v60, the **global mbox-asynchronous type** is used to ensure ` Target` waits for the ` Marketing Cloud` opt-out service to respond. The opt-out service is part of the Data Co-op releasing in the fall of 2016. Because all calls are returned using ajax , ` document.write()` should not be used with ` mbox.js` version 60. 


|  Creation Method  | mbox.js v57  | mbox.js v58  | mbox.js v59  | mbox.js v60  |
|---|---|---|---|---|
|  autocreate global mbox  | autocreate global mbox - synchronous  | autocreate global mbox - synchronous  | autocreate global mbox - synchronous  | autocreate global mbox - asynchronous (to support development of the Data Co-op, which will be released later in 2016)  |
|  mboxCreate  | standard  | standard  | standard  | ajax  |

>## Create an Order Confirmation mbox - mbox.js {#task_0036D5F6C062442788BB55E872816D82}The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y." 
<draft-comment otherprops="merge">
  ov/t_orderconfirm_create.xml 
</draft-comment>
>[!NOTE]
>
>If users make purchases on your website, we recommend implementing an Order Confirmation mbox even if you use Analytics for Target (A4T) for your reporting.



>[!NOTE]
>
>You can also create an Order Confirmation mbox for ` at.js` using the same method; however, the ` at.js` method is preferred. For more information, see [ Create an OrderConfirmPage mbox - at.js ](c_target-atjs-implementation.md#task_E85D2F64FEB84201A594F2288FABF053). 



>1. In your order details page, insert the mbox script following the model below.
>1. Replace the WORDS IN CAPITAL LETTERS with either dynamic or static values from your catalog.


>       >[!NOTE]
>       >
>       >Use comma delimiting to separate multiple product IDs.

>       **Tip:**You can also pass order information in any mbox (it does not need to be named ` orderConfirmPage`). You can also pass order information in multiple mboxes within the same campaign. 
>    
>       ```
>       <div class="mboxDefault"> 
>          <!-- CONTENT TO SHOW IF NO OFFERS AVAILABLE. --> 
>       </div> 
>       <script type="text/javascript">    
>          mboxCreate('orderConfirmPage', 
>          'productPurchasedId=PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3', 
>          'orderTotal=ORDER TOTAL FROM YOUR ORDER PAGE', 
>          'orderId=ORDER ID FROM YOUR ORDER PAGE'); 
>       </script> 
>       ```

>## mbox.js Frequently Asked Questions {#concept_240B3B89071A4D35AD2EFF409EC86F1E}Answers to frequently asked questions about 
<filepath>
  mbox.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov2/c_mboxjs-frequently-asked-questions.xml 
</draft-comment>
## What is the impact of mbox.js on page-load times? {#section_90B3B94FE0BF4B369577FCB97B67F089}

For more information, see [ Understanding the Target JavaScript Libraries ](c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB). 

## Why do I get "Parser-blocking" warning messages in Google Chrome when using mbox.js and document.write ? {#section_355A3A5BF02F42EEB8271C96EF41590A}

This console message displays when using Chrome in many scenarios in which the ` document.write` function is used within the ` mbox.js` file. This is a warning message and should not affect your activity setup process. 
The best way to prevent this situation is to [ migrate your Target implementation to the ` at.js` JavaScript library ](c_target-atjs-implementation.md#task_DE55DCE9AC2F49728395665DE1B1E6EA), which doesn't use the ` document.write` function. Using ` at.js` provides many advantages versus using ` mbox.js`. For more information, see [ at.js Frequently Asked Questions ](c_target-atjs-implementation.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769). 

## Why are my mboxes not firing on my web pages? {#section_4BA5DA424B734324AAB51E4588FA50F5}

Target customers sometimes use cloud-based instances with ` Target` for testing or simple proof-of-concept purposes. These domains, and many others, are part of the [ Public Suffix List ](https://publicsuffix.org/list/public_suffix_list.dat). 
Modern browsers won't save cookies if you are using these domains unless you customize the ` cookieDomain` setting using targetGlobalSettings(). For more information, see [ Using Cloud-Based Instances with Target ](c_targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566). 

## What is the domain tt.omtrdc.net that Target server calls go to? {#section_999C29940E8B4CAD8A957A6B1D440317}

` tt.omtrdc.net` is the domain name for Adobe's EDGE network, used to receive all server calls for Target. 
>## mbox.js Functions {#concept_F607080C3FF54AE9AD7F8CFB4D685B07}List of mbox.js functions to use when implementing with mbox.js. 
<draft-comment otherprops="merge">
  ov/c_mboxjs-function 
</draft-comment>
>[!NOTE]
>
>If you are using ` at.js`, these methods do not apply. 




<table id="table_0E99AD9702944F749BE37DCBAA34DD76"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Method </th> 
   <th colname="col2" class="entry"> Notes </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.getName() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.getURL() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.getDiv() </span> </p> </td> 
   <td colname="col2"> Returns the <span class="codeph"> div </span> associated with the mbox (containing default content or an offer) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.getParameters() </span> </p> </td> 
   <td colname="col2"> An array of parameters with two fields, name and value </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.setOnError() </span> </p> </td> 
   <td colname="col2"> Example: <p> <span class="codeph"> mbox.setOnError(function() { alert(this.getName() +" had error"}); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.setMessage(message) </span> </p> </td> 
   <td colname="col2"> You can see message in debug window . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.activate() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.cancelTimeout() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.finalize() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getDefaultDiv() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getDiv() </span> </p> </td> 
   <td colname="col2"> Returns the <span class="codeph"> div </span> associated with the mbox (containing default content or an offer) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getEventTimes() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getFetcher() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getId() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getImportName() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getName() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getOffer() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getParameters() </span> </p> </td> 
   <td colname="col2"> An array of parameters with two fields, name and value . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getURL() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.getURLBuilder() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.hide() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.isActivated() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.load() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.loaded() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.setEventTime() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.setFetcher() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.setMessage() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.setMessage(message) </span> </p> </td> 
   <td colname="col2"> View message in debug window . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.setOffer() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.setOnError() </span> </p> </td> 
   <td colname="col2"> Example: <p> <span class="codeph"> mboxCurrent.setOnError(function(){ alert(this.getName() +" had error"}); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.setOnLoad() </span> </p> </td> 
   <td colname="col2"> Example: <p> <span class="codeph"> mboxCurrent.setOnLoad(function(){alert(this.getName()+" loaded")}); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.show() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxCurrent.showContent() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.addOnLoad(action) </span> </p> </td> 
   <td colname="col2"> Action is called when page loads. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getMboxes().each() </span> </p> </td> 
   <td colname="col2"> Example: <p> <span class="codeph"> mboxFactoryDefault.getMboxes().each(function() { alert(mbox.getName()) }; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getMboxes().length() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getPageId() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getPCId().getId() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getSessionId().getId() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactories.get('default').getSessionId().forceId("1276011116668"); </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactories.get('default').getPCId().forceId("1276011116668"); </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.create() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.disable() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.enable() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.get() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getCookieManager() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getDisableReason() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getEllapsedTime() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getEllapsedTimeUntil() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getMboxes() </span> </p> </td> 
   <td colname="col2"> Returns an <span class="codeph"> mboxList </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getSignaler() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getURLBuilder() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.isAdmin() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.isDomLoaded() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.isEnabled() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.isSupported() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.limitTraffic() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.update() </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getCookieManager().getCookie("name")//!= null) { </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxFactoryDefault.getCookieManager().setCookie(_name,_value, _duration); </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

>## mbox.js Version Details {#reference_DBB5EDB79EC44E558F9E08D4774A0F7A}This page shows changes to each version of 
<filepath>
  mbox.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov/r_mboxjs_change_log.xml 
</draft-comment>
<a id="section_C915897051644B40BFF4DC6B914944C2"></a>


>[!NOTE]
>
>We recommend that all ` mbox.js` users upgrade to version 57 or later. Some users have experienced timeout issues when ` target.js` couldn't be loaded. Version 57 fixed that issue. However, if you are using the ` Marketing Cloud Visitor ID` service, version 58 or later is required. 


The way Target responds to calls from your page depends on the version of the Target library you are using, whether the visitor ID implementation is present, and whether the visitor ID exists. For information, see [ Target Call Responses by Library Version ](t_mbox_download.md#concept_A95A4758A1E7405D947E9B4BCB5D62F0). 

>[!NOTE]
>
>The ` mbox.js` library is no longer being developed. All customers should migrate from ` mbox.js` to ` at.js`. For more information, see [ Migrate to at.js from mbox.js ](c_target-atjs-implementation.md#task_DE55DCE9AC2F49728395665DE1B1E6EA). 


This section contains information about the following ` mbox.js` versions: 

## mbox.js version 63 {#section_ED8EFCF653A845ED8927F759578C4A33}

**Target Release:**17.7.1 
` mbox.js` version 63 is now available. For more information, see [ Download mbox.js ](https://marketing.adobe.com/resources/help/en_US/target/ov/t_target-download-config-mbox.html). 
The following enhancements and fixes are included in ` mbox.js` version 63: 

* Fixes an issue with SDID generation when using ` mboxDefine()` and ` mboxUpdate()`. This affects only clients that have Visitor API on the page.


## mbox.js version 62 {#section_723A9119FE204183847D3B0929A99B41}


* Fixed flicker issues in redirect activities when viewed in Google Chrome browsers.

* Added ` secureOnly` setting that indicates whether ` mbox.js` should use HTTPS only or be allowed to switch between HTTP and HTTPS based on the page protocol. This is an advanced setting that defaults to False. 



## mbox.js version 61 {#section_F3B59C5578B64883AE013B9342151193}

**Target Release:** 16.7.2 
**Release Date:** July 28, 2016 
mbox.js version 61 contains the following enhancements:

* The mboxSession ID generation algorithm in the JavaScript Date API now generates a random string instead of using a timestamp plus a random string.
* The following details apply only if you have the Visitor API on the page: 
    * ` mbox.js` version 61 doesn't override the Visitor API ` loadTimeout` property. Clients can use ` visitorApiTimeout` + ` visitorApiPageDisplayTimeout` to control Visitor API integration. 

    * Added an ` optoutEnabled` setting to support future Adobe Marketing Cloud opt-out functionality. The default value is false. If this property is enabled, all requests execute asynchronously against the ` /ajax` endpoint, just like version 60. 

    * Body hiding is disabled by default. Target uses body hiding only when global mbox auto-create is enabled and body hiding is enabled.

    * If there are no Marketing Cloud Visitor ID cookies, all requests execute asynchronously against ` /ajax` on the first page load. On the second page load, Target uses the normal flow because Visitor ID values are already present. 

    * If you use Adobe Analytics as your activity's reporting source, you do not need to specify a tracking server during activity creation if you are using ` mbox.js` version 61 (or later) or ` at.js` version 0.9.1 (or later). The ` mbox.js` or ` at.js` library automatically sends tracking server values to ` Target`. During activity creation, you can leave the ` Tracking Server` field empty on the ` Goals &amp; Settings` page. 




## mbox.js version 60 {#section_3BDAB885FA13444A8D35940A4BFF5825}

**Target Release:** 16.4.1 
**Release Date:** April 21, 2016 
By default, page content is not hidden. Version 60 hides page content only when the "auto-create global mbox" option is enabled. It uses the CSS ` opacity:0` property for page hiding instead of ` display:none`. This ensures proper delivery for responsive sites and aligns with ` at.js`. 
You can enable body hiding using two settings:

* ` bodyHidingEnabled` The default value is false, which means HTML BODY is not hidden.

* bodyHiddenStyle The default value is ` body{opacity:0}`. This value can be changed to something different, like ` body{display:none}`. 


These settings can be overridden by including something like:

```
<script> 
window.targetGlobalSettings = { 
 bodyHidingEnabled: true, 
 bodyHiddenStyle: "body{opacity:0}", 
 visitorApiPageDisplayTimeout: 2000 
}; 
</script>
```

The page hiding technique uses style tags to add and remove styles. This ensures that the site's styles remain unchanged after the page hiding code executes.
**DTM Users:** Note that this will prevent you from using the Automatic import option since there is no way to save the above configuration in the Target UI. You will have to use the instructions above and then paste the contents into the code box of the Custom hosting option. 
Also in Version 60, if the ` visitorAPI.js` file is present for the Marketing Cloud Visitor ID service, all mboxes are requested via an AJAX endpoint. This is required because Visitor API methods are asynchronous. One benefit of this approach is that the Start Render time is decreased dramatically, because mbox requests do not block rendering. However, this also means that all ` Target` offer content runs asynchronously, so all offer code must be written accordingly. Offers containing ` document.write` and other code that assumes it will run on initial page load will not execute as expected. 

* V60 asynchronous calls When using v60 with the visitor id service, all mbox calls are made asynchronously. This is a change from how mboxes have always worked, so be careful if upgrading to this version. Review the [ Asynchronous Considerations ](c_target-atjs-implementation.md#section_B586360A3DD34E2995AE25A18E3FB953) section of the ` at.js` documentation ( ` at.js` also uses asynchronous calls) to understand some of the risks. 

* New Visitor scenarios might have flicker When using v58 to v60 with the visitor id service, mbox calls will wait for the visitor id to be set before firing (or until a timeout has occurred). This happens on the first page load of a new visitor.



## mbox.js version 59 {#section_FF0E70C4C17E402D8374DE428C5D996E}

**Target Release:** 16.2.1 
**Release Date:** February 17, 2016 
mbox.js version 59 contains the following enhancements:

* Mbox disabled has been lowered to 30 minutes
* An issue related to page hiding/unhiding has been fixed Rather than using ` display:none` to hide the page as in version 58, ` opacity:0` is used. This resolves issues with responsive-designed sites that resulted from the previous method of hiding the page. 



## mbox.js version 58 {#section_5070B0D1C87F4937BB97727923DD36C7}

**Target Release:** 15.7.1 
**Release Date:** July 30, 2015 
This version of mbox.js is required if you use Analytics as the reporting source for Target and is highly recommended for Profiles and Audiences.
Version 58 of mbox.js ensures the Marketing Cloud Visitor ID service returns with a visitor ID before Target calls are made. This ensures that audience data shared through the Profiles and Audiences core service are available for the first Target call in the visitor's session. To avoid flickering of default content before test content returns, Target hides the ` <BODY>` until the visitor ID service returns. ` display:none` is used to hide the page. 
This update also fixes an issue when using Analytics as the reporting source for Target that caused an inflated number of visitors to be reported in Analytics for visits that only included one page.
Mbox.js sets timeout values in case the visitor ID service does not return. Default timeout for the visitor ID service is 500ms (0.5 seconds). An additional timeout sets the upper limit for how long the ` <BODY>` tag will be hidden. That default is 500ms (0.5 seconds). These timeouts can be changed by inserting the following code before the mbox.js reference on each page: 

```
<script> 
window.targetGlobalSettings = { 
 visitorApiTimeout: 500, 
 visitorApiPageDisplayTimeout: 500 
}; 
</script> 

```

Mbox.js version 58 and later executes non-JavaScript content for the global mbox immediately after the HTML ` BODY` tag is present. JavaScript content inside ` <script>` tags for the global mbox executes after the ` DOMContentLoaded` event is fired. This order of content delivery ensures that JavaScript content for the global mbox is delivered and rendered properly. 

## mbox.js version 57 {#section_6BA1CDBF75B14A94B59E8624ACF583D4}

**Target Release:** 15.4.1 
**Release Date:** April 21, 2015 
The following changes have been made in this version:

* Auto-created global mbox response for Target Standard no longer uses document.write() or creates a &lt;div&gt; element. This removes the requirement for the mbox.js file to be the last item in the &lt;head&gt; of the page. Strong QA is recommended when upgrading to this new version.
  This change might cause changes in behavior when delivering some offer types. Here are the specific conditions that will need to be considered:

    * HTML content returned as part of a "plug in offer" does not render correctly, but JavaScript within the offers executes as expected.
    * JavaScript offers that are being returned to the global mbox can have the JavaScript code embedded in the ` <script>` tag, or referenced by a ` src` attribute. To do this, add the ` async` attribute to the script call, as follows: 
      ` <script src='external-url' async='true'></script>` 
      Note that the ` async` attribute has limited support in Internet Explorer (details here: [ https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility ](https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility)) so you should exclude visitors who use older IE versions from tests that include these 3rd party scripts. 



* Fixed problems reported in Version 56 due to changes in the Extra JavaScript section of mbox.js. All code in the Extra JavaScript section is again available in the global scope.

The following functionality is not supported in mbox.js version 57:

* An auto-created global mbox generated in Target Standard does not work with hosted offer types from Target Classic. Hosted offer types include "offer on your site" and "offer outside Test&amp;Target." This means that in Target Classic, you must not select the auto-created global mbox from Target Standard when one of these offers is required.

* Only JavaScript plugins are supported. If a plugin's offer combines JavaScript code, and HTML, then the JavaScript code is executed but the HTML content is not shown.


mbox.js version 57 also includes important fixes:

* Fixed an issue that caused the SiteCatalyst plugin to not work in mbox.js v56.
* Fixed an issue that resulted in extra JavaScript errors due to scoping change.
* Revert changes to constructor of mboxFactory.


## mbox.js version 56 {#section_C4F4A53584B741FF9FD907D81CB7E164}

**Target Release:** 15.1.2 
**Release Date:** February 17, 2015 

>[!NOTE]
>
>Some users have experienced timeout issues when ` target.js` couldn't be loaded. Version 57 fixed that issue. However, if you are using the ` Marketing Cloud Visitor ID` service, version 58 or later is required. 


The following changes have been made in this version:

* Changes for Premium Recommendations to support passing parameters into global mbox
* Adds a 5 second timeout to the target.js load call. In the rare case that the file doesn't load, the page will render and no Target Standard activities will display.
* Moved "extra JavaScript" to be executed before global mbox All settings in v56+ are name spaced. If there are functions declared in "extra JavaScript," they must be prefixed with ` window`. 
  For example:
  ` function foo {` 
  ` }` 
  Becomes:
  ` window.foo = function() {` 
  ` }` 
  Any variables that should be globally accessible must also be prefixed with ` window`. 

* Added a cookie called "em-disabled" that mbox.js gives to the user if target.js fails to load during delivery. This cookie prevents offers created using the Visual Experience Composer from rendering on the site. Users with this cookie neither see the test content nor get counted in those activity reports. All other offer content (from campaigns in Target Classic for example) will continue to load. The cookie has a lifetime of 30 min from the time of load failure.


## Previous Releases {#section_FAB0A088308A42BEA855936F4E7D89C6}



<table id="table_2311674B4A054BFE825854743EB803F1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Version </th> 
   <th colname="col002" class="entry"> Target Release </th> 
   <th colname="col02" class="entry"> Date </th> 
   <th colname="col2" class="entry"> Changes </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 55 </td> 
   <td colname="col002"> 15.1 </td> 
   <td colname="col02"> January 19, 2015 </td> 
   <td colname="col2"> Modifies version 53 with IE fixes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 54 </td> 
   <td colname="col002"> 14.9.2 </td> 
   <td colname="col02"> September 30, 2014 </td> 
   <td colname="col2"> <p>Changes the global mbox implementation to AJAX from document.write. This removes the requirement for the mbox.js file to be the last item in the page's &lt;head&gt; section. This version is only available via API. Clients can download it and use this mbox.js file. Some sites experience content flicker with this implementation, so please validate the integration on your site.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 53 </td> 
   <td colname="col002"> 14.9.1 </td> 
   <td colname="col02"> September 14, 2014 </td> 
   <td colname="col2"> Fixed an issue where Target page params do not fire correctly in Internet Explorer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 52 </td> 
   <td colname="col002"> 14.8 </td> 
   <td colname="col02"> August 14, 2014 </td> 
   <td colname="col2"> <p> 
     <!--TNT-19408--> <span class="codeph"> mboxParameter </span> function now works in Target Standard and Premium. </p> <p>Fixed an issue that kept Analytics tracking from working in IE 9 &amp; 11. This change only affects users of Analytics.</p> <p> 
     <!--TNT-19403-->Now you can <a href="https://marketing.adobe.com/resources/help/en_US/target/ov/c_pass_parameters_to_global_mbox.html" format="https" scope="external"> pass in parameters </a> as an array, as a JSON object, or as a comma-delimited list (previously supported) to target-global-mbox using the <span class="codeph"> targetPageParams() </span> function. </p> <p> 
     <!--TNT-19117-->Renamed <span class="codeph"> M2PcId </span> and everything related to VisitorId. </p> <p> 
     <!--TNT-16921-->Allow the <span class="codeph"> defaultDiv </span> of a registered mbox to be cleared. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 51 </td> 
   <td colname="col002"> 14.6 </td> 
   <td colname="col02"> June 25, 2014 </td> 
   <td colname="col2"> <p>Fixed a bug that set an incorrect cookie in sites with two characters in their top-level domain.</p> <p>Fixed a minor bug in mbox.js that caused hashtag values to be returned.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 50 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Improved synchronization between Target Standard and Target Classic. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 49 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Improved Internet Explorer 10 support for nested mboxes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 48 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Added support for Adobe Analytics as the reporting source for Target. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 47 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> mbox.js now supports using a custom global mbox name for Target Standard. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 46 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> 
    <!--TNT-17519, TGT-1547, TGT-1497--> Added complete support for Marketing Cloud visitor ID service for Target Standard's single-line-of-code implementation. This enables server-side Adobe Analytics integration and the Marketing Cloud shared profile. <p>Fixed an issue with delivering content in IE10 in document mode.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 45 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Added complete support for Marketing Cloud visitor ID service. This enables server-side Adobe Analytics integration and the Marketing Cloud shared profile. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 44 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> 
    <!--TNT-18142-->Added new parameter in URL by mboxVizTarget: <p> <span class="codeph"> mboxDOMLoaded </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 43 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Added support for Target Standard. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 42 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Added initial support for Marketing Cloud shared visitor ID service. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 41 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> 
    <ol id="ol_07CF02C8B272406694B8FFC5F7D02C8F"> 
     <li id="li_732204D00534423B80391F4E801FC85D">Even with x-only setting, disable the first party cookie to improve load time and prevent continuous page refreshes <p>A timeout cookie is set if the call to Target fails to return in time. This is a faster method than using only the 3rd-party cookie. With just the 3rd-party cookie, the page is continually refreshed while waiting for a good response from Target's servers.</p> </li> 
     <li id="li_F9E3078A5348450684E55D6EBC1863C1">Fixed traffic limitation to occur only when <span class="filepath"> mbox.js </span> is enabled 
      <!--(#17540)--> <p>This issue occurred if a customer had a traffic limitation on their mbox.js, causing the timeout setting to not work. This resulted in the page refreshing while waiting foir a good response from the Target servers.</p> </li> 
     <li id="li_B20DFA3CAB964D87B92FC7AD1B421BC3">Fixed SiteCalyst plugin to always use the Ajax fetcher 
      <!--(#16527)--> <p>Prior to this change, there were some situations for users of the Test&amp;Target to SiteCatalyst plugin where, depending on when the plugin loaded, a document.write that would wipe out the page could be triggered.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 38 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Added support for page-based SiteCatalyst to Test&amp;Target integration (must be enabled) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 37 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Encoded URL keys </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 36 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> Changed mbox to use <span class="filepath"> tt.omtrdc.net </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 35 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> <p> </p> <p> 
     <ol id="ol_DB2B0D9035E24AAD80D2689777CE241B"> 
      <li id="li_CE57D9EC5BC3475B8B2887632CC21823">Mbox debug is now always remote</li> 
      <li id="li_96F8FC4CB17648C097CD401538FB078C">Added the <span class="codeph"> mboxTime </span> parameter. This parameter is the time as the user sees it, in ms since the epoch, GMT. This is only calculated once. </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 34 </td> 
   <td colname="col002"> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> 
    <ol id="ol_DE06E076E7564F44966F22A0E3131335"> 
     <li id="li_5038B012262848ADB03D4EB39E24D304">Always try to get the latest default <span class="codeph"> div </span> instead of referring to a cached version. <p>This fixes a problem with a cached default content <span class="codeph"> div </span> not being in the DOM due to an <span class="codeph"> mboxUpdate </span>, which provided the content for the default <span class="codeph"> div </span>. </p> <p> <span class="codeph"> mbox.getDefaultDiv </span> has a new optional boolean parameter. If <span class="codeph"> true </span>, it returns the current default <span class="codeph"> div </span>. If <span class="codeph"> false </span>, it returns the last cached default <span class="codeph"> div </span>. 
       <!--(initially in #9501, updated in #7529)--> </p> </li> 
     <li id="li_24DC79ECDED34D58BA3BD4CCF3CFE878">Updated <span class="codeph"> mbox.loaded </span> to support Ajax load 
      <!--(see #7529)--> </li> 
     <li id="li_F43C29D0F60A44C8B063377ED69030AD"> <span class="codeph"> mboxURL </span> parameter is now encoded using <span class="codeph"> encodeURIComponent </span> rather than <span class="codeph"> escape </span> 
      <!--see #8965--> </li> 
     <li id="li_7E3080E931C74304B99DAD70C8F378FF"> 
      <!--(see #10010)-->Test whether <span class="codeph"> encodeURIComponent </span> is supported by the browser and show default content if it isn't. Also removed the following mbox.js config options: 
      <ul id="ul_66BAA15593194833ACCB2234D9182B45"> 
       <li id="li_5505591AE70F45AFBB27B57DB4A02552"> <span class="codeph"> encode_mbox_parameters </span> </li> 
       <li id="li_FB2A7539397F47F4AAA4B1962CF271C0"> <span class="codeph"> mbox_signal_support </span> </li> 
      </ul> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

