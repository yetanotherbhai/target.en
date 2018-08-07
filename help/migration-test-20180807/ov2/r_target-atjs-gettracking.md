---
description: Returns an object that contains all the tracking info used by Target.
keywords: adobe.target.getTracking(Options);element;selector;getTracking;tracking
seo-description: Returns an object that contains all the tracking info used by Target.
seo-title: adobe.target.getTracking()
solution: Target
title: adobe.target.getTracking()
topic: Standard
uuid: 25c43cef-5089-4a20-a24f-d9d76f65aec4
index: y
internal: n
snippet: y
translate: y
---

# adobe.target.getTracking()



>>[!IMPORTANT]
>>
>>This function was removed in[ ` at.js` version 0.9.1 ](r_target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A). 
>

>Here are the object details:


>|  Key  | Type  | Description  |
>|---|---|---|
>|  sessionId  | String  | Target session ID  |
>|  deviceId  | String  | Target device ID also known as TNT ID or PC ID  |

>**Example** 
>
>```
>adobe.target.getTracking();
>```

>**Result** 
>
>```
>{ 
>  sessionId: "21311312", 
>  deviceId: "4343242342" 
>}
>```


## Usage {#section_76BB45891EC7436A97AB17FA636B5AFC}

The result of this method should be used for integration with other systems, cross referencing, or passing tracking data around.
