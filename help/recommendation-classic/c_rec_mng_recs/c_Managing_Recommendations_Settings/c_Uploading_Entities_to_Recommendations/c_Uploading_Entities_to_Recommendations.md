---
description: You can create a .CSV file that contains display information for your products, then bulk upload it to the recommendations server.
seo-description: You can create a .CSV file that contains display information for your products, then bulk upload it to the recommendations server.
seo-title: Uploading Entities to Recommendations
solution: Target
title: Uploading Entities to Recommendations
topic: Recommendations
uuid: 75bd22d0-6c17-42d4-933c-398b68c885ec
index: y
internal: n
snippet: y
translate: y
---

# Uploading Entities to Recommendations

Use the bulk upload method to send display information if you don't have mboxes on your page, or you want to supplement your display information with items that are not available on your site. For example, you might want to send inventory information that might not be published on your site. 

Any data uploaded using the upload template file overwrites that value in our database, so if you send price information in JavaScript and then send different price values in the file, the values in the file override the information sent with JavaScript. 


>[!NOTE]
>
>You can't overwrite an existing value with a blank value. You have to pass another value in its place to overwrite it. In the case of sale price, a common solution is to either pass in an actual "NULL" or some other message. You can then write a template rule to exclude items with that value.



The product is available in the admin interface approximately two hours after successfully uploading its entity. 
>[!MORE_LIKE_THIS] {class="- topic/related-links "}* [ Creating Global Exclusions ](t_Creating_Global_Exclusions.md#task_ABDA6F68D8BD47988A67A06396121318)* [ Using Entity Feeds ](t_Using_Entity_Feeds.md#task_4034B221DC754633B1280893AE6B5F86)