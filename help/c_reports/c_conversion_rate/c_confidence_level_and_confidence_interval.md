---
description: For each experience, confidence level and confidence interval are displayed.
keywords: confidence level;confidence interval;conversion;continuous variables;conversion rate;sample size;standard deviation
seo-description: For each experience, confidence level and confidence interval are displayed.
seo-title: Confidence Level and Confidence Interval
solution: Target
title: Confidence Level and Confidence Interval
topic: Advanced,Standard,Classic
uuid: 0397c1fb-6dae-4a07-ab1b-bfb5dee1f60c
index: y
internal: n
snippet: y
translate: y
---

# Confidence Level and Confidence Interval

Conversions and continuous variables for Target-based metrics, such as revenue and engagement metrics, are calculated as follows: 


* **Conversion:** Either yes or no
* **All others:** Values across a range


You can perform offline calculations for Analytics for Target (A4T), but it requires a step with data exports in [!DNL  Analytics]. For more information, see "Performing Offline Calculations for Analytics for Target (A4T)" below. 

This section contains the following information: 


* [ Confidence Level ](../../c_reports/c_conversion_rate/c_confidence_level_and_confidence_interval.md#section_26FE5E44BDD5478792A65FCFD83DCCDC)
* [ Confidence Interval ](../../c_reports/c_conversion_rate/c_confidence_level_and_confidence_interval.md#section_F582738DFE1648C78B93D81EBC6CACF7)
* [ Confidence Calculation and How to Perform It Offline ](../../c_reports/c_conversion_rate/c_confidence_level_and_confidence_interval.md#section_86F7C231943043A5B8B6BFE67B706E3B)
* [ Performing Offline Calculations for Analytics for Target (A4T) ](../../c_reports/c_conversion_rate/c_confidence_level_and_confidence_interval.md#section_B34BD016C8274C97AC9564F426B9607E)


## Confidence Level {#section_26FE5E44BDD5478792A65FCFD83DCCDC}

The *confidence level* is represented by the darker percentage in the Conversion Rate column for each experience. 

![](assets/conf_report.png)  ![](assets/conf_report_detail.png) 

The confidence level, or statistical significance, indicates how likely it is that an experience's success was not due to chance. A higher confidence level indicates: 


* The experience is performing significantly different from control.
* The experience performance is not just due to noise.
* If you ran this test again, it is likely that you would see same results.


If the confidence level is over 90% or 95%, then the result can be considered statistically significant. Before making any business decisions, try to wait until your sample size is large enough and that the four bars of confidence on one or more experiences stays consistent for a continuous length of time to ensure the results are stable. 


>[!NOTE]
>
>The confidence rounds up to 100.00% when the confidence is greater than or equal to 99.995%.



## Confidence Interval {#section_F582738DFE1648C78B93D81EBC6CACF7}


>[!NOTE]
>
>Currently, the confidence interval is calculated only for binary metrics.



The *confidence interval* is a range within which the true value can be found at a given confidence level. The confidence interval appears as a light gray +/- percentage in the Conversion Rate column. In the example below, the confidence interval for Experience B's lift is plus or minus 15.65%. 

![](assets/conversion_rate.png) 

**Example:** An experience's RPV is $10, its confidence level is 95% and its **confidence interval** is $5 to $15. If we ran this test multiple times, 95% of the time the RPV would be between $5 and $15. 

**What impacts the confidence interval?** The formula follows standard statistical methods for calculating confidence intervals. 


* **Sample size:** As sample grows the interval will shrink or narrow. This is preferred as it means your reports are getting closer to the true value of the success metric.
* **Standard deviation smaller:** More similar results, such as similar AOVs or similar numbers or visitors converting each day, reduces the standard deviation.


## Confidence Calculation and How to Perform It Offline {#section_86F7C231943043A5B8B6BFE67B706E3B}

The [ downloaded CSV report ](../../c_reports/c_downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) includes only raw data and does not include calculated metrics, such as revenue per visitor, lift, or confidence used for A/B tests. 

To calculate these calculated metrics, download the [ Target's Complete Confidence Calculator ](https://marketing.adobe.com/resources/help/en_US/target/target/complete_confidence_calculator.xlsx) Excel file to input the activity's value, or review the [ statistical calculations used by Target ](https://marketing.adobe.com/resources/help/en_US/target/target/Statistical Calculations.pdf). 

## Performing Offline Calculations for Analytics for Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

You can perform offline calculations for A4T, but it requires a step with data exports in [!DNL  Analytics]. 

For A4T, we use a Student's t-test calculation for continuous variables (rather than binary metrics). In Analytics, a visitor is always tracked, and every action taken is counted. Therefore, if the visitor purchases multiple times or visit a success metric multiple times, those additional hits are counted. This makes the metric a continuous variable. To perform the Student's t-test calculation, the "sum of squares" is required. This can be retrieved from [!DNL  Analytics]. To get the sum of squares data, you need to perform a visitor-level export for the metric you are optimizing to, for a sample time period. 

For example, if you’re optimizing to page views per visitor, you’d export a sample of the total number of page views on a per visitor basis for a specified time frame, perhaps a couple of days (a few thousand data points is all you need). You would then square each value and sum the totals (the order of operations is critical here). This "sum of squares" value is then used in the Complete Confidence Calculator. Use the "revenue" section of that spreadsheet for these values. 

**To use the [!DNL  Analytics] data export feature to do this:** 


1. Log in to [!DNL  Adobe Analytics]. 

1. Click **[!UICONTROL  Tools]** > **[!UICONTROL  Data Warehouse]**. 

1. On the **[!UICONTROL  Data Warehouse Request]** tab, fill in the fields. 

   For more information about each field, see "Data Warehouse Descriptions" in [ Data Warehouse ](https://marketing.adobe.com/resources/help/en_US/reference/data_warehouse.html). 



<table id="table_0644A7F8ABCB429B85DFF8C73762619F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Field </th> 
   <th colname="col2" class="entry"> Instructions </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Request Name </p> </td> 
   <td colname="col2"> <p>Specify a name for your request. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting Date </p> </td> 
   <td colname="col2"> <p>Specify a time period and granularity. </p> <p>As best practice, choose no more than an hour or one day of data for your first request. </p> <p>Data Warehouse files take longer to process the longer the time period requested, so it is always a best practice to request a small time period data first to make sure your file returns the expected result. Then, go to the Request Manager, duplicate your request, and ask for more data the second time. Also, if you toggle granularity to anything other than “None,” the file size will increase drastically. </p> <p style="text-align: center;"> <img href="assets/datawarehouse.png" id="image_D58215BCAF2B4DA3B22437C199A59418" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Available Segments </p> </td> 
   <td colname="col2"> <p>Apply a segment, as needed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Breakdowns </p> </td> 
   <td colname="col2"> <p>Select the desired dimensions: </p> <p>Standard is out-of-the-box (OOTB), while Custom includes eVars &amp;amp; props. It is recommended you use “Visitor ID” if visitor ID level information is needed, rather than “Experience Cloud Visitor ID.” </p> <p> 
     <ul id="ul_2F4D7201447240AF974F73BD2D607F3D"> 
      <li id="li_6FF1F0D5F91C41398AA6CDE0A69E154A"> <p>Visitor ID is the final ID used by Analytics. It will either be AID (if the customer is legacy) or MID (if the customer is new or cleared cookies since the MC visitor ID service was launched). </p> </li> 
      <li id="li_5E0099C92E6C4F88A54BAA352D04E4E0"> <p>Experience Cloud Visitor ID will only be set for customers who are new or cleared cookies since the MC visitor ID service was launched. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Metrics </p> </td> 
   <td colname="col2"> <p> Select your desired metrics. Standard is OOTB, while Custom includes custom events. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Preview </p> </td> 
   <td colname="col2"> <p>Review your settings before scheduling the report. </p> <p style="text-align: center;"> <img href="assets/datawarehouse2.png" id="image_D209CF4053204BE591CEF42BEB0C065C" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Schedule Delivery </p> </td> 
   <td colname="col2"> <p>Enter an email address to deliver the file to, name the file, then select <span class="uicontrol"> Send Immediately </span>. </p> <p> <p>Note:  The file can be delivered via FTP under <span class="wintitle"> Advanced Delivery Options </span>. </p> </p> <p style="text-align: center;"> <img href="assets/datawarehouse3.png" id="image_DD2DA7CA0FAB4EC78D9BC80476301576" /> </p> </td> 
  </tr> 
 </tbody> 
</table>


1. Click **[!UICONTROL  Request this Report]**. 

   File delivery can take up to 72 hours, depending on the amount of data requested. You can check on the progress of your request at any time by clicking [!UICONTROL  Tools] > [!UICONTROL  Data Warehouse] > [!UICONTROL  Request Manager]. 

   If you would like to re-request data that you’ve requested in the past, you can duplicate an old request from the [!UICONTROL  Request Manager] as needed. 



For more information about [!DNL  Data Warehouse], see the following links in the [!DNL  Analytics] Help documentation: 


* [ Create a Data Warehouse Request ](https://marketing.adobe.com/resources/help/en_US/reference/t_dw_create_request.html) 

* [ Data Warehouse Best Practices ](https://marketing.adobe.com/resources/help/en_US/reference/data_warehouse_bp.html) 


