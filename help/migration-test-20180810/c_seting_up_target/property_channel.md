---
description: Information about creating properties and using the Properties and Permissions functionality that lets Target administrators create separate workspaces (product profiles) in Target and then assign users different roles and permissions for individual pages, properties, or web sites based on these workspaces.
keywords: add user;project;user group;properties;workspace;manage property;property;at_property;roles;permissions
seo-description: Information about creating properties and using the Properties and Permissions functionality that lets Target administrators create separate workspaces (product profiles) in Target and then assign users different roles and permissions for individual pages, properties, or web sites based on these workspaces.
seo-title: Enterprise User Permissions
solution: Target
subtopic: Getting Started
title: Enterprise User Permissions
title_outputclass: premium
topic: Premium
uuid: 0bb4903e-bdc2-4086-84a0-0bbd530d16de
badge: asstes/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Enterprise User Permissions



<table id="table_FD223AA7282243338769C27AC146FD51"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Properties and Permissions functionality is available as part of the <span class="keyword"> Target Premium </span> solution. They are not available in <span class="keyword"> Target Standard </span> without a <span class="keyword"> Target Premium </span> license. </p> <p>Your Target implementation can be using any version of at.js or mbox.js. </p> <p>You can tell whether your organization has a Standard or Premium license by clicking the <span class="wintitle"> Setup </span> link at the top of the Target UI. </p> <p> 
     <ul id="ul_3911B1BA89C54A9D91F5CD47ADC31C6E"> 
      <li id="li_439701DC0EA9408FA833314D7569D5FA"> <p><b>Target Standard Customers: </b>If you see the <span class="wintitle"> Users </span> tab ( <span class="wintitle"> Setup </span> &gt; <span class="wintitle"> Users </span>), your organization has a Target Standard license. Target Standard customers should follow the instructions in <a href="../ov/c_user_management.xml#concept_501166A5F8FB4964A3AAA15D6095C6BE" format="dita" scope="local"> Users </a> to add users and assign permissions in the Adobe Admin Console. </p> <p>Target Standard users see the following error message when clicking the Properties tab. There is nothing wrong with Target. Target Standard users do not have access to the Target Premium Enterprise Permissions functionality. </p> <p style="text-align: center;"> <img href="../graphics/sorry.png" id="image_4ED3EC4ECEB0465E9863DEF38BE459D7" /> </p> </li> 
      <li id="li_82A31FD812AA49F9A684B5860240DF26"> <p><b>Target Premium Customers: </b>If you see the <span class="wintitle"> Properties </span> tab ( <span class="wintitle"> Setup </span> &gt; Properties), your organization has a Target Premium license. Target Premium customers should follow the instructions in this topic and in <a href="property_channel.xml#concept_22F2855DBF0D4754B9460F5D68749C71" format="dita" scope="local"> Configure Enterprise Permissions </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


>[!IMPORTANT]
>
>Ensure that you read the[ Caveats ](property_channel.md#section_9714311B1CD9497A86F4910F8AE635E2) section below before proceeding with Enterprise Permissions. 



## Enterprise Permissions Training Video {#section_2FA080303A064242B63FF16CFA6DB31D}

This video explains the Enterprise Permissions: 



<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Enterprise Permissions </th> 
   <th colname="col3" class="entry"> 3:16 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://video.tv.adobe.com/v/19042/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://video.tv.adobe.com/v/19042/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p>Learning objectives: </p> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F"> <p>The three role levels that Adobe Target users can hold </p> </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F"> <p>The concepts of Properties and Workspaces, and how these boundaries and groupings work to allow for control over users' access levels </p> </li> 
      <li id="li_6C4D1871E45D40118D7D9D4DF81547B5"> <p>Different Property examples for your organization to consider </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Terms and Definitions Used in this Section {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

The following terms are used throughout this section and might be new to users wanting to use the Properties and Permissions functionality in Target Premium. 



<table id="table_3A0AF4EDED5C45A68CB3F03CDE9E3C47"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Term </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Property </p> </td> 
   <td colname="col2"> <p>Properties are similar in nature to those within <span class="keyword"> Dynamic Tag Management </span> ( <span class="keyword"> Activation </span>) in that they use a unique snippet of code to differentiate them. </p> <p>A web property is a library of rules and one embed code. A web property can be any grouping of one or more domains and subdomains. </p> <p>Properties are enabled by adding a specific name/value pair as a parameter with any call (mbox, api, etc.) to Target. </p> <p>Properties belong to specific channels (Web, Mobile, Email, or API/Other). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Workspace (Product Profile) </p> </td> 
   <td colname="col2"> <p>A workspace lets an organization assign a specific set of users to a specific set of properties. In many ways, a workspace is similar to a report suite in <span class="keyword"> Adobe Analytics </span>. </p> <p> <p>Note:  Workspaces are known as <span class="wintitle"> Product Profiles </span> in the <span class="keyword"> Adobe Admin Console for Enterprise </span>. </p> </p> <p>If you are part of a multi-national organization, you might have a workspace for your European web pages, properties, or sites and another workspace for your American web pages, properties, or sites. If you are part of a multi-brand organization, you might have a separate workspace for each of your brands. </p> <p>Users can be part of multiple workspaces and can even have different roles within each workspace. </p> <p>Users can have different views of Adobe Target by moving between workspaces, similar to how Analytics users have different views of Analytics by moving between Report Suites. </p> <p>Workspaces can include complete different audiences, code offers, and activities. </p> <p>All audiences and activities created before the new Enterprise Permissions model migration will be grouped together in the "Default Workspace," discussed below. </p> <p>All activities created via Adobe Experience Manager (AEM), Adobe Mobile Services, and Adobe Target Classic will be part of the "Default Workspace." </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Default Workspace </p> </td> 
   <td colname="col2"> <p>All existing workspaces (product profiles) within Admin Console are merged into a single workspace called "Default Workspace" during your organization's migration to the new Enterprise Permissions model. </p> <p> <p type="important">Note:  Do not delete the Default Workspace. </p> </p> <p>All user roles and access to all Target functionality remains exactly the same as they were prior to the migration to the new Enterprise Permissions model. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>User Groups </p> </td> 
   <td colname="col2"> <p>You can create user groups, such as Developers, Analysts, Marketers, Executives, etc., and then assign privileges across multiple Adobe products and workspaces. Assigning a new team member all the appropriate privileges across different Adobe products can be as easy as adding them to a specific user group. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Roles and Permissions </p> </td> 
   <td colname="col2"> <p>Roles and permissions determine the access levels that users have to create and manage activities in your <span class="keyword"> Target </span> implementation. In <span class="keyword"> Target </span>, roles include the following: </p> <p> 
     <ul id="ul_3F57367D49494CA9A05C3F8B16C45ED1"> 
      <li id="li_672C00988A354BC2B6A6376CFD9A5EA8"> <p><b>Observer: </b>Can view activities, but cannot create or edit them. </p> </li> 
      <li id="li_B65D3D9CC79A416AB1F9F0EACD3196DE"> <p><b>Editor: </b>Can create and edit activities before they are live, but cannot approve the launch of an activity. </p> </li> 
      <li id="li_6964D91D40F6489AA706AE623BAB9397"> <p><b>Approver: </b>Can create, edit, and activate or stop activities. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Channel </p> </td> 
   <td colname="col2"> <p>Channel refers to the content type of where your <span class="keyword"> Target </span> activities are delivered: webpages, mobile apps, email messages, and so forth. </p> <p>When you create a new activity, it is created in the currently selected workspace. You'll see channel selection options in the first dialog box that lets you choose the desired channel for the activity: Web, Mobile App, Email, or Other/API. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Permissions Overview {#section_DC2172520DA84605B218A5E9FB6D187A}

The following information explains the way permissions were enforced previously in [!DNL  Target] and how they are enforced using the [!UICONTROL  Properties] and [!UICONTROL  Permissions] functionality. 

The new [!UICONTROL  Permissions] functionality lets you create different projects (called "Product Profiles" in the [!DNL  Adobe Admin Console for Enterprise]) to allow you to assign different permissions for a single user that dictate that user's access rights for each project. These distinct projects can be compared to the way that report suites work in [!DNL  Adobe Analytics]. Each project can have specific users with specific roles that apply to a set of properties. The result is that customers will be able to restrict the view, edit, and approval access to their users based on region, environment (dev/stage/prod), channel, or other custom criteria, as shown below: 

![](graphics/permissions.png) 

For example, a specific user might have "approval" access on the Americas websites but only "view" access on the European mobile app. That same user might not have any access to even view the activities offered on web and mobile properties in the APAC region. 

The current [!DNL  Target] [!UICONTROL  Permissions] model has three permission roles (Observer, Editor, and Approver), as shown in the following illustration: 

![](graphics/permissions 1.png) 

Each role has different levels of permissions: 



<table id="table_4B17E288A7364A738FE0637AC53820C8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Role </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Observer </p> </td> 
   <td colname="col2"> <p>Has read-only access to activities. Can view activities, but cannot create or edit them. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Editor </p> </td> 
   <td colname="col2"> <p>Can create and edit activities before they are live, but cannot approve the launch of an activity. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Approver </p> </td> 
   <td colname="col2"> <p> Can create, edit, and activate or stop activities. </p> </td> 
  </tr> 
 </tbody> 
</table>

It is important to note that each user's role applies to every page, property, or site in your account that includes [!DNL  Target] tags, as shown below: 

![](graphics/permissions 2.png) 

The new [!DNL  Target] [!UICONTROL  Permissions] model has the same three permission roles (Observer, Editor, and Approver); however, you can assign a user's permissions roles separately for individual pages, properties, or sites, as shown below: 

![](graphics/permissions 3.png) 

In this example, Jan has Approver permissions to the US Homepage and the US Site and Observer permissions to the France Site. 

Furthermore, Jan won't be able to see pages, properties, or sites in [!DNL  Target] that she doesn't have permissions to see, as shown below: 

![](graphics/permissions 4.png) 

In this example, Jan cannot see the Product Pages, Russia Site, and the Careers Site. 

## Use Case Scenarios {#section_F3CE8576959E4F4CB13BEEED38311DD8}

The following use cases might be helpful to understand how properties, projects, roles, and permissions can help you achieve your marketing goals with [!DNL  Target]: 



<table id="table_93CA752C63844160A415C164882E8952"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type of Organization </th> 
   <th colname="col2" class="entry"> Example Project and Permissions Structure </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Multi-national organization </p> </td> 
   <td colname="col2"> <p>If you are part of a multi-national organization, you might have a workspace for your European web pages, properties, or sites and another workspace for your American web pages, properties, or sites. </p> <p>After a reorganization, using the personas in the illustrations above, you might set up workspaces and permissions similar to the following: </p> <p> 
     <ul id="ul_92A2A83608764DED95AF938EEF95B7C5"> 
      <li id="li_6F935ABAE5504633B3AACB67CE2E1FA2"> <p><b>Jan: </b>Jan is the Head of Optimization in the Center of Excellence for her organization's United States web pages, properties, and sites. She most likely has System Admin rights in the <span class="keyword"> Adobe Marketing Cloud </span>. </p> <p>In her role, she has Approver permissions for the US Homepage and the US Site. With Approver permissions, she can create, edit, and activate or stop activities. </p> <p>Jan also consults with the optimization team in France and, therefore, has Observer permissions for the France Site that give her read-only access to activities. Jan can view activities, but cannot create or edit them. </p> <p>Because Jan has no role that necessitates her seeing the Product Pages, Russia Site, or Careers Site, she cannot see activities for those sites. </p> </li> 
      <li id="li_843C4F69B6ED48169388A58080D0ECBA"> <p><b>Ernie:</b> Ernie is a Marketing Manager for the organization in charge of marketing in the United States. </p> <p>Because Ernie is fairly new to the organization and somewhat inexperienced with <span class="keyword"> Target </span>, he has Editor permissions for the US Homepage, US Site, and Product Pages. With Editor permissions, Ernie can create and edit activities before they are live, but he cannot approve the launch of an activity—someone with Approval permissions, such as Jan, must approve the activity before it can be put into production. </p> <p>Because Ernie has no role that necessitates him seeing the Russia Site, France Site, or Careers Site, he cannot see activities for those sites. </p> </li> 
      <li id="li_B37A4D41680F443F82A1A487CB83BD7D"> <p><b>Diana: </b>Diana is now an Analyst for the organization and has been granted Observer permissions for the US Homepage, US Site, Product Pages, Russia Site, and the France Site that give her read-only access to activities. Diana can view activities, but cannot create or edit them. </p> <p>Because Diana has no role that necessitates her seeing the Careers Site, she cannot see activities for those sites. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Multi-brand organization </p> </td> 
   <td colname="col2"> <p>If you are part of a multi-brand organization, you might have a separate workspace for each brand's web pages, properties, or sites. </p> <p>After a reorganization, using the personas in the illustrations above, you might set up projects and permissions similar to the following: </p> <p> 
     <ul id="ul_CAB7F8536FBA4CCC89382C4DDCEF6462"> 
      <li id="li_0C10E3344A764A98A485D42875D93874"> <p><b>Jan: </b>Jan is the Head of Optimization in the Center of Excellence for a heath-care organization that operates in the hospital-product and consumer-product spaces. She most likely has System Admin rights in the <span class="keyword"> Adobe Marketing Cloud </span>. </p> <p>In her role, she has Approver permissions for the Hospital Site. With Approver permissions, she can create, edit, and activate or stop activities. </p> <p>Jan also consults with the optimization team in the consumer-products space and, therefore, has Observer permissions for that site that give her read-only access to activities. Jan can view activities, but cannot create or edit them. </p> </li> 
      <li id="li_2245E59E82B74DBDA948434458B8D3CF"> <p><b>Ernie:</b> Ernie is a Marketing Manager for the organization in charge of marketing in the consumer-product space. </p> <p>Because Ernie is fairly new to the organization and somewhat inexperienced with <span class="keyword"> Target </span>, he has Editor permissions for the Consumer Site. With Editor permissions, Ernie can create and edit activities before they are live, but he cannot approve the launch of an activity—someone with Approval permissions for the Consumer Site, but not Jan in this scenario, must approve the activity before it can be put into production. </p> <p>Because Ernie has no role that necessitates him seeing the Hospital Site, he cannot see activities for that site. </p> </li> 
      <li id="li_5DF3DB9698C146EA9D8A560BEC8B0036"> <p><b>Diana: </b>Diana is now an Analyst for the organization and has been granted Observer permissions for the Hospital Site and the Consumer Site that give her read-only access to activities. Diana can view activities, but cannot create or edit them. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Target UI Property and Permissions Touchpoints {#section_3414371393BB42999A268628B5456EC9}

The new Permissions functionality can be seen in various places in the [!DNL  Target] UI. 


* **Workspace (Product Profile) drop-down list: **The Workspace drop-down list displays at the top of the [!UICONTROL  Activities] and [!UICONTROL  Audiences] pages. Select the desired workspace to filter the list to display only activities in the selected workspace. 

  ![](graphics/workspace drop-down.png) 

* **Activity Creation: **When you create a new activity, it is created in the currently selected workspace. You'll see channel selection options in the first dialog box that lets you choose the desired channel for the activity: Web, Mobile App, Email, or Other/API. 

  ![](graphics/channel options.png) 

* **Properties page (Setup &amp;gt; Properties): **You can use the [!UICONTROL  Search] box, the [!UICONTROL  Channel], and [!UICONTROL  Product Profile] options to filter the [!UICONTROL  Property] List. 

  ![](graphics/properties list.png) 



## Caveats {#section_9714311B1CD9497A86F4910F8AE635E2}

Consider the following when configuring properties and permissions in Target Premium: 


* 
  >[!IMPORTANT]
  >
  >Do not delete workspaces with activities. If this happens, work with client care to recover those activities.


* Any setting on the following the Setup pages can be controlled by any Approver in any workspace: 

    * Preferences 

    * Implementation 

    * Scene7 Settings 

    * Hosts 


* Users cannot move resources from one workspace (product profile) to another. Copy, however, is supported. 

* When viewing audiences from the [!DNL  Audiences] page, the page loads slower than expected. If you interact with the search bar in any way, audiences display faster. This is a known issue and will be fixed in an upcoming update. This issue does not affect selecting audiences during the activity-creation workflow. 

* The following resources are or are not part of the new Enterprise Permissions model: 



<table id="table_56155869DF7F4674A5B8BAF676E23EB2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Are Part of New Enterprise Permissions Model </th> 
   <th colname="col2" class="entry"> Are Not Part of New Enterprise Permissions Model </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>The following resources are part of the new Enterprise Permissions model: </p> 
    <ul id="ul_DADD4A6354C048438B905DBA91CAFE9E"> 
     <li id="li_D52CF7EBE74F43D0AE8ABF91CD265399"> <p>Activities, audiences, and code offers created within Target Standard/Premium after the customer is enabled for permissions. (Note: customers must be entitled to Target Premium.) </p> </li> 
     <li id="li_7E1ED21EBB1E4296879130EF56BD7ACB"> <p>Properties can be added to existing activities in the Default Workspace; however, this is subject to change. </p> </li> 
    </ul> </td> 
   <td colname="col2"> <p>The following resources are not part of the new Enterprise Permissions model: </p> 
    <ul id="ul_5EDEF20E83A24FF59004D5B0287779CA"> 
     <li id="li_7C7C341539DE46C1B322D2E47790F0B2"> <p>Image offers </p> </li> 
     <li id="li_2AE7D54CF6A34A2D8B3C2BEF8F531D3E"> <p>All Recommendations resources: </p> 
      <ul id="ul_C24501026C1E43819BEA589D9406048D"> 
       <li id="li_4E703E322B8440B0B68FE6403D48A99C"> <p>Criteria Library </p> </li> 
       <li id="li_F1FE90CE3A7B4ED0BE8A6DC49F22D480"> <p>Design Library </p> </li> 
       <li id="li_0FDF0E7D45F247B89F0D3AF1689950D7"> <p>Catalog </p> </li> 
       <li id="li_2469CB2A2B2440DC8DECCB381BE201B5"> <p>Recommendations Setup </p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Only new resources (such as activities, code offers, and audiences) created within Target Premium (after Enterprise Permissions are enabled) will be available to restrict by permissions. </p> </td> 
   <td colname="col2"> <p>Existing resources (such as activities, code offers, and audiences) created within Target Premium prior to enabling Enterprise Permissions can be copied but cannot be moved to other workspaces. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>External resources are available only to users in the Default Workspace. A user's role in the Default Workspace applies globally (to all Target requests and all Target resources). </p> </td> 
   <td colname="col2"> <p>Activities, audiences, code offers, image offers, or any other resource created using the following solutions or methods cannot be controlled by the Enterprise Permissions model, but will be part of the Default Workspace: </p> 
    <ul id="ul_1974180FE424479880FAF405809DB362"> 
     <li id="li_A3E8270F72684568833883CD833B17F7"> <p>Target Classic </p> </li> 
     <li id="li_DEFB3650EA494DF586B75F86577A9A74"> <p>Adobe Experience Manager (AEM) </p> </li> 
     <li id="li_AE56A1D00F5641B3B0470539F7A487B9"> <p>Adobe Mobile Services </p> </li> 
     <li id="li_F731A6DA33774846AD3FC5952EB76398"> <p>Resources created via API (including activities, audiences, code offers, and image offers). </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Image offers (assets stored under <span class="filepath"> https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library </span>) cannot be controlled by the Enterprise Permissions model at this time. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>clickTracking and redirects will only work when the destination link or destination page are part of a property that is included in the activity. Additionally, clickTracking may not work when using the t <span class="codeph"> argetPageParams() </span> function. The <span class="codeph"> targetPageParamsAll() </span> is the recommended function. </p> <p>Target currently requires an <span class="codeph"> at_property </span> token to be present on any page where tracking occurs. In the event that the token is (1) not present, (2) not detected at the time of activity setup (within the VEC), or (3) not passed to the clickTracking mbox via the <span class="codeph"> targetPageParamsAll() </span> function, the metric will not be incremented and will appear as "0." </p> <p>The same applies for activities using redirects. The destination page must have an <span class="codeph"> at_property </span> token and be recognized at the time of setup within the VEC. </p> <p>In a future release, Target will work on pages where no <span class="codeph"> at_property </span> token is present or pages where a different <span class="codeph"> at_property </span> token is present. </p> </td> 
  </tr> 
 </tbody> 
</table>


* The Enterprise User Permissions functionality is not supported in [ Adobe I/O API calls ](http://developers.adobetarget.com). 



## Frequently Asked Questions {#section_31D3450ADEAE4A29963A34F8E8C19FE0}

**Can I move an activity from one workspace to another?** 

Unfortunately, you cannot move activities from one workspace to another. However, you can copy an activity to any workspace knowing that reporting data will not carry over. 

Activities created before the migration continue to run the same way in the Default Workspace unless they are edited and assigned properties. Activities under a specific workspace will honor properties assigned to that workspace and, therefore, behavior might not remain same as before the migration. 

>[!NOTE]
>
>Properties and Permissions functionality is available as part of the [!DNL  Target Premium] solution. They are not available in [!DNL  Target Standard] without a [!DNL  Target Premium] license. 



The following table lists the tasks you should perform to create properties and assign user roles and permissions: 



<table id="table_D3FFB40000DC4CBAA18B1D0E52D40565"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Task </th> 
   <th colname="col2" class="entry"> Performed In </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="property_channel.xml#concept_22F2855DBF0D4754B9460F5D68749C71/section_A92AF0F921B743FEB9E9033433BD816A" format="dita" scope="local"> 1. Add Users (Optional) </a> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Admin Console for Enterprise </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="property_channel.xml#concept_22F2855DBF0D4754B9460F5D68749C71/section_B82EB409B67C4D9D9D20CE30E48DB1DC" format="dita" scope="local"> 2. Create a Workspace (Product Profile) </a> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Admin Console for Enterprise </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="property_channel.xml#concept_22F2855DBF0D4754B9460F5D68749C71/section_5F5CB9AA7A9F4D26953E22016DA59605" format="dita" scope="local"> 3. Create User Groups (Optional) </a> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Admin Console for Enterprise </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="property_channel.xml#concept_22F2855DBF0D4754B9460F5D68749C71/section_E8F2C92BE0F4466AB87604059C9CF3FD" format="dita" scope="local"> 4. Create Properties </a> </p> </td> 
   <td colname="col2"> <p>Target UI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="property_channel.xml#concept_22F2855DBF0D4754B9460F5D68749C71/section_9B17A59807A94712BE642942442EBBC8" format="dita" scope="local"> 5: Update Your Implementation to Include the at_property Parameter </a> </p> </td> 
   <td colname="col2"> <p>Target UI / <span class="codeph"> at.js </span> functions / Dynamic Tag Management </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="property_channel.xml#concept_22F2855DBF0D4754B9460F5D68749C71/section_8C425E43E5DD4111BBFC734A2B7ABC80" format="dita" scope="local"> 6: Specify Roles and Permissions </a> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Admin Console for Enterprise </span> </p> </td> 
  </tr> 
 </tbody> 
</table>


<a id="section_79796E0227D048F59BAE0AB02E544EBE"></a>

For those tasks performed in the Adobe Admin Console for Enterprise, access the console by following these steps: 


1. Go to [ https://adminconsole.adobe.com/enterprise/ ](https://adminconsole.adobe.com/enterprise/) &gt; sign in using your Adobe ID, if you have not already logged in. 

   Or 

   If you are already logged in to the Marketing Cloud, go to [ http://www.marketing.adobe.com ](http://www.marketing.adobe.com/), then click the [!UICONTROL  App] icon (  ![](graphics/icon_mc_apps.png) ) in the top navigation bar > click ** [!UICONTROL  Administration] ** on the right side > then click ** [!UICONTROL  Launch Admin Console] **. 

1. (Conditional) If you have access to the [!DNL  Admin Console for Enterprise] for more than one organization, click the user avatar in the right corner or the top navigation bar, then select the desired organization. 



## 1. Add Users (Optional) {#section_A92AF0F921B743FEB9E9033433BD816A}

When you start using the new [!UICONTROL  Properties] functionality, all user management must be performed in the [!DNL  Adobe Admin Console for Enterprise]. However, all of your existing users in [!DNL  Target] will be migrated from [!DNL  Target] to the [!DNL  Admin Console for Enterprise]. 


1. [ In the Admin Console ](property_channel.md#section_79796E0227D048F59BAE0AB02E544EBE), click ** [!UICONTROL  User Management] ** > ** [!UICONTROL  Users] ** to create new users or to edit existing users. 

1. Follow the instructions in [ Manage Users and Groups in the Marketing Cloud ](https://helpx.adobe.com/enterprise/help/users.html) in the *Enterprise User Guide*. 



## 2. Create a Workspace (Product Profile) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

A workspace (Product Profile) lets an organization assign a specific set of users to a specific set of properties. In many ways, a workspace is similar to a report suite in [!DNL  Analytics]. 

Organizations can begin taking advantage of Enterprise permissions functionality by creating new workspaces within Admin Console, assigning Target properties to these workspaces, and moving users from the "Default Workspace" configuration to these newer, limited-access workspaces. 

Customers can use these workspaces to separate access to different teams by region, by business unit, by sight section, or via any other method they choose. 

Users can be part of multiple workspaces and can even have different roles within each workspace. 

This video explains how to create workspaces: 



<table id="table_38936C8A1EAC4164B9BD5A646A71D181"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> How to Configure Target Workspaces </th> 
   <th colname="col3" class="entry"> 6:55 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://video.tv.adobe.com/v/19463/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://video.tv.adobe.com/v/19463/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_AE48A4920BD643A0AB3CEBFCF28A5D7C"> 
      <li id="li_5440ACDE887442F495FCC50DF72974C8"> <p>Access the Adobe Admin Console from the Adobe Target interface (3 ways) </p> </li> 
      <li id="li_31F8EBF4B5A44CFB9BB15723C078ABA9"> <p>Configure a workspace in Adobe Admin Console </p> 
       <ul id="ul_A50E942C80954C6AB57801F2CE953469"> 
        <li id="li_5C713316FB5447C1A209AA2689F4B644"> <p>Add users to workspaces </p> </li> 
        <li id="li_DD52CDD690EB4EB4A7D11BAEA6179D6F"> <p>Add properties to workspaces </p> </li> 
       </ul> </li> 
      <li id="li_80054E078EE84DD0A75119F28BA8351C"> <p>Understand default workspaces </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


1. [ In the Admin Console ](property_channel.md#section_79796E0227D048F59BAE0AB02E544EBE), click ** [!UICONTROL  Products] **, then select the name of the desired product. 

   ![](graphics/workspace.png) 

1. Create the desired workspace (Product Profile): 


    * **Default Access: **All existing activities will be merged into a single project called "Default Access." This will have no impact on customers. All user roles and functionality will remain exactly the same as they are prior to this change. 

      All activities created via [!DNL  Adobe Experience Manager] (AEM), [!DNL  Adobe Mobile Services], and [!DNL  Target Classic] will also be part of the "Default Access" workspace. You cannot currently move projects from "Default Access" to another project. 

    * **New workspaces (Product Profiles): **You can begin taking advantage of the new permissions functionality by doing the following: 
    
        * Creating new workspaces within the [!DNL  Admin Console for Enterprise]. 

        * Assigning Target properties to the workspaces. 




   You can use these workspaces to divide access to different teams by region, business unit, site section, or via any other method you choose. Users can be part of multiple workspaces and can have different roles within each workspace. 

1. Follow the instructions in [ Create and Manage Product Configurations ](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) in the *Enterprise User Guide*. 



## 3. Create User Groups (Optional) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

You can create user groups, such as Developers, Analysts, Marketers, Executives, etc., and then assign privileges across multiple Adobe products and workspaces. Assigning a new team member all the appropriate privileges across different Adobe products can be as easy as adding them to a specific user group. 


1. [ In the Admin Console ](property_channel.md#section_79796E0227D048F59BAE0AB02E544EBE), click ** [!UICONTROL  User Management] ** > ** [!UICONTROL  User Groups] ** to create new user groups or to edit existing groups. 

1. Follow the instructions in [ Manage Users and Groups of a Product Configuration ](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) in the *Enterprise User Guide*.


## 4. Create Properties {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

This video explains how to create properties: 



<table id="table_201FE2DAE4724C089B0AD2588AED1DC4"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> How to Create Properties </th> 
   <th colname="col3" class="entry"> 3:05 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://video.tv.adobe.com/v/18990/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://video.tv.adobe.com/v/18990/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_08141C3B8BC74D24940211C2C903A2A8"> 
      <li id="li_A06E00FF338749C8BA5239DA2B4F0420"> <p>How to create a property within the <span class="keyword"> Adobe Target </span> interface </p> </li> 
      <li id="li_27E5710B24254F75BB48A0CAE7A2F64F"> <p>How to generate a property token to include in your property implementation </p> </li> 
      <li id="li_15ABAB48A8A84D1EBB064F8457C840CB"> <p>Familiarize yourself with the three implementation methods: </p> <p> 
        <ul id="ul_ACF4CEAD7B3948488C70606FF473BE77"> 
         <li id="li_1EE1205D3F5A49F8801886E4668ACEA8"> <p>Web </p> </li> 
         <li id="li_F3D894969C33480C8A3CD88FA955F129"> <p>Mobile app </p> </li> 
         <li id="li_9801FEA2BF79453C99AEDEBD95549C36"> <p>Email, set top box, or API calls </p> </li> 
        </ul> </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Properties are enabled by adding a specific name/value pair as a parameter with any call (mbox, api, etc.) to Target. 

Properties belong to specific channels (Web, Mobile, Email, and API/Other). 


1. In [!DNL  Target], click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Properties] ** to display the [!UICONTROL  Properties] list. 

1. Click **Create Property**. 

   ![](graphics/new property.png) 

   Fill in the fields: 


    * **Channel: **Specify the desired channel for the property: Web, Mobile App, Email, or Other/API (for example a set-top box or PlayStation console). 

    * **Name (Required): **Specify a descriptive name for the property. 

    * **Description: **Specify an optional description for the property. 



1. Click ** [!UICONTROL  Generate Code] ** to generate the code you'll use while performing the steps in [ 5: Update Your Implementation to Include the at_property Parameter ](property_channel.md#section_9B17A59807A94712BE642942442EBBC8). 

1. Copy the code to your clipboard. 

1. Click ** [!UICONTROL  Save] ** when done. 



## 5: Update Your Implementation to Include the at_property Parameter {#section_9B17A59807A94712BE642942442EBBC8}

To use the [!DNL  Target] user-permissions functionality, you must add the ` at_property` parameter to any call that is hitting Target (mbox, api, etc.). 

**To obtain the ` at_property` parameter code:** 


1. (Conditional) Use the implementation code you generated and saved to your clipboard while performing the steps in [ 4. Create Properties ](property_channel.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) and proceed to Step 2. 

   Or 

   In [!DNL  Target], click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Properties] ** to display the [!UICONTROL  Properties] list. 

    1. Hover your mouse pointer over the [!UICONTROL  Last Updated] column for the desired property to display and click the [!UICONTROL  Code] icon (  ![](graphics/icon_code.png)). 

       ![](graphics/code property.png) 

    1. Right-click the highlighted implementation code to copy it to your clipboard. 

       ![](graphics/code property 2.png) 


1. Update your Target implementation with the implementation code obtained in the previous step. 

   There are several ways to update your [!DNL  Target] implementation. For example, the following methods can be used for web pages: 


    * **Via a "Global Parameter" in [!DNL  Dynamic Tag Management] (Adobe Activation):** 

      ![](graphics/property token 2.png) 

      For more information, see [ Global Parameters - Adobe Target ](https://marketing.adobe.com/resources/help/en_US/dtm/target_global_params.html) in the *Dynamic Tag Management Product Documentation*. 

    * **Via the targetPageParams() function: **Place the following code in the &lt;body&gt; tags, above the at.js or mbox.js reference. 

      ![](graphics/property token 1.png) 

      For more information about how to do this with at.js, see [ targetPageParams() ](c_target-ats-functions.md#reference_B235C9F6DA79449ABE3E23F914FEABAE). 

    * **Via the mboxCreate() function:** 

      ![](graphics/property token 3.png) 

      For more information about how to do this with at.js, see [ targetPageParams() ](c_target-ats-functions.md#reference_B235C9F6DA79449ABE3E23F914FEABAE). [ mboxCreate(mbox,params) ](c_target-ats-functions.md#reference_E68805FE86C64792B2066DB17B253D74) 





## 6: Specify Roles and Permissions {#section_8C425E43E5DD4111BBFC734A2B7ABC80}


1. [ In the Admin Console ](property_channel.md#section_79796E0227D048F59BAE0AB02E544EBE), click ** [!UICONTROL  Products] **, then select the name of the desired product. 

   ![](graphics/workspace.png) 


   >[!NOTE]
   >
   >The Properties and Permissions functionality applies to [!DNL  Target Standard/Premium] only. You cannot use this functionality with [!DNL  Target Classic]. 


1. Click the name of the desired profile. 

1. Click ** [!UICONTROL  Configuration Users] **. 

   The [!UICONTROL  Configuration Users] tab displays all of the users in that workspace. 

   ![](graphics/configuration users.png) 

1. Select the desired permissions role (Approver, Editor, or Observer) by using the drop-down list for each user in the [!UICONTROL  Product Role] column. 



<table id="table_92B2935FEB0A4DFEAC24C074EDEBD409"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Role </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Observer </p> </td> 
   <td colname="col2"> <p>Can view activities, but cannot create or edit them. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Editor </p> </td> 
   <td colname="col2"> <p>Can create and edit activities before they are live, but cannot approve the launch of an activity. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Approver </p> </td> 
   <td colname="col2"> <p> Can create, edit, and activate or stop activities. </p> </td> 
  </tr> 
 </tbody> 
</table>

   For more information, see [ Manage Product Permissions and Roles in the Admin Console ](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in the *Enterprise User Guide*. 

