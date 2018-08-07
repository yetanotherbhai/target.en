---
description: Modify the following code sample to add an orderConfirm targetLocation to your mobile app.
seo-description: Modify the following code sample to add an orderConfirm targetLocation to your mobile app.
seo-title: Add an orderConfirm targetLocation
title: Add an orderConfirm targetLocation
uuid: 66529bd3-2460-4781-83b3-524a1ab3ccbf
index: y
internal: n
snippet: y
translate: y
---

# Add an orderConfirm targetLocation


>This location should be placed on the view where confirmation of a transaction occurs.
>
>```
>ADBTargetLocationRequest *req = [ADBMobile targetCreateOrderConfirmRequestWithName: "orderConfirm" 
>      orderId:  
<span class="varname"> orderId </span> 
>      orderTotal:  
<span class="varname"> @"39.95" </span> 
>      productPurchasedId:  
<span class="varname"> _galleryItem.title </span> 
>      parameters:  
<span class="varname"> nil]; </span> 
>[ADBMobile targetLoadRequest: req callback: nil];
>```



>|  Parameters  | Description  |
>|---|---|
>|  ` * ` orderId` *`  | Replace with a dynamic variable representing a unique order ID.  |
>|  ` * ` @"39.95"` *`  | Replace with a dynamic variable representing a unique order total.  |
>|  ` * ` _galleryItem.title` *`  | Replace with a dynamic variable representing a comma-delimited list of products purchased.  |
>|  ` * ` parameters: nil` *`  | Optional dictionary of additional parameters.  |


>>[!NOTE]
>>
>>If this is not a revenue transaction, reserved parameters are not required.
>

