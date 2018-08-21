---
description: You can create an mbox on a page whose code is changed after the page loads.
seo-description: You can create an mbox on a page whose code is changed after the page loads.
seo-title: Creating a Dynamic Mbox
solution: Target
title: Creating a Dynamic Mbox
topic: Recommendations
uuid: 3f895c6c-fa4e-4820-8898-90dc776e1377
index: y
internal: n
snippet: y
translate: y
---

# Creating a Dynamic Mbox


>Many Rich Internet Applications (RIAs) manipulate HTML after the page has already loaded by using technologies like DHTML and AJAX. For example, after clicking a button, your Web page might display a new section of content. Adobe supports this scenario, allowing you to define [ dynamic mboxes ](../../../c_rec_mng_recs/c_Managing_Mboxes/t_Creating_the_Mbox/c_about_dynamic_mboxes.md#concept_062FE49B25A64AA49F3918340E4A587D) through its ` mboxDefine()` and ` mboxUpdate()` functions. 

>For example, if you want to serve content when an HTML node called ` dynamicElement` appears on the page: 

>
>```
><div id="dynamicElement"></div>
>```


>Then you could trigger the following script on a JavaScript event: 

>
>```
><script type="text/javascript" >  
>mboxDefine('dynamicElement’,'mbox_dynamic’, 
> 
>'parameter1=value1’);  
>mboxUpdate('mbox_dynamic’, 'parameter1=value1’); 
> 
></script>
>```


>Of note: 

>
>* ` mboxDefine()` defines an HTML element as a container for content to be served. This function takes in the unique element id, the mbox name, and any number of parameters. The parameters can be used for targeting by the active campaign, even if not passed in again with a later ` mboxUpdate()` call. 

>  ` mboxDefine()` does not actually serve content so it should be followed with ` mboxUpdate()`. 

>* ` mboxUpdate()` retrieves the content from Adobe. This function may be called multiple times if you want to further change the content. Like ` mboxCreate`, it takes in the mbox name and any number of parameters. 

>* The usual ` mboxCreate()` function only works for HTML elements that exist on the page on the initial load.
>* ` mboxUpdate()` can also be used for mboxes created with ` mboxCreate()` rather than ` mboxDefine()`.


>This allows the page to update content dynamically after the initial page load. 
>[!MORE_LIKE_THIS] {class="- topic/related-links "}
>
>* [ Placing an Mbox Around a Table ](r_Placing_an_Mbox_Around_a_Table.md#reference_361F35DEA8CC4E2B87B470F72C9E344F)
>* [ Placing an Mbox Around a Table Cell ](r_Placing_an_Mbox_Around_a_Table_Cell.md#reference_CBE33BC9DE884F14B39478818C164F43)
>* [ Creating Multiple Mboxes on a Page ](c_Creating_Multiple_Mboxes_on_a_Page.md#concept_4AC9A22530C44C7580877B5DD4C5F863)
>* [ Creating a Whole Page as an Mbox ](r_Creating_a_Whole_Page_as_an_Mbox.md#reference_F3E59E7326D946E4897AE41C3A6B40CE)
>* [ About Dynamic Mboxes ](c_about_dynamic_mboxes.md#concept_062FE49B25A64AA49F3918340E4A587D)
