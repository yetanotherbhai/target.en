---
description: Rule-based targeting uses parameters you establish to target based on specific criteria. If visitors meet the criteria, they are included in the campaign and campaign reports.
keywords: Targeting
seo-description: Rule-based targeting uses parameters you establish to target based on specific criteria. If visitors meet the criteria, they are included in the campaign and campaign reports.
seo-title: Rule-Based Targeting
solution: Target
subtopic: Multivariate Test
title: Rule-Based Targeting
topic: Premium
uuid: b65853ad-4ede-4fae-bab7-d9d354b82f93
index: y
internal: n
snippet: y
translate: y
---

# Rule-Based Targeting

## Rule-Based Targeting {#concept_087408B488304A54917585D40482791A}Rule-based targeting uses parameters you establish to target based on specific criteria. If visitors meet the criteria, they are included in the campaign and campaign reports.You can group visitors based on anything Target knows about the visitor, including how the visitor reached the site, technographic information such as the browser and operating system, geographic data, and visitor behavior attributes. You can specify parameters and values passed on your Web site as preconditions for display. 

For information about the targeting categories that are available for audiences, see [ Rule Categories for Audiences ](c_target_rules.md#concept_E3A77E42F1644503A829B5107B20880D). 

You must enter unencoded characters in targeting conditions to match correctly. All activity targeting criteria use unencoded characters. 

The following list shows some examples of targeting: 


* An experience targeting activity that shows exclusive content to visitors coming from an email notice Everyone else sees default content. 

* An A/B/C/D test to only visitors from your sports affiliates
* An A/B/C/D test limited to a single category in your merchandising database
* A multivariate test only to visitors who searched on the keywords "mortgage" or "mortgage rate"
* An A/B...N campaign that shows different content based a returning visitor's category affinity
* An A/B...N campaign offering a high-margin product to consumers fitting into top cells, according to your RFM analysis


This video includes information about setting up audience rules. 

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Using Audiences </th> 
   <th colname="col3" class="entry"> 6:22 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/TAMBpW9vpOI/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/TAMBpW9vpOI/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Explain the term "audience" </li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405">Explain the two ways audiences are used for optimization </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Find audiences in the Audiences List </li> 
      <li id="li_699D4D5D089A4FB7BA4C5E95337AC34A">Target an activity to an audience </li> 
      <li id="li_87E7AFFEEC9C42ABB51C279221E17A14">Use audiences for passive reporting in an activity </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Behavioral Targeting {#concept_CEE693A71E8D4C2CBF51DAA97DE8D61D}Behavioral targeting refers to all of the visitor data that can be stored and used to segment your population and target different content to different people based on their visitor profile. 
<draft-comment otherprops="merge">
  target/c_target_behavioral.xml 
</draft-comment>Some of the information you can track includes (but is not limited to): 


* How often someone comes to the site
* Whether they purchase items
* How much they spend
* Whether they are a member


All of these elements can greatly impact what you learn from your tests and other optimization activities. 
>## Behavioral Targeting Basic Steps {#reference_26AAC9E3D2734CA7B48CF141A68D6030}The following steps outline the process of setting up behavioral targeting. 
<draft-comment otherprops="merge">
  target/r_target_behavioral_steps.xm 
</draft-comment>
>
>1. Define your business objective. 

>
>    * Clear out old inventory?
>    * Highlight a niche product?
>    * Increase form completion from female visitors?
>    * Map your customer segmentation to your Web content.


>1. Define the user most likely to help you. 

>
>    * Who are these people?
>    * Start with simple, broad segments and refine them over time.


>1. Define the behaviors the user is most likely to exhibit. 

>
>    * Are they a return visitor?
>    * Are they a frequent visitor?
>    * What pages do they visit?
>    * Have they filled out a form before?
>    * Have they purchased something before?
>    * Are they weekend shoppers?
>    * Did they come from specific search engines? Social referrers?
>    * Do they come primarily from certain geographies?


>1. Capture relevant behaviors in profiles. 

>
>    * Custom created labels for your users
>    * Stored in databases and associated with your visitor through a cookie
>    * Two strategies: either in-mbox profile parameters or [ script profile parameters ](c_target_rules.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)
>    * In-mbox profile parameters are placed in the page's mboxCreate call: >    
>      ```
>      <script type="text/javascript"> 
>       
>         mboxCreate('myMbox', 'profile.name1=value1', 'profile.name2=value2'); 
>       
>      </script> 
>       
>      <script type="text/javascript"> mboxCreate('myMbox', 
>       
>      'profile.name1=value1', 'profile.name2=value2'); </script>
>      ```


>    * Script profile parameters are defined with JavaScript in the admin tool: >    
>        1. Select ` Segments` > ` Profiles`. 

>        1. Clicking ` add attribute` to add a new parameter.
>        1. Name your profile and type the JavaScript code into the text fields. 

>        1. Click ` Start` to start the script.
>      The profile data is now available for use in campaigns. 



>1. Target content to those users based on their profiles. >
>    * Create offers and use the targeting features to send that content to specific users.



>For more information and ideas about leveraging behavioral targeting, see [ Examples and Tips ](c_target_behavioral_examples.md#concept_4B15FDC3EA484294886F8BB00B34EACC). 
>## Percentage Targeting {#concept_9D0C47368EB942C9A66CE03C6BD92412}You can set up your campaign so a specified percentage of visitors sees each experience. 
<draft-comment otherprops="merge">
  target/c_target_percent.xm 
</draft-comment>For example, you might have three experiences, and set them up so 50% of visitors see Experience A while 25% of visitors see Experience B and another 25% see Experience C. 

When a visitor enters the campaign, a random number is generated. That number is used to choose the experience to display. If there has been very little traffic, for example at the beginning of a campaign, the traffic might not be split exactly as specified in the percentages. The more traffic you get, the more exact the percentages will become. 

The total of the percentages for the campaign should add up to 100%. 
>## Combined Rules-Based and Percentage Targeting {#concept_D6B6F16F931C4E67AAB8F90621879FCC}You can combine percentage-based and rules-based targeting. 
<draft-comment otherprops="merge">
  target/c_target_percentandrule.xml 
</draft-comment>For example, you might want to show a particular offer to 60 percent of visitors from California. When using the two targeting styles together, the rule is considered first, then the percentage. In this example, all California visitors are sampled first, then 60% of those visitors see the specified content. 

You might want to test within mutually exclusive groups, such as new or returning visitors, or purchasers vs. non-purchasers. And, you might want to show 30% of your new users one set of content. Or you might want 75% of non-purchasers to view a particular offer that you only want to show to 25% of purchasers. 

For example, you might create a campaign with four experiences that you want to target as follows: 


* Experience A: Targeted to 20% of male visitors
* Experience B: Targeted to 80% of male visitors
* Experience C: Targeted to 10% of female visitors
* Experience D: Targeted to 90% of female visitors


In this example, the segments * ` Male` * or * ` Female` * are determined first, then the segments are divided according to the specified percentages. 


* Segment * ` Male` * 
    * 20% Experience A
    * 80% Experience B

* Segment * ` Female` * 
    * 10% Experience C
    * 90% Experience D


>## How Target Decides Who Sees What Content {#concept_014AB6795D2D4B6EB5E45A226A4FF7E9}Target uses the criteria you set up for your activity to determine who sees what content, based on a specific order of operations. 
<draft-comment otherprops="merge">
  target/c_target_whoseeswhat.xml 
</draft-comment>Target does not automatically split traffic if you have two experiences with the same rules-based targeting. If the visitor qualifies for Experience B and Experience C based on the targeting, then 100% of those users go into the first experience (in this case, Experience B). 

The same is true for experiences with no targeting. In the following example, if the user does not qualify for Experience A or B, then they are always placed into Experience C (in other words, no one will make it to Experience D): 


* Experience A - 10% of visitors 

* Experience B - Only show Fri/Sat/Sun 

* Experience C - (not targeting) 

* Experience D - (not targeting) 



One way around this is to create a profile script that generates a random number from 1...100 and then set up the targeting this way: 


* Experience A - 10% of visitors 

* Experience B - Only show Fri/Sat/Sun 

* Experience C - (random number profile has value 1..50) 

* Experience D - (random number profile has value 51..100) 



You can add percentage targeting to Experience C (set Experience C to 50% of traffic and leave Experience D without any targeting) to make sure visitors get into all experiences. 

If your activity has multiple experiences that are set up with specific percentage targets, for example four experiences each configured to receive 25% of the traffic, a random number is generated and that number determines the experience shown to a visitor. In this example, if the random number is 30, the visitor would receive the second experience because 30 is between 25 and 50, the second range when dividing 100 into 25% chunks. 
>## Validate Targeting to URL or Referring URL Parameters {#task_378FB18E8C7244CDA8C1D029DBACBAEE}Follow these steps to validate targeting to a URL or referring URL parameters. 
<draft-comment otherprops="merge">
  target/t_target_validate_url.xml 
</draft-comment>
>1. Append the targeting parameters and values to the end of the URL, or referring page URL.

>       The example below shows an appended target condition where your targeting condition is met when the keyword equals "chairs": 

>    [!DNL  http://www.yourcompany.com/asp/feature_item.asp?​keyword=chair&amp;amp;categoryId=45] 
>1. Confirm that you see the correct content for the targeting condition.
>1. Delete cookies and confirm you do not see the content when you do not meet the targeting condition.
>1. If segments filters are set, confirm reports correctly capture the URL parameter values.
>## Validate Targeting to New or Returning Visitors {#task_C9BF77B62B4943A7BF1DC37AA752001C}Follow these steps to validate targeting to new or returning users. 
<draft-comment otherprops="merge">
  target/t_target_validate_visitors.xml 
</draft-comment>
>1. In your browser, delete all mbox cookies.

>       This allows you to appear as a new user (new visitor). 
>1. Browse to the targeted campaign, experience or mbox, or conversion mbox.
>1. Verify you see the expected content for a new user.
>1. Test the expected content (or lack of content ) shows for a returning visitor.

>       Close your browser, and reopen it. Do not delete your mbox cookies. Confirm that as a returning visitor, you see the expected content. 

>       A "returning visitor" is someone who is on the website for at least their second session. 

>       **Tip:** To imitate being a return visitor for testing purposes, there must be at least 30 minutes of inactivity between site views. When a second session has started, a new ` sessionID` appears in the ` mboxDebug` popup utility. 
>1. If segments filters are set, confirm reports correctly capture the parameter values.
>## Validate Targeting to Profile Parameters {#task_FEE3A70A4F944B35958CF4B5DA82EB0D}Follow these steps to validate targeting to profile parameters. 
<draft-comment otherprops="merge">
  target/t_target_validate_profile.xml 
</draft-comment>
>1. Perform any action that sets the required profile value.
>1. Close and reopen your browser.

>       Do not delete any files. The profile value is connected to your browser cookie. 
>1. Return to the page where the campaign should display.
>1. Confirm that the correct offer content is shown to you.
>1. If segments filters are set, that reports correctly capture the parameter values.
