---
description: How you implement Target depends on whether you use mbox.js or at.js, and whether you use Adobe DTM.
keywords: technical implementation;migration;migrate from target classic to target standard;dtm;mbox,js;dynamic tag management;at.js
seo-description: How you implement Target depends on whether you use mbox.js or at.js, and whether you use Adobe DTM.
seo-title: Technical Implementation
solution: Target
title: Technical Implementation
topic: Premium
uuid: 12a86ab2-88c9-4fc6-9ec0-e56508a8d89c
index: y
internal: n
snippet: y
translate: y
---

# Technical Implementation

The technical implementation phase is complete when you have completed the following steps:


<table id="table_85803800F7E443F8A2FDAC8267B364BD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Step</th> 
   <th colname="col2" class="entry">Task</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><img href="../a4t/graphics/step1_icon.png" id="image_F0F2AF68C34544D3856622AE07408FEA" /> </td> 
   <td colname="col2">Implement mbox.js or at.js, with no incompatible plugins. <p> <p type="important">Note: If you are moving from <span class="keyword">Target Classic</span> to <span class="keyword">Target Standard/Premium</span> and want to continue using <span class="filepath">mbox.js</span>, you must download a new <span class="filepath">mbox.js</span> file from the <span class="keyword">Target Standard/Premium</span> UI and update your web pages accordingly, even if you already have <span class="filepath">mbox.js</span> deployed. This is especially important if you are planning to edit page content in the <span class="wintitle">Visual Experience Composer</span> (VEC) in <span class="keyword">Target Standard/Premium</span> (see <a href="../target/c_experience_composer_best_practices.xml#concept_E284B3F704C04406B174D9050A2528A6" format="dita" scope="local">Visual Experience Composer Best Practices and Limitations</a>). However, there are advantages when using the newer <span class="keyword">Target</span> JavaScript <span class="codeph">at.js</span> library that you should consider during the transition. For more information, see <a href="../ov2/c_target-implement.xml#concept_60B748DE4293488F917E8F1FA4C7E9EB" format="dita" scope="local">Understanding the Target JavaScript Libraries</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><img href="../a4t/graphics/step2_icon.png" id="image_B2F94231CCDC407BB07F98E1237ADEFB" /> </td> 
   <td colname="col2">A global mbox firing successfully either across your site globally or on pages where testing or tracking will occur.</td> 
  </tr> 
 </tbody> 
</table>

***Optional: My organization uses Adobe DTM to deploy the Marketing Cloud*** 
Follow the [deployment steps for DTM](https://marketing.adobe.com/resources/help/en_US/dtm/target/). 
***My digital properties are deployed on the latest library files for Target, either at.js or mbox.js V53+*** 
Either update your [mbox.js](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420) file or update to [at.js](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17). 

>[!NOTE]
>
>mbox.js V58 is the minimum version if using Marketing Cloud Core Services.



## mbox.js {#section_22295EBBD27445C3B9AC12DF24B90141}

Choose the option below that applies to you:

* ***I want to use my JavaScript library to auto-deploy my target-global-mbox for a Single Line of Code implementation*** Make sure the Auto Create option in the mbox.js download settings is enabled. To set the Auto Create option, click ** `Setup` ** > ** `Implementation` ** > ** `Edit mbox.js Settings` **, then enable ** `Auto create global mbox` **. 

  >[!NOTE]
  >
  >If you are on a Target Classic SKU, you might exceed your allotted number of server calls.


* ***I already have a global mbox deployed (hard coded) and want to keep it*** Ensure that the Auto Create option in the mbox.js download settings is enabled. To set the Auto Create option, click ** `Setup` ** > ** `Implementation` ** > ** `Edit mbox.js Settings` **, then enable ** `Auto create global mbox` **. 

* ***I have already deployed (hard coded) a global mbox, but I want to get rid of it in favor of auto deployment*** 
    1. Make sure the Auto Create option in the mbox.js download settings is enabled. To set the Auto Create option, click ** `Setup` ** > ** `Implementation` ** > ** `Edit mbox.js Settings` **, then enable ** `Auto create global mbox` **. 

    1. Remove your hard coded global mbox from your site code.
    1. Deploy the mbox.js file with these settings enabled.


  >[!NOTE]
  >
  >If you are on a Target Classic SKU, you might exceed your allotted number of server calls.


* ***I want to migrate to only a global mbox to reduce server calls*** 
    1. Make sure no Target Classic campaigns are running against your classic regional [mboxes](c_mboxes.md#concept_85E01D9DD0B64BD3A138C2D3DB83BD57).
    1. [Deactivate](c_activities.md#table_B68BB1AD61394C749822FF4938E404E7) other mboxes in the Target UI first to verify site experience.
    1. Remove Target Classic regional mboxes from your site code.

  For information about implementing mbox.js, see [Mbox.js Implementation](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420). 




## at.js {#section_1A3EA327724846E2B8DD49D82CBA5817}

***My digital property uses a Single Page Application Design and I want to use at.js instead of mbox.js*** 
Review the [at.js documentation](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) to make sure your Target implementation is compatible with the at.js library file. 
***Our deployment of Target uses Response Plugins*** 
Audit Response Plugins for illegal methods deprecated in the file. See [at.js Plugins](c_target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF). 
***Our mbox.js features custom code modifications or other edits*** 
Audit Custom Code for illegal methods deprecated in the file, for example AAM&gt;Target. See [at.js Limitations](c_target-atjs-limitations.md#concept_FA99E4D6EC274552BF45E01AFB76CCAE). 
***We make sure of custom site code using documented mbox.js methods*** 
Audit site code for illegal methods deprecated in the file, such as mboxFactory. See [at.js Limitations](c_target-atjs-limitations.md#concept_FA99E4D6EC274552BF45E01AFB76CCAE). 
***We fire a global mbox on a hash change, route change, or state change*** 
Work with Adobe Target Consulting to build an SPA Framework Plan for implementation.

## Next Step {#section_9DAF58FBB4D8458784A93692C46E0514}

[Advanced Feature Considerations](c_trans-advanced-feature-considerations.md#concept_D8DB7801889A464D9197A739F7B185A7) 
