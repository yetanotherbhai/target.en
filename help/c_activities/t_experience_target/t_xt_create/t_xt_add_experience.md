---
description: The Experience Composer provides a visual interface for editing the experiences on your page.
keywords: create experience;experience create;priority;audience;experience;visual experience composer
seo-description: The Experience Composer provides a visual interface for editing the experiences on your page.
seo-title: Create Experience
solution: Target
title: Create Experience
topic: Advanced,Standard,Classic
uuid: eb57c73a-7934-4973-9e91-b71e3c91e001
index: y
internal: n
snippet: y
translate: y
---

# Create Experience

For additional detail about experiences, see [ Experiences ](../../../c_experiences/c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

>1. Click **[!UICONTROL  Add Experience]**.


>       >[!NOTE]
>       >
>       >If you are targeting an experience to an audience, you must select the audience before you can add an experience. A message appears to remind you to choose your audience.

>1. When prompted, enter the activity URL. Type the complete URL (including ` http://`), then click **[!UICONTROL  Continue]**.

>       The Experience Composer (see [ Experiences ](../../../c_experiences/c_experiences.md#concept_1D011219034B492BB03C08B3BB80E3F0)) opens the page that is specified in your [ Account Preferences ](https://marketing.adobe.com/resources/help/en_US/target/target/t_account_preferences.html). To display a different page, click the Globe icon and enter the URL in the Select URL box in the Experience Composer and click **[!UICONTROL  Continue]**. If you entered a URL for a site that does not include the Target Standard JavaScript code, you cannot select page elements. 

>       By default, the Visual Experience Composer does not allow changes to elements containing JavaScript, such as rotating banners. You can select to disable JavaScript if you want to be able to alter those elements using the Visual Experience Composer. 


>       >[!NOTE]
>       >
>       >If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.

>1. Select the elements you want to change and make the desired changes.

>       As you hover the elements on your page, the elements are highlighted. Any highlighted element can be altered using the Experience Composer. 

>       **Visual Experience Composer (1 of 2) (7:17)** 

>       The video below provides information about using the Visual Experience Composer options. 

>    
>    * Change the content of a page
>    * Change the layout of a page


>       >[!VIDEO](https://vimeo.com/2KUDgu6Mscg) 

>       If you created an mbox on the page using Target Classic (formerly Test&amp;amp;Target), that mbox appears as an element that shows the mbox name, and can be modified like any other element. 

>       The following actions can be performed on an element on the displayed page to change the experience: 



>       #### Title
>       |   |  |
>       |---|---|


>       >[!NOTE]
>       >
>       >If you deliver an image from a source other than your main page (such as an image hosted on akamai.net and delivered on dell.com), then that image does not display in the thumbnail of the page shown in the flow diagram.

>1. Click the Check Mark button when you are finished designing the experience.

>       The activity diagram displays: 

>       ![](assets/xt_diagram.png) 

>       If an experience includes cross-domain content, the thumbnail might not display accurately and is replaced by an icon. 
>1. Create additional experiences, as desired.


>       >[!NOTE]
>       >
>       >You can drag and drop audience/experience pairs while creating or editing XT activities to arrange the pairs in the desired order. Visitors will be evaluated for experiences in order, from top to bottom.


>       ![](assets/move_experiences.jpg) 

>       Experience Targeting assumes that order matters. If a visitor falls into the first audience/experience pair, the first experience is delivered. 

>       For example, suppose you were not aware that order matters while creating an XT activity. You later realize during testing that visitors that you think should qualify for experiences B or C are instead qualifying for experience A. This could be because the audiences are not mutually exclusive and are not in the proper order (for example, experience A = United States, experience B = San Francisco, and experience C = California). In this scenario, all users from the United States qualify for experience A, even if they are located in San Francisco or elsewhere in California. You can reorder the audience/experience pairs from most restrictive to least restrictive (San Francisco &amp;gt; California &amp;gt; United States) without re-creating the entire activity. 

>       Note that you can click the  ![](assets/icon_more_options.png) icon on an experience in an A/B Test or Experience Targeting (XT) activity and choose from the following options, as necessary: 
>    
>    * Rename 

>    * Edit 

>    * Delete 

>       ![](assets/experience_edit.png) 
>       **[!UICONTROL  Continue]**