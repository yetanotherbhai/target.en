---
description: Target Standard introduces several terms and concepts that are different than those used in Target Classic. These terms are shared across the Adobe Marketing Cloud, so your marketing teams can easily work together.
keywords: terminology;migration;migrate from target classic to target standard
seo-description: Target Standard introduces several terms and concepts that are different than those used in Target Classic. These terms are shared across the Adobe Marketing Cloud, so your marketing teams can easily work together.
seo-title: Terminology Comparison Between Target Classic and Standard
solution: Target
title: Terminology Comparison Between Target Classic and Standard
topic: Premium
uuid: b5150ae3-8d67-4097-812e-342e5642c8ea
index: y
internal: n
snippet: y
translate: y
---

# Terminology Comparison Between Target Classic and Standard

This video explains the terminology changes between Target Classic and Target Standard/Premium.


<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2">Adobe Target Terminology Changes</th> 
   <th colname="col3" class="entry">3:32</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/JjilhQxLgOA/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/JjilhQxLgOA/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_4578966D6A6F444FAE10252554142D79">Understand terminology differences between Target Classic and Target Standard/Premium</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Key terms from Target Classic (formerly Test&amp;Target) have changed in Target Standard:


<table id="table_52D42488D90A45E0827D40C4AA53CEB4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Target Classic Terms and Concepts</th> 
   <th colname="col2" class="entry">Target Standard Terms and Concepts</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">1:1</td> 
   <td colname="col2"> <p> <a href="../target/t_automated_personalization.xml#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Automated Personalization</a> </p> <p>Automated Personalization is available as part of the Target Premium solution. It is not included with Target Standard without a Target Premium license. If you have a Target Premium license, the Target Premium card replaces the Target Standard card in the Adobe Marketing Cloud.</p> <p>Major differences between 1:1 and Automated Personalization include:</p> 
    <ul id="ul_65DD19A8E21F4E2B82D20D7EB639C353"> 
     <li id="li_2AAD68D77901410CB05E178450329077">Modeling groups have been replaced by reporting groups</li> 
     <li id="li_A01666CAE91749C288EED7081EF2AC79">The new Random Forest algorithm creates individual decision trees for each model offer. <p>This algorithm creates more efficient models by retaining the information that the Residual Variance Model algorithm discards after a decision is made that does not use that data. The Decision Tree Ensemble algorithm uses this data to learn faster, providing faster results.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Campaign</td> 
   <td colname="col2"> <p><a href="../target/c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local">Activity</a> </p> <p>Formerly called "campaigns", activities are managed in the centralized Activity List, which you reach as soon as you click into the Adobe Target user interface.</p> <p>Activities have a broader definition than only a campaign. They include tests and content targeted to a specific audience. Every activity has an objective and a goal. The objective is a high-level description of what you hope to achieve with the activity. The goal clearly specifies what action a visitor performs to count as a success. For example, you might want to increase revenue (objective), measured by the number of page views of your Checkout Confirmation page (goal).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Campaign Summary</td> 
   <td colname="col2"> <p>Activity diagram</p> <p>The Activity diagram shows the audience, experiences, and other information for an activity. The diagram leads you through the creation and editing of an activity.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Campaign Targeting</td> 
   <td colname="col2"> <p><a href="../target/c_target.xml#concept_A782F8481A5041EBA75103CB26376522" format="dita" scope="local">Activity Targeting</a> </p> <p>Activities are targeted to a specific audience. Visitors are evaluated during each page load to determine whether they still meet the audience criteria. In Target Classic, activity entrants are evaluated one time for campaign entry and continue to see content until they convert, even if their segment membership changes.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Click from Display Mboxes</td> 
   <td colname="col2"> <p> <a href="../target/t_click_tracking.xml#task_AB0B7EBF96AE4BD1BAB6F7550BBF1504" format="dita" scope="local">"Clicked a Link"</a> </p> <p>Target Classic only tracks clicks inside mboxes used in the campaign, and the user must land on a page with the <span class="filepath">mbox.js</span> file. Standard tracks clicks on any element on the page, with no code required other than the single <span class="filepath">mbox.js</span> reference, and no page destination limitations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Conversion</td> 
   <td colname="col2"> <p>Conversion</p> <p>The conversion event is set to "always convert" in Target Standard. The visitor always sees the test content.</p> <p>In Target Classic, a visitor who converts and then reenters the campaign is counted as a new user.</p> <p>In Target Standard, a visitor who converts and then renters the campaign is not counted as a new user. However, each time that visitor converts, the conversion is counted.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Mboxes Around Content Areas</td> 
   <td colname="col2"> <p><a href="../ov2/c_target-implement.xml#concept_60B748DE4293488F917E8F1FA4C7E9EB" format="dita" scope="local">A single line of code is referenced once per page</a>. This JavaScript library manages all communication required between your site and Adobe Target. You can also continue to use mboxes already on your site for displaying content and tracking user behavior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Offers</td> 
   <td colname="col2"> <p><a href="../target/c_manage_content.xml#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local">Content</a> </p> <p>Content refers to both HTML offers and image "assets." The Content Library in Standard stores images and HTML offers. Images can be delivered directly to your site if you are an Adobe Scene7 customer. If you do not use Scene7, you can reference images hosted on your own server or content delivery network (CDN).</p> <p>Although you can create HTML offers separately from the activity, they are typically set up using the Visual Experience Composer during activity creation. If you use the Visual Experience Composer to change content on your site, those changes are specific to that experience and do not get saved to the Content Library for reuse.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Segments</td> 
   <td colname="col2"> <p><a href="../target/c_target.xml#concept_A782F8481A5041EBA75103CB26376522" format="dita" scope="local">Audiences</a> </p> <p>Formerly called "segments" or "audience segments," audiences are managed from the central Audience Library, which includes out-of-the-box and custom created audiences within Adobe Target, as well as audiences sourced from other Adobe Experience Cloud solutions (leveraging our People core service in Adobe Experience Cloud).</p> <p>An audience, like a Target Classic segment, is a set of site visitors who meet specific criteria. Activities are often targeted at a specific audience. An audience might be visitors who use a particular browser, operating system, search engine, or any of several other criteria. Multiple criteria can be combined to define an audience.</p> <p>Separate audiences can be created for content delivery or reporting. Reusable segments in Target Classic are synced with Target Standard for use in Activities.</p> <p>Audiences are created globally. In other words, any audience you create is available in the Audiences list for reuse in other activities.</p> </td> 
  </tr> 
 </tbody> 
</table>

