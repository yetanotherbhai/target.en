---
description: You can target on any of several categories. Each category functions as a tab that enables you to create targeting rules (or groups) for each category. target/c_target_rules.xml
keywords: visitor profile;target visitor profile
seo-description: You can target on any of several categories. Each category functions as a tab that enables you to create targeting rules (or groups) for each category. target/c_target_rules.xml
seo-title: Categories for Audiences
solution: Target
subtopic: Multivariate Test
title: Categories for Audiences
topic: Premium
uuid: 2ddd14bc-7593-424b-8f0f-47b351ad0703
index: y
internal: n
snippet: y
translate: y
---

# Categories for Audiences

## Categories for Audiences {#concept_E3A77E42F1644503A829B5107B20880D}You can target on any of several categories. Each category functions as a tab that enables you to create targeting rules (or groups) for each category. 
<draft-comment otherprops="merge">
  target/c_target_rules.xml 
</draft-comment>When a particular category is selected, you can apply one or more targeting conditions. For example, in the Geo category, define a rule like City=San Francisco. Adding multiple values creates an OR condition. The visitor has to match only one of the values to meet the targeting condition. For AND conditions on the same parameter, create a custom expression target. 

After you have created a rule, click ** [!UICONTROL  Save] **. A summary of the rule displays next to the targeting link for the level you are targeting. 

You can further refine a rule by adding more conditions or by creating additional rules in other categories. For example, to target only Firefox users from San Francisco who accessed your site from Google, set the [!UICONTROL  Geo] category to target users from San Francisco, the [!UICONTROL  Visitor Behavior] category to Firefox, and the [!UICONTROL  Traffic Sources] category to Google. All of the rules created across categories are combined with "AND." To create complex targeting rules that include "OR" operations across categories, create an expression target. 

You can also target custom profile parameters and ` user.` parameters. When adding an audience, click ** [!UICONTROL  Visitor Profile] **, then under [!UICONTROL  Custom User Parameters] or [!UICONTROL  Custom Profile Parameters] in the [!UICONTROL  Visitor Profile] drop-down list, choose the parameter you use want to use to target your activity. If the desired parameter does not appear, the parameter has not been fired by an mbox. Other custom mbox parameters are available in the [!UICONTROL  Custom Parameters] drop-down list. 

Use the search box to search your [!UICONTROL  Audiences] list. You can search for any part of an audience name, or you can enclose a specific string in quotes. 

You can sort the Audience list by audience name or by the date when it was last modified. 

You can create targeting rules for each of the following categories: 


* Browser 

* Custom Parameters 

* Geo 

* Network 

* Mobile 

* Operating System 

* Site Pages 

* Target Library 

* Time Frame 

* Traffic Sources 

* Visitor Profile 


>## Browser {#concept_925EAD7A8A42431395F9792AC7C3F76B}You can target users who use a specific browser or specific browser options when they visit your page. 
<draft-comment otherprops="merge">
  target/c_browser.xml 
</draft-comment>The following browsers can be targeted: 



<table id="table_71E18114B6E2469C836D9A8067BFA811"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Chrome </p> </td> 
   <td colname="col2"> <p>Microsoft Edge </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Firefox </p> </td> 
   <td colname="col2"> <p>Opera </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Safari </p> </td> 
   <td colname="col2"> <p>iPad </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Internet Explorer </p> </td> 
   <td colname="col2"> <p>iPhone </p> </td> 
  </tr> 
 </tbody> 
</table>

There are two ways to target browsers: 

* **Pre-built Audience: **Use the pre-built audience if you want to target only visitors who use a specific browser to visit your site. For example, if you are offering a Chrome extension, you would target only Chrome users. 


    1. When setting up your activity, select the browser from the audience drop-down list. This option targets the activity only to visitors who use the specified browser. 



* **Customized Browser Audience Rule: **A customized audience enables you to target multiple browsers, or to set up rules or exclusions for specific browsers, browser versions, or browser languages. This provides significant flexibility when targeting a campaign based on browser attributes. 


    1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

    1. Name the audience. 

    1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Browser] **. 

       ![](../graphics/target_browser.png) 

    1. Click ** [!UICONTROL  Select] **, then select one of the following options: 

    
        * **Type:** Target or exclude a certain browser. See [ Type ](c_target_rules.md#section_6ADC758F23F145B3A310151546D83D56). 

        * **Language:** Target or exclude a certain browsers that are set to use specific languages. See [ Language ](c_target_rules.md#section_7520D1AA464A45A6843EABE2D2B431A1). 

        * **Version:** Target or exclude certain browser versions. See [ Version ](c_target_rules.md#section_37CC8CE45DA04E8682AE6388321BA6EF). 



    1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

    1. Click ** [!UICONTROL  Save] **. 



The following example shows an audience that includes Internet Explorer users on versions 10 or 11: 

![](../graphics/target_exclude_ie.png) 
>## Browser Options {#concept_221D8EEF53CC45AEACEB17CF336A3658}Target or exclude activity entrants based on their browser type, language, or version. 
<keyword> 
 <draft-comment otherprops="merge">
   target/c_browser_options.xml 
 </draft-comment> 
</keyword>
## Type {#section_6ADC758F23F145B3A310151546D83D56}

Target or exclude a certain browser. 

Select ** [!UICONTROL  Type] **, then choose either equals or does not equal. 


* Equals: Target the selected browsers.
* Does not equal: Exclude the selected browsers.


Select one or more browsers. 

Multiple options are connected with an OR. 

## Language {#section_7520D1AA464A45A6843EABE2D2B431A1}

Target or exclude a certain browsers that are set to use specific languages. 

For example, if an offer is only available in English, you might target browsers with their language set to English. Or, if your page is not double-byte enabled, you might exclude browsers set to East Asian languages. 

Including or excluding browser language can provide more accurate visitor targeting than targeting based on geography in cases where language is more important than location. For example, if you are offering an article written in English, you could either target English-speaking countries, or you could target browsers that are set to English. Targeting to the browser makes the article available to English speakers in countries where English is not the primary language. 

Select ** [!UICONTROL  Language] **, then choose either equals or does not equal. 
* Equals: Target the selected browser languages.
* Does not equal: Exclude the selected browser languages.


Select one or more languages. 

The following browser languages can be targeted or excluded: 


* English
* French
* German
* Japanese
* Korean
* Portuguese
* Russian
* Spanish
* Traditional Chinese


Multiple options are connected with an OR. 

## Version {#section_37CC8CE45DA04E8682AE6388321BA6EF}

Target or exclude certain browser versions. 

For example, if your page does not appear correctly in Internet Explorer version 11 or earlier, you can create an audience that excludes those versions. In that case, you would set up a rule where the browser type equals Internet Explorer and add a second rule where the version is less than or equal to 11. 

Select ** [!UICONTROL  Version] **, then choose an operator: 


* Equals
* Does not equal
* Is greater than
* Is greater than or equal to
* Is less than
* Is less than or equal to


Type the version number. 

Only major versions can be entered in the text field. The specified version includes any minor version of that release. For example, if you specify version 10, visitors on version 10.1 are included. 

Multiple options are connected with an OR. 
>## Custom Parameters {#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B}Custom parameters are mbox parameters. If you pass any mbox parameters to mboxes, or use the targetPageParams function, those parameters appear here for use in audiences. 
<draft-comment otherprops="merge">
  target/c_custom_parameters.xml 
</draft-comment>For more information, see [ Passing Parameters to a Global Mbox ](https://marketing.adobe.com/resources/help/en_US/target/ov/c_pass_parameters_to_global_mbox.html). 
>## Geo {#concept_5B4D99DE685348FB877929EE0F942670}Target users based on their geographical location, including their country, state/province, city, zip/postal code, DMA, or mobile carrier. 
<draft-comment otherprops="merge">
  target/c_geo.xm 
</draft-comment>Geo location parameters allow you to target activities and experiences based on your visitors' geography. You can include or exclude visitors based on their country, state/province, city, zip/postal code, DMA, or mobile carrier. This data is sent with each mbox request and is based on the visitor's IP address. Select these parameters just like any targeting values. 

## Create an Audience with Geo Targeting {#section_49CBFFAAC8694C4AAD3DE4B2DB7B05DE}


1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Geo] **. 

   ![](../graphics/target_geo.png) 

1. Click ** [!UICONTROL  Select] **, then select one of the following options: 


    * Country
    * State
    * City
    * Zip Code
    * Latitude
    * Longitude
    * DMA
    * Mobile Carrier


   A visitor's IP address is passed with an mbox request, once per visit (session), to resolve geo targeting parameters for that visitor. 

   For Mobile Carrier, [!DNL  Target] uses the IP address registration data (who owns the block of IP addresses) to determine the appropriate mobile carrier using [ Mobile Country Codes (MCC) and Mobile Network Codes MNC) ](http://www.mcc-mnc.com). 

1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

1. Click ** [!UICONTROL  Save] **. 



## Accuracy {#section_D63D5FFCB49C42F9933AFD0BD7C79DF1}

The accuracy of geo targeting depends on several factors. WiFi connections are more accurate than cellular networks. When the visitor is using a cellular data connection, the accuracy of the geo-lookup can be affected by location, the provider's data relationship with deviceatlas, and other factors. Cell tower-based network connections might be less accurate than wired or WiFi connections. Also, a visitor's IP address might be mapped to his or her ISP location, which might not be the same as the visitor's actual location. Some mobile geo-location issues can be solved using the [ HTML 5 Geo location API ](http://diveintohtml5.info/geolocation.html). 

The following table shows the accuracy of IP-based geographical information from [ DigitalEnvoy ](http://www.digitalelement.com/solutions/) for wired or WiFi Internet connections. DigitalEnvoy provides the most accurate data in the industry. Global accuracy is more than 99.9 percent at the country level and is up to 97 percent accurate at a city level. Accuracy information does not apply to cell tower-based networks. 



<table id="table_9F4BD43BF51A400E81D43876D4310820"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Country </th> 
   <th colname="col2" class="entry"> State </th> 
   <th colname="col3" class="entry"> City </th> 
   <th colname="col4" class="entry"> Region </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>US </p> </td> 
   <td colname="col2"> <p>99.99% </p> </td> 
   <td colname="col3"> <p>96% </p> </td> 
   <td colname="col4"> <p>94% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Canada </p> </td> 
   <td colname="col2"> <p>99.99% </p> </td> 
   <td colname="col3"> <p>96% </p> </td> 
   <td colname="col4"> <p>94% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe </p> </td> 
   <td colname="col2"> <p>99.99% </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>UK </p> </td> 
   <td colname="col2"> <p>99.99% </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>87% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Germany </p> </td> 
   <td colname="col2"> <p>99.99% </p> </td> 
   <td colname="col3"> <p>95% </p> </td> 
   <td colname="col4"> <p>93% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scandinavia </p> </td> 
   <td colname="col2"> <p>99% </p> </td> 
   <td colname="col3"> <p>Low 90s </p> </td> 
   <td colname="col4"> <p>Mid 80s </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Spain </p> </td> 
   <td colname="col2"> <p>99.99% </p> </td> 
   <td colname="col3"> <p>Around 90% </p> </td> 
   <td colname="col4"> <p>Mid to high 90s </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Asia </p> </td> 
   <td colname="col2"> <p>99% </p> </td> 
   <td colname="col3"> <p>Mid 90s </p> </td> 
   <td colname="col4"> <p>Low 90s </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan </p> </td> 
   <td colname="col2"> <p>99.99% </p> </td> 
   <td colname="col3"> <p>Mid 90s </p> </td> 
   <td colname="col4"> <p>Low 90s </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Australia </p> </td> 
   <td colname="col2"> <p>99.99% </p> </td> 
   <td colname="col3"> <p>94% </p> </td> 
   <td colname="col4"> <p>91% </p> </td> 
  </tr> 
 </tbody> 
</table>


## Using Geo-Targeting in Profile Scripts {#section_92C93138542C4A94997E3F4BE3F5DA28}

You can use geo information for profile scripts. 

For example, use: 


* ` profile.geolocation.country`
* ` profile.geolocation.state`
* ` profile.geolocation.city`
* ` profile.geolocation.zip`
* ` profile.geolocation.dma`
* ` profile.geolocation.domainName`
* ` profile.geolocation.ispName`
* ` profile.geolocation.connectionSpeed`
* ` profile.geolocation.mobileCarrier`


So, you can write a target expression called "From North America" with the following code: 

` return profile.geolocation.country == 'united states' || profile.geolocation.country == 'canada' || profile.geolocation.country == 'mexico';` 

## Using Geo-Targeting Values as Tokens {#section_E7F7FDF62C3B4934A6565D04B24655F6}

You can now use ` profile.geolocation` values directly as tokens in offers, plugins, and so forth. 

For example, use: 


* ` ${profile.geolocation.country}`
* ` ${profile.geolocation.state}`
* ` ${profile.geolocation.city}`
* ` ${profile.geolocation.zip}`
* ` ${profile.geolocation.dma}`
* ` ${profile.geolocation.domainName}`
* ` ${profile.geolocation.ispName}`
* ` ${profile.geolocation.connectionSpeed}`
* ` ${profile.geolocation.mobileCarrier}`
* ` ${profile.geolocation.latitude}`
* ` ${profile.geolocation.longitude}`


## Geotargeting FAQ {#section_DD308A53AF0F48FA8C81423580561FE7}

**How do I specify latitude and longitude?** 


* The value for latitude/longitude should be a numeric value in degrees. 

* The value for latitude/longitude can have a maximum precision of five decimal places. 

* The value for latitude should be between -90 and 90. 

* The value for longitude should be between -180 and 180. 



** How does geo targeting work for mobile devices? ** 

The vast majority of mobile device users access content via WiFi, which means Target's IP-based geo targeting is as accurate as on a desktop. Cell tower-based connections might be less accurate because the visitor's IP address is based on the tower where the signal is being picked up. Some mobile geo-location issues can be solved using the [ HTML 5 Geo location API ](http://diveintohtml5.info/geolocation.html). 

** How does geo feature handle visitors from AOL? ** 

Due to the way AOL proxies its traffic, we can only target them at a country level. For example, a campaign targeted to France will successfully target AOL users in France. But a campaign targeted to Paris will not successfully target AOL users in Paris. If your intent is to specifically target AOL users, you can set the region field to "aol." In fact, you can target US AOL users by specifying two targeting conditions: country exactly matches "united states" and region exactly matches "aol." 

** What location granularity does geo targeting provide? ** 


* Country - global
* State/province/region - global
* City - global
* Zip/postal code - US, Germany, Canada
* DMA/ITV (UK) - US, UK
* Mobile carrier - global


** How can I test my campaigns as if I'm a user coming from a different location?** 

You can override your IP address with an IP address from a different location and use the ` mboxOverride.browserIp url` parameter. So if your company is in the UK, but your global campaign targets visitors in Aukland, New Zealand, use this style of URL assuming that ` 60.234.0.39` is an IP address in Auckland: 

` http://www.mycompany.com?mboxOverride.browserIp=60.234.0.39` 

You'll need to clear your cookies before doing this. 
>## Network {#concept_3673F0FAA4374047BA656248C9CE7C1B}You can create audiences based on network details. 
<draft-comment otherprops="merge">
  target/c_network.xml 
</draft-comment>
1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Network] **. 

   ![](../graphics/target_network.png) 

1. Click ** [!UICONTROL  Select] **, then select one of the following options: 


    * **ISP: **An ISP is an organization that provides internet access to its subscribers, usually at a monthly or yearly fee. Many ISPs provide additional services, such as web hosting or email. The ISP field is either a commercial ISP (such as Comcast or TimeWarner) or another entity such as a business or educational institution. 

      The following are some examples of popular ISPs in the United States: 



      |  Popular Name  | ISP Name  | Domain Name  | Sample IP Address  |
      |---|---|---|---|
      |  Cablevision  | Cablevision Systems Corp.  | *.optonline.net  | 68.196.130.239  |
      |  CenturyLink  | Qwest Communications Company, LLC  | *.centurylink.net  | 64.40.65.0  |
      |  Charter Communications  | Charter Communications  | *.charter.com  | 71.85.225.124  |
      |  Comcast  | Comcast Cable Communications, Inc.  | *.comcast.net  | 76.27.24.28  |
      |  Cox  | Cox Communications Inc.  | *cox.net  | 68.224.174.22  |
      |  Speakeasy  | MegaPath Corporation  | *.speakeasy.net  | 66.93.240.0  |
      |  Time Warner  | Time Warner Cable Internet LLC  | *.res.rr.com  | 72.229.28.185  |
      |  Verizon FiOS  | MCI Communications Services, Inc. d/b/a Verizon Business  | *.fios.verizon.net  | 173.68.112.34  |
      |  Vivint  | Smartrove Inc.  | *.vivintwireless.net  | 170.72.26.105  |
      |  AT&amp;amp;T Wireless  | AT  | *.mycingular.net  |  |
      |  Sprint mobile  | Sprint Personal Communications Systems  | ip address  |  |
      |  T-Mobile  | T-Mobile USA, Inc.  | ip address  | 208.54.86.0  |
      |  Verizon Wireless  | Cellco Parternship DBA Verizon Wireless  | *.myvzw.com  | 70.195.74.199  |


      >[!NOTE]
      >
      >When targeting based on ISP, use the ISP name, not the popular name.


      If you'd like to see more ISPs referenced in this table, please contact Customer Care with your suggestion. 

      You can test the ISP and domain name values. [ http://www.whoismyisp.org ](http://www.whoismyisp.org) is a good resource for targeting purposes. You can use the sample IP addresses given in the table above, or enter your own. Then use the ` themboxOverride.browserIp= URL` parameter to mimic that IP address. 

    * **Domain Name: **This is the domain name for the visitor's IP address. This is not the domain name of the website you are using with [!DNL  Target]. This domain name is related to the visitor's IP address and is sometimes called a hostname. It is usually very similar to the ISP name. Sometimes the hostname references older names of companies that have rebranded their ISP name but not the domain name. 

    * **Connection Speed: **This is the speed of the visitor's connection to the internet. Options include: broadband, cable, dialup, mobile, oc3, oc12, satellite, t1, t2, and wireless, and xdsl. This field is based on the type of connection and not the actual speed itself. [!DNL  Target] cannot determine the exact connection speeds of connections. The Broadband connection type is used when there is no indication of other connection types so a specific type cannot be chosen. 



1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

1. Click ** [!UICONTROL  Save] **. 


>## Mobile {#concept_2A794199DC1A4D349FFFBC7DCF1FEB89}Target mobile devices based on parameters such as mobile device, type of device, device vendor, screen dimensions (by pixels), and more. 
<draft-comment otherprops="merge">
  target/c_mobile.xml 
</draft-comment>For example, you might want to show different content to users who enter your page from a phone than you would if they visit from a computer. In that case, you could select the Mobile audience, then select the ** [!UICONTROL  Is Mobile Phone] ** option, then add any specific details that are important to you, such as the type of phone, size of the screen (in pixels), and so on. 

Mobile targeting is delivered by [ DeviceAtlas ](https://deviceatlas.com/device-data/user-agent-tester), a service of DotMobi. DeviceAtlas is a comprehensive database of mobile devices built on data compiled from numerous sources, including manufacturers and network operators. This data is then verified, cross-referenced, and validated to build a large and accurate mobile device database available. 


>[!NOTE]
>
>Device detection is accomplished by analyzing User-Agent strings. Some device manufacturers, such as Apple, disable this functionality by not providing enough information in the UA. For example, Apple devices don’t share device model-specific tokens in the UA. The result is that it is not possible to detect iPhone models (such as iPhone 5S, iPhone SE, iPhone 6, and so forth) using a simple keyword-based method. For more information and possible methods to work around this issue, see[ How DeviceAtlas Detects iPhone Models ](https://deviceatlas.com/blog/how-deviceatlas-detects-iphone-models) in the DeviceAtlas documentation. 



You can choose more than one mobile device parameter. Multiple selections are joined with an OR. 

"displayWidth" is the name of the attribute you can use in profile scripts. The value is a number. 


1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Mobile] **. 

   ![](../graphics/target_mobile.png) 

1. Click ** [!UICONTROL  Select] **, then select one of the following options: 


    * Device Marketing Name
    * Device Model
    * Device Vendor
    * Is Mobile Device
    * Is Mobile Phone
    * Is Tablet
    * OS
    * Screen Height (px)
    * Screen Width (px)



   >[!NOTE]
   >
   >You can target by mobile device carrier using the[ Geo settings ](c_target_rules.md#concept_5B4D99DE685348FB877929EE0F942670). 


1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

1. Click ** [!UICONTROL  Save] **. 


>## Operating System {#concept_F5B4EE486E734DC19482103EEC359EEF}You can target visitors who use a certain operating system. 
<draft-comment otherprops="merge">
  target/c_operating_system.xml 
</draft-comment>
1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Operating System] **. 

   ![](../graphics/target_os.png) 

1. Click ** [!UICONTROL  Select] **, then select one of the following options: 

    * Linux
    * Macintosh
    * Windows

1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

1. Click ** [!UICONTROL  Save] **. 


>## Site Pages {#concept_6425D5304568490899E8340CC94798A9}Target visitors who are on a specific page or have a specific mbox parameter. 
<draft-comment otherprops="merge">
  target/c_site_pages.xml 
</draft-comment>
>[!NOTE]
>
>Audience site page types and comparison operators now match types and comparison operators in Target Classic. You can also create site page audiences using you own "user defined query parameter" or "user defined header."




1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Site Pages] **. 

   ![](../graphics/target_site_pages.png) 

1. Click ** [!UICONTROL  Select] **, then select one of the following options: 


    * ** Current Page: **The page the user is currently on, which is the page that contains an mbox in the activity. If you target at the activity level, this could be a page with an mbox that you are using to define entry conditions, or a page that displays content. If you are targeting by experience, then the current page is the page that the display mbox is on. For Success metric or conversion targeting, then it is the page that those mboxes are on. 

    * **Previous Page: **The page the user was on before clicking to the current page. (The user has to click from the previous page to the current page for the page to be tracked. The previous page is not tracked if the user types a new URL in the browser.) The actual content of this page depends on the design of your site. For example, if the current page displays information about a specific product, the previous page might be a category page where the visitor selects the specific item (such as a page displaying several cameras of a certain type), or it might be the home page that leads to the final page. 

    * ** Landing Page: **The landing page is the first page the visitor sees when accessing your site. For example, if the visitor clicks a link on Google that leads to a category page, then the category page is the landing page. If the link leads to your home page, then the home page is the landing page. The landing page is remembered for the visitor's session. You can target deeper in the site based on what the visitor's landing page was in this session. 


      >[!NOTE]
      >
      >The ` landing.url` object is reset on a subdomain change or direct URL replacement. 


    * ** Mbox: **The mbox you are targeting on. For example, if you want to count orders with an order total of $100 or more, you would pass ` orderTotal` as an mbox parameter with that targeting specified here. 

    * **Domain: ** The full domain of the page. When specifying a domain, best practice is to use "contains." For example, "Domain equals facebook.com" will not accept m.facebook.com or www.facebook.com. "Domain contains facebook.com" will accept any variant of facebook.com. 

    * **Query: ** The content of the URL after the first question mark (?). For example, the query is shown in bold in the following sample URL: 

      ` foo.html? e0a72cb2a2c7` 



1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

1. Click ** [!UICONTROL  Save] **. 



You can also create site pages audiences using you own "user-defined query parameter" or "user-defined header."

Use a: 


* Query parameter if the rule selected by the user is Current Page, Landing Page, or Previous Page. 

* Header if the rule select by the user is an HTTP header. 



as illustrated below: 

![](../graphics/site pages.png) 
>## Target Library {#concept_D0FD063ECF7543F2A7587AF6A9502E06}Target users based on pre-built targeting rules. 
<draft-comment otherprops="merge">
  target/c_target_library.xml 
</draft-comment>The pre-built audiences in the Target Library category are legacy audiences and exist in other categories. For more information and best practices, see [ Targets and Audiences Frequently Asked Questions ](c_troubleshooting_targets_and_audiences.md#concept_C4EE4B8F4840430CBD798D579A8F208D). 


>[!NOTE]
>
>Target Classic used expression targets to let you create sophisticated targets once and then use them repeatedly in different activities, experiences, and so on. This functionality is not included in Target Standard/Premium. For alternative methods, see "I use Expression Targets" in[ Advanced Feature Considerations ](c_target-transition-classic-to-standard.md#concept_D8DB7801889A464D9197A739F7B185A7). 




1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Target Library] **. 

   ![](../graphics/target_library.png) 

1. Click ** [!UICONTROL  Select] **, then select a pre-built targeting rule. 

   Pre-built targeting rules include, Window Operating System, Tablet Device, Safari Browser, Returning Visitors, Referred from Google, and more. 

   The predefined audience "Tablet Device" already qualifies when the user agent contains one of the following strings (some of which are model numbers of devices. You do not have to create custom targeting rules for these devices. 

   Kindle, Silk, iPad, Sony Tablet, TF101, GT-P1000, GT-P1000R, GT-P1000M, SGH-T849, SHW-M180S, GT-I9000T, BNTV250, and Tablet PC. 

1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

1. Click ** [!UICONTROL  Save] **. 


>## Time Frame {#concept_0FE1E8DACD104F8B870B0BADE3197F0A}You can add start/end dates and times to target users who visit your site during a specific time frame. You can also set 
<wintitle>
  Week and Day Parting 
</wintitle> options to create recurring patterns for audience targeting. 
<draft-comment otherprops="merge">
  target/c_time-frame.xml 
</draft-comment>For example, using the [ combined, ad-hoc audiences feature ](c_audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), you can target low-spenders with specific content during the three days leading up to Black Friday and other content after Black Friday. 


1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Time Frame] **. 

   ![](../graphics/target_timeframe_dialog.png) 

1. Specify the Start and End dates and times for the audience. 

   Leave the start date empty to start targeting according to the activity's schedule. Leave the end date empty to continue targeting until the activity's end date and time. 

   You can also leave both the start or end dates empty. This lets you use the same audience in multiple activities (without making a copy of the audience) while controlling the start and end dates at the activity level. 


   >[!NOTE]
   >
   >Time zone is displayed as GMT +/- NN:NN, where NN:NN is the offset from GMT and reflects the account-level time zone rather than the visitor's time zone. For example, California's time zone would be displayed as GMT +08:00.


1. (Conditional) Click ** [!UICONTROL  Week and Day Parting] ** to set recurring patterns, including days of the weeks and times. 

   ![](../graphics/week and day parting.png) 

   You could use Week and Day Parting options, for example, to display a "Chat Now" option to visitors only during the days and hours that your call center is staffed. 

   Select one or more days of the week, then set the start and end times. Click [!UICONTROL  Add More]to specify additional patterns, as desired. 

1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

   Note that you can repeat Step 5 for each rule, if desired. 

1. Click ** [!UICONTROL  Save] **. 


>## Traffic Sources {#concept_F01A2673272C4455B0F8B90CC2DBD650}Target visitors based on the search engine or landing page that refers them to your site. 
<draft-comment otherprops="merge">
  target/c_traffic_sources.xml 
</draft-comment>For example, you can target based on the visitor's browser, search engine, or the referring landing page. The referring landing page is the page you clicked from to reach the current site this session. (For example, if you click an ad on Google and it leads you to the ` adobe.com` home page, the referring landing page is ` google.com`.) 

You can combine multiple traffic sources to create a complex targeting rule. 


1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Traffic Sources] **. 

   ![](../graphics/target_traffic_source.png) 

1. Click ** [!UICONTROL  Select] **, then select one of the following options: 


    * From Baidu
    * From Bing
    * From Google
    * From Yahoo
    * Referring Landing Page: URL
    * Referring Landing Page: Domain
    * Referring Landing Page: Query


1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

1. Click ** [!UICONTROL  Save] **. 



You can target users who are referred to your site by a specific search engine or from a specific landing page. 
>## Visitor Profile {#concept_E972690B9A4C4372A34229FA37EDA38E}Target visitors who meet specific profile parameters. 
<draft-comment otherprops="merge">
  target/c_visitor_profile.xml 
</draft-comment>
1. In the [!DNL  Target] interface, click ** [!UICONTROL  Audiences] ** > ** [!UICONTROL  Create Audience] **. 

1. Name the audience. 

1. Click ** [!UICONTROL  Add Rule] ** > ** [!UICONTROL  Visitor Profile] **. 

   ![](../graphics/target_visitor_profile.png) 

1. Click ** [!UICONTROL  Select] **, then select one of the following options: 

   Visitor profile parameters are passed via the mbox (profile). You can target either new or returning visitors, or include all users. 


    * New Visitor
    * Returning Visitor
    * In Other Tests
    * Not In Other Tests
    * First Page of Session
    * Not First Page of Session
    * Category Affinity


   When a site visitor logs in mid-session and gets a ` 3rdpartyId`, all previously-loaded profile attributes tied to the ` 3rdPartyId` are immediately available. 

   You can target custom profile parameters and ` user.` parameters. Choose the parameter you use want to use to target your activity. If the desired parameter does not appear, the parameter has not been fired by an mbox. 

1. (Optional) Click ** [!UICONTROL  Add Rule] ** and set up additional rules for the audience. 

1. Click ** [!UICONTROL  Save] **. 


