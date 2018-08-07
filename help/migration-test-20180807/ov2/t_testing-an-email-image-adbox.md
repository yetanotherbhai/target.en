---
description: Dynamically test images in email, and even change those images on the fly when someone opens their email.
keywords: Implementation;mbox.js non javascript;mbox;adbox;email
seo-description: Dynamically test images in email, and even change those images on the fly when someone opens their email.
seo-title: Test an Email Image Adbox
solution: Target
subtopic: Getting Started
title: Test an Email Image Adbox
topic: Standard
uuid: 8aebfce0-24de-4017-9617-68ca2b09596c
index: y
internal: n
snippet: y
translate: y
---

# Test an Email Image Adbox

By running a self-optimizing campaign on images in an email, early responders to your email can influence what delayed email openers see in their email. Redirectors can also be used in emails to track clicks and dynamically control which landing page people reach.
Email image testing is achieved through using modified versions of adboxes. Since email clients do not allow cookies to be set, a unique identifier must be generated for each email. This number is appended to the adbox URL and to any redirectors used in the email to track clicks from the email.
[ Download a How-To Document about Email Testing ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/TTemailCampaignSetup.pdf) 
**Sample code for an email image adbox:** 
` <img src="http://< clientcode>.tt.omtrdc.net/m2/​ clientcode/ubox/​ image?mbox=​ email_Header&amp;mboxDefault=​ http%3A%2F%2Fwww.domain.com%2Fheader.jpg&amp;​ mboxXDomain=disabled&amp;​ mboxSession=123456&amp;​ mboxPC=123456" border="0" >` 


<table id="table_DD29523C6FB54061B40AD2B07AE8EDAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Where </th> 
   <th colname="col2" class="entry"> Is </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>clientcode</p> </td> 
   <td colname="col2"> <p>Your company's client code.</p> <p><b>at.js:</b>Your client code is available at the top of the Setup &gt; Implementation &gt; Edit at.js Settings page of the Target interface. </p> <p><b>mbox.js:</b>Your client code is available at the top of the Setup &gt; Implementation &gt; Edit Mbox.js Settings page. </p> <p>Your company's client code is all lower case and has no special characters.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>image</p> </td> 
   <td colname="col2"> <p>The offer type. It is always "image" for graphic ads; it is "page" for redirectors.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>email_header</p> </td> 
   <td colname="col2"> <p>The name of the adbox.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>http%3A%2F%2Fwww.domain.com%2Fheader.jpg</p> </td> 
   <td colname="col2"> <p>The adbox's default content. This must be an absolute reference and must be URL encoded.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxXDomain=disabled</p> </td> 
   <td colname="col2"> <p>Tells Target to not attempt to set a cookie.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxSession=123456 and mboxPC=123456</p> </td> 
   <td colname="col2"> <p>Two values required by Test&amp;Target to merge this user's profile with their existing profile for your site. 123456 is the unique identifier generated per email. Dynamically insert this value into every adbox and redirector URL. This number must be unique for each email sent to each person. If a weekly email is sent to 1,000 people, 1,000 unique IDs need to be generated.</p> <p class="- topic/p ">The unique identifier per email needs to be assigned to the <span class="+ topic/ph pr-d/codeph codeph"> mboxSession </span> and <span class="+ topic/ph pr-d/codeph codeph"> mboxPC </span> in each adbox and redirector URL. The recommended format for this identifier is <span class="+ topic/ph pr-d/codeph codeph"> timestamp-NNNNN </span> where <span class="+ topic/keyword sw-d/varname varname"> NNNNN </span> is a random 5-digit number, but any alphanumeric format will work. Some mass e-mail services and any programming language are capable of generating this unique identifier. </p> </td> 
  </tr> 
 </tbody> 
</table>

