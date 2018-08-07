---
description: Instructions for downloading at.js from the Target interface.
keywords: at,js;download at.js;use target to download at.js
seo-description: Instructions for downloading at.js from the Target interface.
seo-title: Download at.js Using the Target Interface
solution: Target
title: Download at.js Using the Target Interface
topic: Premium
uuid: a199146f-1851-4f07-80c3-944af9470cc2
index: y
internal: n
snippet: y
translate: y
---

# Download at.js Using the Target Interface


>1. Click ** `Setup` ** > ** `Implementation` **.
>1. Select ** `at.js` **.
>1. Click ** `Edit at.js Settings` **.

>       The Settings page shows your `at.js` settings. Some of these settings are informational only. 
>1. Change any settings as needed.



>    <table id="table_03B0D41E2A574BB98B28A8D845BE3CDB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Setting</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Auto create global mbox</td> 
   <td colname="col2"> <p>Use <span class="filepath">at.js</span> to auto-deploy target-global-mbox for a single line of code implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Global mbox name</td> 
   <td colname="col2"> <p>Specify a name for the global mbox. The default is target-global-mbox.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Advanced Settings</td> 
   <td colname="col2"> <p>Refer to <a href="c_target-atjs-advanced-settings.xml#concept_2FA0456607D04F82B0539C5BF5309812" format="dita" scope="local">at.js Advanced Settings</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Code Settings</td> 
   <td colname="col2"> <p>(Optional) Specify custom code to include in the page header and footer. We recommend that you consult with Client Care before changing these settings.</p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Click ** `Code` ** and enter any custom header and footer JavaScript to execute at the top of the library, such as `targetPageParams`.

>       If you used `mbox.js` in the past, you might notice fewer fields. However, there are ways to do many of the same things in `at.js` that you did in `mbox.js`. For example, if you used mbox parameters in `mbox.js`, in `at.js` you can use [targetPageParamsAll](r_target-atjs-targetpageparamsall.md#reference_97E77FCDD793403685ECCA5A44305F93). The `mbox.js` Extra JavaScript field is replaced by the `at.js` Header and Footer fields, which provide more control of the code. 
>1. Click ** `Save` **.

>1. Return to the Implementation page and click ** `Download at.js` **.

