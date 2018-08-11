---
description: Organize your sites and pre-production environments for easy management and separated reporting.
keywords: host;hosts;host group;environment
seo-description: Organize your sites and pre-production environments for easy management and separated reporting.
seo-title: Hosts
solution: Target
title: Hosts
topic: Standard
uuid: dd97ffe6-5eb8-49dc-a00a-53a0e25cd374
index: y
internal: n
snippet: y
translate: y
---

# Hosts

Similar functionality existed in [!DNL  Target Classic]. Host groups in [!DNL  Target Classic] were called "environments" in [!DNL  Target Standard/Premium]. 

The primary goal of host management is to ensure that no inactive content accidentally appears on websites. Host management also lets you separate report data by environment. 

A host is any web server (or web domain) from where you serve content during any stage of your project. Any host serving an mbox is recognized. 

Hosts are bundled into environments for ease of management. For example, you might have dozens of hosts grouped in two or three environments. The preset environments include Production, Staging, and Development. You can add new environments and rename your environments, if desired. 

One environment, the default environment, is pre-named Production. This default environment cannot be deleted, even if you rename it. [!DNL  Target] assumes that this is where you will serve final, approved activities and tests. 

When an mbox request is received from new websites or domains, these new domains always appear in the Production environment. The Production environment cannot have its settings changed, so unknown or new sites are guaranteed to see only content that is active and ready. Host management also lets you easily ensure the quality of new activities and content in your test, staging, and development environments before you activate the activities. 

Target does not limit a host that can send and receive mboxes, so when new servers or domains come up, they automatically work (unless you've set up a whitelist or blacklist). This also enables ad testing on different domains you don't know or can't anticipate. 

To manage hosts and environments, click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Hosts] **. 

![](../assets/hosts_list.png) 
