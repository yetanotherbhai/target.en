---
description: If you use a page template to provide structure to your pages, or if your pages contain similar elements, this feature makes it possible to test variations in similarly structured page elements.
keywords: template testing;template;same experience on similar pages;template test
seo-description: If you use a page template to provide structure to your pages, or if your pages contain similar elements, this feature makes it possible to test variations in similarly structured page elements.
seo-title: Include the Same Experience on Similar Pages
solution: Target
title: Include the Same Experience on Similar Pages
topic: Premium
uuid: a17fe6ed-1341-487d-a84f-9811cf97ed13
index: y
internal: n
snippet: y
translate: y
---

# Include the Same Experience on Similar Pages

To work correctly, this feature must be used on pages that have a very similar structure. or contain template elements that are structured the same on all pages. 


>[!IMPORTANT]
>
>Using this feature to change elements across dissimilar pages will likely cause unexpected results.



For example, you might use this feature to do one of the following: 

* Test a global navigation bar by rearranging or removing elements
* Remove an item from all product pages that use a particular page template
* Add a banner to all product pages
* Change the layout of article template
The following demo video includes information about using a template: 



<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Visual Experience Composer (2 of 2) </th> 
   <th colname="col3" class="entry"> 7:29 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/qwUKEp8en_k/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/qwUKEp8en_k/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F">Rename and duplicate an experience </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Create a redirect experience </li> 
      <li id="li_79866ECECA2D4ACB9AE991B2922ADA84">Target an activity to a single URL or a group of URLs </li> 
      <li id="li_67ED273861FC493785AC049CC0B37E6A">Create a multi-page activity </li> 
      <li id="li_F4646D966373499DA6A32ED62411DF57">Preview and build experience for responsive websites </li> 
      <li id="li_4CA9280B227C4ACBB3EDDC23AB8ECCC3">Use overlays to highlight types of elements </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

You can specify pages that include the change elements, or apply the change across your site. 

>1. Create an activity as described in [ Activities](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).
>1. To specify the pages where the experience will appear, in the Visual Experience Composer click the gear icon, then select ** [!UICONTROL  URL] **.

>1. Click ** [!UICONTROL  Add Rule] **, then specify the criteria for the pages you want to add the experience to.

>    
>    1. Specify the page range. The page range can be one of the following: >    
>        * URL
>        * Domain
>        * Path
>        * Hash (#) Fragment (Target the part of a URL that follows the # symbol.)
>        * Query
>        * Mbox parameter


>    1. Choose an operator. The operator specifies how the items after the operator relate to the page range. Available operators are: 

>    
>        * Contains
>        * Does not contain
>        * Is
>        * Is not


>    1. Type the strings that define where the experience is added, such as the domain or the strings contained in the page name. For example, if you select ** [!UICONTROL  Domain] ** and ** [!UICONTROL  Is] **, type the domain where you want the experience added to all pages. 

>       You can include multiple items. 


>       >[!IMPORTANT]
>       >
>       >Multiple items use ` OR` logic, meaning that any single item in the list makes the condition true. 



>1. If desired, enter additional criteria by clicking ** [!UICONTROL  Add Criteria] **and repeating the procedure in the previous step.

