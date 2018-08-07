---
description: Best practices for managing and troubleshooting hosts in Adobe Target.
keywords: host;hosts;host group;environment;troubleshooting;best practices
seo-description: Best practices for managing and troubleshooting hosts in Adobe Target.
seo-title: Troubleshooting Hosts
solution: Target
title: Troubleshooting Hosts
topic: Standard
uuid: 62b9ba09-32b7-41aa-9c3f-ea482cd56b2a
index: y
internal: n
snippet: y
translate: y
---

# Troubleshooting Hosts

Try the following troubleshooting tips if you experience problems with your hosts:
**Host does not appear in mbox list for your account.** 

* Refresh the `Hosts` page in your browser. 

* Confirm that the mbox code is correct, including the `mbox.js` reference. 

* Try browsing to one of the mboxes on the host. It's possible that no mbox on the host was ever rendered in a browser.


**Random or unknown domains appear in the `Host` list.** 
A domain appears in this list if a call to `Target` is made from the domain. Often, you could see domains from spider engines, language translator sites, or local disk drives. If the listed domain is not one your team uses, you can click `Delete` to remove it. 
**My mbox call returns /* no display - unauthorized mbox host */.** 
If an mbox call is made on an unauthorized host, the call will respond with /* no display - unauthorized mbox host */.
