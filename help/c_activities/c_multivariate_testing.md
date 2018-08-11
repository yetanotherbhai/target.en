---
description: Multivariate Testing (MVT) compares combinations of offers in elements on a page to determine which combination performs the best for a specific audience, and identifies which element most impacts the activity's success.
keywords: multivariate test;mvt;full factorial;mvt or a/b;multivariate a/b;traffic estimator;when to use mvt;mvt considerations;multivariate
seo-description: Multivariate Testing (MVT) compares combinations of offers in elements on a page to determine which combination performs the best for a specific audience, and identifies which element most impacts the activity's success.
seo-title: Multivariate Test
solution: Target
title: Multivariate Test
topic: Premium
uuid: 9d685f33-2fd8-4279-9197-95dab7fd6f1d
index: y
internal: n
snippet: y
translate: y
---

# Multivariate Test

This section contains the following information: 


* [ MVT Overview ](c_multivariate_testing.md#section_C73A2D1409EC42C9B0EDD4B976651C5E)
* [ MVT Terminology ](c_multivariate_testing.md#section_DF475CA7F34B4CFDB7BE7363761D64AE)
* [ When to Use MVT vs A/B ](c_multivariate_testing.md#section_3D2B966B6671406C861A1843EA41D28C)
* [ Considerations ](c_multivariate_testing.md#section_979FE3F398654C1EA1C86E7DBC9A8DAD)


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

![](../assets/multivariate.png) 

Because of the number of combinations that can be generated, a multivariate test requires more time and traffic than an A/B test. The page must receive enough traffic to produce statistically significant results for each experience. To obtain useful results, you need to understand the amount of traffic your page receives and test the optimal number of combinations for the right amount of time to get the required results. Target's [ Traffic Estimator ](t_traffic_estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) can help you design a test that works with your traffic. Before you use the Traffic Estimator, you should have good statistics showing the number of impressions and conversions your site normally receives. Consider your traffic levels per day. The more experiences in an activity, the more traffic the activity will need to include or the longer your activity will need to run. If your traffic isn't very high, you should test a small number of combinations; otherwise, the amount of time required to produce meaningful test results might be too long to be useful. 

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





For more considerations and best practices, see [ Multivariate Test Best Practices ](r_best_practices.md#reference_53635817FFB741EF8C4E56CC70688EDD). 
