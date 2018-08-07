---
description: Target enables you to track clicks on any element as a success metric.
keywords: Click tracking;track clicks;clicks
seo-description: Target enables you to track clicks on any element as a success metric.
seo-title: Click Tracking
solution: Target
subtopic: Getting Started
title: Click Tracking
topic: Standard
uuid: 5aa180e7-61e6-47ae-a26b-b77eaa17fd21
index: y
internal: n
snippet: y
translate: y
---

# Click Tracking


>1. When setting your goals on the `Goals &amp; Settings` page for your activity , select the ** `Conversion` ** success metric.
>1. For the action, select ** `Clicked an element` **, then click ** `Select elements` **.

>       Your page opens in the `Visual Experience Composer` (VEC). 
>1. Select any elements that you want to track.

>       There are several things to consider when selecting elements:
>    
>    * You can browse to a different page to track clicks on a page where you might not be changing content. This different page must be included in the activity using the[multipage feature](c_multipage_activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) and `at.js` or `mbox.js` must be implemented on it. 

>    * If you select more than one element, if an entrant clicks on any one of the chosen elements, the click is counted. To count each item separately, set up individual success metrics for each element.

>    * Make sure you select the level of element you want to track. For example, when specifying a button, make sure you select the link and not the button text.

>    * Click events are sent to `Target` on the same page as the click. 

>    * If the click-tracking metric is the Goal metric of an A4T activity, the visitor must click this element within 60 seconds of the page loading in order for the metric to track.

>    * Click tracking does not work on elements that include escaped characters in their selectors, including the following:


>      | Character |Description |
>      |---|---|
>      | # |Number sign or Hash |
>      | : |Colon |
>      | . |Period |
>      | $ |Dollar sign |
>      | [ ] |Square brackets |


>    * If you use `at.js` click tracking and you also use Analytics AppMeasurement, `at.js` click tracking cancels all other click event handlers. As a result, the AppMeasurement click handler never executes. 
>      If you are using Analytics for click tracking, `at.js` has special handling for click tracking when the underlying element is an `A` (link) tag or `FORM` tag. 
>      The following steps are executed by `at.js` when the click tracking event is attached to an `A` (link) tag or a `FORM` tag: 
>    1. Invoke `event.preventDefault()`. 
>      2. Fire Target request.
>      3. On Target request success or error callback, execute default behavior:
>    
>        * `A` (link) tag: The default behavior is to navigate to the URL defined by HREF attribute. 

>        * `FORM` tag: The default behavior is to submit the form. 


>      This default behavior might interfere with Analytics click tracking. If you are using Analytics, you should rely on Analytics for click tracking rather than Target.


>1. Click the check mark at the top of the screen to save your selections.
