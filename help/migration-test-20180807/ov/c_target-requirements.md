---
description: Information about the minimum Target library requirements (mbox.js or at.js).
keywords: Overview and Reference;webkit
seo-description: Information about the minimum Target library requirements (mbox.js or at.js).
seo-title: Target Requirements
solution: Target
subtopic: Getting Started
title: Target Requirements
topic: Standard
uuid: 4684a0df-c82b-4d6d-90f1-5f604dd5ee27
index: y
internal: n
snippet: y
translate: y
---

# Target Requirements

## Target Requirements {#concept_8B60C50C0CC24E279FAA4DB7E165F209}Information about the minimum 
<keyword>
 Target
</keyword> library requirements (
<filepath>
 mbox.js
</filepath> or 
<filepath>
 at.js
</filepath>).To implement Target, you need one of the following `Target` libraries: 


<table id="table_C8F7C650B54B46C6AB8D137656CA4840"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Library</th> 
   <th colname="col2" class="entry">Minimum Requirements</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js</p> </td> 
   <td colname="col2"> <p>Version 0.9.3 or later.</p> <p>For more information, see <a href="../ov2/c_target-atjs-implementation.xml#concept_8AC8D169E02944B1A547A0CAD97EAC17" format="dita" scope="local">at.js Implementation</a>. </p> <p>If you want to use redirect offers in activities that use Adobe Analytics as the reporting source (A4T), there are additional minimum requirements your implementation must meet. For more information, see <a href="../a4t/c_a4t-faq-redirect-offers.xml#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local">Redirect Offers - A4T FAQ</a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mbox.js</p> </td> 
   <td colname="col2"> <p>Version 53 or later.</p> <p>Version 58 or later is recommended. If the Marketing Cloud ID Service and Adobe Analytics in Target (A4T) are being used, v58 is the minimum-supported <span class="filepath">mbox.js</span> version. </p> <p>For more information, see <a href="t_mbox_download.xml#task_4EAE26BB84FD4E1D858F411AEDF4B420" format="dita" scope="local">Mbox.js Implementation</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Supported Browsers {#reference_01B4BF99E7D545A7998773202A2F6100}The 
<keyword>
 Adobe Target
</keyword> application and content delivery has been tested across a wide range of browsers and devices. 
<draft-comment otherprops="merge">
 ov/r_supported_browsers.xml
</draft-comment>
## Target Standard/Premium Interface {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

The `Target Standard/Premium` interface supports the following browsers and devices: 


<table id="table_28F120EDC9714B60B315EA1ED0FF6582"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry">Device Type</th> 
   <th colname="col3" class="entry">Browser Version</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2">Windows</td> 
   <td colname="col3"> <p> 
     <ul id="ul_B6F9F5BC38E249ECA5AA512B94082BF9"> 
      <li id="li_5B63829413D24320AB812546794A7934"> <p>Microsoft Internet Explorer 11</p> </li> 
      <li id="li_9441697F249C4AB28E96FC1DC8A27B6F"> <p>Google Chrome (Latest, Latest minus 1)</p> </li> 
      <li id="li_BA8F65110C6643ADA40FB334F61EF36F"> <p>Mozilla Firefox (Latest, Latest minus 1)</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2">Mac</td> 
   <td colname="col3"> <p> 
     <ul id="ul_BE238F7BB80742D98A361A3A9EFA0B05"> 
      <li id="li_B1D1E029963C4DBD8CD05D4E7F3D2395">Firefox (Latest, Latest minus 1)</li> 
      <li id="li_84EA2E024EB34E38AF302974FE7A1CAA">Chrome (Latest, Latest minus 1)</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Content Delivery {#section_1045A946056441268D40025529918D3D}

Content delivery has been tested across the following browsers and devices:


<table id="table_ED385191F8BC44549BF263090688840A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Device Type</th> 
   <th colname="col2" class="entry">Browser Version</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Windows</td> 
   <td colname="col2"> <p> 
     <ul id="ul_86C7D2C185A14DDAA87E0A59B91431B9"> 
      <li id="li_865C65F014044440A800DD2306BD6453"> <p>Internet Explorer 9 and 10. Tested in emulation mode.</p> </li> 
      <li id="li_409DEA504A4A4894B15EAADC7204B8BB"> <p>Internet Explorer 11/Edge</p> </li> 
      <li id="li_91B58BFD0B5C491AB27F5D4241545EE7"> <p>Chrome (Latest, Latest minus 1)</p> </li> 
      <li id="li_E8C5BD70AAA449AE81A43D0AD3F62B56"> <p>Firefox (Latest, Latest minus 1)</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Mac</td> 
   <td colname="col2"> <p> 
     <ul id="ul_550A4C0C8E384C48ADE8C9E38BB3662F"> 
      <li id="li_442E1CE6507146A795B774B8B28F1F3F"> <p>Apple Safari (Latest)</p> <p>For more information about how Safari handles first- and third-party cookies, see <a href="c_cookie_behavior.xml#concept_4D8107E193B64168A3C0B85B51612991" format="dita" scope="local">Target Cookie</a>. </p> </li> 
      <li id="li_81347CC1A29946EF9AFC4BBBEFEBBF74"> <p>Firefox (Latest, Latest minus 1)</p> </li> 
      <li id="li_642DBDCAB3F3423488D790C8D368961A"> <p>Chrome (Latest, Latest minus 1)</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Mobile/Tablet</td> 
   <td colname="col2"> <p> 
     <ul id="ul_4747E73A79234E4E9B1AC1BA805475BB"> 
      <li id="li_75B42139B1F44B14800B752135E72181"> <p>Apple iOS (Latest)</p> </li> 
      <li id="li_F0EB81D5CCD14BF2A00ADC384EE7617A"> <p>Android devices and tablets (Android 4 and later)</p> </li> 
      <li id="li_18E1FF948A3D4869942F2E4DA0791B43"> <p>Microsoft Surface (Windows 8.1)</p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

For `at.js` implementations, Target displays default content in earlier versions of Internet Explorer (versions 8 and earlier) and in earlier versions of the above-listed browsers. For `mbox.js` implementations, Target tries to render content but might not be successful. 
Target displays default content in browsers not listed above and in browsers using [quirks mode](https://en.wikipedia.org/wiki/Quirks_mode). 
>## Target Cookie {#concept_4D8107E193B64168A3C0B85B51612991}The cookie behavior depends on whether it is a first-party cookie, a third-party cookie with a first-party cookie, or a third-party cookie alone. 
<draft-comment otherprops="merge">
 ov/c_cookie_behavior.xml
</draft-comment>
See also [Delete the Target Cookie](https://marketing.adobe.com/resources/help/en_US/target/target/t_cookie_deleting.html). 

## When to Use First- or Third-Party Cookies {#section_F71B29420C004A7FA3B1921E619B326E}

Your site set up determines which cookies you want to use. It is helpful to understand how Target works when trying to understand first and third-party cookies. See [How Adobe Target Works](c_how_target_works.md#concept_459AB4DEE7364A9290C2FD405DC29584) for more information. 
There are three main use cases for cookies:

1. One domain. All of your testing will take place within one top-level domain ( `www.domain.com`, `store.domain.com`, `anysub.domain.com`, etc.). 
   Approach: Use only first-party cookies. This is the default.

1. Users cross domains and you want to track and test their behavior across these domains. Example: A user comes to your site to shop but checks out through Yahoo stores. Three approaches (work with your account representative to determine the best approach):

    * Enable first- and third-party cookies.
    * Enable third-party only (very rare, but has the benefit of keeping the mbox cookie out of your domain).
    * Enable only first-party cookies and pass `mboxSession` parameter when crossing domain. The `mboxSession` parameter must be passed to a landing page with `mbox.js` referenced. It cannot be an intermediate redirector page. 


1. You are only using adboxes or Flashboxes on a third-party site.
   Two approaches (work with your client services manager to determine the best approach):

    * Enable first- and third-party cookies. First- and third-party cookies are required for Flashbox and dynamic creatives.

    * Enable only third-party cookies. This approach is only for the rare case where AdBox implementations are used without on-site targeting.



## First-Party Cookie Behavior {#section_CE6313D979EA4D0897D2F661E7A8AFA7}

The first-party cookie is stored in `clientdomain.com`, where `clientdomain` is your domain. 
`Mbox.js` generates an `mboxSession ID` and stores it in the mbox cookie. The first mbox response contains the offer, as well as the JavaScript to store the `mboxPC ID` generated by the application, in the mbox cookie. 

>[!NOTE]
>
>The `AMCV_###@AdobeOrg` 1st-party cookie is always set with the Marketing Cloud Visitor ID. 


[Top](c_cookie_behavior.md#concept_4D8107E193B64168A3C0B85B51612991) 

## Third-Party Cookie Behavior {#section_4C3A83990BF8415BB1806602D84AED48}

The third-party cookie is stored in `clientcode.tt.omtrdc.net` and the first-party cookie is stored in `clientdomain.com`, where `clientdomain` is your domain. 
`Mbox.js` generates an `mboxSession` ID. The first location request returns HTTP response headers that attempt to set third-party cookies named `mboxSession` and `mboxPC` and a redirect request is sent back with an extra parameter ( `mboxXDomainCheck=true`). 
If the browser accepts third-party cookies, the redirect request includes those cookies, and the offer is returned.
If the browser rejects third-party cookies, the redirect request does not include those cookies, and default content is displayed for all locations on the page. Because there are no cookies set, the same process above happens again on every page request.

>[!NOTE]
>
>The `demdex.net` cookie is set if third-party cookies are not blocked. 



## Third-Party and First-Party Cookie Behavior {#section_F0C9AD8BFDF8457A999C4A07A0F7A981}

The third-party cookie is stored in `clientcode.tt.omtrdc.net` and the first-party cookie is stored in `clientdomain.com`, where `clientdomain` is your domain. 
`Mbox.js` generates an `mboxSession ID`. The first location request returns HTTP response headers that attempt to set third-party cookies named `mboxSession` and `mboxPC`, and a redirect request is sent back with an extra parameter ( `mboxXDomainCheck=true`). 
If the browser accepts third-party cookies, the redirect request includes those cookies, and the offer is returned.
Some browsers reject third-party cookies. If the third-party cookie is blocked, the first-party cookie still works. Target attempts to set the thrid-party cookie, and if it cannot, then Target can only track on the client's specific domain. Cross-domain tracking does not work if the third-party is blocked, unless the `mboxSession` is appended in the link that crosses domains. In this case, another first-party cookie is set and synched with the prior domain's first-party cookie. 

## Cookie Settings {#section_B498B8D1A34A444BBF84CC720EE9D87F}

The cookie has several default settings. You can change these settings if needed, with the exception of the cookie duration. Consult your account representative when changing cookie settings.


<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Setting</th> 
   <th colname="col2" class="entry">Information</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie name</p> </td> 
   <td colname="col2"> <p>mbox.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie domain</p> </td> 
   <td colname="col2"> <p>The second and top levels of the domains from which you serve the content. Because it is served from your company's domain, the cookie is a first party cookie. Example: <span class="filepath">mycompany.com</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Server domain</p> </td> 
   <td colname="col2"> <p> <span class="filepath">clientcode.tt.omtrdc.net</span>, using the client code for your account. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie duration</p> </td> 
   <td colname="col2"> <p>The cookie remains on the visitor's browser two weeks from his or her last login. You cannot change the cookie duration.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>P3P policy</p> </td> 
   <td colname="col2"> <p>The cookie is published with a P3P policy, as required by the default setting in most browsers. A P3P policy indicates to a browser who is serving the cookie and how the information will be used.</p> </td> 
  </tr> 
 </tbody> 
</table>

The cookie keeps a number of values to manage how your visitors experience campaigns:


<table id="table_5245F72A2D5A4322B40ABB10B7DFB338"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Value</th> 
   <th colname="col2" class="entry">Definition</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">session ID</span> </p> </td> 
   <td colname="col2"> <p>A unique ID for a user session. By default, this lasts 30 minutes.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">pc ID</span> </p> </td> 
   <td colname="col2"> <p>A semi-permanent ID for a visitor's browser. Lasts 14 days.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">check</span> </p> </td> 
   <td colname="col2"> <p>A simple test value used to determine if a visitor supports cookies. Set each time a visitor requests a page.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">disable</span> </p> </td> 
   <td colname="col2"> <p>Set if visitor's load time exceeds the timeout configured in the <span class="filepath">mbox.js</span> file. By default, this lasts 1 hour. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Impact on Target for Safari Visitors Due to Apple WebKit Tracking Changes {#section_2A2E5730ED7D4A0985C904AFEA310AAE}

**How does Adobe Target Tracking work?** 


<table id="table_E8AD8A6804F846C2B0C565EF195947DC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Cookies</th> 
   <th colname="col2" class="entry">Details</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>First-party domains</p> </td> 
   <td colname="col2"> <p>This is the standard implementation for Target customers.</p> <p>The "mbox" cookies is set in the customer's domain.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Third-party tracking</p> </td> 
   <td colname="col2"> <p>Third-party tracking is important for advertising and targeting use cases in Target and in Adobe Audience Manager (AAM).</p> <p>Third-party tracking requires cross-site scripting techniques.</p> <p>Target uses two cookies, "mboxSession" and "mboxPC" set in the <span class="filepath">clientcode.tt.omtrd.net</span> domain. </p> </td> 
  </tr> 
 </tbody> 
</table>

**What is Apple's approach?** 
From Apple:
"Intelligent Tracking Prevention is a new WebKit feature that reduces cross-site tracking by further limiting cookies and other website data."
"This is what's called cross-site tracking and the cookie used by example-tracker.com is called a third-party cookie. In our testing we found popular websites with over 70 such trackers, all silently collecting data on users."


<table id="table_1541BEC92F984A67A85FEC2CBA8B33F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Approach</th> 
   <th colname="col2" class="entry">Details</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Intelligent tracking prevention</p> </td> 
   <td colname="col2"> <p>For more information, see <a href="https://webkit.org/blog/7675/intelligent-tracking-prevention/" format="https" scope="external">Intelligent Tracking Prevention</a> on the WebKit Open Source Web Browser Engine website. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookies</p> </td> 
   <td colname="col2"> <p>How Safari handles cookies:</p> <p> 
     <ul id="ul_EDBB8181D89343FA8050158E60BA5A42"> 
      <li id="li_1DA7965CF023424F8AFAC8DB05DD7123"> <p>Third-party cookies that are not on a domain the user accesses directly are never saved.</p> <p>This behavior is not new. Third-party cookies are already not supported in Safari.</p> </li> 
      <li id="li_49424C46E45A45669336E8A24B8BAE5D"> <p>Third-party cookies set on a domain the user accesses directly are purged after 24 hours.</p> </li> 
      <li id="li_C4174E5033D84562AA4EBB72F34613BB"> <p>First-party cookies are purged after 30 days if that first-party domain has been classified as tracking users across sites.</p> 
       <ul id="ul_5DE2163E3ECB4EE2AEDF97E828A2F344"> 
        <li id="li_CDB5D52FCBCC4CE7A5778289C7B35CB8"> <p>This issue might apply to large companies that send users to different domains online.</p> </li> 
        <li id="li_E5A07F1A61744D2D8FA0F1232B6E4ABA"> <p>Apple has not made it clear how exactly these domains will be classified, or how a domain can determine if they've been classified as tracking users cross-site.</p> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Machine Learning to identify domains that are cross-site</p> </td> 
   <td colname="col2"> <p>From Apple:</p> <p>Machine Learning Classifier: A machine learning model is used to classify which top privately-controlled domains have the ability to track the user cross-site, based on the collected statistics. Out of the various statistics collected, three vectors turned out to have strong signal for classification based on current tracking practices: subresource under number of unique domains, sub frame under number of unique domains, and number of unique domains redirected to. All data collection and classification happens on-device.</p> <p>However, if the user interacts with <span class="filepath">example.com</span> as the top domain, often referred to as a first-party domain, Intelligent Tracking Prevention considers it a signal that the user is interested in the website and temporarily adjusts its behavior as depicted in this timeline: </p> <p>If the user interacted with <span class="filepath">example.com</span> the last 24 hours, its cookies will be available when <span class="filepath">example.com</span> is a third-party. This allows for "Sign in with my X account on Y" login scenarios. </p> <p> 
     <ul id="ul_69EF882AA7834DC68A68659235D90EC8"> 
      <li id="li_F99751217B1744CA952B6D58634AC0F3"> <p>Domains that are visited as top level domain won't be affected.</p> <p> 
        <ul id="ul_CD0D66E0862C46C29449EB66774EE3F9"> 
         <li id="li_58E038008DE74C888A3D1D9111B83EAC"> <p>Sites like OKTA for example</p> </li> 
        </ul> </p> </li> 
      <li id="li_CE55903E379C49548362511664EEF718">Identifies domains that are sub domain or sub frame of current page across multiple unique domains</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**How will Adobe be affected?** 


<table id="table_59EB5C77BF62423A8722711256412586"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Affected Functionality</th> 
   <th colname="col2" class="entry">Details</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Opt-out support</p> </td> 
   <td colname="col2"> <p>Apple's WebKit tracking changes breaks opt-out support.</p> <p>Target opt-out uses a cookie in the <span class="filepath">clientcode.tt.omtrdc.net</span> domain. For more details, see <a href="c_privacy.xml#concept_639482A343DB4963A6144378E1D8D7F0" format="dita" scope="local">Privacy</a>. </p> <p>Target supports two opt-outs:</p> <p> 
     <ul id="ul_BC41B5AA41884FFE8EAA34F3EB5EF254"> 
      <li id="li_1D79215CB0714FD7B33E7A310B6236C7"> <p>One per client (the client manages the opt-out link).</p> </li> 
      <li id="li_C0CB5430AFA54FC79CAD62676602EB8B"> <p>One via Adobe that opts the user out of all Target functionality for all customers.</p> </li> 
     </ul> </p> <p>Both methods use the third-party cookie.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target activities</p> </td> 
   <td colname="col2"> <p>Customers can choose their <a href="c_visitor_profile_lifetime.xml#concept_D9F21B416F1F49159F03036BA2DD54FD" format="dita" scope="local">profile lifetime length</a> for their Target accounts—up to 90 days. The concern is that if the account's profile lifetime is longer than 30 days, and the first-party cookie gets purged because the customer's domain has been marked as tracking users cross-site, behavior for Safari visitors will be affected in the following areas in Target: </p> <p> 
     <ul id="ul_FB4D6702D440456EBD16DA4108F90DA9"> 
      <li id="li_AB4D43B0CAFD49ADAFD1DF7C2DFC5A55"> <p><b>Target Reports</b> </p> <p> 
        <ul id="ul_0CFA08EDE5A449A68FC8493B67C7668E"> 
         <li id="li_6D778B39C7F4494CAE52C62A11BAFD84"> <p>If a Safari user enters into an activity, returns after 30 days, and then converts, that user counts as two visitors and one conversion.</p> <p>This behavior is the same for activities using Analytics as the reporting source (A4T).</p> </li> 
        </ul> </p> </li> 
      <li id="li_7A37E7601D3F4AA3A4F520021D2FDD1C"> <p><b>Profile &amp; Activity Membership</b> </p> <p> 
        <ul id="ul_D1C3DAE15B45428094396B6D77E6450D"> 
         <li id="li_B0B44CE2B18F47B59AD18AC484A9DA37"> <p>Profile data is erased when the first-party cookie expires.</p> </li> 
         <li id="li_00B5B9E7B65F48A594CF60DD5BB9B3E2"> <p>Activity membership is erased when the first-party cookie expires.</p> </li> 
         <li id="li_65FADF68F4C7400A9B63B8F5136B3D95"> <p>Target does not function in Safari for accounts using a third-party cookie implementation or a first- and third-party cookie implementation.</p> <p>Note that this behavior is not new. Safari has not allowed third-party cookies for awhile.</p> </li> 
        </ul> </p> </li> 
     </ul> </p> <p><b>Suggestions:</b>If there is a concern that the customer domain might be marked as one tracking visitors cross-session, it's safest to set the profile lifetime to 30 days or fewer in Target. This ensures that users will be tracked similarly in Safari and all other browsers. </p> </td> 
  </tr> 
 </tbody> 
</table>

