---
description: It is useful to understand how the integration between Adobe Target and Adobe Analytics works.
keywords: Marketing cloud audiences;Shared audiences
seo-description: It is useful to understand how the integration between Adobe Target and Adobe Analytics works.
seo-title: Target and Analytics Integration Overview
solution: Target,Analytics,Marketing Cloud
title: Target and Analytics Integration Overview
uuid: 0b5dc133-3773-44c1-8ae0-04909c9db057
index: y
internal: n
snippet: y
translate: y
---

# Target and Analytics Integration Overview

This video explains how to use Adobe Analytics as a reporting source in Adobe Target to drive the analysis of your optimization program.


<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2">Analytics for Target (A4T)</th> 
   <th colname="col3" class="entry">4:32</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/eS_LeNmcJug/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/eS_LeNmcJug/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_536EBE8EF3D34C2BBB43043DA339F371"> <p>Explain what A4T is and why you would use it</p> </li> 
      <li id="li_BCE359271A534D8D9F880C98A0D8811B"> <p>Explain how A4T works</p> </li> 
      <li id="li_0CACB4D122324A659025639A3567DC6F"> <p>Understand the prerequisites needed before using A4T</p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

The integration that enables Adobe Analytics as the data source for Adobe Target (A4T) represents the next generation of the Test&amp;Target to SiteCatalyst plug-in. This plug-in has been deprecated, but is still supported for customers who already use it.
A server-to-server call from Target to Analytics sends campaign and experience information to Analytics.

>[!NOTE]
>
>This integration does not result in additional server calls for either Target or Analytics.


The "Target Activities" report in Adobe Analytics provides data about Target experiences and activities. Target Standard uses Analytics web services to pull the data into Target Standard.
All Analytics metrics (including calculated, etc) are available in Target Standard and the Target Activities report in Analytics. Likewise, any segment available in Analytics can be applied to the Target Activities report in Analytics, as well as in Target Standard.
Segments created in Analytics can be applied to any test, even if the segments are created after the test has completed.
Only one mbox-based metric is allowed when using Analytics as the reporting source.
