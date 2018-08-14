---
description: A successful A/B test requires an adequate number of visitors. The Target Sample Size Calculator helps you determine the sample size needed for a successful test.
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content
seo-description: A successful A/B test requires an adequate number of visitors. The Target Sample Size Calculator helps you determine the sample size needed for a successful test.
seo-title: Plan an A/B Test
solution: Target
title: Plan an A/B Test
uuid: 549667e8-8cea-4077-b2f6-844f65b16f28
index: y
internal: n
snippet: y
translate: y
---

# Plan an A/B Test

This section contains the following information: 


* [ Access the Sample Size Calculator ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_286EB6E671184239BB1552F0387DAEB5)
* [ Overview ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)
* [ Statistical Significance ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_8230FB9C6D1241D8B1786B72B379C3CD)
* [ Statistical Power ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_1169C27F8E4643719D38FB9D6EBEB535)
* [ Minimum Reliably Detectable Lift ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_6101367EE9634C298410BBC2148E33A9)
* [ Baseline Conversion Rate ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_39380C9CA3C649B6BE6E1F8A06178B05)
* [ Estimating the Sample Size ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_19009F165505429E95291E6976E498DD)
* [ Revenue per Visit Metric ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_C704C0861C9B4641AB02E911648D2DC2)
* [ Correction for Comparing Multiple Offers ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_1474113764224D0B85472D8B023CCA15)
* [ Conclusion ](../../c_activities/t_test_ab/c_sample_size_determination.md#section_AEA2427B90AE4E9395C7FF4F9C5CA066)


## Access the Sample Size Calculator {#section_286EB6E671184239BB1552F0387DAEB5}

Access the Adobe Target [ sample size calculator ](https://docs.adobe.com/content/target-microsite/testcalculator.html) (https://docs.adobe.com/content/target-microsite/testcalculator.html). 

## Overview {#section_6B8725BD704C4AFE939EF2A6B6E834E6}

Before setting up your A/B test, use the sample size calculator (link provided above). 

It is important to determine an adequate sample size (number of visitors) prior to doing any A/B test, in order to establish the time that the test should be allowed to run before evaluating the results. Simply monitoring the test until statistical significance is achieved causes the confidence interval to be vastly underestimated, making the test unreliable. The intuition behind this result is that, in the event a statistically significant result is detected, the test is stopped and a winner is declared. However, if the result is not statistically significant the test is allowed to continue. This procedure strongly favors the positive outcome, which increases the false positive rate, and so distorts the effective significance level of the test. 

This can result in a large number of false positives, which leads to implementation of offers that do not deliver the predicted lift in the long run. Poor lift itself is a dissatisfying outcome, but an even more serious consequence is that over time the inability to accurately predict lift erodes organizational trust in testing as a practice. 

This article discusses the factors that must be balanced when a sample size is determined and introduces a spreadsheet calculator for estimating an adequate sample size. Calculating the sample size using the sample size calculator (link provided above) before any A/B test begins ensures that you always run high quality A/B tests that comply with statistical standards. 

There are five user-defined parameters that define an A/B test. These parameters are interlinked so when four of them are established, the fifth can be calculated: 


* Statistical significance
* Statistical power
* Minimum reliably detectable lift
* Baseline conversion rate
* Number of visitors


For an A/B test, the statistical significance, statistical power, minimum reliably detectable lift, and baseline conversion rate are set by the analyst and then the required number of visitors is calculated from these numbers. This article discusses these elements and gives guidelines for how to determine these for a specific test. 

![](assets/samplesize.png) 

The figure below illustrates the four possible outcomes of an A/B test: 

![](assets/outcomes.png) 

It is desirable to get no false positives or false negatives. However, this can never be guaranteed by a statistical test. It is always possible that observed trends are not representative of the underlying conversion rates. For example, in a test to see if heads or tails on a coin flip was more likely, even with a fair coin, you could get 10 heads on 10 tosses just by chance. The statistical significance and power help us quantify the false positive and false negative rates and allow us to keep them at reasonable levels for a given test. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Statistical Significance {#section_8230FB9C6D1241D8B1786B72B379C3CD}

The significance level of a test determines how likely it is that the test reports a significant difference in conversion rates between two different offers when in fact there is no real difference. This is known as a false positive or a Type I error. The significance level is a threshold specified by the user and is a trade-off between the tolerance for false positives and the number of visitors that have to be included in the test. 

In an A/B test, it is initially assumed that both offers have the same conversion rate. Then the probability of the observed outcome is computed based on this assumption. If this probability (the p-value) is smaller than some predefined threshold (the significance level) Target concludes that the initial assumption--that both offers have the same conversion rate--is incorrect and, therefore, the conversion rates of A and B are statistically different at the given significance level. 

A commonly used significance level in A/B testing is 5%, which corresponds to a confidence level of 95% (confidence level = 100% - significance level). A confidence level of 95% means that every time you do a test, there is a 5% chance of detecting a statistically significant lift even if there is no difference between the offers. 

Typical interpretations of the confidence level are summarized in the table below: 



<table id="table_DC424DC8BF4A406E88E6D8FE493772E0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Confidence Level </th> 
   <th colname="col2" class="entry"> Interpretation </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> &amp;lt; 90% </td> 
   <td colname="col2"> <p>No evidence that there is a difference between the conversion rates </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 90-95% </td> 
   <td colname="col2"> <p>Weak evidence that there is a difference between the conversion rates </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 95-99% </td> 
   <td colname="col2"> <p>Moderate evidence that there is a difference between the conversion rates </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 99-99.9% </td> 
   <td colname="col2"> <p>Strong evidence that there is a difference between the conversion rates </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> +99.9% </td> 
   <td colname="col2"> <p>Very strong evidence that there is a difference between the conversion rates </p> </td> 
  </tr> 
 </tbody> 
</table>

It is recommended to always using a confidence level of 95% or above. 

It is desirable to use the highest possible confidence level, so that the test will yield few false positives. However, a higher confidence level requires a larger number of visitors, which increases the time required to do the test. Furthermore, an increase in the confidence level causes a decrease in the statistical power. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Statistical Power {#section_1169C27F8E4643719D38FB9D6EBEB535}

The statistical power of an A/B test is the probability of detecting a real difference in conversion rate of a certain magnitude. Because of the random (stochastic) nature of conversion events it is possible that a statistically significant difference is not observed--just by chance--even though there is a real difference in conversion rate between the two offers. This is called a false negative or a Type II error. 

The statistical power is often ignored because the determination of statistical power, in contrast to statistical significance, is not required to do an A/B test. However, by ignoring the statistical power there is a substantial chance that real differences between the conversion rates of different offers will not be detected by the test because the sample size is too small. This results in the tests being dominated by false positives. 

It is desirable to have high statistical power so that the test has a high chance of identifying a real difference in conversion rates and yields fewer false negatives. However, a larger number of visitors is required to increase the statistical power of detecting any given lift, which increases the time required to do the test. 

A commonly used value for statistical power is 80%, which means that the test has an 80% chance of detecting a difference equal to the minimum reliably detectable lift. The test has a lower probability of detecting smaller lifts and a higher probability of detecting larger lifts. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Minimum Reliably Detectable Lift {#section_6101367EE9634C298410BBC2148E33A9}

Most organizations want to measure the smallest possible difference in conversion rate because even a small lift is worth implementing. However, if you want the A/B test to have a high probability of detecting a very small lift, the number of visitors that must be included in the test would be prohibitively large. The reason for this is that, if the difference in conversion rate is small, both conversion rates must be estimated with high accuracy to identify the difference, which requires a large number of visitors. Therefore, the minimum reliably detectable lift should be determined by the business requirements considering the trade-offs between detecting small lifts and running the test for longer periods of time. 

For example, suppose that two offers (A and B) have true conversion rates of 10% and 15%, respectively. If these offers are shown to 100 visitors each, there is a 95% chance of observing conversion rates in the range 4% to 16% for offer A and 8% to 22% for offer B due to the stochastic nature of conversions. These ranges are known as confidence intervals in statistics. They represent the confidence in the accuracy of the estimated conversion rates. The larger the sample size (more visitors) the more confident you can be that the estimates of the conversion rates are accurate. 

The figure below shows these probability distributions. 

![](assets/probability_distributions.png) 

Because of the large overlap between the two ranges, the test cannot determine whether the conversion rates are different. Therefore, this test with 100 visitors cannot distinguish between the two offers. However, if we expose the offers to 5,000 visitors each, then there is a 95% chance that the observed conversion rates will fall in the ranges of 9% to 11% and 14% to 16%, respectively. 

![](assets/probability_distributions2.png) 

In this case, it is very unlikely that the test will come to a wrong conclusion, so the test with 5,000 visitors can distinguish between the two offers. The test with 5,000 visitors has a confidence interval of approximately +/-1%. This means the test can detect differences of about 1%. Therefore, even more visitors would be needed if the true conversion rates of the offers were, for example, 10% and 10.5% instead of 10% and 15%. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Baseline Conversion Rate {#section_39380C9CA3C649B6BE6E1F8A06178B05}

The baseline conversion rate is the conversion rate of the control offer (offer A). Often, you have a good sense of the conversion level for the offer based on prior experience. If that is not the case, for example because it is a new type of offer or creative, the test can be allowed to run for a day or so to get a rough estimate of the baseline conversion rate that can be used in the sample size calculation. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Estimating the Sample Size {#section_19009F165505429E95291E6976E498DD}

It can be difficult to balance the opportunity costs of running a test for a long time with the risk of false positives and false negatives. Obviously, you do not want to make the wrong decisions, but being paralyzed by too strict or rigid testing standards is not desirable either. As a general guideline, a 95% confidence level and an 80% statistical power are recommended. 

The sample size calculator (link provided above) asks you to decide on the statistical significance (recommendation: 95%), and the statistical power (recommendation: 80%). After entering the baseline conversion rate and the daily traffic across all offers, the spreadsheet outputs the number of visitors required for detecting a lift of 1%, 2%, 5%, 10%, 15%, and 20% with a probability equal to the specified power of the test. The spreadsheet also allows the user to input a custom minimum reliably detectable lift. Furthermore, the spreadsheet outputs the number of weeks required for the test based on the traffic level entered by the user. The required number of weeks is rounded up to the nearest whole week in order to avoid day-of-week effects influencing the results. 

There is a trade-off between the minimum lift that can be reliably identified by the test and the required number of visitors. The figure below, which is valid for a baseline (control) conversion rate of 5%, shows strong diminishing returns for increasing the number of visitors. The minimum lift that can be reliably detected improves tremendously when adding the first few visitors to the test, but it takes an increasingly larger number of visitors to improve the test. The figure helps in finding an adequate tradeoff between the time required to run the test (as determined by the number of visitors required and the site traffic) and the minimum lift that can be reliably detected by the test. 

![](assets/samplesizecontrol.png) 

In this example, you might decide that being able to detect a lift of 5% (corresponding to a conversion rate of the alternative offer of (100%+5%)*5% = 5.25%) in 80 out of 100 tests is adequate, so you need a sample size of 100,000 visitors to each offer. If the site has 20,000 visitors per day and you are testing two offers, the test should be allowed to run for 2*100,000/20,000 = 10 days before it can be determined whether the alternative offer is statistically significantly superior to the control offer. Again, it is recommended that the required time always be rounded up to the nearest whole week, so day-of-week effects are avoided. Thus, in this example, the test would be run for two weeks before evaluating the results. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Revenue per Visit Metric {#section_C704C0861C9B4641AB02E911648D2DC2}

When using Revenue per Visit (RPV) as a metric, an additional source of variance is added because RPV is the product of revenue per order and conversion rate (RPV = Revenue / #visitors = (Revenue per order * #orders) / # visitors = Revenue per order * (#visitors * CTR) / #visitors = Revenue per Order * CTR), each with its own variance. The variance of the conversion rate can be estimated directly using a mathematical model but the variance of revenue per order is specific to the campaign. Therefore, use knowledge of this variance from past campaigns or run the A/B test for a few days to estimate the variance in revenue. The variance is calculated from the values of Sum of Sales, Sum of Sales Squared, and Number of visitors that are found in the CSV download file. Once this is established, use the spreadsheet to calculate the required time to complete the test. 

The sample size calculator (link provided above) can help you configure the RPV metric. When you open the calculator, you'll see a tab labeled RPV Metric. You'll need the following information when using the RPV version of the calculator: 




* Number of visitors to the control offer
* Total revenue for the control offer Make sure the extreme order filter is checked. 

* The sum of squares revenue for the control offer Make sure the extreme order filter is checked. 



In general, using RPV as a metric requires 20-30% longer to achieve the same level of statistical confidence for the same level of measured lift, because RPV has the added variance of different order sizes per conversion. That should be a consideration when choosing between straight conversion rate and RPV as the metric on which to base your final business decision. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Correction for Comparing Multiple Offers {#section_1474113764224D0B85472D8B023CCA15}

Each time you compare two offers the chance of getting a false positive (observing a statistically significant difference even when there is no difference in conversion rate) is equal to the significance level. For example, if five offers are present, A/B/C/D/E, and A is the control offer, then four comparisons are done (control to B, control to C, control to D, and control to E), and the probability of a false positive is 18.5% even when the confidence level is 95% because Pr(at least one false positive) = 1 - Pr(no false positives) = 1 - 0.95 = 18.5%. A false positive is in this context defined as either the control being reported to be better than the alternative or the alternative being reported to be better than the control when, in fact, there is no difference between them. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Conclusion {#section_AEA2427B90AE4E9395C7FF4F9C5CA066}

By using the sample size calculator (link provided above) introduced in this article and allowing the test to run for the amount of time suggested by it, you can ensure that you are always doing high quality A/B tests that adhere to the false positive and false negative rates you have decided are adequate for the specific test. This ensures that your tests are consistent and able to reliably detect the lift you are looking for. 

[ Top ](../../c_activities/t_test_ab/c_sample_size_determination.md#concept_2801F552DB874C20B8A17C1B774C0383) 
