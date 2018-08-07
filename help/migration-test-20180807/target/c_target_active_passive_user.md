---
description: Imagine that you have a video site like YouTube, where you want to message active users who upload videos or post comments on videos differently from passive users who tend to just watch videos. You can apply this concept to other types of sites as well, such as whether a user participates in your support forums.
seo-description: Imagine that you have a video site like YouTube, where you want to message active users who upload videos or post comments on videos differently from passive users who tend to just watch videos. You can apply this concept to other types of sites as well, such as whether a user participates in your support forums.
seo-title: Active or Passive User
solution: Target
title: Active or Passive User
topic: Standard
uuid: 9fc23cf6-3265-41be-91e8-d84c61fc9b4f
index: y
internal: n
snippet: y
translate: y
---

# Active or Passive User

In the profile page, write some scripts that capture the behaviors describing a visitor's engagement. For example, if you run a video upload site, you may opt to watch the number of video uploads, comments and video views for a user, and classify users with a higher ratio of uploads and comments to video views as "active users."
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
