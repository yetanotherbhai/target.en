---
description: The Activity URL determines the page that is used in the test, and that opens when the test is designed.
keywords: Targeting
seo-description: The Activity URL determines the page that is used in the test, and that opens when the test is designed.
seo-title: Activity URL
solution: Target
title: Activity URL
uuid: 37574580-5d5a-4009-aab1-b541707e3827
index: y
internal: n
snippet: y
translate: y
---

# Activity URL

When prompted during activity creation, enter the activity URL. Type the complete URL (including http://), then click **[!UICONTROL  Create Activity]**. 


>[!NOTE]
>
>[!DNL  Target] does not differentiate between URL protocols ( [!DNL  https] and [!DNL  http]). As a result, [!DNL  https://adobe.com] and [!DNL  http://adobe.com] both match. 



By default, the Visual Experience Composer opens the page that is specified in your [ Account Preferences](https://marketing.adobe.com/resources/help/en_US/target/target/t_account_preferences.html). You can specify a different page during activity creation. 

To display a different page after the Visual Experience Composer opens, click **[!UICONTROL  Configure]**, select **[!UICONTROL  URL]**, and enter the URL in the Activity URL box. 

![](assets/url-config.png) 

Click **[!UICONTROL  Add Template Rule]** to add more pages or sections to the activity. 

Additional rules can be based on any of the following: 


* URL
* Domain
* Path
* Hash (#) Fragment
* Query
* mbox Parameter


Additional rules can be joined to the Activity URL with AND or OR. All rules you add are evaluated against each other with AND. 

Click **[!UICONTROL  Save]** when you have finished. 

<a id="section_373CAB401E6A43EFA4D82E000581A4D3"></a>


>[!NOTE]
>
>If you entered a URL for a site that does not include the Target Standard JavaScript code, you cannot select page elements.



By default, the [!UICONTROL  Visual Experience Composer] does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off **[!UICONTROL  Render using JavaScript]** if you want to be able to alter those elements using the [!UICONTROL  Visual Experience Composer]. 


>[!NOTE]
>
>If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.


