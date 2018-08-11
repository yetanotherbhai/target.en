---
description: Information about how the Target at.js JavaScript library prevents flicker during page or app load.
keywords: flicker;Target Standard;at.js;implementation
seo-description: Information about how the Target at.js JavaScript library prevents flicker during page or app load.
seo-title: How at.js Manages Flicker
solution: Target
title: How at.js Manages Flicker
topic: Standard
uuid: f789235d-57da-4c2a-900b-58791b0c4a27
index: y
internal: n
snippet: y
translate: y
---

# How at.js Manages Flicker

Flicker happens when default content momentarily displays to visitors before it is replaced by the activity content. Flicker is undesirable because it can be confusing to visitors. 

Target provides several ways to prevent flicker: 


* [ Using an Auto Created Global mbox ](../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/c_manage-flicker-with-atjs.md#section_C502170D551C4F52AAFD8E82C41BB63A)
* [ Using a Custom Global mbox with getOffer() and applyOffer() ](../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/c_manage-flicker-with-atjs.md#section_E42C06BB3B16456A920B3332BC6B1C28)
* [ Using a Regional mbox with mboxCreate() ](../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/c_manage-flicker-with-atjs.md#section_D4946235531544BF9B9B4A80CCF09226)


## Using an Auto Created Global mbox {#section_C502170D551C4F52AAFD8E82C41BB63A}

If you enable the [ Auto Create Global Mbox ](../c_seting_up_target/c_implementing_target/c_understanding-global-mbox.md#concept_76AC0EC995A048238F3220F53773DB13) setting when configuring at.js, at.js manages flicker by changing the opacity setting as the page loads. When at.js loads, it will change the opacity setting of the &lt;body&gt; element to "0", making the page initially invisible to visitors. After a response from Target is received—or if an error with the Target request is detected—at.js resets opacity to "1". This ensures that the visitor only sees the page after your activities' content has been applied. 

If you enable the setting when configuring ` at.js`, ` at.js` will set HTML BODY style opacity to 0. After a response from Target is received, ` at.js` resets HTML BODY opacity to 1. 

Opacity set to 0 keeps the page content hidden to prevent flicker, but the browser still renders the page and loads all the necessary assets like CSS, images, etc. 

If opacity 0 does not work in your implementation, you can also manage flicker by customizing ` bodyHiddenStyle` and set it to ` body {visibility:hidden !important}`. You can use either value body ` {opacity:0 !important`} or ` body {visibility:hidden !important}`, whichever works best for your specific circumstance. 

The following illustration shows the Hide Body and Show Body calls in the [ overall auto created global mbox flow ](../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/c_how_atjs_works.md#concept_7B5951B4394D4478B01FE80D57735F8B): 

![](../../../assets/target-flow2.png) 

For more information about the ` bodyHiddenStyle` override, see [ targetGlobalSettings() ](../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/cmp_at.js_Functions.md#concept_8DACBC47ABDE4279BB102B42609FE506). 

## Using a Custom Global mbox with getOffer() and applyOffer() {#section_E42C06BB3B16456A920B3332BC6B1C28}

In almost all implementations, the auto created mbox should be used. In the rare instance that a [ custom global mbox ](../c_seting_up_target/c_implementing_target/c_understanding-global-mbox/t_customize-global-mbox.md#task_8FE8D068DE924B3B96A784643015D830) is required, you can use a combination of [ ` getOffer()` ](../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/cmp_at.js_Functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF) and [ ` applyOffer()` ](../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/cmp_at.js_Functions.md#reference_BBE83F513B5B4E03BBC3F50D90864245). You must use your own flicker-handling code. The following sample pre-hides HTML BODY and then displays it after a response is received from Target: 


```
document.documentElement.style.opacity = "0"; 
  
adobe.target.getOffer({ 
    mbox: 'target-global-mbox', 
    success: function(offer) { 
        adobe.target.applyOffer({ 
            mbox: 'target-global-mbox', 
            offer: offer 
        }); 
  
        document.documentElement.style.opacity = "1"; 
    }, 
    error: function() { 
        document.documentElement.style.opacity = "1";         
    } 
});
```


Because both ` getOffer()` and ` applyOffer()` are low-level APIs, there is no built-in flicker control. You can pass a selector or HTML element as an option to ` applyOffer()`, in this case ` applyOffer()` will add the activity content to this particular element; however, you must make sure the element is properly pre-hidden before invoking ` getOffer()` and ` applyOffer()`. 

## Using a Regional mbox with mboxCreate() {#section_D4946235531544BF9B9B4A80CCF09226}

If you use a regional mbox implementation, you can use [ ` mboxCreate()` ](../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/cmp_at.js_Functions.md#reference_E68805FE86C64792B2066DB17B253D74) with your page provisioned similar to the following sample code: 


```
<div class="mboxDefault"> 
Some default content 
</div> 
<script> 
mboxCreate('some-mbox'); 
</script> 

```


If your pages are properly provisioned, ` at.js` will manage flicker by appropriately switching the CSS "visibility" property of the element with the mboxDefault class. 
