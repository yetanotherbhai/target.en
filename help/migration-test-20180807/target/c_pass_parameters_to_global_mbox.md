---
description: You can use JavaScript to pass parameters to a global mbox.
keywords: targetPageParams;global mbox;mbox.js;target-global-mbox;query string;JSON;Array
seo-description: You can use JavaScript to pass parameters to a global mbox.
seo-title: Passing Parameters to a Global Mbox
solution: Target
title: Passing Parameters to a Global Mbox
topic: Standard
uuid: 562f0ded-1af6-43d2-b19a-75adf5c7790f
index: y
internal: n
snippet: y
translate: y
---

# Passing Parameters to a Global Mbox

You must define the JavaScript function before adding the global mbox to the page. The requirements for the function are:

* Name: ` targetPageParams`
* Return value: a "&amp;" delimited parameters, with URL encoded parameter values. Example:

  ```
  p1=v1&amp;p2=v2&amp;p3=hello%20world
  ```

  In this example, p3 has the value ` hello world`, which is URL encoded. 


The following is an example of how the code for the page might look:

```
<html> 
  <head> 
    <title>Title here..</title> 
    <script type="text/javascript"> 
        function targetPageParams() { 
           
<b>return "p1=v1&amp;p2=v2&amp;p3=hello%20world"</b>; 
        } 
    </script> 
    <script src="mbox.js" type="text/javascript"></script> 
  </head> 
  <body>Body here... 
  </body> 
</html>
```

