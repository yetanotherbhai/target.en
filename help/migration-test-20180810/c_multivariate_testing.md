---
description: Multivariate Testing (MVT) compares combinations of offers in elements on a page to determine which combination performs the best for a specific audience, and identifies which element most impacts the activity's success.
keywords: Mobile Web Experience Editor
seo-description: Multivariate Testing (MVT) compares combinations of offers in elements on a page to determine which combination performs the best for a specific audience, and identifies which element most impacts the activity's success.
seo-title: Multivariate Test
solution: Target
subtopic: Mobile Viewports
title: Multivariate Test
topic: Standard
uuid: 70013527-26dd-4932-876d-1a6eacc657fe
index: y
internal: n
snippet: y
translate: y
---

# Multivariate Test

## Multivariate Test {#concept_628695CDC71B449B8DCC2F5654C11499}Multivariate Testing (MVT) compares combinations of offers in elements on a page to determine which combination performs the best for a specific audience, and identifies which element most impacts the activity's success.
## MVT Overview {#section_C73A2D1409EC42C9B0EDD4B976651C5E}

This video explains how to understand, plan, and create a multivariate test using the Target three-step guided workflow. 



<table id="table_33BCDB2150924461AAC293736DBB5E1B"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Multivariate Tests </th> 
   <th colname="col3" class="entry"> 9:25 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/X8w5IQqEOow/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/X8w5IQqEOow/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_E55300E2EFA5405F86A6707FA5E3798F"> 
      <li id="li_E507A698929F4A4CAA9AF9ED08254B37">Define and design a multivariate test </li> 
      <li id="li_ED282D46E29F41868EDC373B79C71F1D">Create a multivariate test </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Multivariate testing can help you discover the relative influence specific elements have on conversion, compared to other elements on the page. It can also help you refine a combination of elements that have been shown to be effective. 

One advantage a multivariate test provides compared to an A/B test is the ability to show you which elements on your page have the greatest influence on conversion. This is also known as the "main effect." This information is useful, for example, by helping you determine where to place content that you want to receive the most attention. 

Multivariate tests also help you find compound effects between two or more elements on a page. For example, a particular ad might produce more conversions when combined with a certain banner or hero image. This is also known as the "interaction effect." 

Adobe Target uses full-factorial multivariate tests to help you optimize your content. A full-factorial multivariate test tests all of the possible combinations of content with equal probability. For example, if you have two page elements with three offers each, there are nine possible combinations (3x3). Three elements, with two containing three possible offers and one with two offers, provide 18 options (3x3x2). 

In Target, each combination is one experience. The multivariate test compares each experience so you can learn which combinations are the most successful. At the same time, data is collected and analyzed to understand how each location and the offers influence the success metric. 

![](graphics/multivariate.png) 

Because of the number of combinations that can be generated, a multivariate test requires more time and traffic than an A/B test. The page must receive enough traffic to produce statistically significant results for each experience. To obtain useful results, you need to understand the amount of traffic your page receives and test the optimal number of combinations for the right amount of time to get the required results. Target's [ Traffic Estimator ](c_multivariate_testing.md#task_71AA6922AFD447EA8C5E610A78ABA714) can help you design a test that works with your traffic. Before you use the Traffic Estimator, you should have good statistics showing the number of impressions and conversions your site normally receives. Consider your traffic levels per day. The more experiences in an activity, the more traffic the activity will need to include or the longer your activity will need to run. If your traffic isn't very high, you should test a small number of combinations; otherwise, the amount of time required to produce meaningful test results might be too long to be useful. 

This video explains the activity types available in Target Standard/Premium. Multivariate testing is discussed beginning at 4:20. 



<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Types </th> 
   <th colname="col3" class="entry"> 9:03 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/vtHg1pPFJp8/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/vtHg1pPFJp8/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F"> <p>Describe the types of activities included in Adobe Target </p> </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F"> <p>Select the appropriate activity type to achieve your goals </p> </li> 
      <li id="li_6C4D1871E45D40118D7D9D4DF81547B5"> <p>Describe the three-step guided workflow that applies to all activity types </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## MVT Terminology {#section_DF475CA7F34B4CFDB7BE7363761D64AE}

When setting up a multivariate test, it is useful to understand some basic terminology. 

There are multiple terms used in different ways across the industry. This section defines the terms used by Target. 

**Combination: ** The content variations created when you test multiple content options in multiple locations. For example, if you are testing three locations, each with three content options, then there are 27 possible combinations (3x3x3). A visitor to your site will see one combination, also referred to as an experience. 

**Content: ** The text or image comprising a test variation within a location. In a multivariate test, a number of content options within multiple locations are compared. In MVT methodology, the content is sometimes referred to as a *level*. 

**Element: ** A DOM element containing content variations to be tested in the MVT test. See also *Location*. 

**Location: ** A specific content area on a page, often contained by a single DOM element. In MVT methodology, a location is sometimes referred to as a *factor*. A full-factorial multivariate test compares all possible combinations of offers in your locations. 

## When to Use MVT vs A/B {#section_3D2B966B6671406C861A1843EA41D28C}

Multivariate tests can be used together with A/B tests to optimize your page. Examples of when you might want to use them together include:
* Use an A/B test to optimize your page layout, followed by an MVT test to determine the best content in each element on the page 

  An A/B test can provide important feedback on the layout, and MVT tests excel on testing the content within the elements in your page design. Running an A/B test on the layout before testing multiple content options can help you determine te best layout and the most impactful content. 

* Use an MVT test to determine which element is the most important, then follow up with a more focused A/B test on that element. 

  When the number of different experiences exceed five and span two or more elements, it's a good idea to consider an MVT test before running your A/B tests. The multivariate test shows which areas on the page are most likely to improve conversion. These are the elements that a marketer should focus on. For example, the MVT test might show that the call to action is the most important element for meeting your goals. Once you have determine which elements and content are most useful for helping you meet your goals, you can run an A/B test to further refine the results, such as to test two specific images against each other, or comparing the wording or colors of a call to action. By following an MVT test with one or more A/B tests, you can determine the best possible content for the results you desire. 



## Considerations {#section_979FE3F398654C1EA1C86E7DBC9A8DAD}


* Use an MVT test when you have at least three elements to test. If you have fewer, run a series of A/B tests. 

* Select the page elements you believe will have the strongest impact on the results.
* Don't include too many elements or locations in a test. The larger the number, the longer the test duration will be. 

* Plan the test design in advance. It's not advisable to edit a test once it goes live and data starts being collected and analyzed. 

* It is recommended that elements be independent of each other. For example, do not test your layout and content in the same test. 

* Plan additional time for QA because of the increase in the number of experiences. 

  Target offers full-factorial multivariate testing as a built-in activity option. In statistics, Design of Experiments offers many approaches, or designs, to determine which factors influence results. One such approach is the Taguchi Method for partial-factorial testing. Taguchi enables marketers to make a set of assumptions that reduce the number of permutations of experiences that need to be tested, and in turn decreases the traffic requirements for a multivariate test. This functionality and testing approach can be leveraged in Target Standard/Premium using [ this offline spreadsheet ](https://marketing.adobe.com/resources/help/en_US/target/mvt/MVT-Taguchi-Partial-Factorial-Design-02102017.xlsx). 

  If your team uses other Design of Experiments approaches, you can use this calculation spreadsheet as a reference implementation for custom experiment designs. 

  As you use the offline calculation spreadsheet, consider the following tips: 


    * Pick the elements you want to change and the number of versions of each element (3x2, 4x3, and so forth). 

    * Keep the numbering consistent. For example, if the button is Element 1 and the options are Blue, Green, and Yellow, the blue button is 1-1, the green button is 1-2, and the yellow button is 1-3. 

    * The offline spreadsheet provides the appropriate number of experiences needed (four for a 3x2, nine for a 4x3, and so forth). 

    * Build the experiences in the A/B workflow with the Form-based Experience Composer or the Visual Experience Composer (VEC). If you use the VEC, you can use custom code, edit HTML, WYSIWYG, or any combination. 

    * After the activity is over (based on the sample size calculator), run results through the spreadsheet to get the other details. 





For more considerations and best practices, see [ Multivariate Test Best Practices ](c_multivariate_testing.md#reference_53635817FFB741EF8C4E56CC70688EDD). 
>## Multivariate Test Best Practices {#reference_53635817FFB741EF8C4E56CC70688EDD}This topic lists tips that will help you improve performance, avoid issues, and correct known issues that might occur. 
<draft-comment otherprops="merge">
  mvt/r_best_practices.xml 
</draft-comment>
## Plan {#section_4D4A1F6226F042379BF48DB753608579}


* Be aware of the locations on your page that are likely to produce significant results. 

  For example, a banner or a hero image is probably going to lead to more conversions that a change in the footer. Including less-influential locations in your test only increases the amount of traffic and time required to test the more prominent locations on the page. 

* Prepare your page variations ahead of time. 

  Be aware of the content differences for each offer, and create any images, text, and HTML offers that you expect to use in the MVT test. 



## Create {#section_C59C722CA82E48ABA58A4A7FA758F193}


* Don't include more combinations than necessary for the test. 

  Every combination tested significantly increases the amount of traffic and time required to achieve acceptable results. For example, if you have three locations with three offers each, there are 27 possible combinations (3x3). Three locations, where two contain three possible offers and one has two offers, provide 18 options (3x3x2). The numbers increase substantially with each additional location and offer. 

* Name locations and offers. 

  You can rename each location and offer in your test to something more useful. The number of offers in each location appears in the location header. Useful names will help you identify your offers when examining reports. 

* Take advantage of the preview features to avoid undesirable combinations of content. 

  Review all the experiences generated by your test before going live. Make sure there are no combinations with contradictory claims (for example, 20% off and $19 off in the same experience) or incompatible designs such as having background and font of the same color. 

* Use the Traffic Estimator to make sure that your test is designed for the amount of traffic your page receives. 

  Make sure the Traffic Estimator gives your test configuration the green light so you can get the results you desire. 

* It is recommended that each element's alternatives be significantly different from each other. 



## Analyze {#section_9A2118CF1039451681C13D9AE79A58AB}


* Make frequent use of the Location Contribution report to monitor the performance of each location and each offer. 

* In the Experience Performance report, base your decisions on the data shown using the Best 5 and Worst 5 filters. 

  The All filter makes it difficult to extract the desired information, and not all experiences can display in the graph. Only use All if you want to look at a specific experience that is not in the best or worst five. 



## Follow Up {#section_1C44A767F6AB4441A3EAA8AC995F46B0}


* Although Target allows you to edit a live activity, be aware that editing an activity that is in progress could reset the test. 

  Target allows you to edit a live activity. Be aware that editing an activity that is in progress could reset the test, so reports might not recognize some of the changes. It is safe to make small changes, such as editing existing text or html offers. 

  The specific actions that reset experience names and reports are: 


    * Adding a new location 

    * Deleting a location 

    * Adding new offers or deleting offers from an exiting location 



* By following an MVT test with one or more A/B tests, you can determine the best possible content for the results you desire. 

  Once you have determined which locations and content are most useful for helping you meet your goals, you can run an A/B test to further refine the results. For example, when you know which locations are most important, test two specific images against each other, or comparing the wording or colors of a call to action. 


>## Plan a Multivariate Test {#concept_7B55D3D9DF25430EA91E071476EFE0F4}Multivariate Tests require some planning before you can create a successful test. 
<draft-comment otherprops="merge">
  mvt/c_plan_mvt.xml 
</draft-comment>This video demonstrates how to plan and create a multivariate test using the Target three-step guided workflow. 



<table id="table_7174E7A100264AFDA9A25793FE854A02"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Multivariate Tests </th> 
   <th colname="col3" class="entry"> 9:25 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/X8w5IQqEOow/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/X8w5IQqEOow/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_3CEB2CE98AF74CAAA7CB86C99B623ECC"> 
      <li id="li_07F169766FD14BAAAC26E7D9A05DFCDA">Define and design a multivariate test </li> 
      <li id="li_17E45068A42D40CE8E8675F5AAA3B37D">Create a multivariate test </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Multivariate tests require sufficient traffic to generate useful results. Before setting up your test, you should be aware of the amount of traffic you typically get, including the number of impressions and conversions. Having this information will reduce the likelihood of designing a test with requirements that exceed your site's traffic. 

It is recommended that elements be independent of each other. (For example, do not test your layout and content in the same test.) 

Examine the HTML code for the pages you want to test. Make sure the HTML elements on your site do not have duplicate DOM IDs. Duplicate IDs can result the same piece of content being delivered to more than one location. 

Plan to test the elements on your page that are likely to produce significant results. For example, a banner or a hero image is probably going to lead to more conversions that a change in the footer. Including less-influential elements in your test only increases the amount of traffic and time required to test the more prominent elements on the page. 

Finally, before you create your test, you should create the content you want to test. Understand the content differences for each offer, and create any images, text, and HTML offers that you expect to use in the test. 
>## Create a Multivariate Test {#task_BF870FA60A8245AB8F0B775BE32EA710}The Visual Experience Composer in Target makes it easy to create your test right on a Target-enabled page and to modify portions of the page within Target. 
<draft-comment otherprops="merge">
  mvt/t_create_multivariate_test.xml 
</draft-comment>This video demonstrates how to create a multivariate test using the Target three-step guided workflow. 



<table id="table_0368C430877545339FBA19BE31F49421"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Multivariate Tests </th> 
   <th colname="col3" class="entry"> 9:25 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/X8w5IQqEOow/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/X8w5IQqEOow/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_655B88B2ABA146DE9424C12B2C5A6556"> 
      <li id="li_E596DA05F60F4ECDB64397E30AF9B0DF">Define and design a multivariate test </li> 
      <li id="li_59352AA1FCB3445F8C29491F0C98D804">Create a multivariate test </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

The Target point-and-click editor enables you to pick any location and add multiple offers. 

The multivariate test takes a page-first report. In other words, the test runs on a specific URL, with the experiences you design for that page. 

>1. Click ** [!UICONTROL  Create Activity] ** > ** [!UICONTROL  Multivariate Test] **.

>       ![](graphics/create_mvt.png) 
>1. [ Specify the URL ](c_multivariate_testing.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) for the page you want to test, then click ** [!UICONTROL  Create Activity] **.

>       ![](graphics/url.png) 


>       >[!NOTE]
>       >
>       >Use a complete URL, including the HTTP or HTTPS at the beginning.


>       If a message appears, asking you to enable your browser for mixed content, follow the instructions in the message. After enabling your browser for mixed content, begin again at Step 1. 

>       The Visual Experience Composer opens. 

>       For troubleshooting information about the VEC, should you have problems, see [ Troubleshooting the Visual Experience Composer ](vec-best-pracitces-and-troubleshooting.md#reference_77743144F10143A3A89D56E116D296E4). 
>1. Type a name for the activity.

>       ![](graphics/activityname.png) 

>       The following characters are not allowed in an activity name: 

>       |  Character  | Description  |
>       |---|---|
>       |  /  | Forward slash  |
>       |  ?  | Question mark  |
>       |  #  | Number sign  |
>       |  :  | Colon  |

>1. [ Create the offers in each location ](c_multivariate_testing.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

>       ![](graphics/editoffers.png) 

>       You can add the following kinds of offers: 

>    
>    * HTML
>    * Image
>    * Text


>       You can rename each location and offer in your test to something more useful. The number of offers in each location appears in the location header. Useful names will help you identify your offers when examining reports. 
>1. [ Preview your experiences ](c_multivariate_testing.md#task_21A700587E88453A9FC2210C0DE53A28).

>       ![](graphics/preview.png) 

>       You can view each experience, and exclude any you do not want to include in your test. 
>1. [ Use the Traffic Estimator ](c_multivariate_testing.md#task_71AA6922AFD447EA8C5E610A78ABA714) to test the feasibility of your test plan.

>       ![](graphics/estimator.png)  ![](graphics/estimator2.png) 
>1. Choose the audience and percentage of qualifying visitors that you want to enter the activity.

>       ![](graphics/mvt_audperc.png) 

>       For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience. 


>       >[!NOTE]
>       >
>       >In addition to selecting an existing audience, you can combine multiple audiences to create ad hoc combined audiences rather than creating a new audience. For more information, see[ Combining Multiple Audiences ](c_audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5). 

>1. [ Review the test summary ](c_multivariate_testing.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) and make any desired changes, then click ** [!UICONTROL  Continue] **..

>       ![](graphics/mvtflow.png) 
>1. [ Specify the goals and settings ](c_multivariate_testing.md#reference_B25389FD6F3A4989801E740364B089CC) for the test.

>       ![](graphics/settings.png) 
>1. Click ** [!UICONTROL  Save and Close] ** to create the activity.
>## Activity URL {#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0}The Activity URL determines the page that is used in the test, and that opens when the test is designed. 
<draft-comment otherprops="merge">
  mvt/c_url.xml 
</draft-comment>When prompted during activity creation, enter the activity URL. Type the complete URL (including ` http://`), then click ** [!UICONTROL  Create Activity] **. 


>[!NOTE]
>
>[!DNL  Target] does not differentiate between URL protocols ( [!DNL  https] and [!DNL  http]). As a result, [!DNL  https://adobe.com] and [!DNL  http://adobe.com] both match. 



By default, the Visual Experience Composer opens the page that is specified in your [ Account Preferences ](https://marketing.adobe.com/resources/help/en_US/target/target/t_account_preferences.html). You can specify a different page during activity creation. 

To display a different page after the Visual Experience Composer opens, click ** [!UICONTROL  Configure] ** and select ** [!UICONTROL  URL] **, then enter the URL in the Activity URL box. 

![](../graphics/url-config.png) 

Click ** [!UICONTROL  Add Template Rule] ** to add more pages or sections to the activity. 

Additional rules can be based on any of the following: 


* URL
* Domain
* Path
* Hash (#) Fragment
* Query
* mbox Parameter


Additional rules can be joined to the Activity URL with AND or OR. All rules you add are evaluated against each other with AND. 

Click ** [!UICONTROL  Save] ** when you have finished. 


>[!NOTE]
>
>If you entered a URL for a site that does not include the Target Standard JavaScript code, you cannot select page elements.



By default, the [!UICONTROL  Visual Experience Composer] does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off ** [!UICONTROL  Render using JavaScript] ** if you want to be able to alter those elements using the [!UICONTROL  Visual Experience Composer]. 


>[!NOTE]
>
>If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.


>## Create Combinations {#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6}Use the Visual Experience Composer to create the offers you want to include in your test. 
<draft-comment otherprops="merge">
  mvt/c_add_offers.xml 
</draft-comment>You can include any of the following offer types in your test: 

* [ Image Offers ](c_multivariate_testing.md#section_A48333211DB149ED926AE467D0032914)
* [ HTML Offers ](c_multivariate_testing.md#section_DF016101AFA9412C9B99862C23DE77B1)
* [ Text Offers ](c_multivariate_testing.md#section_6CAD265D53534350BAC2780F10B140A8)

>[!NOTE]
>
>You can click ** [!UICONTROL  Expand Selection] ** when selecting objects on the page to select the parent element in addition to the originally selected element. When you select any parent element, all children of that element are automatically selected. You can expand the selection multiple times. 



The Visual Experience Composer makes it possible to edit offers, offer names, and location names. An overlay appears to show you where you have made changes. 

![](graphics/overlay.png) 

## Image Offers {#section_A48333211DB149ED926AE467D0032914}

Test multiple image offers within a location to determine which image is most successful. 


1. Click an image on your page, and then select ** [!UICONTROL  Change Image] **. ![](graphics/changeimage.png) 

1. Select all images you want to include in the test, then click ** [!UICONTROL  Add] **. ![](graphics/addimage.png) 



Each image becomes a separate experience in that location. 

## HTML Offers {#section_DF016101AFA9412C9B99862C23DE77B1}

Test multiple HTML offers within a location to determine which offer is most successful. 


1. Click an HTML offer on your page, then click ** [!UICONTROL  Change HTML] **. ![](graphics/changehtml.png) 

1. Click ** [!UICONTROL  Add HTML Offer] **, name the offer, then type or paste the code for the HTML offer. ![](graphics/editoffers.png) 


   >[!NOTE]
   >
   >Internet Explorer 10 does not support HTML5 input placeholders. As a result, if you use IE10, the "Add content" placeholder text remains in the Text field when you enter content.


   Repeat for any additional HTML offers you want to include. 

1. Click ** [!UICONTROL  Apply] **.


Each HTML offer becomes a separate experience in that location. 

## Text Offers {#section_6CAD265D53534350BAC2780F10B140A8}

You can test alternative text in text elements on your page. 


1. Click a text offer on your page, then click ** [!UICONTROL  Change Text] ** ![](graphics/changetext.png) 

1. Click ** [!UICONTROL  Add Text Offer] **, name the offer, and enter the text for the new offer. ![](graphics/changetexttext.png) 

   You can change the offer name for each offer. 

   Repeat for any additional text offers you want to include. 

1. Click ** [!UICONTROL  Apply] **.


Each text offer becomes a separate experience in that location. 

## Best Practices {#section_2E98C23D2F1A460FA732A31799CE6291}


* Don't include more locations than necessary for the test. Every experience you include in the test significantly increases the amount of traffic and time required to achieve acceptable results. For example, if you have page elements with three offers each, there are nine possible combinations (3x3). Three elements, where two contain three possible offers and one has two offers, provide 18 options (3x3x2). The numbers increase substantially with each additional element and offer. 

* When creating multivariate tests, you can now exclude more than 10 percent of experiences from the test, provided you acknowledge the warning that you must then use offline reporting for analysis. 

* Take advantage of the preview features to avoid undesirable combinations of content. For example, you might have two images that offer different discounts on the same item or service. Showing both of these images on the same page is illogical and is likely to create confusion. 

* Use the Traffic Estimator to make sure that your test is designed for the amount of traffic your page receives. Make sure the Traffic Estimator gives your test configuration the green light so you can get the results you desire. 

* You must have at least three elements to test. If you have fewer, run a series of A/B tests. 

* It is recommended that each element's alternatives be significantly different from each other. 

* Although not required, it is good practice for each element to have the same number of alternatives. 


>## Preview Experiences for a Multivariate Test {#task_21A700587E88453A9FC2210C0DE53A28}Because a multivariate test compares multiple experiences on a page, it is helpful to preview the page with each experience. 
<draft-comment otherprops="merge">
  mvt/t_preview_experiences.xml 
</draft-comment>
>1. From the Experience Composer, click ** [!UICONTROL  Preview] **.

>       A list of all experiences appears. 

>       ![](graphics/preview.png) 
>1. Click an experience in the list to view that experience.

>1. To exclude an experience from the multivariate test, select that experience and click ** [!UICONTROL  Exclude] **.

>       ![](graphics/excludeexperience.png) 

>       You might exclude an experience that shows conflicting variations or an experience that is not aesthetically balanced. 


>       >[!NOTE]
>       >
>       >When creating multivariate tests, you can now exclude more than 10 percent of experiences from the test, provided you acknowledge the warning that you must then use offline reporting for analysis.


>       By default, all experiences are included in the multivariate test. To include an experience that has been excluded, select the excluded experience and click ** [!UICONTROL  Include] **. 
>## Estimate the Traffic Required for a Successful Test {#task_71AA6922AFD447EA8C5E610A78ABA714}Because a multivariate test compares multiple experiences, it is important to know how much traffic is required to provide meaningful results. The Traffic Estimator uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration needed to make the test successful. 
<draft-comment otherprops="merge">
  mvt/t_traffic_estimator.xml 
</draft-comment>The Traffic Estimator predicts the sample size needed to ensure the following: 


* 95% confidence 

  This means that the chance of reporting a false positive if there is no real lift is 5% (100% - confidence level). 

* 80% statistical power 

  This means that the test has a 80% probability of detecting a true lift of 25% or more. 

* 25% minimum reliably detectable lift 

  Target computes the amount of traffic required to have an 80% chance of detecting a true lift of 25% or more. 



The test uses the Bonferroni correction to correct for multiple comparisons. This method is known for being conservative, which is balanced out by enforcing a relatively large minimum reliably detectable lift. 

The Traffic Estimator also provides feedback that lets you know whether you have sufficient traffic for the test you designed to succeed. 

>1. From the Experience Composer, click ** [!UICONTROL  Traffic] **.

>       The Traffic Estimator opens. You can click ** [!UICONTROL  Traffic] ** again to hide the Traffic Estimator. 

>       ![](graphics/estimatorempty.png) 
>1. Provide the typical conversion rate, estimated activity impressions per day, and test duration.

>    
>    * Number of Content Combinations 

>      Calculated automatically based on the number of experiences being created as a part of your activity after any exclusions. 

>    * Typical Conversion Rate 

>      The conversion rate is expressed as a percentage, based on your estimation or past data from your analytics system 

>    * Estimated Activity Impressions Per Day 

>      This is the number of visitors who are likely to view this page based on the targeting criteria. This could be based on your analytics data. 

>    * Test Duration 

>      The number of days you want the activity to run. 



>       The Traffic Estimator uses these statistics to determine what adjustments are needed to run a successful test. 

>       Near the top of the Traffic Estimator, the values you entered are calculated and the results are shown. 

>       ![](graphics/estimatorinsufficient.png) 

>       As you change the numbers, the estimate changes. For example, if you are testing a large number of experiences and your conversion rate and impressions are too low, the Traffic Estimator shows how long the test will need to run to be successful. Or, if your traffic is low, the Traffic Estimator might suggest a lower number of experiences so you can run the test the desired number of days. 

>       If you do not have sufficient traffic, you can do one or both of the following: 

>    
>    * Reduce the number of combinations of offers and the number of locations.
>    * Increase the duration of the test.


>       Adjust the numbers until the Traffic Estimator says you have sufficient traffic, then design your test accordingly. 

>       ![](graphics/estimatorok.png) 
>## Test Summary {#reference_971AB225963A4DC18EEB5B0E20F0A4A7}The test summary provides a visual overview of your multivariate test. 
<draft-comment otherprops="merge">
  mvt/r_test_summary.xml 
</draft-comment>
>![](graphics/summary2.png) 

>The test summary shows: 
>
>* Test name
>* URL
>* Audience Click the audience to select a different one from the list of available audiences. 

>* Algorithm Currently, the only available algorithm is Full Factorial. The algorithm name is provided for informational purposes, so you are aware of the algorithm being used. 

>* The numbers of included and excluded experiences.
>Click ** [!UICONTROL  Continue] ** when you are satisfied with the test configuration. The Goals and Settings page opens. 
>## Goals and Settings {#reference_B25389FD6F3A4989801E740364B089CC}The Goals and Settings page is where you enter information about the goals of the test. 
<draft-comment otherprops="merge">
  mvt/r_goals_and_settings.xml 
</draft-comment>
<a id="section_9B98C5E38DC244D0829B9B06CA627EA9"></a>


* Activity Settings
* Reporting Settings
* Other Metadata


This video includes information about activity settings. 

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Settings </th> 
   <th colname="col3" class="entry"> 3:02 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/6XNEM8tUADo/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/6XNEM8tUADo/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Enter an objective for your activity </li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405">Set the priority level of your activities </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Schedule activity start and end times </li> 
      <li id="li_699D4D5D089A4FB7BA4C5E95337AC34A">Add audiences for reporting to create report filters </li> 
      <li id="li_0EDDBA5E70B54F22A76F1D6D722914BE">Enter notes for your activities </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

This video demonstrates how to create a multivariate test using the Target three-step guided workflow. Goals and settings are discussed beginning at 7:00. 



<table id="table_6F26C2EA7336463AA952A096D5DFA99B"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Multivariate Tests </th> 
   <th colname="col3" class="entry"> 9:25 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/X8w5IQqEOow/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/X8w5IQqEOow/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_64641B23C08843DDA6F6B94D81E6C80F"> 
      <li id="li_595D9626314A4F0DA0D1DD0C694401FE">Define and design a multivariate test </li> 
      <li id="li_873A89BF532C48369F68C100609DD173">Create a multivariate test </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

The available settings depend on whether you use Target or Analytics as the data source. 

![](graphics/mvt_settings.png) 

## Activity Settings {#section_DCBDC354261F420EBD4B43EA34947BAC}



<table id="table_464BE186EE1F463DA99D16FC482A4AFA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Settings </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Objective </td> 
   <td colname="col2"> <p>Type an optional objective. The objective can be any information that helps you and your team members identify the campaign. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Priority </td> 
   <td colname="col2"> <p>Depending on your settings, the UI and options for <span class="wintitle"> Priority </span> vary. You can use the legacy settings of Low, Medium, or High, or you can enable fine-grained priorities from 0 to 999. </p> <p>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays. </p> <p>If this option is not enabled in <span class="wintitle"> Setup </span> (the default), specify a priority: Low, Medium, or High. </p> <p> To enable fine-grained priorities, click <span class="wintitle"> Setup </span>, then toggle the <span class="wintitle"> Enable Fine-Grained Priorities </span> option to the "On" position. </p> <p>If this option is enabled, specify a value between 0 and 999: </p> <p> 
     <ul id="ul_FCA07A04D6F248759429BC46BA57CCE5"> 
      <li id="li_88F440506D22467295C71F2B14470AD7">0 = Low </li> 
      <li id="li_AEC7893759464944A6501FA742A2B0FE">999 = High </li> 
     </ul> </p> <p>For activities created in previous versions of <span class="keyword"> Target Standard/Premium </span>, Low priority is converted to 0, Medium is converted to 5, and High is converted to 10. You can adjust these values as necessary. </p> <p> <p>Note:  Before you can disable this option after using fine-grained priories, all priorities must be set back to 0, 5, and 10. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Duration </td> 
   <td colname="col2"> <p>The activity can start when approved, or you can set a specific date and time. Likewise, the activity can either end when it is deactivated or you can set a date and time. The time picker uses a 24-hour clock, with 00:00 being midnight. The time zone is set to the time zone configured in your browser. To use a different time zone, set your browser to another time zone and restart the browser. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Reporting Settings {#section_13119392051044FBA6387D9B3B1C43CF}



<table id="table_178993EC689C4C538F3EC7E3FC205592"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Settings </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Reporting Solution </td> 
   <td colname="col2"> <p>Specify whether data is collected from Adobe Target or from Adobe Analytics. See <a href="https://marketing.adobe.com/resources/help/en_US/target/a4t/a4t.html" format="https" scope="external"> Adobe Analytics as the Reporting Source for Target </a> to learn about the differences between the reporting solutions and the advantages of each. </p> <p>When selecting Analytics as the reporting source for Target, you select an Analytics report suite to receive Target activity data. To do this, first choose from any of the Analytics companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to Adobe Target will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the Adobe Marketing Cloud to try again. If the report suite is still missing from the list, please contact Customer Care. </p> <p>Analytics for Target requires a tracking server to report results correctly. A default tracking server will appear in the Tracking Server field. If you use more than one tracking server, you should check to ensure you include the correct tracking server in this field. See <a href="../a4t/a4t.xml#task_72077BA7E93C4A65A715A18F32228823" format="dita" scope="local"> Using an Analytics Tracking Server </a> for more information. </p> <p>If a reporting solution is specified in your account settings, the specified solution is used and this setting is not visible. </p> <p> <p>Note:  You cannot change your reporting source after the activity goes live in order to keep reports consistent. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Goal </td> 
   <td colname="col2"> <p>Select the action taken by a visitor to achieve the goal. For example, choose a Conversion metric, then set the parameters that determine when success is achieved. </p> <p> <p>Note:  If the reporting solution is set to Analytics, the only available goal metric is Conversion. Analytics metrics cannot be selected as a goal. </p> </p> <p>When you select your success metric, a selector displays. Use this selector to choose the specifics for the success metric. </p> <p>If enabled, the Estimated Value of the Conversion field (not available for the Page Score metrics) provides a value for your goal, but not for other metrics. This value enables Target to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. For all revenue metrics (Revenue per Visitor, Average Order Value, Total Sales, and Orders), the estimate uses Revenue per Visitor. The data type is currency. </p> <p> After reaching the activity goal, a visitor continues to see the activity content, unless that visitor qualifies for a higher priority activity. If the visitor reaches the goal again, it is counted as another conversion. Note that this is different than the default behavior in Target Classic, which counts visitors as new if they see the test again. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Additional Metrics </td> 
   <td colname="col2"> <p>Create additional success metrics. </p> <p>This setting is not available if the reporting solution is set to Analytics. In this case, the metrics defined for the Analytics report suite are applied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Audiences for Reporting </td> 
   <td colname="col2"> <p>By default, reports show results for all qualified visitors. You can add report audiences to show only information about specific audiences. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Advanced Settings {#section_E2FE441AFB324E498793ABB025ED9974}

Advanced settings are available for Multivariate Test goal metrics. 

![](graphics/Menu_AdvancedSettings.png) 


>[!NOTE]
>
>If you use Adobe Analytics as your reporting source, settings are managed by the Analytics server. The advanced settings option will not be available.





<table id="table_5706360D23704F16AA18597D4C8F3438"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Which success metric must be reached before incrementing this metric? </td> 
   <td colname="col2"> <p>Use this option to only count someone as reaching the success metric if they’ve previously reached a different success metric. For example a test conversion might only be valid if the visitor clicks on the offer, or reaches a particular page before converting. </p> <p>You can provided dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increase. </p> <p>You must define both (or multiple) success metrics before you can make one dependent on another. </p> <p>The <span class="wintitle"> Add Dependency </span> option allows the success metric to increment if another success metric has been reached or has not been reached. </p> <p>To add a dependency: </p> <p> 
     <ol id="ol_7CE86C31CD5541039A3265E14D0C3630"> 
      <li id="li_3E374D8B28B443FA9FE8AF2B02814A82"> <p>After adding additional metrics, click <span class="uicontrol"> Advanced Settings </span>. </p> </li> 
      <li id="li_F65C369C8F354A6CBD447ED26D9F79E4"> <p>Click the <span class="uicontrol"> Add Dependency </span> option: </p> <p style="text-align: center;"> <img href="../graphics/add dependency.png" id="image_D3C6E4862509435E86A1F61B88F342CA" /> </p> </li> 
      <li id="li_9A6F187B4C294A9C8B5C834C76B32767"> <p>Drag and drop the desired metrics from the left pane into the right pane, then click <span class="uicontrol"> Reached </span> to toggle the setting between <span class="uicontrol"> Reached </span> and <span class="uicontrol"> Not Reached </span>. </p> <p style="text-align: center;"> <img href="../graphics/add dependency reached.png" id="image_CA136FD10D754BD1B26C621DF2A4858D" /> </p> </li> 
     </ol> </p> <p>You can edit or remove dependencies after adding them. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> What will happen after a user encounters this goal metric? </td> 
   <td colname="col2"> There are three options for what happens after a visitor reaches the goal metric: 
    <ul id="ul_2347FFB59E804DB382C3440BE684000E"> 
     <li id="li_5A8C13D4D43C436786D9FBE24C701CE1">Select <span class="uicontrol"> Increment Count &amp;amp; Keep User in Activity </span> to specify how the count is incremented. </li> 
     <li id="li_04D4A04310354FB4A7F23023E1FE0DE0">Select <span class="uicontrol"> Increment Count, Release User &amp;amp; Allow Reentry </span> to specify the experience the user sees if they reenter the activity. </li> 
     <li id="li_32FEAFA4C6BC469998C9181792B29BEE">Select <span class="uicontrol"> Increment Count, Release User &amp;amp; Bar from Reentry </span> to specify what the user sees instead of the activity content. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

See [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924) for more information about advanced settings. 

## Other Metadata {#section_2E8917BEFB954480A4206B9E9E917F80}



|  Settings  | Description  |
|---|---|
|  Notes  | Type any information about your activity that is useful to keep on hand for yourself or other team members. The Notes pane is resizable.  |

>## Set Metrics {#task_A04AB66007C1467DA1C21A519A5C7BEB}Use metrics in a Multivariate Test to determine when a visit is successful. 
<draft-comment otherprops="merge">
  mvt/t_mvt_set_metrics.xml 
</draft-comment>For detailed information about success metrics, see [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924). 

>1. Specify the goal of the activity.
>1. Select a [ success metric ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924)

>       ![](graphics/mvt_metrics.png) 

>       The [!UICONTROL  Select Metrics] page lists the success metrics you can choose for your activity. The success metrics are divided into the following categories: 

>    
>    * Conversion
>    * Revenue
>    * Engagement


>       You can use any of the pre-built success metrics, or create a custom success metric. You can also mark a success metric as a primary metric. Reports and Marketing Cloud cards default to show the primary metric, if one is set. 
>1. Specify the settings for your metrics.

>       The available settings depend on the success metric you are using. 

>       If enabled, the [!UICONTROL  Estimated Value of the Conversion]field (not available for the Page Score metrics) provides a value for your goal. This value enables Target to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. The data type is currency. This field is progressively shown after the user indicates the action taken to satisfy the goal. See [ Estimating Lift in Revenue ](c_estimating_lift_in_revenue.md#concept_32F875D8F91349CE86AF391F65BEAEEE) for more information. 

>       The correct configuration of success metrics is critical for making sure you get the data you expect. 

>       For more information, see [ Success Metrics ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924) 
>1. (Optional) Add additional metrics.
>1. Click ** [!UICONTROL  Continue] ** when you are finished setting your metrics.
>## Experience Performance Report {#concept_4470C6A177924695A6595B54E3A7FD90}The Experience Performance report shows how each experience in the activity performs.This report includes information about the number of entrants, the conversion rate, the lift, and the confidence. 
<draft-comment otherprops="merge">
  mvt/c_experience_performance_report.xml 
</draft-comment>This video demonstrates how to create a multivariate test using the Target three-step guided workflow. The Experience Performance report is described beginning at 8:20. 



<table id="table_77DBEEC9317244F2BE3FE16E6CE02798"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Multivariate Tests </th> 
   <th colname="col3" class="entry"> 9:25 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/X8w5IQqEOow/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/X8w5IQqEOow/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_D52ED76BE4904AC4AE3595F4BAA23C0C"> 
      <li id="li_EB1624CA5A7542F09CE25AF38C7981EC">Define and design a multivariate test </li> 
      <li id="li_68BDD4041ED741A782B4FD838F7B5019">Create a multivariate test </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

You can select one or more experiences to compare them. Click on an experience and select ** [!UICONTROL  Preview] ** to open the experience in a browser tab. 

![](graphics/experienceperformancetable.png) 

The top of the report shows the metric, start and end dates, and audience used in the report. You can change any of these factors. 


>[!NOTE]
>
>The audience and metric pickers are only available if Analytics is used as the reporting source.



Next, a line graph provides a visual comparison of each experience at specific time intervals. This graph helps you see how well each experience performs, and how the time of day affects performance. 

You can display the best five, worst five, or all experiences. The best and worst five are determined by lift, and include a sixth experience showing the control for comparison. It is suggested that you view the best and worst five to determine the success of your experiences. Viewing all makes it difficult to extract the desired information, and not all experiences can display in the graph. Use View All if you want to look at a specific experience that is not in the best or worst five. 


>[!NOTE]
>
>Multivariate test reports do not show any excluded experiences when either the Best Five or Worst Five filter is selected.



Below the graph, a table shows how many entrants saw each experience, as well as other information relevant to your success metric. 
>## Location Contribution Report {#concept_95A285CEDB674FE7A05B323AA2771906}The Location Contribution report shows the performance of each element and each offer. 
<draft-comment otherprops="merge">
  mvt/c_location_contribution_report.xml 
</draft-comment>This video demonstrates how to create a multivariate test using the Target three-step guided workflow. The Location Contribution report is described beginning at 8:45. 



<table id="table_F143B927DB0349849AF3E9CB20313CD3"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Multivariate Tests </th> 
   <th colname="col3" class="entry"> 9:25 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/X8w5IQqEOow/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/X8w5IQqEOow/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_3FC00E95274C42C5AE044781AC0A3900"> 
      <li id="li_8C3F61390B3348B98C1D0704B4DDE60A">Define and design a multivariate test </li> 
      <li id="li_9D59BAEA7B29469D9A22C67B79F4C803">Create a multivariate test </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

The top of the report shows the metric, start and end dates, and audience used in the report. You can change any of these factors. 


>[!NOTE]
>
>The audience and metric pickers are only available if Analytics is used as the reporting source.



The Location Contribution report includes two tables. 

The first table shows the relative influence of each element. This shows you which of the elements where you have added offers is resulting in the most conversions. 

![](graphics/locationcontributiontop.png) 

The second table provides an offer-level report. It shows the conversion rate, lift, and confidence for each offer in each element. This helps you determine which offers are the most successful. The second column shows values for the selected metric (conversion rate, RPV, AOV, orders, or engagement metrics) of the offer and one standardization. 

![](graphics/locationcontributionbottom.png) 
>## Troubleshooting Multivariate Tests {#reference_E4C33F55F38046F89125F6773BD034D0}This topic contains suggestions for resolving some issues that might occur when designing an MVT test. 
<draft-comment otherprops="merge">
  mvt/r_troubleshooting.xml 
</draft-comment>

* When editing an activity, if you used Analytics-based metrics and the report suite doesn't load (spinner displays), switch the metrics to Target metrics and then switch again to Analytics-based metric. The report suite should now load.
* If make changes to a test that is already running, you might reset the test and its data. Target allows you to edit a live activity. Be aware that editing an activity that is in progress could reset the test, so reports might not recognize some of the changes. 

  It is safe to make small changes, such as editing existing text or html offers. 

  The specific actions that reset experience names and reports are: 


    * Adding a new location
    * Deleting a location
    * Adding new offers or deleting offers from an exiting location



