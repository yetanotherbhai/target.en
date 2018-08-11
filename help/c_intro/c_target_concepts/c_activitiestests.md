---
description: An activity determines the experiences a site visitor might encounter.
keywords: Overview and Reference
seo-description: An activity determines the experiences a site visitor might encounter.
seo-title: Activities and Tests
solution: Target
subtopic: Getting Started
title: Activities and Tests
topic: Standard
uuid: 74b5480c-2756-493d-9433-efb347234a43
index: y
internal: n
snippet: y
translate: y
---

# Activities and Tests

[!DNL  Target] lets you test different experiences to determine which will be most successful. An activity compares two or more [ experiences](../../c_intro/c_target_concepts/c_experience.md#concept_B91F0F36E9F24AA58A3C6BC0A02871E8) against the success metrics you specify so you can choose the experience that is most likely to provide the results you want. 

For example, you might design an activity that tests two different landing pages, one that highlights information about women's summer shoes, and one that highlights more general summer apparel. The activity determines the conditions that control when each of these landing pages appears, and the metrics that determine which page is more successful. The activity is configured to start and end when specific conditions are met, such as between specific dates, or to start when the activity is approved and to end when it is deactivated. 

When designing an activity, you should plan carefully. Determine when the activity will start and how long it will last. Then, list your offers and assign a target audience to each one. 

This video explains the activity types available in [!DNL  Target Standard/Premium]. 



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
      <li id="li_916224D2105348BE93D60015B2F43D4F">Describe the types of activities included in <span class="keyword"> Adobe Target </span> </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Select the appropriate activity type to achieve your goals </li> 
      <li id="li_6C4D1871E45D40118D7D9D4DF81547B5">Describe the three-step guided workflow that applies to all activity types </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

There are several types of activities: 



<table id="table_B1D68605447642F29CC02157582B921B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Activity Type </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p class="- topic/p "> <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_test_ab.html" format="https" scope="external"> A/B test</a> </p> </td> 
   <td colname="col2"> <p class="- topic/p ">A/B Testing compares two or more versions of your Web site content to see which version best improves your conversions during a pre-specified test period. </p> <p>The following are two types of A/B tests you can use: </p> 
    <ul id="ul_1A94061695D74ABEADE7C579B1349F09"> 
     <li id="li_97B7AB009C86403AA6ABEECE03B15659"> <p><a href="../../c_activities/automated_traffic_allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Auto-Allocate</a> </p> <p>Auto Allocate identifies a winner among two or more experiences and automatically reallocates more traffic to the winner to increase conversions while the test continues to run and learn. </p> </li> 
     <li id="li_69D72AECB5524DC0B2C80AE332B5A178"> <p><a href="../../c_activities/c_auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Target For Personalized Experiences</a> </p> <p>Auto Target uses advanced machine learning to identify multiple high performing marketer-defined experiences, and serves the most tailored experience to each visitor based on their individual customer profile and the behavior of previous visitors with similar profiles, in order to personalize content and drive conversions. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_create_a4t.html" format="https" scope="external"> A/B test with Analytics data</a> </p> </td> 
   <td colname="col2"> <p>You can configure an activity to use <span class="keyword"> Adobe Analytics</span> as the reporting source. This activity type requires that you link your <span class="keyword"> Adobe Experience Cloud</span> account with both <span class="keyword"> Analytics</span> and <span class="keyword"> Target</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="- topic/p "> <a href="https://marketing.adobe.com/resources/help/en_US/target/mvt/" format="https" scope="external"> Multivariate test </a> </p> </td> 
   <td colname="col2"> <p class="- topic/p ">Multivariate Testing (MVT) compares combinations of offers in elements on a page to determine which combination performs the best for a specific audience, and identifies which element most impacts the activity's success. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="- topic/p "> <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_experience_target.html" format="https" scope="external"> Experience targeting </a> </p> </td> 
   <td colname="col2"> <p class="- topic/p ">Experience Targeting (XT) delivers content to a specific audience based on a set of marketer-defined rules and criteria. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/target/target/t_automated_personalization.html" format="https" scope="external"> Automated personalization </a> </p> </td> 
   <td colname="col2"> <p>Automated Personalization (AP) combines offers or messages, and uses advanced machine learning to match different variations to each visitor based on their individual customer profile, in order to personalize content and drive conversions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/rec/" format="https" scope="external"> Recommendations </a> </p> </td> 
   <td colname="col2"> <p>A recommendation determines how a product is suggested to a website user, depending on that user's activities on the site. </p> <p>For example, you might want to encourage people who purchase a backpack to consider buying hiking shoes and trekking poles. You could create a recommendation that shows items that are often purchased together, using the "People who bought this also bought that" algorithm. Or, you might want to encourage visitors to spend more time on your media site by recommending similar video to the one they are watching, using the "People who viewed this viewed that" algorithm. </p> </td> 
  </tr> 
 </tbody> 
</table>

