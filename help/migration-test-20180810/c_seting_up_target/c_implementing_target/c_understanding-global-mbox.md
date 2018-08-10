---
description: Information about the global mbox, a name used to refer to the single server call made at the top of each web page in your Target implementation.
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;global;global mbox
seo-description: Information about the global mbox, a name used to refer to the single server call made at the top of each web page in your Target implementation.
seo-title: Understanding the Global mbox
solution: Target
subtopic: Getting Started
title: Understanding the Global mbox
topic: Standard
uuid: 32390916-9b48-46f4-bbfb-2b52d9643cec
index: y
internal: n
snippet: y
translate: y
---

# Understanding the Global mbox

## Understanding the Global mbox {#concept_76AC0EC995A048238F3220F53773DB13}Information about the global mbox, a name used to refer to the single server call made at the top of each web page in your 
<keyword>
  Target 
</keyword> implementation.By default, the global mbox is named [!DNL  target-global-mbox]. It can be renamed for your account, if necessary. 

There are several differences between a regular mbox (non-global mbox) and the global mbox, including: 



<table id="table_D849378A87FE478487DA11581D274F61"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Regular mbox </th> 
   <th colname="col2" class="entry"> Global mbox </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A regular mbox typically wraps around content with a <span class="codeph"> &amp;lt;DIV&amp;gt; </span> tag. </p> </td> 
   <td colname="col2"> <p>The global mbox is "empty" and does not wrap around any content. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Content from only one activity can be delivered in a regular mbox. </p> </td> 
   <td colname="col2"> <p>Content from multiple activities can be delivered in one response to a global mbox. </p> </td> 
  </tr> 
 </tbody> 
</table>

If multiple activities are delivered via the global mbox or via multiple regular mboxes, [!DNL  Target] [ determines the priority ](c_activities.md#concept_1780C11FEA57440499F0047DD6900E0F) by which the activity (or activities) are delivered to a web page. 

Additional page-level data can be sent to [!DNL  Target] along with the global mbox by using the ` targetPageParams` function. This is similar to the mbox parameter functionality. For more information, see [ Passing Parameters to a Global mbox ](c_understanding-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5). 
>## Customize a Global mbox {#task_8FE8D068DE924B3B96A784643015D830}Information to help you customize a global mbox for both 
<filepath>
  at.js 
</filepath> and 
<filepath>
  mbox.js 
</filepath>. 
<draft-comment otherprops="merge">
  ov/t_customize-global-mbox.xml 
</draft-comment>
>1. Edit mbox.js.

>       Go to ** [!UICONTROL  Target] ** > ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] **. 

>    
>    * For mbox.js, click ** [!UICONTROL  Edit mbox.js Settings] **.
>    * For [!DNL  at.js], select ** [!UICONTROL  at.js] ** under the Implementation Method, and then click ** [!UICONTROL  Edit mbox.js Settings] **.


>       ![](graphics/step-1-edit-mboxjs.png) 
>1. Edit [!DNL  mbox.js] or [!DNL  at.js].

>       Disable ** [!UICONTROL  Auto create global mbox] **, then add the name of the custom global mbox that you would like to use to deliver activities from [!DNL  Target Standard/Premium]. This custom global mbox is also used for click tracking. 

>       ![](graphics/step-2-edit-mboxjs-or-atjs.png) 

>       Click ** [!UICONTROL  Save] ** when you are finished. 
>1. Implement the [!DNL  mbox.js] or [!DNL  at.js] library on your site.

>    
>    * For mbox.js, see [ mbox.js Implementation ](t_mbox_download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420).
>    * For at.js, see [ at.js Implementation ](c_target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17).

>1. Time the transition with your release.

>       As soon as you are ready for [!DNL  Target Standard/Premium] to start using your global mbox for all activities moving forward, you can proceed with this step. 

>       Update the name of the custom global mbox to match the name used in Step 2, above. 

>       ![](graphics/step-4-time-the-transition-with-your-release.png) 


>       >[!IMPORTANT]
>       >
>       >When you save, all activities in your account sync with this mbox. If this mbox is not on your site, all activities will stop functioning.


>       Click ** [!UICONTROL  Save] **. 
>## Using a Global mbox from a Legacy Implementation {#task_D9189CE28B2540B187CE6D6F4C590B39}By default, 
<keyword>
  Target Standard 
</keyword> creates a global mbox called 
<codeph>
  target-global-mbox 
</codeph>, which is used to run activities created in 
<keyword>
  Target Standard 
</keyword>. However, if you have already created a global mbox on your pages for your legacy implementations, you can use that mbox for your 
<keyword>
  Target Standard 
</keyword> activities. 
<draft-comment otherprops="merge">
  ov/t_mbox_global_target_standard.xml 
</draft-comment>
>[!NOTE]
>
>You can have only one global mbox per account.



To use your existing global mbox for both [!DNL  Target Standard] and your legacy implementation, you must set a few parameters. 

>1. Go to [!DNL  Target Standard], then click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Implementation] **.

>       By default, [!UICONTROL  Auto Create Global Mbox] is enabled, and the custom global mbox is named ` target-global-mbox`. 
>1. If you want to use an existing mbox, disable [!UICONTROL  Auto Create Global Mbox], and specify the name of a previously created global mbox in the [!UICONTROL  Custom Global Mbox] field.

>       The [!UICONTROL  Custom Global Mbox] drop-down lists all mboxes in your account. If you want to use an mbox that does not yet exist, create the mbox in Target Classic. 
>1. Click ** [!UICONTROL  Save] **.

>       The mbox.js settings for your account are updated. 
>1. Download the new ` mbox.js` file and reference it on your site.

>       After you've updated your production site with the new ` mbox.js` file, you are ready to set your preferences. 
>1. Click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Preferences] **.
>1. In the [!UICONTROL  Custom Global Mbox] field, specify the name of the global mbox you selected on the Implementation page.
>1. Click ** [!UICONTROL  Submit] **.

>       All existing activities update to use the specified global mbox, including activities that have previously been created and implemented. 
>## Passing Parameters to a Global mbox {#concept_33362A04146C4E3C8E7089B65F38B5E5}The JavaScript 
<codeph>
  targetPageParams 
</codeph> function is used to pass parameters to the global mbox. This is needed in any scenario where additional targeting/context information is to be passed into Target. 
<draft-comment otherprops="merge">
  ov/c_pass_parameters_to_global_mbox.xml 
</draft-comment>

For example, in a Recommendations activity, use the parameters to represent the current product or category that is being viewed. 

The code to call the JavaScript function must come before the global mbox on the page, whether the global mbox is fired as a part of mbox.js or is manually included in the page code. 

You can pass in parameters to ` target-global-mbox` using the ` targetPageParams()` function in any of the following ways: 


* An array
* A JSON object
* An ampersand-delimited list


Use these three methods to verify that the parameters are being passed correctly. You might also be able to verify the passing of parameters using the [ Adobe Marketing Cloud Debugger ](c_manage_content.md#concept_D2548B486C984B1E97ED7A72075B8EEA). 

You must define the JavaScript function before adding the global mbox to the page. The name must be ` targetPageParams`. 

**Query String** 


```
p1=v1&amp;amp;p2=v2&amp;amp;p3=hello%20world
```



* Name: ` targetPageParams`
* Return value: a "&amp;" delimited parameters, with URL encoded parameter values. Example: 

  In this example, p3 has the value ` hello world`, which is URL encoded. 



The following is an example of how the code for the page might look: 


```
<html> 
  <head> 
    <title>Title here..</title> 
    <script type="text/javascript"> 
        function targetPageParams() { 
           
<b>return&amp;nbsp;"p1=v1&amp;amp;p2=v2&amp;amp;p3=hello%20world"</b>; 
        } 
    </script> 
    <script src="mbox.js" type="text/javascript"></script> 
  </head> 
  <body>Body here... 
  </body> 
</html>
```


This example sends the following data to the mbox edge: 


* p1=v1
* p2=v2
* p3=hello world


**Array** 


```
<!--window.-->targetPageParams = function() { 
  return ["a=1", "b=2", "c=hello world"]; 
}; 

```


Values do not need to be URL encoded. For example, if a value contains a space, there is no need to encode the space. 

This example sends the following data to the mbox edge: 


* a=1
* b=2
* c=hello world


**JSON** 

JSON is a powerful way to pass parameters. Target uses the JSON object keys to flatten complicated structures into simple parameters. 


```
<!--window.-->targetPageParams = function() { 
  return { 
    "a": 1, 
    "b": 2, 
    "profile": { 
                  "memberStatus": Gold, 
                  "country": { 
                                "city": "San Francisco" 
                            } 
              } 
  }; 
}; 

```


Values do not need to be URL encoded. For example, "San Francisco" does not require the space to be encoded. A space suffices. 

This example sends the following data to the mbox edge: 


* a=1
* b=2
* ` profile.age`=26
* ` profile.country.city`=San Francisco


**Using DTM to Add mbox Parameters** 

This video explains how to add mbox parameters using DTM. 



<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Adding mbox Parameters via Activation (DTM) </th> 
   <th colname="col3" class="entry"> 4:25 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/hA0MctwZKlg/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/hA0MctwZKlg/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F">Map a static name/value pair to a parameter or profile parameter in the target-global-mbox </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">understand the basics of a data element </li> 
      <li id="li_6C4D1871E45D40118D7D9D4DF81547B5">Map a dynamic data element value to a parameter or profile parameter in the target-global-mbox </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Global mbox Frequently Asked Questions {#concept_246B0FCF5A7542879DA6613C0C59267F}List of frequently asked questions (FAQs) about global mboxes. 
<draft-comment otherprops="merge">
  ov2/c_global-mbox-frequently-asked-questions.xml 
</draft-comment>
## Can I have more than one global mbox if my Target account is set across multiple domains? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

Only one global mbox is supported across your account. 

You can limit where your activities run by adding URL rules to your activities. For more information, see [ Include the Same Experience on Similar Pages ](c_experiences.md#task_2539D51A18044F82B0D9895636546781). 

You could also pass a parameter on the page using ` [ targetPageParams() ](c_target-ats-functions.md#reference_B235C9F6DA79449ABE3E23F914FEABAE)` and then select those parameters in the "configure URL" section in the [!UICONTROL  Visual Experience Composer] (VEC) or by adding the parameters as "refinements" in the Form-Based Experience Composer. 

## How do I pass revenue data on a Target global mbox? {#section_17AEA933BADA4D169CCEDF5833C41306}

To collect revenue and order information on the target-global-mbox, "mbox parameters" must be sent to Target. These parameters are name/value pairs used to send more information to Target. Target automatically looks for these parameters (reserved names) to populate revenue data. 

For the ` orderConfirmPage`, you should pass in ` orderTotal`, ` orderId`, and ` productPurchasedId`. For more information, see [ Create an Order Confirmation mbox - mbox.js ](t_mbox_download.md#task_0036D5F6C062442788BB55E872816D82). 

These same parameters must be sent to the target-global-mbox via ` targetPageParams()`. For more information, see [ Passing Parameters to a Global mbox ](c_understanding-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5). 

You'll also want to add targeting to the conversion piece so that Target only counts conversions on the target-global-mbox when the order confirmation page has been viewed, as shown below: 

![](../graphics/revenue1.png) 

The Site Pages section illustrated above contains the following selections: Current Page, URL, contains, orderconfirm. 

![](../graphics/revenue2.png) 

The options in the above illustration include the following settings: 


* **What do you want to measure with this activity: **Revenue 

* **Default View for Reporting: **Revenue Per Visitor (RPV) 

* **What action was taken by your audience to indicate your goal has been reached? **Viewed an mbox, target-global-mbox 


