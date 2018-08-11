---
description: The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y."
keywords: order confirmation;orderConfirmPage
seo-description: The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y."
seo-title: Create an Order Confirmation mbox - at.js
solution: Target
subtopic: Getting Started
title: Create an Order Confirmation mbox - at.js
uuid: 2e928c65-dd3c-4f72-bfbb-57d4d64b5fb8
index: y
internal: n
snippet: y
translate: y
---

# Create an Order Confirmation mbox - at.js


>[!NOTE]
>
>If users make purchases on your website, we recommend implementing an Order Confirmation mbox even if you use Analytics for Target (A4T) for your reporting.




>[!NOTE]
>
>If you are migrating to ` at.js` from ` mbox.js`, your [ existing Order Confirmation mbox ](../c_seting_up_target/c_implementing_target/t_mbox_download/t_orderconfirm_create.md#task_0036D5F6C062442788BB55E872816D82) might work as is. If this is the case, you don't need to use the ` trackEvent()` technique explained below. 



>1. In your order details page, insert the mbox script following the model below.
>1. Replace the WORDS IN CAPITAL LETTERS with either dynamic or static values from your catalog.


>       >[!NOTE]
>       >
>       >Use comma delimiting to separate multiple product IDs.


>       **Tip: **You can also pass order information in any mbox (it does not need to be named ` orderConfirmPage`). You can also pass order information in multiple mboxes within the same campaign. 

>    
>       ```
>       <script type="text/javascript"> 
>       adobe.target.trackEvent({ 
>           "mbox": "orderConfirmPage", 
>           "params":{  
>               "orderId": "ORDER ID FROM YOUR ORDER PAGE",  
>               "orderTotal": "ORDER TOTAL FROM YOUR ORDER PAGE",  
>               "productPurchasedId": "PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3"  
>           } 
>       }); 
>       </script> 
>       ```

