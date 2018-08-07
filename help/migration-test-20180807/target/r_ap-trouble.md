---
description: This page documents problems that have been reported when using Automated Personalization
seo-description: This page documents problems that have been reported when using Automated Personalization
seo-title: Troubleshooting Automated Personalization
title: Troubleshooting Automated Personalization
uuid: b33d0b32-83e2-47a7-9e52-c564be6e4c66
index: y
internal: n
snippet: y
translate: y
---

# Troubleshooting Automated Personalization




><table id="table_07072F1481A34D67A5F73DD8E79BADC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Issue</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>AP activity URL showing offer content on incorrect pages</p> </td> 
   <td colname="col2"> <p>In AP, the url and template testing rules are added to the mbox entry contraint, for example target-global-mbox, where they are evaluated only once. Once a user qualifies for a campaign the mbox level targeting rules are not re-evaluated. However the targeting audience is added to location targeting rules.</p> <p><b>Solution:</b> Add the necessary template rules as the input-audience of the campaign. Audience evaluation happens upon each request/call. </p> <p>This will be fixed in an upcoming release.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Any metric dependent on conversion metric never converts.</p> </td> 
   <td colname="col2"> <p>This is expected.</p> <p>In an AP activity, once a conversion metric (whether optimization goal or post goal) is converted, the user is released from the experience and the activity is restarted.</p> <p>For example, there is an activity with a conversion metric (C1) and an additional metric (A1). A1 is dependent on C1. When a visitor enters the activity for the first time, and the criteria for converting A1 and C1 are not converted, metric A1 is not converted due to the success metric dependency. If the visitor converts C1 and then converts A1, A1 is still not converted because as soon as C1 is converted, the visitor is released.</p> </td> 
  </tr> 
 </tbody> 
</table>

