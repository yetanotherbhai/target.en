---
description: Audiences determine who will see content and experiences in a targeted activity.
keywords: audience;audience rules;combine audiences;exclusion;add exclusion;exclude;combining audiences;adhoc audience;ad hoc audience
seo-description: Audiences determine who will see content and experiences in a targeted activity.
seo-title: Creating Audiences
solution: Target
title: Creating Audiences
topic: Advanced,Standard,Classic
uuid: 72d6d2bc-abff-4aea-862d-71c5fcd42378
index: y
internal: n
snippet: y
translate: y
---

# Creating Audiences

## Creating Audiences {#concept_65BE870D290E412D8BBF557EEA67C271}Audiences determine who will see content and experiences in a targeted activity.Audiences are used anywhere targeting is available. When targeting an activity, you can either select a reusable audience from the [!UICONTROL  Audiences] list, create an activity-specific audience and target it, or [ combine multiple audiences ](c_audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) to create an ad hoc audience. 

You can also use audience data collected by [!DNL  Analytics] for real-time targeting and personalization in [!DNL  Adobe Target] and other [!DNL  Marketing Cloud] solutions. See [ Audiences in the Marketing Cloud Product Documentation ](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html). 

This video includes information about using audiences. 

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Using Audiences </th> 
   <th colname="col3" class="entry"> 6:22 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/TAMBpW9vpOI/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/TAMBpW9vpOI/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532"> <p>Explain the term "audience" </p> </li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405"> <p>Explain the two ways audiences are used for optimization </p> </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A"> <p>Find audiences in the Audiences List </p> </li> 
      <li id="li_699D4D5D089A4FB7BA4C5E95337AC34A"> <p>Target an activity to an audience </p> </li> 
      <li id="li_87E7AFFEEC9C42ABB51C279221E17A14"> <p>Use audiences for passive reporting in an activity </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

[!DNL  Target] defines two types of audiences: 


* **Targeting Audiences: **Used to deliver different content to different types of visitors. 

* **Reporting Audiences: **Used to determine how different types of visitors respond to the same content so you can analyze your test results. 

  In [!DNL  Target], you can configure reporting audiences only if you use [!DNL  Target] as your reporting source. If you use [ [!DNL  Adobe Analytics] as your reporting source (A4T) ](a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE), you must configure your reporting audiences within [!DNL  Analytics]. 



To access the [!UICONTROL  Audiences] list, click ** [!UICONTROL  Audiences] ** in the top menu bar: 

![](graphics/audiences_list.png) 

The [!UICONTROL  Audiences] list contains all of the audiences that you can use in your activities. Use the [!UICONTROL  Audiences] list to create, edit, delete, copy, or combine audiences. The list also shows the source where the audience was created ( [!DNL  Target], [!DNL  Target Classic], [!DNL  Marketing Cloud], and so forth). Predefined audiences, such as "New Visitors" and "Returning Visitors," cannot be renamed. 

You can also target custom profile parameters and ` user.` parameters. When adding an audience, click ** [!UICONTROL  Visitor Profile] **, then under [!UICONTROL  Custom User Parameters] or [!UICONTROL  Custom Profile Parameters] in the [!UICONTROL  Visitor Profile] drop-down list, choose the parameter you use want to use to target your activity. If the desired parameter does not appear, the parameter has not been fired by an mbox. Other custom mbox parameters are available in the [!UICONTROL  Custom Parameters] drop-down list. 

Use the search box to search your [!UICONTROL  Audiences] list. You can search for any part of an audience name, or you can enclose a specific string in quotes. 

You can sort the [!UICONTROL  Audiences] list by audience name or by the date when it was last modified. To sort by name or date, click the column header, then select to display audiences in ascending or descending order. 

You can view audience definitions 

## Viewing Audience Definitions {#section_11B9C4A777E14D36BA1E925021945780}

You can view audience definition details on a pop-up card in various places in the Target UI without opening the audience. This functionality applies to audiences created in Target Standard/Premium and audiences imported from Target Classic or created via API. 

For example, the following audience definition card is accessed by hovering over an audience on the Audience List, then clicking the information icon: 

![](graphics/audience definition list.png) 

The following audience definition card is accessed by clicking the information icon on an activity's Overview page: 

![](graphics/audience definition.png) 

The following audience definition card is for an audience imported from the Adobe Marketing Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM). Notice that Target does not show detailed audience definition information because that information is not present in Target. 

![](graphics/audience definition mc.png) 

The following details are available for these imported audience types: 



<table id="table_BEE4E80E557B4BC9B703A5B80BF59F0F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Audience Type </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Mobile audience </p> </td> 
   <td colname="col2"> <p>Marketing Name, Vendor, and Model. </p> <p>The <span class="codeph"> matches|does not match </span> operator displays instead of <span class="codeph"> equals|does not equal </span>. </p> <p style="text-align: center;"> <img href="../graphics/imported mobile audience.png" id="image_D858836141D34047ABEBCE9FBE302826" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visitor-behavior audience </p> </td> 
   <td colname="col2"> <p>user.categoryAffinity: <span class="codeph"> categoryAffinity </span> with <span class="codeph"> FAVORITE </span> parameter. </p> <p style="text-align: center;"> <img href="../graphics/imported category affinity.png" id="image_117DA80E582F45ACB03B244798A24264" /> </p> <p>Monitoring: <span class="codeph"> Monitoring service equals true </span>. </p> <p>No Monitoring Service: <span class="codeph"> Monitoring service equals false </span>. </p> <p style="text-align: center;"> <img href="../graphics/imported monitoring.png" id="image_D63245B224C14837B5DDA33247394CB5" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences using the NOT operator </p> </td> 
   <td colname="col2"> <p>Single Rule: Target displays the audience in the format <span class="codeph"> [All Visitor AND [NOT [rule] </span>. Single NOT rule displays with AND with AllVisitor audience. </p> <p style="text-align: center;"> <img href="../graphics/imported not audience.png" id="image_E1D8B2BF23C64213984A58CFEF7951F4" /> </p> </td> 
  </tr> 
 </tbody> 
</table>

Keep the following points in mind as you work with imported audiences: 


* Expression target audiences are no longer supported in Target Standard/Premium. 

* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created. 


>## Creating an Audience {#task_E18BD77A9A8F4ED0AC50569F94556558}You can create customized audiences and save them to the 
<keyword>
  Target 
</keyword> library for use in your activities. You can copy an existing audience that you can then edit to create a similar audience and combine multiple audiences. 
<draft-comment otherprops="merge">
  target/t_create-audience.xml 
</draft-comment>This video includes information about creating audiences. 

<table id="table_AC2ED046B98C423994055438CA021858"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Audiences </th> 
   <th colname="col3" class="entry"> 9:58 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/wV9lVTSOxMk/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/wV9lVTSOxMk/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_115F242E72F445299958D3C82265B59D"> 
      <li id="li_B7FDC532F1F444E0A20ACB335ABB88DA"> <p>Create audiences </p> </li> 
      <li id="li_8529CB01E80B4C89B74287882AE0DA9D"> <p>Define audience categories </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Audiences are defined by rules that determine who is included or excluded from a [!DNL  Target] activity. An audience definition can include multiple rules and each rule can include multiple parameters. Complex audience definitions use the boolean operators AND and OR to combine rules and parameters to give you detailed control over which site visitors are counted as activity entrants. 

When you combine rules or parameters with AND, any potential audience member must meet *all* of the defined conditions to be included as an entrant. For example, if you define an OS rule AND a browser rule, only visitors using both the defined OS *and* the defined browser are included in the activity. 

When you combine rules or parameters with OR, any potential audience member need only meet any single defined condition to be included as an entrant. For example, if you define multiple mobile rules connected by OR, visitors meeting *any* of the defined criteria are included in the activity. 

You can mix both boolean operators to create complex rules; however, operators at the same rule level must match. The user interface automatically applies the correct operator. 

For example, the following rule targets visitors who use either Chrome or Firefox on a Windows computer: 

![](../graphics/audience_create.png) 


>[!NOTE]
>
>Be careful to avoid creating rules that exclude all potential audience members. For example, it is not possible for someone to visit a page using browser x AND browser y simultaneously.



**To create a new audience:** 

>1. Click ** [!UICONTROL  Audiences] ** in the top menu bar.

>       ![](graphics/audiences_list.png) 
>1. From the [!UICONTROL  Audiences] list, click ** [!UICONTROL  + Create Audience] **.
>   Or 

>   To copy an existing audience, from the [!UICONTROL  Audiences] list, hover over the desired audience, then click the ** [!UICONTROL  Copy] ** icon (  ![](graphics/icon_copy.png) ). You can then edit the audience to create a similar audience. 
>
>1. Type a descriptive audience name.
>1. Click ** [!UICONTROL  + Add Rule] **.

>       Rules make it possible to limit your audience to a subset of you site visitors. 
>1. Select a rule type.

>       Each rule type has its own parameters. See [ Categories for Audiences ](c_target_rules.md#concept_E3A77E42F1644503A829B5107B20880D) for more information on configuring each type of audience rule. 
>1. Define the rule parameters.
>1. Click ** [!UICONTROL  Save] **.

>       Newly created audiences appear in the list after a few seconds of processing delay. If the audience does not display immediately in the list, try searching for the audience or refresh the list. 
>## Creating an Activity-Only Audience {#concept_A6BADCF530ED4AE1852E677FEBE68483}Create activity-only audiences from within the three-step guided workflow when creating an activity. These ad hoc audiences can be used in other places within the same activity, but are not stored in the Audiences Library for use in other activities. 
<draft-comment otherprops="merge">
  target/creating-activity-only-audience.xml 
</draft-comment>Activity-only audiences provide the following benefits: 


* You can use activity-only audiences to create an audience that you want to use only once and you do not want to store it in the Audience Library. This prevents the Audience Library from being cluttered with audiences that you never want to use again. 

* Activity-only audiences are not visible in the Audience Library. Because of this, they are shielded from unwanted changes by others in your organization. 



**To create an activity-only audience:** 


1. While creating an activity, in the ** [!UICONTROL  Audience] ** box, click the ** [!UICONTROL  Edit] ** icon (  ![](https://marketing.adobe.com/resources/help/en_US/target/graphics/icon_more_options.png) ), then click ** [!UICONTROL  Replace Audience] **. 

   ![](graphics/replace audiience.png) 

1. On the Choose Audience page, click ** [!UICONTROL  Activity Only Audience] **. 

   ![](graphics/activity-only-aud.png) 

1. Click ** [!UICONTROL  Create Audience] **. 

1. Type a descriptive audience name. 

1. Click ** [!UICONTROL  + Add Rule] **. 

   Rules make it possible to limit your audience to a subset of you site visitors. 

1. Select a rule type. 

   Each rule type has its own parameters. See [ Categories for Audiences ](c_target_rules.md#concept_E3A77E42F1644503A829B5107B20880D) for more information on configuring each type of audience rule. 

1. Define the rule parameters. 

1. Click ** [!UICONTROL  Save] **. 



Keep the following information in mind as you work with activity-only audiences: 


* You can create activity-only audiences in the Visual Experience Composer (VEC) or in the Form-Based Experience Composer. This functionality replaces refinement rules in previous versions of Target. 

* You can create an activity to store in the Audience Library for reuse in other activities or you create an activity-only audience. After saving the audience, you cannot change the audience type. 

* Refinements for existing activities are migrated to activity-only audiences. 

* Activity-only audiences have a status of Used or Unused. Unused activity-only audiences display until the activity is saved. If left unused and you try to save the activity, a warning message displays informing you that unused activity-only audiences will be deleted. 

* You can view audience definition details on a pop-up card accessed from the audience picker without opening the audience. 

* You can [ combine multiple audiences ](c_audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) to create activity-only audiences. 


>## Combining Multiple Audiences {#concept_A7386F1EA4394BD2AB72399C225981E5}Combine multiple audiences (including 
<keyword>
  Adobe Marketing Cloud 
</keyword> audiences and 
<keyword>
  Target 
</keyword> audiences) on the fly to create ad hoc audiences. You can also create exclusion rules and exclude audiences from a rule. 
<draft-comment otherprops="merge">
  target/c_combining-multiple-audiences.xml 
</draft-comment>Suppose that you have a "New Visitors" audience and a "Chrome Users" audience. For a specific activity, you might want to combine these existing audiences to target new visitors using Chrome browsers. Instead of creating a third audience and storing it in the [!UICONTROL  Audiences] library, you can combine these two audiences during activity creation or while editing an existing activity. 

As another example, you can target all loyalty customers by including a specific [!DNL  Audience Manager] segment for loyalty status and combining it with a [!DNL  Target] segment made up of people who signed up for your loyalty program during the current session, instead of creating a third, permanent audience. 

You can combine up to ten audiences using AND and OR operators. 

You can create and use combined audiences in various places throughout the [!DNL  Target] UI. 

## Create a Combined Audience While Creating an Activity {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

You can create an ad hoc combined audience on the activity's [!UICONTROL  Target] page during the three-step guided workflow. 


1. While creating an [ activity ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), on the ** [!UICONTROL  Target] ** page, click the ** [!UICONTROL  Edit Audience] ** icon (  ![](../graphics/icon_edit_audience.png)), then click ** [!UICONTROL  Change Audience] **. 

   ![Step Result](graphics/edit_audience.png) 

1. On the [!UICONTROL  Choose Audience] page, select the check boxes next to the desired audiences that you want to use as building blocks for your combined audience. 

   ![Step Result](graphics/combine_multiple_audiences1.png) 

1. Click ** [!UICONTROL  Combine Multiple Audiences] ** in the top right corner. 

   ![Step Result](graphics/combine_multiple_audiences2.png) 

1. (Conditional) Edit the new combined audience as desired. 

   The [!UICONTROL  Edit Audience] dialog box lets you drag and drop additional audience building blocks from the left side into the new combined audience as well as add exclusion rules and exclude audiences. 

    1. You can use drag-and-drop functionality to add audiences within an existing section as a level 2 building block. To add a level 1 building block, select the check box next to the desired audience, then click ** [!UICONTROL  Add to Rules] **. 

       For example, suppose in the previous example, you now want to include Firefox users in the combined audience. Search for and drag the "Browser: Firefox" audience into the "Browser: Safari" box on the right side, as in the following example: 

       ![](graphics/combine_multiple_audiences3.png) 

       Notice that the operator between the two browser-type audiences is "AND." Select the And drop-down list and change it to "OR" to create a new combined audience for new visitors using either Safari or Firefox. Be careful to avoid creating rules that exclude all potential audience members. For example, it is not possible for someone to visit a page using browser x AND browser y simultaneously. 


       >[!NOTE]
       >
       >The operator (AND or OR) must remain the same as you combine audiences. You cannot mix &amp;amp; match operators.


    1. To add an exclusion to a rule, click ** [!UICONTROL  Exclusion] ** > ** [!UICONTROL  Add Exclusion] **. 

       ![](graphics/combine_multiple_audiences3a.png) 

       Drag and drop an audience in the box: 

       ![](graphics/combine_multiple_audiences3b.png) 

       For example, to exclude San Francisco visitors from new visitors, you could drag the San Francisco audience into the box, as shown below: 

       ![](graphics/combine_multiple_audiences3b2.png) 

       This combined audience includes all new visitors to your site (excluding those from San Francisco) using Safari or Firefox. 

    1. To exclude an audience from a rule, click ** [!UICONTROL  Exclusion] ** > ** [!UICONTROL  Exclude this Audience.] **. 

       For example, you could create a combined audience that includes all new visitors to your site, excluding those using Firefox. Excluding visitors using Firefox is easier and quicker than creating a combined audience that explicitly includes multiple browsers (Safari, Chrome, and Internet Explorer), but does not include Firefox. 


1. Provide a descriptive name for the combined audience, then click ** [!UICONTROL  Save] **. 



## Create a Combined Audience for Use in Metric Targeting {#section_A42E795AFCBD4575809C5942039910F0}

You can create an ad hoc combined audience on the activity's [!UICONTROL  Goals &amp;amp; Settings] page to use in metric targeting. For example to create targeting based on conversion using a combined audience: 


1. While editing or creating an [ activity ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), on the ** [!UICONTROL  Goals &amp;amp; Settings] ** page, select ** [!UICONTROL  Conversion] ** for the success metric, then select ** [!UICONTROL  Viewed an Mbox] ** as the action. 

1. Select the desired mbox in the ** [!UICONTROL  Search mbox] ** field. 

   ![](graphics/combine_multiple_audiences4.png) 

1. Click the gear icon (  ![](graphics/icon_gear.png) ), then click ** [!UICONTROL  Add Audience Targeting] **. 

1. Click the ** [!UICONTROL  Add Audience/Targeting Condition] ** link to display the [!UICONTROL  Choose Audience] dialog box. 

   ![](graphics/combine_multiple_audiences5.png) 

1. Proceed with [ Step 2 ](c_audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) under "Create a Combined Audience While Creating an Activity" to create the combined audience. 



## Create a Combined Audience for Use in Reporting {#section_4682D342EFBB43C38E54B99B3A1E14CD}

You can create an ad hoc combined audience on the activity's [!UICONTROL  Goals &amp;amp; Settings] page to use in reporting. 


1. While editing or creating an [ activity ](c_activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), on the ** [!UICONTROL  Goals &amp;amp; Settings] ** page, click the ** [!UICONTROL  Add Audience] ** icon (  ![](../graphics/icon_plus_sign.png) ) under [!UICONTROL  Audiences for Reporting] to display the [!UICONTROL  Choose Audience] page. 

   ![](graphics/combine_multiple_audiences6.png) 

1. Proceed with [ Step 2 ](c_audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) under "Create a Combined Audience While Creating an Activity" to create the combined audience. 



## Create a Combined Audience While Editing an Activity {#section_364A12CE96E04B61B7C18113AA586C2C}

You can create an ad hoc combined audience while editing an existing activity. 


1. From the [!UICONTROL  Activities] page, hover over the desired activity, then click the ** [!UICONTROL  Edit] ** icon (  ![](graphics/icon_edit.png). 

   Or 

   Click the desired activity to open it, then click ** [!UICONTROL  Edit Activity] **. 

1. Click the gear icon (  ![](graphics/icon_gear.png) ) > ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Multiple Audiences] **. 

1. Click the more options icon (  ![](../graphics/icon_more_options.png) ) next to the activity's current audience, then click ** [!UICONTROL  Change Audience] **. 

1. Proceed with [ Step 2 ](c_audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) under "Create a Combined Audience While Creating an Activity" to create the combined audience. 


