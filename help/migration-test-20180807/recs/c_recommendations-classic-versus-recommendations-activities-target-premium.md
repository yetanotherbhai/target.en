---
description: Information to help you choose between Recommendations Classic and Recommendations activities in Target Premium.
keywords: Recommendations;recommendations algorithms;recommendations activity;recommendations classic
seo-description: Information to help you choose between Recommendations Classic and Recommendations activities in Target Premium.
seo-title: Recommendations Classic versus Recommendations Activities in Target Premium
solution: Target
title: Recommendations Classic versus Recommendations Activities in Target Premium
topic: Premium
uuid: b405d1e8-ee9d-4115-8efb-2d54f8ce77f8
index: y
internal: n
snippet: y
translate: y
---

# Recommendations Classic versus Recommendations Activities in Target Premium


>[!NOTE]
>
>Recommendations activities are available as part of the `Target Premium` solution. They are not available in `Target Standard` without a `Target Premium` license. 


In the classic `Recommendations` product, recommendations were displayed by creating a data collection mbox on a page, then adding a display mbox in a specific page location. The `Recommendations` activity in `Target Premium` allows you to collect visitor information and create your recommendations anywhere on the page without the need to create an mbox for each location where you want to recommend products or content. A simple JavaScript reference in the header of the page enables recommendations anywhere on the page. Use this JavaScript reference to pass keys to the global `Target` mbox, such as the `entity.id` and `entity.categoryId` keys. 
`Recommendations Classic` appears as its own card in the `Marketing Cloud` UI. A `Recommendations` activity is available from within the `Target Premium` workflow. 
`Recommendations Classic` users can continue to use their `Recommendations` mboxes in `Target Recommendations`. They can also combine the classic and `Target` approaches by keeping their mboxes and using the JavaScript code in the header to activate `Recommendations` functionality for the other elements on the page. To gain full `Target` functionality, however, `Recommendations Classic` users might prefer to delete their old mbox and rely solely on `Target Recommendations`. 
The `Recommendations` activity in `Target` improves on `Recommendations Classic` in the following main areas: 

## Criteria {#section_117709846DAA404580EBE879FFCBD9BA}

`Target Recommendations` includes a criteria library containing prepackaged sets of rules and configurations. In `Recommendations Classic`, each recommendation was built manually by filling out a form and choosing from the large list of rules. Now, when creating a `Recommendations` activity, you simply choose a pre-configured criteria set. You can still create custom recommendations, but the criteria library contains many of the most common configurations, pre-built to simplify the process, and using language that people understand. These prepackaged criteria can be used as is, or they can be copied and edited to fit your specific needs. 
![](graphics/overview_criteria.png) 
Criteria are pre-configured and sorted by industry verticals, page types, and implementation. For example, you can look for the criteria that apply to the retail vertical, for use on a product page, showing products from within a particular category (as defined by the `entity.categoryID` parameter). 
For more information about using and creating criteria, see [Criteria](c_algorithms.md#concept_4BD01DC437F543C0A13621C93A302750). 

## Workflow {#section_76B4A26297BF422382DE2C79A2713D3C}

The `Recommendations` workflow has been simplified. Instead of filling out complicated forms, you follow a visual workflow to: 

1. Select the criteria.

1. Select a pre-configured [design](c_design-overview.md#task_CC5BD28C364742218C1ACAF0D45E0E14). 

1. Preview the resulting recommendations.



## Visual Preview {#section_639B9E38C9EC4093BF9023EE0F2A15AC}

You can preview your recommendations after you set them up and make any necessary changes without having to create them on the page and then test them. Previews are available from within `Target`. 

## Targeting {#section_93295EA0DBA14210B8518AF4802A459F}

In `Recommendations Classic`, there were six targeting options. Recommendations activities use Target's full range of targeting options. Define an audience using either `Target` or other `Adobe Marketing Cloud` audiences (such as `Audience Manager` and `Analytics`), then select the percentage of activity entrants who see each design, and the percentages who see the control. 
![](graphics/overview_targeting.png) 

## Reporting {#section_25C2FCCE4BC1488496C517C0470B5CD6}

In `Target`, `Recommendations` provides improved reporting that takes advantage of the capabilities provided by `Target` and the `Marketing Cloud`. Rather than simply showing the lift provided by `Recommendations` compared to the results without them, you can view complete information about your `Recommendations` activity. 
![](graphics/overview_report.png) 
