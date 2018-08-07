---
description: A/B Testing compares two or more versions of your Web site content to see which version best improves your conversions during a pre-specified test period.
keywords: AB;A/B;AB...n;mistakes;pitfalls;mistake;pitfall
seo-description: A/B Testing compares two or more versions of your Web site content to see which version best improves your conversions during a pre-specified test period.
seo-title: A/B Test
solution: Target
title: A/B Test
topic: Standard
uuid: cb024202-c0ef-429f-ba15-1f682593354e
index: y
internal: n
snippet: y
translate: y
---

# A/B Test

## A/B Test {#task_05E33EB15C4D4459B5EAFF90A94A7977}A/B Testing compares two or more versions of your Web site content to see which version best improves your conversions during a pre-specified test period.An A/B test (sometimes referred to as an A/B...N test) compares two or more versions of your Web site content to see which best lifts your conversions, sales, or other metrics you identify. Use an A/B test to compare changes to your page against your default page design to determine which experience produces the best results.
A/B tests are particularly useful when you have a clear hypothesis of ways to improve your page performance based on success metrics or alternative content delivery.
A/B tests are well-suited for large changes that might involve new layouts or drastically different treatments of the elements. If your test design does not easily break down into individual page elements, you should run an A/B test before a multivariate test.
When you set up your test, you can determine what percentage of visitors see each experience. For example, you might split traffic evenly between the control and a second experience, or you might test out a new, more risky experience by showing it to only 5% of your audience.

>[!NOTE]
>
>For detailed information about determining the optimum sample size for an A/B test, see[ Plan Your A/B Test ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383). 


When the number of different experiences exceeds five and span two or more locations, it's a good idea to consider an [ MVT test ](https://marketing.adobe.com/resources/help/en_US/target/mvt/) before running your A/B tests. The multivariate test shows which areas on the page are most likely to improve conversion. These are the locations that a marketer should focus on. For example, the MVT test might show that the call to action is the most important location for meeting your goals. Once you have determine which locations and content are most useful for helping you meet your goals, you can run an A/B test to further refine the results, such as to test two specific images against each other, or comparing the wording or colors of a call to action. By following an MVT test with one or more A/B tests, you can determine the best possible content for the results you desire. 
This video explains the activity types available in Target Standard/Premium. A/B testing is discussed beginning at 3:30.


<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Types </th> 
   <th colname="col3" class="entry"> 9:03 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/vtHg1pPFJp8/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/vtHg1pPFJp8/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F">Describe the types of activities included in Adobe Target</li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Select the appropriate activity type to achieve your goals</li> 
      <li id="li_6C4D1871E45D40118D7D9D4DF81547B5">Describe the three-step guided workflow that applies to all activity types</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Plan an A/B Test {#concept_2801F552DB874C20B8A17C1B774C0383}<!--Jonas Dahl and John Kucera-->A successful A/B test requires an adequate number of visitors. The Target Sample Size Calculator helps you determine the sample size needed for a successful test. 
<draft-comment otherprops="merge">
  target/c_sample_size_determination.xml 
</draft-comment>
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
![](../graphics/samplesize.png) 
The figure below illustrates the four possible outcomes of an A/B test:
![](../graphics/outcomes.png) 
It is desirable to get no false positives or false negatives. However, this can never be guaranteed by a statistical test. It is always possible that observed trends are not representative of the underlying conversion rates. For example, in a test to see if heads or tails on a coin flip was more likely, even with a fair coin, you could get 10 heads on 10 tosses just by chance. The statistical significance and power help us quantify the false positive and false negative rates and allow us to keep them at reasonable levels for a given test.
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 

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
   <td colname="col1"> &lt; 90% </td> 
   <td colname="col2"> <p>No evidence that there is a difference between the conversion rates</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 90-95% </td> 
   <td colname="col2"> <p>Weak evidence that there is a difference between the conversion rates</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 95-99% </td> 
   <td colname="col2"> <p>Moderate evidence that there is a difference between the conversion rates</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 99-99.9% </td> 
   <td colname="col2"> <p>Strong evidence that there is a difference between the conversion rates</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> +99.9% </td> 
   <td colname="col2"> <p>Very strong evidence that there is a difference between the conversion rates</p> </td> 
  </tr> 
 </tbody> 
</table>

It is recommended to always using a confidence level of 95% or above.
It is desirable to use the highest possible confidence level, so that the test will yield few false positives. However, a higher confidence level requires a larger number of visitors, which increases the time required to do the test. Furthermore, an increase in the confidence level causes a decrease in the statistical power.
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Statistical Power {#section_1169C27F8E4643719D38FB9D6EBEB535}

The statistical power of an A/B test is the probability of detecting a real difference in conversion rate of a certain magnitude. Because of the random (stochastic) nature of conversion events it is possible that a statistically significant difference is not observed--just by chance--even though there is a real difference in conversion rate between the two offers. This is called a false negative or a Type II error.
The statistical power is often ignored because the determination of statistical power, in contrast to statistical significance, is not required to do an A/B test. However, by ignoring the statistical power there is a substantial chance that real differences between the conversion rates of different offers will not be detected by the test because the sample size is too small. This results in the tests being dominated by false positives.
It is desirable to have high statistical power so that the test has a high chance of identifying a real difference in conversion rates and yields fewer false negatives. However, a larger number of visitors is required to increase the statistical power of detecting any given lift, which increases the time required to do the test.
A commonly used value for statistical power is 80%, which means that the test has an 80% chance of detecting a difference equal to the minimum reliably detectable lift. The test has a lower probability of detecting smaller lifts and a higher probability of detecting larger lifts.
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Minimum Reliably Detectable Lift {#section_6101367EE9634C298410BBC2148E33A9}

Most organizations want to measure the smallest possible difference in conversion rate because even a small lift is worth implementing. However, if you want the A/B test to have a high probability of detecting a very small lift, the number of visitors that must be included in the test would be prohibitively large. The reason for this is that, if the difference in conversion rate is small, both conversion rates must be estimated with high accuracy to identify the difference, which requires a large number of visitors. Therefore, the minimum reliably detectable lift should be determined by the business requirements considering the trade-offs between detecting small lifts and running the test for longer periods of time.
For example, suppose that two offers (A and B) have true conversion rates of 10% and 15%, respectively. If these offers are shown to 100 visitors each, there is a 95% chance of observing conversion rates in the range 4% to 16% for offer A and 8% to 22% for offer B due to the stochastic nature of conversions. These ranges are known as confidence intervals in statistics. They represent the confidence in the accuracy of the estimated conversion rates. The larger the sample size (more visitors) the more confident you can be that the estimates of the conversion rates are accurate.
The figure below shows these probability distributions.
![](../graphics/probability_distributions.png) 
Because of the large overlap between the two ranges, the test cannot determine whether the conversion rates are different. Therefore, this test with 100 visitors cannot distinguish between the two offers. However, if we expose the offers to 5,000 visitors each, then there is a 95% chance that the observed conversion rates will fall in the ranges of 9% to 11% and 14% to 16%, respectively.
![](../graphics/probability_distributions2.png) 
In this case, it is very unlikely that the test will come to a wrong conclusion, so the test with 5,000 visitors can distinguish between the two offers. The test with 5,000 visitors has a confidence interval of approximately +/-1%. This means the test can detect differences of about 1%. Therefore, even more visitors would be needed if the true conversion rates of the offers were, for example, 10% and 10.5% instead of 10% and 15%.
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Baseline Conversion Rate {#section_39380C9CA3C649B6BE6E1F8A06178B05}

The baseline conversion rate is the conversion rate of the control offer (offer A). Often, you have a good sense of the conversion level for the offer based on prior experience. If that is not the case, for example because it is a new type of offer or creative, the test can be allowed to run for a day or so to get a rough estimate of the baseline conversion rate that can be used in the sample size calculation.
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Estimating the Sample Size {#section_19009F165505429E95291E6976E498DD}

It can be difficult to balance the opportunity costs of running a test for a long time with the risk of false positives and false negatives. Obviously, you do not want to make the wrong decisions, but being paralyzed by too strict or rigid testing standards is not desirable either. As a general guideline, a 95% confidence level and an 80% statistical power are recommended.
The sample size calculator (link provided above) asks you to decide on the statistical significance (recommendation: 95%), and the statistical power (recommendation: 80%). After entering the baseline conversion rate and the daily traffic across all offers, the spreadsheet outputs the number of visitors required for detecting a lift of 1%, 2%, 5%, 10%, 15%, and 20% with a probability equal to the specified power of the test. The spreadsheet also allows the user to input a custom minimum reliably detectable lift. Furthermore, the spreadsheet outputs the number of weeks required for the test based on the traffic level entered by the user. The required number of weeks is rounded up to the nearest whole week in order to avoid day-of-week effects influencing the results.
There is a trade-off between the minimum lift that can be reliably identified by the test and the required number of visitors. The figure below, which is valid for a baseline (control) conversion rate of 5%, shows strong diminishing returns for increasing the number of visitors. The minimum lift that can be reliably detected improves tremendously when adding the first few visitors to the test, but it takes an increasingly larger number of visitors to improve the test. The figure helps in finding an adequate tradeoff between the time required to run the test (as determined by the number of visitors required and the site traffic) and the minimum lift that can be reliably detected by the test.
![](../graphics/samplesizecontrol.png) 
In this example, you might decide that being able to detect a lift of 5% (corresponding to a conversion rate of the alternative offer of (100%+5%)*5% = 5.25%) in 80 out of 100 tests is adequate, so you need a sample size of 100,000 visitors to each offer. If the site has 20,000 visitors per day and you are testing two offers, the test should be allowed to run for 2*100,000/20,000 = 10 days before it can be determined whether the alternative offer is statistically significantly superior to the control offer. Again, it is recommended that the required time always be rounded up to the nearest whole week, so day-of-week effects are avoided. Thus, in this example, the test would be run for two weeks before evaluating the results.
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Revenue per Visit Metric {#section_C704C0861C9B4641AB02E911648D2DC2}

When using Revenue per Visit (RPV) as a metric, an additional source of variance is added because RPV is the product of revenue per order and conversion rate (RPV = Revenue / #visitors = (Revenue per order * #orders) / # visitors = Revenue per order * (#visitors * CTR) / #visitors = Revenue per Order * CTR), each with its own variance. The variance of the conversion rate can be estimated directly using a mathematical model but the variance of revenue per order is specific to the campaign. Therefore, use knowledge of this variance from past campaigns or run the A/B test for a few days to estimate the variance in revenue. The variance is calculated from the values of Sum of Sales, Sum of Sales Squared, and Number of visitors that are found in the CSV download file. Once this is established, use the spreadsheet to calculate the required time to complete the test.
The sample size calculator (link provided above) can help you configure the RPV metric. When you open the calculator, you'll see a tab labeled RPV Metric. You'll need the following information when using the RPV version of the calculator:


* Number of visitors to the control offer
* Total revenue for the control offer Make sure the extreme order filter is checked.

* The sum of squares revenue for the control offer Make sure the extreme order filter is checked.


In general, using RPV as a metric requires 20-30% longer to achieve the same level of statistical confidence for the same level of measured lift, because RPV has the added variance of different order sizes per conversion. That should be a consideration when choosing between straight conversion rate and RPV as the metric on which to base your final business decision.
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Correction for Comparing Multiple Offers {#section_1474113764224D0B85472D8B023CCA15}

Each time you compare two offers the chance of getting a false positive (observing a statistically significant difference even when there is no difference in conversion rate) is equal to the significance level. For example, if five offers are present, A/B/C/D/E, and A is the control offer, then four comparisons are done (control to B, control to C, control to D, and control to E), and the probability of a false positive is 18.5% even when the confidence level is 95% because Pr(at least one false positive) = 1 - Pr(no false positives) = 1 - 0.95 = 18.5%. A false positive is in this context defined as either the control being reported to be better than the alternative or the alternative being reported to be better than the control when, in fact, there is no difference between them. 
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 

## Conclusion {#section_AEA2427B90AE4E9395C7FF4F9C5CA066}

By using the [ sample size calculator ](http://adobe-target.com/testcalculator.html) introduced in this article and allowing the test to run for the amount of time suggested by it, you can ensure that you are always doing high quality A/B tests that adhere to the false positive and false negative rates you have decided are adequate for the specific test. This ensures that your tests are consistent and able to reliably detect the lift you are looking for. 
[ Top ](t_test_ab.md#concept_2801F552DB874C20B8A17C1B774C0383) 
>## Create an A/B Test {#task_68C8079BF9FF4625A3BD6680D554BB72}Use the 
<wintitle>
  Visual Experience Composer 
</wintitle> in 
<keyword>
  Target 
</keyword> to create your test directly on a Target-enabled page and to modify portions of the page within 
<keyword>
  Target 
</keyword>. 
<draft-comment otherprops="merge">
  target/t_test_create_ab.xml 
</draft-comment>This video demonstrates how to create an A/B test using the ` Target` three-step guided workflow. 


<table id="table_411C4C930FD944ABA1B78F8480CCB636"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating A/B Tests </th> 
   <th colname="col3" class="entry"> 8:36 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/JG0dbWDAvtk/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/JG0dbWDAvtk/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B2DF3BCF8AD6456FA85AF4AE98881076"> 
      <li id="li_8596E7B7C6F94D2BB8A001C28BCCC1A7">Create an A/B activity in Adobe Target</li> 
      <li id="li_FB164278D49A4D0AB6C663B17DBE7876">Allocate traffic using a manual split or automatic traffic allocation</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**To Create an A/B test:** 

>1. From the ` Activities` list, click ** ` Create Activity` ** > ** ` A/B Test` **.

>       ![](../graphics/ab_select.png) 

>       >[!NOTE]
>       >
>       >The available activity types depend on your ` Target` account. Some activity types might not appear in your list. 

>       For information about the various activity types, see [ Activities ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). 
>       ![](../graphics/ab_newactivityurl.png) 
>1. Select ** ` Visual Experience Composer` **, if necessary.

>       For troubleshooting information about the VEC, should you have problems, see [ Troubleshooting the Visual Experience Composer ](vec-best-pracitces-and-troubleshooting.md#reference_77743144F10143A3A89D56E116D296E4). 
>       If you prefer to use the Form-Based Experience Composer, select that option. See [ Form-Based Experience Composer ](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html). 
>1. Specify your [ activity URL ](t_test_ab.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), then click ** ` Create` **.

>       If your account is configured with a default URL, that URL appears by default. You can change from the default to another URL.
>       The ` Visual Experience Composer` opens, showing the page specified in the URL. 
>       ![](../graphics/vec.png) 
>1. Type a name for the activity in the space provided.

>       ![](../graphics/ab_newname.png) 
>       The following characters are not allowed in an activity name:


>       |  Character  | Description  |
>       |---|---|
>       |  /  | Forward slash  |
>       |  ?  | Question mark  |
>       |  #  | Number sign  |
>       |  :  | Colon  |

>1. Create any new experiences by changing the elements on the page.
>   The ` Visual Experience Composer` displays two tabs on the left side after you create a new activity: Experience A and Experience B. Experience A is the control experience. Your focus will be on the Experience B tab, which you can modify as desired. Experience B is the alternate experience you can add to your test. You can add multiple experiences to the test. You can also delete Experience A from the activity if you don't want to include a default site experience as an option. 
>   For more information about adding and modifying experiences in the ` Visual Experience Composer`, see [ Add Experience ](t_test_ab.md#task_454646F2895242D3B92DC395A0CE1A00). To modify Experience B, start with Step 3. 
>
>1. Click ** ` Target` ** at the top of the ` Visual Experience Composer` to move to the next step in the three-step guided workflow.

>       The flow diagram opens.
>       ![](../graphics/ab_flow.png) 
>       The flow diagram leads you through the steps of choosing the audience for the activity and setting up experiences.
>1. In the ` Audience` box, click the edit icon (  ![](graphics/icon_edit.png) ), then [ select the audience ](t_test_ab.md#concept_A268236C1224451DB7844BF67F41A087) for your activity.

>1. Choose the percentage of qualifying visitors that you want to enter the activity.

>       ![](../graphics/audperc.png) 
>       For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience.
>1. Set up your traffic allocation.

>       You can show multiple experiences to the same audience. A diagram displays showing your selected audience and the experiences you've added to the activity.
>       If you select ** ` Manual` **, specify the percentage of entrants you want to see each experience. You can split the percentages evenly between all experiences, or specify higher or lower percentages for each experience. The total for all experiences must equal 100%. 
>       If you select ** ` Auto-allocate to best experience` **, most activity entrants are automatically directed to higher-performing experiences. Some visitors are allocated to all experiences, to maintain exploration of experiences and to recognize changes in performance trends. See [ Automated Traffic Allocation ](automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4). 
>       **First Look:**If you select ** ` Auto-target to optimize` **, Target uses advanced machine learning algorithms to automatically target visitors with the best experience to maximize your goals. 

>       >[!NOTE]
>       >
>       >This "First Look" offering is enabled for a few customers in this release for testing and feedback.

>       For more information, see [ Auto-Target to Optimize ](c_auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3). 
>       You can also click ** ` Add Experience` ** to add another experience to the activity. 
>1. When you are satisfied with your audience and experience choices, click ** ` Next` ** to move to the third step of the three-step guided workflow.
>1. Specify the [ goals and settings ](t_test_ab.md#reference_B25389FD6F3A4989801E740364B089CC) for the activity.

>       ![](../graphics/ab_settings.png) 
>1. Click ** ` Save` **.
>## Activity URL {#concept_D28549AAA0A14E3BB5F05F32BE8ABC90}The 
<wintitle>
  Activity URL 
</wintitle> determines the page that is used in the test and that opens when the test is designed. 
<draft-comment otherprops="merge">
  target/c_ab_activity_url.xml 
</draft-comment>When prompted during activity creation, specify the activity URL. Type the complete URL (including ` http://`), then click ** ` Create` **. 

>[!NOTE]
>
>` Target` does not differentiate between URL protocols ( ` https` and ` http`). As a result, ` https://adobe.com` and ` http://adobe.com` both match. 


By default, the ` Visual Experience Composer` opens the page that is specified in your [ Account Preferences ](https://marketing.adobe.com/resources/help/en_US/target/target/t_account_preferences.html). You can specify a different page during activity creation. 
To display a different page after the ` Visual Experience Composer` opens, click the ** ` Configure` ** gear icon, then select ** ` URL` **. Enter the URL in the Activity URL field. 
![](../graphics/url-config.png) 
Click ** ` Add Template Rule` ** to add more pages or sections to the activity. 
Additional rules can be based on any of the following:

* URL
* Domain
* Path
* Hash (#) Fragment
* Query
* mbox Parameter

Additional rules can be joined to the Activity URL with AND or OR. All rules you add are evaluated against each other with AND.
Click ** ` Save` ** when you have finished. 

<a id="section_373CAB401E6A43EFA4D82E000581A4D3"></a>


>[!NOTE]
>
>If you entered a URL for a site that does not include the ` Target` Standard JavaScript code, you cannot select page elements. 


By default, the ` Visual Experience Composer` does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off ** ` Render using JavaScript` ** if you want to be able to alter those elements using the ` Visual Experience Composer`. 

>[!NOTE]
>
>If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.


>## Add Experience {#task_454646F2895242D3B92DC395A0CE1A00}The 
<wintitle>
  Visual Experience Composer 
</wintitle> provides a visual interface for editing the experiences on your page. 
<draft-comment otherprops="merge">
  target/t_ab_add_experience.xml 
</draft-comment>For additional detail about experiences, see [ Experiences ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

>1. Click ** ` Add Experience` **.


>       >[!NOTE]
>       >
>       >If you are targeting an experience to an audience, you must select the audience before you can add an experience. A message appears to remind you to choose your audience.

>1. When prompted, enter the activity URL. Type the complete URL (including ` http://`), then click ** ` Continue` **.

>       The Experience Composer (see [ Experiences ](c_experiences.md#concept_1D011219034B492BB03C08B3BB80E3F0)) opens the page that is specified in your [ Account Preferences ](https://marketing.adobe.com/resources/help/en_US/target/target/t_account_preferences.html). To display a different page, click the Globe icon and enter the URL in the Select URL box in the Experience Composer and click ** ` Continue` **. If you entered a URL for a site that does not include the Target Standard JavaScript code, you cannot select page elements. 
>       By default, the Visual Experience Composer does not allow changes to elements containing JavaScript, such as rotating banners. You can select to disable JavaScript if you want to be able to alter those elements using the Visual Experience Composer.

>       >[!NOTE]
>       >
>       >If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.

>1. Select the elements you want to change and make the desired changes.

>       As you hover the elements on your page, the elements are highlighted. Any highlighted element can be altered using the Experience Composer.
>       The video below provides information about using the Visual Experience Composer options.


>    <table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Visual Experience Composer (1 of 2) </th> 
   <th colname="col3" class="entry"> 7:17 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/2KUDgu6Mscg/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/2KUDgu6Mscg/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Change the content of a page</li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Change the layout of a page</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>       If you created an mbox on the page using Target Classic (formerly Test&amp;Target), that mbox appears as an element that shows the mbox name, and can be modified like any other element.
>       The following actions can be performed on an element on the displayed page to change the experience:


>    <table id="table_B146BECBBF554EEA8BA6F72C09CCE73F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Option </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Edit Text/HTML </td> 
   <td colname="col2"> <p>Change the HTML code for the element, such as the text for a text area, button, or link.</p> <p>In addition to HTML code, you can edit and inject custom JavaScript.</p> <p>Several rich text formatting options are available when editing text and HTML for A/B and Experience Targeting activities. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Edit Background Color</p> </td> 
   <td colname="col2"> <p>Use the color picker to select or configure a background color. You can select a color swatch, and adjust it using RGB values or color hex codes. The red x in the color picker makes the background transparent.</p> <p> <p>Note:  This option is not available for an element where a background image is set. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Insert Element </td> 
   <td colname="col2"> <p>Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.</p> <p>Select an element on the page, then click <span class="uicontrol"> Insert Element </span> and choose whether you want to insert an image, HTML, or text. The inserted element appears after the selected element. </p> <p>The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.</p> <p> <p>Note:  Inserting an image requires that Adobe Scene7 Publishing System is enabled so you have access to the image library. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Edit Link </td> 
   <td colname="col2"> <p>Change the URL in the link.</p> <p>Use <span class="uicontrol"> Edit Link </span> to update the selector to point to the same image element. However, linking to a different image element is not supported. To link to a different image element, delete the original action from the code editor and use the <span class="wintitle"> Visual Experience Composer </span> to apply the action on the other image element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Edit CSS Class </td> 
   <td colname="col2"> <p>Specify the predefined CSS class used for the element. If more than one element is selected, separate multiple CSS classes with a space.</p> <p>Available for A/B, Automated Personalization, and Multivariate test activities.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Swap Offer </td> 
   <td colname="col2"> <p>Select a different offer from the Content Library.</p> <p> <p>Note:  HTML Offers are stored on Target servers. </p> </p> <p>An HTML offer can be up to 256KB in size.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Swap Image </td> 
   <td colname="col2"> <p>Select a different image from the Content Library. The images available for swapping include the images uploaded to the Marketing Cloud assets folder or uploaded in the Content Library in Target.</p> <p>During initial activity creation, the URL displayed is not the URL used for delivery. Upon activity synching, that URL is updated to a production Scene7 URL.</p> <p>For example, the initial URL might look like the following example:</p> <p> 
     <codeblock>
       https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867 
     </codeblock> </p> <p>After activity syncing, the delivery URL might look like the following example:</p> <p> 
     <codeblock>
       http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&amp;fit=constrain&amp;hei=173&amp;wid=300 
     </codeblock> </p> <p> <p>Note:  Swapping images requires an Adobe Scene7 Publishing System account. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Remove Item </td> 
   <td colname="col2"> <p>Remove the element. The white space behind the image is removed and the space where the element was is collapsed.</p> <p> <p>Note:  Items within a "classic" mbox (an mbox created within a <span class="keyword"> Target Classic </span> campaign) cannot be removed using this option. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hide Item </td> 
   <td colname="col2"> <p>Hide the element. The white space remains, but the content is removed.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rearrange </td> 
   <td colname="col2"> <p>Drag the element to another location inside the same parent element or <span class="filepath"> &lt;div&gt; </span>. Other elements shift location to make space for the rearranged element. </p> <p> <p>Note:  Click tracking does not work on rearranged items. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Move </td> 
   <td colname="col2"> <p>Move elements on your page. Unlike the <span class="wintitle"> Rearrange </span> option, <span class="wintitle"> Move </span> does not shift other elements to make room for the element being moved. Use the arrow keys to fine tune the move. (Planned enhancement: support for making sure moved elements are not hidden behind other elements.) </p> <p>In some cases, such as when a CSS restriction requires an element to remain inside its parent element, you cannot move the element outside its parent.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Resize </td> 
   <td colname="col2"> <p>Resize an element on your page. When you select <span class="uicontrol"> Resize </span>, a handle appears in the bottom right corner of the element that lets you drag that corner to resize. Hold the Shift key to retain the same aspect ratio. </p> <p> <p>Note:  Inline elements cannot be resized. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Expand Selection </td> 
   <td colname="col2"> <p>Select the parent element in addition to the originally selected element. When you select any parent element, all children of that element are automatically selected. You can expand the selection multiple times.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Navigate to this Link </td> 
   <td colname="col2"> <p>Open the destination of the link.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Undo/Redo </td> 
   <td colname="col2"> <p>Undo changes you make to your activities during an editing session. You can also redo changes that have been previously undone.</p> </td> 
  </tr> 
 </tbody> 
</table>


>       >[!NOTE]
>       >
>       >If you deliver an image from a source other than your main page (such as an image hosted on akamai.net and delivered on dell.com), then that image does not display in the thumbnail of the page shown in the flow diagram.

>1. Click the Check Mark button when you are finished designing the experience.

>       The activity diagram displays:
>       ![](../graphics/ab_flodia.png) 
>       If an experience includes cross-domain content, the thumbnail might not display accurately and is replaced by an icon.
>1. Specify the percentage of visitors who will see each experience in the activity.

>       You can show multiple experiences to the same audience. A diagram displays showing your selected audience and the experiences you've added to the activity. Specify the percentage of times you want each experience to be shown. You can split the percentages evenly between all experiences, or specify higher or lower percentages for each experience. The total for all experiences must equal 100%. You can also click ** ` Add Experience` ** to add another experience to the activity. 
>       Click ** ` Continue` ** when you are finished with this step. 
>## Select Audience {#concept_A268236C1224451DB7844BF67F41A087}The audience determines which site visitors are entered into your activity. 
<draft-comment otherprops="merge">
  target/c_ab_audience.xml 
</draft-comment>
>[!NOTE]
>
>In addition to selecting an existing audience, you can combine multiple audiences to create ad hoc combined audiences rather than creating a new audience. For more information, see[ Combining Multiple Audiences ](c_audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5). 


This video includes information about using audiences.

<table id="table_E4F516D8E7E142D69D9216EE54B996EF"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Using Audiences </th> 
   <th colname="col3" class="entry"> 6:22 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/TAMBpW9vpOI/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/TAMBpW9vpOI/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_F52B83BBBED445B0B95041661DE3274B"> 
      <li id="li_6CB2FEACFDD94B279160E7280DAFDECE">Explain the term "audience"</li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405">Explain the two ways audiences are used for optimization</li> 
      <li id="li_DFCEC529C47F4D78AE32A6F1FB0C4EFD">Find audiences in the Audiences List</li> 
      <li id="li_699D4D5D089A4FB7BA4C5E95337AC34A">Target an activity to an audience</li> 
      <li id="li_87E7AFFEEC9C42ABB51C279221E17A14">Use audiences for passive reporting in an activity</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

In the ` Audience` box, click the Edit icon (  ![](../graphics/icon_more_options.png) ), then click ** ` Replace Audience` **. 
By default, all visitors are your audience. However, you can change the audience. Audiences are selected from the audience library or you can create an activity-only audience. The audience library contains audiences that have previously been defined, including some common audiences that are pre-built as a part of Target. You can either select an audience from the library, [ create a new audience ](c_audiences.md#task_1D507519D3AD4390B507F188BD294DC1), or [ create an activity-only audience ](c_audiences.md#concept_A6BADCF530ED4AE1852E677FEBE68483). For an A/B test without specific audience targeting, choose the default, All Visitors. 
Note that you can also edit or copy an audience by hovering over the desired audience in the ` Choose Audience` dialog box, as shown below. Copying an audience is helpful if you want to create a similar audience to an existing audience. You can make a copy of the audience, make your edits, then save it as a new audience. This hover functionality exists in other activity types as well. 
![](../graphics/audience picker hover.png) 
When creating an audience, you can select a location (mbox) and specify parameters for that location. Under Custom Parameters, select the mbox, then specify the desired parameters.

>[!NOTE]
>
>Audiences are automatically imported in the background when you open the audience list and the imported audiences are more than 10 minutes old.


Click the down arrow to remove the existing audience or change the audience.
You can specify the percentage of qualifying visitors to include in the activity. For example, you might choose to include 50% of all visitors.
![](../graphics/audperc.png) 
You can also choose to let Target [ allocate traffic automatically ](automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4). 
This video includes information about setting up audiences.

<table id="table_DCFB43FDA2794B0C97054C6E907AD5D9"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Workflow - Targeting </th> 
   <th colname="col3" class="entry"> 2:14 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/LOmBgKPeBtA/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/LOmBgKPeBtA/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_4541DFF59E2A44788839B0EDEFC985AC"> 
      <li id="li_ADAEEAC4A85F42599FA4D4111B68C498">Assign an audience to your activity</li> 
      <li id="li_B0FFB33A346243089DFB41618F4F0D1C">Throttle traffic up or down</li> 
      <li id="li_CC325839811844A097187835B22000A9">Select your traffic allocation method</li> 
      <li id="li_EEE7ADB8CB09442C8D21C5EA1598C206">allocate traffic between different experiences</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

For detailed information, see [ Audiences ](c_audiences.md#concept_65BE870D290E412D8BBF557EEA67C271). 
>## Goals and Settings {#reference_B25389FD6F3A4989801E740364B089CC}The Goals and Settings page is where you enter information about the goals of the test. 
<draft-comment otherprops="merge">
  target/r_ab_goals_and_settings.xml 
</draft-comment>
<a id="section_9B98C5E38DC244D0829B9B06CA627EA9"></a>

This video includes information about activity settings.

<table id="table_BE6C847587DF48F78B4CDB51D82B616D"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Settings </th> 
   <th colname="col3" class="entry"> 3:02 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/6XNEM8tUADo/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/6XNEM8tUADo/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_83E87DDC778244D4B5B643B6ED309216"> 
      <li id="li_22A90DE1BB2542A699B569F131A1F639">Enter an objective for your activity</li> 
      <li id="li_ECEA0F36F9BC416FB8002979195FBF0B">Set the priority level of your activities</li> 
      <li id="li_5DF904E9214F458BB393375F99F1DCE9">Schedule activity start and end times</li> 
      <li id="li_6AE7B0397B8048C8B9DEE443D1A64148">Add audiences for reporting to create report filters</li> 
      <li id="li_0EDDBA5E70B54F22A76F1D6D722914BE">Enter notes for your activities</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

This video demonstrates how activity settings fit within the three-step guided workflow when creating an activity. Goals and settings are discussed beginning at 5:30.


<table id="table_C4F410819E2943B4993442A9001FBEF4"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating A/B Tests </th> 
   <th colname="col3" class="entry"> 8:36 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/JG0dbWDAvtk/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/JG0dbWDAvtk/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_993AF0E2F2F64B3EB2F76CB65009E96E"> 
      <li id="li_7B13E4A9E1BA4244B1E1111EC898BBE7">Create an A/B activity in Adobe Target</li> 
      <li id="li_4224721DB79D4EF9A2521B016A8FA09B">Allocate traffic using a manual split or automatic traffic allocation</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

The available settings depend on whether you use Target or Analytics as the data source.
![](graphics/ab_settings.png) 

## Activity Settings {#section_DCBDC354261F420EBD4B43EA34947BAC}



<table id="table_464BE186EE1F463DA99D16FC482A4AFA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Settings </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Objective </td> 
   <td colname="col2"> <p>Type an optional objective. The objective can be any information that helps you and your team members identify the campaign.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Priority </td> 
   <td colname="col2"> <p>Depending on your settings, the UI and options for <span class="wintitle"> Priority </span> vary. You can use the legacy settings of Low, Medium, or High, or you can enable fine-grained priorities from 0 to 999. </p> <p>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.</p> <p>If this option is not enabled in <span class="wintitle"> Setup </span> (the default), specify a priority: Low, Medium, or High. </p> <p> To enable fine-grained priorities, click <span class="wintitle"> Setup </span>, then toggle the <span class="wintitle"> Enable Fine-Grained Priorities </span> option to the "On" position. </p> <p>If this option is enabled, specify a value between 0 and 999:</p> <p> 
     <ul id="ul_FCA07A04D6F248759429BC46BA57CCE5"> 
      <li id="li_88F440506D22467295C71F2B14470AD7">0 = Low</li> 
      <li id="li_AEC7893759464944A6501FA742A2B0FE">999 = High</li> 
     </ul> </p> <p>For activities created in previous versions of <span class="keyword"> Target Standard/Premium </span>, Low priority is converted to 0, Medium is converted to 5, and High is converted to 10. You can adjust these values as necessary. </p> <p> <p>Note:  Before you can disable this option after using fine-grained priories, all priorities must be set back to 0, 5, and 10. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Duration </td> 
   <td colname="col2"> <p>The activity can start when approved, or you can set a specific date and time. Likewise, the activity can either end when it is deactivated or you can set a date and time. The time picker uses a 24-hour clock, with 00:00 being midnight. The time zone is set to the time zone configured in your browser. To use a different time zone, set your browser to another time zone and restart the browser.</p> </td> 
  </tr> 
 </tbody> 
</table>


## Reporting Settings {#section_13119392051044FBA6387D9B3B1C43CF}



<table id="table_178993EC689C4C538F3EC7E3FC205592"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Settings </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Reporting Source </td> 
   <td colname="col2"> <p>Specify whether data is collected from Adobe Target or from Adobe Analytics. See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/a4t.html" format="https" scope="external"> Adobe Analytics as the Reporting Source for Target </a> to learn about the differences between the reporting solutions and the advantages of each. </p> <p>When selecting Analytics as the reporting source for Target, you select an Analytics report suite to receive Target activity data. To do this, first choose from any of the Analytics companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to Adobe Target will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the Adobe Marketing Cloud to try again. If the report suite is still missing from the list, please contact Customer Care.</p> <p>If a reporting source is specified in your account settings, the specified source is used and this setting is not visible.</p> <p> <p>Note:  You cannot change your reporting source after the activity goes live in order to keep reports consistent. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Goal </td> 
   <td colname="col2"> <p>Select the action taken by a visitor to achieve the goal. For example, choose a Conversion metric, then set the parameters that determine when success is achieved.</p> <p>For more information about setting metrics, see <a href="t_test_ab.xml#task_A04AB66007C1467DA1C21A519A5C7BEB" format="dita" scope="local"> Set Metrics </a>. </p> <p> <p>Note:  If the reporting solution is set to Analytics, the only available goal metric is Conversion. Analytics metrics cannot be selected as a goal. </p> </p> <p>When you select your success metric, a selector displays. Use this selector to choose the specifics for the success metric.</p> <p>If enabled, the Estimated Value of the Conversion field (not available for the Page Score metrics) provides a value for your goal, but not for other metrics. This value enables Target to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. For all revenue metrics (Revenue per Visitor, Average Order Value, Total Sales, and Orders), the estimate uses Revenue per Visitor. The data type is currency.</p> <p>After reaching the activity goal, a visitor continues to see the activity content, unless that visitor qualifies for a higher priority activity. If the visitor reaches the goal again, it is counted as another conversion. Note that this is different than the default behavior in Target Classic, which counts visitors as new if they see the test again.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Additional Metrics </td> 
   <td colname="col2"> <p>Create additional success metrics.</p> <p>This setting is not available if the reporting solution is set to Analytics. In this case, the metrics defined for the Analytics report suite are applied.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Audiences for Reporting </td> 
   <td colname="col2"> <p>By default, reports show results for all qualified visitors. You can add report audiences to show only information about specific audiences.</p> <p>This setting is not available if you choose Analytics as your reporting solution. The audience defined for the Analytics report suite are applied.</p> </td> 
  </tr> 
 </tbody> 
</table>


## Advanced Settings {#section_E2FE441AFB324E498793ABB025ED9974}

Advanced settings are available for A/B Test goal metrics.
![](graphics/Menu_AdvancedSettings.png) 

>[!NOTE]
>
>If you use Adobe Analytics as your reporting source, settings are managed by the Analytics server. The advanced settings option will not be available.




<table id="table_5706360D23704F16AA18597D4C8F3438"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Which success metric must be reached before incrementing this metric? </td> 
   <td colname="col2"> <p>Use this option to only count someone as reaching the success metric if they’ve previously reached a different success metric. For example a test conversion might only be valid if the visitor clicks on the offer, or reaches a particular page before converting.</p> <p>You can provided dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increase.</p> <p>You must define both (or multiple) success metrics before you can make one dependent on another.</p> <p>The <span class="wintitle"> Add Dependency </span> option allows the success metric to increment if another success metric has been reached or has not been reached. </p> <p>To add a dependency:</p> <p> 
     <ol id="ol_7CE86C31CD5541039A3265E14D0C3630"> 
      <li id="li_3E374D8B28B443FA9FE8AF2B02814A82"> <p>After adding additional metrics, click <span class="uicontrol"> Advanced Settings </span>. </p> </li> 
      <li id="li_F65C369C8F354A6CBD447ED26D9F79E4"> <p>Click the <span class="uicontrol"> Add Dependency </span> option: </p> <p style="text-align: center;"> <img href="../graphics/add dependency.png" id="image_D3C6E4862509435E86A1F61B88F342CA" /> </p> </li> 
      <li id="li_9A6F187B4C294A9C8B5C834C76B32767"> <p>Drag and drop the desired metrics from the left pane into the right pane, then click <span class="uicontrol"> Reached </span> to toggle the setting between <span class="uicontrol"> Reached </span> and <span class="uicontrol"> Not Reached </span>. </p> <p style="text-align: center;"> <img href="../graphics/add dependency reached.png" id="image_CA136FD10D754BD1B26C621DF2A4858D" /> </p> </li> 
     </ol> </p> <p>You can edit or remove dependencies after adding them.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> What will happen after a user encounters this goal metric? </td> 
   <td colname="col2"> There are three options for what happens after a visitor reaches the goal metric: 
    <ul id="ul_2347FFB59E804DB382C3440BE684000E"> 
     <li id="li_5A8C13D4D43C436786D9FBE24C701CE1">Select <span class="uicontrol"> Increment Count &amp; Keep User in Activity </span> to specify how the count is incremented. </li> 
     <li id="li_04D4A04310354FB4A7F23023E1FE0DE0">Select <span class="uicontrol"> Increment Count, Release User &amp; Allow Reentry </span> to specify the experience the user sees if they reenter the activity. </li> 
     <li id="li_32FEAFA4C6BC469998C9181792B29BEE">Select <span class="uicontrol"> Increment Count, Release User &amp; Bar from Reentry </span> to specify what the user sees instead of the activity content. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

See [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924) for more information about advanced settings. 

## Other Metadata {#section_2E8917BEFB954480A4206B9E9E917F80}



|  Settings  | Description  |
|---|---|
|  Notes  | Type any information about your activity that is useful to keep on hand for yourself or other team members. The Notes pane is resizable.  |

>## Using Analytics Data {#task_FE48F7B077C44A5BA015B087428412EF}You can configure an Activity in Target Standard to use Adobe Analytics as the reporting source (A4T). 
<draft-comment otherprops="merge">
  target/t_create_a4t.xm 
</draft-comment>For detailed information about setting up Analytics as the data source for Target, see the [ Adobe Analytics as the Reporting Source for Adobe Target ](https://marketing.adobe.com/resources/help/en_US/target/a4t/a4t.html). 
Before you set up an activity that uses Analytics as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks on your shopping cart. Choose a final success metric for the campaign. Although you can select additional metrics at any time in Analytics, you must still specify a particular metric you expect this test to affect.

>[!NOTE]
>
>The Adobe Analytics option is available if you've linked your Adobe Marketing Cloud account with both Analytics and Target, even if integration between Target and Analytics has not been set up for your account.


When selecting Analytics as the reporting source for Target, you select an Analytics report suite to receive Target activity data. To do this, first choose from any of the Analytics companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to Adobe Target will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the Adobe Marketing Cloud to try again. If the report suite is still missing from the list, please contact Customer Care.
Analytics for Target requires a tracking server to report results correctly. A default tracking server will appear in the Tracking Server field. If you use more than one tracking server, you should check to ensure you include the correct tracking server in this field. See [ Using an Analytics Tracking Server ](a4t.md#task_72077BA7E93C4A65A715A18F32228823) for more information. 

>[!NOTE]
>
>If you use Adobe Analytics as your activity's reporting source, you do not need to specify a tracking server during activity creation if you are using ` mbox.js` version 61 (or later) or ` at.js` version 0.9.1 (or later). The ` mbox.js` or ` at.js` library automatically sends tracking server values to ` Target`. During activity creation, you can leave the ` Tracking Server` field empty on the ` Goals &amp; Settings` page. 


When setting up activity after setting up Analytics as your reporting source, there is no option to set up audiences for reporting. Analytics segments are available in the Target Activities report.
You are required to select a success metric to uses as a goal for each test. Your activity goal is the conversion activity that signals a successful campaign. It is best practice never to run a test without having a goal to improve in some specific way. You can choose any Analytics metric available in the Analytics metric selector.
Setting a goal doesn't mean you can't use another metric when evaluating test results. The goal is, however, a reminder of the one thing you want to improve with the test.
After a visitor completes your goal, that visitor is no longer included in the campaign. If the visitor re-enters your campaign after completing an activity, he or she is counted as a new visitor.
>## Set Metrics {#task_A04AB66007C1467DA1C21A519A5C7BEB}Use metrics in an A/B activity to determine when a visit is successful. 
<draft-comment otherprops="merge">
  target/t_ab_set_metrics.xml 
</draft-comment>For detailed information about success metrics, see [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924). 

>1. Specify the goal of the activity.
>1. Select a [ success metric ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924)

>       ![](../graphics/ab_metrics.png) 
>       The ` Select Metrics` page lists the success metrics you can choose for your activity. The success metrics are divided into the following categories: 
>    
>    * Conversion
>    * Revenue
>    * Engagement

>       You can use any of the pre-built success metrics, or create a custom success metric. You can also mark a success metric as a primary metric. Reports and Marketing Cloud cards default to show the primary metric, if one is set.
>1. Specify the settings for your metrics.

>       The available settings depend on the success metric you are using.
>       If enabled, the ` Estimated Value of the Conversion`field (not available for the Page Score metrics) provides a value for your goal. This value enables Target to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. The data type is currency. This field is progressively shown after the user indicates the action taken to satisfy the goal. See [ Estimating Lift in Revenue ](c_estimating_lift_in_revenue.md#concept_32F875D8F91349CE86AF391F65BEAEEE) for more information. 
>       The correct configuration of success metrics is critical for making sure you get the data you expect.
>       For more information, see [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924). 
>1. (Optional) Add additional metrics.
>1. Click ** ` Continue` ** when you are finished setting your metrics.
>## Multiple Experience Versions in an A/B Test {#task_0138112E283A4A5B9F8AB9AAF2FBC2FF}You can target versions of the same experience to different audiences in A/B activities. You can set up multiple audiences for an experience in the Visual Experience Composer or in the Form-Based Experience Composer. 
<draft-comment otherprops="merge">
  target/t_target-experience-to-multiple-audiences.xml 
</draft-comment>Users can switch between experience audiences as their profile changes. They are not stuck in the same experience for the activity's lifetime.
For example, if your site uses a consistent design across pages or products and you want to use the same experience for multiple audiences (such as visitors with different browser languages), you can set up multiple versions of the experience. You might present the same experience to English and Japanese speakers, with the only difference being that the text is presented in the visitor's language. Data is collected for the experience, regardless of language, so the report shows the performance of the experience, rather than the version.
Without the ability to set up experience versions, you would have to set up different tests for each language (in this example), then manually aggregate the results to try to get an idea how a single experience with both languages might perform. This produces less accurate results. For some tests, these calculations might not even be useful because of the way visitors are randomized.
By creating different versions of an experience, you receive more accurate information without the need for manual calculations and assumptions.
**Scenario** 
You are testing two experiences, a geo-targeted banner vs. a generic banner. The banner for each geography needs to be different, but the overall test is to determine whether geotargeting is better than showing generic content. If you set up a separate experience for each location, you would actually be measuring how each geo performs against the other, rather than whether geotargeting helps meet your success goals when measured against the generic banner.
In this case, what you need are geo-specific versions of the experience, so you can test the geotargeted experience against a non-geotargeted control.

>1. [ Create an A/B activity ](t_test_ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) as you normally would.

>1. Select the experience, then click ** ` Configure` ** > ** ` Audiences` ** > ** ` Multiple Audiences` **.

>       ![](../graphics/multiple-audiences.png) 
>1. Click ** ` Add Audience` **, then select the first audience you want to target. Repeat for each audience.

>       ![](../graphics/exp-versions.png) 
>       If the audience does not yet exist, click [ Create Audience ](c_audiences.md#task_E18BD77A9A8F4ED0AC50569F94556558) and set it up. 
>       If a visitor qualifies for more than one audience, the content for all audiences is returned, with the last one in the list actually rendering on the page.
>1. Continue setting up the activity.
>## Nine Common A/B Testing Pitfalls and How to Avoid Them {#concept_578A7947C9554868B30F12DFF9E3F8E3}A/B testing forms the backbone of most digital marketing optimization programs, helping marketers offer optimized and targeted experiences to their visitors and customers. This section outlines nine of the most significant pitfalls that companies fall prey to when performing A/B testing. It also includes ways to avoid them, so your company can achieve greater ROI through its testing efforts and have greater confidence in its reported A/B test results. 
<draft-comment otherprops="merge">
  target/c_common-ab-testing-pitfalls.xml 
</draft-comment>
## 1. Ignoring the Effects of the Significance Level {#section_55F5577A13C6470BA1417C2B735C6B1D}

How likely is it that your test reports a significant difference in conversion rate between two offers when in fact there is none? That's what the *significance level* of a test helps determine. Such misleading findings are often called a false positive, and in the world of statistics, are called a Type I error. 
When you specify the significance level of an A/B test, you're making a trade-off between your tolerance for false positives versus the number of visitors that the test must include.
Another directly related term, the *confidence level*, takes more of a glass half-full approach. Rather than stating the likelihood that you'll get a false positive, as the significance level does, the confidence level represents the likelihood that your test will not make that mistake. 
Confidence level and significance level are directly related because:
100% - confidence level = significance level
In A/B testing, marketers often use 95% confidence levels. Clearly, based on the above equation, that corresponds to a significance level of 5%. Testing with a 95% confidence level means you have a 5% chance of detecting a statistically significant lift, even when in reality, there's no difference between the offers.
As the graph below illustrates, the more tests that you run, the more likely at least one of those tests will result in a false positive. For example, if you run 10 tests using a 95% confidence level, there is approximately a 40% chance that you will detect one or more false positives (given that there is no real lift: Pr(at least one false positive) = 1 - Pr(no false positives) = 1 - 0.95^10 = 40%).
![](graphics/pitfalls1.png) 
In a marketing organization, 95% usually constitutes a reasonable trade-off between the risk of a false positive and the opportunity costs of running the test for a longer time to have greater confidence in the results.
However, two situations warrant paying close attention to the significance level and its implications for test results: post-test segmentation and testing multiple offers.

* **Post-Test Segmentation:**Marketers often slice and dice the results of a test based on visitor segments after the A/B test concludes. Common segments include browser type, device type, geographic areas, time of day, and new versus returning visitors. This practice, known as post-test segmentation, provides excellent insight into visitor segments. In turn, marketers can use these insights to create better-targeted and more-relevant and differentiated content. 
  If there is no real difference in conversion rate, each time you test a segment, the probability of a false positive equals the significance level. And, as mentioned, the more tests you run, the greater the likelihood that you'll experience at least one false positive among those tests. In essence, each post-test segment represents a separate test. With a significance level of 5%, on average you'll fall prey to one false positive every time you look at 20 post-test segments. The chart above shows how that likelihood increases.
  Should you simply not do post-test segmentation? No, post-test segments are valuable. Instead, to avoid this cumulative false positive issue with post-test segmentation, after you've identified a post-test segment, consider testing it in a new test. Alternatively, you can apply the Bonferroni correction, discussed next.

* **Testing Multiple Offers:**Marketers frequently test more than two offers (or experiences) against each other. That's why you sometimes see A/B testing solutions called A/B/n testing, where n is the number of offers that you are testing simultaneously. 
  It's important to note that *each* offer tested has a false positive rate equal to the significance level, as described above. Again, you are effectively running multiple tests when several offers are pitted against each other within a single test environment. For example, if you compare five offers in an A/B/C/D/E test, effectively you form four comparisons: control to B, control to C, control to D, control to E. With a confidence level of 95%, rather than the 5% probability of a false positive, you actually have 18.5%. 2 
  To keep your overall confidence level at 95% and avoid this issue, you apply what is known as the Bonferroni correction. Using this correction, you simply divide the significance level by the number of comparisons to come up with the significance level that you need to achieve a 95% confidence level.
  Applying the Bonferroni correction to the example above, you would use a 5%/4 = 1.25% significance level, which is the same as a 98.75% confidence level for an individual test (100% - 1.25% = 98.75%). This adjustment maintains the effective confidence level at 95% when you have four tests, as in the described example.



## 2. Declaring Winners of Multiple Offer Tests with No Statistically Significant Difference {#section_FA83977C71DB4F69B3D438AF850EF3B6}

With multiple offer testing, marketers often declare the offer with the highest lift as the test winner, even though there is no statistically significant difference between the winner and the runner-up. This situation occurs when the difference between the alternatives is smaller than the difference between the alternatives and the control. The figure below illustrates this concept, with the black error bars representing 95% lift confidence intervals. The true lift for each offer relative to the control offer is 95% likely to be included within the confidence interval-the range shown by the error bars.
![](graphics/pitfalls2.png) 
Offers A and B have the highest observed lift during the test, and it would be unlikely that offer C would outperform those offers in a future test, because the confidence interval of C does not even overlap with the confidence intervals of A or B. However, even though offer A has the highest observed lift during the test, it is quite possible that offer B could perform better in a future test because the confidence intervals overlap.
The takeaway here is that both offers A and B should be considered winners of the test.
It's typically not feasible to run the test long enough to identify the true relative performance of the alternatives, and oftentimes the difference in performance between the alternatives is too small to substantially impact the conversion rate. In such cases, you can interpret the outcome as a tie and use other considerations, such as strategy or alignment with other elements of the page, to determine which offer to implement. With multiple tests, you must be open to more than one winner, which in some cases considerably opens up the possibilities for the direction to take with your website development.
Note that if you do want to identify the offer with the highest conversion rate, you are comparing all offers to every other offer. In the example above, you have n = 5 offers—you have to make n(n-1)/2 comparisons, or 5*(5-1)/2 = 10 comparisons. In this case, the Bonferroni correction requires that the significance level of the test be 5%/10 = 0.5%, which corresponds to a confidence level of 99.5%. However, such a high confidence level might require you to run the test for an unreasonably long period of time.

## 3. Ignoring the Effects of Statistical Power {#section_0D517079B7D547CCAA75F80981CBE12A}

Statistical power is the probability that a test will detect a real difference in conversion rate between offers. Because of the random, or as statisticians like to call it, "stochastic," nature of conversion events, a test might not show a statistically significant difference, even when a real difference exists in conversion rate between two offers in the long run. Call it bad luck or by chance. Failing to detect a true difference in conversion rate is called a false negative or a Type II error.
The single most important factor that determines the power of a given test is the sample size, that is, the number of visitors included in the test. The statistical power also depends on the magnitude of the difference in conversion rate you want the test to detect. Perhaps this is somewhat intuitive, but if you are interested in only detecting large conversion rate differences, there's a much higher probability that the test will actually detect such large differences—kind of like discovering that you have an elephant in your living room versus a fly while looking through a paper towel tube. Along those lines, the smaller the difference you want to detect, the more observations, and therefore, time to get those observations, you require.
Today's marketers under-power a remarkable number of tests. In other words, they use a sample size that is too small. That means that they have a slim chance of detecting true positives, even when a substantial difference in conversion rate actually exists. In fact, if you continually run underpowered tests, the number of false positives can be comparable to, or even dominate, the number of true positives. This often leads to implementing neutral changes to a site (a waste of time) or changes that actually reduce conversion rates.
![](graphics/pitfalls3.png) 
To avoid under-powering your test, consider that a typical standard for a well-powered test includes a confidence level of 95% and a statistical power of 80%. Such a test offers a 95% probability that you'll avoid a false positive and an 80% probability that you'll avoid a false negative.

## 4. Using One-Tailed Tests {#section_8BB136D1DD6341FA9772F4C31E9AA37C}

One-tailed tests require a smaller observed difference in conversion rates between the offers to call a winner at a certain significance level. This seems appealing because winners can be called earlier and more often than when using two-tailed tests. But in keeping with the saying, "There's no free lunch," one-tailed tests come at an expense.
In a one-tailed test, you test whether offer B is better than offer A. The direction of the test has to be determined before the test commences, or "a priori" in statistics-speak. In other words, you must decide whether to test for B being better than A or A being better than B *before* initiating the test. However, if you look at the results of the A/B test and see that B is doing better than A and *then* decide to do a one-tailed test to see whether that difference is statistically significant, you are violating the assumptions behind the statistical test. Violating the assumptions of the test means that your confidence intervals are unreliable and the test has a higher false positive rate than you would expect. 
You might view a one-tailed test as putting an offer on trial with a judge who has already made up his or her mind. In a one-tailed test, you've already decided what the winning offer will be and are out to prove it, rather than giving each experience an equal chance to prove itself as the winner. One-tailed tests should only be used in the rare situations in which you are only interested in whether one offer is better than the other and not the other way around. To avoid the issue of the one-tailed test, use an A/B testing solution that always uses two-tailed tests, such as ` Adobe Target`. 

## 5. Monitoring Tests {#section_EA42F8D5967B439284D863C46706A1BA}

Marketers frequently monitor A/B tests until the test determines a significant result. After all, why test after you've achieved statistical significance?
Unfortunately, it's not that simple. Not to throw a wrench in the works, but it turns out that monitoring the results adversely impacts the effective statistical significance of the test. It actually greatly increases the likelihood of false positives and makes your confidence intervals untrustworthy.
This might seem confusing. It sounds like we are saying that just from looking at your results mid-test, you can cause them to lose their statistical significance. That's not exactly what's going on. The following example explains why.
Let's say you simulate 10,000 conversion events of two offers, with both offers having 10% conversion rates. Because the conversion rates are the same, you should detect no difference in conversion lift when you test the two offers against each other. Using a 95% confidence interval, the test results in the expected 5% false positive rate when it is evaluated after collecting all 10,000 observations. So if we run 100 of these tests, on average we will get five false positives (in actuality, all positives are false in this example because there is no difference in conversion rate between the two offers). However, if we evaluate the test 10 times during the test—every 1,000 observations—it turns out that the false positive rate jumps up to 16%. Monitoring the test has more than tripled the risk of false positives! How can this be?
To understand why this occurs, you have to consider the different actions taken when a significant result is detected and when it is not detected. When a statistically significant result is detected, the test is stopped and a winner is declared. However, if the result is not statistically significant, we allow the test to continue. This situation strongly favors the positive outcome, and hence, distorts the effective significance level of the test.
To avoid this problem, you must determine an adequate sample size—the number of visitors exposed to each offer—before initiating the test. While it's fine to look at the test results during the test to make sure that you implemented the test correctly, do not draw conclusions or stop the test before the required number of visitors is reached.

## 6. Stopping Tests Prematurely {#section_DF01A97275E44CA5859D825E0DE2F49F}

It is tempting to stop a test if one of the offers performs much better or worse than the others in the first few days of the test. However, when the number of observations is low, there is a high likelihood that a positive or negative lift will be observed just by chance because the conversion rate is averaged over a low number of visitors. As the test collects more data points, the conversion rates converge toward their true long-term values.
The figure below shows five offers that have the same long-term conversion rate. Offer B had a poor conversion rate for the first 2,000 visitors, and it takes a long time before the estimated conversion rate returns to the true long-term rate.
![](graphics/pitfalls4.png) 
This phenomenon is known as "regression to the mean," and can lead to disappointment when an offer that performed well during the initial days of a test fails to keep up this level of performance in the long run. It can also lead to lost revenue when a good offer is not implemented because it happened to underperform in the early days of a test just by chance.
Much like the pitfall of monitoring your test, the best way to avoid these issues is to determine an adequate number of visitors before running the test and then let the test run until this number of visitors has been exposed to the offers.

## 7. Not Considering Novelty Effects {#section_90F0D24C40294A8F801B1A6D6DEF9003}

Other unexpected things can happen if we don't allow enough time for running a test. This time the problem is not a statistics problem; it's simply a reaction to change by the visitors. If you change a well-established part of your website, returning visitors might at first engage less fully with the new offer because of changes to their usual workflow. This can temporarily cause a superior new offer to perform less optimally until returning visitors become accustomed to it—a small price to pay given the long-term gains that the superior offer will deliver.
To determine if the new offer underperforms because of a novelty effect or because it's truly inferior, you can segment your visitors into new and returning visitors and compare the conversion rates. If it's just the novelty effect, the new offer will win with new visitors. Eventually, as returning visitors get accustomed to the new changes, the offer will win with them, too.
The novelty effect can also work in reverse. Visitors often react positively to a change just because it introduces something new. After a while, as the new content becomes stale or less exciting to the visitor, the conversion rate drops. This effect is harder to identify, but carefully monitoring changes in the conversion rate is key to detecting this.

## 8. Not Considering Differences in the Consideration Period {#section_B166731B5BEE4E578816E351ECDEA992}

The consideration period is the time period from when the A/B testing solution presents an offer to a visitor to when the visitor converts. This can be important with offers that affect the consideration period substantially—for example, an offer that implies a deadline, such as "Time-limited offer—Purchase by this Sunday."
Such offers nudge visitors to convert sooner and will be favored if the test is stopped immediately after the offer expires, because the alternative offer might have a longer deadline or no deadline, and therefore, a longer consideration period. The alternative would get conversions in the period after the termination of the test, but if you stop the test at the end of the deadline, further conversions do not get counted toward the test conversion rate.
The figure below shows two offers that two different visitors see at the same time on a Sunday afternoon. The consideration period for offer A is short, and the visitor converts later that day. However, offer B has a longer consideration period, and the visitor who saw offer B thinks about the offer for a while and ends up converting Monday morning. If you stop the test Sunday night, the conversion associated with offer A is counted toward offer A's conversion metric, whereas the conversion associated with offer B is not counted toward offer B's conversion metric. This puts offer B at a significant disadvantage.
![](graphics/pitfalls5.png) 
To avoid this pitfall, allow some time for visitors who were exposed to the test offers to convert after a new entry to the test has been stopped. This step gives you a fair comparison of the offers.

## 9. Using Metrics that Do Not Reflect Business Objectives {#section_F0CD6DC7993B4A6F9BEEBB31CD1D9BEE}

Marketers might be tempted to use high-traffic and low-variance conversion metrics in the upper funnel, such as click-through rate (CTR), to reach an adequate number of test conversions faster. However, carefully consider whether CTR is an adequate proxy for the business goal that you want to attain. Offers with higher CTRs can easily lead to lower revenue. This can happen when offers attract visitors with a lower propensity to buy, or when the offer itself-for example, a discount offer-simply leads to lower revenue.
![](graphics/pitfalls6.png) 
Consider the skiing offer below. It generates a much higher CTR than the cycling offer, but because visitors spend much more money on average when they follow the cycling offer, the expected revenue of putting the cycling offer in front of a given visitor is higher. Therefore, an A/B test with CTR as the metric would pick an offer that does not maximize revenue-the fundamental business objective.
![](graphics/pitfalls7.png) 
To avoid this issue, monitor your business metrics carefully to identify the business impact of the offers, or better yet, use a metric that is closer to your business goal, if possible.

## Conclusion: Success with A/B Testing by Recognizing and Stepping Around the Pitfalls {#section_54D33248163A481EBD4421A786FE2B15}

After learning about the common A/B testing pitfalls, we hope you can identify when and where you might have fallen prey to them. We also hope we've armed you with a better understanding of some of the statistics and probability concepts involved in A/B testing that often feel like the domain of people with math degrees.
The steps below help you avoid these pitfalls and focus on achieving better results from your A/B testing:

* Carefully consider the right metric for the test based on relevant business goals.

* Decide on a confidence level before the test starts, and adhere to this threshold when evaluating the results after the test ends.

* Calculate the sample size (number of visitors) before the test is started.

* Wait for the calculated sample size to be reached before stopping the test.

* Adjust the confidence level when doing post-test segmentation or evaluating more than one alternative—for example, by using the Bonferroni correction.


