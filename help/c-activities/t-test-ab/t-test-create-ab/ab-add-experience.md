---
description: The Visual Experience Composer provides a visual interface for editing the experiences on your page.
keywords: Targeting;experience;add experience;experience add
seo-description: The Visual Experience Composer provides a visual interface for editing the experiences on your page.
seo-title: Add experience
solution: Target
title: Add experience
uuid: 9cb4c897-8701-4737-aec8-b0d4f5d62b94
---

# Add experience{#add-experience}

The Visual Experience Composer provides a visual interface for editing the experiences on your page.

For additional detail about experiences, see [Experiences](../../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

1. Click **[!UICONTROL Add Experience]**.

   >[!NOTE]
   >
   >If you are targeting an experience to an audience, you must select the audience before you can add an experience. A message appears to remind you to choose your audience.

1. When prompted, enter the activity URL. Type the complete URL (including `https://`), then click **[!UICONTROL Continue]**.

   The Experience Composer (see [Experiences](../../../c-experiences/experiences.md#concept_1D011219034B492BB03C08B3BB80E3F0)) opens the page that is specified in your Account Preferences. To display a different page, click the Globe icon and enter the URL in the Select URL box in the Experience Composer and click **[!UICONTROL Continue]**. If you entered a URL for a site that does not include the Target Standard JavaScript code, you cannot select page elements.

   By default, the Visual Experience Composer does not allow changes to elements containing JavaScript, such as rotating banners. You can select to disable JavaScript if you want to be able to alter those elements using the Visual Experience Composer.

   >[!NOTE]
   >
   >If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.

1. Select the elements you want to change and make the desired changes.

   As you hover the elements on your page, the elements are highlighted. Any highlighted element can be altered using the Experience Composer.

   If you created an mbox on the page using Target Classic (formerly Test&Target), that mbox appears as an element that shows the mbox name, and can be modified like any other element.

   For a list of actions that can be performed on an element on the displayed page to change the experience, see [Visual Experience Composer Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md)


   >[!NOTE]
   >
    >If you deliver an image from a source other than your main page (such as an image hosted on akamai.net and delivered on dell.com), then that image does not display in the thumbnail of the page shown in the flow diagram.

1. Click the Check Mark button when you are finished designing the experience.

   The activity diagram displays:

   ![](assets/ab_flodia.png)

   If an experience includes cross-domain content, the thumbnail might not display accurately and is replaced by an icon. 
   
1. Specify the percentage of visitors who will see each experience in the activity.

   You can show multiple experiences to the same audience. A diagram displays showing your selected audience and the experiences you've added to the activity. Specify the percentage of times you want each experience to be shown. You can split the percentages evenly between all experiences, or specify higher or lower percentages for each experience. The total for all experiences must equal 100%. You can also click **[!UICONTROL Add Experience]** to add another experience to the activity.

   Click **[!UICONTROL Continue]** when you are finished with this step. 

## Rename, edit, or delete an experience

Note that you can click the More (three vertical ellipses) icon on an experience in an A/B Test or Experience Targeting (XT) activity and choose from the following options, as necessary: 

* Rename 
* Edit 
* Delete 

![](assets/experience_edit.png)

Note that when you name or rename an experience, the following characters are not allowed: 

| Character | Description |
|--- |--- |
|/|Forward slash|
|?|Question mark|
|#|Number sign|
|:|Colon|
|=|Equals to|
|+|Plus|
|-|Minus|
|@|At sign|

## Duplicate an Experience

You can copy an experience in an A/B Test so you can make minor changes to it without having to re-create the experience from scratch. 

On the **[!UICONTROL Experiences]** page (the first step in the three-step guided workflow), click the three vertical ellipses > **[!UICONTROL Duplicate]**. 

![](assets/duplicate_experience_ab.png)

## Training video: Using the Visual Experience Composer

The video below provides information about using the Visual Experience Composer options. (7:17)

* Change the content of a page 
* Change the layout of a page

>[!VIDEO](https://www.youtube.com/watch?v=2KUDgu6Mscg)
