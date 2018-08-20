---
description: For each experience, confidence level and confidence interval are displayed.
seo-description: For each experience, confidence level and confidence interval are displayed.
seo-title: Confidence Level and Confidence Interval
solution: Target
title: Confidence Level and Confidence Interval
topic: Recommendations
uuid: c21dceff-8ee3-481f-bbc0-6d99884115fc
index: y
internal: n
snippet: y
translate: y
---

# Confidence Level and Confidence Interval

**Confidence Level** 

The *confidence level* is represented by the filled-in bars in the confidence column for each experience. To see the exact confidence level percentage, hover your mouse over the confidence column for the experience. In the example below, the confidence level is four bars and 99.90%. 

The confidence level, or statistical significance indicates how likely it is that an experience's success was not due to chance. A higher confidence level indicates: 


* The experience is performing significantly different from control.
* The experience performance is not just due to noise.
* If you ran this test again, it is likely that you would see same results.


If the confidence level is over 90% or 95%, then the result can be considered statistically significant. Before making any business decisions, try to wait until your sample size is large enough and that the 4 bars of confidence on one or more experiences stays consistent for a continuous length of time to ensure the results are stable. 

The following list shows the meaning of the number of confidence bars: 


* One bar: significance &amp;lt; 60%
* Two bars: significance &amp;lt; 75%
* Three bars: significance &amp;lt; 90%
* Four bars: significance &amp;gt;= 90%


**Confidence Interval** 

The *confidence interval* is a range within which the true value can be found at a given confidence level. To view the confidence interval, rollover the "Lift" column of any experience. In the example above, the confidence interval for Experience B's lift is -10.15 to 68.82%. 

**Example:** An experience's RPV is $10, its confidence level is 95% and its **confidence interval** is $5 to $15. If we ran this test multiple times, 95% of the time the RPV would be between $5 and $15. 

**What impacts the confidence interval?** The formula follows standard statistical methods for calculating confidence intervals. 


* **Sample size:** As sample grows the interval will shrink or narrow. This is preferred as it means your reports are getting closer to the true value of the success metric.
* **Standard deviation smaller:** More similar results, such as similar AOVs or similar numbers or visitors converting each day, reduces the standard deviation.

>[!MORE_LIKE_THIS] {class="- topic/related-links "}* [ Viewing Test Results on a Recommendations Card ](c_Viewing_Test_Results_on_a_Recommendations_Card.md#concept_C035768E243F4382A5FF953E1BB870B1)* [ Viewing Complete Recommendation Results ](t_Viewing_Complete_Recommendation_Results.md#task_19A3022F3E2044CCA535F3CEC594300E)* [ Viewing the Optimizing Recommendation Report ](t_Viewing_the_Optimization_Recommendation_Report.md#task_55777B3740594D8489EF04E62D2327D8)* [ Viewing the Trended Graph Report ](t_Viewing_the_Trended_Graph_Report.md#task_1D399DB0E0A14BF5A672E99C6695BAE7)