---
description: Information to help you set several settings on the at.js Settings page.
keywords: Implementation;at.js;at.js advanced settings;client code;ims organization id;profile lifetime;x-domain;timeout;time out;legacy browser support;Autocreate global mbox;Global mbox name
seo-description: Information to help you set several settings on the at.js Settings page.
seo-title: Configure at.js
solution: Target
subtopic: Getting Started
title: Configure at.js
topic: Standard
uuid: 7a0ec8b2-551e-4325-b46b-67019fecc5bc
index: y
internal: n
snippet: y
translate: y
---

# Configure at.js


>[!NOTE]
>
>You can override settings in the ` at.js` library, rather than configuring the settings in the Target Standard/Premium UI or by using REST APIs. For more information, see [ targetGlobalSettings()](../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/cmp_at.js_Functions.md#concept_8DACBC47ABDE4279BB102B42609FE506). 



To open the [!UICONTROL  Settings] page: 


1. Click **[!UICONTROL  Setup]** > **[!UICONTROL  Implementation]**. 

1. Select **[!UICONTROL  at.js]** > **[!UICONTROL  Edit at.js Settings]**. 



The section contains the following information: 


* [ Content Delivery Settings](../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/c_target-atjs-advanced-settings.md#section_118D290DFC444509AD8E4AE86C9D92C0)
* [ Advanced Settings](../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/c_target-atjs-advanced-settings.md#section_33B697B77BA64A01B5939D7EC75231F2)
* [ Code Settings](../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/c_target-atjs-advanced-settings.md#section_D41C905D0F8149949F525C85F2CCFF7F)


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
   <td colname="col2"> <p>Select whether to embed the global mbox call in the <span class="filepath"> at.js</span> file to automatically fire on each page load. </p> <p>Changing this setting affects both <span class="filepath"> at.js</span> and <span class="filepath"> mbox.js</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Global mbox name </td> 
   <td colname="col2"> <p>Select a name for the global mbox. By default, this name is <span class="codeph"> target-global-mbox</span>. </p> <p> Special characters, including ampersands (&amp;), can be used in mbox names with <span class="codeph"> at.js</span>. </p> <p>Changing this setting affects both <span class="filepath"> at.js</span> and <span class="filepath"> mbox.js</span>. </p> </td> 
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
   <td colname="col2"> <p>The client code is a client-specific sequence of characters often required when using the <span class="keyword"> Target</span> APIs. </p> <p>This setting cannot be changed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IMS Organization ID </td> 
   <td colname="col2"> <p> This ID ties your implementation to your <span class="keyword"> Adobe Experience Cloud</span> account. </p> <p>This setting cannot be changed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profile Lifetime </td> 
   <td colname="col2"> <p>This setting determines how long visitor profiles are stored. By default, profiles are stored for two weeks. </p> <p>To change the <span class="wintitle"> Profile Lifetime</span> setting, contact <a href="http://helpx.adobe.com/marketing-cloud/contact-support.html" format="http" scope="external"> Client Care</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> X-Domain </td> 
   <td colname="col2"> <p>Determines whether the browser sets cookies in your own domain (1st party cookies), Target's domain, or both. </p> <p>Changing this setting affects both <span class="filepath"> at.js</span> and <span class="filepath"> mbox.js</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Timeout </td> 
   <td colname="col2"> <p>If <span class="keyword"> Target</span> does not respond with content within the defined period, the server call times out and default content is displayed. Additional calls continue to be attempted during the visitor's session. The default is 15 seconds. </p> <p>Changing this setting affects both <span class="filepath"> at.js</span> and <span class="filepath"> mbox.js</span>. </p> <p>The <span class="filepath"> at.js</span> library uses the timeout setting in <span class="codeph"> XMLHttpRequest</span>. The timeout starts when the request is fired and stops when <span class="keyword"> Target</span> gets a response from the server. For more information, see <span class="codeph"><a href="https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout" format="https" scope="external"> XMLHttpRequest.timeout</a></span> on the Mozilla Developer Network. </p> <p>If the specified timeout occurs before receiving the response, default content is shown and the visitor might be counted as a participant in an activity because all data collection happens on the <span class="keyword"> Target</span> edge. If the request reaches the <span class="keyword"> Target</span> edge, the visitor is counted. </p> <p>Consider the following when configuring the timeout setting: </p> <p> 
     <ul id="ul_F9154E3EC6BF41ECA49216BF4373AF6C"> 
      <li id="li_C26553FD85B94850944F623CA94CD370"> <p>If the value is too low, users might see default content most of the time, although the visitor could be counted as a participant in the activity. </p> </li> 
      <li id="li_6BDF05026AA747D2A494BE5E5A199717"> <p>If the value is too high, visitors might see blank regions on your web page or blank pages if you use body hiding for extended periods of time. </p> </li> 
     </ul> </p> <p>To get a better understanding of mbox response times, look at the Network tab in your browser's Developer Tools. You can also use third-party web performance monitoring tools, such as Catchpoint. </p> <p> <p>Note: The <a href="../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/cmp_at.js_Functions.md#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> visitorApiTimeout setting</a> ensures that <span class="keyword"> Target</span> doesn't wait for the Visitor API response for too long. This setting and the <span class="wintitle"> Timeout</span> setting for <span class="codeph"> at.js</span> described here do not affect each other. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Legacy Browser Support </td> 
   <td colname="col2"> <p> <p>Note: The <span class="wintitle"> Legacy Browser Support</span> option is available in <span class="codeph"> at.js</span> version 0.9.3 and earlier. This option was removed in <span class="codeph"> at.js</span> version 0.9.4. For a list of browsers supported by <span class="codeph"> at.js</span>, see <a href="../../../c_seting_up_target/c_implementing_target/c_target-requirements/r_supported_browsers.md#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Supported Browsers</a>. </p> </p> <p> Legacy browsers are older browsers that do not fully support CORS (Cross Origin Resource Sharing). These browsers include: Internet Explorer browsers earlier than version 11 and Safari versions 6 and below. If Legacy Browser Support is disabled, Target does not deliver content or count visitors in reports on these browsers. If this option is enabled, it is recommended to do quality assurance across older browsers to ensure a good customer experience. </p> </td> 
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

