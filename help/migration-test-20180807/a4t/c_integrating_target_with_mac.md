---
description: Integrating Adobe Target with Adobe Analytics and other Marketing Cloud solutions enables the use of the same data, audiences, and metrics in both solutions.
keywords: Overview and Reference
seo-description: Integrating Adobe Target with Adobe Analytics and other Marketing Cloud solutions enables the use of the same data, audiences, and metrics in both solutions.
seo-title: Integrating Adobe Target with the Marketing Cloud
solution: Target
title: Integrating Adobe Target with the Marketing Cloud
topic: Standard
uuid: 96d0217d-94e2-488b-be55-83055882822a
index: y
internal: n
snippet: y
translate: y
---

# Integrating Adobe Target with the Marketing Cloud


>[!NOTE]
>
>Currently, you must contact Adobe Consulting to enable integration with Adobe Analytics.


This integration requires both the Adobe Target and Adobe Analytics solutions of the Adobe Marketing Cloud. Additional features are available if the Adobe Audience Manager solution is also used.
This integration is discussed in its own section. For more information, see [Adobe Analytics as the Reporting Source for Adobe Target (A4T)](a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE). 
For detailed information, refer to [Audiences](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html) in the Marketing Cloud Product Documentation. 
For more information, see [Target and Dynamic Tag Management](https://marketing.adobe.com/resources/help/en_US/dtm/target.html). 
To optimize your email content--for example, to display different offers for male and female recipients--you can create a redirect offer in Target, then use Adobe Campaign to manage the email offers.
The integration takes place when the email is opened. When the customer opens the email, a call is made to Target and a dynamic version of the content appears. The content consists of a static image supported by all browsers. Target tracks the reaction to the offer at the audience or session level and that data is available in Target reports.
Target can track the following data:

* User agent
* IP address
* Geographical location
* Segment associated with the visitor's ID in Target (subject to legal approval)
* Data from Campaign Datamart

There are several limitations:

* Because only an image can be used, content cannot be personalized.
* Tracking is not consolidated in Adobe Campaign.
* No unified user experience. You must use both Target and Campaign to set up different parts of the integration: 
    * The rawbox and the experience in Target
    * The delivery in Campaign




## Before You Begin {#section_FF19BF1BCA064260930BF6C141313B0E}

Before you use Adobe Campaign to set up your targeted email offers, set up the following in Target:

* Two or more Target redirect offers See [Create a Redirect Offer](https://marketing.adobe.com/resources/help/en_US/target/target/t_offer_redirect.html). 

* A Target activity with an experience for each offer and the desired [success metric](https://marketing.adobe.com/resources/help/en_US/target/target/r_success_metrics.html). See [Redirect to a URL](https://marketing.adobe.com/resources/help/en_US/target/target/t_redirect_offer.html). 


Start the activity in Target before setting up the Campaign portion of the integration.

## Include a Target Offer in an Adobe Campaign Email {#section_B201BBE27A704E18AF0D553F35695837}


1. Create an email in Adobe Campaign.
1. In the email properties, click ** `Include` ** > ** `Dynamic image served by Adobe Target` **.
1. Select the default image from the shared assets.
1. Specify the location (rawbox).
1. Add any other decisioning parameters, such as the gender of the recipient.
1. Preview the email, selecting at least one recipient for each offer (in this case, a male and a female).
1. In Campaign, define the Target Edge server you are using to control the activity and the name of the tenant.
1. Specify the external account used for the Marketing Cloud so you can access the resources in the Marketing Cloud.

For more information, refer to the Adobe Campaign documentation.
