---
description: The conversion rate, lift, confidence (statistical significance) and confidence interval are reported for each experience.
seo-description: The conversion rate, lift, confidence (statistical significance) and confidence interval are reported for each experience.
seo-title: Conversion Rate
solution: Target
title: Conversion Rate
topic: Advanced
uuid: 288c6be2-4675-418b-85ee-283a20b5ab16
index: y
internal: n
snippet: y
translate: y
---

# Conversion Rate


>[!NOTE] {class="- topic/note "}
>
>In all data, duplicate orders are ignored if an `orderID` is passed. The audit report lists the ignored duplicate orders. 



* **Conversion Rate** shows the median conversion rate, confidence, interval, and the number of conversions. For example, examine the following Conversion Rate report column:
  ![](../graphics/conversion_rate.png) 
  The first line is the control experience. It shows a 15% conversion rate, with three conversions. The second line, Experience B, shows a 15% conversion rate, with a confidence interval of plus or minus 15.65% and three conversions.

  >[!NOTE]
  >
  >Currently, the confidence interval is calculated only for binary metrics.


* **Lift** compares the conversion rate for each experience against the control experience. Lift = (Experience CR - Control CR) / Control CR
  If control is 0, there is no percentage lift.

* **Confidence (statistical significance)** This number represents the likelihood that the results would be duplicated if the test were run again. The confidence rounds up to 100.00% when the confidence is greater than or equal to 99.995%. See [Confidence Level and Confidence Interval](c_confidence_level_and_confidence_interval.md#concept_0D0002A1EBDF420E9C50E2A46F36629B). 

* **Retail Data** AOV, RPV and Sales data are displayed for each experience if you inserted a [Place Order](t_Creating_a_Place_Order_Mbox.md#task_0036D5F6C062442788BB55E872816D82) ( `orderConfirmPage`) mbox and selected it as the conversion mbox.

