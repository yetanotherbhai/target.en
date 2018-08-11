---
description: To use Target Standard or Target Premium, add one line of code to call mbox.js.
keywords: Implementation;Mbox;download mbox.js;download api;mbox.js api
seo-description: To use Target Standard or Target Premium, add one line of code to call mbox.js.
seo-title: mbox.js Implementation
solution: Target
subtopic: Getting Started
title: mbox.js Implementation
topic: Standard
uuid: b14ae295-4591-49e0-98ab-70dd17aab42c
index: y
internal: n
snippet: y
translate: y
---

# mbox.js Implementation

You can use either of two library references: [!DNL  mbox.js] or [!DNL  at.js]. [ Understanding the Target JavaScript Libraries ](../../c_seting_up_target/c_implementing_target/c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB) explains the differences between the two libraries. 


>[!NOTE]
>
>The mbox.js library is still supported, but there will be no feature updates. All customers should migrate to at.js. For more information, see[ Migrate to at.js from mbox.js ](../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/t_target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA). 



The single reference to [!DNL  mbox.js] on each page provides the libraries needed for all of your activities. [!DNL  mbox.js] calls [!DNL  Target] from every page that references the [!DNL  mbox.js] file. This enables [!DNL  Target] to do the following: 


* Deliver Target activities
* Track clicks
* Track most success metrics



>[!TIP]
>
>To simplify implementation, you could reference [!DNL  mbox.js] in your global header. 



This video explains how to implement [!DNL  mbox.js]. 



<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> mbox.js Implementation Overview </th> 
   <th colname="col3" class="entry"> 8:52 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/f-A1zET6AwE/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/f-A1zET6AwE/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F">Select the correct settings for your <span class="filepath"> mbox.js </span> file </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Implement <span class="keyword"> Target </span> by adding the <span class="filepath"> mbox.js </span> file to the &lt;head&gt; of your site </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

You do not need to maintain different activity-specific versions of the file. 

>1. Reference [!DNL  mbox.js] in the ` &amp;lt;head&amp;gt;` section of each page on your site.

>       ` <script src="/ * ` directory` */ * ` scripts` */mbox.js"></script>` 

>       Where ` * ` directory` */ * ` scripts` *` is the directory where you saved your [!DNL  mbox.js] file after downloading it. 
