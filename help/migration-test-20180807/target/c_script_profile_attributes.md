---
description: Define a profile script attribute with its associated JavaScript code snippet.
keywords: Profile script;profile script attributes;profile script best practices
seo-description: Define a profile script attribute with its associated JavaScript code snippet.
seo-title: Profile Script Attributes
solution: Target
title: Profile Script Attributes
topic: Advanced,Standard,Classic
uuid: 8bc12c73-61c7-4779-b650-dcc3f68be246
index: y
internal: n
snippet: y
translate: y
---

# Profile Script Attributes

You can use profile scripts to capture visitor attributes across multiple visits. Profile scripts are code snippets defined within Target using a form of server-side JavaScript. For example, you might use a profile script to capture how frequently a visitor visits your site, and when they last visited.
Profile scripts are not the same as profile parameters. Profile parameters capture information about visitors using the mbox code implementation of Target.
This section contains the following information:

* [ Create Profile Scripts ](c_script_profile_attributes.md#section_CB02F8B97CAF407DA84F7591A7504810)
* [ Target Disables Profile Scripts in Certain Situations ](c_script_profile_attributes.md#section_C0FCB702E60D4576AD1174D39FBBE1A7)
* [ Best Practices ](c_script_profile_attributes.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0)


## Create Profile Scripts {#section_CB02F8B97CAF407DA84F7591A7504810}

Profile scripts are available under the ` Audiences` tab in the ` Target` interface. 
To add a new profile script, click ** ` Create Profile Script` **, then write your script. 
Or
To copy an existing profile script, from the ` Profile Scripts` list, hover over the desired script, then click the ** ` Copy` ** icon (  ![](graphics/icon_copy.png) ). You can then edit the audience to create a similar audience. 
![](../graphics/profile-script.png) 
This video includes information about using and creating profile scripts.

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Profile Scripts </th> 
   <th colname="col3" class="entry"> 8:19 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/m0jH2tIR1XQ/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/m0jH2tIR1XQ/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Explain what a profile script is</li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405">Explain how a profile script is different from a profile parameter</li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Create a simple profile script</li> 
      <li id="li_699D4D5D089A4FB7BA4C5E95337AC34A">Use the Available Token menu to access available options</li> 
      <li id="li_87E7AFFEEC9C42ABB51C279221E17A14">Enable and disable profile scripts</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Profile scripts run profile attribute "catchers" on each location request. When a location request is received, Target determines which activity should run and displays content that is appropriate to that activity and that experience, tracks the success of the activity, and runs any relevant profile scripts. This enables you to track information about the visit, such as the visitor's location, time of day, number of times that visitor has been to the site, if they've purchased before and so on. This information is then added to the visitor's profile so you can better track that visitor's activity on your site.
Profile script attributes have the ` user.` tag inserted before the attribute name. For example: 

```
if(mbox.name == 'Track_Interest') { 
     if(profile.get('model') == "A5" &amp;&amp; profile.get('subcat') == "KS6") { 
          return (user.get('A5KS6')||0)+1; 
     } 
}
```


* Refer to profile script attributes (including itself) in the code with ` user.get('parameterName')`
* Save variables that may be accessed the next time the script is run (on the next mbox request) with ` user.setLocal('variable_name', 'value')`. Reference the variable with ` user.getLocal('variable_name')`. This is useful for situations where you want to reference the date and time of the last request. 

* Parameters and values are case sensitive. Match the case of the parameters and values you will receive during the campaign or test.

* Reference the [ JavaScript Expressions for Targeters and Profile Scripts Cheat Sheet ](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/js_expression_cheat_sheet.pdf) for more JavaScript syntax.


## Target Disables Profile Scripts in Certain Situations {#section_C0FCB702E60D4576AD1174D39FBBE1A7}

` Target` will automatically disable profile scripts in certain situations, such as if they take too long to execute or have too many instructions. 
When a profile script is disabled, a yellow alert icon displays next to the profile script in the Target UI, as illustrated below:
![](graphics/profile script invalid.png) 
On hover, details on the error display, as illustrated below:
![](graphics/profile script hover.png) 
Typical reasons for the system to disable profile scripts include the following:

* An undefined variable to referenced.

* An invalid value is referenced. This is often caused by referencing URL values and other user-inputted data without proper validation.

* Too many JavaScript instructions are used. Target has limit of 2,000 JavaScript instructions per script, but this cannot simply be calculated by manually reading the JavaScript. For example, Rhino treats all function calls and "new" calls as 100 instructions. Also, the size of any entry data, such as URL values, can impact the instructions count.

* Not following items highlighted in the [ best practices ](c_script_profile_attributes.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0) section below. 



## Best Practices {#section_64AFE5D2B0C8408A912FC2A832B3AAE0}

The following guidelines are meant to help write simplified profile scripts that are as error-failing-free as possible by writing code that fails gracefully so the scripts are processed without forcing a system-script-halt. These guidelines are a result of best practices that have been proven to run efficiently. These guidelines are to be applied alongside principles and recommendations drawn by the Rhino development community.

* Set current script value to a local variable in the user script, set a failover to blank string.

* Validate the local variable by ensuring it is not a blank string.

* Use string based manipulation functions vs. Regular Expressions.

* Use limited for loops vs. open ended for or while loops.

* Do not exceed 1,300 characters or 50 loop iterations.

* Do not exceed 2,000 JavaScript instructions. Target has limit of 2,000 JavaScript instructions per script, but this cannot simply be calculated by manually reading the JavaScript. For example, Rhino treats all function calls and "new" calls as 100 instructions. Also, the size of any entry data, such as URL values, can impact the instructions count.

* Be mindful of not only the script performance, but the combined performance of all scripts as it must be under 5000 executions in total.

* If all fails, wrap script in a try/catch.

* See the JS Rhino engine documentation for more information: [ http://www.mozilla.org/rhino/doc.html ](http://www.mozilla.org/rhino/doc.html). 


