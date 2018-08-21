---
description: You should place an mbox on the order confirmation page to capture order information as input to be used by recommendation algorithms and for measuring the performance of your recommendations.
seo-description: You should place an mbox on the order confirmation page to capture order information as input to be used by recommendation algorithms and for measuring the performance of your recommendations.
seo-title: Implementing an Order-Confirmation Details Mbox
solution: Target
title: Implementing an Order-Confirmation Details Mbox
topic: Recommendations
uuid: e19dc139-7292-48ce-8730-52a1bd3a740f
index: y
internal: n
snippet: y
translate: y
---

# Implementing an Order-Confirmation Details Mbox

Sales data can be sent from any mbox, but the parameters must follow the strict syntax in the sample code below. The parameters ` orderId` and ` orderTotal` are required. The ` productPurchasedId` attribute must match the ` entity.id` display variable. 

` productPurchasedId` is only required if you are using mbox data to drive algorithms. It is highly recommended. 


>[!NOTE] {class="- topic/note "}
>
>Replace the text shown in bold with the real values for your product. Parameters are case sensitive and must be written "camel case" as shown.




```
<div class="mboxDefault"></div> 
 
<script type="text/javascript"> 
 
mboxCreate('orderConfirmPage', 
 
'productPurchasedId= 
<b class="+ topic ph hi-d="" b "="">
  LIST OF PRODUCT IDs FROM ORDER PAGE', 
  
 'orderId= 
 <b class="+ topic ph hi-d="" b "="">
   ORDER ID FROM ORDER PAGE', 
   
  'orderTotal= 
  <b class="+ topic ph hi-d="" b "="">
    ORDER TOTAL FROM ORDER PAGE'); 
    
   </script> 
  </b class="+ topic> 
 </b class="+ topic> 
</b class="+ topic>
```


` orderConfirmPage` is the default mbox and is recommended. 
Although it is recommended that you use the ` orderConfirmPage` mbox name, the name can be changed. If you change the name, you must contact consulting or Client Care. [!MORE_LIKE_THIS] {class="- topic/related-links "}
>
>* [ Preparing Your Website for Recommendations ](t_preparingsite_recs.md#task_30B8C075A14B426F9042119553F750B8)
>* [ Downloading the mbox.js Library File ](t_mboxjs_dl_recs.md#task_6B577DD43FD346F7BC01962DAA822816)
>* [ Validating the mbox.js Download ](t_Validating_the_mboxjs_Download.md#task_FA78EB3B991C43F9ADE507A16522B770)
>* [ Referencing the mbox.js File on Your Web Pages ](t_mboxjs_referencing_recs.md#task_69315D69881442209EB5CC8A5644CF37)
>* [ Implementing Display Data Mboxes ](t_data_mboxes_implementings_recs.md#task_83C1EA8433C249E1AC4BBEF591AC4FC3)
>* [ Placing Mboxes to Display Recommendations ](t_mbox_placing_recs.md#task_F3638B849C9B45F197DBE49791AE13A1)
