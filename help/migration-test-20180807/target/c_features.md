---
description: Adobe Target Standard provides a visual interface that helps you create and manage A/B tests and rules-based targeting activities and share information with the Adobe Marketing Cloud.
seo-description: Adobe Target Standard provides a visual interface that helps you create and manage A/B tests and rules-based targeting activities and share information with the Adobe Marketing Cloud.
seo-title: Target Standard Features
solution: Target
title: Target Standard Features
topic: Standard
uuid: 12feb05b-fbde-43ff-b02a-a78916b128a5
index: y
internal: n
snippet: y
translate: y
---

# Target Standard Features

Target Standard provides the following functionality:


<table id="table_6571A9CC12EE41D1B19D1EB246CEAA3D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Feature</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Visual Experience Composer</td> 
   <td colname="col2"> <p>The Visual Experience Composer provides a visual tool for creating and editing experiences. The Visual Experience Composer lets you do the following:</p> <p> 
     <ul id="ul_D5F591184FBB47B8A30D885325A2EE37"> 
      <li id="li_BA1B8C68DEB648FD8CF2641E01011F1C">Visually edit text and HTML</li> 
      <li id="li_7AB34BB079B444B3BC997FEFC610614E">Change link destinations</li> 
      <li id="li_CC361F067E3D41B89A2C162F9F79E34A">Swap the content of an element with new content.</li> 
      <li id="li_ED19864C6419424683598801ECE62323">Remove an element from a page (area used by element is collapsed)</li> 
      <li id="li_B65C76EBC5C44839B1BFB173D9379D64">Hide an element on the page (area used by element remains as white space)</li> 
      <li id="li_CFD9099A37A049A7B686D88B73B0A099">Change the CSS class for an element.</li> 
      <li id="li_6781C0B1FC894AEC919ECAFA0F2DA81F">Track clicks on an element.</li> 
      <li id="li_250FE50346ED4B00BF8FCF0ED6FEEAF4">Create goals (success metrics) for the page or for clickable elements.</li> 
      <li id="li_CC99A487118F43A383C439274AD11A40">Visually simulate an activity.</li> 
     </ul> </p> <p>Experiences can also be modified manually in your page code. However, manually editing experiences is outside the scope of this document.</p> <p>See <a href="c_experiences.xml#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local">Experiences</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Flow Diagram</td> 
   <td colname="col2"> <p>The Flow Diagram leads you through the workflow of creating an activity and its audience, setting up experiences, and specifying success metrics. It shows where you are in the process of creating an activity, and lets you easily navigate to another step.</p> <p>See <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local">Activities</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Single Line of Code Implementation</td> 
   <td colname="col2"> <p>Target Standard requires one line of code on each page that you want to test or target. This line of code makes it possible to use the Visual Experience Composer to make changes anywhere on the page to design your tests. Typically, the code is added to a global header that is used throughout the site.</p> <p>See <a href="c_implementation.xml#concept_70A4547532954655895AB9996825D0BF" format="dita" scope="local">Implementation</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Click Tracking</td> 
   <td colname="col2"> <p>You can track clicks on any element on the page, without adding any code. These links can lead to another page on your site, or on an external site. Clicks on multiple elements can be grouped together and viewed as a single success metric.</p> <p>See <a href="r_success_metrics.xml#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local">Success Metrics</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">User and Role Management</td> 
   <td colname="col2"> <p>Administrators are set up in the Adobe Marketing Cloud.</p> <p>Much of the user management is now done in the Marketing Cloud interface. In the Adobe Marketing Cloud, click <span class="uicontrol">Tools</span> &gt; <span class="uicontrol">User Management</span>. </p> <p>See <a href="c_user_management.xml#concept_501166A5F8FB4964A3AAA15D6095C6BE" format="dita" scope="local">User Management</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Image Swapping</td> 
   <td colname="col2"> <p>To swap images in an experience, click on the image in the Visual Experience Composer, and select <span class="uicontrol">swap image</span>. Then choose an image stored in the Adobe DAM. This feature requires an Adobe Scene7 license. If you do not have Adobe Scene 7, host your images on your standard image server, and simply link to them by entering their URL in the Visual Experience Composer. </p> <p>See <a href="c_manage_content.xml#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local">Manage Content</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Activity Management</td> 
   <td colname="col2"> <p>View a list of all of your activities and their statuses, sort by status, last modified date or user, and view details about each activity.</p> <p>See <a href="c_activities.xml#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local">Activities</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Audiences</td> 
   <td colname="col2"> <p>An audience is a group of people who meet a rule condition, like "users on Firefox" or "new visitors." You can display an activity to a particular audience. In your reports, you can show how an activity performed for a particular audience. Several audiences are pre-configured for you, and you can create others that meet your specific requirements. Activities can be created with a single audience.</p> <p>See <a href="c_audiences.xml#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local">Audiences</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Metrics</td> 
   <td colname="col2"> <p>You can choose from several out-of-the-box metrics and assign them to activities. You can also create and assign your own custom metrics based on following categories:</p> <p> 
     <ul id="ul_1353E412E6F14D10AE02DD96CEAC9989"> 
      <li id="li_03CABD0C2101416EA87D23977262574B">Conversion and pre-conversion: for example, accessing a Shipping page.</li> 
      <li id="li_91C3DCCE120643A59A6B5A3055E93A5F">Revenue: revenue per visitor (RPV) or average order value (AOV).</li> 
      <li id="li_D6F2B9BF7A1443E094EFDFC7B95BF7B2">Engagement: for example, page views, time on site, and page scores.</li> 
      <li id="li_A653939A717E4E229720E0B1847C26B6">Click tracking: for example, tracking clicks on a shopping cart page.</li> 
     </ul> </p> <p>See <a href="r_success_metrics.xml#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local">Success Metrics</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Reporting</td> 
   <td colname="col2"> <p>Reports show full results of activities. Statistical confidence and lift calculations are available, and reports can be segmented by defined audiences. Reports can be filtered and shared with the Adobe Marketing Cloud.</p> <p>See <a href="c_reports.xml#concept_B5077F5503AA4C98901AA99EDCE6CDE6" format="dita" scope="local">Reports</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

