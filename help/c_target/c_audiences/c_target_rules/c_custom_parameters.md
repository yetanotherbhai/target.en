---
description: Custom parameters are mbox parameters. If you pass any mbox parameters to mboxes, or use the targetPageParams function, those parameters appear here for use in audiences.
keywords: custom parameters;target custom parameters;targetpageparams;targeting mbox parameters
seo-description: Custom parameters are mbox parameters. If you pass any mbox parameters to mboxes, or use the targetPageParams function, those parameters appear here for use in audiences.
seo-title: Custom Parameters
solution: Target
title: Custom Parameters
topic: Standard
uuid: f4344626-709b-4ec9-9b58-5b88ffdebbd7
index: y
internal: n
snippet: y
translate: y
---

# Custom Parameters

For more information, see [ Passing Parameters to a Global Mbox](https://marketing.adobe.com/resources/help/en_US/target/ov/c_pass_parameters_to_global_mbox.html). 

This video includes information about using audience categories. 

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Audiences </th> 
   <th colname="col3" class="entry"> 9:58 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/wV9lVTSOxMk/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/wV9lVTSOxMk/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Create audiences </li> 
      <li id="li_8529CB01E80B4C89B74287882AE0DA9D">Define audience categories </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

When creating a custom audience based on an mbox parameter, ` mboxParameter` no longer prompts you for ` mboxName`. mbox name is now optional. This change lets you use parameters from multiple mboxes or reference a parameter that has not yet been recorded on the edge. 

To select the desired parameter: 


* While creating a new audience, select a parameter name from the list, start typing the first characters of the desired parameter name, or type the full name of the desired parameter name. 

* If you remember the mbox name, but not the parameter name, use the checkbox to filter on a known mbox passing the desired parameter. 



Using either method, there is no link between the mbox and the parameter. The audience will work on the basis of parameter across all mboxes that pass that parameter. 

If you edit an existing audience, the filtering criteria displays with the mbox name that was supplied during creation. 

The audience's [ definition details pop-up card](c_audiences.md#section_11B9C4A777E14D36BA1E925021945780) shows the parameter name in the Rules section. There is no reference to the mbox used for filtering. 
