---
description: Operational milestones help you determine whether your migration is complete.
keywords: operational milestones;migration;migrate from target classic to target standard
seo-description: Operational milestones help you determine whether your migration is complete.
seo-title: Managing the Transition
solution: Target
title: Managing the Transition
topic: Premium
uuid: 8e4b80f7-b582-41f2-9eba-6ed0b051d52c
index: y
internal: n
snippet: y
translate: y
---

# Managing the Transition

Check the following operational milestones:


<table id="table_C6EF0E7850B94C0BA2713F081EA6937C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Step</th> 
   <th colname="col2" class="entry">Milestone</th> 
   <th colname="col3" class="entry">Details</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><img href="../a4t/graphics/step1_icon.png" id="image_8EDE37E33BAC44F4A98DF71698FF58B7" /> </td> 
   <td colname="col2"><a href="../ov2/c_target-implement.xml#concept_60B748DE4293488F917E8F1FA4C7E9EB" format="dita" scope="local">Deploy either mbox.js or at.js</a> on your site </td> 
   <td colname="col3"> <p>Deploy one of the following:</p> 
    <ul id="ul_46B825DED1234424A2E57A02E10A60DA"> 
     <li id="li_2FDCAB8D9E944606B3EFEDDF874E0CF1"><a href="../ov2/c_target-atjs-implementation.xml#concept_8AC8D169E02944B1A547A0CAD97EAC17" format="dita" scope="local">at.js</a> </li> 
     <li id="li_B6A321C4A3BE492BA39B075ECA362D0D"><a href="t_mbox_download.xml#task_4EAE26BB84FD4E1D858F411AEDF4B420" format="dita" scope="local">mbox.js</a> version 53 or later (if not using Marketing Cloud <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/core-services-overview.html" format="https" scope="external">Core Services</a>) </li> 
     <li id="li_6302DF7D889440B5A269D6D421024AA6">mbox.js version 58 or later (if using Marketing Cloud Core Services)</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><img href="../a4t/graphics/step2_icon.png" id="image_3A43329215D34B569536B706E625DBA3" /> </td> 
   <td colname="col2"><a href="https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Deactivating_a_Campaign.html" format="https" scope="external">Deactivate</a> and archive or delete Target Classic activities when they end </td> 
   <td colname="col3">Build a deactivation schedule for any remaining Target Classic activities.</td> 
  </tr> 
  <tr> 
   <td colname="col1"><img href="../a4t/graphics/step3_icon.png" id="image_392B266D65A3455FBC936B5F892B3883" /> </td> 
   <td colname="col2">Move evergreen activities to Target Standard/Premium</td> 
   <td colname="col3">Re-create your evergreen campaigns in Target Standard (or hard code if available) and close the Target Classic campaigns.</td> 
  </tr> 
  <tr> 
   <td colname="col1"><img href="../a4t/graphics/step4_icon.png" id="image_CF7C2F5F3955448FBC8B2BD53D91AD41" /> </td> 
   <td colname="col2">Rebuild your <a href="../target/c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local">audiences</a> in Target Standard/Premium (Audiences + Expression Targets) </td> 
   <td colname="col3">Use the <a href="../target/t_create-audience.xml#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local">customized audiences capabilities</a> in Target Standard/Premium to re-create your audiences. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><img href="../a4t/graphics/step5_icon.png" id="image_8BD96B901C2E4AB2A8748176D101F102" /> </td> 
   <td colname="col2"> Create all of your new<a href="../target/c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local">activities</a> in Target Standard/Premium </td> 
   <td colname="col3">Set all Target Classic users to Read Only or Editor to prevent new activities from being published from Target Classic.</td> 
  </tr> 
  <tr> 
   <td colname="col1"><img href="../a4t/graphics/step6_icon.png" id="image_49449656FE924B02B1B63A350CE6EF4A" /> </td> 
   <td colname="col2"> Run a test using the <a href="../target/c_experiences.xml#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local">Visual Experience Composer</a> </td> 
   <td colname="col3">Verify successful delivery and reporting.</td> 
  </tr> 
 </tbody> 
</table>

