---
description: Information about using a redirector to pas costs per click and revenue per click.
keywords: Implementation;mbox.js non javascript;redirector;costs per click;revenue per click
seo-description: Information about using a redirector to pas costs per click and revenue per click.
seo-title: Use a Redirector to Pass Costs per Click and Revenue Per Click
solution: Target
subtopic: Getting Started
title: Use a Redirector to Pass Costs per Click and Revenue Per Click
topic: Standard
uuid: 99357a86-6b7b-41d4-bfd0-c9120867b1f5
index: y
internal: n
snippet: y
translate: y
---

# Use a Redirector to Pass Costs per Click and Revenue Per Click

This section contains the following information:

* [Passing Costs per Click](c_using-a-redirector-to-pass-costs-per-click-and-revenue-per-click.md#section_DEB889470F7D4360B5CEA85FD05DEDFA)
* [Passing Revenue per Click](c_using-a-redirector-to-pass-costs-per-click-and-revenue-per-click.md#section_3E48AC465E7D42DAAC51B4BFF83F64B1)


## Passing Costs per Click {#section_DEB889470F7D4360B5CEA85FD05DEDFA}

Use a redirector to pass the costs per click.

>[!NOTE]
>
>Best practice is to determine the cost value using the**Score per visit** engagement metric, as described in [Engagement](https://marketing.adobe.com/resources/help/en_US/tnt/help/c_Capturing_Engagement.html). 


Add `&amp;mboxPageValue=-value` to the URL. Note the negative value. 
Example: For a .10 cents cost per click:

```
http://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456
&amp;mboxPageValue=-0.1&amp;mboxDefault=​http://www.yourcompany.com/usualdestination.htm
```


## Passing Revenue per Click {#section_3E48AC465E7D42DAAC51B4BFF83F64B1}

Use a redirector to pass the revenue per click.

>[!NOTE]
>
>Best practice is to determine the revenue value using the**Score per visit** engagement metric, as described in [Engagement](https://marketing.adobe.com/resources/help/en_US/tnt/help/c_Capturing_Engagement.html). 


Add `&amp;mboxPageValue=value` to the URL. 
Example: For a .10 cents revenue per click.

```
http://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456
&amp;mboxPageValue=0.1​&amp;mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```

