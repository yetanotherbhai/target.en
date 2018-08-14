---
description: The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y."
keywords: order confirmation;orderConfirmPage
seo-description: The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y."
seo-title: Create an Order Confirmation mbox - mbox.js
solution: Target
subtopic: Getting Started
title: Create an Order Confirmation mbox - mbox.js
uuid: e9bbbd6c-5c63-46ee-89bc-d225664b5793
index: y
internal: n
snippet: y
translate: y
---

# Create an Order Confirmation mbox - mbox.js


>[!NOTE]
>
>If users make purchases on your website, we recommend implementing an Order Confirmation mbox even if you use Analytics for Target (A4T) for your reporting.




>[!NOTE]
>
>You can also create an Order Confirmation mbox for ` at.js` using the same method; however, the [!DNL  at.js] method is preferred. For more information, see [ Create an OrderConfirmPage mbox - at.js ](../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/t_create_orderconfirm-page-mbox-atjs.md#task_E85D2F64FEB84201A594F2288FABF053). 



>1. In your order details page, insert the mbox script following the model below.
>1. Replace the WORDS IN CAPITAL LETTERS with either dynamic or static values from your catalog.


>       >[!NOTE]
>       >
>       >Use comma delimiting to separate multiple product IDs.


>       **Tip: **You can also pass order information in any mbox (it does not need to be named ` orderConfirmPage`). You can also pass order information in multiple mboxes within the same campaign. 

>    
>       ```
>       <div class="mboxDefault"> 
>          <!-- CONTENT TO SHOW IF NO OFFERS AVAILABLE. --> 
>       </div> 
>       <script type="text/javascript">    
>          mboxCreate('orderConfirmPage', 
>          'productPurchasedId=PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3', 
>          'orderTotal=ORDER TOTAL FROM YOUR ORDER PAGE', 
>          'orderId=ORDER ID FROM YOUR ORDER PAGE'); 
>       </script> 
>       ```

