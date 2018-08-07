---
description: Use a redirector to pass the revenue per click.
keywords: Implementation;mbox.js non javascript;redirector;revenue per click
seo-description: Use a redirector to pass the revenue per click.
seo-title: Revenue Per Click
solution: Target
subtopic: Getting Started
title: Revenue Per Click
topic: Standard
uuid: 070f749a-570f-40bd-9245-9175566608a9
index: y
internal: n
snippet: y
translate: y
---

# Revenue Per Click


>[!NOTE]
>
>Best practice is to determine the revenue value using the**Score per visit** engagement metric, as described in [Engagement](https://marketing.adobe.com/resources/help/en_US/tnt/help/c_Capturing_Engagement.html). 


Add `&amp;mboxPageValue=value` to the URL. 
Example: For a .10 cents revenue per click.

```
http://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456
&amp;mboxPageValue=0.1​&amp;mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```

