---
description: Before you can use a redirector, you must create it.
keywords: Implementation;mbox.js non javascript;redirector
seo-description: Before you can use a redirector, you must create it.
seo-title: Create a Redirector
solution: Target
subtopic: Getting Started
title: Create a Redirector
topic: Standard
uuid: 7248eff0-b5a2-4086-8e25-e49a1ecd9763
index: y
internal: n
snippet: y
translate: y
---

# Create a Redirector


>1. Determine the ad's destination variations, including the default destination.
>1. Create the Redirector URL.

>    
>       ```
>       http://<your_testandtarget_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456
>       &amp;mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm
>       ```



>    <table id="table_DD29523C6FB54061B40AD2B07AE8EDAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Where</th> 
   <th colname="col2" class="entry">Is</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>yourclientcode</p> </td> 
   <td colname="col2"> <p>Your company's client code.</p> <p><b>at.js:</b>Your client code is available at the top of the Setup &gt; Implementation &gt; Edit at.js Settings page of the Target interface. </p> <p><b>mbox.js:</b>Your client code is available at the top of the Setup &gt; Implementation &gt; Edit Mbox.js Settings page. </p> <p>Your company's client code is all lower case and has no special characters.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>redirectorlink_456</p> </td> 
   <td colname="col2"> <p>The name of the Redirector mbox that appears in your account to use in campaigns and tests.</p> <p class="- topic/p ">Redirectors function differently from other mboxes, but appear just as any other mbox in your account. Name the redirector so it is easily distinguished them from the standard type mboxes in your account.</p> <p class="- topic/p ">As best practice, begin the mbox name with<span class="+ topic/ph pr-d/codeph codeph">'redirectorlink'</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm</p> </td> 
   <td colname="col2"> <p>The default destination.</p> <p class="- topic/p ">This must be URL encoded and must be an absolute reference.</p> <p class="- topic/p ">Tip:<span class="+ topic/ph sw-d/filepath filepath">http://www.w3schools.com/tags/ref_urlencode.asp</span> quickly encodes your URLs. </p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Validate the Redirector.
>   >1. Insert the Redirector URL into a browser and refresh.
>   >1. Log in to your account, refresh your mbox list and verify the new Redirector is listed as an mbox.
>1. If you will test different destinations for one ad, create [Redirect Offers](t_redirect_offer.md#task_9578678D42784F5EB9638F8AC8C911FA) for each version.
>1. Create the campaign.

>       See [Non-JavaScript-Based Implementations](c_non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) for the right setup to meet your goals. 
>1. Complete QA on the campaign.

>       Create a dummy page with an `<a href>` containing the Redirector URL. Example: 
>    
>       ```
>       <a href=http://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=
>       
>       redirectorlink_456&amp;mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2F​usualdestination%2Ehtm>
>       ```

>1. Verify that all experiences, default content, and reports act as expected on all browser types, for all of your environments.


>       >[!NOTE] {class="- topic/note "}
>       >
>       >
>       >* Redirectors are not supported by Offer Preview or Browse for mbox. Preview experiences directly in a browser.

>       >* `mboxDebug` does not work with Redirectors . 




>1. Submit the full Redirector URL to your Display Ad Network as the ad destination.
