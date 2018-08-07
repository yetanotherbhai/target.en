---
description: Instructions to download the at.js library using the Target interface or the Download API.
keywords: at,js;download at.js;use target to download at.js;download api
seo-description: Instructions to download the at.js library using the Target interface or the Download API.
seo-title: Download at.js
solution: Target
title: Download at.js
topic: Premium
uuid: add3accd-605d-4eb9-89e3-4d9c47987b09
index: y
internal: n
snippet: y
translate: y
---

# Download at.js


>[!IMPORTANT]
>
>The Target team maintains only two versions of `at.js`—the current version and the second-latest version. Please upgrade `at.js` as necessary to ensure that you are running a supported version. For more information about what's in each version, see [at.js Version Details](r_target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A). 



>[!NOTE]
>
>If you are migrating your `Target` implementation from using the mbox.js library to the at.js library, see [Migrate to at.js from mbox.js](t_target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA). 


This section contains the following information:

* [Download at.js Using the Target Interface](c_target-configure-atjs.md#section_1F5EE401C2314338910FC57F9592894E)
* [Download at.js Using the Target Download API](c_target-configure-atjs.md#section_C0D9D2A9068144708D08526BA5CA10D0)


## Download at.js Using the Target Interface {#section_1F5EE401C2314338910FC57F9592894E}

To download `at.js` from the `Target` interface: 

1. Click ** `Setup` ** > ** `Implementation` **. 

1. Select ** `at.js` **. 

1. Click ** `Edit at.js Settings` **. 
   The Settings page shows your `at.js` settings. Some of these settings are informational only. 

1. Change any settings as needed.


<table id="table_03B0D41E2A574BB98B28A8D845BE3CDB"> 
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


1. Click ** `Code` ** and enter any custom header and footer JavaScript to execute at the top of the library, such as `targetPageParams`. 
   If you used `mbox.js` in the past, you might notice fewer fields. However, there are ways to do many of the same things in `at.js` that you did in `mbox.js`. For example, if you used mbox parameters in `mbox.js`, in `at.js` you can use [targetPageParamsAll](r_target-atjs-targetpageparamsall.md#reference_97E77FCDD793403685ECCA5A44305F93). The `mbox.js` Extra JavaScript field is replaced by the `at.js` Header and Footer fields, which provide more control of the code. 

1. Click ** `Save` **. 

1. Return to the Implementation page and click ** `Download at.js` **. 



## Download at.js Using the Target Download API {#section_C0D9D2A9068144708D08526BA5CA10D0}

To download `at.js` using the API. 

1. Get your client code.
   Your client code is available at the top of the ** `Setup` ** > ** `Implementation` ** > ** `Edit at.js Settings` ** page of the `Target` interface. 

1. Get your admin number.
   Load this URL:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<
<span class="varname">client code</span>>
   ```

   Replace `< * `client code` *>` with the client code from Step 1. 
   The result of loading this URL should look similar to the following example:

   ```
   {
     "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1"
   }
   ```

   In this example, "6" is the admin number.

1. Download `at.js`. 
   Load this URL with the following structure:

   ```
   https://admin<
<span class="varname">admin number</span>>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<
<span class="varname">client code</span>>&amp;version=<version number>
   ```


    * Replace `< * `admin number` *>` with your admin number. 

    * Replace `< * `client code` *>` with the client code from Step 1. 

    * Replace `< * `version number` *>` with the desired [ `at.js` version number](r_target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) (for example, 0.9.4). 


   Loading this URL starts the download of your customized `at.js` file. 


