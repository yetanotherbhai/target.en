---
description: Define a script profile attribute with its associated JavaScript code snippet on the Profile Attributes page.
seo-description: Define a script profile attribute with its associated JavaScript code snippet on the Profile Attributes page.
seo-title: Script Profile Attributes
solution: Target
title: Script Profile Attributes
topic: Advanced
uuid: c66b4754-d41b-4694-ae78-9897b88ca6cc
index: y
internal: n
snippet: y
translate: y
---

# Script Profile Attributes

Profile scripts run profile attribute "catchers" on each mbox request. When an mbox request is received, Target determines which campaign should run and displays content that is appropriate to that campaign and that experience, tracks the success of the campaign, and runs any relevant profile scripts. This enables you to track information about the visit, such as the visitor's location, time of day, number of times that visitor has been to the site, if they've purchased before and so on. This information is then added to the visitor's profile so you can better track that visitor's activity on your site.
To see a list of your profile scripts, click ** ` Audiences` ** > ** ` Profile Scripts` **. 

1. Click ` Segments` > ` Profiles`.
1. Click ` Create Attribute for Every Mbox` or ` Create Profile Attribute`. The ` Create Profile Attribute` dialog box opens. 

1. Select ` Every Mbox` from the ` Type` selector.
1. Type a name for the profile attribute. You can select predefined variables that can be tracked in the script. Select either ` Profile` or ` Mbox` to determine which variables you can select, then select a variable to add to your script. 

1. Type your JavaScript script and a description of what the script is intended to do, then save the attribute. The attribute is added to the ` Customizable Attributes` list. 

1. Turn the attribute ` On` to start collect data.

If an attribute is automatically turned off by the system, an icon appears for that attribute in the ` Collection Status` column. Click on the icon for an explanation of why the attribute has been turned off. 
Script profile attributes have the ` user.` tag inserted before the attribute name. For example: 

```
if(mbox.name == 'Track_Interest') { 
     if(profile.get('model') == "A5" &amp;&amp; profile.get('subcat') == "KS6") { 
          return (user.get('A5KS6')||0)+1; 
     } 
}
```


* Refer to script profile attributes (including itself) in the code with ` user.get('parameterName')`
* Save variables that may be accessed the next time the script is run (on the next mbox request) with ` user.setLocal('variable_name', 'value')`. Reference the variable with ` user.getLocal('variable_name')`. This is useful for situations where you want to reference the date and time of the last request. 

* Parameters and values are case sensitive. Match the case of the parameters and values you will receive during the campaign or test.

* Reference the [ JavaScript Expressions for Targeters and Profile Scripts Cheat Sheet ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf) for more JavaScript syntax.

To add another attribute and profile script, click ` Create Profile Attribute`. 
To add a session-expiry attribute and profile script, click ` Create Session Expiry Attribute`. Session-Expiry profile scripts help you update your site visitor's profile at the end of a session, without the visitor needing to see another mbox. 
**Best Practices** 
The following guidelines are meant to help write simplified profile scripts that are as error-failing-free as possible by writing code that fails gracefully so the scripts are processed without forcing a system-script-halt. These guidelines are a result of best practices that have been proven to run efficiently. These guidelines are to be applied alongside principles and recommendations drawn by the Rhino development community.

1. Set current script value to a local variable in the user script, set a failover to blank string.
1. Validate the local variable by ensuring it is not a blank string.
1. Use string based manipulation functions vs. Regular Expressions.
1. Use limited for loops vs. open ended for or while loops.
1. Do not exceed 1300 characters or 50 loop iterations.
1. Be mindful of not only the script performance, but the combined performance of all scripts as it must be under 5000 executions in total.
1. If all fails, wrap script in a try/catch.
1. JS Rhino engine documentation here: [ http://www.mozilla.org/rhino/doc.html ](http://www.mozilla.org/rhino/doc.html).

>[!MORE_LIKE_THIS] {class="- topic/related-links "}* [ In-Mbox Profile Attributes ](c_Using_In-Mbox_Profile_Parameters.md#concept_D8394323B5EC4E40BADFA03585A1307F)* [ Smart Targeter Profile Attributes ](c_Using_Smart_Targeter_Profile_Parameters.md#concept_C62023564BA94591A7109662E20CEC5D)* [ Profile Exports ](c_Profile_Exports.md#concept_85A8548182E94590BE36FE56B4C019F7)