---
description: Target enables you to track clicks on any element as a success metric.
keywords: Click tracking;track clicks;clicks;AppMeasurement
seo-description: Target enables you to track clicks on any element as a success metric.
seo-title: Click Tracking
solution: Target
subtopic: Getting Started
title: Click Tracking
topic: Standard
uuid: 2bd49512-d152-459f-abd0-58a93d6d31bb
index: y
internal: n
snippet: y
translate: y
---

# Click Tracking


<a id="section_AC7098C369144B2080697986FA6BAD7B"></a>

This section contains the following information: 


* [ Training Video ](t_click_tracking.md#section_36607204DAE146E3B8E2C609D244EDB1) 

* [ Setting Up Click Tracking ](t_click_tracking.md#section_5540C5A533114E57BAE022A600B02E72) 

* [ Considerations ](t_click_tracking.md#section_DD49EBA86CC5475E96BA87D2468FDB36) 




>[!NOTE]
>
>Tracking clicks is not supported on the target global mbox when it is used as a location in a form-based activity.



## Training Video {#section_36607204DAE146E3B8E2C609D244EDB1}

This video includes information about creating click-tracking success metrics. 

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Metrics </th> 
   <th colname="col3" class="entry"> 7:43 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/oCMD2SymhoI/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/oCMD2SymhoI/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Understand "goal" metrics </li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405">Understand and build Conversion, Revenue, and Engagement metrics </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Build a click-tracking metric </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Setting Up Click Tracking {#section_5540C5A533114E57BAE022A600B02E72}


1. When setting your goals on the [!UICONTROL  Goals &amp;amp; Settings] page for your activity , select the ** [!UICONTROL  Conversion] ** success metric. 

1. For the action, select ** [!UICONTROL  Clicked an element] **, then click ** [!UICONTROL  Select elements] **. 

   Your page opens in the [!UICONTROL  Visual Experience Composer] (VEC). 

1. Select any elements that you want to track. 

   See the Considerations section below for tips on selecting elements. 

1. Click the check mark at the top of the screen to save your selections. 



When an activity entrant clicks a selected element, that click is counted as a conversion. 

## Considerations {#section_DD49EBA86CC5475E96BA87D2468FDB36}

There are several things to consider when selecting elements: 


* You can browse to a different page to track clicks on a page where you might not be changing content. This different page must be included in the activity using the [ multipage feature ](c_multipage_activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) and [!DNL  at.js] or [!DNL  mbox.js] must be implemented on it. 

* If you select more than one element, if an entrant clicks on any one of the chosen elements, the click is counted. To count each item separately, set up individual success metrics for each element. 

* Make sure you select the level of element you want to track. For example, when specifying a button, make sure you select the link and not the button text. 

* Click events are sent to [!DNL  Target] on the same page as the click. 

* If the click-tracking metric is the Goal metric of an A4T activity, the visitor must click this element within 60 seconds of the page loading in order for the metric to track. 

* Click tracking does not work on elements that include escaped characters in their selectors, including the following: 



  |  Character  | Description  |
  |---|---|
  |  #  | Number sign or Hash  |
  |  :  | Colon  |
  |  .  | Period  |
  |  $  | Dollar sign  |
  |  [ ]  | Square brackets  |


* If you use [!DNL  at.js] click tracking and you also use Analytics AppMeasurement, [!DNL  at.js] click tracking cancels all other click event handlers. As a result, the AppMeasurement click handler never executes. 

[!DNL  at.js] has special handling for click tracking when the underlying element is an ` A` (link) tag or ` FORM` tag. 

  The following steps are executed by [!DNL  at.js] when the click tracking event is attached to an ` A` (link) tag or a ` FORM` tag: 

1. Invoke ` event.preventDefault()`. 

  2. Fire Target request. 

  3. On Target request success or error callback, execute default behavior: 
    * ` A` (link) tag: The default behavior is to navigate to the URL defined by HREF attribute. 

    * ` FORM` tag: The default behavior is to submit the form. 



  This default behavior might interfere with Analytics click tracking. If you are using Analytics, you should rely on Analytics for click tracking rather than Target. 


