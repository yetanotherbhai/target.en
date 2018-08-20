---
description: Wrap the default mbox around an entire table. Do not wrap rows.
seo-description: Wrap the default mbox around an entire table. Do not wrap rows.
seo-title: Placing an Mbox Around a Table
solution: Target
title: Placing an Mbox Around a Table
topic: Recommendations
uuid: bf954d1d-7e07-41ca-9866-1d180cd8e04f
index: y
internal: n
snippet: y
translate: y
---

# Placing an Mbox Around a Table




><table id="table_7F153BD58A154433988167D3E2B265FC"> 
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
       &lt;div&nbsp;class="mboxDefault"&gt; 
       
      &lt;table&gt; 
       
      &lt;tr&gt; 
       
      &lt;td&gt;peaches&lt;/td&gt; 
       
      &lt;td&gt;cherries&lt;/td&gt; 
       
      &lt;/tr&gt; 
       
      &lt;tr&gt; 
       
      &lt;td&gt;walnuts&lt;/td&gt; 
       
      &lt;td&gt;almonds&lt;/td&gt; 
       
      &lt;/tr&gt; 
       
      &lt;/table&gt; 
       
      &lt;/div&gt; 
       
      &lt;script&nbsp;type="text/javascript"&nbsp;&gt;&nbsp;mboxCreate('myMbox'); 
       
      &lt;/script&gt; 
       
     </codeblock> </p> </td> 
   <td colname="col2"> <p> 
     <codeblock>
       &lt;table&gt; 
       
      &lt;div&nbsp;class="mboxDefault"&gt; 
       
      &lt;tr&gt; 
       
      &lt;td&gt;peaches&lt;/td&gt; 
       
      &lt;td&gt;cherries&lt;/td&gt; 
       
      &lt;/tr&gt; 
       
      &lt;tr&gt; 
       
      &lt;td&gt;walnuts&lt;/td&gt; 
       
      &lt;td&gt;almonds&lt;/td&gt; 
       
      &lt;/tr&gt; 
       
      &lt;/div&gt; 
       
      &lt;/table&gt; 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!MORE_LIKE_THIS]
>
>* [ Placing an Mbox Around a Table Cell ](r_Placing_an_Mbox_Around_a_Table_Cell.md#reference_CBE33BC9DE884F14B39478818C164F43)
>* [ Creating Multiple Mboxes on a Page ](c_Creating_Multiple_Mboxes_on_a_Page.md#concept_4AC9A22530C44C7580877B5DD4C5F863)
>* [ Creating a Whole Page as an Mbox ](r_Creating_a_Whole_Page_as_an_Mbox.md#reference_F3E59E7326D946E4897AE41C3A6B40CE)
>* [ Creating a Dynamic Mbox ](r_Creating_a_Dynamic_Mbox.md#reference_60A14E7EB8754383B2DC6A7E4D531AB4)
