---
description: Choose a success metric that qualifies the user for the reporting audience.
keywords: Targeting;audience;reporting;success metric
seo-description: Choose a success metric that qualifies the user for the reporting audience.
seo-title: Apply a Reporting Audience to a Success Metric
solution: Target
title: Apply a Reporting Audience to a Success Metric
uuid: 1deaf099-6ade-41de-ba05-b1a26f0658a7
index: y
internal: n
snippet: y
translate: y
---

# Apply a Reporting Audience to a Success Metric

For all activities, the `Applied At` drop-down list lets you apply an audience to a success metric so you can view reporting numbers after the metric has been reached and for subsequent actions. 
![](graphics/success metric.png) 
For example, suppose you have created an activity for all visitors entering from your home page and reaching the conversion page, but you also want to drill down more on visitors who have added more than $50 into the cart before converting.
The Applied At drop-down list potentially provides three categories: any visitors to the activity, only visitors who reach a certain step in the activity, or only visitors who reach conversion. Or, to phrase it another way, you can specify that a visitor must have reached an mbox on the entry page of the activity, an mbox that defines some point in the middle of the activity, or the conversion mbox at the end of the activity.
[Success metrics](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924) are available only if you have configured them for your activity. If you have not defined success metrics, you'll see only two options from the drop-down list: Campaign Entry and Conversion. 
Consider the following information when applying a reporting audience to a success metric:

* For actions before the action with the applied success metric, Target does not apply a segmented audience.

* For actions after the applied success metric, Target applies a segmented audience.


To view the segmentation in reporting, select the desired audience from the Audience drop-down list in the activity's report.
![](graphics/reporting audience dropdown.png) 
