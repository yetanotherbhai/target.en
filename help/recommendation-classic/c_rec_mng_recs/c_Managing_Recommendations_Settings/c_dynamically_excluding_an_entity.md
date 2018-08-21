---
description: In the query string, you can pass entity ids for entities that you want to exclude from your recommendations. For example, you might want to exclude items that are already in the shopping cart.
seo-description: In the query string, you can pass entity ids for entities that you want to exclude from your recommendations. For example, you might want to exclude items that are already in the shopping cart.
seo-title: Dynamically Excluding an Entity
solution: Target
title: Dynamically Excluding an Entity
topic: Recommendations
uuid: 0ac9e18a-13f4-4a68-b53a-4a86787d21e4
index: y
internal: n
snippet: y
translate: y
---

# Dynamically Excluding an Entity

To enable the exclusion functionality, use the ` excludedIds` mbox parameter. This parameter points to a list of comma-separated entity ids. For example, ` mboxCreate(..., "excludedIds=1,2,3,4,5")`. The value is sent when requesting recommendations. 


>[!NOTE]
>
>If too many entities are excluded, recommendations behave as if there aren't enough entities to fill the recommendation template.



To excluded entityIds, append the ` &amp;excludes=${mbox.excludedIds}` token to the offer content url. When the content url is extracted, the required parameters are substituted using current mbox request parameters. 

By Default, this feature is enabled for newly created recommendations. Existing recommendations need to be saved to support Dynamically Excluded entities. 
