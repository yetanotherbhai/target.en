---
description: Information about inserting experience fragments containing content and layout created in Adobe Experience Manager (AEM) into Target activities to aid optimization or personalization.
keywords: experience;aem;adobe experience manager;export to adobe target;experience fragments;fragments;XF
seo-description: Information about inserting experience fragments containing content and layout created in Adobe Experience Manager (AEM) into Target activities to aid optimization or personalization.
seo-title: AEM Experience Fragments
solution: Target
title: AEM Experience Fragments
topic: Standard
uuid: e477ff6b-33cd-41ef-a5d4-9a1a1fe94337
index: y
internal: n
snippet: y
translate: y
---

# AEM Experience Fragments

## AEM Experience Fragments {#topic_1E1E4EA01F074349B2CF8785387B5FE8}Information about inserting experience fragments containing content and layout created in Adobe Experience Manager (AEM) into Target activities to aid optimization or personalization.
>[!NOTE]
>
>The AEM Experience Fragments functionality is offered as a first-look feature to select customers to obtain feedback to help us improve the feature before making it available to all customers.



This section contains the following information: 


* [ Overview ](aem-experience-fragments.md#section_95A91830530F493B81C5C9CDB9B783EA) 

* [ Requirements ](aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A) 

* [ Creating and Configuring Experience Fragments in AEM ](aem-experience-fragments.md#section_745C8EFE29F547A2958FDBF61A5ADF7B) 

* [ Consuming Experiment Fragments in Target Activities ](aem-experience-fragments.md#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9) 



## Overview {#section_95A91830530F493B81C5C9CDB9B783EA}

Using experience fragments created in AEM in Target activities lets you combine the ease-of-use and power of AEM with powerful Automated Intelligence (AI) and Machine Learning (ML) capabilities in Target to test and personalize experiences at scale.&amp;nbsp;&amp;nbsp; 

AEM brings together all of your content and assets in a central location to fuel your personalization strategy. AEM lets you easily create content for desktops, tablets, and mobile devices in one location without writing code. There’s no need to create pages for every device—AEM automatically adjusts each experience using your content. 

Target lets you deliver personalized experiences at scale based on a combination of rules-based and AI-driven machine learning approaches that incorporate behavioral, contextual, and offline variables.&amp;nbsp; With Target you can easily set up and run A/B and Multivariate activities to determine the best offers, content, and experiences. 

Experience fragments represent a huge step forward to link the content/experience creators and managers to the optimization and personalization professionals who are driving business outcomes using Target. 

## Requirements {#section_AE6F0971E1574B3AA324003599B96E5A}

As a first-look feature, you must be provisioned with the Experience Fragments functionality within Target. In addition, you must be using AEM 6.3 with the appropriate feature pack. Your account representative can help ensure that you meet the requirements to use this feature if your company is provisioned with this feature. 

## Creating and Configuring Experience Fragments in AEM {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

In order to use AEM experience fragments in Target, you must perform the following steps: 



<table id="table_A7836BBD5DEB4A088E30B1B1445F2D15"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Task </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1: Integrate AEM with Target </p> </td> 
   <td colname="col2"> <p>For more information, see <a href="https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html" format="html" scope="external"> Opting into Adobe Analytics and Adobe Target </a> in the <i>Adobe Experience Manager 6.3</i> documentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2: Create the experience fragment </p> </td> 
   <td colname="col2"> <p>Experience fragments are created in AEM. For more information, see <a href="https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html" format="html" scope="external"> Experience Fragments </a> in the <i>Adobe Experience Manager 6.3</i> documentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3: Configure AEM to share the experience fragment with Target </p> </td> 
   <td colname="col2"> <p> 
     <ol id="ol_185B3C5984D64ECDB69BEC12CED8B6D9"> 
      <li id="li_832CAA9039EC4C9F81DA7841570C7489"> <p>From within AEM, select the desired experience fragment, then click <span class="uicontrol"> Properties </span>. </p> </li> 
      <li id="li_1B6DECBF48434D6DA61096C343AC91CD"> <p>Click the <span class="uicontrol"> Cloud Services </span> tab, then from the <span class="uicontrol"> Cloud Service Configuration </span> drop-down list, select <span class="uicontrol"> Adobe Target </span>. </p> <p> <p>Note:  The previous step assumes that someone in your organization has created the Adobe Target configuration. </p> </p> </li> 
      <li id="li_73024D20AC934D9591CCEFA558B4AE21"> <p>Click <span class="uicontrol"> Save &amp;amp; Close </span>. </p> </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4: Publish the experience fragment </p> </td> 
   <td colname="col2"> <p> 
     <ol id="ol_7700A6562F514538BBDB24EA542B3D2A"> 
      <li id="li_22D1CC5CDFD24EE29929DC4BDF87EEC9"> <p>From within AEM, select the desired experience fragment, click the <span class="uicontrol"> Publish </span> tab, then click the <span class="uicontrol"> Publish </span> button. </p> </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5: Export the experience fragment to Target </p> </td> 
   <td colname="col2"> <p> 
     <ol id="ol_B8797E6528C14F41BFB92564A9933F44"> 
      <li id="li_F2F2BF28564C422D824DF1E972E7C696"> <p>From within AEM, select the desired experience fragment, click <span class="uicontrol"> Export to Adobe Target </span>, then click <span class="uicontrol"> OK </span>. </p> <p style="text-align: center;"> <img href="graphics/experience fragment export to target.png" id="image_5A03C93F0A7D40B786D77DE24E24C16B" /> </p> </li> 
     </ol> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Consuming Experiment Fragments in Target Activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

After performing the preceding tasks, the experience fragment displays on the [!UICONTROL  Offers] page in Target. 

You can hover over an experience fragment in the list, then click the View icon (  ![](graphics/icon_info.png) ) to see additional information about the experience fragment, including its public offer delivery URL, its AEM path, and a deep link to open the experience fragment inside of AEM. 

You can consume Experience Fragments in Target activities using the Visual Experience Composer (VEC) or the Form-Based Experience Composer. 

>[!NOTE]
>
>To fully utilize Target's AI and ML functionality, you can select[ Auto-Allocate ](automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) or [ Automated Personalization ](t_automated_personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) while creating an A/B Test. 

**To consume Experience Fragments using the VEC:** 


1. In Target, while creating or editing an experience in the [ Visual Experience Composer ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), click the location on the page where you want to insert AEM content, then select ** [!UICONTROL  Swap with Experience Fragment] ** to display the [!UICONTROL  Choose an Experience Fragment] list. 


   >[!NOTE]
   >
   >The [!UICONTROL  Swap with Experience Fragment] option is not available for images. If you want to use this option with an image, click the container element that contains the desired image. 


   The [!UICONTROL  Experience Fragment] list displays all of the content created in AEM that is now natively available from within Target. 

   ![](graphics/experience fragment list.png) 

1. Select the desired experience fragment, then click ** [!UICONTROL  Save] **. 

1. Finish configuring the activity. 

   For more information about configuring the various activity types, see the following topics: 


    * **A/B Test: ** [ Create an A/B Test ](t_test_ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) 

    * **Auto-Allocate: ** [ Auto-Allocate ](automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 

    * **Auto-Target: ** [ Auto-Target For Personalized Experiences ](c_auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3) 

    * **Automated Personalization (AP): ** [ Creating an Automated Personalization Activity ](t_automated_personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) 

    * **Experience Targeting (XT): ** [ Create an Experience Targeting Activity ](t_experience_target.md#task_D6B3429AC31549E1A70EDF04B3DDC765) 

    * **Multivariate Test (MVT): ** [ Create a Multivariate Test ](c_multivariate_testing.md#task_BF870FA60A8245AB8F0B775BE32EA710) 

    * **Recommendations: ** [ Create a Recommendations Activity ](t_create_recs_activity.md#task_6874328773C64C44A73F0A130AD3F96F) 





**To consume Experience Fragments using the Form-based Experience Composer:** 

1. In Target, while creating or editing an experience in the [ Form-Based Experience Composer ](t_form_experience_composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), select the location on the page where you want to insert AEM content, then select ** [!UICONTROL  Change Experience Fragment] ** to display the [!UICONTROL  Choose an Experience Fragment] list. 

   ![](graphics/experience fragment list.png) 

   The [!UICONTROL  Experience Fragment] list displays all of the content created in AEM that is now natively available from within Target. 

1. Select the desired experience fragment, then click ** [!UICONTROL  Save] **. 

1. Finish configuring the activity. 

