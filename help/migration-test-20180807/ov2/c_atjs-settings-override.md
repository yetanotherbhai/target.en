---
description: You can override settings in the at.js library using targetGlobalSettings(), rather than configuring the settings in the Target Standard/Premium UI or by using REST APIs.
keywords: Implementation;at.js;at.js advanced settings;client code;secureOnly;ims organization id;profile lifetime;x-domain;timeout;legacy browser support;Autocreate global mbox;Global mbox name;override settings
seo-description: You can override settings in the at.js library using targetGlobalSettings(), rather than configuring the settings in the Target Standard/Premium UI or by using REST APIs.
seo-title: targetGlobalSettings()
solution: Target
subtopic: Getting Started
title: targetGlobalSettings()
topic: Standard
uuid: 32dafe2c-9a2c-4ebb-b606-5929b87ca2e4
index: y
internal: n
snippet: y
translate: y
---

# targetGlobalSettings()

There are use cases, especially when ` at.js` is delivered via ` Dynamic Tag Management` (DTM) when you would like to override some of the settings. 
This section contains the following information:

* [ Settings ](c_atjs-settings-override.md#section_42C759AE9B524A43B8659018677224B8)
* [ Usage ](c_atjs-settings-override.md#section_9AD6FA3690364F7480C872CB55567FB0)


## Settings {#section_42C759AE9B524A43B8659018677224B8}

You can override the following settings:


<table id="table_8819BEE90E8244AEB6EDB3E5C8693FA7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Settings </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Default Value </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>clientCode</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Value set via UI</p> </td> 
   <td colname="col4"> <p>Represents client code</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>serverDomain</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Value set via UI</p> </td> 
   <td colname="col4"> <p>Represents Target edge server</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cookieDomain</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>If possible set to top level domain</p> </td> 
   <td colname="col4"> <p>Represents the domain used when saving cookies</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>crossDomain</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Value set via UI</p> </td> 
   <td colname="col4"> <p>Indicates whether cross-domain tracking is enabled or not.</p> <p>The allowed values are:</p> <p> 
     <ul id="ul_3D197DC987354C9A80C15FB76654FE61"> 
      <li id="li_7EAAB587A34441ECA337AEB511278684"> <p>disabled</p> </li> 
      <li id="li_FE98D6B22A604D2691222681E3BAEE08"> <p>enabled</p> </li> 
      <li id="li_EA29FC67438646F9B5EFE6288DF2EEBB"> <p>x-only</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>timeout</p> </td> 
   <td colname="col2"> <p>Number</p> </td> 
   <td colname="col3"> <p>Value set via UI</p> </td> 
   <td colname="col4"> <p>Represents Target edge request timeout</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>globalMboxAutoCreate</p> </td> 
   <td colname="col2"> <p>Boolean</p> </td> 
   <td colname="col3"> <p>Value set via UI</p> </td> 
   <td colname="col4"> <p>Indicates whether the global mbox request should be fired or not</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>visitorApiTimeout</p> </td> 
   <td colname="col2"> <p>Number</p> </td> 
   <td colname="col3"> <p>2000 ms = 2 s</p> </td> 
   <td colname="col4"> <p>Represents the Visitor API request timeout</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>enabled</p> </td> 
   <td colname="col2"> <p>Boolean</p> </td> 
   <td colname="col3"> <p>true</p> </td> 
   <td colname="col4"> <p>Indicates whether <span class="codeph"> at.js </span> as library is enabled, meaning if it should execute anything or not. The main use case for this setting being opt-out cookies or other custom decisions that would disable <span class="codeph"> at.js </span> functionality </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>defaultContentHiddenStyle</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>visibility: hidden</p> </td> 
   <td colname="col4"> <p>Used only for wrapping mboxes that use DIV with class name "mboxDefault" and are executed via <span class="codeph"> mboxCreate() </span>, <span class="codeph"> mboxUpdate() </span>, or <span class="codeph"> mboxDefine() </span> to hide default content </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>defaultContentVisibleStyle</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>visibility: visible</p> </td> 
   <td colname="col4"> <p>Used only for wrapping mboxes that use DIV with class name "mboxDefault" and are executed via <span class="codeph"> mboxCreate() </span>, <span class="codeph"> mboxUpdate() </span>, or <span class="codeph"> mboxDefine() </span> to reveal applied offer if any or default content </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bodyHiddenStyle</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>body { opacity: 0 }</p> </td> 
   <td colname="col4"> <p>Used only when <span class="codeph"> globalMboxAutocreate === true </span> to minimize the chance of flicker </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bodyHidingEnabled</p> </td> 
   <td colname="col2"> <p>Boolean</p> </td> 
   <td colname="col3"> <p>true</p> </td> 
   <td colname="col4"> <p>Used to control flicker when <span class="codeph"> target-global-mbox </span> is used to deliver offers created in the <span class="wintitle"> Visual Experience Composer </span>, also known as visual offers </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>imsOrgId</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>IMS ORG ID</p> </td> 
   <td colname="col4"> <p>Represents the IMS ORG ID</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>secureOnly</p> </td> 
   <td colname="col2"> <p>Boolean</p> </td> 
   <td colname="col3"> <p>false</p> </td> 
   <td colname="col4"> <p>Indicates whether <span class="codeph"> at.js </span> should use HTTPS only or be allowed to switch between HTTP and HTTPS based on the page protocol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>overrideMboxEdgeServer</p> </td> 
   <td colname="col2"> <p>Boolean</p> </td> 
   <td colname="col3"> <p>false</p> </td> 
   <td colname="col4"> <p>Indicates if we should use <span class="codeph"> &lt;clientCode&gt;.tt.omtrdc.net </span> domain or <span class="codeph"> mboxedge&lt;clusterNumber&gt;.tt.omtrdc.net </span> domain. If this value is true, <span class="codeph"> mboxedge&lt;clusterNumber&gt;.tt.omtrdc.net </span> domain will be saved to a cookie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>overrideMboxEdgeServerTimeout</p> </td> 
   <td colname="col2"> <p>Number</p> </td> 
   <td colname="col3"> <p>1860000 =&gt; 31 minutes</p> </td> 
   <td colname="col4"> <p>Indicates the cookie lifetime that contains the <span class="codeph"> mboxedge&lt;clusterNumber&gt;.tt.omtrdc.net </span> value. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>optoutEnabled</p> </td> 
   <td colname="col2"> <p>Boolean</p> </td> 
   <td colname="col3"> <p>false</p> </td> 
   <td colname="col4"> <p>Indicates whether Target should call the Visitor API <span class="codeph"> isOptedOut() </span> function. This is part of Device Graph enablement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>selectorsPollingTimeout</p> </td> 
   <td colname="col2"> <p>Number</p> </td> 
   <td colname="col3"> <p>5000 ms = 5 s</p> </td> 
   <td colname="col4"> <p>In <span class="codeph"> at.js </span> 0.9.6, Target introduced this new setting that can be overridden via <span class="codeph"> targetGlobalSettings </span>, </p> <p> <span class="codeph"> selectorsPollingTimeout </span> represents how long the client is willing to wait for all the elements identified by selectors to appear on the page. </p> <p>Activities created via the Visual Experience Composer (VEC) have offers that contain selectors.</p> </td> 
  </tr> 
 </tbody> 
</table>


## Usage {#section_9AD6FA3690364F7480C872CB55567FB0}

This function can be defined before ` at.js` is loaded or in ** ` Setup` ** > ** ` Implementation` ** > ** ` Edit at.js Settings` ** > ** ` Code Settings` ** > ** ` Library Header` **. 
The Library Header field allows you to enter free-form JavaScript. The customization code should look something similar to the following example:

```
window.targetGlobalSettings = {  
   timeout: 200, // using custom timeout  
   visitorApiTimeout: 500, // using custom API timeout  
   enabled: document.location.href.indexOf('http://www.adobe.com') >= 0 // enabled ONLY on adobe.com  
};
```

