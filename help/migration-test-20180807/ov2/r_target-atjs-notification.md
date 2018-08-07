---
description: Information about at.js custom events, which lets you know when an mbox request or offer fails or succeeds.
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Information about at.js custom events, which lets you know when an mbox request or offer fails or succeeds.
seo-title: at.js custom events
solution: Target
title: at.js custom events
topic: Standard
uuid: 33b2ef24-9cd1-4b4c-aceb-5bed62c7f229
index: y
internal: n
snippet: y
translate: y
---

# at.js custom events


>Historically, ` mbox.js` didn't let other JavaScript code that runs on the page know what happens behind the scenes. With the advancement of ` at.js`, we had a unique opportunity to fix this issue. 
>According to our customers there are several scenarios that they would like to be notified of, including:
>
>* An mbox request failed due to timeout, wrong status code, JSON parse error, etc.

>* An mbox request succeeded.

>* Offer rendering failed due to wrapping mbox element missing, selector can not be found, etc.

>* Offer rendering succeeded. DOM changes have been applied.


>Pre-defined events have a structure that allows you to extract the required data, based on event type.
>To make sure that events can be used in different scenarios, the custom events have a payload object that is assigned to the detail property of the event object (that is passed to the handler). Also to avoid passing strings as event names, the events are exposed as constants using ` adobe.target.event` namespace. 
>This section contains the following information:
>
>* [ Structure ](r_target-atjs-notification.md#section_0E5C9A13DE234A5DAECBCBF9F23F94FE)
>* [ Usage ](r_target-atjs-notification.md#section_0500FF09D3A04450B5DC8F85C6F793E0)


## Structure {#section_0E5C9A13DE234A5DAECBCBF9F23F94FE}



<table id="table_5B00CCB9BA3C4EE491D6460450823680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Key </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>type</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Event type, can be one of ( <span class="codeph"> adobe.target.event </span>), e.g.: </p> <p> 
     <ul id="ul_D18535E9FF78405E9D76618D0A745321"> 
      <li id="li_14D4D4F8BCC44DD19E9822B9E07FC00C"> <p>at-request-failed - <span class="codeph"> adobe.target.event.REQUEST_FAILED </span> </p> </li> 
      <li id="li_782D2123D58049F1B561C9FEE504FE98"> <p>at-request-succeeded - <span class="codeph"> adobe.target.event.REQUEST_SUCCEEDED </span> </p> </li> 
      <li id="li_BF1821570E9E45769E088890EF211763"> <p>at-content-rendering-failed - <span class="codeph"> adobe.target.event.CONTENT_RENDERING_FAILED </span> </p> </li> 
      <li id="li_2796F4A3A68B419295DA8249A174E044"> <p>at-content-rendering-succeeded - <span class="codeph"> adobe.target.event.CONTENT_RENDERING_SUCCEEDED </span> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mbox</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>mbox name</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>message</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Contains human-readable description, such as what happened, the error message, etc.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tracking</p> </td> 
   <td colname="col2"> <p>Object</p> </td> 
   <td colname="col3"> <p>Contains the <span class="codeph"> sessionId </span> and <span class="codeph"> deviceId </span>. In some cases, <span class="codeph"> deviceId </span> could be missing because <span class="keyword"> Target </span> couldn't retrieve it from edge server. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Usage {#section_0500FF09D3A04450B5DC8F85C6F793E0}


```
document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(event) { 
  console.log('Event', event); 
});
```
