---
description: Information about implementing Target in non-JavaScript scenarios, such as using an AdBox or Redirector.
keywords: Implementation;mbox.js non javascript;redirector;costs per click;revenue per click
seo-description: Information about implementing Target in non-JavaScript scenarios, such as using an AdBox or Redirector.
seo-title: Non-JavaScript-Based Implementations
solution: Target
subtopic: Getting Started
title: Non-JavaScript-Based Implementations
topic: Standard
uuid: 08f7b393-d690-442d-939b-fa40b2b8c8af
index: y
internal: n
snippet: y
translate: y
---

# Non-JavaScript-Based Implementations

## Non-JavaScript-Based Implementations {#concept_4799C58B081A43F6B3B8CC25A8D5D7C4}Information about implementing Target in non-JavaScript scenarios, such as using an AdBox or Redirector.You can track visits to ads and other offsite content. You can also identify the same user on and off your site and deliver a consistent experience throughout their web experience. Using a single URL, the AdBox allows testing without JavaScript or [!DNL  at.js] or [!DNL  mbox.js]. 

An AdBox is useful for sites that do not have [!DNL  at.js] or [!DNL  mbox.js], such as affiliates. If your activity needs dynamic creative (for example, you need to show a product in the ad that was abandoned in the cart), you cannot use an AdBox. 

AdBox ads and Redirector can be used with any kind of activity. The following table compares Adbox and Redirector, and when to use each: 



<table id="table_0FCE44A165574C609FF7F94A7DDF8926"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Purpose </th> 
   <th colname="col3" class="entry"> When To Use </th> 
   <th colname="col4" class="entry"> URL Structure </th> 
   <th colname="col5" class="entry"> Offer Type </th> 
   <th colname="col6" class="entry"> Offer Content </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>AdBox </p> </td> 
   <td colname="col2"> <p>Returns different images to the ad </p> </td> 
   <td colname="col3"> <p>To change the content of an ad </p> </td> 
   <td colname="col4"> <p> <span class="codeph"> clientcode​.tt.​omtrdc​.net/​m2​/​ clientcode/ubox/​ image? </span> </p> </td> 
   <td colname="col5"> <p>redirect offer </p> </td> 
   <td colname="col6"> <p>URL for an image </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Redirector </p> </td> 
   <td colname="col2"> <p>Redirects a visitor to a different web page </p> </td> 
   <td colname="col3"> <p>To change the landing page of an ad </p> </td> 
   <td colname="col4"> <p> <span class="codeph">  clientcode​.tt.omtrdc.net/​m2/ clientcode​/ubox/ page? </span> </p> </td> 
   <td colname="col5"> <p>redirect offer </p> </td> 
   <td colname="col6"> <p>URL for a page </p> </td> 
  </tr> 
 </tbody> 
</table>

The following sections contain more information: 


* [ Constraints ](c_non-javascript-based-implementation.md#section_38F559DCF1324271926608BCD4AB1227)


## Constraints {#section_38F559DCF1324271926608BCD4AB1227}


* There is no client-side timeout as with standard mboxes. If Target is completely down, visitors to the ad will not see content, not even default. 

* 3rd-party cookies are used to track the visits. If the PCIds are different, by default the visitor's 3rd party is merged with any existing 1st-party profiles. 

* To use 1st-party cookies on the AdBox itself, you will need to pass the mBox session in the URL. Talk to your account representative to do this. 

* To use 1st-party cookies to track ad clicks, pass the mbox session in the URL. Talk to your account representative to do this. 

* To use more than one AdBox on the same page, you must pass the Mbox session in the URL. Talk to your account representative to do this. You might have one AdBox and one Redirector link on the same page (because the Redirector is actually on a second page). 


>## Create an Adbox for an Image {#task_24C59DF05D454066BC33D9FCC4A841D9}Use an AdBox to deliver images in an off-site implementation. 
<draft-comment otherprops="merge">
  ov2/t_testing-content-with-the-adbox.xml 
</draft-comment>An AdBox is like an mbox, but it is controlled by a URL rather than JavaScript. AdBoxes are created with a special AdBox URL that loads an "ad" mbox (or AdBox) into your Adobe account. Use this AdBox in place of the mbox in your activities. Use the AdBox URL instead of a direct image reference in email or other non-JavaScript implementations. 

For help selecting the right setup see [ Non-JavaScript-Based Implementations ](c_non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4). 

>1. Create the AdBox URL:

>       ` http:// myClientCode​.tt.omtrdc.net​/m2/​ ​myClientCode/​ubox/ image​?mbox= emailHeroImage123_320x200​&amp;mboxDefault=​ ​http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2F​img%2F​logo%2Egif` 



>    <table id="table_DD29523C6FB54061B40AD2B07AE8EDAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Where </th> 
   <th colname="col2" class="entry"> Is </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>myClientCode </p> </td> 
   <td colname="col2"> <p>Your company's client code. </p> <p><b>at.js: </b>Your client code is available at the top of the Setup &gt; Implementation &gt; Edit at.js Settings page of the Target interface. </p> <p><b>mbox.js: </b>Your client code is available at the top of the Setup &gt; Implementation &gt; Edit Mbox.js Settings page. </p> <p>Your company's client code is all lower case and has no special characters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>image </p> </td> 
   <td colname="col2"> <p>The call type. In this case it is an image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>emailHeroImage123_320x200 </p> </td> 
   <td colname="col2"> <p>The name of the AdBox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif </p> </td> 
   <td colname="col2"> <p>The mbox's default content. This must be an image. </p> <p class="- topic/p ">This must be URL encoded and must be an absolute reference. </p> <p class="- topic/p ">Tip: <span class="+ topic/ph sw-d/filepath filepath"> http://www.w3schools.com/tags/ref_urlencode.asp </span> quickly encodes your URLs. </p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Create [ Redirect Offers ](c_manage_content.md#task_33C80CD722564303B687948261484F94) for each alternative image.


>       >[!NOTE] {class="- topic/note "}
>       >
>       >AdBoxes must be loaded with a Redirect Offer or the default content offer. Other offers types will not work. Because the AdBox is a URL, it can only display the URLs it receives, so only the Redirect Offer works.

>1. Create the activity.

>       See [ Non-JavaScript-Based Implementations ](c_non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) for the right set up to meet your goals. 
>1. Complete QA on the activity.

>1. Launch the activity.
>## Test an Email Image Adbox {#task_47D47E16051D4EF398D91FD84C07645D}Dynamically test images in email, and even change those images on the fly when someone opens the email. 
<draft-comment otherprops="merge">
  target/t_testing-email-image-adbox.xml 
</draft-comment>Redirectors can be used in emails to track clicks and dynamically control which landing page people reach. 

Email image testing is achieved through using modified versions of adboxes. Because email clients do not allow cookies to be set, a unique identifier must be generated for each email. This number is appended to the adbox URL and to any redirectors used in the email to track clicks from the email. 

**Sample code for an email image adbox:** 


```
<img src="http://< 
<b class="+ topic ph hi-d="" b "="">
  clientcode>.tt.omtrdc.net/m2/​ 
 <b class="+ topic ph hi-d="" b "="">
   clientcode/ubox/​ 
  <b class="+ topic ph hi-d="" b "="">
    image?mbox=​ 
   <b class="+ topic ph hi-d="" b "="">
     email_Header&amp;mboxDefault=​ 
    <b class="+ topic ph hi-d="" b "="">
      http%3A%2F%2Fwww.domain.com%2Fheader.jpg&amp;​  
          
     <b class="+ topic ph hi-d="" b "="">
       mboxXDomain=disabled&amp;​ 
      <b class="+ topic ph hi-d="" b "="">
        mboxSession=123456&amp;​ 
       <b class="+ topic ph hi-d="" b "="">
         mboxPC=123456" border="0" >  
              
           
       </b class="+ topic> 
      </b class="+ topic> 
     </b class="+ topic> 
    </b class="+ topic> 
   </b class="+ topic> 
  </b class="+ topic> 
 </b class="+ topic> 
</b class="+ topic>
```


Where the bold values are specific to you: 



<table id="table_13516D41801B4E58AC6E7724DF168C7B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Value </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>clientcode </p> </td> 
   <td colname="col2"> <p>Your company's client code. Find this in your <span class="codeph"> at.js </span> or <span class="codeph"> mbox.js </span> listed as <span class="codeph"> clientCode='yourclientcode' </span>. This is all lower case and has no special characters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>image </p> </td> 
   <td colname="col2"> <p> The offer type. It is always "image" for graphic ads and "page" for redirectors. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>email_header </p> </td> 
   <td colname="col2"> <p>The name of the adbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>http%3A%2F%2Fwww.domain.com%2Fheader.jpg </p> </td> 
   <td colname="col2"> <p>The adbox's default content. This must be an absolute reference and must be URL encoded. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxXDomain=disabled </p> </td> 
   <td colname="col2"> <p> Tells <span class="keyword"> Target </span> to not attempt to set a cookie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mboxSession=123456 and mboxPC=123456 </p> </td> 
   <td colname="col2"> <p>Two values required by <span class="keyword"> Target </span> to merge this user's profile with the existing profile for your site. 123456 is the unique identifier generated per email. Dynamically insert this value into every adbox and redirector URL. This number must be unique for each email sent to each person. If a weekly email is sent to 1,000 people, 1,000 unique IDs need to be generated. </p> <p class="- topic/p ">The unique identifier per email needs to be assigned to the <span class="+ topic/ph pr-d/codeph codeph"> mboxSession </span> and <span class="+ topic/ph pr-d/codeph codeph"> mboxPC </span> in each adbox and redirector URL. The recommended format for this identifier is <span class="+ topic/ph pr-d/codeph codeph"> timestamp-NNNNN </span> where <span class="+ topic/keyword sw-d/varname varname"> NNNNN </span> is a random 5-digit number, but any alphanumeric format will work. Some mass e-mail services and any programming language are capable of generating this unique identifier. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Working with Redirectors {#concept_D5EF059F4DC94C67A8B684C9F9910EE4}Use a Redirector similarly to how you use an mbox in your tests. 
<draft-comment otherprops="merge">
  ov2/c_working-with-redirectors.xml 
</draft-comment>Redirectors are created with a special Redirector URL that loads a Redirector mbox (Redirector) into your account. Use this Redirector similarly to how you use an mbox in your tests. Submit the Redirector URL to your Ad Network as the ad's destination link. 

Use the Redirector to do the following: 


* Track clicks from your display ads to your site 

* Create a single centralized report to track clicks to display ads on multiple ad networks 

* Vary display ad destinations 

  For example the same banner lands on your home page, category page and product page. 

* Find which landing page leads to the most conversions 



For help deciding the right setup see [ Non-JavaScript-Based Implementations ](c_non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4). 
>## Create a Redirector {#task_76608B0F73FC45C4A9F125B894DCF821}Before you can use a redirector, you must create it. 
<draft-comment otherprops="merge">
  ov2/t_creating-a-redirector.xml 
</draft-comment>
>1. Determine the ad's destination variations, including the default destination.
>1. Create the Redirector URL.

>    
>       ```
>       http://<your_testandtarget_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456 
>       &amp;mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm
>       ```




>    <table id="table_79DC24DC68C54DFE907F4A0652DEA18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Where </th> 
   <th colname="col2" class="entry"> Is </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>yourclientcode </p> </td> 
   <td colname="col2"> <p>Your company's client code. </p> <p><b>at.js: </b>Your client code is available at the top of the Setup &gt; Implementation &gt; Edit at.js Settings page of the Target interface. </p> <p><b>mbox.js: </b>Your client code is available at the top of the Setup &gt; Implementation &gt; Edit Mbox.js Settings page. </p> <p>Your company's client code is all lower case and has no special characters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>redirectorlink_456 </p> </td> 
   <td colname="col2"> <p>The name of the Redirector mbox that appears in your account to use in campaigns and tests. </p> <p class="- topic/p ">Redirectors function differently from other mboxes, but appear just as any other mbox in your account. Name the redirector so it is easily distinguished them from the standard type mboxes in your account. </p> <p class="- topic/p ">As best practice, begin the mbox name with <span class="+ topic/ph pr-d/codeph codeph"> 'redirectorlink' </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm </p> </td> 
   <td colname="col2"> <p>The default destination. </p> <p class="- topic/p ">This must be URL encoded and must be an absolute reference. </p> <p class="- topic/p ">Tip: <span class="+ topic/ph sw-d/filepath filepath"> http://www.w3schools.com/tags/ref_urlencode.asp </span> quickly encodes your URLs. </p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Validate the Redirector.
>   >1. Insert the Redirector URL into a browser and refresh.
>   >1. Log in to your account, refresh your mbox list and verify the new Redirector is listed as an mbox.
>1. If you will test different destinations for one ad, create [ Redirect Offers ](t_redirect_offer.md#task_9578678D42784F5EB9638F8AC8C911FA) for each version.
>1. Create the campaign.

>       See [ Non-JavaScript-Based Implementations ](c_non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) for the right setup to meet your goals. 
>1. Complete QA on the campaign.

>       Create a dummy page with an ` &amp;lt;a href&amp;gt;` containing the Redirector URL. Example: 

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

>       >* ` mboxDebug` does not work with Redirectors . 




>1. Submit the full Redirector URL to your Display Ad Network as the ad destination.
>## Use a Redirector to Pass Costs per Click and Revenue Per Click {#concept_3078EF48E9C44B34992D62AAB9628853}Information about using a redirector to pas costs per click and revenue per click. 
<draft-comment otherprops="merge">
  ov2/c_using-a-redirector-to-pass-costs-per-click-and-revenue-per-click.xml 
</draft-comment>
## Passing Costs per Click {#section_DEB889470F7D4360B5CEA85FD05DEDFA}

Use a redirector to pass the costs per click. 


>[!NOTE]
>
>Best practice is to determine the cost value using the**Score per visit** engagement metric, as described in [ Engagement ](https://marketing.adobe.com/resources/help/en_US/tnt/help/c_Capturing_Engagement.html). 



Add ` &amp;amp;mboxPageValue=-value` to the URL. Note the negative value. 

Example: For a .10 cents cost per click: 


```
http://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456 
&amp;mboxPageValue=-0.1&amp;mboxDefault=​http://www.yourcompany.com/usualdestination.htm
```


## Passing Revenue per Click {#section_3E48AC465E7D42DAAC51B4BFF83F64B1}

Use a redirector to pass the revenue per click. 


>[!NOTE]
>
>Best practice is to determine the revenue value using the**Score per visit** engagement metric, as described in [ Engagement ](https://marketing.adobe.com/resources/help/en_US/tnt/help/c_Capturing_Engagement.html). 



Add ` &amp;amp;mboxPageValue=value` to the URL. 

Example: For a .10 cents revenue per click. 


```
http://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456 
&amp;mboxPageValue=0.1​&amp;mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```

