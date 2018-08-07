---
description: On a retail site, the highest amount spent by a user during a single visit can predict future shopping behavior.
keywords: Marketing cloud audiences;Shared audiences
seo-description: On a retail site, the highest amount spent by a user during a single visit can predict future shopping behavior.
seo-title: Highest Amount Spent in a Single Order
solution: Target,Analytics,Marketing Cloud
title: Highest Amount Spent in a Single Order
uuid: 7e745ba2-4fe7-42d3-85bc-0a04e5176c51
index: y
internal: n
snippet: y
translate: y
---

# Highest Amount Spent in a Single Order

As a marketer, you might want to test a hypothesis that users who have purchased over $100 are more likely to buy expensive products, so your home page should highlight products with a higher cost.
In the Profile Attributes list, write a script that stores the highest amount spent in a single order.
The following script assumes that the cost for the current order is passed as an mbox parameter named ` orderTotal` in an mbox named ` orderConfirm`. 

```
user.mostSpent 
 
if (mbox.name == 'orderConfirm') { 
 
   var orderTotal = parseInt(mbox.param('orderTotal')); 
 
   if (orderTotal > user.get('mostSpent')) { 
 
      return orderTotal; 
 
   } 
 
}
```

Next, create some expression targets that segment users based on the most they've spent in one visit.

```
zero_spender: 
 
return typeof(user.get('mostSpent')) == 'undefined'; 
 
  
 
low_spender: 
 
return user.get('mostSpent') > 0 &amp;&amp; user.get('amountSpent') < 100; 
 
  
 
medium_spender: 
 
return user.get('mostSpent') >= 100 &amp;&amp; user.get('mostSpent') < 500; 
 
  
 
high_spender: 
return user.get('mostSpent') >= 500;
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
Once the expression targets are created, create a campaign and target the experiences accordingly.
