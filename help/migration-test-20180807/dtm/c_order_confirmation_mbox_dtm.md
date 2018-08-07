---
description: The orderConfirmPage mbox records details about your product, permitting reports on sales data, orders, and recommendations.
keywords: Dynamic tag management
seo-description: The orderConfirmPage mbox records details about your product, permitting reports on sales data, orders, and recommendations.
seo-title: Deploy an Order Confirmation Mbox Through Dynamic Tag Manager
solution: Target
title: Deploy an Order Confirmation Mbox Through Dynamic Tag Manager
uuid: 6c4ae93a-aaf2-4e7a-b259-568ac04ac93c
index: y
internal: n
snippet: y
translate: y
---

# Deploy an Order Confirmation Mbox Through Dynamic Tag Manager

Use an Order Confirmation Mbox on the Thank you or Confirmation page in checkout.
The `orderConfirmPage` mbox requires three parameters (name-value pairs) to be passed to Adobe target for data collection through the mbox: 

* orderID
* orderTotal (Amount of sales)
* product PurchasedID (SKUs)
To set up an order confirmation mbox through DTM, you must:

1. Create data elements.
1. Create a page load rule.
