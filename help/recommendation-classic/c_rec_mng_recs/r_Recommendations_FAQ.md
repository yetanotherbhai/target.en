---
description: The Recommendations FAQ contains answers to common questions.
seo-description: The Recommendations FAQ contains answers to common questions.
seo-title: Recommendations FAQ
solution: Target
title: Recommendations FAQ
topic: Recommendations
uuid: a0376d60-415d-4b26-900b-d3cea02e330c
index: y
internal: n
snippet: y
translate: y
---

# Recommendations FAQ


>**Can I turn off backup recommendations?** 

>Yes. Keep in mind that backup recommendations apply to all campaigns, not just one. Also, if backup recommendations are disabled and there aren't enough real recommendations to fill the number of slots in the template, then default content is shown. 

>**Can I geo-target recommendations?** 

>Use the built-in profiles that are shown in the Available Tokens window when creating a new user script profile in Adobe Target. They are: 

>
>* profile.geolocation.city
>* profile.geolocation.country
>* profile.geolocation.dma
>* profile.geolocation.state
>* profile.geolocation.zip


>** Does the recommendations server store products in its back-end database independently for each campaign or is the data shared across all campaigns? For example, if I create a new campaign, then download the .csv file, does the file already have data in it, because data has already been collected for another campaign, or do I get a new, empty .csv file? What if I create a new algorithm in an existing recommendation, then download the .csv file?** 

>Data is gathered the moment mboxes start sending recommendation data. This data is stored at the account level. Recommendations do not need to be set up for this data to be gathered. Once the algorithm runs the first time (usually within 30 minutes of setup), you have a full, ready to use recommendation. Recommendations driven from Adobe Analytics data work historically as well; therefore, as soon as you set it up you can pull usage data from up to two months in the past. 

>** To collect data for multiple algorithms, do I need to set up each type of algorithm up front, or will setting up just one type of algorithm capture data relationships for all other algorithm types?** 

>Data collection is not tied to algorithm or recommendation setup. 

>**How long is back-end data stored? Does it disappear after a certain amount of time? How long is reporting stored? Does it disappear after one year like other Adobe Target data?** 

>Usage data that drives an algorithm is completely separate from performance report data. Usage data expires after two months. Product data expires after 60 days. Performance report data follows the Target expiration rules. 

>** Is data in the .csv files ordered in the same way that it appears in a display recommendation? ** 

>Yes. For example, for a *Purchase Affinities* algorithm, if column A is the key, then column B is the product most often purchased with product A. Column C is the second most purchased item with product A, and so on. 

>**What actions will reset the campaign's CSV data? ** 

>When you change a campaign's catalog setting, algorithm type, or template, the cross-sell data (CSV) for that campaign will reset to prevent any information that is no longer viable from displaying. 

>**What actions will reset the Recommendation reporting data? ** 

>
>* Switching mboxes
>* Switching algorithms
>* Switching templates


>** How many recommended products are stored for each key? Does it depend on the algorithm? ** 

>More is displayed in the .csv file than is supported in display. Up to 20 products are displayed, but more can be included in the .csv if you want to use that data for other purposes. 

>**When I download the .csv file, does it only download data for the time frame specified when setting up a recommendation, or does it download all data?** 

>The .csv file follows the rules established in the algorithm setup, except for any information filtered at display time (price limit and inventory limit). For example, if you set up a recommendation to use two weeks of data and only include ` brand=jjesquire`, your download only includes activity for JJ Esquire products for the last two weeks. 

>**What is the difference between ` entity.categoryId` and the regular parameter ` categoryId`, and is there a priority system? ** 

>The ` categoryId`parameter is given higher weight than either ` entity.category` or ` entity.categoryId`even if ` categoryId` is in the URL and ` entity.categoryId` is in the mbox. 

>** If the character limit is exceeded, how are the categories prioritized? Which ones will be saved?** 

>Categories are prioritized by chronology. The first category passed is the first one in the list of categories that a product belongs to. 

>**How many categories can a product support?** 

>There is a 250-character limit for ` categoryId`. 

>**What is the default setting for conversion, restart the same experience or is it always convert? ** 

>It's restart the same experience. So, two visitors, two conversions. 

>**How many views are needed for a product before a recommendation is served? For example, if two products are viewed once in one session will they then be related to display in the view affinity recommendation for the next user? ** 

>At least two sessions are required. Two people need to view the same product. 
>[!MORE_LIKE_THIS]
>
>* [ Adobe Recommendations Home ](recs_home.md#topic_74F655D8648E4586BCCFD789E60D13CE)
>* [ Getting Started ](c_gettingstarted_recs.md#concept_CCF04F19782145099178353D37517D9E)
>* [ Managing Your Recommendations ](c_rec_mng_recs.md#concept_8BD886F4E0954B46B8EC0EA4626A00E1)
>* [ Managing Templates ](c_Managing_Templates.md#concept_C3A712A99D47406C855955161DB699A1)
>* [ Managing Recommendations Settings ](c_Managing_Recommendations_Settings.md#concept_70257C38F0A74F3E88B1E7ED278A8DB4)
>* [ Managing Mboxes ](c_Managing_Mboxes.md#concept_B2EE9F6FDDD74A5AAAE6D14C263BCDEB)
>* [ Using the Recommendations Download API ](r_Using_the_Recommendations_Download_API.md#reference_09DA9D1AB3884CEC9144C7BDD07AB30A)
>* [ Deleting an Item From the System ](r_Deleting_an_Item_From_the_System.md#reference_9D644188516045E295DD69065118ED2D)
>* [ Deleting All Items From the System ](r_Deleting_All_Items_From_the_System.md#reference_A916F48DE01E41DA81F2C35AF2A5E58F)
>* [ Integrating Recommendations with Email ](r_Integrating_Recommendations_with_Email.md#reference_256B16C894864F24AF970E43DC174420)
