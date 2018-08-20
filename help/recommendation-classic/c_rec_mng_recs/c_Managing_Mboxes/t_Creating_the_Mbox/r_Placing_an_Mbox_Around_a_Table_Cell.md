---
description: Insert the default mbox within the cell, not outside the cell.
seo-description: Insert the default mbox within the cell, not outside the cell.
seo-title: Placing an Mbox Around a Table Cell
solution: Target
title: Placing an Mbox Around a Table Cell
topic: Recommendations
uuid: ab907d9e-2a4e-4175-a582-ce57e834836c
index: y
internal: n
snippet: y
translate: y
---

# Placing an Mbox Around a Table Cell




><table id="table_16FF5E62AC12497082F2B7E355699C89"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Right </th> 
   <th colname="col2" class="entry"> Wrong </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <codeblock>
       &lt;table&gt; 
       
      &lt;tr&gt; 
       
      &lt;td&gt; 
       
      &lt;div&nbsp;class="mboxDefault"&gt; 
       
      Peaches 
       
      &lt;/div&gt; 
       
      &lt;script&nbsp;type="text/javascript"&nbsp;&gt;&nbsp;mboxCreate('myMbox'); 
       
      &lt;/script&gt; 
       
      &lt;/td&gt; 
       
      &lt;td&gt;cherries&lt;/td&gt; 
       
      &lt;/tr&gt; 
       
      &lt;tr&gt; 
       
      &lt;td&gt;walnuts&lt;/td&gt; 
       
      &lt;td&gt;almonds&lt;/td&gt; 
       
      &lt;/tr&gt; 
       
      &lt;/table&gt; 
     </codeblock> </p> </td> 
   <td colname="col2"> <p> 
     <codeblock>
       &lt;table&gt; 
       
      &lt;tr&gt; 
       
      &lt;div&nbsp;class="mboxDefault"&gt; 
       
      &lt;td&gt;&nbsp;peaches&nbsp;&gt;&nbsp;&lt;/td&gt; 
       
      &lt;/div&gt; 
       
      &lt;td&gt;cherries&lt;/td&gt; 
       
      &lt;/tr&gt; 
       
      &lt;tr&gt; 
       
      &lt;td&gt;walnuts&lt;/td&gt; 
       
      &lt;td&gt;almonds&lt;/td&gt; 
       
      &lt;/tr&gt; 
       
      &lt;/table&gt; 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!MORE_LIKE_THIS]* [ Placing an Mbox Around a Table ](r_Placing_an_Mbox_Around_a_Table.md#reference_361F35DEA8CC4E2B87B470F72C9E344F)* [ Creating Multiple Mboxes on a Page ](c_Creating_Multiple_Mboxes_on_a_Page.md#concept_4AC9A22530C44C7580877B5DD4C5F863)* [ Creating a Whole Page as an Mbox ](r_Creating_a_Whole_Page_as_an_Mbox.md#reference_F3E59E7326D946E4897AE41C3A6B40CE)* [ Creating a Dynamic Mbox ](r_Creating_a_Dynamic_Mbox.md#reference_60A14E7EB8754383B2DC6A7E4D531AB4)