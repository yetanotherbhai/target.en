---
description: List of frequently asked questions about reporting in Target.
keywords: troubleshooting;metric discrepancies;FAQ;reports
seo-description: List of frequently asked questions about reporting in Target.
seo-title: Reporting Frequently Asked Questions
solution: Target
title: Reporting Frequently Asked Questions
topic: Standard
uuid: 737c7c16-0b4d-4114-bc15-7a9620fac323
index: y
internal: n
snippet: y
translate: y
---

# Reporting Frequently Asked Questions

This section contains the following information:

* [Why are the number of visits lower in Target than...](c_reporting-frequently-asked-questions.md#section_7E626FDB417E41B8B58BBF30FB207409)
* [Why is there no data available for my activity's report?](c_reporting-frequently-asked-questions.md#section_E4722F6445884130951DF79981C8289B)


## Why are the number of visits lower in Target than in other Marketing Cloud solutions? {#section_7E626FDB417E41B8B58BBF30FB207409}

Metric numbers, for example visits, reported by `Target` will always be lower than the reported numbers in other `Marketing Cloud` solutions for a number of reasons: 

* `Target` counts visits only for visitors that qualified for the activity. Other solutions count visits for visitors that display the page, regardless of which activity brought them to the page. 

* There might be situation where different activities compete for the same location (mutually exclusive). As a result, visitors see different content on a web page, which affects the metric numbers reported by `Target`. 



## Why is there no data available for my activity's report? {#section_E4722F6445884130951DF79981C8289B}

If an activity's content was successfully delivered to users but its report contains no data, ensure that you have the correct environment (host group) selected in the report's settings.
If you have a development environment selected, you might see the following error message: "There is no data available for the selected report settings."
To change the environment for an activity's report:

1. Click ** `Activities` **, click the desired activity from the list, then click the ** `Reports` ** tab. 

1. Click the `Settings` icon (  ![](graphics/icon_gear.png) ) to configure report settings. 
   ![](graphics/ab_settings_dialog.png) 

   >[!NOTE]
   >
   >The Settings icon ( ![](graphics/icon_gear.png) ) is not available for Automated Personalization reports. 


1. From the ** `Environment` ** drop-down list, select ** `Production` **. 
   Report data might not be available if you have a development environment selected.

1. Click ** `Save Settings` **. 


For more information about environments, see [Hosts](c_hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E). 
