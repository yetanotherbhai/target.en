---
description: The Automated Personalization activity workflow varies from the workflow of the other activity types.
keywords: automated personalization;Audiences;ensemble;random forest;residual variance;error variance;lifetime value
seo-description: The Automated Personalization activity workflow varies from the workflow of the other activity types.
seo-title: Creating an Automated Personalization Activity
solution: Target
title: Creating an Automated Personalization Activity
topic: Advanced
uuid: 7dd1f7d5-e73a-47bb-a3ce-6a189c6227a8
index: y
internal: n
snippet: y
translate: y
---

# Creating an Automated Personalization Activity


>1. From the Target Standard Activities list, click ** `Create Activity` ** > ** `Automated Personalization` **.

>       ![](../graphics/ap_create.png) 
>       If you prefer to use the Form-Based Experience Composer, select that option. See [Form-Based Experience Composer](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html). 
>1. Verify or enter the activity URL, then click ** `Next` **.


>       >[!NOTE]
>       >
>       >`Target` does not differentiate between URL protocols ( `https` and `http`). As a result, `https://adobe.com` and `http://adobe.com` both match. 

>       The page with the specified URL opens in the Visual Experience Composer.
>       ![](../graphics/ap_url.png) 
>       For troubleshooting information about the VEC, should you have problems, see [Troubleshooting the Visual Experience Composer](r_troubleshoot_composer.md#reference_77743144F10143A3A89D56E116D296E4). 
>1. To name the activity, click the Name field and type your activity name.

>       ![](../graphics/ab_newname.png) 
>       The following characters are not allowed in an activity name:

>       | Character |Description |
>       |---|---|
>       | / |Forward slash |
>       | ? |Question mark |
>       | # |Number sign |
>       | : |Colon |

>1. Modify page elements as explained in [Experiences](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), then click ** `Next` **.

>       You can select multiple images at once from the asset manager. This enables you to quickly view the page with each of the images configured for the activity. You can also easily edit text elements in your offers. When you edit an element, bars appear on that element to indicate you have changed it.

>1. Click ** `Content` ** to configure the available combinations.

>       ![](../graphics/ap_content.png) 

>       >[!NOTE]
>       >
>       >You can create up to 30,000 experiences in an AP test.

>       The Content list shows each piece of content selected for the activity, and the location it is assigned to. You can select pieces of content and assign them to reporting groups.
>       For information about targeting an offer to specific audiences, see [Target AP Offers](t_ap_target_offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E). 
>1. Click ** `Combinations` ** in the Content list to choose any combinations of elements that you want to exclude from the activity.

>       ![](../graphics/ap_combos.png) 

>       >[!NOTE]
>       >
>       >You can include up to 30,000 combinations.

>       Click ** `Filter` ** to create a filter that shows only the combinations you want to see. 
>       Click ** `Exclude` ** to hide a combination. Excluded combinations are never displayed. Click ** `Include` ** to include a previously excluded combination. 
>       Use the Display drop-down to filter the list of combinations to show all combinations, included combinations only, or excluded combinations only.
>       ![](../graphics/ap_display.png) 
>1. Click ** `Continue` ** when you have finished setting up the content of your activity.

>       The Activity Summary appears.
>       Click ** `View Experience URLs` ** to preview how your experiences will look when delivered. A pop-up appears that you can use to view and share links to your AP experiences on your site to get a "true preview" of the experiences outside of Target's Visual Experience Composer. You must share the links from the message to share the preview. Clicking a link and then copying the URL directly from the page won't work because the URL contains a parameter that only displays the page correctly when you access the page from the link in the message. 
>1. Select an audience and specify the percentage of visitors who will see the control experience, then click ** `Next` **.

>       The control experience provides a comparison to determine how much lift is provided by the automated test.
>       Automated Personalization always measures performance against a control group. Best practice is to place 5-10% of entrants into the control group, and display the default content to them.

>       >[!NOTE]
>       >
>       >In Automated Personalization activities, entry criteria (URL targeting, template rules, audience target) are evaluated for each request. In previous versions, entry criteria were evaluated once per session.

>1. Configure the control experience.

>       You can choose from the following control experiences:
>    
>    * Default Experience The default page design is used as the default experience.

>    * Randomized Experience (default) The modeling system randomly creates an experience from the offers and locations used for that page. The visitor continues to see that experience until the session expires. If the visitor returns and begins a new session, a new random experience is generated.

>    * Selected Experience You select the experience by choosing the content that displays in each location.
>      If, after creating the activity, you delete a location from the control, your activity will reset. Because the control is different, the activity must reset to provide accurate data using the new control.

>1. Review the Experiences card.

>       The Experiences card lists each location in the experience and shows the numbers of offers available for each location.
>1. Click ** `Continue` **.

>       The Goal &amp; Settings page opens.
>1. Configure the activity with the following settings, then click ** `Create` **.


>    <table id="table_136C5D05E9A544C6977050EC50B9F49B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Setting</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Name</td> 
   <td colname="col2"> <p>Name the activity. Give the activity a name that is descriptive enough that team members can recognize it in the Activities list.</p> <p>The following characters are not allowed in an activity name:</p> <p> 
     <ul id="ul_5710602E3CF24EAD9C2C6BF10B83841F"> 
      <li id="li_1E06CC79069F4A3C825FAEB5C32F6C9F">/</li> 
      <li id="li_0C716E01A8C74BE7BF540D21A249E692">?</li> 
      <li id="li_924D064F365C45B8B0F8AC15A23ABE3D">#</li> 
      <li id="li_E9F2F644FC5C4E9B91101745590DD6D8">:</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Objective</td> 
   <td colname="col2">(Optional) Type the objective of the test. The objective helps you remember the purpose of the activity.</td> 
  </tr> 
  <tr> 
   <td colname="col1">Priority</td> 
   <td colname="col2"> <p>Depending on your settings, the UI and options for <span class="wintitle">Priority</span> vary. You can use the legacy settings of Low, Medium, or High, or you can enable fine-grained priorities from 0 to 999. </p> <p>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.</p> <p>If this option is not enabled in <span class="wintitle">Setup</span> (the default), specify a priority: Low, Medium, or High. </p> <p> To enable fine-grained priorities, click <span class="wintitle">Setup</span>, then toggle the <span class="wintitle">Enable Fine-Grained Priorities</span> option to the "On" position. </p> <p>If this option is enabled, specify a value between 0 and 999:</p> <p> 
     <ul id="ul_FCA07A04D6F248759429BC46BA57CCE5"> 
      <li id="li_88F440506D22467295C71F2B14470AD7">0 = Low</li> 
      <li id="li_AEC7893759464944A6501FA742A2B0FE">999 = High</li> 
     </ul> </p> <p>For activities created in previous versions of <span class="keyword">Target Standard/Premium</span>, Low priority is converted to 0, Medium is converted to 5, and High is converted to 10. You can adjust these values as necessary. </p> <p> <p>Note: Before you can disable this option after using fine-grained priories, all priorities must be set back to 0, 5, and 10.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Duration</td> 
   <td colname="col2">Set the start and end dates for the activity.</td> 
  </tr> 
  <tr> 
   <td colname="col1">Optimization Goal</td> 
   <td colname="col2"> <p>Provide a name for the goal, then specify the optimization goal, which consists of two parameters:</p> <p> 
     <ul id="ul_F6238CFA3890414DAADB6896E17653B8"> 
      <li id="li_5366B2CCA42041F38C2B3888BEE3F7E8">What you want to measure with the activity</li> 
      <li id="li_A77B6CFF0A7E46EB9675CA5B4D22CAF3">The action taken by an activity entrant that shows that the goal has been achieved.</li> 
     </ul> </p> <p>Automated Personalization activities can measure conversion, RPV, and AOV. Conversion can be achieved by viewing a page or viewing an mbox. Clicks can also be tracked.</p> <p>The primary goal also becomes the modeling metric, used by the modeling system to calculate the success of te experience.</p> <p>Visitors can be kept in the activity for tracking purposes after reaching the modeling goal. For example, often an Automated Personalization activity is used to improve click-rates, and that is set as the modeling goal. However, it's important to see how increased click-rates lead to final conversion, so tracking through the final conversion is essential.</p> <p>You can provided dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increase.</p> <p>You must define both (or multiple) success metrics before you can make one dependent on another.</p> <p>The <span class="wintitle">Add Dependency</span> option allows the success metric to increment if another success metric has been reached or has not been reached. </p> <p>To add a dependency:</p> <p> 
     <ol id="ol_7CE86C31CD5541039A3265E14D0C3630"> 
      <li id="li_3E374D8B28B443FA9FE8AF2B02814A82"> <p>After adding additional metrics, click <span class="uicontrol">Advanced Settings</span>. </p> </li> 
      <li id="li_F65C369C8F354A6CBD447ED26D9F79E4"> <p>Click the <span class="uicontrol">Add Dependency</span> option: </p> <p style="text-align: center;"><img href="../graphics/add dependency.png" id="image_D3C6E4862509435E86A1F61B88F342CA" /> </p> </li> 
      <li id="li_9A6F187B4C294A9C8B5C834C76B32767"> <p>Drag and drop the desired metrics from the left pane into the right pane, then click <span class="uicontrol">Reached</span> to toggle the setting between <span class="uicontrol">Reached</span> and <span class="uicontrol">Not Reached</span>. </p> <p style="text-align: center;"><img href="../graphics/add dependency reached.png" id="image_CA136FD10D754BD1B26C621DF2A4858D" /> </p> </li> 
     </ol> </p> <p>You can edit or remove dependencies after adding them.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Conversion Metric</td> 
   <td colname="col2"> <p>Set the conversion metric.</p> <p>You can:</p> <p> 
     <ul id="ul_09EA8187A57D4924BA0069CE4157A4FA"> 
      <li id="li_4AD5D0C60BF348D2B9B8C1CD0CB9771F">Name the conversion metric.</li> 
      <li id="li_D1B104D6B3354CDE84D8DF8F964EC4A7">Set the conversion metric to be the same as the optimization goal.</li> 
      <li id="li_AB85CE2490EF4A6F901C38671FB8CA75">If not the same as the optimization goal, select a different method.</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Additional Metrics</td> 
   <td colname="col2"> <p>Add any additional reporting metrics you want to use. You can add conversion or revenue metrics.</p> <p> <p>Note: The Engagement metric is not supported as an additional metric as well. The UI might let you select the Engagement metric, but data will not display accurately in reports.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Audiences for Reporting</td> 
   <td colname="col2"> <p>Add audiences to enable filtering by audiences in reports. By default, the report shows results for all qualified visitors. Add audiences to filter results for more specific subsets of visitors.</p> <p> <p>Note: Unlike other activity types, Automated Personalization cannot use Adobe Analytics as its reporting source.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Notes</td> 
   <td colname="col2">Type any information about your activity that is useful to keep on hand for yourself or other team members. The Notes pane is resizable.</td> 
  </tr> 
 </tbody> 
</table>

