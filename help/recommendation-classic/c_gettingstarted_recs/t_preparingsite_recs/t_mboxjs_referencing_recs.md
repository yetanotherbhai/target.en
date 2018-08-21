---
description: Any Web page that includes an mbox must reference the mbox.js file on the host. This allows the page to contact the recommendations server.
seo-description: Any Web page that includes an mbox must reference the mbox.js file on the host. This allows the page to contact the recommendations server.
seo-title: Referencing the mbox.js File on Your Web Pages
solution: Target
title: Referencing the mbox.js File on Your Web Pages
topic: Recommendations
uuid: 1aa4d2b2-2b27-406b-97a1-e5e33b700351
index: y
internal: n
snippet: y
translate: y
---

# Referencing the mbox.js File on Your Web Pages


>[!NOTE] {class="- topic/note "}
>
>Add the ` mbox.js` reference to an include or header file that exists in the head all of your Web pages. 

Keep the following points in mind when adding the ` mbox.js` reference to a Web page: 

* Add the reference to the Web page only once, regardless of the number of mboxes on the page.
* Use a relative or absolute path depending on where you saved your ` mbox.js` and as suits your file structure. An absolute path is preferred. 

* Best practice is to place the reference in the head section, but you can place it anywhere before the first mbox on your page.

>1. Create the reference code.

>       For example, if the ` mbox.js` file is saved in a directory called ` /js`, the reference must be similar to: 

>    
>       ```
>       <script src="http://www.mycompany.com/js/mbox.js" type="text/javascript"></script>
>       ```

>1. Add a reference to the head section of all Web pages that will have an mbox.

>       For example: 
>    
>       ```
>       <head> 
>        
>       <script src="http://www.mycompany.com/js/mbox.js" type="text/javascript"></script> 
>        
>       </head> 
>       ```
>[!MORE_LIKE_THIS] {class="- topic/related-links "}
>
>* [ Preparing Your Website for Recommendations ](t_preparingsite_recs.md#task_30B8C075A14B426F9042119553F750B8)
>* [ Referencing the mbox.js File on Your Web Pages ](t_mboxjs_referencing_recs.md#task_69315D69881442209EB5CC8A5644CF37)
>* [ Downloading the mbox.js Library File ](t_mboxjs_dl_recs.md#task_6B577DD43FD346F7BC01962DAA822816)
>* [ Validating the mbox.js Download ](t_Validating_the_mboxjs_Download.md#task_FA78EB3B991C43F9ADE507A16522B770)
>* [ Implementing Display Data Mboxes ](t_data_mboxes_implementings_recs.md#task_83C1EA8433C249E1AC4BBEF591AC4FC3)
>* [ Implementing an Order-Confirmation Details Mbox ](t_mbox_orderconfirm_implementing_recs.md#task_AC372C1B9DFC4F5FB9DB4BDC759343EA)
>* [ Placing Mboxes to Display Recommendations ](t_mbox_placing_recs.md#task_F3638B849C9B45F197DBE49791AE13A1)
