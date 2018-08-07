---
description: Instructions for downloading at.js using the API.
keywords: at.js;download at.js;download api
seo-description: Instructions for downloading at.js using the API.
seo-title: Download at.js Using the Target Download API
solution: Target
subtopic: Getting Started
title: Download at.js Using the Target Download API
topic: Standard
uuid: f3ffacb7-335c-4155-bc9f-68347be91521
index: y
internal: n
snippet: y
translate: y
---

# Download at.js Using the Target Download API


>1. Get your client code.

>       Your client code is available at the top of the ** `Setup` ** > ** `Implementation` ** > ** `Edit Mbox.js Settings` ** page of the `Target` interface. 
>1. Get your admin number.

>       Load this URL:
>    
>       ```
>       https://admin.testandtarget.omniture.com/rest/v1/endpoint/<
<span class="varname">client
 >       code</span>>
>       ```

>       Replace `< * `client code` *>` with the client code from Step 1. 
>       The result of loading this URL should look similar to the following example:
>    
>       ```
>       {
>         "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1"
>       }
>       ```

>       In this example, "6" is the admin number.
>1. Download `at.js`.

>       Load this URL with the following structure:
>    
>       ```
>       https://admin<
<span class="varname">admin number</span>>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<
<span class="varname">client code</span>>
>       ```

>    
>    * Replace `< * `admin number` *>` with your admin number.
>    * Replace `< * `client code` *>` with the client code from Step 1.

>       Loading this URL starts the download of your customized `at.js` file. 
