---
description: The following steps outline the process of setting up behavioral targeting.
seo-description: The following steps outline the process of setting up behavioral targeting.
seo-title: Behavioral targeting basic steps
solution: Target
title: Behavioral targeting basic steps
topic: Standard
uuid: 8d5f25c0-f436-491f-9429-36118f2b1098
index: y
internal: n
snippet: y
---

# Behavioral targeting basic steps

The following steps outline the process of setting up behavioral targeting.

1. Define your business objective.

    * Clear out old inventory? 
    * Highlight a niche product? 
    * Increase form completion from female visitors? 
    * Map your customer segmentation to your Web content.

1. Define the user most likely to help you.

    * Who are these people? 
    * Start with simple, broad segments and refine them over time.

1. Define the behaviors the user is most likely to exhibit.

    * Are they a return visitor? 
    * Are they a frequent visitor? 
    * What pages do they visit? 
    * Have they filled out a form before? 
    * Have they purchased something before? 
    * Are they weekend shoppers? 
    * Did they come from specific search engines? Social referrers? 
    * Do they come primarily from certain geographies?

1. Capture relevant behaviors in profiles.

    * Custom created labels for your users 
    * Stored in databases and associated with your visitor through a cookie 
    * Two strategies: either in-mbox profile parameters or [script profile parameters](../../../c-target/c-visitor-profile/c-profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2) 
    * In-mbox profile parameters are placed in the page's mboxCreate call:

      ```    
      <script type="text/javascript"> 
       
         mboxCreate('myMbox', 'profile.name1=value1', 'profile.name2=value2'); 
       
      </script> 
       
      <script type="text/javascript"> mboxCreate('myMbox', 
       
      'profile.name1=value1', 'profile.name2=value2'); </script>
      ```

    * Script profile parameters are defined with JavaScript in the admin tool:

        1. Select **[!UICONTROL Segments]** > **[!UICONTROL Profiles]**.

        1. Clicking **[!UICONTROL add attribute]** to add a new parameter. 
        1. Name your profile and type the JavaScript code into the text fields.

        1. Click **[!UICONTROL Start]** to start the script.

      The profile data is now available for use in campaigns.

1. Target content to those users based on their profiles.

    * Create offers and use the targeting features to send that content to specific users.

