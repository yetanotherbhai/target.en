---
description: Upload a CSV file to customize your recommendations.
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
seo-description: Upload a CSV file to customize your recommendations.
seo-title: Uploading Custom Criteria
solution: Target
title: Uploading Custom Criteria
title_outputclass: premium
topic: Premium
uuid: 8e5c4bdc-7f9d-4c0d-8f53-61eb9af8a7bd
badge: premium
index: y
internal: n
snippet: y
translate: y
---

# Uploading Custom Criteria

There are multiple ways to reach the [!UICONTROL  Create New Criteria] screen. Some screen options vary depending on how you reach the screen. 

* When you are creating a [!UICONTROL  Recommendations] activity, click **[!UICONTROL  Create New]** on the [!UICONTROL  Select Criteria] screen. You will have the option to save your new criteria for use with other [!UICONTROL  Recommendations] activities. 

* When you are editing a [!UICONTROL  Recommendations] activity, click in a [!UICONTROL  Recommendations Location] box on your page, and select **[!UICONTROL  Change Criteria]**. On the [!UICONTROL  Select Criteria] screen, click **[!UICONTROL  Create New]**. You will have the option to save your new criteria for use with other [!UICONTROL  Recommendations] activities. 

* On the **[!UICONTROL  Recommendations]** > **[!UICONTROL  Criteria]** library screen, click **[!UICONTROL  Create Criteria]**. Criteria you create here are automatically made available for all [!UICONTROL  Recommendations] activities. 


>1. Click **[!UICONTROL  Create Criteria]**.

>       ![](assets/button_CreateCriteria.png) 
>1. Select **[!UICONTROL  Upload Custom Criteria]**.

>       ![](assets/CreateNewCriteria_csv.png) 
>1. Type a **[!UICONTROL  Criteria Name]**.

>       This is the "internal" name used to describe the criteria. 
>1. Type a public-facing **[!UICONTROL  Display Title]** to appear on the page for any recommendations that use this criteria.

>       For example, you might want to display "People who viewed this viewed that" or "Similar products" when you use this criteria to show recommendations. 
>1. Type a short **[!UICONTROL  Description]** of the criteria.

>       The description should help you identify the criteria, and might include information about the purpose of the criteria. 
>1. Select an **[!UICONTROL  Industry Vertical]**.

>1. Select a **[!UICONTROL  Page Type]**.

>       You can select multiple page types. 

>       Together, the industry vertical and page types are used to categorize your saved criteria, making it easier to reuse criteria for other [!UICONTROL  Recommendations] activities. 
>1. Select a **[!UICONTROL  Recommendation Key]**.

>       For more information about basing criteria on a key, see [ Base the Recommendation on a Recommendation Key ](../../c_recommendations/c_algorithms/t_create_new_algorithm.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B). 
>1. Set your **[!UICONTROL  Content]** rules.

>       Content rules determine what happens if the number of recommended items does not fill your design. For example, if your design has space for five items, but your criteria causes only three items to be recommended, you can leave the remaining space empty, or you can use backup recommendations to fill the extra space. Select the appropriate toggles. See [ Content Settings ](../../c_recommendations/c_algorithms/t_create_new_algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96). 
>1. Set your **[!UICONTROL  Inclusion Rules]**.

>       [ Inclusion Rules ](../../c_recommendations/c_algorithms/t_create_new_algorithm.md#task_28DB20F968B1451481D8E51BAF947079)1. Select the **[!UICONTROL  Location]** of your CSV file.

>       The CSV file must be formatted correctly to upload successfully. Click **[!UICONTROL  Download the CSV template]** to get a correctly formatted CSV file. 

>       You have two location options: 

>    
>    * **FTP: **To upload your CSV file from an FTP server, select **[!UICONTROL  FTP]**, then enter the required information. You have the option to use SSL, which uses the FTPS protocol to transfer your CSV file securely. 

>    * **URL: **To upload your CSV file from a URL, select **[!UICONTROL  URL]**, then and enter a feed URL. 


>1. Click **[!UICONTROL  Save]**.


>       >[!NOTE]
>       >
>       >Custom criteria entities (rows) can contain up to 1,000 recommended items (columns).

