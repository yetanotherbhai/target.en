---
description: Information about the status of traditional Target debugging techniques when used with at.js.
keywords: at.js;debug at.js;adobe Experience Cloud debugger;atlist;mboxhighlight
keywords__at_debug: console
keywords_mboxdebug: x-cookie
keywords_mboxdebux: x-profile
keywords_mboxdisable: 1
keywords_mboxtrace: console
seo-description: Information about the status of traditional Target debugging techniques when used with at.js.
seo-title: Debugging at.js
title: Debugging at.js
topic: Target
uuid: 11f95959-56fb-4ea4-a0b1-674cdf67047b
index: y
internal: n
snippet: y
translate: y
---

# Debugging at.js

Debugging options are slightly different for mbox calls using [!DNL  at.js]. 

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
      <li id="li_4610283D0A4649469C0D88FCE8F6D47A">Use the Experience Cloud Debugger, mboxTrace, and ttMETA </li> 
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
   <td colname="col1"> <p>Adobe Marketing Cloud Debugger bookmarklet </p> </td> 
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

