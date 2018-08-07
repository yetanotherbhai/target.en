---
description: The orderConfirmPage mbox records details about your product, permitting reports on sales data, orders, and recommendations.
seo-description: The orderConfirmPage mbox records details about your product, permitting reports on sales data, orders, and recommendations.
seo-title: Create an orderConfirmPage Mbox
solution: Target
title: Create an orderConfirmPage Mbox
topic: Advanced
uuid: ee2eb498-738f-474e-b499-f7662b1d7f79
index: y
internal: n
snippet: y
translate: y
---

# Create an orderConfirmPage Mbox


>1. In your order details page, insert the mbox script following the model below.
>1. Replace the WORDS IN CAPITAL LETTERS with either dynamic or static values from your catalog.


>       >[!NOTE]
>       >
>       >Use comma delimiting to separate multiple product IDs.

>       **Tip:**You can also pass order information to any mbox (not only the ` orderConfirmPage` mbox). You can also pass order information to multiple mboxes within the same campaign. 
>    
>       ```
>       <div class="mboxDefault"> 
>        
>          <!-- CONTENT TO SHOW IF NO OFFERS AVAILABLE. --> 
>        
>       </div> 
>        
>       <script type="text/javascript"> 
>           
>          mboxCreate('orderConfirmPage', 
>        
>          'productPurchasedId=PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3', 
>        
>          'orderTotal=ORDER TOTAL FROM YOUR ORDER PAGE', 
>        
>          'orderId=ORDER ID FROM YOUR ORDER PAGE'); 
>        
>       </script> 
>       ```

