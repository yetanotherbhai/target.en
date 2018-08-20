---
description: You can set up an entire page as an mbox.
seo-description: You can set up an entire page as an mbox.
seo-title: Creating a Whole Page as an Mbox
solution: Target
title: Creating a Whole Page as an Mbox
topic: Recommendations
uuid: 0b115393-7966-4a52-b3b7-1022c7c346af
index: y
internal: n
snippet: y
translate: y
---

# Creating a Whole Page as an Mbox


>Use an mbox to replace all of the content between the ` <body></body>` tags. Do not place the mbox outside the ` body` tags. Mboxes depend on the ` <body> onLoad` function to execute, and mbox recursion problems can occur when a ` <body>` is used in an offer. 

>
>```
><html> 
> 
><body> 
> 
><div class=”mboxDefault”> 
> 
><...> 
> 
>... 
> 
></...> 
> 
></div> 
> 
><script type="text/javascript" > mboxCreate(‘wholePageMbox’); 
> 
></script> 
> 
></body> 
> 
></html>
>```

>[!MORE_LIKE_THIS]* [ Placing an Mbox Around a Table ](r_Placing_an_Mbox_Around_a_Table.md#reference_361F35DEA8CC4E2B87B470F72C9E344F)* [ Placing an Mbox Around a Table Cell ](r_Placing_an_Mbox_Around_a_Table_Cell.md#reference_CBE33BC9DE884F14B39478818C164F43)* [ Creating Multiple Mboxes on a Page ](c_Creating_Multiple_Mboxes_on_a_Page.md#concept_4AC9A22530C44C7580877B5DD4C5F863)* [ Creating a Dynamic Mbox ](r_Creating_a_Dynamic_Mbox.md#reference_60A14E7EB8754383B2DC6A7E4D531AB4)