---
description: Returns all the user settings.
keywords: adobe.target.getSettings(Options);element;selector;getSettings;settings
seo-description: Returns all the user settings.
seo-title: adobe.target.getSettings()
solution: Target
title: adobe.target.getSettings()
topic: Standard
uuid: 9bb5f7e8-a3fa-4e85-bd95-bb4ab920535a
index: y
internal: n
snippet: y
translate: y
---

# adobe.target.getSettings()



>>[!IMPORTANT]
>>
>>This function was removed in[ ` at.js` version 0.9.1 ](r_target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A). 
>

>These are the settings you might see on the Edit Mbox.js page such as client code, auto-create global mbox, global mbox name, and so on.
>Here are the currently exported settings.


>|  Key  | Type  | Description  |
>|---|---|---|
>|  clientCode  | String  | Client code  |
>|  serverDomain  | String  | Target edge server domain  |
>|  timeout  | Number  | Request timeout measured in milliseconds  |
>|  globalMboxName  | String  | Target global mbox name  |
>|  globalMboxAutoCreate  | Boolean  | Indicates if we should execute target global mbox while ` at.js` is loaded  |

>**Example** 
>
>```
>adobe.target.getSettings();
>```

>**Result** 
>
>```
>{ 
>  clientCode: "demo", 
>  serverDomain: "demo.tt.omtrdc.net", 
>  timeout: 1000, 
>  globalMboxName: "target-global-mbox", 
>  globalMboxAutoCreate: false 
>}
>```


## Usage {#section_E20461869F2348648D22C7D9D25EF872}

` adobe.target.getSettings()`should be used mostly for integrations with third-party libraries or frameworks like AngularJS, EmberJS, and so on to reuse the same settings everywhere (for example, request timeout). 
