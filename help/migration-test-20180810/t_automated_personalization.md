---
description: Automated Personalization (AP) combines offers or messages, and uses advanced machine learning to match different offer variations to each visitor based on their individual customer profile, in order to personalize content and drive lift.
keywords: experience preview;experience urls;generate urls;view experience urls
seo-description: Automated Personalization (AP) combines offers or messages, and uses advanced machine learning to match different offer variations to each visitor based on their individual customer profile, in order to personalize content and drive lift.
seo-title: Automated Personalization
solution: Target
title: Automated Personalization
title_outputclass: premium
topic: Standard
uuid: e5aa6f34-0db6-4fe6-8604-df9f68db23ab
badge: asstes/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Automated Personalization

## Automated Personalization {#task_8AAF837796D74CF893CA2F88BA1491C9}Automated Personalization (AP) combines offers or messages, and uses advanced machine learning to match different offer variations to each visitor based on their individual customer profile, in order to personalize content and drive lift.Similarly to Auto-Target, Automated Personalization uses a Random Forest algorithm, a leading data science ensemble method, as its main personalization algorithm to determine the best experience to show a visitor. Automated Personalization can be valuable in the discovery phase of testing. It is also useful to allow machine learning to determine the most effective content when targeting diverse visitors. Over time, the algorithm learns to predict the most effective content and displays the content most likely to achieve your goals. 

To find more information about how Automated Personalization differs from Auto Target, see [ Auto-Target For Personalized Experiences ](c_auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3). 


>[!NOTE]
>
>Automated Personalization is available as part of the Target Premium solution. It is not included with Target Standard without a Target Premium license. If you have a Target Premium license, the Target Premium card replaces the Target Standard card in the Adobe Marketing Cloud.



This video explains the activity types available in Target Standard/Premium. Automated Personalization is discussed beginning at 5:55. 



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
      <li id="li_916224D2105348BE93D60015B2F43D4F">Describe the types of activities included in Adobe Target </li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Select the appropriate activity type to achieve your goals </li> 
      <li id="li_6C4D1871E45D40118D7D9D4DF81547B5">Describe the three-step guided workflow that applies to all activity types </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Marketers implement one file on their site which enables them to point and click on any content and then visually create and select additional content options for that area using the VEC (Visual Experience Composer). Then, the algorithm automatically determines which piece of content to deliver to each individual visitor based on all the behavioral data that the system has about that visitor, providing a personalized experience. Because Automated Personalization can adapt to changes in visitor behavior, it can be run without a set end date to provide ongoing lift and personalization. This is sometimes referred to as “always-on” mode. The marketer does not need to run a test, analyze the results, then deliver a winner before realizing the lift found from optimization—a standard order of operations to implement the outcome of a standard A/B activity. 

The following terms are useful when discussing Automated Personalization: 



|  Term  | Definition  |
|---|---|
|  Multi-armed bandit  | A multi-armed bandit approach to optimization balances exploratory learning and exploitation of that learning.  |
|  Random Forest  | Random Forest is a leading machine learning approach. In data-science speak, it is an ensemble classification or regression method that works by constructing a large number of decision trees based on visitor and visit attributes. Within Target, Random Forest is used to determine which experience is expected to have the highest likelihood of conversion (or highest revenue per visit) for each specific visitor. For more information about Random Forest in Target, see [ Random Forest Algorithm ](t_automated_personalization.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).  |
|  Thompson Sampling  | The goal of Thompson Sampling is to determine which experience is the best overall (non-personalized), while minimizing the “cost” of finding that experience. Thompson sampling always picks a winner, even if there is no statistical difference between two experiences. For more information, see [ Thompson Sampling ](https://en.wikipedia.org/wiki/Thompson_sampling).  |

Consider the following details when using Automated Personalization: 

**Automated Personalization uses a Random Forest algorithm to personalize.** 

Random Forest is a leading machine learning approach. In data-science speak, it is an ensemble classification or regression method that works by constructing a large number of decision trees based on visitor and visit attributes. Within Target, Random Forest is used to determine which experience is expected to have the highest likelihood of conversion (or highest revenue per visit) for each specific visitor. For example, visitors who use Chrome, are gold loyalty members, and access your site on Tuesdays might be more likely to convert with Experience A, while visitors from New York might be more likely to convert with Experience B. For more information about Random Forest in Target, see [ Random Forest Algorithm ](t_automated_personalization.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA). 

**The personalization model optimizes for each visit.** 


* The algorithm predicts a visitor's likelihood of conversion (or estimated revenue from conversion) in order to serve the best experience. 

* A visitor is eligible for a new experience upon the end of an existing session (unless he or she is in the control group, in which case the experience that visitor sees on the first visit is the same experience he or she will see in subsequent visits). 

* Within a session, the experience presented does not change to maintain visual consistency. 



**The personalization model adapts to changes in visitor behavior.** 


* The multi-arm bandit ensures that the model is always “spending” a small fraction of traffic to continue learning throughout the life of the activity, and to prevent over-exploitation of previously learned trends. 

* The underlying models are re-built every 12 hours using the latest visitor behavior data to ensure Target is always leveraging changing visitor preferences. 

* If the algorithm can't determine winning experiences for individual visitors, it automatically switches to showing the overall best-performing experience, while still continuing to look for personalized winners. The best-performing experience is found using [ Thompson Sampling ](https://en.wikipedia.org/wiki/Thompson_sampling). 



**The model continually optimizes a single goal metric.** 


* This metric could be conversion-based or revenue-based (more specifically, Revenue per Visitor). 



**Target automatically collects information about visitors to build the personalization models.** 


* For more information about the attributes used in Auto-Target and Automated Personalization, see [ Automated Personalization Data Collection ](t_automated_personalization.md#reference_255BD3DE7AD04DC9B766E0BC78961058).


**Target automatically uses all Experience Cloud shared audiences to build the personalization models.** 
* You don’t have to do anything specific to add audiences to the model. For information about using Marketing Cloud Audiences with Target, see [ Audiences ](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html) in the *Experience Cloud and Core Services* Help. 



**Marketers can upload offline data, propensity scores or other custom data to build personalization models.** 

Offline data, such as CRM information or customer churn propensity scores, can be incredibly valuable when building personalization models. There are several ways to input data in Automated Personalization (AP) and Auto-Target personalization algorithms. 


* Experience Cloud shared audiences (AAM, Analytics) 

* [ mbox parameters ](c_methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) 

* [ Profile parameters ](c_methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) 

* [ Server-side APIs for profile update ](c_methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) 



For information about the data automatically collected and used by Automated Personalization and Auto-Target personalization algorithms, see [ Automated Personalization Data Collection ](t_automated_personalization.md#reference_255BD3DE7AD04DC9B766E0BC78961058). 
>## Random Forest Algorithm {#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA}Target's main personalization algorithm used in both Automated Personalization and Auto-Target is Random Forest. Ensemble methods like Random Forest use multiple learning algorithms to obtain better predictive performance than could be obtained from any of the constituent learning algorithms. The Random Forest algorithm in Automated Personalization is a classification or regression method that operates by constructing a multitude of decision trees when it is being trained.When you think of statistics, a single regression model used to predict an outcome might come to mind. The latest data science research suggests that "ensemble methods," where multiple models are created from the same data set and then intelligently combined, produce better results than would predicting based on a single model alone. 

The Random Forest algorithm is the key underlying personalization algorithm used in Automated Personalization and Auto-Target activities. Random Forest combines hundreds of decisions trees together in order to arrive at a better prediction than a single tree could make by itself. 

## What is a Decision Tree? {#section_7F5865D8064447F4856FED426243FDAC}

The goal of a decision tree is to break down all available visit data a system can learn from and then group that data, where visits within each group are as similar as possible to each other with regard to the goal metric. Across groups, however, the visits are as different as possible, with respect to the goal metric (e.g. conversion rate). The decision tree looks at the different variables it has in the training set to determine how to split the data in a MECE (Mutually-Exclusive-Collectively-Exhaustive) way into these groups (or "leaves") to maximize this goal. 

In a simple example, let's assume we only have two input variables: 


* Gender (with two potential values, Male or Female) 

* Zip Code (with five potential values in our small data set: 11111, 22222, 33333, 44444, or 55555) 



If our goal metric is conversion, then the tree would first determine which of our two variables explains the largest amount of variation in the visit data's conversion rate. 

Let's say zip code is most predictive. This variable would then form the first "branch" of the tree. The decision tree would then determine how to split the visit data, such as the conversion rate of the records within each split was as similar as possible, and the conversion rate between the splits was as different as possible. In our example, we'll assume 11111, 22222, 33333 are one split and 44444 and 55555 are a second split. 

This action would result in the first layer of our decision tree: 

![](graphics/decsion tree 1.png) 

The decision tree would ask the question, "What is the most predictive variable?" In our example, we only have two variables, so the answer here is clearly gender. The tree now will look to complete a similar exercise to split the data *within each branch*. First, let's consider the 11111, 22222, and 33333 branch. In these zip codes, if there is a difference in conversion between men and women, then there would be two leaves (men and women), and this branch would be complete. In the other branch, 44444 and 55555, let's assume there is no statistical difference between how women and men convert. In this case, the first branch becomes the final split. 

Our example would result in the below tree: 

![](graphics/decsion tree 2.png) 

## How are Decision Trees used by Random Forest? {#section_536C105EF9F540C096D60450CAC6F627}

Decision trees can be a powerful statistical tool. However, they have some disadvantages. Most critically, they can "over-fit" the data so that an individual tree poorly predicts future data that wasn't used to build the initial tree. This challenge is known as the[ bias-variance tradeoff ](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) in statistical learning. Random forests help overcome this overfitting challenge. At the highest level, a random forest is a collection of decision trees that are built slightly differently on the same data set that "vote" together to yield a better model than an individual tree. The trees are built by randomly selecting a sub-set of visits records with replacement (known as bagging), as well as randomly selecting a sub-set of the attributes, so that the forest consists of slightly different decision trees. This method introduces small variations into the trees that are created in the Random Forest. Adding in this controlled amount of variance helps improve the predictive accuracy of the algorithm. 
## How do Target's Personalization Algorithms use Random Forest? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

** How Models are Built** 

The following diagram summarizes how models are built for Auto-Target or Automated Personalization activities: 

![](graphics/random forest flow.png) 


1. Target collects data on visitors while randomly serving experiences / offers 

1. After Target hits a critical mass of data, it performs feature engineering 

1. Target builds Random Forest models for each experience / offer 

1. Target checks if the model meets a threshold quality score 

1. Target pushes the model to production to personalize future traffic 



Target uses data it collects automatically, as well as custom data provided by you, to build its personalization algorithms. These models predict the best experience or offer to show to visitors. Generally, one model is built per experience (if an Auto-Target activity) or per offer (if an Automated Personalization activity). Target then chooses to display the experience or offer that yields the highest predicted success metric (e.g. conversion rate). These models must be trained on randomly served visits before they can be used for prediction. As a result, when an activity first starts, even those visitors who are in the personalized group are randomly shown different experiences or offers until the personalization algorithms are ready. 

Each model must be validated to ensure it is good at predicting the behavior of visitors before it is used in your activity. Models are validated based on their AUC (area under the curve). Because of the need for validation, the exact time when a model will start serving personalized experiences is dependent on the details of the data. In practice, and for traffic planning purposes, it usually takes more than the minimum number of conversions before each model is valid. 

When a model becomes valid for an experience or offer, the clock icon to the left of experience/offer name changes to a green checkbox. When there are valid models for at least two experiences/offers, some visits start to become personalized. 

** Feature Transformation ** 

Before the data goes through the personalization algorithm, it undergoes a feature transformation, which can be thought of as prepping the data collected in the training records for use by the personalization models. 

The feature transformations depend on the type of attribute. Mainly, there are two types of attributes (or "features" as they are sometimes described by data scientists): 


* ** Categorical: **Categorical features cannot be counted but can be sorted into different groups. They could be features like country, gender, or zip code. 

* ** Numeric: ** Numeric features can be measured or counted, such as age, income, and so on. 



For categorical features, a set of all possible features is maintained and the likelihood transformation is used to reduce the data size. For numeric features, re-scaling ensures that the features are comparable across the board. 

** Balancing Learning vs. Personalizing with the Multi-Armed Bandit** 

After Target has personalization models built to personalize your traffic, there is a clear tradeoff you face for future visitors to your activity: should you personalize all the traffic based on the current model or should you continue to learn from new visitors by randomly serving them random offers? You want to make sure the personalization algorithm is always learning about new trends in your visitors, while personalizing most of the traffic. 

The multi-arm bandit is how Target helps you meet this goal. The multi-arm bandit ensures the model is always "spending" a small fraction traffic to continue to learn throughout the life of the activity learning and to prevent over-exploitation of previously learned trends. 

In the data-science world, the multi-armed bandit (MAB) problem is a classic example of the exploration vs. exploitation dilemma in which a collection of one-armed bandits, each with unknown reward probability, is given. The key idea is to develop a strategy, which results in the arm with the highest success probability to be played so the total reward obtained is maximized. Multi-armed bandit is used in the system when for online scoring after the online models are built. This helps with online learning during exploration. The current multi-armed algorithm is epsilon (ε) greedy algorithm. In this algorithm, with probability 1- ε, the best arm is chosen. And, with probability ε, any other arm is randomly chosen. 
>## Creating an Automated Personalization Activity {#task_12B93AC558FF4AAA8A0D9A7362FC96A6}The Automated Personalization activity workflow varies from the workflow of the other activity types. 
<draft-comment otherprops="merge">
  target/t_create_ap_activity.xml 
</draft-comment>
>1. From the Target Standard Activities list, click ** [!UICONTROL  Create Activity] ** > ** [!UICONTROL  Automated Personalization] **.

>       ![](../graphics/ap_create.png) 

>       If you prefer to use the Form-Based Experience Composer, select that option. See [ Form-Based Experience Composer ](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html). 
>1. Verify or enter the activity URL, then click ** [!UICONTROL  Next] **.


>       >[!NOTE]
>       >
>       >[!DNL  Target] does not differentiate between URL protocols ( [!DNL  https] and [!DNL  http]). As a result, [!DNL  https://adobe.com] and [!DNL  http://adobe.com] both match. 


>       The page with the specified URL opens in the Visual Experience Composer. 

>       ![](../graphics/ap_url.png) 

>       For troubleshooting information about the VEC, should you have problems, see [ Troubleshooting the Visual Experience Composer ](vec-best-pracitces-and-troubleshooting.md#reference_77743144F10143A3A89D56E116D296E4). 
>1. To name the activity, click the Name field and type your activity name.

>       ![](../graphics/ab_newname.png) 

>       The following characters are not allowed in an activity name: 

>       |  Character  | Description  |
>       |---|---|
>       |  /  | Forward slash  |
>       |  ?  | Question mark  |
>       |  #  | Number sign  |
>       |  :  | Colon  |

>1. Modify page elements as explained in [ Experiences ](c_experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), then click ** [!UICONTROL  Next] **.

>       You can select multiple images at once from the asset manager. This enables you to quickly view the page with each of the images configured for the activity. You can also easily edit text elements in your offers. When you edit an element, bars appear on that element to indicate you have changed it. 


>1. Click ** [!UICONTROL  Content] ** to configure the available combinations.

>       ![](../graphics/ap_content.png) 


>       >[!NOTE]
>       >
>       >You can create up to 30,000 experiences in an AP test.


>       The Content list shows each piece of content selected for the activity, and the location it is assigned to. You can select pieces of content and assign them to reporting groups. 

>       For information about targeting an offer to specific audiences, see [ Target AP Offers ](t_automated_personalization.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E). 
>1. Click ** [!UICONTROL  Combinations] ** in the Content list to choose any combinations of elements that you want to exclude from the activity.

>       ![](../graphics/ap_combos.png) 


>       >[!NOTE]
>       >
>       >You can include up to 30,000 combinations.


>       Click ** [!UICONTROL  Filter] ** to create a filter that shows only the combinations you want to see. 

>       Click ** [!UICONTROL  Exclude] ** to hide a combination. Excluded combinations are never displayed. Click ** [!UICONTROL  Include] ** to include a previously excluded combination. 

>       Use the Display drop-down to filter the list of combinations to show all combinations, included combinations only, or excluded combinations only. 

>       ![](../graphics/ap_display.png) 
>1. Click ** [!UICONTROL  Continue] ** when you have finished setting up the content of your activity.

>       The Activity Summary appears. 

>       Click ** [!UICONTROL  View Experience URLs] ** to preview how your experiences will look when delivered. A pop-up appears that you can use to view and share links to your AP experiences on your site to get a "true preview" of the experiences outside of Target's Visual Experience Composer. You must share the links from the message to share the preview. Clicking a link and then copying the URL directly from the page won't work because the URL contains a parameter that only displays the page correctly when you access the page from the link in the message. 
>1. Select an audience and specify the percentage of visitors who will see the control experience, then click ** [!UICONTROL  Next] **.

>       The control experience provides a comparison to determine how much lift is provided by the automated test. 

>       Automated Personalization always measures performance against a control group. Best practice is to place 5-10% of entrants into the control group, and display the default content to them. 


>       >[!NOTE]
>       >
>       >In Automated Personalization activities, entry criteria (URL targeting, template rules, audience target) are evaluated for each request. In previous versions, entry criteria were evaluated once per session.

>1. Configure the control experience.

>       You can choose from the following control experiences: 
>    
>    * Default Experience The default page design is used as the default experience. 

>    * Randomized Experience (default) The modeling system randomly creates an experience from the offers and locations used for that page. The visitor continues to see that experience until the session expires. If the visitor returns and begins a new session, a new random experience is generated. 

>    * Selected Experience You select the experience by choosing the content that displays in each location. 

>      If, after creating the activity, you delete a location from the control, your activity will reset. Because the control is different, the activity must reset to provide accurate data using the new control. 

>1. Review the Experiences card.

>       The Experiences card lists each location in the experience and shows the numbers of offers available for each location. 
>1. Click ** [!UICONTROL  Continue] **.

>       The Goal &amp;amp; Settings page opens. 
>1. Configure the activity with the following settings, then click ** [!UICONTROL  Create] **.


>    <table id="table_136C5D05E9A544C6977050EC50B9F49B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Name </td> 
   <td colname="col2"> <p>Name the activity. Give the activity a name that is descriptive enough that team members can recognize it in the Activities list. </p> <p>The following characters are not allowed in an activity name: </p> <p> 
     <ul id="ul_5710602E3CF24EAD9C2C6BF10B83841F"> 
      <li id="li_1E06CC79069F4A3C825FAEB5C32F6C9F"> / </li> 
      <li id="li_0C716E01A8C74BE7BF540D21A249E692">? </li> 
      <li id="li_924D064F365C45B8B0F8AC15A23ABE3D"># </li> 
      <li id="li_E9F2F644FC5C4E9B91101745590DD6D8">: </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Objective </td> 
   <td colname="col2"> (Optional) Type the objective of the test. The objective helps you remember the purpose of the activity. </td> 
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
   <td colname="col2"> Set the start and end dates for the activity. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Optimization Goal </td> 
   <td colname="col2"> <p>Provide a name for the goal, then specify the optimization goal, which consists of two parameters: </p> <p> 
     <ul id="ul_F6238CFA3890414DAADB6896E17653B8"> 
      <li id="li_5366B2CCA42041F38C2B3888BEE3F7E8">What you want to measure with the activity </li> 
      <li id="li_A77B6CFF0A7E46EB9675CA5B4D22CAF3">The action taken by an activity entrant that shows that the goal has been achieved. </li> 
     </ul> </p> <p>Automated Personalization activities can measure conversion, RPV, and AOV. Conversion can be achieved by viewing a page or viewing an mbox. Clicks can also be tracked. </p> <p>The primary goal also becomes the modeling metric, used by the modeling system to calculate the success of te experience. </p> <p>Visitors can be kept in the activity for tracking purposes after reaching the modeling goal. For example, often an Automated Personalization activity is used to improve click-rates, and that is set as the modeling goal. However, it's important to see how increased click-rates lead to final conversion, so tracking through the final conversion is essential. </p> <p>You can provided dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increase. </p> <p>You must define both (or multiple) success metrics before you can make one dependent on another. </p> <p>The <span class="wintitle"> Add Dependency </span> option allows the success metric to increment if another success metric has been reached or has not been reached. </p> <p>To add a dependency: </p> <p> 
     <ol id="ol_7CE86C31CD5541039A3265E14D0C3630"> 
      <li id="li_3E374D8B28B443FA9FE8AF2B02814A82"> <p>After adding additional metrics, click <span class="uicontrol"> Advanced Settings </span>. </p> </li> 
      <li id="li_F65C369C8F354A6CBD447ED26D9F79E4"> <p>Click the <span class="uicontrol"> Add Dependency </span> option: </p> <p style="text-align: center;"> <img href="../graphics/add dependency.png" id="image_D3C6E4862509435E86A1F61B88F342CA" /> </p> </li> 
      <li id="li_9A6F187B4C294A9C8B5C834C76B32767"> <p>Drag and drop the desired metrics from the left pane into the right pane, then click <span class="uicontrol"> Reached </span> to toggle the setting between <span class="uicontrol"> Reached </span> and <span class="uicontrol"> Not Reached </span>. </p> <p style="text-align: center;"> <img href="../graphics/add dependency reached.png" id="image_CA136FD10D754BD1B26C621DF2A4858D" /> </p> </li> 
     </ol> </p> <p>You can edit or remove dependencies after adding them. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Conversion Metric </td> 
   <td colname="col2"> <p>Set the conversion metric. </p> <p>You can: </p> <p> 
     <ul id="ul_09EA8187A57D4924BA0069CE4157A4FA"> 
      <li id="li_4AD5D0C60BF348D2B9B8C1CD0CB9771F">Name the conversion metric. </li> 
      <li id="li_D1B104D6B3354CDE84D8DF8F964EC4A7">Set the conversion metric to be the same as the optimization goal. </li> 
      <li id="li_AB85CE2490EF4A6F901C38671FB8CA75">If not the same as the optimization goal, select a different method. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Additional Metrics </td> 
   <td colname="col2"> <p>Add any additional reporting metrics you want to use. You can add conversion or revenue metrics. </p> <p> <p>Note:  The Engagement metric is not supported as an additional metric as well. The UI might let you select the Engagement metric, but data will not display accurately in reports. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Audiences for Reporting </td> 
   <td colname="col2"> <p>Add audiences to enable filtering by audiences in reports. By default, the report shows results for all qualified visitors. Add audiences to filter results for more specific subsets of visitors. </p> <p> <p>Note:  Unlike other activity types, Automated Personalization cannot use Adobe Analytics as its reporting source. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Notes </td> 
   <td colname="col2"> Type any information about your activity that is useful to keep on hand for yourself or other team members. The Notes pane is resizable. </td> 
  </tr> 
 </tbody> 
</table>

>## Automated Personalization Data Collection {#reference_255BD3DE7AD04DC9B766E0BC78961058}Automated Personalization collects a variety of data. 
<draft-comment otherprops="merge">
  target/r_ap_data.xml 
</draft-comment>
>The following table shows the data collected by Automated Personalization by default, without the marketer having to do anything. You can augment the input data set at any time. 



><table id="table_F46105983FD14051BBE9C429EE9B2ACB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Data Type </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Shared Audiences </td> 
   <td colname="col2"> <p>Created through: </p> <p> 
     <ul id="ul_FFC96DB0C89A4563B83B8BFACA57A766"> 
      <li id="li_1A6F8C26F6EB48DAA6FAD9ED106A671E">Adobe Audience Manager </li> 
      <li id="li_B31BAFFAB5BA4B4F9C05BF6F5467802B">Adobe Target Classic </li> 
      <li id="li_1009D43E727246ABA61CF66A80C744EF">Adobe Analytics </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URL Parameters </td> 
   <td colname="col2"> Anything present in the URLs </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Interest Areas </td> 
   <td colname="col2"> <p>Automated Personalization uses crawler technology that develops key tokens characterizing content within each page URL. The technique used is generally known as term-frequency/inverse-document-frequency or TF/IDF. These tokens are then stored in each user profile as the user crawls through different pages. These tokens are recency ranked. For example: </p> <p> 
     <table id="table_366C8BDF8D294BC0B24B579D96A35B2E">  
     </table> </p> <p>If a visitor views url1 and then url4, then the user profile, that visitor will have following ordered interest areas: </p> <p> 
     <ol id="ol_DB8451DEA9314251B827AF91ACB81573"> 
      <li id="li_D77E3351C9944F9E83A9A15C90D31C2E">black </li> 
      <li id="li_B279553BDB054642B3F8EE18362B79A1">coat </li> 
      <li id="li_538103CC3C8246B59DCC142BFFF5D55F">rain </li> 
      <li id="li_8026751986194534BEAD0D3030B27202">shoe </li> 
      <li id="li_3F586ACBC2F344DAB41A86915B7EE43E">heel </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> User Profile Parameters </td> 
   <td colname="col2"> Information stored in the user profile </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mbox Parameters </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7F3F3C41B9D148748503FBC9B4FE203D"> 
      <li id="li_9EB369DDE3814B2BBBD24BB0ACEB1A57"> <span class="codeph"> BOX_mboxTime </span> </li> 
      <li id="li_E07C25901FAC4A6785CDACF48849009A"> <span class="codeph"> BOX_mboxXDomain </span> </li> 
      <li id="li_F6E4DA11D3C743B78FF99EB23E9494B9"> <span class="codeph"> BOX_mboxXDomainCheck </span> </li> 
      <li id="li_9567463BCF984AE9A44403D50F1EE7BC">Other information passed by mboxes </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Environment/Technographics </td> 
   <td colname="col2"> <p> 
     <ul id="ul_9C5FCB33757B49B7986C1C8FADCF479C"> 
      <li id="li_5CC0454891494C58BEDF152A3121E417"> <span class="codeph"> ENV_Browser </span> </li> 
      <li id="li_0BE7968D9E2D4C08839500B7373B14AA"> <span class="codeph"> ENV_BrowserHeight </span> </li> 
      <li id="li_6093F549D55D4540AE621ADD915A687F"> <span class="codeph"> ENV_BrowserTimezoneOffsetMinutes </span> </li> 
      <li id="li_2944DD932D95464988AEC74DD86A0F7B"> <span class="codeph"> ENV_BrowserVersion </span> </li> 
      <li id="li_96AADEAD6A494845B58E9E2EE595DCFD"> <span class="codeph"> ENV_BrowserWidth </span> </li> 
      <li id="li_38DE5712CE0447C982B4092B54E7F32C"> <span class="codeph"> ENV_ColorDepth </span> </li> 
      <li id="li_CDFDA212FEDD43C392E7D0D488EB2DF4"> <span class="codeph"> ENV_DayOfWeek </span> </li> 
      <li id="li_B13473B801BC4AC4B8B60CAAD52E6167"> <span class="codeph"> ENV_Language </span> </li> 
      <li id="li_C598D22AF2E947F7AB89F6862BA8BF4E"> <span class="codeph"> ENV_LocalTimePeriod </span> </li> 
      <li id="li_BD9850B487CD4C9E978E16D938F3385C"> <span class="codeph"> ENV_OperatingSystem </span> </li> 
      <li id="li_F6345E117AAE462A87F0C3ED2390F13B"> <span class="codeph"> ENV_OperatingSystemVersion </span> </li> 
      <li id="li_995338C827F34CB2B274C12B601CF386"> <span class="codeph"> ENV_PageId </span> </li> 
      <li id="li_71A320C5E84C4C7B96D425FEE6FD4B2B"> <span class="codeph"> ENV_Referrer </span> </li> 
      <li id="li_3B39DA2B08F14CAEA4F177CF022F3E5B"> <span class="codeph"> ENV_ScreenHeight </span> </li> 
      <li id="li_E8EAD35B4D65496A8A949EDA4AD09CE1"> <span class="codeph"> ENV_ScreenWidth </span> </li> 
      <li id="li_2587338069C2465E93D5AB3C22A7C9DD"> <span class="codeph"> ENV_ServerHour </span> </li> 
      <li id="li_8005A679EB43456BABE32B4D3AE8F644"> <span class="codeph"> ENV_UserHour </span> </li> 
      <li id="li_8F151294CD6C414A8EC5D5BFBF93429C"> <span class="codeph"> ENV_UserHourType </span> </li> 
      <li id="li_56B58005720C4A31876DB6C0D57D6F62"> <span class="codeph"> ENV_WeekHour </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geography </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_1A91E143076C4970A3BF0DF15649555D"> 
      <li id="li_63A72EC470594ED2905C5368D6598536"> <span class="codeph"> GEO_City </span> </li> 
      <li id="li_2369DE40B88D4032976D3E2D35CC49DD"> <span class="codeph"> GEO_Country </span> </li> 
      <li id="li_5A3ABFF39CED451D866654E46E46CAC2"> <span class="codeph"> GEO_DMA </span> </li> 
      <li id="li_0DFB24429C354A2A83D526F51C3F25DC"> <span class="codeph"> GEO_Latitude </span> </li> 
      <li id="li_BCA9361B01914CFE85EFF4E36F5AD431"> <span class="codeph"> GEO_Longitude </span> </li> 
      <li id="li_1849BB1B82F74D22807DB97BBAD9A937"> <span class="codeph"> GEO_Region </span> </li> 
      <li id="li_46B4BDEE6E9041EBB5FF24E08B9145E1"> <span class="codeph"> GEO_ZipCode </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Device </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6E22B6B5C0A84E7EBA1A5EF436FF62EC"> 
      <li id="li_677A553C77E747438B9792649024697E"> <span class="codeph"> MOB_targeting.mobile.model </span> </li> 
      <li id="li_2F49F9701DB34A69AFE4B70380818401"> <span class="codeph"> MOB_targeting.mobile.vendor </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>User Session </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_41AB5DEA936C43959AC1F1A6A179C3F5"> 
      <li id="li_F25F9BE374144A00B42632179FCDE1F8"> <span class="codeph"> SES_CUMULATIVE_ACTION_1_99858 </span> </li> 
      <li id="li_0862A3B8A48549AFBDB91159B427BCA1"> <span class="codeph"> SES_CUMULATIVE_ORDER_VALUE </span> </li> 
      <li id="li_1BA949A060E74E99B194EC4EA76BC29A"> <span class="codeph"> SES_CUMULATIVE_SUCCESSES </span> </li> 
      <li id="li_3A5CD3ED97344B29B8C7D33DC6CB089A"> <span class="codeph"> SES_HOURS_SINCE_LAST_VISIT </span> </li> 
      <li id="li_D511B116BBD645A8AAB8C77DE0BC2DB0"> <span class="codeph"> SES_LAST_SESSION_START </span> </li> 
      <li id="li_97F7C53DB8C04FC8B909FAFF03157726"> <span class="codeph"> SES_PREVIOUS_VISIT_COUNT </span> </li> 
      <li id="li_5D0FACA15D5D494BB0801EDC5F6DBFA7"> <span class="codeph"> SES_PROFILE_CREATION_TIME </span> </li> 
      <li id="li_0CB6245A3F7B468CB3A697D120C9EF90"> <span class="codeph"> SES_PROFILE_UPDATE_TIME </span> </li> 
      <li id="li_DAF9A2C361B343839BD8B9A4B20132A2"> <span class="codeph"> SES_RECENCY </span> </li> 
      <li id="li_15076BFF7FD54797AA86E77E8BD57388"> <span class="codeph"> SES_REQEUSTS_PER_SESSION </span> </li> 
      <li id="li_B6D00FFCDA7648FDA7194079EA044FDD"> <span class="codeph"> SES_SESSION_POSITION </span> </li> 
      <li id="li_6F3D04D1C99F47888000E7B3A7A6CE69"> <span class="codeph"> SES_SESSION_START </span> </li> 
      <li id="li_A6618515B46C47AC8CBB07DE72DE2CFB"> <span class="codeph"> SES_SESSION_TIME </span> </li> 
      <li id="li_C486DA86E8B64206B3EEE3E87C2C0ED1"> <span class="codeph"> SES_SUCCESS_RECENCY </span> </li> 
      <li id="li_714839EEC68D41D5A3A1DD43C51A513B"> <span class="codeph"> SES_TIME_PER_SESSION </span> </li> 
      <li id="li_9DDAAE8EAC314133BD2355427A19EDCF"> <span class="codeph"> SES_TOTAL_PAGE_VIEWS </span> </li> 
      <li id="li_1D0850183CE7434E85128E0B18D37976"> <span class="codeph"> SES_TOTAL_SESSIONS </span> </li> 
      <li id="li_293DBDC1D6CA4804898811E2BDE8030E"> <span class="codeph"> SES_TOTAL_TIME </span> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Estimate the Traffic Required for Success {#task_71AA6922AFD447EA8C5E610A78ABA714}The Traffic Estimator provides feedback that lets you know whether you have sufficient traffic for the test you designed to succeed. 
<draft-comment otherprops="merge">
  target/t_ap_traffic_estimator.xml 
</draft-comment>Because an Automated Personalization activity uses multiple content combinations, it is important to know how much traffic is required to provide meaningful results. The Traffic Estimator uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration needed to make the test successful. 

The Traffic Estimator determines if there is enough traffic to generate personalized models, by comparing the estimated page impressions and typical conversion rate for the pages. Ideally, for a successful activity, the correct sample size ensures that personalized content is ready within 50% of the activity duration or 14 days, whichever is less. This allows sufficient time for obtaining personalized content and learning which content to deliver. 

Once a predictive model passes the required quality criteria and is deemed valid, it is considered ready and is used to calculate a personalized score for offer decisioning. A visual indicator shows when the model is ready and Target is able to begin delivering personalized content. Since lift is expected only after the models are ready, the visual indication allows you to set the right expectation. Use the traffic estimator in the Visual Experience Composer to get a guideline of when the models will be ready. 

>1. From the Experience Composer, click ** [!UICONTROL  Traffic] **.

>       The Traffic Estimator opens. You can click ** [!UICONTROL  Traffic] ** again to hide the Traffic Estimator. 

>       ![](../graphics/ap_est.png) 
>1. Provide the typical conversion rate, estimated activity impressions per day, and test duration.

>    
>    * Number of Content Combinations Calculated automatically based on the number of experiences being created as a part of your activity after any exclusions. 

>    * Typical Conversion Rate The conversion rate is expressed as a percentage, based on your estimation or past data from your analytics system 

>    * Estimated Activity Impressions Per Day This is the number of visitors who are likely to view this page based on the targeting criteria. This could be based on your analytics data. 

>    * Test Duration The number of days you want the activity to run. 



>       The Traffic Estimator uses these statistics to determine what adjustments are needed to run a successful test. 

>       Near the top of the Traffic Estimator, the values you entered are calculated and the results are shown. 

>       ![](../graphics/ap_est_no.png) 

>       As you change the numbers, the estimate changes. For example, if you are testing a large number of combinations and your conversion rate and impressions are too low, the Traffic Estimator shows how long the test will need to run to be successful. Or, if your traffic is low, the Traffic Estimator might suggest a lower number of combinations so you can run the test the desired number of days. 

>       If you do not have sufficient traffic, you can do one or both of the following: 

>    
>    * Reduce the number of combinations.
>    * Increase the duration of the test.


>       Adjust the numbers until the Traffic Estimator says you have sufficient traffic, then design your test accordingly. 

>       ![](../graphics/ap_est_yes.png) 

>       If the traffic is sufficient, the Traffic icon shows a green check. If it is insufficient, the icon shows a red warning label. 
>## Preview Experiences for an Automated Personalization Test in the Visual Experience Composer {#task_21A700587E88453A9FC2210C0DE53A28}Because an automated personalization test compares multiple experiences on a page, it is helpful to preview the page with each experience. 
<draft-comment otherprops="merge">
  target/t_ap_preview_experiences.xml 
</draft-comment>
>1. From the Experience Composer, click ** [!UICONTROL  Preview] **.

>       A list of all experiences appears. 

>       ![](../graphics/ap_preview.png) 
>1. Click an experience in the list to view that experience.

>1. To exclude an experience from the test, select that experience and click ** [!UICONTROL  Exclude] **.

>       ![](../graphics/ap_exclude.png) 

>       You might exclude an experience that shows conflicting variations or an experience that is not aesthetically balanced. 

>       By default, all experiences are included in the Automated Personalization activity. To include an experience that has been excluded, select the excluded experience and click ** [!UICONTROL  Include] **. 
>## Target AP Offers {#task_F207ED7A41B84FD39BB6FCBFABF4B23E}In an Automated Personalization activity, you can target offers to specific audiences. 
<draft-comment otherprops="merge">
  target/t_ap_target_offers.xml 
</draft-comment>
>1. Create an Automated Personalization activity containing the offers you want to Target.
>1. After setting up the offers for the activity in the Visual Experience Composer, click ** [!UICONTROL  Content] **.

>       The Manage Content dialog box opens. 

>       ![](../graphics/ap_content.png) 


>       >[!NOTE]
>       >
>       >You can set up 50 locations, and up to 250 offers per location.

>1. In the Content column, select the offer, then click Targeting and choose the audiences you want to see that offer.

>       Only the selected audiences will be presented that offer. 


>       >[!NOTE]
>       >
>       >In addition to selecting an existing audience, you can combine multiple audiences to create ad hoc combined audiences rather than creating a new audience. For more information, see[ Combining Multiple Audiences ](c_audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5). 

>1. Click ** [!UICONTROL  Done] **.

>## Create Exclusion Groups {#task_AAAA6C7239A84F7696C8492F04B575A2}Create exclusion groups in Automated Personalization (AP) activities to ensure that experiences with the designated offers are automatically excluded. 
<draft-comment otherprops="merge">
  target/t_create-exclusion-groups.xml 
</draft-comment>Exclusion groups are a great way to ensure that incompatible offers are not presented in the same experience in different locations. For example, suppose you have two offers: one is for 20% off of all merchandise and the other is for 15% off. You would never want these two offers to be presented to visitors in the same experience. If you add these two offers to an exclusion group, you can ensure that this will never be the case. 

**To create an exclusion group:** 

>1. While creating or editing an AP activity, click ** [!UICONTROL  Manage Content] ** in the header bar.
>1. in the [!UICONTROL  Manage Content] dialog box, click ** [!UICONTROL  Exclusion Group] **.

>       ![Step Result](graphics/exclusion group create.png) 

>       If you have previously created exclusion groups, they display in the list. If you have not yet create an exclusion group, you are prompted to create one. 
>1. Click ** [!UICONTROL  Create Exclusion Group.] **

>       ![Step Result](graphics/exclusion group create dialog.png) 
>1. (Required) Specify a descriptive name for the exclusion group.

>       A descriptive name helps you or others quickly locate and understand a group's purpose. 
>1. Locate and select the desired offers that you want to add to the exclusion group.

>       Because it makes sense that you select only one offer in a specific location, when you select an offer, all other offers in the same location are greyed out. 
>1. Click ** [!UICONTROL  Save] **.
>## Exclude Duplicate Offers {#concept_EF78A3B7CF4A42A0B336A007A576D7A6}Prevent offers from the offer library from being duplicated when used in different locations in 
<wintitle>
  Automated Personalization 
</wintitle> activities. 
<draft-comment otherprops="merge">
  target/c_exclude_duplicate_offers.xml 
</draft-comment>You might have an activity, for example, with six locations on a page with 12 offers. There is a chance that the same offer could be placed in one or more locations in the activity. This feature prevents duplicate offers from displaying in the same activity. 


>[!NOTE]
>
>If you select to exclude duplicate offers after creating exclusion groups, the experience count on the activity diagram may be incorrect.



Click ** [!UICONTROL  Configure] ** > ** [!UICONTROL  Duplicate Offers] **, then click ** [!UICONTROL  Allow Duplicates] ** or ** [!UICONTROL  Disallow Duplicates] **. 

![](graphics/duplicate_offers.png) 
>## Automated Personalization FAQ {#concept_A688E73D767C4D51855B7B9B5FA6CCD5}List of frequently asked questions (FAQs) about Automated Personalization (AP). 
<draft-comment otherprops="merge">
  target/c_automated_personalization-faq.xml 
</draft-comment>
## How can I compare Automated Personalization to a default experience? {#section_46C1A620A2384C2C8392D6716DD18495}

There is no turn-key option of comparing AP to a default experience. However, as a workaround, if a default offer or experience exists as part the overall activity, to understand its baseline performance you can click the “Control” segment in the reports and locate that particular offer in the resulting offer-level report. The conversion rate recorded for this offer can be used to compare with the conversation rate of the entire “Random Forest” segment. This helps to compare how the machine is doing compared to the default offer. 

## What are best practices to set up an Automated Personalization activity? {#section_E155B26282BE49B58EA2683413D11DE6}

In general, when the models have been built as indicated by the checkmarks on all of the offers, it is time to start cutting back on the random percentage. 

If you want the best information as to how well Automated Personalization is performing, you should first scale back to a 50% random - 50% targeted setting. This will give the most accurate estimate of the lift. 

However, if you are already happy with the lift, you can scale the random component down to an amount that depends on the time scale over which you expect things to change. For example, if it takes one week to build a good model using 90% random traffic, if you scale the random traffic to 90% / 2 weeks = 45%, it will take two weeks to fully incorporate changes into the models. If you do not expect that the offers or response to the campaign will change on a one-month, time-scale then you, in the above example, can scale the traffic down to 90% / 4 weeks = 22.5% random. 

## What are some limits in Automated Personalization? {#section_08BA09ED51B547299963C94FE6417CFA}


* Target has a hard limit of 30,000 experiences. This is crucial. 

* In our empirical understanding of Automated Personalization, we have never observed or understood more than 17 or so modeling groups. Consider this when designing reporting groups. 


>## Share Preview URLs for Automated Personalization Outside of Target {#task_586C6655A6FD4AF08F5678FC3F481EFC}Experience URLs can be generated for Target Automated Personalization activities to see experience content directly on your site before the activity is live for preview and QA purposes. Experience URLs bypass targeting to force viewing of a particular experience. 
<draft-comment otherprops="merge">
  target/t_experience_preview.xml 
</draft-comment>
>[!NOTE]
>
>The Activity QA mode lets you create Activity URLs for other types of activities. For more information, see[ Activity QA ](c_activities.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) 

.

To use experience URLs, you have to share the links generated from Target, and not the final URL you land on when viewing the experience. Also, if the content changes, new URLs must be generated. If you generates new URLs, old ones may not work. 

Use experience URLs to share experiences with team members and to QA experiences across browsers and environments, without creating a separate QA activity. This feature is particularly useful if a site is complex, or if your security policies do not allow the site to be viewed in a simulator. 

>1. Create an Automated Personalization activity.

>       The activity does not have to be live to preview an experience. 
>1. Click the activity to open it.
>1. Click ** [!UICONTROL  View Experience URLs] **, then specify the URL.

>    
>    * If you are using the Visual Experience Composer, the default URL you specified for the activity is entered automatically. You can change this URL and add others, if desired.
>    * If you are using the Form-Based Experience Composer, no default URL is entered automatically. You must specify all URLS you want to preview.


>       You can add multiple URLs, which is useful when running a multi-page test or a template test and you want to preview the activity on more than one page. 

>       A modal window displays links to your experiences on your site to get a "true preview" of the experiences outside of Target's Visual Experience Composer. You must share the links from the message to share the preview. Clicking a link and then copying the resulting URL from the page won't work because the URL contains a parameter that only displays the page correctly when you access the page from the link in the message. Instead, copy the text in the modal window and email the whole text to your team. 

>       If you then make changes to the experience, make sure to generate new preview links for your team by returning to the modal window and clicking "share" to get new links. 


>       >[!NOTE]
>       >
>       >The preview links open in new tabs and require that the pop-up blocker on your browser is disabled.


>       You can also click the Link icon  ![](../graphics/link_icon.png) to view the experience URL. 
>1. Click ** [!UICONTROL  Generate URLs] **, then click each experience to preview it..
>1. Click ** [!UICONTROL  Done] **.
>## Troubleshooting Automated Personalization {#reference_281954549C3E49E2B5498009BBDC62CA}This page documents problems that have been reported when using Automated Personalization. 
<draft-comment otherprops="merge">
  target/r_ap-trouble.xml 
</draft-comment>


><table id="table_07072F1481A34D67A5F73DD8E79BADC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Issue </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>AP activity URL showing offer content on incorrect pages </p> </td> 
   <td colname="col2"> <p> In AP, the url and template testing rules are added to the mbox entry contraint, for example target-global-mbox, where they are evaluated only once. Once a user qualifies for a campaign the mbox level targeting rules are not re-evaluated. However the targeting audience is added to location targeting rules. </p> <p><b>Solution:</b> Add the necessary template rules as the input-audience of the campaign. Audience evaluation happens upon each request/call. </p> <p>This will be fixed in an upcoming release. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Any metric dependent on conversion metric never converts. </p> </td> 
   <td colname="col2"> <p>This is expected. </p> <p>In an AP activity, once a conversion metric (whether optimization goal or post goal) is converted, the user is released from the experience and the activity is restarted. </p> <p>For example, there is an activity with a conversion metric (C1) and an additional metric (A1). A1 is dependent on C1. When a visitor enters the activity for the first time, and the criteria for converting A1 and C1 are not converted, metric A1 is not converted due to the success metric dependency. If the visitor converts C1 and then converts A1, A1 is still not converted because as soon as C1 is converted, the visitor is released. </p> </td> 
  </tr> 
 </tbody> 
</table>

