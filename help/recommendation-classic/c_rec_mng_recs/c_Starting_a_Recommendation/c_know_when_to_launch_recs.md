---
description: Launch a recommendation once data is being collected.
seo-description: Launch a recommendation once data is being collected.
seo-title: Knowing When to Launch a Recommendation
solution: Target
title: Knowing When to Launch a Recommendation
topic: Recommendations
uuid: c3b45a3e-8e4e-4aa6-bc30-de6359ad6c8a
index: y
internal: n
snippet: y
translate: y
---

# Knowing When to Launch a Recommendation

The recommendations server begins gathering item description data when mboxes are placed on the site or the entity details are uploaded via a CSV file, even if no recommendations are set up yet. These mboxes also start capturing usage data, such as views and purchases of products that are used for the recommendations algorithms. If you use Adobe Analytics for algorithm data, this information is also immediately available. 

When a new recommendation is created, or a new algorithm is added to an existing recommendation, data is generated within 30 minutes for the algorithm(s). These new algorithms use existing item information and usage information, and data gathering starts before each algorithm is created. If an existing algorithm is updated or changed, then the changes are used by the system the next time the algorithm is run. 

The algorithm schedule is determined by the data range specified for the algorithm. If one day of data is used, the algorithm updates every two to four hours. If two months of data is selected, then the algorithm updates every 24 hours. After the initial run of an algorithm within 30 minutes of creation, it runs on this schedule. 

Algorithm filters and weighting are applied during these algorithm updates. Other controls like inventory and price rules are applied at display time. When the recommendations server is updated with item information about price and inventory (either via an mbox or csv upload), those changes are immediately reflected in the recommendation displaying on the site, even if the algorithm has not updated yet. 

To confirm that recommendations are prepared and ready to go, download the recommendation output from the edit page by clicking the orange x icon next to the name. The downloaded file includes all recommendation data that is ready. The recommendation is ready to be activated there is one row per key for an algorithm based on a particular product or category view. For a popularity algorithm, only one row of data displays. 
>[!MORE_LIKE_THIS]
>
>* [ Activating a Recommendation ](t_activate_recs.md#task_B0A6D22AA72E405DBEC81D22B12477DF)
>* [ Deactivating a Recommendation ](t_deactivate_recs.md#task_EE1A8BDC4C3E4FBE8D694DF31CFC2DDC)
