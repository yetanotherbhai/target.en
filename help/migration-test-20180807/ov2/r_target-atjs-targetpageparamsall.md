---
description: This method allows you to attach parameters to all mboxes from outside of the request code.
keywords: adobe.target.targetPageParamsAll(Options);element;selector;targetPageParamsAll;parameters
seo-description: This method allows you to attach parameters to all mboxes from outside of the request code.
seo-title: targetPageParamsAll()
solution: Target
title: targetPageParamsAll()
topic: Standard
uuid: 93759cec-6a63-4cbd-a17e-060ebb1902ff
index: y
internal: n
snippet: y
translate: y
---

# targetPageParamsAll()


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

