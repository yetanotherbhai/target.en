---
description: Because of the different ways that Target and Analytics work, it is expected that data will vary between the two systems.
seo-description: Because of the different ways that Target and Analytics work, it is expected that data will vary between the two systems.
seo-title: Expected Data Variances (Deprecated)
solution: Target
title: Expected Data Variances (Deprecated)
topic: Advanced
uuid: 1af3d96a-5e1e-4c6c-9e56-44f7cb18556a
index: y
internal: n
snippet: y
translate: y
---

# Expected Data Variances (Deprecated)


|   ![](graphics/warning.jpg)  | As of April 17, 2014, the information in this section has been deprecated, and is replaced by the [ Adobe Analytics as the Reporting Source for Adobe Target ](http://marketing.adobe.com/resources/help/en_US/target/a4t/) functionality. Adobe is continuing to support the former integration methods, but it is recommended that you use the new functionality.  |
|---|---|


Variances of 15-20% are normal, even with similar data sets. Systems that count differently can result in much higher data variances, as much as 35-50%. In some cases, variances can be even higher.
Although actual data can vary significantly, trends are usually consistent. As long as the differences and trends remain consistent, the data remains valuable and useful. If the differences and trends are inconsistent, it could mean that something is set up incorrectly. In this case, contact your account representative for assistance.
Analytics uses a system based on visits and transactions, but Target uses visitor-based metrics. That means that whenever a visitor opens a page, it counts as a visit in Analytics, but Target does not count the visit until the conditions set in the campaign are met.
Reports in Target show performance based on the conversion mbox selected when defining the campaign, but this conversion mbox data is not sent to Analytics, which has its own conversion variables as defined by your Analytics tagging implementation. In cases where you may expect identical data (for example, if a retailer's order confirm page contains both a conversion mbox and an Analytics purchase event), data may differ due to the placement of these tags. In general, trends in the two products' reports should be the similar.
Expected data variances can be caused by both technical and business variances.
**Examples of Technical Variances** 
The following can cause data variances based on technical differences:

* Target visitors must allow cookies and JavaScript
* First- and third-party cookies are processed differently; as a result, data from these cookie types do not match.
* Relative location of tags on pages and "leakage" caused by visitors who exit the page before it fully loads
* Time zone considerations
* Differences in which devices can be counted

**Examples of Business Variances** 
The following can cause data variances based on business differences:

* Differences between visitor and visit metrics
* Targeting on campaigns excludes some visitors
* A single mbox can be located on multiple pages, counting visitors on each of those pages
* Campaign priorities might include some visitors and exclude others on a page
* Visitors who have converted once can be counted again when they re-enter the campaign
* Analytics counts all conversions for all visits and visitors, but Target only counts conversions for those visits and visitors that are included in the campaign

