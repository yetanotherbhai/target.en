---
description: Information to help you set up users and assign them roles using the Adobe Admin Console for Enterprise.
keywords: add user;manage user;user permissions
seo-description: Information to help you set up users and assign them roles using the Adobe Admin Console for Enterprise.
seo-title: User Management
solution: Target
subtopic: Getting Started
title: User Management
topic: Standard
uuid: 384d0f51-f508-49db-8384-58ffd0d066f3
index: y
internal: n
snippet: y
translate: y
---

# User Management


>[!NOTE]
>
>All user management must now be performed in the `Adobe Admin Console for Enterprise`. However, all of your existing users in `Target` will be migrated from `Target` to the `Admin Console for Enterprise`. 


If you see the `Properties` tab ( `Setup` > `Properties`) instead of the `Users` tab, your organization has a Target Premium subscription. The properties and permissions functionality in Target Premium provide you with greater flexibility and control. `Target` administrators can create separate workspaces in `Target` and then assign users different roles and permissions for individual pages, properties, or sites based on these workspaces. For more information, see [Properties](property_channel.md#concept_E396B16FA2024ADBA27BC056138F9838). 
Only system admin users can add users and manage their permissions. The system admin role is assigned at the `Explerience Cloud` level. `Experience Cloud` roles are separate from the roles managed in each solution. 

>[!NOTE]
>
>When you get started with `Adobe Target`, you will find IDs (ending in Adobe.com) pre-populated in your `Adobe Experience Cloud` account. These IDs are for members of Adobe teams so that they can assist you with your new account and with your use of `Adobe Target`, should you need help. To get assistance, reach out to your Adobe teams in the usual way. 


Only system administrators can set user roles. For example, a user with the Approver user cannot change an Observer to an Approver, without also having Experience Cloud Admin rights.
System admin users must add users to the system. Users are not automatically added. They are invited by email from the Experience Cloud and must confirm their email addresses before their accounts are registered.
You can also use the `Adobe Admin Console for Enterprise` to create groups within Target for each level of access: observer, editor, and approver. Then, when you add a new user to one of those groups, they receive the right access immediately. 
For more information about managing users in the Adobe Marketing Cloud, see [User and Group Administration in the Adobe Marketing Cloud Documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/#mc-user-group-admin). 

>[!NOTE]
>
>You will not see the new user listed on the `Users` page until the user logs in using his or her Adobe Experience Cloud account and then logs in to `Target Standard/Premium` by clicking the `Target` card. 


**To create a new user:** 

1. Go to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) &gt; sign in using your Adobe ID, if you have not already logged in. 
   Or
   If you are already logged in to the Marketing Cloud, go to [http://www.marketing.adobe.com](http://www.marketing.adobe.com/), then click the `App` icon (  ![](../target/graphics/icon_mc_apps.png) ) in the top navigation bar > click ** `Administration` ** on the right side > then click ** `Launch Admin Console` **. 

1. (Conditional) If you have access to the `Admin Console for Enterprise` for more than one organization, click the user avatar in the right corner or the top navigation bar, then select the desired organization. 

1. [In the Admin Console](properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE), click ** `User Management` ** > ** `Users` ** to create new users or to edit existing users. 

1. Follow the instructions in [Manage Users and Groups in the Marketing Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/user_mgmt_admin.html) in the *Marketing Cloud and Core Services Product Documentation*. 

1. To assign users the proper roles and permissions in Target, assign one of the following roles to each user:



<table id="table_4B17E288A7364A738FE0637AC53820C8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Role</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Observer</p> </td> 
   <td colname="col2"> <p>Can view activities, but cannot create or edit them.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Editor</p> </td> 
   <td colname="col2"> <p>Can create and edit activities before they are live, but cannot approve the launch of an activity.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Approver</p> </td> 
   <td colname="col2"> <p>Can create, edit, and activate or stop activities.</p> </td> 
  </tr> 
 </tbody> 
</table>

By default all `Target` users start with observer permissions. 
System admin users are identified in the Target Users list. Contact one of those system admin users if you need your access level changed.
