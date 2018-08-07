---
description: On a retail site, a visitor's lifetime purchase history can predict future shopping behavior. As a marketer, you might have a hypothesis that users who have purchased over $200 are more likely to buy products in the future, so your homepage should highlight higher margin products.
seo-description: On a retail site, a visitor's lifetime purchase history can predict future shopping behavior. As a marketer, you might have a hypothesis that users who have purchased over $200 are more likely to buy products in the future, so your homepage should highlight higher margin products.
seo-title: Total Amount Purchased
solution: Target
subtopic: Multivariate Test
title: Total Amount Purchased
topic: Standard
uuid: 99784688-999c-4286-a8d3-a02bf93a473d
index: y
internal: n
snippet: y
translate: y
---

# Total Amount Purchased

Select ** ` Segments` ** > ** ` Profiles` **. Write a script that calculates a user's total lifetime amount spent by adding the new order total on the order confirm page. 
The following script assumes that the amount for the current order is passed as an mbox parameter named ` orderTotal`: 

```
user.amountSpent 
 
if (mbox.name == 'orderConfirm') { 
 
   return (user.get('amountSpent') || 0) + parseInt(mbox.param('orderTotal')); 
 
}
```

Next, create some expression targets that segment users based on their total amount purchased. In this example, we categorize users as zero, low, medium, and high spenders.

```
zero_spender: 
return typeof(user.get('amountSpent')) == 'undefined'; 
 
low_spender: 
return user.get('amountSpent') > 0 &amp;&amp; user.get('amountSpent') < 100; 
 
medium_spender: 
return user.get('amountSpent') >= 100 &amp;&amp; user.get('amountSpent') < 500; 
 
high_spender: 
return user.get('amountSpent') >= 500;
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
Once the expression targets are created, create a campaign and target the experiences accordingly.
