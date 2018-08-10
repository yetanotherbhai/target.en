---
description: Use the Offers library to manage your code offer and image offer content.
keywords: debug mbox;troubleshoot mbox;mbox issues;flicker;mboxDebug;mboxTrace;authorization token;token;debugger;priority;activity priority;Adobe Marketing Cloud Debugger;orderConfirmPage mbox;SiteCatalyst  purchase mbox;top selling;top seller
seo-description: Use the Offers library to manage your code offer and image offer content.
seo-title: Offers
solution: Target
subtopic: Multivariate Test
title: Offers
topic: Standard
uuid: 85deaa2d-899a-4092-9243-50310a46a8ab
index: y
internal: n
snippet: y
translate: y
---

# Offers

## Offers {#concept_17874A6FCBB743AA84C5988E8571CCF3}Use the Offers library to manage your code offer and image offer content.
>[!NOTE]
>
>In the January 2017 release, offers created via [!DNL  Target Classic], [!DNL  Adobe Experience Manager] (AEM), [!DNL  Adobe Mobile Services] (AMS), and APIs are visible in the [!DNL  Target Standard/Premium] user interface. Offers updated in the last two years using these methods will be visible (i.e. January 2015 and beyond). The initial synchronization will occur the first time any user in your organization opens the [!UICONTROL  Offers] page. The amount of time for the initial synchronization will depend on the amount of data. After the initial synchronization, data will sync incrementally. If you had code and images in the same folder before this release, [!DNL  Target] will split them into two duplicate folders. Note that the Updated date and time refers to the time when the folder was migrated and does not reflect the date you originally created the folder. 



This video includes information about managing offers. 

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Offers Library </th> 
   <th colname="col3" class="entry"> 4:56 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/ZNIGgXOATMY/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/ZNIGgXOATMY/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Connection between the <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/creative_cloud.html" format="https" scope="external"> Marketing Cloud Asset Library </a> and the Target Content Library </li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405">Custom HTML Offers </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Custom HTML Offer in the Visual Experience Composer </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Click ** [!UICONTROL  Offers] ** to open the library. The library contains the offers that have been set up via [!DNL  Target Standard/Premium], [!DNL  Target Classic], [!DNL  Adobe Experience Manager] (AEM), [!DNL  Adobe Mobile Services] (AMS), and APIs. Offers created in [!DNL  Target Classic] or other solutions are editable in [!DNL  Target Standard/Premium]. 

The [!UICONTROL  Offers] page has two tabs along the right side: Code Offers and Image Offers that let you view offers by type. 

![](../graphics/offers page.png) 

You can filter offers by type ( HTML Offer, Redirect Offer, Remote Offer, or Folder) and by source (Adobe Target, Adobe Target Classic, Adobe Experience Manager, Adobe Mobile Services, or API). 

![](../graphics/offers filter.png) 

You can edit or copy a folder or offer by hovering over the desired item, then by clicking the Edit or Copy icons. 

![](graphics/offer-picker-large.png) 

## Viewing Offer Definitions {#section_6B059DD121434E6292CAB393507D010E}

You can view offer definition details on a pop-up card in the Offers Library without opening the offer. 

For example, the following offer definition card for an HTML offer is accessed by hovering over an offer on the Contents List, then clicking the information icon: 

![](graphics/offer-card-html.png) 

The following information is available: 


* Name 

* Source 

* Type 

* Offer ID 

* Offer path 

* Last Modified 



Click the [!UICONTROL  Offer Usage] tab to view the activities that reference a code offer in each offer's definition pop-up card. This functionality does not apply to image offers. This way you can avoid impact to other activities while editing offers. Information includes Live Activities and Inactive Activities. 

![](graphics/offer-card-usage.png) 

The following offer definition card for a Redirect offer: 

![](graphics/offer-card-redirect.png) 

The following information is available: 


* Name 

* Source 

* Type 

* Offer ID 

* Offer Path 

* Last Modified 

* Redirect URL 

* Include all URL parameters (on or off) 

* Pass mbox session ID (on or off) 



The following offer definition card for a Remote offer: 

![](graphics/offer-card-remote.png) 

The following information is available: 


* Name 

* Source 

* Type 

* Offer ID 

* Offer Path 

* Last Modified 

* Redirect URL Type 

* Absolute or Relative URL 


>## Create Offer Folder {#task_E9D147919DF74245BBF49FF145F0E7D7}Create a folder to hold items in the Offers library. 
<draft-comment otherprops="merge">
  target/t_create_content_folder.x 
</draft-comment>
>1. Click ** [!UICONTROL  Offers] **, then select the ** [!UICONTROL  Code Offers] ** or ** [!UICONTROL  Image Offers] ** tab, as appropriate.
>1. Click ** [!UICONTROL  Create] ** > ** [!UICONTROL  Folder] **.
>1. Fill in the fields:


>    <table id="table_363A1AC11C4143749C2E265A93F3B146"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Field </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Title (Applies to image offers only) </p> </td> 
   <td colname="col2"> <p>Specify a descriptive name for the folder. For example, you could include the type of content it will hold. </p> <p> The name cannot contain the following characters: </p> <p>  </p>
    <table id="table_CBE0B2CA9590435DBEC1EACE0780D48B">  
    </table> <p>You can use a hyphen (-) instead of these characters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Name (Applies to both code and image offers) </p> </td> 
   <td colname="col2"> <p>Edit the name, if desired. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Private (Applies to image offers only) </p> </td> 
   <td colname="col2"> <p>Specifies that the folder private so only you can see it and its contents. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reorder-able in List View (Applies to image offers only) </p> </td> 
   <td colname="col2"> <p>Specifies that you and others can reorder the folder's position in the List View. </p> <p>To toggle between the Card View and List View, click the Card View icon ( <img href="graphics/icon_card_view.png" id="image_51ABE05ED3F44080ACF9030848E22593" /> ) or the List View icon ( <img href="graphics/icon_list_view.png" id="image_4F40A7CFCB64420B839565DBB21C7002" /> ) in the upper right corner of the content library. You can also select <span class="wintitle"> View Settings </span> to include or exclude columns in the List View. </p> </td> 
  </tr> 
 </tbody> 
</table>

>1. Click ** [!UICONTROL  Create] **.
>## Uploading Content {#task_75F8EF8CF0054C5A857E04F7B1717F06}You can add items to the Image Offers list. 
<draft-comment otherprops="merge">
  target/t_assets_upload.xml 
</draft-comment>
>1. Click ** [!UICONTROL  Offers] **, then select the ** [!UICONTROL  Image Offers] ** tab.
>1. Click ** [!UICONTROL  Create] ** > ** [!UICONTROL  Files] **.
>1. Select the item you want to add, then click ** [!UICONTROL  Open] **.
>1. Edit the item's filename, in necessary, then click ** [!UICONTROL  Upload] **.

>       The item is added to the library. 
>## Create Redirect Offers {#task_33C80CD722564303B687948261484F94}The Redirect Offer causes a browser to redirect to a new page. 
<draft-comment otherprops="merge">
  target/t_offer_redirect.xml 
</draft-comment>You might have two completely different pages to test instead of just changing pieces of content within a page. In this case, your A/B test compares page A vs. page B. Set up an A/B test campaign with two experiences: one pointing to the default page A, and the other redirecting to page B. The offer is configured to redirect the visitor to a different page. 


>[!NOTE] {class="- topic/note "}
>
>You cannot use redirect offers in ajax mboxes ( ` mboxUpdate`). 




>[!NOTE]
>
>For redirect offers in activities using A4T, your implementation must meet certain minimum requirements. In addition, there is important information that you need to know. For more information, see[ Redirect Offers - A4T FAQ ](c_a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905). 



For information about setting up an experience that redirects, see [ Redirect to a URL ](t_redirect_offer.md#task_9578678D42784F5EB9638F8AC8C911FA). 

The redirect offer executes JavaScript code to redirect the browser. It uses the ` window.location.replace();` method, so the page the visitor is redirected from is not stored in the browser history. This allows the visitor to still use the back button in their browser. 


>[!NOTE] {class="- topic/note "}
>
>If you want to pass the referrer value of the landing page, it is recommended that you use an HTML offer rather than a redirect offer.



**To create a Redirect Offer: ** 

>1. Click ** [!UICONTROL  Offers] **, then select the ** [!UICONTROL  Code Offers] ** tab.
>1. Click ** [!UICONTROL  Create] ** > ** [!UICONTROL  Redirect Offer] **.
>1. Type an offer name.
>1. Enter the URL for the unique content or destination you want to redirect to. This must be an absolute URL.
>1. Select the desired options to customize your redirect offer:

>    
>    * ** Include all URL parameters: ** Check this box if you want all the URL parameters present on the previous page to be propagated to the redirected page. 

>      For example, you want to redirect people directly from a men's page to a men's shirts category page. You also want the dynamic parameters in the URL to be passed because this is how you track if people reached your site via email, banner ad, search ad, or organically. By checking this box, your redirect offer on page ` http://www.mycompany.com/mens.html?emailId=123` will automatically become ` http://www.mycompany.com/mensShirts.html?emailId=123` when all you entered in the URL box was ` http://www.mycompany.com/mensShirts.html`. 

>    * ** Pass mbox session ID (required to redirect to a different domain): **Check this box if you want the ` sessionId` to automatically be included in the redirect. This is only required when you are testing clicks from an email or clicks from one domain to another. The ` sessionId` matches the visitor's cookie so the visitor can continue to be tracked and the proper content is shown. If you use the 1st &amp;amp; 3rd party cookie setup, you do not need to pass the mbox session ID when crossing domains. It is persistent on the 3rd-party cookie, so it is not necessary in the URL. 


>## Create Remote Offers {#concept_657016A0E6174C22B89036E9C8A0170F}Use remote offers to host content outside of 
<keyword>
  Target 
</keyword> that Target references and delivers to users' websites. This content might be in a content management or other system, either for ease-of-use or for security reasons. 
<draft-comment otherprops="merge">
  target/c_about-remote-offers.xml 
</draft-comment>
>[!NOTE]
>
>Remote offers can be created only in the forms-based composer. Content will be injected in the mbox locations, so these are most likely not appropriate for a global mbox.




>[!NOTE]
>
>[!DNL  Target Classic] included similar features: [!UICONTROL  Offer on Your Site] and [!UICONTROL  Offer Outside Test&amp;amp;Target]. 



Some examples of remote offers include: 


* Different versions of your cross-sells
* Dynamic shopping cart messages
* Forms
* Calculators
* Interest rate updates


**To create a remote offer:** 


1. Click ** [!UICONTROL  Offers] **, then select the ** [!UICONTROL  Code Offers] ** tab. 

1. Click ** [!UICONTROL  Create] ** > ** [!UICONTROL  Remote Offer] **. 

   ![](graphics/remote_offer_ui.png) 

1. Provide a descriptive name for the offer. 

   A descriptive name helps you and others quickly find the offer in the [!UICONTROL  Assets] library. 

1. Specify the remote URL for the remote offer: 



<table id="table_E030736D80514A53B65D26DFF62ED67C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Option </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cached </p> </td> 
   <td colname="col2"> <p>The content for a cached remote offer is served from <span class="keyword"> Target </span>. </p> <p>Every two hours, <span class="keyword"> Target </span> fetches the content at the remote URL and then stores the content inside <span class="keyword"> Target </span>. When visitors load a site with an experience that includes a remote offer, the offer is delivered by <span class="keyword"> Target </span>. </p> <p>Cached remote offers provide enhanced security because somebody logged in to Target cannot change the content. To change the content, someone would need to log in to the content management or other system and change the content there. </p> <p>You can specify an absolute or relative URL for a cached remote offer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic </p> </td> 
   <td colname="col2"> <p>A dynamic remote offer is served from the content management or other system rather than from <span class="keyword"> Target </span>. </p> <p>You might not want the content periodically cached and then delivered by <span class="keyword"> Target </span> whenever visitors load a site with an experience that includes a remote offer. Instead, you want to call the system that is hosting the content, possibly pass in specific information so that the returned offer can be dynamic, or different, for each user. </p> <p>For example, if a user logs in to a website for a credit card that includes an experience with a dynamic remote offer, you could pass parameters into the URL for the user's account information. Then the website could provide user-specific information, such as account balance. </p> <p>Click <span class="wintitle"> Add Parameter </span> to add one or more mbox or request parameters. </p> </td> 
  </tr> 
 </tbody> 
</table>


1. Click ** [!UICONTROL  Save] **.


## Best Practices for Using Remote Offers {#section_7718512D08E14121B6F6B8C38134F4BC}

Best practices for using remote offers in your activities: 


* If your offer resides in the same domain as the mboxes, using the [!UICONTROL  Cached] option lets you use relative URLs in describing your offer location. 

  This means that when you move your activity from your staging servers to production, the content will automatically be accessible without having to change the URL manually. 

* If your test involves data dynamically generated by your server, the [!UICONTROL  Dynamic] option might be the right choice. 

* If you plan to test only the appearance of your existing remote offer content, use the [!UICONTROL  Visual Experience Composer] to change the look and feel of the content that is returned from the content management system. 

* Use the Remote Offer Selection Matrix to help you choose the offer best suited for your specific case. Consult your account representative if you have questions. 


>## How Dynamic Remote Offers Work {#concept_CC2A969420B34364A9FA78C1CE251818}Dynamic remote offers use your dynamic page technology to pass values to the offer. 
<draft-comment otherprops="merge">
  target/c_how-remote-offers_work.xml 
</draft-comment>The offer is executed after you render the page. An invisible iframe gathers the data, copies it out of the frame and inserts in on the page, loading your passed values. 

![](graphics/remote_offer_howitworks 2.jpeg) 
>## Remote Offer Selection Matrix {#reference_B23BEDD29DDD47709A7651AFD27E776B}The Remote Offer Selection Matrix helps you decide which type of remote offer to choose: 
<wintitle>
  Cached 
</wintitle> or 
<wintitle>
  Dynamic 
</wintitle>. 
<draft-comment otherprops="merge">
  target/r_remote-offer-selection-matrix.xml 
</draft-comment>


><table id="table_6D4312DFE1A241958CE1E867FC20F9A8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col002" class="entry"> Cached </th> 
   <th colname="col2" class="entry"> Dynamic </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Updates each time a visitor makes a request </p> </td> 
   <td colname="col002"> <p>No </p> </td> 
   <td colname="col2"> <p>Yes </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Content updates </p> </td> 
   <td colname="col002"> <p>Cached every 2 hours </p> </td> 
   <td colname="col2"> <p>Updated immediately upon each request </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Load time </p> </td> 
   <td colname="col002"> <p>Faster </p> </td> 
   <td colname="col2"> <p>Slower due to request processing </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Can see JavaScript on page </p> </td> 
   <td colname="col002"> <p>Yes </p> </td> 
   <td colname="col2"> <p>No, but can pass via URL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers can include JavaScript </p> </td> 
   <td colname="col002"> <p>Yes </p> </td> 
   <td colname="col2"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offer URL </p> </td> 
   <td colname="col002"> <p>Absolute or Relative </p> </td> 
   <td colname="col2"> <p>Relative </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Requesting computer </p> </td> 
   <td colname="col002"> <p>Adobe servers </p> </td> 
   <td colname="col2"> <p>The visitor's computer, which carries the visitor's cookies </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Create JSON Offers {#concept_63C7BEE1F0DB4A7596D997219B7C136D}Create JSON offers in the Offer Library for use in the Form-Based Experience Composer.JSON offers can be used in form-based activities whereby enabling use cases where Target's decisioning is required to send an offer in JSON format for consumption in SPA framework or server-side integrations. 

Consider the following information as you work with JSON offers: 


* JSON offers are currently available only for AB and XT activities. 

* JSON offers can be used in form-based activities only. 

* All offers deliver asynchronously if you are using any version of [!DNL  at.js] or [!DNL  mbox.js] version 60 or later. 

* JSON offers are delivered as native JSON objects rather than as strings. Consumers of these objects are no longer required to handle objects as strings and convert them to JSON objects. 

* JSON offers are not applied automatically as opposed to other offers (such as HTML offers) because JSON offers are non-visual offers. Developers must write code to explicitly get the offer using [ adobe.target.getOffer(options) ](c_target-ats-functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF). 



## Creating a JSON Offer {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}


1. Click ** [!UICONTROL  Offers] **, then select the ** [!UICONTROL  Code Offers] ** tab. 

1. Click ** [!UICONTROL  Create] ** > ** [!UICONTROL  JSON Offer] **. 

   ![](graphics/offer-json.png) 

1. Type an offer name. 

1. Type or paste your JSON code in the ** [!UICONTROL  Code] ** box. 

1. Click ** [!UICONTROL  Save] **. 



## Example {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON offers are supported only in activities created using the Form-based Experience Composer. Currently the only way to be able to use JSON offers is via direct API calls. 

Here is an example: 


```
adobe.target.getOffer({ 
  mbox: "some-mbox", 
  success: function(actions) { 
    console.log('Success', actions); 
  }, 
  error: function(status, error) { 
    console.log('Error', status, error); 
  } 
});
```


The actions passed to success callback is an array of object. Assuming that we have a single JSON offer, that has this content: 


```
{ 
  "demo": {"a": 1, "b": 2} 
}
```


The actions array will have this structure: 


```
[ 
 { 
   action: "setJson", 
   content: [{ 
     "demo": {"a": 1, "b": 2} 
   }] 
 }  
]
```


To extract the JSON offer you iterate through actions and find the action with ` setJson` action and then iterate through the content array. 

## Use Case {#section_85B07907B51A43239C8E3498EF58B1E5}

Let's say the following JSON offer gets delivered to your web page: 


```
{ 
    "_id": "5a65d24d8fafc966921e9169", 
    "index": 0, 
    "guid": "7c006504-c6f7-468d-a46f-f72531ea454c", 
    "isActive": true, 
    "balance": "$2,075.06", 
    "picture": "http://placehold.it/32x32", 
    "tags": [ 
      "esse", 
      "commodo", 
      "excepteur", 
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      }, 
    ], 
    "greeting": "Hello, Stephenson Fernandez! You have 4 unread messages.", 
    "favoriteFruit": "strawberry" 
} 
  
```


The following code shows how to access the "greeting" attribute: 


```
adobe.target.getOffer({   
  "mbox": "name_of_mbox", 
  "params": {}, 
  "success": function(offer) {           
        console.log(offer[0].content[0].greeting); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```


## Filtering Offers by the JSON Offer Type {#section_52533555BCE6420C8A95EB4EB8907BDE}

You can filter the Offers Library by the JSON offer type by clicking the ** [!UICONTROL  Type] ** drop-down list, then by selecting the ** [!UICONTROL  JSON] ** checkbox. 

![](graphics/offer-json-filter.png) 
>## Working with Content in the Library {#task_6ADAFE9C6DC74F2884C904C7804FAA1A}There are a number of tasks you can perform on an asset in the library. 
<draft-comment otherprops="merge">
  target/t_assets_working.xml 
</draft-comment>
>1. Click ** [!UICONTROL  Offer] **, select the ** [!UICONTROL  Code Offer] ** or ** [!UICONTROL  Image Offer] ** tab, then locate the asset you want to work with.
>   For more information about searching the Offer library and creating Smart Collections, see [ Filter and Search Content ](c_manage_content.md#concept_3B59B8F025BF4CEA82ECC5199D365276). 
>
>1. Hover over the item you want to work with, then select an action.



>    <table id="table_72572C019D7444B08BF1A08FA1CED1FB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Action </th> 
   <th colname="col2" class="entry"> Asset Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Annotate </td> 
   <td colname="col2"> <p>Image </p> </td> 
   <td colname="col3"> Add a note to the asset. Click the asset, then select the area you want to annotate and type your note. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Copy </td> 
   <td colname="col2"> <p>Experience </p> <p>Image </p> <p>Folder </p> <p>Text/HTML </p> </td> 
   <td colname="col3"> Copy the asset to the clipboard. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Delete </td> 
   <td colname="col2"> <p>Experience </p> <p>Image </p> <p>Folder </p> <p>Text/HTML </p> </td> 
   <td colname="col3"> Delete the asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Download </td> 
   <td colname="col2"> <p>Experience </p> <p>Image </p> <p>Text/HTML </p> </td> 
   <td colname="col3"> Download the asset to your device or computer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Edit </td> 
   <td colname="col2"> <p>Image </p> <p>Text/HTML </p> </td> 
   <td colname="col3"> Edit the asset. The Edit Asset screen opens, which contains some editing options, such as rotate and crop. </td> 
  </tr> 
  <!-- <row> <entry colname="col1">Move </entry> <entry colname="col2"> <p>Experience </p> <p>Image </p> <p>Folder </p> <p>Text/HTML </p> </entry> <entry colname="col3">Move the asset to another location. To move the asset, specify a name for the asset, select a destination, adjust any references to the asset, and republish to the new location. </entry> </row> --> 
  <tr> 
   <td colname="col1"> Share Card </td> 
   <td colname="col2"> <p>Experience </p> <p>Image </p> <p>Text/HTML </p> </td> 
   <td colname="col3"> Share the card on another board. You can draw an annotation, select the board to share with, and add a comment about the card. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> View Properties </td> 
   <td colname="col2"> <p>Experience </p> <p>Image </p> <p>Text/HTML </p> </td> 
   <td colname="col3"> View the asset's properties. Click the Pencil icon on the properties page to edit the properties and add more info. You can add metadata information, publication status, and license data. </td> 
  </tr> 
 </tbody> 
</table>

>1. To change the image that represents an item in the library, click the item, then click the ** [!UICONTROL  Properties] ** icon, click ** [!UICONTROL  Edit] **, and then add an image.
>## Search Content and Create Smart Collections {#concept_3B59B8F025BF4CEA82ECC5199D365276}Search for assets by keywords and save search folders, called smart collections, that are automatically updated with search results. 
<draft-comment otherprops="merge">
  target/c_filter-and-search-content.xml 
</draft-comment>This section contains the following information: 


* [ Search for Assets by Keyword ](c_manage_content.md#section_2465A71BC95942588F586B1EC8B9E5DB)
* [ Save Smart Collection ](c_manage_content.md#section_5C95159543B5405EB8C8E47B518DF4AB)


## Search for Assets by Keyword {#section_2465A71BC95942588F586B1EC8B9E5DB}


1. Click ** [!UICONTROL  Offers] ** > ** [!UICONTROL  Image Offers] ** to access the [!UICONTROL  Asset Library]. 

   You can click the [!UICONTROL  Card View] icon (  ![](graphics/icon_card_view.png) ) in the top right corner to display assets in card-view format. 

   Or 

   You can click the [!UICONTROL  List View] icon (  ![](graphics/icon_list_view.png) ) in the top right corner to display assets in list-view format. 

1. Click the ** [!UICONTROL  Content Only] ** icon (  ![](graphics/icon_filter.png) ) in the top left corner to display the search box. 

   ![](graphics/search_assets.png) 

1. In the search box, type a keyword for the asset(s) you want to locate, then press Enter. 



## Save Smart Collection {#section_5C95159543B5405EB8C8E47B518DF4AB}

You can create saved searches, called smart collections, to save time when performing similar searches. A saved search creates a smart collection that is automatically updated with search results. 


1. Click ** [!UICONTROL  Offers] ** > ** [!UICONTROL  Image Offers] ** to access the [!UICONTROL  Assets Library]. 

   ![](graphics/content.png) 

1. Click the ** [!UICONTROL  Content Only] ** icon (  ![](graphics/icon_filter.png) ) in the top left corner to display the [!UICONTROL  Filter &amp;amp; Options] panel in the left rail. 

1. Click the ** [!UICONTROL  Browse] ** icon (  ![](graphics/icon_browse.png) ) to display the [!UICONTROL  Select Path] dialog box. 

   ![](graphics/browse folders.png) 

1. Browse to and select the desired folder that you want to base the smart collection on, then click the ** [!UICONTROL  Confirm] ** icon (  ![](graphics/icon_confirm.png) ). 

   ![](graphics/browse folders2.png) 

1. (Optional) Select from among the various options to narrow your filter, for example, file type and size. 

1. Click ** [!UICONTROL  Save Smart Collection] ** at the bottom of the [!UICONTROL  Filter &amp;amp; Options] panel to display the Save options. 

   ![](graphics/save_smart_collection_options.png) 

1. Specify a name for the smart collection, select the ** [!UICONTROL  Public] ** check box if you want all users in your [!DNL  Target] account to be able to access this smart collection, then click ** [!UICONTROL  Save] **. 

   The smart collection is added to your saved searches list for future use: 

   ![](graphics/saved_smart_collection.png) 



You can edit a saved smart collection by selecting it from the [!UICONTROL  Saved Searches] drop-down list to open it, then by clicking [!UICONTROL  Edit Smart Collection]. 
>## Pass Dynamic Data into Offers {#reference_324B171BB77F4D41BB62FAE8CE80B445}You can display profile values and campaign information directly in an HTML or Flash Offer. 
<draft-comment otherprops="merge">
  target/r_passing-profile-attributes-to-the-html-offer.xml 
</draft-comment>
>**Business Case** 

>A visitor arrives on your landing page with ` keyword=world` ` cup`. You display the term *World cup* in the offer. 

>** Technical Advantages** 

>Because it is stored in the user profile, you can repeat this message on his next visits. Just one offer or campaign can manage these custom messages for all your visitors. As the visitor's intent changes your website content automatically reflects those changes. 

>**Example** 

>
>* ` mboxCreate("landingpage"`, ` "profile.keyword=World Cup");`
>* HTML Offer code: ` Get your ${profile.keyword} information here!`
>* User sees: Get your World Cup information here!


>The following values can be "token replaced": 



><table id="table_392FA513A3494227A00DCB2B464FFE95"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Values </th> 
   <th colname="col2" class="entry"> Examples </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>In-mbox profile parameters </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ${profile.age} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Script profile parameters </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ${user.lifetimeSpend} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mbox parameters </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ${mbox.favoriteColor} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Campaign information </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ${campaign.name}, ${campaign.recipe.name}, ${campaign.id}, </span> </p> <p> <span class="codeph"> ${campaign.recipe.id} </span> </p> <p> <span class="codeph"> ${campaign.recipe.trafficType} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Unique visitor id </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ${user. pcId} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Unique session id </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ${user.sessionId} </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visitor's first session (true or false) </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ${user.isFirstSession} </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>**Tip:** This information can be useful for debugging. 

>** Implementation** 

>For profile parameters passed into an mbox, use the syntax: ` ${profile.parameter}` For profile parameters created in a script, use the syntax: 

>` ${user.parameter}` 

>These variables are replaced with the value on the server side, so no quotes or other JavaScript is required for the proper display. 

>Default values can also be specified for values you wish to expose to offers. The syntax is like this: 

>` ${user.testAttribute default="All Items!"}` 

>When ` testAttribute` doesn’t exist or is blank, "All Items!" will be written out. If an empty attribute value is valid, and you want to write it out instead of showing the default, you can use: 

>` ${user.testAttribute default="All Items!" show_blank="true"}` 

>You can also escape and unescape values to be displayed. If your value has an apostrophe for example, you would want to escape the value so it does not break the JavaScript on the page. (Offers are written in JavaScript, so a single apostrophe can be confused for a quote.) For example: 

>` ${user.encodedValue encode="unescape"}` 

>` ${user.unencodedValue encode="escape"}` 


>>[!NOTE]
>>
>>Please work with your representative to use this feature.
>

>## Troubleshooting Content Delivery {#concept_D2548B486C984B1E97ED7A72075B8EEA}If your page does not display the expected content, there are a few steps you can take to debug content delivery. 
<draft-comment otherprops="merge">
  target/c_content_trouble.xml 
</draft-comment>
* Check your activity or campaign code carefully. A typo or other error could cause the expected content not to display. 

* Use mboxTrace or mboxDebug to troubleshoot the mbox. 

* Use the Adobe Marketing Cloud Debugger, an easy-to-use tool that provides much of the same information as mboxDebug, to troubleshoot the mbox. 



mboxDebug is especially useful when you are setting up Target on your page to make sure the mbox is firing and the cookie is being set. However, it does not go into the kind of detail that is useful when debugging content delivery. If your activity does not appear on your page or undesired content appears, use mboxTrace to examine and debug the page in detail. 

## Troubleshooting Video {#section_9D3E12A8238E414B9C4241D1528FA1FB}

The following video demonstrates tools to troubleshoot [!DNL  Target]: 



<table id="table_5D6D1E2890AE4415BB7A998BFBCECA50"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Tools for Troubleshooting Adobe Target </th> 
   <th colname="col3" class="entry"> 14:14 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/OXznmfKjxwU/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/OXznmfKjxwU/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_744189D183E1464DB503DABBEE6AD191"> 
      <li id="li_60D93D321E0C4220BAE46E3CA43699E2">Use native browser tools for inspecting mbox requests </li> 
      <li id="li_4610283D0A4649469C0D88FCE8F6D47A">Use the Marketing Cloud Debugger, mboxTrace, and ttMETA </li> 
      <li id="li_297A797915ED4278BC17340951024427">Understand the Target timeout </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Retrieve the Authorization Token to Use With Debugging Tools {#section_BED130298E794D1FA229DB7C3358BA54}

Because mboxTrace and mboxDebug can expose campaign data and profile data to external parties, an authorization token is required. The authorization token can be retrieved in the [!DNL  Target] UI. The token is valid for six hours. 

To retrieve the authorization token: 


1. Click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] **. 

1. Select ** [!UICONTROL  mbox.js] ** or ** [!UICONTROL  at.js] **. 

1. Click ** [!UICONTROL  Generate Authentication Token] **. 

   ![](../graphics/gen-auth-token.png) 

1. Add the generated token as a parameter to your URL to enable one of the advanced debugging tools. 



## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace enables you to receive trace information attached to mbox replies. Trace information reflects the outcome of an mbox call (for example, a conversion or an impression) and any additional data that may help in determining why this particular outcome happened, such as a set of available branches among which the selection was made in a campaign. Use this information to debug content delivery. 

The following parameters are available: 



<table id="table_91A8471DD2FC4D4CB3CFB9FF0E11C5DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> mboxTrace Options </th> 
   <th colname="col2" class="entry"> Outcome </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ?mboxTrace=console </td> 
   <td colname="col2"> <p>Prints into console log as objects </p> <p>For <span class="filepath"> at.js </span>, instead of popping a new browser window or outputting to the console as in <span class="filepath"> mbox.js </span>, you will need to inspect the Network request and look under Preview (Chrome) or Response (Firefox). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ?mboxTrace=json </td> 
   <td colname="col2"> <p>Prints into console log as a literal JSON string </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ?mboxTrace=window </td> 
   <td colname="col2"> <p>Prints into a popup window as a JSON string </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ?mboxTrace=disable </td> 
   <td colname="col2"> <p>Turns off tracing session mode </p> </td> 
  </tr> 
 </tbody> 
</table>

**Example mboxTrace Call** 

` http://www.mysite.com/page.html?mboxTrace=window&amp;amp;authorization=f543abf-0111-4061-9619-d41d665c59a6` 

The output displays very detailed information about your content. mboxTrace shows details about your campaign or activity and profile It also provides a snapshot of the profile before execution, and a snapshot of what changed after execution. It also shows which campaigns or activities were evaluated for each location. 

Some of the information includes matched and unmatched segment and target IDs: 


* **SegmentId**: The IDs of segments, either from the reusable segments library or anonymous ones created for the particular campaign. 

* **TargetId**: The IDs of targets, either from the target expression library or anonymous targets for any segments from campaign. 

* **Unmatched**: The request did not qualify in this call for those segments or targets. 

* **Matched**: The request qualified for the specified segments or targets. 



**Using mboxTrace on Recommendations pages**: Adding mboxTrace as a query parameter on pages with recommendations replaces the Recommendations design on the page with an mboxTrace details window, which displays in-depth information about your recommendations, including: 


* Recommendations returned vs. recommendations requested 

* The key used, and if it is generating recommendations 

* Criteria-generated recommendations vs. backup recommendations 

* Criteria configuration 

* Exclusions and inclusions applied 

* Collection rules 



You do not need to include , , or  in the query parameter. When you are done with the mboxTrace details, add  and press ** [!UICONTROL  Enter] ** to return to the normal display mode. 

The normal functioning and appearance of your site is not affected by mboxTrace. Visitors will see your regular Recommendations design. 

## mboxDebug {#section_DC92A0E4388A4A2787365AD9D556FEFA}

To use mboxDebug, append an mboxDebug parameter to the end of your URL. The following table contains information about mbox-related URL parameters. 


>[!NOTE]
>
>Some mboxDebug parameters are available with or without authentication.





<table id="table_A39547BF527643BCBD168B7B2085D881"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> URL Parameters </th> 
   <th colname="col2" class="entry"> Purpose </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxDebug=1 </span> </p> </td> 
   <td colname="col2"> <p>Debugger </p> <p>Adding this parameter to any URL with mboxes defined opens a pop-up window with valuable debugging details. Cookie information, PCid and Session ID values are written out, and all of the mbox URLs are visible. Click on a mbox URL to show the response for that mbox. More details are available in <a href="https://marketing.adobe.com/resources/help/en_US/tnt/pdf/mbox_debug.pdf" scope="external" format="html"> mbox_debug.pdf </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxDebug=x-cookie </span> </p> </td> 
   <td colname="col2"> <p>Modify the cookie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxDisable=1 </span> </p> </td> 
   <td colname="col2"> <p>Disable mboxes on the page </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxDebug=x-profile </span> </p> </td> 
   <td colname="col2"> <p>View profiles set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxDebug=x-time </span> </p> </td> 
   <td colname="col2"> <p>Show response time for each mbox request </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxOverride.browserIp= <span class="varname"> Insert IP address </span> </span> </p> </td> 
   <td colname="col2"> <p>Test geotargeting </p> <p>Test geotargeting with this URL parameter. Type an IP address as the value for this attribute, and Test&amp;amp;Target's geotargeting evaluates that IP address to match against any geotargeting or segmentation set in a campaign. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Adobe Marketing Cloud Debugger {#section_A2798ED3A431409690A4BE08A1BFCF17}

The Adobe Marketing Cloud Debugger is installed as a bookmarklet in your browser. To install the debugger, follow the [ Adobe Debugger installation instructions ](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger_install.html). Open the debugger on the page you want to troubleshoot. The debugger does not require parameters or an authorization token. 

![](graphics/Screen_AdobeMktCldDebug.png) 

## If target.js Fails to Load During Delivery {#section_ABBA5EFDFFB749D8BEE172DB1F973058}

Mbox.js sends a cookie called "em-disabled" to the visitor if target.js fails to load during delivery. This cookie prevents offers created using the Visual Experience Composer from rendering on the site. Visitors with this cookie neither see the test content nor get counted in those activity reports. All other offer content (from campaigns in Target Classic for example) continues to load. The cookie has a lifetime of 30 min from the time of load failure. 

## Top sellers are not appearing in Recommendations {#section_3920C857270A406C80BE6CBAC8221ECD}

The * ` SIteCatalyst: purchase` * mbox can't be used for Purchase algorithm traffic data. Use the * ` orderConfirmPage` * mbox instead. 

## Check Activity Priority {#section_3D0DD07240F0465BAF655D0804100AED}

Form-based activities created with [!DNL  Target Standard/Premium] might collide with activities created in the [!DNL  Target Classic] UI that have the same priority and use the same mbox. 

## Custom code does not produce the expected results in Internet Explorer 8. {#section_FAC3651F19144D12A37A3E4F14C06945}

Target no longer supports IE 8. 

## JavaScript content delivered by the global mbox doesn't load when using mbox.js . {#section_03EC9B9C410B4F52A7FCD81840311709}

Upgrade to [!DNL  mbox.js] version 58 or later. 

Mbox.js version 58 and later executes non-JavaScript content for the global mbox immediately after the HTML ` BODY` tag is present. JavaScript content inside ` &amp;lt;script&amp;gt;` tags for the global mbox executes after the ` DOMContentLoaded` event is fired. This order of content delivery ensures that JavaScript content for the global mbox is delivered and rendered properly. 

## Target Cookie Does Not Get Set {#section_77AFEB541C0B495EB67E29A4475DF960}

If your site has a sub domain, such as [!DNL  us.domain.com], but you need the Target cookie set on [!DNL  domain.com] (instead of [!DNL  us.domain.com]), you must override the ` cookieDomain` setting. For more information, see [ targetGlobalSettings() ](c_target-ats-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506) 

## Target content flickers or is not shown if an element is also part of AEM personalization. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

If a DOM element is part of Adobe Experience Manager (AEM) personalization targeting and a Target activity, Target content might flicker or not be shown. 

To remedy this, you can disable AEM personalization on pages on which Target is running. 
