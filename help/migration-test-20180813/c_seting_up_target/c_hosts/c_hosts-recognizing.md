---
description: Information about the conditions that must be met for Target to recognize a host and add it to the Hosts list.
keywords: host;hosts;host group;environment
seo-description: Information about the conditions that must be met for Target to recognize a host and add it to the Hosts list.
seo-title: Recognizing Hosts
solution: Target
title: Recognizing Hosts
topic: Standard
uuid: 69e46bd7-3db2-4d7a-896a-f110b17516f3
index: y
internal: n
snippet: y
translate: y
---

# Recognizing Hosts

To recognize a host, the following conditions must be met: 


* At least one mbox must exist on the host
* A page on the host must have the following: 
    * An accurate [!DNL  mbox.js] reference
    * An mbox or an auto-generated global mbox call

* The page with the mbox must be viewed in a browser


After the page is viewed, the host is listed in the [!UICONTROL  Hosts] list, allowing you to manage it in an environment as well as preview and launch activities and tests. 


>[!NOTE] {class="- topic/note "}
>
>This includes any personal development servers.



After a host is added to the [!UICONTROL  Host] list, make sure that the host is recognized. 


1. Click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Hosts] **. 

1. If your host is not listed, refresh your browser. 
   By default, a newly recognized host is placed in the Production environment. This is the safest environment because it does not allow inactive activities to be viewed from these hosts.
1. (Conditional) Move the host into the Development or Staging environment. 




>[!NOTE]
>
>The Production environment cannot be deleted, even if you rename it. It is assumed that this is where you will serve final, active activities and tests. The default environment does not allow inactive campaigns to be viewed.


