---
description: Information to help you update your Target implementation to include the at_property parameter.
keywords: properties;manage property;at_property;user groups;workspace;product configuration
seo-description: Information to help you update your Target implementation to include the at_property parameter.
seo-title: Update Implementation to Include the at_property Parameter
solution: Target
subtopic: Getting Started
title: Update Implementation to Include the at_property Parameter
topic: Premium
uuid: 72b241d8-89b7-45e1-88c3-833437a0c658
index: y
internal: n
snippet: y
translate: y
---

# Update Implementation to Include the at_property Parameter


>[!NOTE]
>
>This "Beta" offering is enabled for a few customers in this release for testing and feedback. This documentation is a work-in-progress and will be frequently updated until this feature is released for all Target users.


To use the `Target` user-permissions functionality, you must add the `at_property` parameter to any call that is hitting Target (mbox, api, etc.). 
**To obtain the `at_property` parameter code:** 

1. (Conditional) Use the implementation code you generated and saved to your clipboard while performing the steps in [Create Properties](create-properties.md#concept_D7FD12FFB2124FB1BEBECE573A2EBC6C) and proceed to Step 2. 
   Or
   In `Target`, click ** `Setup` ** > ** `Properties` ** to display the `Properties` list. 

    1. Hover your mouse pointer over the `Last Updated` column for the desired property to display and click the `Code` icon (  ![](graphics/icon_code.png)). 
       ![](graphics/code property.png) 

    1. Right-click the highlighted implementation code to copy it to your clipboard.
       ![](graphics/code property 2.png) 


1. Update your Target implementation with the implementation code obtained in the previous step.
   There are several ways to update your `Target` implementation. For example, the following methods can be used for web pages: 

    * **Via a "Global Parameter" in `Dynamic Tag Management` (Adobe Activation):** 
      ![](graphics/property token 2.png) 
      For more information, see [Global Parameters - Adobe Target](https://marketing.adobe.com/resources/help/en_US/dtm/target_global_params.html) in the *Dynamic Tag Management Product Documentation*. 

    * **Via the targetPageParams() function:**Place the following code in the &lt;body&gt; tags, above the at.js or mbox.js reference. 
      ![](graphics/property token 1.png) 
      For more information about how to do this with at.js, see [targetPageParams()](r_target-atjs-targetpageparams.md#reference_B235C9F6DA79449ABE3E23F914FEABAE). 

    * **Via the mboxCreate() function:** 
      ![](graphics/property token 3.png) 
      For more information about how to do this with at.js, see [targetPageParams()](r_target-atjs-targetpageparams.md#reference_B235C9F6DA79449ABE3E23F914FEABAE).[mboxCreate(mbox,params)](r_target-atjs-mboxcreate.md#reference_E68805FE86C64792B2066DB17B253D74) 




