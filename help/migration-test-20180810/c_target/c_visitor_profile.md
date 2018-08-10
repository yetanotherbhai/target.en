---
description: Visitor profiles contain information about how your visitors use your pages and other optimized content locations
keywords: variables;profiles;parameters;built in profiles;methods;url variables;geo profiles;third party profiles;mbox variables;campaign variables;customer attributes
seo-description: Visitor profiles contain information about how your visitors use your pages and other optimized content locations
seo-title: Visitor Profiles
solution: Target
subtopic: Getting Started
title: Visitor Profiles
topic: Standard
uuid: 3ae71904-b8a5-4626-8607-e32100c6f2fd
index: y
internal: n
snippet: y
translate: y
---

# Visitor Profiles

## Visitor Profiles {#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1}Visitor profiles contain information about how your visitors use your pages and other optimized content locationsIf your Target is used together with other Adobe Marketing Suite solutions, such as Adobe Analytics, Marketing Cloud Audiences shares visitor information across solutions. 

By default, Target profile information is stored in a single first-party cookie. The configuration can easily be changed to serve third-party cookies as well. 
>## Visitor Profile Lifetime {#concept_D9F21B416F1F49159F03036BA2DD54FD}By default, visitor profiles are stored for 14 days. This profile lifetime can be extended. 
<draft-comment otherprops="merge">
  ov/c_visitor_profile-mig.xml 
</draft-comment>[ Contact Client Care or your Adobe consultant ](r_release_notes.md#reference_ACA3391A00EF467B87930A450050077C) to extend the profile lifetime at no additional cost. The lifetime can be set to as many as 90 days. 

The [!DNL  Target] JavaScript library you are using ( [!DNL  mbox.js] or [!DNL  at.js]) determines whether or not you need to download a new file: 



<table id="table_2BD28C564EE44016A2B241DB7205F1DE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Target Library </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>mbox.js </p> </td> 
   <td colname="col2"> <p>If your profile is extended beyond the 14-day default, you must download a new <span class="filepath"> mbox.js </span> file after your consultant or Client Care changes your settings. The cookie extension to support the changed profile lifetime is included in the updated <span class="filepath"> mbox.js </span> file. After you start using the new library, your visitors' profile lifetimes will update. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>You do not need to download a new <span class="filepath"> at.js </span> file if your profile is extended beyond the default. </p> </td> 
  </tr> 
 </tbody> 
</table>

The expiration date is not reset for existing profiles. If a previous visitor does not return for 15 days, that profile expires. If a previous visitor returns before the original two-week profile expires, the profile is reset to the extended lifetime. All new visitor profiles are set to the extended profile lifetime. 

If you have two sites under one client code and a visitor visits both sites, the profile is set to the lifetime of profiles on whichever site was visited last. For example, if Site 1 has an 84-day profile lifetime and Site 2 has a 14-day lifetime, and the visitors visits Site 1 and then Site 2, that visitor's profile will expire in14 days. If the visitor visits Site 1 after visiting Site 2, the profile will expire in 84 days. 
>## Profile Attributes {#concept_01A30B4762D64CD5946B3AA38DC8A201}Profile attributes are parameters that are specific to the visitor. These attributes are stored in the visitor's profile to provide information about the visitor that can be used in your campaigns. 
<draft-comment otherprops="merge">
  target/c_profile_parameters.xml 
</draft-comment>As the visitor browses, or when the visitor returns for another session, the saved profile attributes can be used to target content, or log information for segment filtering. 

To set up profile attributes, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Profile Scripts.] ** 

The following types of profile attributes are available: 



<table id="table_B82609FE1EC84FB194189F4FE07B0884"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter Type </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Mbox </p> </td> 
   <td colname="col2"> <p>Passed in directly through page code when creating the mbox. See <a href="../ov/c_understanding-global-mbox.xml#concept_33362A04146C4E3C8E7089B65F38B5E5" format="dita" scope="local"> Passing Parameters to a Global Mbox </a>. </p> <p> <p>Note:  <span class="keyword"> Target </span> has a limit of 50 unique profile attributes per mbox call. If you need to pass more than 50 profile attributes to <span class="keyword"> Target </span>, you can pass them using the <span class="wintitle"> Profile Update </span> API method. For more information, see <a href="https://www.adobe.io/apis/marketingcloud/target/docs/reference/profiles/profile-update.html" format="html" scope="external"> Profile Update </a> in the Adobe Target API documentation. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Script </p> </td> 
   <td colname="col2"> <p>Defined directly with a JavaScript code snippet. These can store running totals like total money spent by consumer and are executed on each mbox request. See <a href="c_visitor_profile.xml#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Script Profile Attributes </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>


>[!NOTE]
>
>[!DNL  Target] has a limit of 50 unique profile attributes per mbox call. If you need to pass more than 50 profile attributes to [!DNL  Target], you can pass them using the [!UICONTROL  Profile Update] API method. For more information, see [ Profile Update ](https://www.adobe.io/apis/marketingcloud/target/docs/reference/profiles/profile-update.html) in the Adobe Target API documentation. 


>## Profile Script Attributes {#concept_8C07AEAB0A144FECA8B4FEB091AED4D2}Define a profile script attribute with its associated JavaScript code snippet. 
<draft-comment otherprops="merge">
  target/c_script_profile_attributes.xml 
</draft-comment>You can use profile scripts to capture visitor attributes across multiple visits. Profile scripts are code snippets defined within Target using a form of server-side JavaScript. For example, you might use a profile script to capture how frequently a visitor visits your site, and when they last visited. 

Profile scripts are not the same as profile parameters. Profile parameters capture information about visitors using the mbox code implementation of Target. 

## Create Profile Scripts {#section_CB02F8B97CAF407DA84F7591A7504810}

Profile scripts are available under the [!UICONTROL  Audiences] tab in the [!DNL  Target] interface. 

To add a new profile script, click ** [!UICONTROL  Create Profile Script] **, then write your script. 

Or 

To copy an existing profile script, from the [!UICONTROL  Profile Scripts] list, hover over the desired script, then click the ** [!UICONTROL  Copy] ** icon (  ![](../target/graphics/icon_copy.png) ). You can then edit the audience to create a similar audience. 

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
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Explain what a profile script is </li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405">Explain how a profile script is different from a profile parameter </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Create a simple profile script </li> 
      <li id="li_699D4D5D089A4FB7BA4C5E95337AC34A">Use the Available Token menu to access available options </li> 
      <li id="li_87E7AFFEEC9C42ABB51C279221E17A14">Enable and disable profile scripts </li> 
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

[!DNL  Target] will automatically disable profile scripts in certain situations, such as if they take too long to execute or have too many instructions. 

When a profile script is disabled, a yellow alert icon displays next to the profile script in the Target UI, as illustrated below: 

![](../target/graphics/profile script invalid.png) 

On hover, details on the error display, as illustrated below: 

![](../target/graphics/profile script hover.png) 

Typical reasons for the system to disable profile scripts include the following: 


* An undefined variable to referenced. 

* An invalid value is referenced. This is often caused by referencing URL values and other user-inputted data without proper validation. 

* Too many JavaScript instructions are used. Target has limit of 2,000 JavaScript instructions per script, but this cannot simply be calculated by manually reading the JavaScript. For example, Rhino treats all function calls and "new" calls as 100 instructions. Also, the size of any entry data, such as URL values, can impact the instructions count. 

* Not following items highlighted in the [ best practices ](c_visitor_profile.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0) section below. 



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


>## Category Affinity {#concept_75EC1E1123014448B8B92AD16B2D72CC}The category affinity feature automatically captures the categories a user visits and then calculates the user's affinity for the category so it can be targeted and segmented on. This helps to ensure that content is targeted to visitors who are most likely to act on that information. 
<draft-comment otherprops="merge">
  target/c_category_affinity.xml 
</draft-comment>
## Passing Category Affinity Information into Target {#section_B0C8E46EEBAC4549AD90352A47787D04}

Whenever a user visits your site, profile parameters specific to the visitor are recorded in the [!DNL  Target] database. This data is tied to the user's cookie. One particularly useful parameter is ` categoryId`, an mbox parameter assigned on a product page. As the visitor continues to browse, or returns for another session, the categories of products a particular user views can be recorded. You can also record category information by passing it as the mbox parameter ` user.categoryId` in any mbox (including a nested mbox), as a URL parameter ` user.categoryId`, or in Target page parameters with a global mbox. See your account representative for more details. 

Separate categories with a comma to create separate categories. For example: 


* ` categoryId=clothing,​shoes,​nike,​running,​shox,​nike shox turbo,​nike shox turbo VI`
* ` entity.categoryId=clothing,​shoes,​nike,​running,​shox,​nike shox turbo,​nike shox turbo VI`


Based on the frequency and recency of visits to your product categories, the category affinity (if any) a user has is recorded. Category affinity can be used to target populations for your activities. 

You can use ` user.categoryAffinities[]` in a profile script to return an array of the affinities that a visitor has populated. 

## Business Case for Category Affinity {#section_D6FF913E88E6486B8FBCE117CA8B253B}

A visitor's activity in one session, such as which category he or she views the most often, can be used for targeting in subsequent visits. Each category page a visitor views during a session is captured, and his or her "favorite" category is calculated based on a recency and frequency model. Then, every time the visitor returns to the home page, the hero image area can be targeted to show content related to that user's favorite category. 

## Example of Using Category Affinity {#section_A4AC0CA550924CB4875F4F4047554C18}

Suppose you sell musical instruments online and want to target sales promotions on bass guitars to visitors who have already expressed interest in guitars in the past. Using category affinity, you can create offers that display only to visitors with this category affinity. 

## Category Affinity Algorithm {#section_8B86C7FF50294208866ABF16F07D5EB9}

The category affinity algorithm works as follows: 


* 10 points for first view
* 5 points for every one after
* At end of session divide all values by 2


For example, viewing categoryA then categoryB in one session results in A: 10, B: 5. When the session ends, you will have A: 5, B: 2.5. If you view the same items in the next session, the values change to A: 15 B: 7.5. 
>## Use Category Affinity for Targeting {#concept_5750C9E6C97A40F8B062A5C16F2B5FFC}Information to help you use a 
<wintitle>
  Category Affinity 
</wintitle> audience for targeting in an activity. 
<draft-comment otherprops="merge">
  target/use-category-affinity-for-targeted-group 
</draft-comment>
## Create an Audience to Use Category Affinity {#section_A27C600BBA664FE7A74F8FE076B78F40}


1. From the ** [!UICONTROL  Audiences] ** list, click ** [!UICONTROL  + Create Audience] **. 

   Or 

   To copy an existing audience, from the Audiences list, hover over the desired audience, then click the Copy icon (  ![](../graphics/icon_copy.png) ). You can then edit the audience to create a similar audience. 

1. Type a descriptive audience name. 

1. Click ** [!UICONTROL  + Add Rule] ** > ** [!UICONTROL  Visitor Profile] **. 

1. From the ** [!UICONTROL  Visitor Profile] ** drop-down list, select ** [!UICONTROL  Category Affinity] **. 

   ![](../target/graphics/affinity.png) 

1. Select the desired category: 


    * Favorite Category
    * First Category
    * Second Category
    * Third Category
    * Fourth Category
    * Fifth Category


1. Chose the Evaluator: 


    * Contains (case insensitive)
    * Does Not Contain (case insensitive)
    * Equals


1. Specify each new value in a separate line (for example, "shoes"). 

1. Click ** [!UICONTROL  Save] **. 



## Use the Category Affinity Audience in an Activity {#section_91526B942D1B4AEBB8FCDF4EBFF931CF}

You can use Category Affinity audiences in any activity. During the three-step guided workflow, on the Target step, choose the desired audience. 
>## Privacy {#concept_639482A343DB4963A6144378E1D8D7F0}Adobe Target has enabled processes and settings that allow you to use Target in compliance with applicable data privacy laws. 
<draft-comment otherprops="merge">
  ov/c_privacy.xml 
</draft-comment>
## Collection of IP Address {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

The IP address of a visitor to your website is transmitted to an Adobe Data Processing Center (DPC) where the IP address may be stored. Depending on the network configuration for the visitor, the IP address does not necessarily represent the IP address of the visitor’s computer. For example, the IP address could be the external IP address of a Network Address Translation (NAT) firewall, HTTP proxy, or Internet gateway. 

## Replacement of Last Octet of the IP Address {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe has developed a new “privacy by design” setting that can be enabled by Adobe Client Care for Adobe Target. When this setting is enabled, the last octet (the last portion) of the IP address is immediately hidden when the IP address is collected by Adobe. This anonymization is performed prior to any processing of the IP address, including before an optional geo-lookup of the IP address. 

When this feature is enabled, the IP address is made sufficiently anonymous so it is no longer identifiable as personal information. As a result, Adobe Target can be used in compliance with data privacy laws in countries that do not permit the collection of personal information. Obtaining city-level information will likely be significantly impacted by the obfuscation of the IP address. Obtaining region- and country-level information should only be slightly impacted. 

Contact Adobe Client Care to enable the IP obfuscation feature. 

## GeoSegmentation {#section_BB69F96559BD44BDA4177537C4A5345A}

If you enable the replacement of the last octet of the IP address, the remaining values of the IP address can be analyzed using reports in Adobe Target. If the last octet of the IP address has not been obfuscated, then the full IP address can be analyzed in Adobe Target. You can use the GeoSegmentation feature to map out visitor location by geographic area. GeoSegmentation data is granular only to the city level or zip code level, and not to the individual level. 

## Opt-Out Link {#section_E7A62B7B99C94B3A806CB262D16E27FC}

You can add an opt-out link to your sites to enable visitors to opt-out of all counting and content delivery. 

1. Add the following link to your site: ` &amp;lt;a href="http://clientcode.tt.omtrdc.net/optout"&amp;gt; Your Opt Out Language Here&amp;lt;/a&amp;gt;` 

1. Replace the ` clientcode` text with your client code, and add the text or image to be linked to the opt-out URL.
Any visitor who clicks this link is not included in any mbox requests called from their browsing sessions until they delete their cookies, or for two years, whichever comes first. This works by setting a cookie for the visitor called ` disableClient` in the ` clientcode.tt.omtrdc.net` domain. 

Even if you use a first-party cookie implementation, the provided opt-out is set via a 3rd-party cookie. If the client is using a first-party cookie only, Target checks whether an opt-out cookie is set. 
>## Customer Attributes {#concept_16C5C434D32D4EB1AD44A71821F3DEE8}Information about using enterprise customer data from a customer relationship management (CRM) databases for content targeting in 
<keyword>
  Adobe Target 
</keyword> by using Customer Attributes in the Adobe Profiles & Audiences core service. 
<draft-comment otherprops="merge">
  target/c_working-with-customer-attributes.xml 
</draft-comment>Enterprise customer data collected through multiple sources and stored inside a CRM database can be used in [!DNL  Target] to strategically deliver the most relevant content to customers, specifically focusing on returning customers. The [!DNL  People] core service (formerly Profiles and Audiences) brings together data collection and analysis with testing and optimization, making data and insights actionable. 

## Customer Attributes Overview {#section_B4099971FA4B48598294C56EAE86B45A}

The People core service is part of the [!DNL  Adobe Experience Cloud] and provides enterprises a tool to push their customer data to the [!DNL  Experience Cloud] platform. Data onboarded to the [!DNL  Experience Cloud] is available for all [!DNL  Experience Cloud] workflows. [!DNL  Adobe Target] utilizes this data for targeting returning customer based on attributes. [!DNL  Adobe Analytics] consumes these attributes and they can be used for analysis and segmentation. 

![](../graphics/crs.png) 

Consider the following information as your work with customer attributes and Target: 


* There are some prerequisite requirements that you must meet before you can use the [!UICONTROL  Customer Attributes] feature in the [!DNL  People] core service. For more information, see "Prerequisites for Uploading Customer Attributes" in [ Customer Attributes ](https://marketing.adobe.com/resources/help/en_US/mcloud/attributes.html) in the *Marketing Cloud and Core Services Product Documentation*. Note that [!DNL  at.js] (any version) or [!DNL  mbox.js] version 58 or later is required. 

* Adobe does not guarantee that 100% of customer attribute (visitor profile) data from CRM databases will be onboarded to the Experience Cloud and thus be available for use for targeting in Target. In our current design, there is a possibility that a small percentage of data might not be onboarded. 

* The lifetime of customer attributes data imported from the Experience Cloud to Target depends on the lifetime of the visitor profile, which is 14 days by default. For more information, see [ Visitor Profile Lifetime ](c_target_rules.md#concept_D9F21B416F1F49159F03036BA2DD54FD). 

* If the ` vst.*` parameters are the only thing identifying the user, the existing "authenticated" profile will not be fetched as long as ` authState` is UNAUTHENTICATED (0). The profile will only come into play if ` authState` is changed to UNAUTHENTICATED (1). 

  For example, if the ` vst.myDataSource.id` parameter is used to identify the user (where ` myDataSource` is the data source alias) and there is no MCID or third-party ID, using the parameter ` vst.myDataSource.authState=0` won't fetch the profile that might have been created through a CRS import. If the desired behavior is to fetch the authenticated profile, the ` vst.myDataSource.authState` has to have the value of 1 (AUTHENTICATED). 



## Customer Attribute Workflow for Target {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Complete the following steps to use CRM data in [!DNL  Target], as illustrated below: 

![](../graphics/crm workflow.png) 

Detailed instructions for completing each of the following tasks can be found in [ Create a Customer Attribute Source and Upload the Data File ](https://marketing.adobe.com/resources/help/en_US/mcloud/t_crs_usecase.html) in the *Marketing Cloud and Core Services Product Documentation*. 


1. Create a data file. 

   Export customer data from your CRM to CSV format to create a [!DNL  .csv] file. Alternately, a zip or gzip file can be created for uploading. Ensure that first row of CSV is the header and all rows (customer data) have the same number of entries. 

   ![](../graphics/CRS_sample.png) 

   ![](../graphics/CRS_CSV_sample.png) 

1. Create the attribute source and upload the data file. 

   Specify a Name and Description of the data source and the alias Id. The alias Id is a unique ID to be used in your Customer Attribute code in VisitorAPI.js. 

   Data files up to 100 MB can be uploaded using the HTTP method. Files larger than 100 MB, up to 4 GB can be uploaded through FTP. 


    * **HTTP: **You can drag-and-drop the [!DNL  .csv] data file or click [!UICONTROL  Browse] to upload from your file system. 

    * **FTP: **Click on FTP link to [ upload file through FTP ](https://marketing.adobe.com/resources/help/en_US/mcloud/t_upload_attributes_ftp.html). First step is to provide a password for the Adobe-provided FTP server. Enter the password, then click [!UICONTROL  Done]. 

      Now transfer your CSV/ZIP/GZIP file to the FTP server. Once this file transfer is successful, create a new file with same name and [!DNL  .fin] extension. Transfer this empty file to the server. This indicates a End Of Transfer and the Experience Cloud starts to process data file. 



1. Validate the schema. 

   The validation process lets you map display names and descriptions to uploaded attributes (strings, integers, numbers, and so on). Map each attribute to its correct data type, display name, and description. 

   Click [!UICONTROL  Save] after schema validation is complete. The file upload time varies depending on the size. 

   ![](../graphics/SchemaValidate.png) 

   ![](../graphics/upload1.png) 

1. Configure subscriptions and activate the attribute source. 

   Click ** [!UICONTROL  Add Subscription] **, then select the solution to subscribe these attributes. [ Configuring a subscription ](https://marketing.adobe.com/resources/help/en_US/mcloud/subscription.html) sets up the data flow between the Experience Cloud and solutions. Activating the attribute source allows the data to flow to subscribed solutions. The customer records you have uploaded are matched up with incoming ID signals from your website or application. 

   ![](../graphics/solution.png.jpeg) 

   ![](../graphics/activate.PNG) 

   While performing this step, be aware of the following limitations: 


    * The maximum file size for each upload using the HTTP method is 100 MB. 

    * The maximum file size for each upload using the FTP method is 4 GB. 

    * The number of attributes allowed to subscribe: 5 for [!DNL  Target Standard] and 200 for [!DNL  Target Premium]. 





## Use Customer Attributes in Target {#section_107E3A0F0EC7478E82E6DBD17B30B756}

You can use customer attributes in [!DNL  Target] in the following ways: 



<table id="table_96AB5A9C2F17437489DF4C42642EB6D3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Method </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Creating targeting audiences </p> </td> 
   <td colname="col2"> <p>In <span class="keyword"> Target </span>, you can select a customer attribute from the <span class="wintitle"> Visitor Profile </span> section when creating an audience. All customer attributes have the prefix &lt; <span class="varname"> data_source_name </span>&gt; in the list. Combine these attributes as required with other data attributes to build audiences. </p> <p style="text-align: center;"> <img href="../graphics/TargetAudience.png" id="image_00473D9BBCE843DAB2C1736FE52CB3DE" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Creating profile scripts using tokens </p> </td> 
   <td colname="col2"> <p>Customer attributes can be referenced in profile scripts using format <span class="codeph"> crs.get('&amp;lt;Datasource Name&amp;gt;.&amp;lt;Attribute name&amp;gt;') </span>. </p> <p>This profile script can be used directly in offers for delivering attributes that belong to the current visitor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Using <span class="codeph"> mbox3rdPartyID </span> in your website for a successful implementation and usage </p> </td> 
   <td colname="col2"> <p>Pass <span class="codeph"> mbox3rdPartyId </span> as a parameter to the global mbox inside the <span class="codeph"> targetPageParams() </span> method. The value of <span class="codeph"> mbox3rdPartyId </span> should be set to the customer ID that was present in CSV data file. </p> 
    <codeblock>
      &lt;script&nbsp;type="text/javascript"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;function&nbsp;targetPageParams()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;'mbox3rdPartyId=2000578'; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
     &lt;/script&gt; 
    </codeblock> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Using the Marketing Cloud ID Service </p> </td> 
   <td colname="col2"> <p>If you are using the Marketing Cloud ID service, you need to set a Customer ID and Authentication State to use customer attributes in targeting. For more information, see <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html" format="html" scope="external"> Customer IDs and Authentication State </a> in the <i>Marketing Cloud ID Service Documentation</i>. </p> </td> 
  </tr> 
 </tbody> 
</table>

For more information about using customer attributes in [!DNL  Target], see the following resources: 


* [ Create a Customer Attribute Source and Upload the Data File ](https://marketing.adobe.com/resources/help/en_US/mcloud/t_crs_usecase.html) in the *Marketing Cloud and Core Services Product Documentation* 

* [ Customer Attributes: The More You Know, The Better You Connect ](https://blogs.adobe.com/digitalmarketing/analytics/customer-attributes-know-better-connect/) in the *Digital Marketing Blog* 



## Issues Frequently Encountered by Customers {#section_BE0F70E563F64294B17087DE2BC1E74C}

You might encounter the following issues when working with customer attributes and [!DNL  Target]: 



<table id="table_4635ECDB7D1A4023A889A9CEC639B360"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Issue </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Customer attributes are removed because the profile is too large </p> </td> 
   <td colname="col2"> <p>There is no character limit on a particular field in the user's profile, but if the profile gets larger than 64K, it is truncated by removing the oldest attributes until the profile is below 64K again. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attributes not listing in the Audience Library in <span class="keyword"> Target </span>, even after several days </p> </td> 
   <td colname="col2"> <p>This is usually a Pipeline connection problem. As a resolution, ask your CRS team to republish the feed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Delivery not working based on the attribute </p> </td> 
   <td colname="col2"> <p>The profile has not been updated on the edge yet. As a resolution, ask your CRS team to republish the feed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Implementation issues </p> </td> 
   <td colname="col2"> <p>Be aware of the following implementation issues: </p> <p> 
     <ul id="ul_5CCB01F625D94208AC7F7B57E38DB0A6"> 
      <li id="li_2D2106650BC444328DF526BEB0C69690"> <p>The Visitor Id was not passed correctly. The ID was passed in <span class="codeph"> mboxMCGVID </span> instead of <span class="codeph"> setCustomerId </span>. </p> </li> 
      <li id="li_7B7A1F2F47E641718A8D5C203DF871BB"> <p>The Visitor Id was passed correctly, but the AUTHENTICATION state was not set to Authenticated. </p> </li> 
      <li id="li_C0A232B444274463988DDF977BC651FB"> <p> <span class="codeph"> mbox3rdPartyId </span> was not passed correctly. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxUpdate </span> not performed properly </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> mboxUpdate </span> was not performed properly with <span class="codeph"> mbox3rdPartyId </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Customer attributes are not being imported into Target. </p> </td> 
   <td colname="col2"> <p>If you cannot find CRS data in Target, ensure that the import occurred within the last <i>x</i> days where <i>x</i> is the Target <a href="c_visitor_profile.xml#concept_D9F21B416F1F49159F03036BA2DD54FD" format="dita" scope="local"> Visitor Profile Lifetime </a> value (14 days by default). </p> </td> 
  </tr> 
 </tbody> 
</table>

Issues in rows 1 and 2 above cause approximately 60% of problems in this area. Issues in row 3 cause approximately 30% of problems. The issue in row 4 causes approximately 5% of problems. The remaining 5% are due to miscellaneous issues. 

## Video: Upload Offline Data using Customer Attributes {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}


<table id="table_52A3C5F82C54466C9EFAD428436E1DF5"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Upload Offline Data using Customer Attributes </th> 
   <th colname="col3" class="entry"> 6:52 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://video.tv.adobe.com/v/17802t1/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://video.tv.adobe.com/v/17802t1/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_E5C5B35CE4304853B2A4AA6BE215D1BB"> 
      <li id="li_242B238F71F7494E87CF60426BA6D6DB">Import offline CRM, help desk, point-of-sale, and other marketing data into the Experience Cloud People service and associate it with visitors using their known IDs. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Real-Time Profile Syncing for mbox3rdPartyID {#concept_BF4113593F614987B1D3E359AE1C5732}The mbox3rdPartyID is your company's visitor ID, such as the membership ID for your company's loyalty program. 
<draft-comment otherprops="merge">
  target/c_3rd-party_id.xml 
</draft-comment>When a visitor logs in to a company's site, the company typically creates an ID that is tied to the visitor's account, loyalty card, membership number, or other applicable identifiers for that company. 

When a visitor accesses a page on which Target is enabled, that visitor is assigned a Target PCID. If the visitor then logs in, and the implementation passes the mbox3rdPartyID to Target, Target connects that visitor's mbox3rdPartyID with the Target PCID. 

Every three to five minutes, updates are synced with the database. When the visitor logs out, the merged data replaces the previous data associated with the mbox3rdPartyID, creating a more complete record of that visitor's actions. If the same attribute exists in both IDs--for example, the PCID has category=hats and the mbox3rdPartyID has category=skis, or if the visitor saw experience A before logging in, but experience B is stored in the mbox3rdPartyID--the attribute stored in the mbox3rdPartyID overwrites the attribute from the PCID. If the visitor was in one activity or experience before logging in, but a different activity and experience are stored in the mbox3rdPartyID, after logging in that visitor is placed into the mbox3rdPartyID activity and experience. 



|  PCID (Not Logged In)  | mbox3rdPartyID (Logged In)  | Merged and Saved to mbox3rdPartyID  |
|---|---|---|
|  category=hats  | category=skis  | category=skis  |
|   | store=94103  | store=94103  |
|  Activity 1, Experience A  | Activity 1, Experience B  | Activity 1, Experience B  |
|  Activity 1  |  | Activity 1  |

When the visitor logs out, the merged profile is maintained. 
>## Profile and Variable Glossary {#reference_F5D9EF735F1044C38E208F3A178903B2}This page lists profiles, variables, and parameters that are useful in profile scripts. 
<draft-comment otherprops="merge">
  target/r_variables_profiles_parameters_methods.xml 
</draft-comment>
## Built-In Profiles {#section_2B694370003C4F8E8E29E0B2F6E52045}



<table id="table_8F26DFF396244388A98F3CD0E776FF44"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Profile </th> 
   <th colname="col2" class="entry"> Notes </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.activeActivities </span> </p> <p> <span class="codeph"> user.activeCampaigns </span> </p> </td> 
   <td colname="col2"> <p>Return the campaign ID for all campaigns/activities that the user is in, even if he or she has not interacted with the campaign/activity in the current session. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.pcId </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.sessionId </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.categoryAffinity </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.categoryAffinities </span> </p> </td> 
   <td colname="col2"> <p> Return an array of the affinities that a visitor has populated </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.isFirstSession </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.isNewSession </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.daysSinceLastVisit </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.browser </span> </p> </td> 
   <td colname="col2"> <p>The user agent </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header </span> </p> </td> 
   <td colname="col2"> <p>All <span class="codeph"> user.header </span> profiles are built-in from mbox request header data </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('x-cluster-client-ip') </span> </p> </td> 
   <td colname="col2"> <p>The public-facing IP address of the network connection that the visitor is on. </p> <p>You can get this in several ways, for example <span class="filepath"> whatismyip.com </span>. The IP address is not the NAT address (internal address), starting with 10., 192.168., or 172. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('host') </span> </p> </td> 
   <td colname="col2"> <p>Website hostname </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('cookie') </span> </p> </td> 
   <td colname="col2"> <p>Visitor cookie data </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('user-agent') </span> </p> </td> 
   <td colname="col2"> <p>Visitor browser user-agent </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('accept-language') </span> </p> </td> 
   <td colname="col2"> <p>Visitor language </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('accept-encoding') </span> </p> </td> 
   <td colname="col2"> <p>Visitor character encoding </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('accept') </span> </p> </td> 
   <td colname="col2"> <p>Visitor language and character encoding </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('connection') </span> </p> </td> 
   <td colname="col2"> <p>Server connection. For example: <span class="codeph"> keep-live </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.header('referer') </span> </p> </td> 
   <td colname="col2"> <p>Website URL of visitor current page. Does not work for Internet Explorer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.getLocal('param_name','value'); </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.setLocal('param_name','value'); </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.get('param_name') </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user.parameter </span> </p> </td> 
   <td colname="col2"> <p> Persistent profile attributes created from profile scripts. Also references “system” profiles like geolocation, visit count, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> profile.get('param_name') </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> profile.param('param_name'); </span> </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> profile.parameter('parameter_name'); </span> </p> </td> 
   <td colname="col2"> <p>Mbox parameters that are made persistent due to their <span class="codeph"> profile. </span> prefix. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> profile.browserTime </span> </p> </td> 
   <td colname="col2"> <p>The visitor's local browser time. For system time, create a new date object in the profile script </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> profile.averageDaysBetweenVisits </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> profile.sessionCount </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameter= </span> </p> </td> 
   <td colname="col2"> <p>Generic term for additional values passed with an mbox, usually as name/value pairs. Not persistent unless made so with <span class="codeph"> profile.parameter </span> or <span class="codeph"> user.parameter </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## URL Variables {#section_8F25958273164EBAA6DC659302993FD3}



|  ` landing`  | ` referrer`  | ` page`  |
|---|---|---|
|  ` landing.url`  | ` referrer.url`  | ` page.url`  |
|  ` landing.domain`  | ` referrer.domain`  | ` page.domain`  |
|  ` landing.protocol`  | ` referrer.protocol`  | ` page.protocol`  |
|  ` landing.param`  | ` referrer.param`  | ` page.param`  |
|  ` landing.query`  | ` referrer.query`  | ` page.query`  |


## Geo and Mobile Carrier Profiles {#section_08441DA42E7346918FBB345818854997}


* ` profile.geolocation.country`
* ` profile.geolocation.state`
* ` profile.geolocation.city`
* ` profile.geolocation.zip`
* ` profile.geolocation.dma`
* ` profile.geolocation.domainName`
* ` profile.geolocation.ispName`
* ` profile.geolocation.connectionSpeed`
* ` profile.geolocation.mobileCarrier`
* ` profile.geolocation.latitude`
* ` profile.geolocation.longitude`


## Mbox Variables {#section_C42F0D33BD8044BE812FA0B7905CC0ED}



<table id="table_1AC13D7874F942349086851980DD5606"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variable </th> 
   <th colname="col2" class="entry"> Notes </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.name </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.param('param_name') </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameters automatically passed with every request: </p> <p> 
     <ul id="ul_67A44986D47745E886A9F0FEDD65832B"> 
      <li id="li_CCBFA7DB2C5F4B0988C59B7B7DB68F5F"> <span class="codeph"> mbox.param('browserHeight') </span> </li> 
      <li id="li_594E67B2FDB1448AA6D3FF769DE3D857"> <span class="codeph"> mbox.param('browserTimeOffset') </span> </li> 
      <li id="li_A935E111B83A42CC8E159B1D3562ABB7"> <span class="codeph"> mbox.param('browserWidth') </span> </li> 
      <li id="li_E48FA9B53D384A69B314426C04A84AAA"> <span class="codeph"> mbox.param('colorDepth') </span> </li> 
      <li id="li_FE70A416B6BC46FAAB7CC7A360C38399"> <span class="codeph"> mbox.param('mboxXDomain') </span> </li> 
      <li id="li_8CEB7C8B2F7B455DA5DF175EAB14BC9F"> <span class="codeph"> mbox.param('mboxTime') </span> </li> 
      <li id="li_2C43D1FFEA3D43A8A60360C131ED4C66"> <span class="codeph"> mbox.param('screenHeight') </span> </li> 
      <li id="li_9F3C670289A34187BCBAEE2327C1FB54"> <span class="codeph"> mbox.param('screenWidth') </span> </li> 
     </ul> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameters passed with order mboxes: </p> <p> 
     <ul id="ul_51D2BF83365F45F0BA72B9D874B025B6"> 
      <li id="li_1EB644FDDD044AEF9F6A2BED55762090"> <span class="codeph"> mbox.param('orderId') </span> </li> 
      <li id="li_2EC9F67E2E214DDA9F90AE09FA99F7BE"> <span class="codeph"> mbox.param('orderTotal') </span> </li> 
      <li id="li_468EC01B4EF745ACA4FDFE58A297071A"> <span class="codeph"> mbox.param('productPurchasedId') </span> </li> 
     </ul> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox3rdPartyId </span> </p> </td> 
   <td colname="col2"> <p>An mbox parameter to sync a customer ID to Target's mboxPCID. A customer ID is an ID your company uses to track visitors, such as a CRM ID, membership ID, or something similar. This ID can then be used to add information via the Profile APIs and <a href="c_visitor_profile.xml#concept_16C5C434D32D4EB1AD44A71821F3DEE8" format="dita" scope="local"> Customer Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxPageValue </span> </p> </td> 
   <td colname="col2"> <p>In each mbox call the page is assigned a value. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxDebug </span> </p> </td> 
   <td colname="col2"> <p>Only used for debug info. Added to the page url where the <span class="filepath"> mbox.js </span> looks for it. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mboxOverride.browserIp </span> </p> </td> 
   <td colname="col2"> <p>Sets a different geo than the actual location so you can test how something would look in another location. </p> <p> <p>Note:  Using mboxOverride parameters should be used only while testing the activity and not in production. The use of any <span class="codeph"> mboxOverride </span> parameters can cause reporting discrepancies when using <a href="../a4t/a4t.xml#concept_7540C8C04259434AB6EE33B09F47A1DE" format="dita" scope="local"> Analytics for Target </a> (A4T). You should use <a href="../target/c_activities.xml#concept_9329EF33DE7D41CA9815C8115DBC4E40" format="dita" scope="local"> Activity QA mode </a> while testing to ensure that your activity works as expected before pushing the activity into your live environment. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Campaign Variables {#section_74DF5A1F22104775A6C9DCE53AA47A09}


* ` campaign.name`
* ` campaign.id`
* ` campaign.recipe.name`
* ` campaign.recipe.id`
* ` offer.name`
* ` offer.id`


## Customer Attributes {#section_62B4821EB6564FF4A14159A837AD4EDB}

Customer attributes can be referenced in profile scripts, formatted as ` crs.get('< * ` Datasource Name` *>.< * ` Attribute name` *>')`. 

These attributes are also available as tokens in profile scripts and directly in offers without first requiring a profile script. The token should be in the form: ` $crs. * ` datasourceName` *. * ` attributeName` *`. 
