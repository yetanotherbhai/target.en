---
description: This function fires a request to a specific endpoint. Common usage is to retrieve data and share across all at.js requests.
keywords: adobe.target.executeAjax(Options);element;selector;executeAJax;ajax
seo-description: This function fires a request to a specific endpoint. Common usage is to retrieve data and share across all at.js requests.
seo-title: adobe.target.executeAjax(options)
solution: Target
title: adobe.target.executeAjax(options)
topic: Standard
uuid: 2889b9a6-c539-45c4-980b-10d5b7e94130
index: y
internal: n
snippet: y
translate: y
---

# adobe.target.executeAjax(options)



>>[!IMPORTANT]
>>
>>This function was removed in[ ` at.js` version 0.9.1 ](r_target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A). 
>

>The ` options` parameter is mandatory and has the following structure: 


><table id="table_0E08F2AAEE874E0899A8805383878BD4"> 
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
   <td colname="col1"> url </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Mbox name </td> 
  </tr> 
  <tr> 
   <td colname="col1"> type </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Represents the request type, if not provided defaults to json.</p> <p>Available types:</p> <p> 
     <ul id="ul_360AAF0FC6234CFEA8B9D8044EA32CD5"> 
      <li id="li_347ABB46E1E147A3B8193647DA466CFB"> json <p>Use XMLHttpRequest to execute cross domain requests</p> </li> 
      <li id="li_D05ECA1321264736AB87683D9849B01C">jsonp <p>Use a SCRIPT tag with a designated callback parameter to wrap the JSON response</p> </li> 
      <li id="li_8FD86C20255D425485CDA8812DDAC472">script <p>Attempts to download a ordinary JavaScript code</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> method </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>HTTP method.</p> <p>If not provided defaults to GET.</p> <p>Use only for json type. For all other types, use only HTTP GET.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> jsonp </td> 
   <td colname="col2"> String </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Represents the name of the callback parameter.</p> <p>Used only when using jsonp type.</p> <p>Defaults to callback. (For AAM the callback parameter name is <span class="codeph"> d_cb </span>.) </p> </td> 
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
   <td colname="col4"> <p>A callback function used to gather the data received from the endpoint.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> error </td> 
   <td colname="col2"> Function </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> <p>A callback function used to signal that something went wrong.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> timeout </td> 
   <td colname="col2"> Number </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Timeout in milliseconds.</p> <p>If not specified, the default timeout (500ms) in <span class="filepath"> at.js </span> is used. </p> <p>The default timeout can be set from the Target UI under <span class="uicontrol"> Setup </span> &gt; <span class="uicontrol"> Implementation </span> &gt; <span class="uicontrol"> Edit Mbox.js Settings </span> &gt; <span class="uicontrol"> Timeout </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>
>* For jsonp request: do not include the ` callback` parameter in the url. Use the ` jsonp` parameter.
>* If you are using ` executeAjax` for integration, use ` at.js` without the ` autocreate` option.


## Examples {#section_6CDB2A889F32405D822B0B5EB2AD971F}


1. Retrieve data.
1. Share the (parsed) data.
1. Fire the global mbox request.


```
function showDocument() { 
  document.documentElement.style.display = 'block'; 
  document.documentElement.style.visibility = 'visible'; 
} 
 
function hideDocument() { 
  document.documentElement.style.display = 'none'; 
  document.documentElement.style.visibility = 'hidden'; 
} 
 
// **Step 0. ** at the early stage - hide the page 
hideDocument(); 
 
function parsePartnerData(data) { 
  return { 
    'parsedParam1' : '(parsed) ' + data['param1'], 
    'parsedParamZ' : '(parsed) ' + data['paramZ'] 
  } 
} 
 
function executeGlobalMbox() { 
  adobe.target.getOffer({ 
    "mbox": "target-global-mbox", 
    "success": function(offer) { 
      adobe.target.applyOffer({offer:offer}); 
      // don't forget to show the document... 
      showDocument(); 
    }, 
    "error": function(status, error) { 
      // ...in both cases 
      showDocument(); 
    } 
  }); 
} 
 
function populateTargetPageParamsAll(partnerData) { 
  window.targetPageParamsAll = function() { 
    // **Step 2.** include parsed data into mbox calls 
    return parsePartnerData(partnerData); 
  }; 
} 
// **Step 1.** retrieve data; 
adobe.target.executeAjax({ 
  url: 'responses/example.json', 
  params: { 
    "param": "value" 
  }, 
  success: function(data) { 
    populateTargetPageParamsAll(data); 
    //** Step 3.** fire global-mbox request 
    executeGlobalMbox(); 
  }, 
  error: function(errorStatus) { 
    console.log('error:', arguments); 
    executeGlobalMbox(); 
  } 
});
```

` executeAjax` fetches some data: 

```
{ 
  "param1": "value1", 
  "paramZ": "valueZ" 
}
```

` myParser` returns parsed data: 

```
{ 
  "parsedParam1": "(parsed) value1", 
  "parsedParamZ": "(parsed) valueZ" 
}
```

The returned parsed data is included in the ` getOffer()` request with parameters: 

```
... 
parsedParam1:(parsed) value1 
parsedParamZ:(parsed) valueZ 
mboxSession:1448974915335-274021 
mboxPC:32232222.01_00 
...
```

