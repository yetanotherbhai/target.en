---
description: The Traffic Estimator provides feedback that lets you know whether you have sufficient traffic for the test you designed to succeed.
seo-description: The Traffic Estimator provides feedback that lets you know whether you have sufficient traffic for the test you designed to succeed.
seo-title: Estimate the Traffic Required for Success
solution: Target
title: Estimate the Traffic Required for Success
topic: Standard
uuid: 345a8543-e3d6-454b-88d5-c82057257c06
index: y
internal: n
snippet: y
translate: y
---

# Estimate the Traffic Required for Success

Because an Automated Personalization activity uses multiple content combinations, it is important to know how much traffic is required to provide meaningful results. The Traffic Estimator uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration needed to make the test successful.
The Traffic Estimator determines if there is enough traffic to generate personalized models, by comparing the estimated page impressions and typical conversion rate for the pages. Ideally, for a successful activity, the correct sample size ensures that personalized content is ready within 50% of the activity duration or 14 days, whichever is less. This allows sufficient time for obtaining personalized content and learning which content to deliver.
Once a predictive model passes the required quality criteria and is deemed valid, it is considered ready and is used to calculate a personalized score for offer decisioning. A visual indicator shows when the model is ready and Target is able to begin delivering personalized content. Since lift is expected only after the models are ready, the visual indication allows you to set the right expectation. Use the traffic estimator in the Visual Experience Composer to get a guideline of when the models will be ready.

>1. From the Experience Composer, click ** `Traffic` **.

>       The Traffic Estimator opens. You can click ** `Traffic` ** again to hide the Traffic Estimator. 
>       ![](../graphics/ap_est.png) 
>1. Provide the typical conversion rate, estimated activity impressions per day, and test duration.

>    
>    * Number of Content Combinations Calculated automatically based on the number of experiences being created as a part of your activity after any exclusions.

>    * Typical Conversion Rate The conversion rate is expressed as a percentage, based on your estimation or past data from your analytics system

>    * Estimated Activity Impressions Per Day This is the number of visitors who are likely to view this page based on the targeting criteria. This could be based on your analytics data.

>    * Test Duration The number of days you want the activity to run.


>       The Traffic Estimator uses these statistics to determine what adjustments are needed to run a successful test.
>       Near the top of the Traffic Estimator, the values you entered are calculated and the results are shown.
>       ![](../graphics/ap_est_no.png) 
>       As you change the numbers, the estimate changes. For example, if you are testing a large number of combinations and your conversion rate and impressions are too low, the Traffic Estimator shows how long the test will need to run to be successful. Or, if your traffic is low, the Traffic Estimator might suggest a lower number of combinations so you can run the test the desired number of days.
>       If you do not have sufficient traffic, you can do one or both of the following:
>    
>    * Reduce the number of combinations.
>    * Increase the duration of the test.

>       Adjust the numbers until the Traffic Estimator says you have sufficient traffic, then design your test accordingly.
>       ![](../graphics/ap_est_yes.png) 
>       If the traffic is sufficient, the Traffic icon shows a green check. If it is insufficient, the icon shows a red warning label.
