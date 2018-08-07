---
description: This function fires a request to report user actions, such as clicks and conversions. It does not deliver activities in the response.
keywords: adobe.target.trackEvent )Options);element;selector;trackEvent;event
seo-description: This function fires a request to report user actions, such as clicks and conversions. It does not deliver activities in the response.
seo-title: adobe.target.trackEvent(options)
solution: Target
title: adobe.target.trackEvent(options)
topic: Standard
uuid: c89a1837-8020-4f22-8bfd-75a26fa2ff70
index: y
internal: n
snippet: y
translate: y
---

# adobe.target.trackEvent(options)


>These event-tracking mbox calls can then be used to define metrics in activities. For more information, see [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924) and [ Create an Order Confirmation mbox - at.js ](t_create_orderconfirm-page-mbox-atjs.md#task_E85D2F64FEB84201A594F2288FABF053). 
>Here are the API details:


><table id="table_F9A0292CB561413F8039E045F8B05E6D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Key </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Required </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> mbox </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> <p>Mbox name</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> selector </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>CSS selectors used to find the HTML elements. The event listeners will be attached to found elements.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> type </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Represents a registered event type. It can be both HTML known events like: click, mousedown etc as well as custom HTML events.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> preventDefault </td> 
   <td colname="col2"> Boolean </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Indicates whether to use <span class="codeph"> event.preventDefault() </span> in the event listener callback. Defaults to false. </p> <p> <p>Note:  Only <span class="codeph"> form[submit] </span>, <span class="codeph"> a[click] </span> are supported. Other scenarios are not supported due to complexity and huge amount of scenarios to support. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> params </td> 
   <td colname="col2"> Object </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Mbox parameters. An object of key-value pairs that has the following structure:</p> <p> <span class="codeph"> { "param1": "value1", "param2": "value2"} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> timeout </td> 
   <td colname="col2"> Number </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Timeout in milliseconds.</p> <p>If not specified, default value is used:</p> <p> <span class="codeph"> {...timeoutInSeconds: 0.15...} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> success </td> 
   <td colname="col2"> Function </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>A callback function used to signal that event has been reported.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> error </td> 
   <td colname="col2"> Function </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>A callback function used to signal that event could not be reported.</p> </td> 
  </tr> 
 </tbody> 
</table>

>**Example** 
>
>```
><a href="http://asite.com">click me!</a>
>```

>plus javaScript code to assign ` trackEvent`: 
>
>```
><script> 
>$('a').click(function(event){ 
>  adobe.target.trackEvent({'mbox':'homePageHero'}) 
>}); 
></script> 
>```

>Or:
>
>```
>adobe.target.trackEvent({ 
>    "mbox": "clicked-cta", 
>    "params": { 
>        "param1": "value1" 
>    } 
>});
>```


>>[!NOTE]
>>
>>In case the mandatory fields are not set, no request is executed, and an error is thrown.
>

