---
description: Information to help you create workspaces (called Product Configurations) in the Adobe Admin Console for Enterprise.
keywords: properties;enterprise dashboard;admin console;manage property;workspace;product configuration
seo-description: Information to help you create workspaces (called Product Configurations) in the Adobe Admin Console for Enterprise.
seo-title: Create Workspaces
solution: Target
subtopic: Getting Started
title: Create Workspaces
topic: Premium
uuid: a3e073e2-efbb-4605-b3d6-5748484f2712
index: y
internal: n
snippet: y
translate: y
---

# Create Workspaces


>[!NOTE]
>
>This "Beta" offering is enabled for a few customers in this release for testing and feedback. This documentation is a work-in-progress and will be frequently updated until this feature is released for all Target users.


A workspace (Product Configuration) lets an organization assign a specific set of users to a specific set of properties. In many ways, a workspace is similar to a report suite in `Analytics`. 
**To create a workspace:** 

1. To access the `Admin Console for Enterprise`, go to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) &gt; sign in using your Adobe ID, if you have not already logged in. 
   Or
   If you are already logged in to the Marketing Cloud, go to [http://www.marketing.adobe.com](http://www.marketing.adobe.com/), then click the `App` icon (  ![](graphics/icon_mc_apps.png) ) in the top navigation bar > click ** `Administration` ** on the right side > then click ** `Launch Admin Console` **. 

1. (Conditional) If you have access to the `Admin Console for Enterprise` for more than one organization, click the user avatar in the right corner or the top navigation bar, then select the desired organization. 

1. Click ** `Products` **, then select the name of the desired product. 
   ![](graphics/workspace.png) 

   >[!NOTE]
   >
   >The Properties and Permissions functionality applies to `Target Standard/Premium` only. You cannot use this functionality with `Target Classic`. 


1. Create the desired workspace (Product Configuration):

    * **Default Access:**All existing activities will be merged into a single project called "Default Access." This will have no impact on customers. All user roles and functionality will remain exactly the same as they are prior to this change. 
      All activities created via `Adobe Experience Manager` (AEM), `Adobe Mobile Services`, and `Target Classic` will also be part of the "Default Access" workspace. You cannot currently move projects from "Default Access" to another project. 

    * **New workspaces (Product Configurations):**You can begin taking advantage of the new permissions functionality by doing the following: 
    
        * Creating new workspaces within the `Admin Console for Enterprise`. 

        * Assigning Target properties to the workspaces.



   You can use these workspaces to divide access to different teams by region, business unit, site section, or via any other method you choose. Users can be part of multiple workspaces and can have different roles within each workspace.

1. Follow the instructions in [Add Product Configurations](https://marketing.adobe.com/resources/help/en_US/mcloud/t_product-configurations.html) in the *Marketing Cloud and Core Services Product Documentation*. 


