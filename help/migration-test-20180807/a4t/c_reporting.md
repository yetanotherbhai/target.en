---
description: Using Analytics as your reporting source for Target (A4T) gives you access to Analytics reports for your Target activities.
seo-description: Using Analytics as your reporting source for Target (A4T) gives you access to Analytics reports for your Target activities.
seo-title: Reporting
solution: Target
subtopic: Multivariate Test
title: Reporting
topic: Standard
uuid: 26c8784d-e6e8-4fbf-9c37-946d23271692
index: y
internal: n
snippet: y
translate: y
---

# Reporting

You can view reports for your activities in both Analytics and Target Standard/Premium.

## Overview {#section_035A62D65608423285D8A5A54731E2C5}

Both Analytics and Target reports measure entrants (the people who enter the tests), rather than visitors to the site.
Every time a visitor sees activity content on the page, Target makes a direct server-to-server call to Analytics, including which activity and experience the visitor saw. Target also calls Analytics whenever the conversion is made. Analytics adds the conversion as a specific new Analytics event named "Activity Conversion," which is tracked along with other data collected by Analytics.
When the Select operation is used and you sort on *Entrants*, then only experiences that received entrants during the selected time period are displayed in the reports. 

>[!NOTE]
>
>Reports powered by Target have a latency of four minutes. For activities powered by A4T, in both the Target and Analytics reports, it can take up to 24 hours after the activity is initially saved before the report data can be broken down by experiences. The data collected in that first 24 hours is still accurate and is assigned to the right experience.



## Reports in Analytics {#section_F6884872DC864AE7913587FAED4CD11C}

In Analytics, click ** `Target` ** > ** `Target Activities` ** in the left menu. In Target, the activity's reports automatically show Analytics data, metrics, and segments. Data appears in these reports approximately an hour after it is collected from the site. All metrics, audiences, and values in the reports come from the report suite you selected when you set up the activity. 
In Analytics, use the Target Activities report to view the results of your Target activity. Test&amp;Target (Legacy) Reports provides information about your old Test&amp;Target plug-in style page integrations and does not include Analytics for Target data. In the Activities report, view information about your Target experiences. Click ** `Metrics` **, then select the ** `Target` ** metric type. Two metrics are available for your report: 

* **Activity Entries:**Matches the Entrants number in the Target report. 

* **Activity Conversions:**Matches the Custom Conversions number in the Target report. 



>[!NOTE]
>
>Target lift and confidence details are also available in Analytics. For more information, see[Target Lift and Confidence Report Type](https://marketing.adobe.com/resources/help/en_US/reference/report_target_lift_confidence.html) in the Adobe Analytics product documentation. 




<table id="table_AB508EF6FCC644BEB3E4A874E70565C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"><img href="graphics/warning.jpg" id="image_38751CD382D741D09736B02A609DD863" /> </td> 
   <td colname="col2"> <p>If your Target Activities report in Analytics lists "unspecified" instead of listing your activities, an update is required to your provisioned account. Please contact Customer Care to resolve this issue.</p> </td> 
  </tr> 
 </tbody> 
</table>


## Reports in Target {#section_C0D1F17F88374B6690BF904D7B83B42E}

When Analytics is used as the reporting source, reports in Target Standard show the data gathered from Analytics. The report differs somewhat from other Target Standard reports:

* The Audiences list shows the audiences available to your Analytics report suite.

* The Metric list shows every metric available through Analytics.
  Every metric is available, including any custom or calculated metrics that are built-in in Analytics.
  Be aware that any numbers that increase are shown as positives in the report, even when an increase is actually undesired. For example, even though you want a lower bounce rate, the higher bounce rate is shown as the winner with highest lift. Be aware of these and similar metrics, and whether you'd prefer to decrease or increase the numbers, when making decisions based on your reports.


You can apply the metric or audience to the report in Target after the test has started, or even after the test has completed. You don't have to know exactly what you want to measure beforehand.
Click to view the full Analytics report directly from the activity report page.

## Activity Creation {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

During activity creation, you must specify a goal for the activity on the `Settings` page. This goal becomes the default metric for the report and is always listed as the first option in the metrics selector. You cannot select segments for reporting like you would for a regular Target activity. A test with Analytics uses Adobe Analytics segments rather than Target Standard audiences. 

## Performing Offline Calculations for Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

You can perform offline calculations for A4T, but it requires a step with data exports in `Analytics`. 
For more information, see [Performing Offline Calculations for Analytics for Target (A4T)](c_confidence_level_and_confidence_interval.md#section_B34BD016C8274C97AC9564F426B9607E). 
