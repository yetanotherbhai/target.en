---
description: Provides a standard way to register a specific extension.
keywords: adobe.target.registerExtension(Options);element;selector;registerExtenstion;extension
seo-description: Provides a standard way to register a specific extension.
seo-title: registerExtension()
solution: Target
title: registerExtension()
topic: Standard
uuid: 3d035028-a2bb-42af-bf94-081b68c40c07
index: y
internal: n
snippet: y
translate: y
---

# registerExtension()


>The options parameter is mandatory and has the following structure:


><table id="table_46A93D7071DE4A3F84D6E05FFC849EAF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Key</th> 
   <th colname="col2" class="entry">Type</th> 
   <th colname="col3" class="entry">Required</th> 
   <th colname="col4" class="entry">Description</th> 
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


>For more information and examples of how to use `registerExtension`, see the [Adobe Marketing Cloud Target atjs Extensions](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions) page on GitHub. 
>This section contains the following information:
>
>* [Settings Module Methods](r_target-atjs-registerextension.md#section_8501CDD4B0624FA2B10532C98C5F4328)
>* [Logger Module Methods](r_target-atjs-registerextension.md#section_10AF62B49AEF48F981E950D26E176138)


## Settings Module Methods {#section_8501CDD4B0624FA2B10532C98C5F4328}



<table id="table_8A5991797599470C87EBB022783087D6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Key</th> 
   <th colname="col2" class="entry">Type</th> 
   <th colname="col3" class="entry">Description</th> 
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
   <th colname="col1" class="entry">Key</th> 
   <th colname="col2" class="entry">Type</th> 
   <th colname="col3" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>log</p> </td> 
   <td colname="col2"> <p>Function</p> </td> 
   <td colname="col3"> <p>Logs the variable list of arguments to the browser console, if it exists. It is activated only when <span class="codeph">mboxDebug=true</span> is passed to the URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>error</p> </td> 
   <td colname="col2"> <p>Function</p> </td> 
   <td colname="col3"> <p>Logs the variable list of arguments to the browser console. It is activated only when there are serious errors, such as network timeout, HTML node not found, etc.</p> </td> 
  </tr> 
 </tbody> 
</table>

