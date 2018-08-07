---
description: Information to help you create properties in the Target UI.
keywords: properties;manage property;user groups;workspace;product configuration
seo-description: Information to help you create properties in the Target UI.
seo-title: Create Properties
solution: Target
subtopic: Getting Started
title: Create Properties
topic: Premium
uuid: bf8eea58-1686-48aa-b63f-837164abfe4f
index: y
internal: n
snippet: y
translate: y
---

# Create Properties


>[!NOTE]
>
>This "Beta" offering is enabled for a few customers in this release for testing and feedback. This documentation is a work-in-progress and will be frequently updated until this feature is released for all Target users.


Properties can now be defined within the Target UI. Properties are similar in nature to those within `Dynamic Tag Management` ( `Activation`) in that they use a unique snippet of code to differentiate them. 
Properties are enabled by adding a specific name/value pair as a parameter with any call (mbox, api, etc.) to Target.
Properties belong to specific channels (Web, Mobile, Email, and API/Other).
**To create a property:** 

1. In `Target`, click ** `Setup` ** > ** `Properties` ** to display the `Properties` list. 

1. Click **Create Property**. 
   ![](graphics/new property.png) 
   Fill in the fields:

    * **Channel:**Specify the desired channel for the property: Web, Mobile App, Email, or Other/API (for example a set-top box or PlayStation console). 

    * **Name (Required):**Specify a descriptive name for the property. 

    * **Description:**Specify an optional description for the property. 



1. Click ** `Generate Code` ** to generate the code you'll use while performing the steps in [Update Implementation to Include at_property Parameter](update-implementation-a-property-parameter.md#concept_7FAEFDE86AFA43699CCFD913E5821CD7). 

1. Copy the code to your clipboard.

1. Click ** `Save` ** when done. 


