---
description: Target can exchange notifications with other Adobe Marketing Cloud solutions using Adobe Pulse.
keywords: Visual Experience Composer;VEC;carousel
seo-description: Target can exchange notifications with other Adobe Marketing Cloud solutions using Adobe Pulse.
seo-title: Notifications
solution: Target
subtopic: Multivariate Test
title: Notifications
topic: Standard
uuid: e434d591-65ba-46fb-95b1-f48885d13a7e
index: y
internal: n
snippet: y
translate: y
---

# Notifications

## Notifications {#concept_557351F8BB7D40F39A65951A77B79D62}<keyword>
 Target
</keyword> can exchange notifications with other 
<keyword>
 Adobe Marketing Cloud
</keyword> solutions using 
<keyword>
 Adobe Pulse
</keyword>.Notifications from `Target` can be seen in all solutions by users who have a `Marketing Cloud`product context of `Target Standard/Premium`. 
For information about setting up Notifications, see [Notifications](https://marketing.adobe.com/resources/help/en_US/mcloud/notifications.html) in the `Adobe Marketing Cloud` documentation. 
Access Notifications from anywhere in `Target`, except from within the activity creation workflow. Click the bell icon in the page header to display or hide the notifications widget. 
![](../graphics/notifications-shell.png) 
`Target` sends two kinds of notifications for all activity types: 

* When an activity becomes live and offer delivery begins: For example:
  ![](../graphics/notif_app.png) 

* When an activity is deactivated and offer delivery ceases: For example:
  ![](../graphics/notif-deact.png) 


Similar notifications also appear when a scheduled activity reaches its start date, and when it ends upon reaching its end date.
All `Target` notifications display the name of activity that was approved or deactivated, and include the words "Adobe Target" for easy identification. 
If a single activity sends multiple notifications of the same type, they are combined into a single card with the number of notifications displayed in it. For example:
![](../graphics/notif-multi.png) 
Click the notification card to view details of each individual notification.
For example, if you click the card shown above, the three notifications display:
![](../graphics/notif-multi-open.png) 

## Limitations {#section_B466EB20B2554CE7B1915374B39F4322}


* Notifications do not tell you who approved, deactivated, or imported the activity.
* MVT notifications appear as "A/B Test" because they are synchronized as A/B campaigns in `Target Classic`.

>## Creating Carousels that Work in the Visual Experience Composer {#task_C818CAF1189E4234BFB1B4CF4228100C}This topic shows how to create a carousel that can be edited in the Visual Experience Composer (VEC). 
<draft-comment otherprops="merge">
 target/t_vec-carousels.xml
</draft-comment>When you use the steps below, `Target` always knows that the selected slide will have the 'selector' for the correct slide, even if it is changed in the Visual Experience Composer after a few seconds. 

>1. Create static HTML placeholders.

>    
>       ```
>       <ul>
>       <li class="show"> slide 1 </li>
>       <li class="hidden"> slide 2 </li>
>       <li class="hidden"> slide 3 </li>
>       </ul>
>       ```

>1. Add CSS to design the look and feel.

>       Don't use JavaScript for this.

>       >[!NOTE]
>       >
>       >The `Render Using JavaScript` option is currently not supported if it is used along with custom code in the Visual Experience Composer. 

>1. Only update the classNames to hide others and show the next with timer/animation.

