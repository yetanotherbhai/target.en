---
description: There are some known issues with the current release of Target.
keywords: Recommendations
seo-description: There are some known issues with the current release of Target.
seo-title: Known Issues
solution: Target
title: Known Issues
topic: Premium
uuid: 86dffa79-6051-4ede-8f02-76952cd9b3e1
index: y
internal: n
snippet: y
translate: y
---

# Known Issues



* Unable to support editing on iframes having iframe buster code Proxy cannot bypass contents on an iframe.

* Unable to navigate to pages which do not allow cross-origin loading The website and proxy are on different domains, and the website configuration cannot be modified by proxy code.

* Cannot maintain the page state inside the Visual Experience Composer This occurs when the URL of the saved activity cannot be opened directly but can only be opened after logging in and reaching that page or after filling some prerequisite information. Target does not save the navigations a user makes inside the Visual Experience Composer, except for the final page on which changes are done all other navigation are not saved.

* Some buttons do not work on touch screens running Windows and Chrome. The workaround is to disable touch at `chrome://flags/`. 

* Any metric dependent on conversion metric never converts. This is expected.
  In an activity, once a conversion metric (whether optimization goal or post goal) is converted, the user is released from the experience and the activity is restarted.
  For example, there is an activity with a conversion metric (C1) and an additional metric (A1). A1 is dependent on C1. When a visitor enters the activity for the first time, and the criteria for converting A1 and C1 are not converted, metric A1 is not converted due to the success metric dependency. If the visitor converts C1 and then converts A1, A1 is still not converted because as soon as C1 is converted, the visitor is released.


