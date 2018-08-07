---
description: Information to help you set the elements you want to appear in your report. Report settings can be saved for later use.
keywords: Target;reports;report settings;environment;host group;success metric;cumulative lift;cumulative difference from control;daily lift;daily difference from control;control
seo-description: Information to help you set the elements you want to appear in your report. Report settings can be saved for later use.
seo-title: Report Settings
solution: Target
title: Report Settings
topic: Premium
uuid: e0493f50-3802-4100-aa78-49b61b159964
index: y
internal: n
snippet: y
translate: y
---

# Report Settings

To display a report, click ** `Activities` **, click the desired activity from the list, then click the ** `Reports` ** tab. 
![](graphics/report ui.png) 
The following options and settings are available on the report page:


<table id="table_C54ED6B14A6B476DBB706BCE2E20F980"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Option or Setting</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Report Metric</p> </td> 
   <td colname="col2"> <p>Click the <span class="uicontrol">Report Metric</span> drop-down list to select a different <a href="r_success_metrics.xml#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local">success metric</a> or multiple metrics to display in the graph and chart. </p> <p>By default, the primary metric is determined in the success metrics setup when you create the activity. If you change the setup and re-save the activity, the primary metric for reporting is updated.</p> <p>For more information about selecting multiple metrics to view in reports, see <a href="c_view-multiple-metrics.xml#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local">View Multiple Metrics in a Report</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audience</p> </td> 
   <td colname="col2"> <p>Click the <span class="wintitle">Audience</span> drop-down list to change the displayed <a href="c_target.xml#concept_A782F8481A5041EBA75103CB26376522" format="dita" scope="local">audience</a> for the report. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Date Range</p> </td> 
   <td colname="col2"> <p>Select new <span class="uicontrol">Start</span> and <span class="uicontrol">End</span> dates for the report. </p> <p>Reports have the following date restrictions:</p> <p> 
     <ul id="ul_D87ACEE170DE4C0A86B89963A53F1C87"> 
      <li id="li_4D53359CB23448E59DC3DE7596A32598">Start date of the report must be within the last two years.</li> 
      <li id="li_8C4F0F5831A94E3E9FA0FDF6159BF39A">Daily reports are limited to 100 days.</li> 
      <li id="li_965EB8A8964146E2B416402C61FA0F07">Hourly reports are limited to 15 days.</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Settings</p> </td> 
   <td colname="col2"> <p>Click the <span class="wintitle">Settings</span> icon ( <img href="graphics/icon_gear.png" id="image_AC78ABAD53934D7D84A5826829E50632" /> ) to configure report settings, then click <span class="uicontrol">Save Settings</span> when done. </p> <p>The following illustration shows the Settings dialog box for an A/B activity:</p> <p style="text-align: center;"><img href="graphics/ab_settings_dialog.png" id="image_0BC1D4BB97D641D398DDAD76A144EB59" /> </p> <p>Depending on the selected activity type, the options vary:</p> <p> 
     <ul id="ul_561C94367E61415EBE2E528A76635FBD"> 
      <li id="li_1BE80026F6CA4E1B9CE38F653E78DF29"> <p><b>Counting Methodology:</b>Select the desired methodology: </p> <p> 
        <ul id="ul_958E45EF725642ACBF6EF773F5C8B38D"> 
         <li id="li_A877AECC573F4686982E9BEACB1F194A">Visitors</li> 
         <li id="li_BE0FB66BDAA64B8AB2906D904972139D">Visits</li> 
         <li id="li_4DEF774018A9437582D58771ECC24E7C">Activity Impressions</li> 
        </ul> </p> </li> 
      <li id="li_CA1E3FEC74ED4F27BF4F830369373641"> <p><b>Control:</b>Select the control experience to use when calculating and comparing lift. 
        <!--This setting is not available for Experience Targeting (XT) activities. --> </p> </li> 
      <li id="li_CE7F820CCA8F432788A0AC6F5D415FC8"> <p><b>Environment:</b>Select the environment (host group) to use for the report. 
        <!--This setting is not available for Recommendation activities.--> For more information, see <a href="../ov2/c_hosts.xml#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local">Hosts</a>. </p> </li> 
      <li id="li_60E43F6BD01C424CB11FC3B559C74D8B"> <p><b>Reset Report Data:</b>Reset reporting data to remove old data. Current visitors will remain in the activity. 
        <!--The <wintitle>Reset Report Data</wintitle> option does not apply to Analytics for Target (A4T) activities.--> This option is available only for those with approver permissions. </p> <p> <p type="important">Note: This is a permanent action and cannot be undone.</p> </p> </li> 
      <li id="li_DA247399B9C3400BA8C35ABA27432759"> <p><b>Exclude Extreme Values:</b> The <span class="wintitle">Exclude Extreme Values</span> toggle applies to activities with Revenue and Engagement metric types only. For more information, see <a href="t_excluding_extreme_orders.xml#task_2AE7743FFCDD466DAEEB720BE5F33DAA" format="dita" scope="local">Excluding Extreme Orders</a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Download</p> <p style="text-align: center;"><img href="graphics/icon download report.png" id="image_416D5D5C14AD47328D47B25991D476A9" /> </p> </td> 
   <td colname="col2"> <p>Click the Download icon ( <img href="graphics/icon download report.png" id="image_E917D35695024DB2B93A62E76CEB1DF6" /> ) to download report data in a <span class="filepath">.csv</span> format for quick import into Excel, Access, or other data analysis programs. For more information, see <a href="c_downloading-data-in-csv-file.xml#concept_3F276FF2BBB2499388F97451D6DE2E75" format="dita" scope="local">Downloading Data in a CSV File</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>More Options</p> <p style="text-align: center;"><img href="../graphics/icon_more_options.png" id="image_97E4953AC53C4F25989C7247D9C89AEA" /> </p> </td> 
   <td colname="col2"> <p>Click the More Options icon ( <img href="../graphics/icon_more_options.png" id="image_C635FA8DCED143EA85FD3CE4799E3C69" /> ) to access the <span class="wintitle">Edit Activity</span> and <span class="wintitle">View Experience URLs</span> options. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Table View</p> <p style="text-align: center;"><img href="graphics/icon table view report.png" id="image_412801B088124D669141A64E939E5865" /> </p> </td> 
   <td colname="col2"> <p>Click the <span class="uicontrol">Table View</span>icon ( <img href="graphics/icon table view report.png" id="image_8ED9F98B983C4F5782833EA2D51DEAA6" /> ) to view the report as a table. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Graph View</p> <p style="text-align: center;"><img href="graphics/icon_graph_report.png" id="image_8B717A04CB7043A6A58B4398E1B9E884" /> </p> </td> 
   <td colname="col2"> <p>Click the <span class="uicontrol">Graph View</span> icon ( <img href="graphics/icon_graph_report.png" id="image_105702B0BFCE4DC3A2496DF643813DA4" /> ) to view the report as a graph. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Confidence interval and lift visual representations</p> <p style="text-align: center;"><img href="graphics/confidence lift visual.png" id="image_2C92452192BA46CBB289A61D1546F058" /> </p> <p>Available only when viewing A/B, Experience Targeting (XT), and Recommendations activities in Table View.</p> <p>This feature is not available for activities that use Analytics as the reporting source (A4T).</p> </td> 
   <td colname="col2"> <p>Reports include visual representations that let you visually see the confidence interval and lift so that you can more accurately determine a winner. You can mouse over the representations to see the actual numbers.</p> <p style="text-align: center;"><img href="graphics/whisker.JPG" id="image_FFA446B6BF0D48CD8B987F8E2FD3A6FA" /> </p> <p>The new visual representations within reports are color coded to help you determine whether any experience is a clear leader with no overlaps with others, or whether there are a few experiences that have overlaps, but with one having an edge. The red and green portion of the experience bar indicate whether the experience is better or worse than the control's performance.</p> <p>An experience with a high confidence value coupled with an interval with low or no overlap with other experiences is a great candidate for declaring a winner in an A/B Test, for example.</p> <p>Low, Mean, and High on hover indicate the upper and lower bounds based on the confidence interval displayed in the Metric column as a +/- value.</p> <p>Note that the confidence and confidence interval calculations vary for different activity types and this feature does not make any changes in that regard.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Location Contribution</p> <p style="text-align: center;"><img href="graphics/icon_location_contribution.png" id="image_EF5DAA5B838A46EC832865574BE6B750" /> </p> </td> 
   <td colname="col2"> <p>
     <!--(Multivariate tests only) -->Click the <span class="uicontrol">Location Contribution</span> ( <img href="graphics/icon_location_contribution.png" id="image_8D13E82D6A2C4B8B81BB8CA72D734A04" /> ) icon to switch the report to show contribution by location. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experiences</p> <p>(Available only when viewing the report in Graph View)</p> </td> 
   <td colname="col2"> <p>Select or deselect experiences on the left side of the chart to display or hide the corresponding experiences from the chart.</p> <p>If the following illustration, only experiences B and C display in the report:</p> <p style="text-align: center;"><img href="graphics/report experiences.png" id="image_25315E8B81794F45921436F24A22BC69" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Running Average</p> <p>(Available only when viewing the report in Graph View)</p> </td> 
   <td colname="col2"> <p>Select the desired graph view:</p> <p> 
     <ul id="ul_BB422529932844E7A447016268F2A40B"> 
      <li id="li_325DD60B965544A3BD425550834BA4EC">Running Average</li> 
      <li id="li_8197935D95EB4BB2BE4BBE674B30D58F">Running Average Lift</li> 
      <li id="li_D6EBB63A447945A69D3679C0F247B104">Daily</li> 
      <li id="li_F12D3E41975B497F825F3CAD1ABA112F">Daily Lift</li> 
     </ul> </p> <p style="text-align: center;"><img href="graphics/report running average.png" id="image_BE44A85D54DA4900B84E9E72A034171F" /> </p> <p> <p>Note: The name of this drop-down list varies depending on the selected view, but it'll be one of the four views listed above.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>Counting Methodology</p> <p>(Available only when viewing the report in Graph View)</p> </td> 
   <td colname="col2"> <p>You can choose the counting methodology for graphs in reports. Note that this is not supported for Automated Personalization (AP) activities.</p> <p>To access the Counting Methodology option, while viewing a report in graph mode, click the <span class="uicontrol">My Primary Goal</span> drop-down, then select the counting methodology. </p> <p>The counting methodology will be the same as the one selected in the <span class="wintitle">Settings</span> dialog, described above. </p> <p style="text-align: center;"><img href="graphics/counting methodology.png" id="image_4C35F2E9638F413D9F48C09929B5B390" /> </p> <p>By default, the graph is plotted in <span class="wintitle">Daily</span> mode. </p> <p>You can change the mode by clicking the <span class="wintitle">Daily</span> drop-down list, then selecting <span class="wintitle">Cumulative</span>. </p> <p style="text-align: center;"><img href="graphics/counting methodology 2.png" id="image_AA2B9E0EF030484AA94BBEB74AE15009" /> </p> <p> <p>Note: The name of this drop-down list varies depending on the selected mode.</p> </p> <p>There are four modes for Auto-Target activities: Daily Control, Daily Targeted, Cumulative Control, and Cumulative Targeted.</p> <p>The default order in which the graph is plotted is as follows:</p> <p> 
     <ul id="ul_BE4C2F84C22743A6BF4F52AAF7C6E3AE"> 
      <li id="li_FBE79E49F543421FA22DE822EC738D3A"> <p>A/B Tests (including Auto-Allocate and Automated Personalization): Order of experience creation, in descending order.</p> </li> 
      <li id="li_2A9EA06D6AB64CE1AC48812871D67F29"> <p>Experience Targeting (XT): Order of experiences in the activity.</p> </li> 
      <li id="li_7EA4D0A33BA844F6A7371629949C2B9B"> <p>Multivariate Test (MVT): Alphabetical by experience name.</p> </li> 
      <li id="li_7B303007D1044D26987AEE9F6CEE3418"> <p>Recommendations: Order of experience creation, in descending order.</p> </li> 
     </ul> </p> <p>As you work with the Counting Methodology options, consider the following caveats:</p> <p> 
     <ul id="ul_E00BAB57DEED426C8E3602B6E1511C0C"> 
      <li id="li_903CADE645D54993B3025E146FA65202"> <p>For an Auto-Target activity, there is no option for selecting "Visitors" as the counting methodology. Auto-Target is the only activity type that you cannot plot by visitors.</p> </li> 
      <li id="li_23C38A7E22A34CD9BA79216059BD8605"> <p>For activities that use Analytics as the reporting source (A4T), you cannot plot Visitor, Visit, or Impression cumulatively.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Working with Graphs That Have More Than 16 Experiences in the Activity</b> </p> <p>If an activity has fewer than 16 experiences, each experience is plotted in a different color in the graph.</p> <p>If an activity has more than 16 experiences, the colored lines for the first 16 experiences display in the graph. The remaining experiences are greyed out in the Experiences pane on the left side and no corresponding plot lines display in the graph. The lines for only 16 experiences can be shown at any given time.</p> <p>If you hover over any of the greyed experiences, a new grey plot line corresponding to that experience temporarily displays in the graph. To display the plot line of a greyed experience in a color, you can deselect an experience that displays in color by clicking its name and then select the desired greyed experience by clicking its name.</p> <p>As an example, the following illustration shows an activity's graph that has 26 experiences:</p> <p style="text-align: center;"><img href="graphics/graph 1.png" id="image_77D9190C5EFB488AB4250B692239AB81" /> </p> <p>The graph displays the lines for the first 16 experiences (some overlap, so it appears that there are fewer than 16 lines). The colored dot in the Experiences pane on the left side next to each experience name indicate that the experience's plot line displays in the corresponding color.</p> <p>If you scroll down in the Experiences pane, you'll notice that the names for the 17th through 26th experiences are greyed out, as shown in the following illustration:</p> <p style="text-align: center;"><img href="graphics/graph 2.png" id="image_CAA13A16A89F4A44B7E275BADF081C64" /> </p> <p>If you hover over one of the greyed experiences, a new grey plot line corresponding to that experience temporarily displays in the graph.</p> <p>Suppose you want to display the plot line for Experience R and you don't want to see the line for Experience P. You can click Experience P's name to deselect it and then click Experience R's name to select it, as shown below:</p> <p style="text-align: center;"><img href="graphics/graph 3.png" id="image_E1AE42CA2BCA49D2B8E9C8B665117E83" /> </p> </td> 
  </tr> 
 </tbody> 
</table>

