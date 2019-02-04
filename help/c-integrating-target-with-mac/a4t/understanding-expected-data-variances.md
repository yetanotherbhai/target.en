---
description: Information about expected data variances between Target and Adobe Analytics when not using Analytics as the Reporting Source (A4T), which eliminates data variance altogether.
keywords: data variances;analytics;differences;variance;a4t;analytics for target;analytics as the reporting source;discrepancies;discrepancy
seo-description: Information about expected data variances between Target and Adobe Analytics when not using Analytics as the Reporting Source (A4T), which eliminates data variance altogether.
seo-title: Expected Data Variances When Not Using A4T
solution: Target
title: Expected Data Variances When Not Using A4T
topic: Advanced
uuid: 61bef460-8613-4251-b1b2-b6226ec86d9b
---

# Expected Data Variances between Target and Analytics when using and not using A4T{#expected-data-variances-when-not-using-a-t}

Information about expected data variances between [!DNL Target] and Adobe [!DNL Analytics] when using and *not* using Analytics as the Reporting Source (A4T), which eliminates data variance altogether.

## There is no expected data variance when using A4T

With A4T, both [!DNL Analytics] and [!DNL Target] reporting of activities use [!DNL Analytics] data exclusively, so there is no variance between the solutions in [!DNL Target] activity reports. In some circumstances, however, customers might compare [!DNL Target] data to [!DNL Analytics] data outside the scope of the A4T integration and, thus, experience the variance issues described below.

Here is a scenario in which you might experience expected data variance: Suppose you create an Auto-Allocate activity open to all visitors to a particular page. Because Auto-Allocate activities don't support A4T, all of the activity data is collected by [!DNL Target]. You might expect that the visitors to the activity in the [!DNL Target] reporting should match the visitors to that page in the [!DNL Analytics] reporting for the same date range. This is a scenario in which the variance described below is expected.

For a complete list of activity types that support A4T, see [Supported Activity Types](../../c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA).

## Expected data variance when *not* using A4T

Variances of 15-20% are normal, even with similar data sets. Systems that count differently can result in much higher data variances, as much as 35-50%. In some cases, variances can be even higher.

Although actual data can vary significantly, trends are usually consistent. As long as the differences and trends remain consistent, the data remains valuable and useful. If the differences and trends are inconsistent, it could mean that something is set up incorrectly. In this case, contact your account representative for assistance.

[!DNL Analytics] uses a system based on visits and transactions, but [!DNL Target] uses visitor-based metrics. That means that whenever a visitor opens a page, it counts as a visit in [!DNL Analytics], but [!DNL Target] does not count the visit until the conditions set in the activity are met.

Reports in [!DNL Target] show performance based on the conversion mbox selected when defining the activity, but this conversion mbox data is not sent to [!DNL Analytics], which has its own conversion variables as defined by your [!DNL Analytics] tagging implementation. In cases where you might expect identical data (for example, if a retailer's order confirm page contains both a conversion mbox and an [!DNL Analytics] purchase event), data might differ due to the placement of these tags. In general, trends in the two products' reports should be the similar.

Expected data variances can be caused by both technical and business variances.

### Examples of Technical Variances {#section_C3B50ED2E2F9416FAC91437CF1A87369}

The following can cause data variances based on technical differences:

* [!DNL Target] visitors must allow cookies and JavaScript 
* 1st- and 3rd-party cookies are processed differently; as a result, data from these cookie types do not match 
* Relative location of tags on pages and "leakage" caused by visitors who exit the page before it fully loads 
* Time zone considerations 
* Differences in which devices can be counted

### Examples of Business Variances {#section_2E1EB5E15BB64A1A80E4CDB1A5062AEE}

The following can cause data variances based on business differences:

* Differences between visitor and visit metrics 
* [!DNL Target]ing on activities excludes some visitors 
* A single mbox can be located on multiple pages, counting visitors on each of those pages 
* Activity priorities might include some visitors and exclude others on a page 
* Visitors who have converted once can be counted again when they re-enter the activity 
* [!DNL Analytics] counts all conversions for all visits and visitors, but [!DNL Target] only counts conversions for those visits and visitors that are included in the activity