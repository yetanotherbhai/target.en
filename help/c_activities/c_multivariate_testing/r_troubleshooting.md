---
description: This topic contains suggestions for resolving some issues that might occur when designing an MVT test.
keywords: Mobile Web Experience Editor
seo-description: This topic contains suggestions for resolving some issues that might occur when designing an MVT test.
seo-title: Troubleshooting Multivariate Tests
solution: Target
subtopic: Mobile Viewports
title: Troubleshooting Multivariate Tests
topic: Standard
uuid: 6aaa76ca-693b-491c-b7cc-beba391e070d
index: y
internal: n
snippet: y
translate: y
---

# Troubleshooting Multivariate Tests



* When editing an activity, if you used Analytics-based metrics and the report suite doesn't load (spinner displays), switch the metrics to Target metrics and then switch again to Analytics-based metric. The report suite should now load.
* If make changes to a test that is already running, you might reset the test and its data. Target allows you to edit a live activity. Be aware that editing an activity that is in progress could reset the test, so reports might not recognize some of the changes. 

  It is safe to make small changes, such as editing existing text or html offers. 

  The specific actions that reset experience names and reports are: 


    * Adding a new location
    * Deleting a location
    * Adding new offers or deleting offers from an exiting location



