---
description: This function fires a request to get a Target offer.
keywords: adobe.target.getOffer (Options);element;selector;getOffer;offer
seo-description: This function fires a request to get a Target offer.
seo-title: adobe.target.getOffer(options)
solution: Target
title: adobe.target.getOffer(options)
topic: Standard
uuid: 3318bdfc-3f89-402b-aed9-5f0b25b02c07
index: y
internal: n
snippet: y
translate: y
---

# adobe.target.getOffer(options)


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
   <td colname="col4"> <p>Callback to be executed when we got a response from the server. The success callback function will receive a single parameter that represents an array of offer objects. Here is a success callback, example:</p> <p> <span class="codeph"> function handleSuccess(response){......} </span> </p> <p>See <a href="r_target-atjs-getoffer.xml#reference_C81525D1598A4A1199740DCAB81A7FDF/section_CF9FD236EF794620BCBF84EB80160183" format="dita" scope="local"> Responses </a> for details. </p> </td> 
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
     </ul> </p> <p>The error callback function will receive two parameters: status and error. Here is an error callback example:</p> <p> <span class="codeph"> function handleError(status, error){......} </span> </p>See <a href="r_target-atjs-getoffer.xml#reference_C81525D1598A4A1199740DCAB81A7FDF/section_1ACCE79AF2CB4FA2AD1371EA06AF129F" format="dita" scope="local"> Error Responses </a> for details. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> timeout </td> 
   <td colname="col2"> Number </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Timeout in milliseconds. If not specified, the default timeout in <span class="filepath"> at.js </span>will be used. The default timeout can be set from the Target UI under <span class="uicontrol"> Setup </span> &gt; <span class="uicontrol"> Implementation </span> &gt; <span class="uicontrol"> Edit Mbox.js Settings </span> &gt; <span class="uicontrol"> Timeout </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>


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

