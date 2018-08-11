---
description: Best practices for managing and troubleshooting hosts in Adobe Target.
keywords: host;hosts;host group;environment;troubleshooting;best practices
seo-description: Best practices for managing and troubleshooting hosts in Adobe Target.
seo-title: Troubleshooting Hosts
solution: Target
title: Troubleshooting Hosts
topic: Standard
uuid: c9f287c4-6cb5-4f3c-bdc8-af27b4548b40
index: y
internal: n
snippet: y
translate: y
---

# Troubleshooting Hosts

Try the following troubleshooting tips if you experience problems with your hosts: 

**Host does not appear in mbox list for your account.** 


* Refresh the [!UICONTROL  Hosts] page in your browser. 

* Confirm that the mbox code is correct, including the [!DNL  mbox.js] reference. 

* Try browsing to one of the mboxes on the host. It's possible that no mbox on the host was ever rendered in a browser. 



**Random or unknown domains appear in the [!UICONTROL  Host] list.** 

A domain appears in this list if a call to [!DNL  Target] is made from the domain. Often, you could see domains from spider engines, language translator sites, or local disk drives. If the listed domain is not one your team uses, you can click [!UICONTROL  Delete] to remove it. 

**My mbox call returns /* no display - unauthorized mbox host */.** 

If an mbox call is made on an unauthorized host, the call will respond with /* no display - unauthorized mbox host */. 
