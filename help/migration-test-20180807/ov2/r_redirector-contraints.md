---
description: There are some constraints on the use of a redirector.
keywords: Implementation;mbox.js non javascript;redirector
seo-description: There are some constraints on the use of a redirector.
seo-title: Redirector Constraints
solution: Target
subtopic: Getting Started
title: Redirector Constraints
topic: Standard
uuid: 368daba8-1579-48b6-9715-ffc251bf42a1
index: y
internal: n
snippet: y
translate: y
---

# Redirector Constraints



* There is no client-side timeout as with standard mboxes. If Target is ever completely down (almost never) a visitor cannot click to your destination.

* Third-party cookies are used to track the clicks on the ad. If the PCIds are different, by default Test&amp;Target merges the visitor's third party with any existing first party profiles.

* To use first-party cookies to track ad clicks, pass the mbox session in the URL. Talk to your account representative to do this.


