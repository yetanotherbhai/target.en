---
description: List of functions that can be used with at.js.
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: List of functions that can be used with at.js.
seo-title: at.js Functions
solution: Target
subtopic: Getting Started
title: at.js Functions
topic: Standard
uuid: 618deb39-782d-4201-b749-6cb6743fc083
index: y
internal: n
snippet: y
translate: y
---

# at.js Functions

## at.js Functions {#concept_EF9BA649A8AF43F5B47977E986E29B17}List of functions that can be used with 
<filepath>
  at.js 
</filepath>.## adobe.target.getOffer(options) {#reference_C81525D1598A4A1199740DCAB81A7FDF}This function fires a request to get a Target offer. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-getoffer.xml 
</draft-comment>
>Use with ` adobe.target.applyOffer()` to process the response or use your own success handling. The options parameter is mandatory and has the following structure: 


><table id="table_53113151402049689D0401DF9C7857D8"> 
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
   <td colname="col4"> Mbox name </td> 
  </tr> 
  <tr> 
   <td colname="col1"> params </td> 
   <td colname="col2"> Object </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Mbox parameters. An object of key-value pairs that has the following structure:</p> <p> <span class="codeph"> { "param1": "value1", "param2": "value2"} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> success </td> 
   <td colname="col2"> Function </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> <p>Callback to be executed when we got a response from the server. The success callback function will receive a single parameter that represents an array of offer objects. Here is a success callback, example:</p> <p> <span class="codeph"> function handleSuccess(response){......} </span> </p> <p>See <a href="c_target-ats-functions.xml#reference_C81525D1598A4A1199740DCAB81A7FDF/section_CF9FD236EF794620BCBF84EB80160183" format="dita" scope="local"> Responses </a> for details. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> error </td> 
   <td colname="col2"> Function </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> <p>Callback to be executed when we got an error. There are a couple of cases that are considered erroneous:</p> <p> 
     <ul id="ul_824F701E2C5B4B0391C97315CC73C89D"> 
      <li id="li_24547266DAA94DBCA9C1F0C702ED30D8">HTTP status code different from 200 OK</li> 
      <li id="li_B373A506F5E644F6AE7D41E811E5BCDF">Response can not be parsed. For example we poorly constructed JSON or HTML instead of JSON.</li> 
      <li id="li_D71425FFA2C34E278E18D4F96DA5C679">Response contains the "error" key. For example an exception was thrown on the edge a request could not be properly processed. We could get an error when an mbox is blocked and we could not retrieve any content for it etc.</li> 
     </ul> </p> <p>The error callback function will receive two parameters: status and error. Here is an error callback example:</p> <p> <span class="codeph"> function handleError(status, error){......} </span> </p>See <a href="c_target-ats-functions.xml#reference_C81525D1598A4A1199740DCAB81A7FDF/section_1ACCE79AF2CB4FA2AD1371EA06AF129F" format="dita" scope="local"> Error Responses </a> for details. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> timeout </td> 
   <td colname="col2"> Number </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Timeout in milliseconds. If not specified, the default timeout in <span class="filepath"> at.js </span>will be used. The default timeout can be set from the Target UI under <span class="uicontrol"> Setup </span> &gt; <span class="uicontrol"> Implementation </span> &gt; <span class="uicontrol"> Edit Mbox.js Settings </span> &gt; <span class="uicontrol"> Timeout </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Examples {#section_A7965B5DEA374DDBBF94C24451481574}

Adding parameters with getOffer() and using applyOffer() for success-handling:

```
adobe.target.getOffer({   
  "mbox": "target-global-mbox", 
  "params": { 
     "a": 1, 
     "b": 2 
  }, 
  "success": function(offer) {           
        adobe.target.applyOffer( {  
           "mbox": "target-global-mbox", 
           "offer": offer  
        } ); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

Adding parameters and profile parameters with getOffer() and using applyOffer() for success-handling:

```
adobe.target.getOffer({   
  "mbox": "target-global-mbox", 
  "params": { 
     "a": 1, 
     "b": 2, 
     "profile.age": 27, 
     "profile.gender": "male" 
  }, 
  "success": function(offer) {           
        adobe.target.applyOffer( {  
           "mbox": "target-global-mbox", 
           "offer": offer  
        } ); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

Using custom timeout and custom success-handling with getOffer():
"YOUR_OWN_CUSTOM_HANDLING_FUNCTION" is a placeholder for a function the customer would define.

```
adobe.target.getOffer({     
  "mbox": "target-global-mbox",   
  "success": function(offer) { 
    YOUR_OWN_CUSTOM_HANDLING_FUNCTION(offer);   
  }, 
  "error": function(status, error) {                 
    console.log('Error', status, error);   
  },   
  "timeout": 2000 
});
```


## Responses {#section_CF9FD236EF794620BCBF84EB80160183}

The response parameter passed to the success callback will be an array of actions. An action is an object that usually has the following format:


<table id="table_07840C5C381C4FE191ACA7F833C74EEB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> action </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> <p>Type of action to be applied to the identified element.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> selector </td> 
   <td colname="col2"> Sting </td> 
   <td colname="col3"> <p>Represents a Sizzle selector.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cssSelector </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> <p>DOM native selector, used for element pre-hiding.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> content </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> <p>The content to be applied to the identified element.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Example** 

```
{ 
    "sessionId": "1444512212156-384616", 
    "tntId": "1444512212156-384616.17_35", 
    "offers": [{ 
        "plugins": ["<script type=\"text/javascript\">\r\n/*mboxHighlight+ (1of2) v1 ==> Response Plugin*/\r\nwindow.ttMETA=(typeof(window.ttMETA)!='undefined')?window.ttMETA:[];window.ttMETA.push({'mbox':'target-global-mbox','campaign':'at: redirect ootb','experience':'Experience B','offer':'/at_redirect_ootb/experiences/1/pages/0/1442082890250'});window.ttMBX=function(x){var mbxList=[];for(i=0;i<ttMETA.length;i++){if(ttMETA[i].mbox==x.getName()){mbxList.push(ttMETA[i])}}return mbxList[x.getId()]}\r\n</script>"], 
        "actions": { 
            "content": [{ 
                "passMboxSession": false, 
                "selector": "body", 
                "action": "redirect", 
                "url": "http://lab.adobetarget.com/04.html", 
                "includeAllUrlParameters": true 
            }] 
        } 
    }] 
}
```


## Error Responses {#section_1ACCE79AF2CB4FA2AD1371EA06AF129F}

The "status" and "error" parameters passed to the error callback will have the following format:


<table id="table_D201E1639CAA454FAA2F9D8F131B7A8C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> status </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> <p>Represents the error status. This parameter can have the following values:</p> <p> 
     <ul id="ul_708148E9CA5F435C914CF247C1D9E0E3"> 
      <li id="li_D74FB1FCB39542E78AB348D92195C850">timeout <p>Indicates that the request timed out</p> </li> 
      <li id="li_D87CC491BDD84B2B88FD365CA7C74F49">parseerror <p>Indicates that the response could not be parsed, for example if we receive HTML or plain text instead of JSON</p> </li> 
      <li id="li_F19E6178AD8F45238B5264225555881C">error <p>Indicates a general error like we received HTTP status different from 200 OK</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> error </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> <p>Contains additional data like exception message or anything else that might be useful for troubleshooting.</p> </td> 
  </tr> 
 </tbody> 
</table>

>## adobe.target.applyOffer(options) {#reference_BBE83F513B5B4E03BBC3F50D90864245}This function is for applying the response content. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-applyoffer.xml 
</draft-comment>

>>[!NOTE]
>>
>>` applyOffer` requires the ` mbox` parameter. If no mbox name is specified, an error occurs. 
>

>The options parameter is mandatory and has the following structure:


><table id="table_FE131775E30240C89BF02369FF48AC6F"> 
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
   <td colname="col1"> <p>mbox</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Yes</p> </td> 
   <td colname="col4"> <p>Mbox name</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>selector</p> </td> 
   <td colname="col2"> <p>String or DOM Element</p> </td> 
   <td colname="col3"> <p>No</p> </td> 
   <td colname="col4"> <p>HTML element or CSS selector used to identify the HTML element where Target should place the offer content. If selector is not provided, Target assumes that the HTML element we should use is HTML HEAD.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>offer</p> </td> 
   <td colname="col2"> <p>Array</p> </td> 
   <td colname="col3"> <p>Yes</p> </td> 
   <td colname="col4"> <p>An array actions that should be applied to the element.</p> </td> 
  </tr> 
 </tbody> 
</table>


## Example {#section_D8D6A17B73DE4542937CDB687193A5CC}

The following example shows how to use ` getOffer` and ` applyOffer` together: 

```
adobe.target.getOffer({   
  "mbox": "mbox",   
  "success": function(offers) {           
        adobe.target.applyOffer( {  
           "mbox": "mbox", 
           "offer": offers  
        } ); 
  },   
  "error": function(status, error) {           
      if (console &amp;&amp; console.log) { 
        console.log(status); 
        console.log(error); 
      } 
  }, 
 "timeout": 5000 
}); 

```

>## adobe.target.trackEvent(options) {#reference_7E0F19368F9C4BC38F1E5DC5E717E487}This function fires a request to report user actions, such as clicks and conversions. It does not deliver activities in the response. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-trackevent.xml 
</draft-comment>
>These event-tracking mbox calls can then be used to define metrics in activities. For more information, see [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924) and [ Create an Order Confirmation mbox - at.js ](c_target-atjs-implementation.md#task_E85D2F64FEB84201A594F2288FABF053). 
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

>## mboxCreate(mbox,params) {#reference_E68805FE86C64792B2066DB17B253D74}Executes a request and applies the offer to the closest DIV with mboxDefault class name. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-mboxcreate.xml 
</draft-comment>
>This function is built into ` at.js` mostly to ease the transition from ` mbox.js` to ` at.js`. A newer alternative to ` mboxCreate()` is ` adobe.target.getOffer()`/ ` adobe.target.applyOffer()` or the Angular directive. 
>**Example** 
>
>```
><div class="mboxDefault"> 
>  default content to replace by offer 
></div> 
><script> 
>  mboxCreate('mboxName','mboxName','param1=value1','param2=value2'); 
></script>
>```

>**Notes** 
>` mboxCreate()` now uses the "json" endpoint instead of the "standard" endpoint and fires asynchronously. Because of this: 
>
>* [ Debugging ](c_target-atjs-implementation.md#concept_CAE591DA8C404C22917584ECD4F7494F) is a little different.
>* Avoid offer code requiring synchronous, blocking calls. For example, offers that set JavaScript variables that are used by site code or other mboxes that come later on the page.

>* Be sure to have a ` <div class="mboxDefault"></div>`before invoking ` mboxCreate()`, because ` at.js` will not add one for you.
>* Empty, top-of-page ` mboxCreate()` functions are not recommended as a global mbox. The auto-created global mbox in ` at.js` is a better option because it fires from the ` <head>` and can return content earlier. 


>## mboxDefine() and mboxUpdate() {#reference_61B2B9F351344CF5B0915D5AFD21C5FE}Define and update an mbox. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-mboxdefine-mboxupdate. 
</draft-comment>

>[!NOTE]
>
>` mboxDefine()` and ` mboxCreate()` are tied to HTML DIV elements where the offer should be displayed. These HTML DIV elements should have the ` mboxDefault` class. If the HTML elements won't have this class attached, you could see some noticeable flicker. 



## mboxDefine {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Creates an internal mapping between a nodeId and an mbox name, but does not execute the request. Used in conjunction with ` mboxUpdate()`. Built into ` at.js`mostly to ease the transition from ` mbox.js`to ` at.js`. 

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Executes the request and applies the offer to the element identified by the ` nodeId` in the ` mboxDefine()`. Can also be used to update an mbox initiated by ` mboxCreate`. Built into ` at.js` mostly to ease the transition from ` mbox.js` to ` at.js`. ` mboxDefine()`/ ` mboxUpdate()` could be replaced by [ ` adobe.target.getOffer()` ](c_target-ats-functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF)and [ ` adobe.target.applyOffer()` ](c_target-ats-functions.md#reference_BBE83F513B5B4E03BBC3F50D90864245) using the selector option. 

## Example {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}


```
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```

>## targetGlobalSettings() {#concept_8DACBC47ABDE4279BB102B42609FE506}You can override settings in the 
<codeph>
  at.js 
</codeph> library using 
<codeph>
  targetGlobalSettings() 
</codeph>, rather than configuring the settings in the 
<keyword>
  Target 
</keyword> Standard/Premium UI or by using REST APIs. 
<draft-comment otherprops="merge">
  ov2/c_atjs-settings-override.xml 
</draft-comment>There are use cases, especially when ` at.js` is delivered via ` Dynamic Tag Management` (DTM) when you would like to override some of the settings. 
This section contains the following information:

* [ Settings ](c_target-ats-functions.md#section_42C759AE9B524A43B8659018677224B8)
* [ Usage ](c_target-ats-functions.md#section_9AD6FA3690364F7480C872CB55567FB0)


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

>## targetPageParams() {#reference_B235C9F6DA79449ABE3E23F914FEABAE}This method allows you to attach parameters to the global mbox from outside of the request code. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-targetpageparams.xml 
</draft-comment>
>This function is very useful for including the same set of parameters on multiple mbox calls. The function needs to be defined by the customer. It should return an array of parameters that will be passed only to the global mbox request. This function can be defined before ` at.js` is loaded or in ** ` Setup` ** > ** ` Implementation` ** > ** ` Edit at.js Settings` ** > ** ` Code Settings` ** > ** ` Library Header` **. 
>You can pass in parameters to target-global-mbox using the ` targetPageParams()` function in any of the following ways: 
>
>* An ampersand-delimited list
>* An array
>* A JSON object

>**Examples** 
>Ampersand-delimited list (values must be URL encoded):
>
>```
>function targetPageParams() { 
>    return "param1=value1&amp;param2=value2&amp;p3=hello%20world"; 
>}
>```

>Array (values do not need to be URL encoded):
>
>```
>targetPageParams = function() { 
>     return ["a=1", "b=2", "c=hello world"]; 
>};
>```

>JSON (values do not need to be URL encoded):
>
>```
>targetPageParams = function() { 
>  return { 
>    "a": 1, 
>    "b": 2, 
>    "profile": { 
>        "age": 26, 
>        "country": { 
>          "city": "San Francisco" 
>        } 
>      } 
>  }; 
>};
>```

>## targetPageParamsAll() {#reference_97E77FCDD793403685ECCA5A44305F93}This method allows you to attach parameters to all mboxes from outside of the request code. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-targetpageparamsall.xml 
</draft-comment>
>This is very useful for including the same set of parameters on multiple mbox calls. The function needs to be defined by the customer. It should return an array of parameters that will be passed to all mbox requests on the page. This function can be defined before ` at.js` is loaded or in ** ` Setup` ** > ** ` Implementation` ** > ** ` Edit at.js Settings` ** > ** ` Code Settings` ** > ** ` Library Header` **. 
>You can pass in parameters to target-global-mbox using the targetPageParamsAll() function in any of the following ways:
>
>* An ampersand-delimited list
>* An array
>* A JSON object

>**Examples** 
>Ampersand-delimited list (values must be URL encoded):
>
>```
>function targetPageParamsAll() { 
>    return "param1=value1&amp;param2=value2&amp;p3=hello%20world"; 
>}
>```

>Array (values do not need to be URL encoded):
>
>```
>targetPageParamsAll = function() { 
>     return ["a=1", "b=2", "c=hello world"]; 
>};
>```

>JSON (values do not need to be URL encoded):
>
>```
>targetPageParamsAll = function() { 
>  return { 
>    "a": 1, 
>    "b": 2, 
>    "profile": { 
>        "age": 26, 
>        "country": { 
>          "city": "San Francisco" 
>        } 
>      } 
>  }; 
>};
>```

>## registerExtension() {#reference_B3ACC004D45E460C8DD94C1476D2625C}Provides a standard way to register a specific extension. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-registerextension.xml 
</draft-comment>
>The options parameter is mandatory and has the following structure:


><table id="table_46A93D7071DE4A3F84D6E05FFC849EAF"> 
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
   <td colname="col1"> <p>name</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Yes</p> </td> 
   <td colname="col4"> <p>Extension name.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>modules</p> </td> 
   <td colname="col2"> <p>Array[String]</p> </td> 
   <td colname="col3"> <p>Yes</p> </td> 
   <td colname="col4"> <p>An array of strings representing requested module names.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>register</p> </td> 
   <td colname="col2"> <p>Function</p> </td> 
   <td colname="col3"> <p>Yes</p> </td> 
   <td colname="col4"> <p>A function used to initialize and build the extension. This function receives arguments based on modules array.</p> </td> 
  </tr> 
 </tbody> 
</table>

>Notes:
>
>* If one of the parameters is not provided, an exception is thrown.

>* If the modules array is empty, an exception is thrown.


>For more information and examples of how to use ` registerExtension`, see the [ Adobe Marketing Cloud Target atjs Extensions ](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions) page on GitHub. 

## Settings Module Methods {#section_8501CDD4B0624FA2B10532C98C5F4328}



<table id="table_8A5991797599470C87EBB022783087D6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Key </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>clientCode</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Client code</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>serverDomain</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Edge server domain</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>globalMboxName</p> </td> 
   <td colname="col2"> <p>String</p> </td> 
   <td colname="col3"> <p>Target global mbox name</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>globalMboxAutoCreate</p> </td> 
   <td colname="col2"> <p>Boolean</p> </td> 
   <td colname="col3"> <p>Indicates if auto-create is enabled or not</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>timeout</p> </td> 
   <td colname="col2"> <p>Number</p> </td> 
   <td colname="col3"> <p>Request timeout</p> </td> 
  </tr> 
 </tbody> 
</table>


## Logger Module Methods {#section_10AF62B49AEF48F981E950D26E176138}



<table id="table_D76DD582EF9A432BB1B5B7F1DD2D853E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Key </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>log</p> </td> 
   <td colname="col2"> <p>Function</p> </td> 
   <td colname="col3"> <p>Logs the variable list of arguments to the browser console, if it exists. It is activated only when <span class="codeph"> mboxDebug=true </span> is passed to the URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>error</p> </td> 
   <td colname="col2"> <p>Function</p> </td> 
   <td colname="col3"> <p>Logs the variable list of arguments to the browser console. It is activated only when there are serious errors, such as network timeout, HTML node not found, etc.</p> </td> 
  </tr> 
 </tbody> 
</table>

>## at.js custom events {#reference_A828E4BA535F4E7692A075F3D70CF6CD}Information about 
<codeph>
  at.js custom events 
</codeph>, which lets you know when an mbox request or offer fails or succeeds. 
<draft-comment otherprops="merge">
  ov2/r_target-atjs-notification.xml 
</draft-comment>
>Historically, ` mbox.js` didn't let other JavaScript code that runs on the page know what happens behind the scenes. With the advancement of ` at.js`, we had a unique opportunity to fix this issue. 
>According to our customers there are several scenarios that they would like to be notified of, including:
>
>* An mbox request failed due to timeout, wrong status code, JSON parse error, etc.

>* An mbox request succeeded.

>* Offer rendering failed due to wrapping mbox element missing, selector can not be found, etc.

>* Offer rendering succeeded. DOM changes have been applied.


>Pre-defined events have a structure that allows you to extract the required data, based on event type.
>To make sure that events can be used in different scenarios, the custom events have a payload object that is assigned to the detail property of the event object (that is passed to the handler). Also to avoid passing strings as event names, the events are exposed as constants using ` adobe.target.event` namespace. 

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
