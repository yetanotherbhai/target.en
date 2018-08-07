---
description: Upload 1st party data, called Customer Attributes, using the Marketing Cloud core service and choose attributes to share to Target. This functionality also exists in Adobe Analytics and integrates directly with Target.
keywords: customer attributes
seo-description: Upload 1st party data, called Customer Attributes, using the Marketing Cloud core service and choose attributes to share to Target. This functionality also exists in Adobe Analytics and integrates directly with Target.
seo-title: Customer Attributes
solution: Target
title: Customer Attributes
topic: Classic
uuid: c528dc26-cf15-4d5f-8e62-19f8a1682764
index: y
internal: n
snippet: y
translate: y
---

# Customer Attributes


>[!NOTE]
>
>For detailed information about Customer Attributes, including prerequisites, implementation details, and integration details, refer to[Customer Attributes](https://marketing.adobe.com/resources/help/en_US/mcloud/attributes.html) in the Marketing Cloud product documentation. 


Mbox.js version 58 or higher is required for Customer Attributes to work correctly with Target.
Target users have a lot of first party data about their customers that they want the Marketing Cloud to use to make better decisions for targeting and to better understand their Analytics data. The Customer Attributes feature makes it easy for customers to upload that data once and use it in Analytics and Target. Previously, Target users could use the Bulk Profile Update API but that data was exclusive to Target. Also, APIs can be more difficult for customers to integrate with than a FTP-based approach like Customer Attributes.
Attributes appear in Target audience creation under Visitor Profile with the prefix CRS (Customer Record Service). If the attribute in the file is `membershipLevel`, the attribute would appear as `crs.membershipLevel`. Target users must build audiences using the attributes to take advantage of them in Target. 
For example, you might use customer data such as membership status (gold, silver, etc.), purchase history, favorite destination, local store, and so on in your CRM or eCommerce/POS system. Now you can upload that data to Marketing Cloud. After the user authenticates on your site, Target can match that data to their web behavior.
You could use Customer Attributes for the following use cases, for example:

* Membership level Understand which promotions and landing pages resonate best for platinum-level customers.

* Age and gender Identify which products and accessories do not appeal to male millennials and replace them with ones that do.

* Job function Determine how managers and senior managers are leveraging the new mobile app and which features are most popular.

* Propensity score Understand the pathing behaviors of visitors with high propensity scores who fail to convert.


For information about implementing Customer Attributes, refer to [Core Services - How to Enable Your Solutions](https://marketing.adobe.com/resources/help/en_US/mcloud/core_services.html). 
