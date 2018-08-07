---
description: Here are some ideas for leveraging behavioral targeting.
keywords: Marketing cloud audiences;Shared audiences
seo-description: Here are some ideas for leveraging behavioral targeting.
seo-title: Examples and Tips
solution: Target
subtopic: Multivariate Test
title: Examples and Tips
topic: Standard
uuid: bc6a7304-3b8a-4015-b805-edcf9c341742
index: y
internal: n
snippet: y
translate: y
---

# Examples and Tips

## Examples and Tips {#concept_4B15FDC3EA484294886F8BB00B34EACC}Here are some ideas for leveraging behavioral targeting.Some ideas are clickable and describe a potential implementation strategy with [ script profile parameters ](c_target_rules.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2). 

* [ Number of Visits ](c_target_behavioral_examples.md#concept_2F5EFE2725434BB2861545D38F3D40E5) (for example, less than 10, between 10 and 20) 
  Surely, a visitor coming to your site for the 20th time would welcome a different experience from a newer user. You might replace instructional messaging with more advanced content, since they already know their way around your Web site.

* [ Recency of Purchase, Visit, Photo Upload, Etc. ](c_target_behavioral_examples.md#concept_E7B20E1D00E84E2AAA9520F35B6F9A2F) 
  If a month has gone by since a shopper bought a pack of 30-day disposable contact lenses, maybe it's time to offer it at a discount. How about reminding a user who hasn't uploaded a photo to your site in three weeks that their gallery is getting stale?

* [ Frequency ](c_target_behavioral_examples.md#concept_8BCEBA6DFDA54251BE4E833BBA98C1D4) 
  If user intent is demonstrated by action, then repeated action increases confidence in that intent. So why not deliver a different offer to a visitor who has purchased five times rather than once? You can also gain insight by measuring the frequency of certain clicks. For example, clicking repeatedly into a high-heeled shoe category provides information about a user's gender, valuable for targeted content.

* [ New or Returning Visitor ](c_target_behavioral_examples.md#concept_5770B59C5C884CA2BE8554B4AD808EF9) 
  Replace introductory content with something more appropriate for an informed user. Can you "sweeten the deal" if a user hasn't converted the first time?

* [ Active or Passive User ](c_target_behavioral_examples.md#concept_8FFD3C333196441EB0125C69B6D2564F) 
  Imagine that you have a video site like YouTube, where you want to message users who upload videos or post comments on videos differently from users who tend to just watch videos. You can apply this concept to other types of sites as well. For example, does a user participate in your support forums?

* [ Total Amount Purchased ](c_target_behavioral_examples.md#concept_BB18B8B9C1474930BFB460B30B410556) 
  On a retail site, a visitor's lifetime purchase history can predict future shopping behavior. Learn how to target content based on amount spent.

* [ Highest Amount Spent in a Single Order ](c_target_behavioral_examples.md#concept_79EF6AB3EE8645429D735830FF2B6057) 
  On a retail site, the highest amount spent by a user in a single visit can predict future shopping behavior. Online marketers might want to test a hypothesis that big spenders will buy higher priced items if they're highlighted on the landing page.

* [ Time of Day and Day of Week ](c_target_behavioral_examples.md#concept_54D8899EB05B477895EB1309DB164438) 
  Does a visitor behave differently based on the day or time? For example, is behavior different during work hours than after work hours? Or weekday versus weekend?

* Recently viewed products or categories

* Labeling a user based on search history and category selection

>## Number of Visits {#concept_2F5EFE2725434BB2861545D38F3D40E5}You can track the number of times a single visitor visits your site. 
<draft-comment otherprops="merge">
  target/c_target_number_of_visits.xml 
</draft-comment>For a profile attribute, write a script to increment a counter whenever a new session is recognized. You'll then reference the script profile parameter in several expression targeters (target tab), which will be used in the campaign edit page. Here is the script:

```
user.numVisits 
 
if(user.sessionId!=user.getLocal('lastSessionId')) { 
 
   user.setLocal('lastSessionId', user.sessionId); 
 
   return (user.get('numVisits') || 0) + 1; 
 
} 
```

Create five expression targets (you may choose more):

```
0visits: 
return typeof(user.get('numVisits')) == 'undefined'; 
 
1visit: 
return user.get('numVisits') == 1; 
 
2to9visits: 
return user.get('numVisits') > 1 &amp;&amp; user.get('numVisits') < 10; 
 
10to19visits: 
return user.get('numVisits') >= 10 &amp;&amp; user.get('numVisits') < 20; 
 
over20visits: 
return user.get('numVisits') >= 20;
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
>## Recency of Purchase, Visit, Photo Upload, Etc. {#concept_E7B20E1D00E84E2AAA9520F35B6F9A2F}If a month has gone by since a shopper bought a pack of 30-day disposable contact lenses, maybe it's time to offer it at a discount. 
<draft-comment otherprops="merge">
  target/c_target_recency.xml 
</draft-comment>How about reminding a user who hasn't uploaded a photo to your site in three weeks that their gallery is getting stale?
For a profile attribute, write a script that calculates how many days elapsed since the last conversion. A conversion doesn't have to be a purchase. It could be uploading a video, visit to a lead generation form, etc. You'll then reference the script profile parameter in several expression targeters (target tab), which will be used in the campaign edit page. Note that the " ` new Date()`" function brings back time in EDT. Here is the script: 

```
user.recency 
 
if (mbox.name == 'orderThankyouPage') { 
 
   user.setLocal('lastPurchaseTime', new Date().getTime()); 
 
} 
 
if (mbox.name == 'someMbox') { 
 
   var lastPurchaseTime = user.getLocal('lastPurchaseTime'); 
 
   if (lastPurchaseTime) { 
 
      return ((new Date()).getTime()-lastPurchaseTime) / (3600 * 24 * 1000); 
 
   } 
 
}
```

Create some expression targets:

```
no_purchases: 
return typeof(user.get('recency')) == 'undefined'; 
 
within_1day: 
return user.get('recency') < 1; 
 
within_1week: 
return user.get('recency') >= 1 &amp;&amp; user.get('recency') < 7; 
 
within_1month: 
return user.get('recency') >= 7 &amp;&amp; user.get('recency') < 31; 
 
over_1month: 
return user.get('recency') >= 31
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
>## Frequency {#concept_8BCEBA6DFDA54251BE4E833BBA98C1D4}If user intent is demonstrated by action, then repeated action increases confidence in that intent. 
<draft-comment otherprops="merge">
  target/c_target_frequency.xml 
</draft-comment>So why not deliver a different offer to a visitor who has purchased five times rather than once? You can also gain insight by measuring the frequency of certain clicks. For example, clicking repeatedly into a high-heeled shoe category provides information about a user's gender, valuable for targeted content.
In the Profile Attributes list, write a script that increments a counter whenever something notable occurs. This could be:

* A purchase
* Uploading a picture or video
* Clicking on a special category or section of the site
* Using the search box

Here's a script that increments the counter whenever an mbox called ` orderConfirm` is seen: 

```
user.purchaseFrequency 
 
if (mbox.name == 'orderConfirm') { 
 
   return (user.get('purchaseFrequency') || 0) + 1; 
 
} 
```

Create some expression targets:

```
buys_never: 
return typeof(user.get('purchaseFrequency')) == 'undefined'; 
 
buys_sometimes: 
return user.get('purchaseFrequency') > 0 &amp;&amp; user.get('purchaseFrequency') < 3; 
 
buys_often: 
return user.get('purchaseFrequency') >= 3 
```

This one looks for the video upload page in the url:

```
user.uploadFrequency 
 
if (page.url.indexOf('upload_video.html) > -1) { 
 
   return (user.get('uploadFrequency') || 0) + 1; 
 
} 
```

Create some expression targets:

```
uploads_never: 
return user.get('uploadFrequency') == 0; 
 
uploads_sometimes: 
return user.get('uploadFrequency') > 0 &amp;&amp; user.get('uploadFrequency') < 10; 
 
uploads_often: 
return user.get('uploadFrequency') >= 10 
```

These scripts determine a visitor's gender, giving a higher weight to search results than category clicks, since a search term implies heavy intent:

```
user.femaleFrequency 
 
if (page.param('category').indexOf('blouses')) { 
 
   return (user.get('femaleFrequency') || 0) + 1; 
 
} 
 
else if (page.param('search_query').indexOf('blouse')) { 
 
   return (user.get('femaleFrequency') || 0) + 5; 
 
} 
 
user.maleFrequency 
 
if (page.param('category').indexOf('tuxedos')) { 
 
   return (user.get('maleFrequency') || 0) + 1; 
 
} 
 
else if (page.param('search_query').indexOf('tuxedo')) { 
 
   return (user.get('maleFrequency') || 0) + 5; 
 
} 
```

Create expression targets, which use a simple heuristic to determine a visitor's gender.

```
male: 
var maleFrequency = user.get('maleFrequency'); 
return maleFrequency &amp;&amp; maleFrequency > user.get('femaleFrequency') &amp;&amp; maleFrequency > 10; 
 
female: 
var femaleFrequency = user.get('femaleFrequency'); 
return femaleFrequency &amp;&amp; femaleFrequency > user.get('maleFrequency') &amp;&amp; femaleFrequency > 10;
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
>## New or Returning Visitor {#concept_5770B59C5C884CA2BE8554B4AD808EF9}Each visitor is counted as either a new or returning visitor. 
<draft-comment otherprops="merge">
  target/c_target_visitor.xml 
</draft-comment>A visitor is included in the "Visitor: New" segment if it is the visitor's first time visiting the site, the first time since clearing cookies, or if the visitor's profile lifetime has expired since their last visit. For information about profile lifetime, see [ Visitor Profile Lifetime ](c_target_rules.md#concept_D9F21B416F1F49159F03036BA2DD54FD). 
The visitor is included in the "Visitor: Returning" segment if the user previously visited the site, left for at least 30 minutes, and returned to the site again with the same cookies. As long as a visitor returns within their profile lifetime, they will be a returning visitor.
If these two segments are applied to an activity, the "new visitor" segment and the "return visitor" segment do not always add up to the total number of visitors. A visitor can be counted as new, and then return and get counted as a return visitor. That visitor is still counted as only a single visitor in the activity's overall visitor count.

>## Active or Passive User {#concept_8FFD3C333196441EB0125C69B6D2564F}Imagine that you have a video site like YouTube, where you want to message active users who upload videos or post comments on videos differently from passive users who tend to just watch videos. You can apply this concept to other types of sites as well, such as whether a user participates in your support forums. 
<draft-comment otherprops="merge">
  target/c_target_active_passive_user.xml 
</draft-comment>In the profile page, write some scripts that capture the behaviors describing a visitor's engagement. For example, if you run a video upload site, you may opt to watch the number of video uploads, comments and video views for a user, and classify users with a higher ratio of uploads and comments to video views as "active users."
Here are the scripts:


<table id="table_B730D8C286AC4B15968A61EAFE0B5BA4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <codeblock class="syntax html">
       user.numUploads 
       
      if&nbsp;(page.url.indexOf('upload_video')&nbsp;&gt;&nbsp;-1)&nbsp;{ 
       
      &nbsp;&nbsp;&nbsp;return&nbsp;(user.get('numUploads')&nbsp;||&nbsp;0)&nbsp;+&nbsp;1; 
       
      } 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>



<table id="table_9974A76B270F44F1903F915DB9D2F848"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <codeblock class="syntax html">
       user.numComments 
       
      if&nbsp;(page.url.indexOf('add_comment')&nbsp;&gt;&nbsp;-1)&nbsp;{ 
       
      &nbsp;&nbsp;&nbsp;return&nbsp;(user.get('numComments')&nbsp;||&nbsp;0)&nbsp;+&nbsp;1; 
       
      } 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>



<table id="table_F5108782A74547C5869DD6167B98B9FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <codeblock class="syntax html">
       user.numViews 
       
      if&nbsp;(page.url.indexOf('view_video')&nbsp;&gt;&nbsp;-1)&nbsp;{ 
       
      &nbsp;&nbsp;&nbsp;return&nbsp;(user.get('numViews')&nbsp;||&nbsp;0)&nbsp;+&nbsp;1; 
       
      } 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

The above scripts assume that the url contains descriptive names like ` upload_video`, ` add_comment`and ` view_video`, but these events are recognized in other ways if not available in your urls, for example as mbox parameters. 
Next, create some expression targets that use the values in the above profile scripts (think of them as Lego blocks). Note how extra weight is given to uploads and comments (multiplying by 25 and 5, respectively) to determine whether a visitor is active or passive.

```
active_user: 
return (25 * user.get('numUploads') + 5 * user.get('numComments') - user.get('numViews') > 0) ; 
 
passive_user: 
return (25 * user.get('numUploads') + 5 * user.get('numComments') - user.get('numViews') <= 0) ; 
```

Now ` active_user` and ` passive_user` can be used for campaign or experience level targeting. 
For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
>## Total Amount Purchased {#concept_BB18B8B9C1474930BFB460B30B410556}On a retail site, a visitor's lifetime purchase history can predict future shopping behavior. As a marketer, you might have a hypothesis that users who have purchased over $200 are more likely to buy products in the future, so your homepage should highlight higher margin products. 
<draft-comment otherprops="merge">
  target/c_target_total_amount.xml 
</draft-comment>Select ** ` Segments` ** > ** ` Profiles` **. Write a script that calculates a user's total lifetime amount spent by adding the new order total on the order confirm page. 
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
>## Highest Amount Spent in a Single Order {#concept_79EF6AB3EE8645429D735830FF2B6057}On a retail site, the highest amount spent by a user during a single visit can predict future shopping behavior. 
<draft-comment otherprops="merge">
  target/c_target_highest_amount.xml 
</draft-comment>As a marketer, you might want to test a hypothesis that users who have purchased over $100 are more likely to buy expensive products, so your home page should highlight products with a higher cost.
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
>## Time of Day and Day of Week {#concept_54D8899EB05B477895EB1309DB164438}Does a visitor behave differently based on the day or time? For example, is behavior different during work hours than after work hours? 
<draft-comment otherprops="merge">
  target/c_target_time_and_day.xml 
</draft-comment>Select ** ` Segments` ** > ** ` Expression Targets` **, then write a script that examines the day and time. In order to use the visitor's local time, use the special * ` profile.browserTime` * variable. Note that this requires ` mbox.js` version 36 or later. Here is the strategy for work hours versus after work hours, but you can modify for your unique situation: 
Create two expression targets:
**work_hours (eg. M-F 9am-6pm):** 

```
var today = profile.browserTime; 
 
var hour = today.getHours(); 
 
var day = today.getDay(); 
 
return (day >= 1) &amp;&amp; (day <= 5) &amp;&amp; (hour >= 9) &amp;&amp; (hour <= 17);
```

**after_work:** 

```
var today = profile.browserTime; 
 
var hour = today.getHours(); 
 
var day = today.getDay(); 
 
return !((day >= 1) &amp;&amp; (day <= 5) &amp;&amp; (hour >= 9) &amp;&amp; (hour <= 17));
```

If you're not concerned with the visitor's local time, instantiate a JavaScript Date object instead. In this case, you will be using the Target server local time, which is EST, so adjust your times appropriately:
**work_hours (eg. M-F 9am-6pm):** 

```
var today = new Date(); 
 
var hour = today.getHours(); 
 
var day = today.getDay(); 
 
return (day >= 1) &amp;&amp; (day <= 5) &amp;&amp; (hour >= 9) &amp;&amp; (hour <= 17);
```

**after_work:** 

```
var today = new Date(); 
 
var hour = today.getHours(); 
 
var day = today.getDay(); 
 
return !((day >= 1) &amp;&amp; (day <= 5) &amp;&amp; (hour >= 9) &amp;&amp; (hour <= 17));
```

For more information, see the [ JavaScript Expression Cheat Sheet (PDF) ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf). 
Once the expression targets are created, create a campaign and target the experiences accordingly. Note that you should use an experience targeting activity ("landing page campaign" in Target Classic) if your intention is for visitors to switch experiences based on the time. Otherwise, they won't switch to the ` after_work` experience if they're already in the ` work_hours` experience. 
