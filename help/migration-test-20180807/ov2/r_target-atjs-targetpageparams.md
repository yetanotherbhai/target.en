---
description: This method allows you to attach parameters to the global mbox from outside of the request code.
keywords: adobe.target.targetPageParams(Options);element;selector;targetPageParams;parameters
seo-description: This method allows you to attach parameters to the global mbox from outside of the request code.
seo-title: targetPageParams()
solution: Target
title: targetPageParams()
topic: Standard
uuid: 33dd4a4b-2bd4-46a0-881b-b46d28fffca0
index: y
internal: n
snippet: y
translate: y
---

# targetPageParams()


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

