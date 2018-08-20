---
description: If you use the backup recommendation feature, any recommendation that does not have enough recommended items will not display default content. Instead, recommendations display the results of the backup algorithm.
seo-description: If you use the backup recommendation feature, any recommendation that does not have enough recommended items will not display default content. Instead, recommendations display the results of the backup algorithm.
seo-title: Using a Backup Recommendation
solution: Target
title: Using a Backup Recommendation
topic: Recommendations
uuid: c1f3593b-b3f6-4373-9b4d-e38a7b27bcb6
index: y
internal: n
snippet: y
translate: y
---

# Using a Backup Recommendation

If you do not use a backup recommendation, if a recommendation does not have enough items to fill the display, the system displays default content to the user. 

The backup recommendation feature always uses the top-viewed items on the site to fill in any remaining slots after the algorithm's data is used. For example, your template is configured to show five recommended items, and you're using the *Purchase Affinities* algorithm. However, you only have enough data to fill two of the five slots, so the backup recommendation feature fills the other three spots with top-viewed items. 

Backup recommendations are randomly chosen from the top 500 most-viewed products across the entire site. The data time period for backup recommendations is one week. 

The 500 most-viewed results are ordered sequentially and then split into buckets of 20. The buckets are served in order, but the results inside each bucket are randomized and returned to the page. If users refresh the page, they are presented with new, randomized results. If the result set from the union of the collection and the filtering rules is smaller than 20, it will randomly select from the collection. 


>[!NOTE] {class="- topic/note "}
>
>If you group your items into catalogs, the backup recommendations generated for each algorithm within the recommendation also uses the catalog, so only items in the catalog are included in the backup recommendation.



Any item that is excluded by global exclusion rules is not served as a backup recommendation. 

Backup recommendations are enabled by default and fill in the extra slots in a template with a random selection of the most popular items on the site. 

Duplicates are removed from batches of recommendations. 

Using backup recommendations is usually part of the discussion with the implementation team during your initial setup. If you want to change the backup recommendation setting after implementation, contact your account manager. 

If partial rendering (see [ Content Serve Settings](../../c_rec_mng_recs/c_Setting_Up_and_Deleting_a_Recommendation/t_create_edit_recs/c_content_serve_settings.md#concept_828721CF007E430DAC6E9ABFCDFA5CA4)) is not enabled and the template doesn't show, then either the backup recommendation or default content is shown instead. 
>[!MORE_LIKE_THIS] {class="- topic/related-links "}* [ Creating or Editing a Recommendation ](t_create_edit_recs.md#task_07791608B4DB4B3EB0EF981116F4B4E2)* [ Previewing a Recommendation ](t_previewing_recs.md#task_0841AD9A5CF640719A486C24F7D4D14F)* [ Using Preview Options to Change the Page View ](r_previewoptions_recs.md#reference_8EBD7A9F6CF247B79A9FDCB85AB55C82)* [ Deleting a Recommendation ](t_deleting_recs.md#task_0364B109FE5D4D0C81204F69DA001AD1)