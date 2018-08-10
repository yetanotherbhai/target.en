---
description: Information about the various methods you can use to get data into Target, including page parameters, in-page profile attributes, script profile attributes, the bulk profile update API, the single profile update API, and Customer Attributes.
keywords: implement;implementing;setting up;setup;page parameter;in-page profile attribute;mbox parameter;in-page profile attributes;script profile attribute;bulk profile update API;single file update API;customer attributes
seo-description: Information about the various methods you can use to get data into Target, including page parameters, in-page profile attributes, script profile attributes, the bulk profile update API, the single profile update API, and Customer Attributes.
seo-title: Methods to get Data into Target
solution: Target
subtopic: Getting Started
title: Methods to get Data into Target
topic: Standard
uuid: d408f0d1-efc2-41b1-b461-80f36b6809cf
index: y
internal: n
snippet: y
translate: y
---

# Methods to get Data into Target

The following methods are available: 



<table id="table_40E09663B889424BA8E6D4D607FE241B"> 
 <tbody> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Page parameters (also called "mbox parameters")</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Page parameters are name/value pairs passed in directly through page code that are not stored in the visitor's profile for future use. </p> <p>Page parameters are useful to send additional page data to Target that does not need to be stored with the visitor's profile for future targeting use. These values are instead used to describe the page or the action the user took on the specific page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>Page parameters are passed into Target via a server call as a string name/value pair. Parameter names and values are customizable (although there are some "reserved names" for specific uses). </p> <p>Examples: </p> <p>page=productPage </p> <p>categoryId=homeLoans </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Product pages: Send information about the specific product viewed (this is how Recommendations works) </p> <p>Order details: Send order ID, orderTotal, and so forth for order collection </p> <p>Category affinity: Send category-viewed information to Target to build knowledge of the user's affinity to particular site categories </p> <p>3rd-party data: Send information from 3rd-party data sources, such as weather targeting providers, account data (for example, DemandBase), demographic data (for example Experian), and more. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>Data gets sent to Target in real-time, and can be used on the same server call the data on which it comes in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Requires page code update (directly or via a tag management system). </p> <p>If the data needs to be used for targeting on a subsequent page/server call, it needs to be translated to a profile script. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p> <span class="codeph"> targetPageParamsAll </span> (appends the parameters to all mbox calls on the page): </p> 
    <codeblock>
      function&nbsp;targetPageParamsAll()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;"param1=value1&amp;param2=value2&amp;p3=hello%20world"; 
     } 
    </codeblock> <p> <span class="codeph"> targetPageParams </span> (appends the parameters to the global mbox on the page): </p> 
    <codeblock>
      function&nbsp;targetPageParams()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;"param1=value1&amp;param2=value2&amp;p3=hello%20world"; 
     } 
    </codeblock> <p>Parameters in mboxCreate code: </p> 
    <codeblock>
      &lt;div&nbsp;class="mboxDefault"&gt; 
     &nbsp;&nbsp;default&nbsp;content&nbsp;to&nbsp;replace&nbsp;by&nbsp;offer 
     &lt;/div&gt; 
     &lt;script&gt; 
     &nbsp;&nbsp;mboxCreate('mboxName','param1=value1','param2=value2'); 
     &lt;/script&gt; 
    </codeblock> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p>Recommendations: <a href="../recs/c_recommendations.xml#reference_DE38BB07BD3C4511B176CDAB45E126FC" format="dita" scope="local"> Implementation According to Page Type </a> </p> <p>Order confirmation: <a href="c_target-atjs-implementation.xml#task_E85D2F64FEB84201A594F2288FABF053" format="dita" scope="local"> Create an Order Confirmation mbox - at.js </a> </p> <p>Category affinity: <a href="../ov/c_visitor_profile.xml#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local"> Category Affinity </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>In-page profile attributes (also called "in-mbox profile attributes)</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>In-page profile attributes are name/value pairs passed directly through page code that are stored in the visitor's profile for future use. </p> <p>In-page profile attributes allow user-specific data to be stored in Target's profile for later targeting and segmentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>In-page profile attributes are passed into Target via a server call as a string name/value pair with the prefix "profile." before the Attribute name. </p> <p>Attribute names and values are customizable (although there are some "reserved names" for specific uses). </p> <p>Examples: </p> <p> <span class="codeph"> profile.membershipLevel=silver </span> </p> <p> <span class="codeph"> profile.visitCount=3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Login information: Share non-PII (Personally Identifiable Information) data to Target based on the user's login. This could be membership status, order history, or more. </p> <p>Store info: Track which store is this user's preferred location. </p> <p>Previous interactions: Track what the user has done on the site previously to inform future personalization. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>Data gets sent to Target in real-time, and can be used on the same server call on which the data comes in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Requires page code updates (directly or via a tag management system). </p> <p>Attributes and values are visible in server calls, so a visitor can see the values. If sharing information such as credit ranges or other potentially private information, this might not be the best approach. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p> <span class="codeph"> targetPageParamsAll </span> (appends the attributes to all mbox calls on the page): </p> 
    <codeblock>
      function&nbsp;targetPageParamsAll()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;"profile.param1=value1&amp;profile.param2=value2&amp;profile.p3=hello%20world"; 
     } 
    </codeblock> <p> <span class="codeph"> targetPageParams </span> (appends the attributes to the global mbox on the page): </p> 
    <codeblock>
      function&nbsp;targetPageParams()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;profile.param1=value1&amp;profile.param2=value2&amp;profile.p3=hello%20world"; 
     } 
    </codeblock> <p>Attributes in mboxCreate code: </p> 
    <codeblock>
      &lt;div&nbsp;class="mboxDefault"&gt; 
     &nbsp;&nbsp;default&nbsp;content&nbsp;to&nbsp;replace&nbsp;by&nbsp;offer 
     &lt;/div&gt; 
     &lt;script&gt; 
     &nbsp;&nbsp;mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); 
     &lt;/script&gt; 
    </codeblock> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p> <a href="../ov/c_visitor_profile.xml#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profile Attributes </a> </p> <p> <a href="../ov/c_visitor_profile.xml#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1" format="dita" scope="local"> Visitor Profiles </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Script profile attributes</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Script profile attributes are name/value pairs defined in the Target solution. The value is determined from executing a JavaScript snippet on Target's server per server call. </p> <p>Users write small code snippets that execute per mbox call, and before a visitor is evaluated for audience and activity membership. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>Script profile attributes are created in the Audiences section of Target. Any attribute name is valid, and the value is the result of a JavaScript function written by the Target user. The attribute name is automatically prefixed by " <span class="codeph"> user. </span>" in Target to distinguish them from in-page profile attributes. </p> <p>The code snippet is written in the Rhino JS language and can reference tokens and other values. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Cart Abandonment: When the visitor reaches the shopping cart, set the profile script to 1. When the visitor converts, reset it to 0. If the value =1, then the visitor has an item in the cart. </p> <p>Visit Count: On every new visit, increment the count by 1 to keep track of how often a visitor returns to the site. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>Requires no page code updates. </p> <p>Executes before audience and activity membership decisions, so these profile script attributes can affect membership on a single server call. </p> <p>Can be very robust. As many as 2,000 instructions can be executed per script. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Requires JavaScript knowledge. </p> <p>The execution order of profile scripts cannot be guaranteed, so they cannot rely on each other. </p> <p>Can be difficult to debug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p>Profile scripts are quite flexible: </p> 
    <codeblock>
      user.purchase_recency: 
     var&nbsp;dayInMillis&nbsp;=&nbsp;3600&nbsp;*&nbsp;24&nbsp;*&nbsp;1000; 
     if&nbsp;(mbox.name&nbsp;==&nbsp;'orderThankyouPage')&nbsp;{ 
     &nbsp;user.setLocal('lastPurchaseTime',&nbsp;new&nbsp;Date().getTime()); 
     } 
     var&nbsp;lastPurchaseTime&nbsp;=&nbsp;user.getLocal('lastPurchaseTime'); 
     if&nbsp;(lastPurchaseTime)&nbsp;{ 
     &nbsp;return&nbsp;((new&nbsp;Date()).getTime()-lastPurchaseTime)/dayInMillis; 
     } 
    </codeblock> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p> <a href="../ov/c_visitor_profile.xml#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profile Script Attributes </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Bulk profile update API</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Via API, send a .csv file to Target with visitor profile updates for many visitors. Each visitor profile can be updated with multiple in-page profile attributes in one call. </p> <p>This option is very similar to Customer Attributes with a few differences: </p> <p> 
     <ul id="ul_75EFDFD9534541E3BBB1A99228E5D0A2"> 
      <li id="li_2F36B7D3580D4AB7983A0EEBBEAD43F4"> <p>Customer Attributes use an FTP upload while the Target Bulk Profile Update API uses an HTTP POST API. </p> </li> 
      <li id="li_C1CB5D8CDB0C4F18AC08D3E506FFB38E"> <p>Customer Attributes data can be shared with Analytics. Bulk Profile Update is useable only in Target. </p> </li> 
      <li id="li_7AE2B90224C54ECE88BE807E2011141D"> <p>Customer Attributes support creating a profile for a user Target has not yet seen. The Bulk Profile Update API updates existing Target profiles only. </p> </li> 
      <li id="li_B7DDD5613526421CBA901B10E2DDAC2E"> <p>Customer Attributes require the use of the Experience Cloud ID (ECID). The Bulk Profile Update API requires either the TNT ID or the <span class="codeph"> mbox3rdPartyId </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>The .csv file must refer to each visitor via his or her Target PCID or <span class="codeph"> mboxThirdPartyId </span>. The Experience Cloud ID (ECID) is not supported. All profile attributes/values are created and updated via the API. Format details are available in the API documentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Your CRM or other internal system stores valuable data about your visitors that you want to consistently update into Target, without exposing the profile data in your page implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>No limit on the number of profile attributes. </p> <p>Profile attributes sent via the site can be updated via the API and vice versa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>The size of the batch file must be less than 50 MB. In addition, the total number of rows should not exceed 500,000 rows per upload. </p> <p>There is no limit on the number or rows you can upload over a period of 24 hours in subsequent batches. However, the ingestion process might be throttled during business hours to ensure that other processes run efficiently. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p>See <a href="http://developers.adobetarget.com/api/#updating-profiles" format="http" scope="external"> Updating Profiles </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p> <a href="http://developers.adobetarget.com/api/#updating-profiles" format="http" scope="external"> Updating Profiles </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Single profile update API</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Almost identical to the Bulk Profile Update API, but one visitor profile is updated at a time, in line in the API call instead of with a .csv file </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>The visitor must be identified via the Target <span class="codeph"> mboxPC </span> value or <span class="codeph"> mboxThirdPartyId </span> value. The Experience Cloud ID (ECID) is not supported. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>You want to update Target in real-time when a visitor performs some offline action, such as reaching a call center, a loan is funded, using a loyalty card in store, accessing a kiosk, and so forth. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>No limit on the number of profile attributes. </p> <p>Profile attributes sent via the site can be updated via the API and vice versa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Limit of 1,000,000 API calls (1 million) per 24-hour period </p> <p> Updates profiles only. Cannot create a profile for a potential user Target has yet to see. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p>GET and POST supported. 
     <codeblock>
       https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&amp;amp;profile.attr1=0&amp;amp;profile.attr2=1... 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p> <a href="http://developers.adobetarget.com/api/#updating-profiles" format="http" scope="external"> Updating Profiles </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Customer Attributes</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Customer attributes let you upload visitor profile data via FTP to the Experience Cloud. Once uploaded, leverage the data in Adobe Analytics and Adobe Target. </p> <p>Target Standard customers can leverage 5 attributes, Target Premium customers can leverage 200 attributes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>A .csv file with Experience Cloud IDs (ECIDs) and attribute name/value pairs is uploaded via FTP or manually in the Experience Cloud UI. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Your CRM or other internal system stores valuable information you want to share with Adobe's Experience Cloud, including Target and Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>Uploading customer data creates a profile entry for that visitor in Target, even if Target has yet to see the visitor. </p> <p>Same data is automatically available in Target and Analytics. </p> <p>FTP can be a simpler implementation method than API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Target Standard customers can leverage 5 attributes, Target Premium customers can leverage 200 attributes </p> <p>Can only update values via Customer Attributes, not on page. </p> <p>Requires Experience Cloud ID (ECID) implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p>Details can be found in <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/t_crs_usecase.html" format="html" scope="external"> Create a Customer Attribute Source and Upload the Data File </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/t_crs_usecase.html" format="html" scope="external"> Create a Customer Attribute Source and Upload the Data File </a> </td> 
  </tr> 
 </tbody> 
</table>

