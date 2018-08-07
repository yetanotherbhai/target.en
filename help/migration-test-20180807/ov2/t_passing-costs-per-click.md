---
description: Use a redirector to pass the costs per click.
keywords: Implementation;mbox.js non javascript;redirector;costs per click
seo-description: Use a redirector to pass the costs per click.
seo-title: Costs Per Click
solution: Target
subtopic: Getting Started
title: Costs Per Click
topic: Standard
uuid: 4c91f43f-50da-40d2-bbb5-bfc5ad93e68e
index: y
internal: n
snippet: y
translate: y
---

# Costs Per Click


>[!NOTE]
>
>Best practice is to determine the cost value using the**Score per visit** engagement metric, as described in [Engagement](https://marketing.adobe.com/resources/help/en_US/tnt/help/c_Capturing_Engagement.html). 


Add `&amp;mboxPageValue=-value` to the URL. Note the negative value. 
Example: For a .10 cents cost per click:

```
http://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456
&amp;mboxPageValue=-0.1&amp;mboxDefault=​http://www.yourcompany.com/usualdestination.htm
```

