---
description: You should place mboxes everywhere on the site where your recommendations display. This might include the home page, category pages, product or article pages, shopping cart, order confirmation pages, and so on.
seo-description: You should place mboxes everywhere on the site where your recommendations display. This might include the home page, category pages, product or article pages, shopping cart, order confirmation pages, and so on.
seo-title: Placing Mboxes to Display Recommendations
solution: Target
title: Placing Mboxes to Display Recommendations
topic: Recommendations
uuid: 53904f60-6d2e-43cd-a45c-ed36ade8e941
index: y
internal: n
snippet: y
translate: y
---

# Placing Mboxes to Display Recommendations

The ` div` before the mbox should be around the default content that displays if no recommendation is returned. The mbox name is completely customizable, but it must be shorter than 255 characters. 

If you display affinity recommendations (those based on a dynamic ` entity.categoryId` or ` entity.id`) in the mbox, then pass the applicable value as an mbox parameter in the ` mboxCreate` call. 

You can display a recommendation based either on a category or on a product. For a category-based recommendation, the code might look like this: 


```
<body> 
 
My existing page. 
 
<div class="mboxDefault"> 
 
Part that I'd like to overlay when a recommendation is displayed 
 
</div> 
 
<script type="text/javascript"> 
 
mboxCreate('sidebar_recommendations','entity.categoryId=EN:Guide:1'); 
 
</script> 
 
</body>
```


For a product-based recommendation, the code might look like this: 


```
<body> 
 
My existing page. 
 
<div class="mboxDefault"> 
 
Part that I'd like to overlay when a recommendation is displayed 
 
</div> 
 
<script type="text/javascript"> 
 
mboxCreate('sidebar_recommendations',’entity.id=12345’); 
 
</script> 
 
</body>
```



>[!NOTE] {class="- topic/note "}
>
>You can pass both the ` entity.categoryId` and ` entity.id` values and then determine what to base the recommendation on when setting up the recommendation. 



For more information about placing an mbox, see [ Using an Mbox on Your Web Site ](../../c_rec_mng_recs/c_Managing_Mboxes/t_Using_an_Mbox_on_Your_Web_Site.md#task_0A087749BA75438D988726255BF097BB). 
>[!MORE_LIKE_THIS] {class="- topic/related-links "}* [ Preparing Your Website for Recommendations ](t_preparingsite_recs.md#task_30B8C075A14B426F9042119553F750B8)* [ Downloading the mbox.js Library File ](t_mboxjs_dl_recs.md#task_6B577DD43FD346F7BC01962DAA822816)* [ Validating the mbox.js Download ](t_Validating_the_mboxjs_Download.md#task_FA78EB3B991C43F9ADE507A16522B770)* [ Referencing the mbox.js File on Your Web Pages ](t_mboxjs_referencing_recs.md#task_69315D69881442209EB5CC8A5644CF37)* [ Implementing Display Data Mboxes ](t_data_mboxes_implementings_recs.md#task_83C1EA8433C249E1AC4BBEF591AC4FC3)* [ Implementing an Order-Confirmation Details Mbox ](t_mbox_orderconfirm_implementing_recs.md#task_AC372C1B9DFC4F5FB9DB4BDC759343EA)