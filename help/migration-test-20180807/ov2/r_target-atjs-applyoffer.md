---
description: This function is for applying the response content.
keywords: adobe.target.applyOffer (Options);element;selector;applyOffer;offer
seo-description: This function is for applying the response content.
seo-title: adobe.target.applyOffer(options)
solution: Target
title: adobe.target.applyOffer(options)
topic: Standard
uuid: bd9cc75e-4b2a-4fda-852f-49d3e0a4e377
index: y
internal: n
snippet: y
translate: y
---

# adobe.target.applyOffer(options)



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

