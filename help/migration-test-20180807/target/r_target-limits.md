---
description: Information about the character limits that affect activities and other elements in Adobe Target.
keywords: character limit;limits;built in profiles;maximum;limit;constraint;character;best practice;orderid;orderTotal;mbox3rdPartyID;category;categoryID
seo-description: Information about the character limits that affect activities and other elements in Adobe Target.
seo-title: Character Limits
solution: Target
title: Character Limits
topic: Standard
uuid: a1513ee1-ba00-434e-ae7e-bb0e6ec08474
index: y
internal: n
snippet: y
translate: y
---

# Character Limits


>The limits listed below are recommended limits. When these limits are approached or exceeded, performance can slow. Slow interface load times can also be caused by a very complex activity, such as many audiences, targets, and experiences all in one activity. Highly complex activities should be reviewed with Adobe Consulting and tested in a limited environment before being released to production.


><table id="table_6B409D2807E647019412FE296603032B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Feature</th> 
   <th colname="col02" class="entry">Limit</th> 
   <th colname="col3" class="entry">Comments</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Customer Attribute Name</p> </td> 
   <td colname="col02"> <p>128 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mbox Name</p> </td> 
   <td colname="col02"> <p>250 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mbox Request URLs</p> </td> 
   <td colname="col02"> <p>2,083 characters</p> </td> 
   <td colname="col3"> <p>Due to URL length restrictions in Internet Explorer.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activity Names</p> </td> 
   <td colname="col02"> <p>250 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Names</p> </td> 
   <td colname="col02"> <p>20 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offer Names</p> </td> 
   <td colname="col02"> <p>250 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offer Size</p> </td> 
   <td colname="col02"> <p>256 KB for HTML offers</p> <p>64 KB for visual offers from the UI</p> <p>512 KB from the API</p> </td> 
   <td colname="col3"> <p>If using a global mbox, the limit is for the whole set of content returned for the page. Limiting offer size improves page load times. If the limit is exceeded, the following message appears:</p> <p>"The content for the experience is too large to deliver. Please modify the experience to affect less page code."</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reusable Audiences/Account</p> </td> 
   <td colname="col02"> <p>75 audiences</p> </td> 
   <td colname="col3"> <p>Recommended limit. JavaScript timeouts occur in the interface if you have too many.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>In-Mbox Profile Names</p> </td> 
   <td colname="col02"> <p>128 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>In-Mbox Profiles in an mbox request</p> </td> 
   <td colname="col02"> <p>50 profiles</p> </td> 
   <td colname="col3"> <p>All profiles after 50 are ignored.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Script Profile Names</p> </td> 
   <td colname="col02"> <p>50 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Script Profile Value</p> </td> 
   <td colname="col02"> <p>255 characters</p> </td> 
   <td colname="col3"> <p>255 characters is the maximum limit.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Script Profile input box in the Target UI</p> </td> 
   <td colname="col02"> <p>1,300 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target Names</p> </td> 
   <td colname="col02"> <p>50 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target input box in the Target UI</p> </td> 
   <td colname="col02"> <p>2,000 characters</p> </td> 
   <td colname="col3"> <p>Recommended limit. Depends on the size of the encoded string, which could be much longer than the raw string. If the string is too large, it fails before it gets to Adobe Target.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target Conditions</p> </td> 
   <td colname="col02"> <p>1,000 values</p> </td> 
   <td colname="col3"> <p>Recommended limit. This refers to the number of line-separated values in the targeting text area. For example, entering 1,000 zip codes into a zip code target.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">productPurchasedId</span> parameter </p> </td> 
   <td colname="col02"> <p>47 characters per comma-separated value</p> </td> 
   <td colname="col3"> <p>Anything longer is clipped by the system.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">orderId</span> parameter </p> </td> 
   <td colname="col02"> <p>120 characters</p> </td> 
   <td colname="col3"> <p>Recommended limit.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">orderTotal</span> parameter </p> </td> 
   <td colname="col02"> <p>120 characters</p> </td> 
   <td colname="col3"> <p>Recommended limit.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">mbox3rdPartyId</span> parameter </p> </td> 
   <td colname="col02"> <p>60 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">categoryId</span> parameter </p> </td> 
   <td colname="col02"> <p>250 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">entityID</span> parameter </p> </td> 
   <td colname="col02"> <p>1,000 characters</p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

