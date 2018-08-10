---
description: Target different content and experiences to specific audiences to optimize your web marketing by displaying the right messages to the right people at the right time.
keywords: targeting;cookie;first-party cookie;1st-party cookie
seo-description: Target different content and experiences to specific audiences to optimize your web marketing by displaying the right messages to the right people at the right time.
seo-title: Audiences
solution: Target
title: Audiences
uuid: 78d8882b-8aa0-4719-bbe9-253b294c632a
index: y
internal: n
snippet: y
translate: y
---

# Audiences

## Audiences {#concept_A782F8481A5041EBA75103CB26376522}Target different content and experiences to specific audiences to optimize your web marketing by displaying the right messages to the right people at the right time.By default, traffic is split evenly between experiences. However, you can specify[ percentage targets](c_target_rulebased.md#concept_9D0C47368EB942C9A66CE03C6BD92412) for each experience. 

Targets can also be [ rule-based](c_target_rulebased.md#concept_087408B488304A54917585D40482791A). A rule-based target is based on information gathered about the visitor, such as the visitor's location, browser, operating system, mobile device, or other data. 

You can [ combine percentage-based and rule-based targeting](c_target_rulebased.md#concept_D6B6F16F931C4E67AAB8F90621879FCC). For example, you might want to show a particular offer to 60 percent of visitors from California. When using the two targeting styles together, the rule is considered first, then the percentage. In this example, all California visitors are sampled first, then 60% of those visitors see the specified content. 

If you want to show the same content to everyone, but break out report data by group, use segment filters instead of targeting. 

When a visitor lands on a page where you have set up an activity, [!DNL  Target] determines whether the visitor qualifies as a member of an audience that has been identified for the activity. If the visitor cannot be identified as a member of a target audience, that visitor is shown default content and is not included in the reports for the activity. 

If the visitor is identified as part of a target audience, [!DNL  Target] determines which experience to display, based on the criteria established when the activity was created. 

This video includes information about setting up targeting and audiences. 

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Workflow - Targeting </th> 
   <th colname="col3" class="entry"> 2:14 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/LOmBgKPeBtA/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/LOmBgKPeBtA/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532"> <p>Assign an audience to your activity </p> </li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405"> <p>Throttle traffic up or down </p> </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A"> <p>Select your traffic allocation method </p> </li> 
      <li id="li_699D4D5D089A4FB7BA4C5E95337AC34A"> <p>Allocate traffic between different experiences </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## How Targeting Works {#concept_459AB4DEE7364A9290C2FD405DC29584}<keyword>
  Adobe Target
</keyword> integrates with your web pages by means of the 
<filepath>
  at.js
</filepath> or 
<filepath>
  mbox.js
</filepath> JavaScript library. 
<draft-comment otherprops="merge">
  target/c_target_how_target_works.xml 
</draft-comment>[!DNL  Target Classic] used mboxes around each area on your page where you want to display targeted content or collect data. These mboxes are not required in [!DNL  Target Standard]. Instead, one [ JavaScript library](c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB) referenced on each page is all you need to run your optimization activities. 

Each time a visitor requests a Target-enabled page, [!DNL  Target] uses the following process to serve offers: 


1. A customer requests a page from your server and it displays in the browser. 

1. A first-party cookie is set in the customer's browser to set a unique visitor ID. 

   A [!DNL  Marketing Cloud visitor ID] is also set if you are using the Master Marketing Profile. 

1. The page makes a call to [!DNL  Target] either via the [!DNL  target.js] file or an mbox on your page. 

1. [!DNL  Target] references the profile associated with the visitor. 

1. [!DNL  Target] executes any profile scripts associated with that profile. 

1. [!DNL  Target] calculates its response. 

1. Content is displayed based on the rules of your activity or campaign. 



The offer that is displayed in a basic A/B test is randomly chosen. As a result of this random splitting of traffic, it can take a lot of initial traffic before the percentages even out. For example, if you have an activity with two experiences, the starting experience is chosen randomly. If there is little traffic, it's possible that the percentage of visitors can be skewed toward one experience. As traffic increases, the percentages should become more equal. 
