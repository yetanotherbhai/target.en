---
description: This topic contains suggestions for resolving some issues that might occur when designing an MVT test.
keywords: Mobile Web Experience Editor
seo-description: This topic contains suggestions for resolving some issues that might occur when designing an MVT test.
seo-title: Troubleshoot Multivariate Tests
solution: Target
subtopic: Mobile Viewports
title: Troubleshoot Multivariate Tests
topic: Standard
uuid: eb42f3b9-ddc0-430e-95a7-f6f1e88d4cab
index: y
internal: n
snippet: y
---

# Troubleshoot Multivariate Tests

This topic contains suggestions for resolving some issues that might occur when designing an MVT test.

* When editing an activity, if you used Analytics-based metrics and the report suite doesn't load (spinner displays), switch the metrics to Target metrics and then switch again to Analytics-based metric. The report suite should now load. 
* If make changes to a test that is already running, you might reset the test and its data.

  Target allows you to edit a live activity. Be aware that editing an activity that is in progress could reset the test, so reports might not recognize some of the changes.

  It is safe to make small changes, such as editing existing text or html offers.

  The specific actions that reset experience names and reports are:

    * Adding a new location 
    * Deleting a location 
    * Adding new offers or deleting offers from an exiting location

