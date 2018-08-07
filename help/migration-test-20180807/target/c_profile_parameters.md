---
description: Profile attributes are parameters that are specific to the visitor. These attributes are stored in the visitor's profile to provide information about the visitor that can be used in your campaigns.
keywords: Recommendations
seo-description: Profile attributes are parameters that are specific to the visitor. These attributes are stored in the visitor's profile to provide information about the visitor that can be used in your campaigns.
seo-title: Profile Attributes
solution: Target
title: Profile Attributes
topic: Premium
uuid: f0ba144b-058f-4d57-bb32-cd4d81c8e9b2
index: y
internal: n
snippet: y
translate: y
---

# Profile Attributes

As the visitor browses, or when the visitor returns for another session, the saved profile attributes can be used to target content, or log information for segment filtering.
To set up profile attributes, click ** `Audiences` ** > ** `Profile Scripts.` ** 
The following types of profile attributes are available:


<table id="table_B82609FE1EC84FB194189F4FE07B0884"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Parameter Type</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Mbox</p> </td> 
   <td colname="col2"> <p>Passed in directly through page code when creating the mbox. See <a href="../ov/c_pass_parameters_to_global_mbox.xml#concept_33362A04146C4E3C8E7089B65F38B5E5" format="dita" scope="local">Passing Parameters to a Global Mbox</a>. </p> <p> <p>Note: <span class="keyword">Target</span> has a limit of 50 unique profile attributes per mbox call. If you need to pass more than 50 profile attributes to <span class="keyword">Target</span>, you can pass them using the <span class="wintitle">Profile Update</span> API method. For more information, see <a href="https://www.adobe.io/apis/marketingcloud/target/docs/reference/profiles/profile-update.html" format="html" scope="external">Profile Update</a> in the Adobe Target API documentation. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Script</p> </td> 
   <td colname="col2"> <p>Defined directly with a JavaScript code snippet. These can store running totals like total money spent by consumer and are executed on each mbox request. See <a href="c_script_profile_attributes.xml#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local">Script Profile Attributes</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


>[!NOTE]
>
>`Target` has a limit of 50 unique profile attributes per mbox call. If you need to pass more than 50 profile attributes to `Target`, you can pass them using the `Profile Update` API method. For more information, see [Profile Update](https://www.adobe.io/apis/marketingcloud/target/docs/reference/profiles/profile-update.html) in the Adobe Target API documentation. 


