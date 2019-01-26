---
description: Information about creating properties and using the Properties and Permissions functionality that lets Target administrators create separate workspaces (product profiles) in Target and then assign users different roles and permissions for individual pages, properties, or web sites based on these workspaces.
keywords: workspaces;manage property;permissions;product configuration;product profile;roles;project
seo-description: Information about creating properties and using the Properties and Permissions functionality that lets Target administrators create separate workspaces (product profiles) in Target and then assign users different roles and permissions for individual pages, properties, or web sites based on these workspaces.
seo-title: Enterprise user permissions
solution: Target
subtopic: Getting Started
title: Enterprise user permissions
title-outputclass: premium
topic: Premium
uuid: 1961730d-2357-406f-acac-a36b7a63bd35
badge: premium
---

# ![PREMIUM](/help/assets/premium.png) Enterprise user permissions{#enterprise-user-permissions}

Information about creating properties and using the Properties and Permissions functionality that lets Target administrators create separate workspaces (product profiles) in Target and then assign users different roles and permissions for individual pages, properties, or web sites based on these workspaces.

## Determine Whether You Have Access to Enterprise User Permissions

>[!NOTE]
>
>Properties and Permissions functionality is available as part of the Target Premium solution. They are not available in Target Standard without a Target Premium license.
>
>Your Target implementation can be using any version of at.js or mbox.js.

You can tell whether your organization has a Standard or Premium license by clicking the [!UICONTROL Setup] link at the top of the [!DNL Target] UI.

* **[!DNL Target Standard] Customers**: If you see the [!UICONTROL Users] tab ([!UICONTROL Setup > Users]), your organization has a [!DNL Target Standard] license. [!DNL Target Standard]customers should follow the instructions in [Users](/help/administrating-target/c-user-management/c-user-management/user-management.md) to add users and assign permissions in the Adobe Admin Console.

  [!DNL Target Standard] users see the following error message when clicking the [!UICONTROL Properties] tab. There is nothing wrong with [!DNL Target]. [!DNL Target Standard] users do not have access to the [!DNL Target Premium] [!UICONTROL Enterprise Permissions] functionality.

  ![Error message](/help/administrating-target/c-user-management/property-channel/assets/sorry.png)

* **[!DNL Target Premium] Customers**: If you see the [!UICONTROL Properties] tab ([!UICONTROL Setup > Properties]), your organization has a [!DNL Target Premium] license. [!DNL Target Premium] customers should follow the instructions in this article and in [Configure enterprise permissions](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

## Before You Get Started with Enterprise Permissions

>[!IMPORTANT]
>
>Ensure that you read the [Caveats](../../../administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) section below before proceeding with Enterprise Permissions.

## Terms and Definitions Used in this Section {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

The following terms are used throughout this section and might be new to users wanting to use the Properties and Permissions functionality in Target Premium.

| Term | Definition |
|--- |--- |
|Property|Properties are similar in nature to those within [!DNL Dynamic Tag Management] (Activation) in that they use a unique snippet of code to differentiate them.<br>A web property is a library of rules and one embed code. A web property can be any grouping of one or more domains and subdomains.<br>Properties are enabled by adding a specific name/value pair as a parameter with any call (mbox, api, etc.) to Target.<br>Properties belong to specific channels (Web, Mobile, Email, or API/Other).|
|Workspace (Product Profile)|A workspace lets an organization assign a specific set of users to a specific set of properties. In many ways, a workspace is similar to a report suite in [!DNL Adobe Analytics].<br>**Note**: Workspaces are known as [!UICONTROL Product Profiles] in the [!DNL Adobe Admin Console for Enterprise].<br>If you are part of a multi-national organization, you might have a workspace for your European web pages, properties, or sites and another workspace for your American web pages, properties, or sites. If you are part of a multi-brand organization, you might have a separate workspace for each of your brands.<br>Users can be part of multiple workspaces and can even have different roles within each workspace.<br>Users can have different views of Adobe Target by moving between workspaces, similar to how Analytics users have different views of Analytics by moving between Report Suites.<br>Workspaces can include complete different audiences, code offers, and activities.<br>All audiences and activities created before the new Enterprise Permissions model migration will be grouped together in the "Default Workspace," discussed below.<br>All activities created via Adobe Experience Manager (AEM), Adobe Mobile Services, and Adobe Target Classic will be part of the "Default Workspace."|
|Default Workspace|All existing workspaces (product profiles) within Admin Console are merged into a single workspace called "Default Workspace" during your organization's migration to the new Enterprise Permissions model.<br>**Important**: Do not delete the Default Workspace.<br>All user roles and access to all Target functionality remains exactly the same as they were prior to the migration to the new Enterprise Permissions model.|
|User Groups|You can create user groups, such as Developers, Analysts, Marketers, Executives, etc., and then assign privileges across multiple Adobe products and workspaces. Assigning a new team member all the appropriate privileges across different Adobe products can be as easy as adding them to a specific user group.|
|Roles and Permissions|Roles and permissions determine the access levels that users have to create and manage activities in your Target implementation. In Target, roles include the following:<ul></li>Observer: Can view activities, but cannot create or edit them.</li><li>Editor: Can create and edit activities before they are live, but cannot approve the launch of an activity.</li><li>Approver: Can create, edit, and activate or stop activities.</li></ul>|
|Channel|Channel refers to the content type of where your  Target  activities are delivered: webpages, mobile apps, email messages, and so forth.<br>When you create a new activity, it is created in the currently selected workspace. You'll see channel selection options in the first dialog box that lets you choose the desired channel for the activity: Web, Mobile App, Email, or Other/API.|

## Permissions Overview {#section_DC2172520DA84605B218A5E9FB6D187A}

The following information explains the way permissions were enforced previously in [!DNL Target] and how they are enforced using the [!UICONTROL Properties] and [!UICONTROL Permissions] functionality.

The new [!UICONTROL Permissions] functionality lets you create different projects (called "Product Profiles" in the [!DNL Adobe Admin Console for Enterprise]) to allow you to assign different permissions for a single user that dictate that user's access rights for each project. These distinct projects can be compared to the way that report suites work in [!DNL Adobe Analytics]. Each project can have specific users with specific roles that apply to a set of properties. The result is that customers will be able to restrict the view, edit, and approval access to their users based on region, environment (dev/stage/prod), channel, or other custom criteria, as shown below:

![](assets/permissions.png)

For example, a specific user might have "approval" access on the Americas websites but only "view" access on the European mobile app. That same user might not have any access to even view the activities offered on web and mobile properties in the APAC region.

The current [!DNL Target] [!UICONTROL Permissions] model has three permission roles (Observer, Editor, and Approver), as shown in the following illustration:

![](assets/permissions_1.png)

Each role has different levels of permissions:

| Role | Description |
|--- |--- |
|Observer|Has read-only access to activities. Can view activities, but cannot create or edit them.|
|Editor|Can create and edit activities before they are live, but cannot approve the launch of an activity.|
|Approver|Can create, edit, and activate or stop activities.|

It is important to note that each user's role applies to every page, property, or site in your account that includes [!DNL Target] tags, as shown below:

![](assets/permissions_2.png)

The new [!DNL Target] [!UICONTROL Permissions] model has the same three permission roles (Observer, Editor, and Approver); however, you can assign a user's permissions roles separately for individual pages, properties, or sites, as shown below:

![](assets/permissions_3.png)

In this example, Jan has Approver permissions to the US Homepage and the US Site and Observer permissions to the France Site.

Furthermore, Jan won't be able to see pages, properties, or sites in [!DNL Target] that she doesn't have permissions to see, as shown below:

![](assets/permissions_4.png)

In this example, Jan cannot see the Product Pages, Russia Site, and the Careers Site.

## Use Case Scenarios {#section_F3CE8576959E4F4CB13BEEED38311DD8}

The following use cases might be helpful to understand how properties, projects, roles, and permissions can help you achieve your marketing goals with [!DNL Target]:

| Type of Organization | Example Project and Permissions Structure |
|--- |--- |
|Multi-national organization|If you are part of a multi-national organization, you might have a workspace for your European web pages, properties, or sites and another workspace for your American web pages, properties, or sites.  After a reorganization, using the personas in the illustrations above, you might set up workspaces and permissions similar to the following:<br>**Jan**: Jan is the Head of Optimization in the Center of Excellence for her organization's United States web pages, properties, and sites. She most likely has System Admin rights in the [!DNL Adobe Experience Cloud].<br>In her role, she has [!UICONTROL Approver] permissions for the US Homepage and the US Site. With Approver permissions, she can create, edit, and activate or stop activities.<br>Jan also consults with the optimization team in France and, therefore, has [!UICONTROL Observer] permissions for the France Site that give her read-only access to activities. Jan can view activities, but cannot create or edit them.<br>Because Jan has no role that necessitates her seeing the Product Pages, Russia Site, or Careers Site, she cannot see activities for those sites.<br>**Ernie**: Ernie is a Marketing Manager for the organization in charge of marketing in the United States.<br>Because Ernie is fairly new to the organization and somewhat inexperienced with [!DNL Target], he has [!UICONTROL Editor] permissions for the US Homepage, US Site, and Product Pages. With [!UICONTROL Editor] permissions, Ernie can create and edit activities before they are live, but he cannot approve the launch of an activity—someone with [!UICONTROL Approval] permissions, such as Jan, must approve the activity before it can be put into production.<br>Because Ernie has no role that necessitates him seeing the Russia Site, France Site, or Careers Site, he cannot see activities for those sites.<br>**Diana**: Diana is now an Analyst for the organization and has been granted [!UICONTROL Observer] permissions for the US Homepage, US Site, Product Pages, Russia Site, and the France Site that give her read-only access to activities. Diana can view activities, but cannot create or edit them.<br>Because Diana has no role that necessitates her seeing the Careers Site, she cannot see activities for those sites.</li></ul>|
|Multi-brand organization|If you are part of a multi-brand organization, you might have a separate workspace for each brand's web pages, properties, or sites.  After a reorganization, using the personas in the illustrations above, you might set up projects and permissions similar to the following:<br>**Jan**: Jan is the Head of Optimization in the Center of Excellence for a heath-care organization that operates in the hospital-product and consumer-product spaces. She most likely has System Admin rights in the [!DNL Adobe Experience Cloud].<br>In her role, she has [!UICONTROL Approver] permissions for the Hospital Site. With [!UICONTROL Approver] permissions, she can create, edit, and activate or stop activities.<br>Jan also consults with the optimization team in the consumer-products space and, therefore, has [!UICONTROL Observer] permissions for that site that give her read-only access to activities. Jan can view activities, but cannot create or edit them.<br>**Ernie**: Ernie is a Marketing Manager for the organization in charge of marketing in the consumer-product space.<br>Because Ernie is fairly new to the organization and somewhat inexperienced with [!DNL Target], he has [!UICONTROL Editor] permissions for the Consumer Site. With [!UICONTROL Editor] permissions, Ernie can create and edit activities before they are live, but he cannot approve the launch of an activity—someone with [!UICONTROL Approval] permissions for the Consumer Site, but not Jan in this scenario, must approve the activity before it can be put into production.<br>Because Ernie has no role that necessitates him seeing the Hospital Site, he cannot see activities for that site.<br>**Diana**: Diana is now an Analyst for the organization and has been granted [!UICONTROL Observer] permissions for the Hospital Site and the Consumer Site that give her read-only access to activities. Diana can view activities, but cannot create or edit them.</li></ul>|

## Target UI Property and Permissions Touchpoints {#section_3414371393BB42999A268628B5456EC9}

The new Permissions functionality can be seen in various places in the [!DNL Target] UI.

* **Workspace (Product Profile) drop-down list:** The Workspace drop-down list displays at the top of the [!UICONTROL Activities], [!UICONTROL Audiences], and [!UICONTROL Offers] pages. Select the desired workspace to filter the list to display only items in the selected workspace.

  ![](assets/workspace_drop-down.png)

* **Activity Creation:** When you create a new activity, it is created in the currently selected workspace. You'll see channel selection options in the first dialog box that lets you choose the desired channel for the activity: Web, Mobile App, Email, or Other/API.

  ![](assets/channel_options.png)

* **Audience Creation:** When you create a new audience, it is created in the currently selected workspace. 
* **Offer Creation:** When you create a new offer, it is created in the currently selected workspace. 
* **Properties page (Setup > Properties):** You can use the [!UICONTROL Search] box, the [!UICONTROL Channel], and [!UICONTROL Product Profile] options to filter the [!UICONTROL Property] List.

  ![](assets/properties_list.png)

## Caveats {#section_9714311B1CD9497A86F4910F8AE635E2}

Consider the following when using or configuring properties and permissions in Target Premium:

* **Important**: Do not delete workspaces with activities. If this happens, work with client care to recover those activities.
* When using the All My Workspaces view:

    * You can see activities, audiences, and offers for all workspaces that you have the proper roles and permissions to access. 
    * When you select the All My Workspaces view, a new column is added to the Activities, Audiences, and Offers page that lists the item's workspace and your user permission associated with that item (Observer, Editor, or Approver), 
    * When creating an activity, audience, or offer in the All My Workspaces view, you must select the workspace where the item is to be created. Only those workspaces can be selected for which you have the Editor or Approver permission. 
    * When copying an activity, audience, or offer in the All My Workspaces view, you must select the workspace where the item is to be copied. Only those workspaces can be selected for which you have the Editor or Approver permission.

* Any setting on the following the Setup pages can be controlled by any Approver in any workspace:

    * Preferences 
    * Implementation 
    * Scene7 Settings 
    * Hosts

* Users cannot move resources from one workspace (product profile) to another. Copy, however, is supported. 
* When viewing audiences from the [!DNL Audiences] page, the page loads slower than expected. If you interact with the search bar in any way, audiences display faster. This is a known issue and will be fixed in an upcoming update. This issue does not affect selecting audiences during the activity-creation workflow. 
* The following resources are or are not part of the new Enterprise Permissions model:

  | Are Part of New Enterprise Permissions Model | Are Not Part of New Enterprise Permissions Model |
  |--- |--- |
  |The following resources are part of the new Enterprise Permissions model:<ul><li>Activities, audiences, and code offers created within Target Standard/Premium after the customer is enabled for permissions. (Note: customers must be entitled to Target Premium.)</li><li>Properties can be added to existing activities in the Default Workspace; however, this is subject to change.</li></ul>|The following resources are not part of the new Enterprise Permissions model:<ul><li>Image offers</li><li>All Recommendations resources: Criteria Library, Design Library, Catalog,and Recommendations Setup</li></ul>|
  |Only new resources (such as activities, code offers, and audiences) created within [!DNL Target Premium] (after [!UICONTROL Enterprise Permissions] are enabled) will be available to restrict by permissions.|Existing resources (such as activities, code offers, and audiences) created within [!DNL Target Premium] prior to enabling [!UICONTROL Enterprise Permissions] can be copied but cannot be moved to other workspaces.|
  |External resources are available only to users in the Default Workspace. A user's role in the Default Workspace applies globally (to all Target requests and all Target resources).|Activities, audiences, code offers, image offers, or any other resource created using the following solutions or methods cannot be controlled by the [!UICONTROL Enterprise Permissions] model, but will be part of the Default Workspace:<ul><li>Target Classic</li><li>Adobe Experience Manager (AEM)</li><li>Adobe Mobile Services</li><li>Resources created via API (including activities, audiences, code offers, and image offers)</li></ul>|
  ||Image offers (assets stored under `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library`) cannot be controlled by the [!UICONTROL Enterprise Permissions] model at this time.|
  ||clickTracking and redirects will only work when the destination link or destination page are part of a property that is included in the activity. Additionally, clickTracking may not work when using the `targetPageParams()` function. The `targetPageParamsAll()` is the recommended function.<br>[!DNL Target] currently requires an `at_property` token to be present on any page where tracking occurs. In the event that the token is (1) not present, (2) not detected at the time of activity setup (within the VEC), or (3) not passed to the clickTracking mbox via the `targetPageParamsAll()` function, the metric will not be incremented and will appear as "0."<br>The same applies for activities using redirects. The destination page must have an `at_property` token and be recognized at the time of setup within the VEC.<br> In a future release, [!DNL Target] will work on pages where no `at_property` token is present or pages where a different `at_property` token is present.|

* The Enterprise User Permissions functionality is not supported in [Adobe I/O API calls](https://developers.adobetarget.com).

## Frequently Asked Questions {#section_31D3450ADEAE4A29963A34F8E8C19FE0}

**Can I move an activity from one workspace to another?**

Unfortunately, you cannot move activities from one workspace to another. However, you can copy an activity to any workspace knowing that reporting data will not carry over. For more information, see "Copying/Editing an Activity When Using Workspaces" in [Copying/Editing an Activity When Using Workspaces](../../../c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Activities created before the migration continue to run the same way in the Default Workspace unless they are edited and assigned properties. Activities under a specific workspace will honor properties assigned to that workspace and, therefore, behavior might not remain same as before the migration. 

## Training video: Enterprise Permissions Training Video {#section_2FA080303A064242B63FF16CFA6DB31D}

Learning objectives:

* The three role levels that Adobe Target users can hold 
* The concepts of Properties and Workspaces, and how these boundaries and groupings work to allow for control over users' access levels 
* Different Property examples for your organization to consider

>[!VIDEO](https://video.tv.adobe.com/v/19042/)