---
description: Many Rich Internet Applications (RIAs) manipulate HTML after the page has already loaded by using technologies like DHTML and AJAX.
seo-description: Many Rich Internet Applications (RIAs) manipulate HTML after the page has already loaded by using technologies like DHTML and AJAX.
seo-title: About Dynamic Mboxes
solution: Target
title: About Dynamic Mboxes
topic: Advanced
uuid: 639812ee-6b5a-43df-b7d9-619198206885
index: y
internal: n
snippet: y
translate: y
---

# About Dynamic Mboxes

For example, after clicking a button, your Web page may display a new section of content. This scenario is supported, allowing you to define dynamic mboxes through its ` mboxDefine()` and ` mboxUpdate()` functions. 

For example, if you want to serve content when an HTML node called "dynamicElement" appears on the page: 


```
<div id="dynamicElement"></div>
```


then you could trigger the following script on a JavaScript event: 


```
<script type="text/javascript"> 
 
    mboxDefine("dynamicElement", "mbox_dynamic", "parameter1=value1"); 
 
    mboxUpdate("mbox_dynamic", "parameter1=value1"); 
 
</script>
```


Of note: 

* ` mboxDefine()` defines an HTML element as a container for content to be served. It takes in the unique element id, the mbox name, and any number of parameters. The parameters can be used for targeting by the active campaign, even if not passed in again with a later ` mboxUpdate()` call. ` mboxDefine()` does not actually serve content so it should be followed with ` mboxUpdate()`. 

* ` mboxUpdate()` retrieves the content. This function may be called multiple times if you want to further change the content. Like ` mboxCreate`, it takes in the mbox name and any number of parameters. 

* The usual ` mboxCreate()` function only works for HTML elements that exist on the page on the initial load.
* ` mboxUpdate()` can also be used for mboxes created with ` mboxCreate()` rather than ` mboxDefine()`. This allows the page to update content dynamically after the initial page load. 

* ` mboxUpdate()` applies the offer only when the DOM-ready event has been fired.
When using dynamic mboxes, delivering offers that include ` document.write` cause the page where the dynamic mbox is located to appear blank because the ` document.write` function is invoked after the DOM has loaded. Note also that plug-ins using offers with ` document.write` should never be used on sites employing dynamic mboxes. 
>[!MORE_LIKE_THIS] {class="- topic/related-links "}
>
>* [ Creating a Dynamic Mbox ](r_Creating_a_Dynamic_Mbox.md#reference_60A14E7EB8754383B2DC6A7E4D531AB4)
