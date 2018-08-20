---
description: Sales data can be sent to Adobe Target from any mbox.
seo-description: Sales data can be sent to Adobe Target from any mbox.
seo-title: Sending Sales Data Values
solution: Target
title: Sending Sales Data Values
topic: Recommendations
uuid: 315f1545-6a81-47e0-a8f9-0e8bd920affa
index: y
internal: n
snippet: y
translate: y
---

# Sending Sales Data Values

The parameters must follow the strict syntax below. The parameters ` orderId` and ` orderTotal` are required. The ` productPurchasedId` attribute must match the ` entity.id` display variable. 


```
<script type="text/javascript"> 
 
mboxCreate('orderConfirmPage', 
 
'productPurchasedId=LIST OF PRODUCT IDs FROM ORDER PAGE', 
 
'orderId=ORDER ID FROM ORDER PAGE', 
 
'orderTotal=ORDER TOTAL FROM ORDER PAGE'); 
 
</script>
```



>[!NOTE] {class="- topic/note "}
>
>You must pass the ` orderId` parameter value as it allows Target to remove double calls (duplicate orders). The parameter names are also case-sensitive and must be followed as shown above. 


>[!MORE_LIKE_THIS] {class="- topic/related-links "}* [ Using an Mbox on Your Web Site ](t_Using_an_Mbox_on_Your_Web_Site.md#task_0A087749BA75438D988726255BF097BB)* [ Preparing for the Mbox ](c_Preparing_for_the_Mbox.md#concept_459B7584184A4C1C9AF183EF9203C52B)* [ Creating the Mbox ](t_Creating_the_Mbox.md#task_A1D1A81FCFF046D2A2DF21814C05DA7D)* [ Troubleshooting Mboxes ](c_Troubleshooting_Mboxes.md#concept_395D034879F7428D9FF58E28068BAA70)