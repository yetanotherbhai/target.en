---
description: Auto-Target uses advanced machine learning to identify multiple high-performing marketer-defined experiences, and serves the most tailored experience to each visitor based on their individual customer profile and the behavior of previous visitors with similar profiles, in order to personalize content and drive conversions.
keywords: auto-target;targeting;traffic allocation
seo-description: Auto-Target uses advanced machine learning to identify multiple high-performing marketer-defined experiences, and serves the most tailored experience to each visitor based on their individual customer profile and the behavior of previous visitors with similar profiles, in order to personalize content and drive conversions.
seo-title: Auto-Target For Personalized Experiences
solution: Target
title: Auto-Target For Personalized Experiences
title_outputclass: premium
topic: Standard
uuid: 1a82655e-6dd2-4d9d-a7b2-4f5652d288ba
badge: asstes/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Auto-Target For Personalized Experiences


>[!NOTE]
>
>Auto-Target is available as part of the [!DNL  Target Premium] solution. This feature is not available in [!DNL  Target Standard] without a [!DNL  Target Premium] license. 



While [ creating an A/B activity using the three-step guided workflow](t_test_ab.md#task_68C8079BF9FF4625A3BD6680D554BB72), you can choose to allocate traffic using the [!UICONTROL  Auto-Target For Personalized Experiences] option: 

![](graphics/auto-target-ui.png) 

This video explains how to set up an Auto-Target A/B activity: 



<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Understanding Auto-Target Activities </th> 
   <th colname="col3" class="entry"> 22:07 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/9ki7XJfzcD4/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/9ki7XJfzcD4/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p>After completing this training, you should be able to: </p> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F"> <p>Define Auto-Target testing </p> </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F"> <p>Compare and contrast Auto-Target to Automated Personalization </p> </li> 
      <li id="li_6C4D1871E45D40118D7D9D4DF81547B5"> <p>Create Auto-Target activities </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Overview {#section_972257739A2648AFA7E7556B693079C9}

The [!UICONTROL  Auto-Target For Personalized Experiences] option lets you harness machine-learning to personalize an arbitrary set of marketer-defined experiences. 

Auto-Target is primarily designed to deliver maximum optimization and personalization. Mathematically, personalization is defined as the additional lift over a static best experience (i.e. winner of an A/B activity). Unlike an A/B activity in which the objective is to find a single winner, Auto-Target automatically determines the best experiences for a given visitor (based on his or her profile) to deliver a highly personalized experience. More colloquially, Auto-Target identifies multiple winners and does the necessary modeling and audience segmentation automatically. 

Unlike an A/B activity in which the experience allocation for a given visitor is sticky, Auto-Target optimizes the specified business goal over each session. Like in Auto Personalization, Auto-Target reserves 10% (by default) of the traffic as a control group to measure lift versus the machine-learning algorithm. Visitors in the control group are served a random experience in the activity. This 10% control group can be adjusted. 

To adjust the Control percentage, click the - or + symbols. You cannot decrease the control group to less than 10%. 

![](../rn/graphics/auto-target-control-bigl.png) 

## When should you choose Auto-Target over Automated Personalization? {#section_BBC4871C87944DD7A8B925811A30C633}

Auto-Target is best when you want to define the entire experience rather than individual offers that will be automatically combined to form an experience. Also, Auto-Target uses the familiar A/B testing workflow with features that are not supported by AP including: the custom code editor, experience audiences, and more. 

## What does Auto-Target Have in Common with Automated Personalization? {#section_2A601F482F9A44E38D4B694668711319}

**The algorithm optimizes for a favorable outcome for each visit.** 


* The algorithm predicts a visitor's propensity for conversion (or estimated revenue from conversion) in order to serve the best experience. 

* A visitor is eligible for a new experience upon the end of an existing session. 

* Within a session, the prediction doesn’t change, to maintain visual consistency. 



**The algorithm adapts to changes in visitor behavior.** 


* The multi-arm bandit ensures that Target spends a small fraction of traffic to prevent over-exploitation of learning and to keep learning new trends. 

* The underlying models are rebuilt every 24 hours using the latest visitor behavior data to ensure Target is always abreast with changing visitor preferences. 

* If the algorithm can't determine winning experiences for individuals, it automatically switches to showing the overall best-performing experience while still continuing to look for personalized winners. The best-performing experience is found using [ Thompson sampling](https://en.wikipedia.org/wiki/Thompson_sampling). 



**The algorithm continually optimizes for a single goal metric.** 


* This metric could be conversion-based or revenue-based (more specifically Revenue per Visit). 



**The algorithm does not support using [!DNL  Analytics] as a data-source or a reporting endpoint.** 

**The algorithm automatically collects numerous parameters to build the models.** 


* For more information about the parameters used in Auto-Target and Automated Personalization, see [ Automated Personalization Data Collection](t_automated_personalization.md#reference_255BD3DE7AD04DC9B766E0BC78961058). 

  This list can be further augmented as desired by the marketer 



**The platform automatically uses all Experience Cloud shared audiences for model-building purposes.** 


* The marketer doesn’t have to do anything specific to add audiences to the model. 



**The algorithm maximizes utilization of learning traffic.** 


* All forms of machine-learning models require learning traffic before they can serve personalized content, and often times when launching a brand-new campaign, this is referred to as the “cold-start." 

* The algorithm will spend more traffic learning initially in an effort to learn as fast as possible and eventually throttle that traffic as the models get up and running. In AP, the marketer can select the percentage of visitors throttled to in the control, while in AT, this percentage is set at 10% by default, but you can adjust the percentage as desired. 



## How Does Auto-Target differ from Automated Personalization? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**Auto-Target requires less traffic than Automated Personalization for a personalized model to build.** 

For Auto Target, these simple rules can be used: per experience, 1000 visits and at least 50 conversions per day

**Auto-Target has full-fledged setup functionality.** 


* Because Auto-Target is embedded in the A/B activity workflow, Auto-Target benefits from the more mature and full-fledged Visual Experience Composer (VEC). 



**Auto-Target provides an extensive online testing framework.** 


* The multi-arm bandit is part of a larger online-testing framework that allows our data-scientists and researchers to understand the benefits of their continual improvements in real-world conditions. 

* In the future, this test bed will allow us to open up our decisioning system to our data-savvy clients so that they can bring in their own models to augment Target's models. 



**Is there an insight report for Auto-Target like in Automated Personalization?** 

No, there is not. 

## Reporting and Auto-Target {#section_42EE7F5E65E84F89A872FE9921917F76}

The following illustration shows what a typical report looks like when using auto-target: 

![](graphics/autotarget.png) 

Consider the following information as you interpret reports: 


* The various rows in the table help understand activity performance. Is Auto-Target outperforming the control experience and thus delivering value? 

* The green check icon next to the activity name in the report indicates that a personalized machine-learning model has been generated for that experience. The clock icon indicates that not enough traffic has been served to build the model. 

* The Total row tells you if the overall machine-learning results are better than the results you would have obtained by simply serving the experiences randomly. 

* Visitors in the control algorithm are allocated to different experiences in the same way as they are for an A/B test. Therefore, the results from the control group between different experiences can be interpreted as an ordinary (e.g. non-personalized) A/B test between the experiences. This can tell you which experiences are best overall. If the difference between the experience responses for the control group visitors is statistically insignificant, this suggests the offers may not be sufficiently differentiated or that the location of the test does not make a big enough difference to the optimization goal. If this happens try changing your test location and/or offers. 



## Caveats {#section_F3197BACA1984575B4ADF08E7E9C595E}

The following caveats are working as designed and will continue to function as described after the feature is released to the public: 


* You cannot switch from Auto-Target enabled activities to Automated Personalization, and vice-versa. 

* You cannot switch from Manual traffic allocation (traditional A/B Test) to Auto-Target, and vice-versa. 

* When using hosts and environments (host groups), models are built for the “Production” environment only. All environments contribute data to build models for “Production” campaigns. 

* You must use a minimum of two experiences. 


