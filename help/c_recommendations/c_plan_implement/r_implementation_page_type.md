---
description: Page type will influence your Recommendations implementation.
keywords: Targeting
seo-description: Page type will influence your Recommendations implementation.
seo-title: Implementation According to Page Type
solution: Target
title: Implementation According to Page Type
title_outputclass: premium
topic: Premium
uuid: 0ab89cac-868d-4b5d-aad3-a9f892835bf6
badge: assets/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Implementation According to Page Type


>For example, the types of recommendations you want to present may be different on a product page than on a category page or your home page. For each page, you can run specific functions prior to the mbox call to display the appropriate recommendations. 

>For information about the attributes in the examples, see [ Entity Attributes ](../../c_recommendations/c_products/r_entity_attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F). 

>Valid JSON formatting is required. 

>The ` targetPageParams` function shown below is especially helpful if you are using a tag management solution to implement your pages. [!DNL  Adobe Launch] or [!DNL  Adobe Dynamic Tag Manager] (DTM) places the at.js/mbox.js reference and the ` targetPageParams` function on your page and allows you to configure the values. You should either place that function before your at.js/mbox.js call, or put it in the Extra JavaScript section of your at.js/mbox.js. 

>The following sections contain more information: 

>
>* [ All Pages ](../../c_recommendations/c_plan_implement/r_implementation_page_type.md#section_A22061788BAB42BB82BA087DEC3AA4AD)
>* [ Category Page ](../../c_recommendations/c_plan_implement/r_implementation_page_type.md#section_F51A1AAEAC0E4B788582BBE1FEC3ABDC)
>* [ Product Page ](../../c_recommendations/c_plan_implement/r_implementation_page_type.md#section_205B3953C9664125A17CA8574FA6B2A3)
>* [ Cart Page ](../../c_recommendations/c_plan_implement/r_implementation_page_type.md#section_D37E48700F074556B925D0CA0291405E)
>* [ Thank You Page ](../../c_recommendations/c_plan_implement/r_implementation_page_type.md#section_C6126A4517A1478693AB7EC2A1D4ACCA)


## All Pages {#section_A22061788BAB42BB82BA087DEC3AA4AD}

All pages that contain recommendations require either an [!DNL  at.js] or [!DNL  mbox.js] reference on the page. Add one of the following references to all pages with recommendations: 


```
&amp;lt;script&amp;nbsp;src="../at.js&amp;nbsp;/&amp;gt;&amp;lt;/script&amp;gt;
```



```
&amp;lt;script&amp;nbsp;src="../mbox.js&amp;nbsp;/&amp;gt;&amp;lt;/script&amp;gt;
```


This implementation requires: 


* [!DNL  at.js] version 0.9.2 (or later) or [!DNL  mbox.js] version 55 (or later)
* [!DNL  mbox.js] must include the reference to [!DNL  target.js] ( [!DNL  at.js] does not require a reference to [!DNL  target.js])


For more information about implementing [!DNL  at.js], see [ at.js Implementation ](../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17). 

For more information about implementing [!DNL  mbox.js], see [ Mbox.js Implementation ](../../c_seting_up_target/c_implementing_target/t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420). 

For more information about the differences between the two Target Javascript libraries, see [ Understanding the Target JavaScript Libraries ](../../c_seting_up_target/c_implementing_target/c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB). 

## Category Page {#section_F51A1AAEAC0E4B788582BBE1FEC3ABDC}

On a category page, you probably want to restrict your recommendations to products or content within that category. To set up a category page, you set up the keys used by the page. For more information about keys, see [ Base the Recommendation on a Recommendation Key ](../../c_recommendations/c_algorithms/t_create_new_algorithm.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B). 


```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": " 
<i>My&amp;nbsp;Category</i>" 
      } 
   } 
}
```


## Product Page {#section_205B3953C9664125A17CA8574FA6B2A3}

On a product page, you might want to recommend specific items, or items with a particular price or inventory level. For a product page, you might need to set up frequently changing attributes (such as value and inventory), in addition to the keys required for a category page. 


```
function targetPageParams() { 
   return { 
      "entity": { 
         "id": " 
<i>32323</i>", 
         "categoryId": " 
<i>My&amp;nbsp;Category</i>", 
         "value": 105.56, 
         "inventory": 329 
      } 
   } 
}
```


## Cart Page {#section_D37E48700F074556B925D0CA0291405E}

On a cart page, you likely want to exclude some items from your recommendations, such as the items that are already in the cart. 


```
<script type="text/javascript"> 
function targetPageParams() { 
   return { 
      "excludedIds": [352, 223, 23432, 432, 553] 
      } 
} 
</script>
```


## Thank You Page {#section_C6126A4517A1478693AB7EC2A1D4ACCA}

On the Thank You page, you might want to show the order total, and the order ID, and show the products that were purchased, without recommending additional items. You can implement a second mbox to capture the order information. 


* If you are using at.js, see [ Create an Order Confirmation mbox - at.js ](../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/t_create_orderconfirm-page-mbox-atjs.md#task_E85D2F64FEB84201A594F2288FABF053). 

* If you are using mbox.js, see [ Create an Order Confirmation mbox - mbox.js ](../../c_seting_up_target/c_implementing_target/t_mbox_download/t_orderconfirm_create.md#task_0036D5F6C062442788BB55E872816D82). 


