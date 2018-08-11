---
description: Target Standard and Premium use a modified version of the Adobe Target mbox.js file.
keywords: Implementation;Mbox;mbox.js;download mbox.js;configure mbox.js
seo-description: Target Standard and Premium use a modified version of the Adobe Target mbox.js file.
seo-title: Download mbox.js
solution: Target
subtopic: Getting Started
title: Download mbox.js
topic: Standard
uuid: 24f6cdac-5b7d-4153-88cb-96056c4c1708
index: y
internal: n
snippet: y
translate: y
---

# Download mbox.js

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
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Implement <span class="keyword"> Target </span> by adding the <span class="filepath"> mbox.js </span> file to the <span class="codeph"> &amp;lt;head&amp;gt; </span> of your site </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

To use the [!DNL  Adobe Target] [!UICONTROL  Visual Experience Editor], you must include an additional line of JavaScript as part of your [!DNL  mbox.js] file. 

>1. Click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] ** in [!DNL  Target Standard].
>1. Click ** [!UICONTROL  Download mbox.js] ** and follow the prompts to save the file.
>1. (Conditional) If you use [!DNL  mbox.js] version 60 or later, you can configure the library to automatically hide page content by default until mboxes load to reduce flicker on responsive sites.
>   For more information, see "Suppress page-load flicker" in [ mbox.js Advanced Settings ](r_advanced_mboxjs_settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C). 
>
>1. Create the [!DNL  mbox.js] reference on the website.

>       Beginning with [!DNL  mbox.js] version 57, the [!DNL  mbox.js] reference can be placed anywhere within the ` &amp;lt;head&amp;gt;` section of the page. 


>       >[!IMPORTANT]
>       >
>       >If you use a version of [!DNL  mbox.js] prior to version 57, the reference must be the last item in the ` &amp;lt;head&amp;gt;` section of your pages. If the reference is not the last item, serious display or performance issues could result. See [ Technical Implementation Details ](https://marketing.adobe.com/resources/help/en_US/target/ov/c_mbox_technical.html) for more information. 

>1. Upload the saved [!DNL  mbox.js] file to the location in your hosting environment that you specified in the code.
