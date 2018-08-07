---
description: Define and update an mbox.
keywords: adobe.target.mboxDefine(Options);adobe.target.mboxUpdate(Options);mboxDefine;mboxUpdate;element;selector;offer
seo-description: Define and update an mbox.
seo-title: mboxDefine() and mboxUpdate()
solution: Target
title: mboxDefine() and mboxUpdate()
topic: Standard
uuid: b71ccf6c-0040-4ac6-a4ed-57e040bc6223
index: y
internal: n
snippet: y
translate: y
---

# mboxDefine() and mboxUpdate()



>[!NOTE]
>
>` mboxDefine()` and ` mboxCreate()` are tied to HTML DIV elements where the offer should be displayed. These HTML DIV elements should have the ` mboxDefault` class. If the HTML elements won't have this class attached, you could see some noticeable flicker. 



## mboxDefine {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Creates an internal mapping between a nodeId and an mbox name, but does not execute the request. Used in conjunction with ` mboxUpdate()`. Built into ` at.js`mostly to ease the transition from ` mbox.js`to ` at.js`. 

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Executes the request and applies the offer to the element identified by the ` nodeId` in the ` mboxDefine()`. Can also be used to update an mbox initiated by ` mboxCreate`. Built into ` at.js` mostly to ease the transition from ` mbox.js` to ` at.js`. ` mboxDefine()`/ ` mboxUpdate()` could be replaced by [ ` adobe.target.getOffer()` ](r_target-atjs-getoffer.md#reference_C81525D1598A4A1199740DCAB81A7FDF)and [ ` adobe.target.applyOffer()` ](r_target-atjs-applyoffer.md#reference_BBE83F513B5B4E03BBC3F50D90864245) using the selector option. 

## Example {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}


```
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```

