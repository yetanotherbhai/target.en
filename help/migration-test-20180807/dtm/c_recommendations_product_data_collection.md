---
description: Display data mboxes send updated catalog data for recommendations, and display product recommendations.
keywords: Dynamic tag management
seo-description: Display data mboxes send updated catalog data for recommendations, and display product recommendations.
seo-title: Recommendations Product Data Collection and Correlation Mbox with DTM
solution: Target
title: Recommendations Product Data Collection and Correlation Mbox with DTM
uuid: 01468905-8109-40e8-aa11-1b19e8dce9e7
index: y
internal: n
snippet: y
translate: y
---

# Recommendations Product Data Collection and Correlation Mbox with DTM

Display data mboxes have two purposes:

* Show recommendations, like any other mbox

* Send dynamic catalog data to the recommendations server

Sending updated catalog data ensures that the recommendations displayed on your site always include the most updated information about your products. Display data mboxes make an offline catalog import strategy unnecessary. The display data mbox sends the `productId` or `productPurchasedId` (referred to as `entity.id` in the code) that is used in the algorithms. 
Using DTM to deploy these on a product page is identical to the OrderConfirmation Mbox process. The process involves two steps:

1. Create data elements.
1. Create a page load rule.

