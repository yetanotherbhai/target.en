---
description: This section contains information about how to send entity data into Recommendations. Entities refer to the items you want to recommend. Entities can be anything, such as products, content (such as articles, slide shows, images, movies, and TV shows), job listings, restaurants, and so forth.
keywords: collection;Targeting
seo-description: This section contains information about how to send entity data into Recommendations. Entities refer to the items you want to recommend. Entities can be anything, such as products, content (such as articles, slide shows, images, movies, and TV shows), job listings, restaurants, and so forth.
seo-title: Creating and Updating Entities and Collections in Recommendations
solution: Target
subtopic: Getting Started
title: Creating and Updating Entities and Collections in Recommendations
title_outputclass: premium
topic: Premium
uuid: ea0b1213-96fd-4eea-b8d4-0a9b58d2b37e
badge: asstes/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Creating and Updating Entities and Collections in Recommendations

## Creating and Updating Entities and Collections in Recommendations {#concept_FD935A24D98745FFB2447933FCEB8062}This section contains information about how to send entity data into Recommendations. Entities refer to the items you want to recommend. Entities can be anything, such as products, content (such as articles, slide shows, images, movies, and TV shows), job listings, restaurants, and so forth.Use Entities to: 


* Set up your collections 

* Use feeds to get entity or content information into your recommendations 

* Set exclusions to prevent certain items from displaying in your recommendations 



You can create [ entities ](c_products.md#concept_FD935A24D98745FFB2447933FCEB8062) in Recommendations using the following methods: 


* [ Feeds ](c_products.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3) (the preferred method) 

    * CSV 

    * Google 

    * Adobe Analytics Product Classifications 


* [ Target Web Tags ](c_products.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) 

    * HTTP requests 

    * API requests 


* [ Entities API ](c_products.md#concept_E7DEC48F973A4F78A66938644FC494E4) 


>## Feeds {#concept_1228B31E3D0B483B9DD42C5E2AE436E3}Use feeds to get 
<xref href="c_products.xml#concept_FD935A24D98745FFB2447933FCEB8062" format="dita" scope="local">
  entities 
</xref> imported into Recommendations. Entities can be sent using CSV files, the Google Product Search feed format, and/or Adobe Analytics product classifications. 
<draft-comment otherprops="merge">
  recs/c_feeds.xml 
</draft-comment>Feeds allow you to bypass [ Target Web Tags ](c_products.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) or augmenting your mbox data with information that is either unavailable on the page or is unsafe to send directly from the page, such as margin, COGS, and so on. 

You can select which columns from your Adobe Target product classifications file or Google Product Search file you want to send to the [!DNL  Recommendations] server. These pieces of data about each item can then be used in template display and for controlling recommendations. 

If data is collected by both an entity feed and an mbox, the most recent data wins. Usually, the most recent data comes from an mbox, because it is viewed more often. In the rare event that entity feed data and mbox data hit at the same time, the mbox data is used. 

The [!UICONTROL  Feeds] list ( ** [!UICONTROL  Recommendations] ** > ** [!UICONTROL  Feeds] **) provides information about any feeds you have created. To edit the name of a feed, you must edit the feed itself. When you save with the new name, the feed is refreshed. 


>[!NOTE]
>
>If the [!UICONTROL  Last Updated] feed says "undefined," then the feed is coming in from [!DNL  Recommendations Classic] and cannot be changed from within [!DNL  Target Premium Recommendations]. 



## CSV {#section_65CC1148C7DD448FB213FDF499D35FCA}

You can create a ` .csv` file using the Adobe proprietary CSV upload format. The file contains display information about the reserved and custom attributes for your products. To upload attributes specific to your implementation, replace ` CustomN` in the header row with the name of the attribute you want to use. In the example below, ` entity.Custom1` has been replaced by: ` entity.availability`. You can then bulk upload the file to the [!DNL  Recommendations] server. 

Using the .csv format has the following advantages over the Google Feed format: 


* It doesn't require field mappings. 

* It supports multi-value attributes (see example below). 

* It supports up to 100 custom attributes. If you need more than 100 custom attributes, you can create a second feed file with a different set of custom attributes specified. 



Use the bulk upload method to send display information if you don't have mboxes on your page, or you want to supplement your display information with items that are not available on your site. For example, you might want to send inventory information that might not be published on your site. 

Any data uploaded using the upload template file overwrites that value in our database, so if you send price information in JavaScript and then send different price values in the file, the values in the file override the information sent with JavaScript. 


>[!IMPORTANT]
>
>Do not enclose values in double quotes ( " ) in your [!DNL  .csv] file unless they are intentional. If you enclose values in double quotes you must escape them by enclosing them in another set of double quotes. Double quotes that are not escaped will prevent the recommendations feed from loading properly. 



For example, the following syntax is incorrect: 

` "Apples "Bananas" Grapes"",` 

The following syntax is correct: 

"Apples ""Bananas"" Grapes""", 


>[!NOTE]
>
>You can't overwrite an existing value with a blank value. You have to pass another value in its place to overwrite it. In the case of sale price, a common solution is to either pass in an actual "NULL" or some other message. You can then write a template rule to exclude items with that value.



The product is available in the admin interface approximately two hours after successfully uploading its entity. 

The following is sample code for a .csv file: 


```
## RECSRecommendations Upload File 
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines. 
## RECS 
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left. 
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'. 
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations. 
## RECSentity.id,entity.name,entity.categoryId,entity.message,entity.thumbnailUrl,entity.value,entity.pageUrl,entity.inventory,entity.margin,entity.last_updated_by,entity.multi_english,entity.availability,entity.tax_country,entity.tax_region,entity.tax_rate,entity.product_type,entity.item_group_id,entity.color,entity.size,entity.brand,entity.gtin 
na3456,RipCurl Watch with Titanium Dial,Watches &amp; Sport,Cutting edge titanium with round case,http://example.com/s7/na3456_Viewer,425,http://example.com/shop/en-us/na3456_RipCurl,24,0.25,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Titanium,44mm,RipCurl,"075380 01050 5" 
na3457,RipCurl Watch with Black Dial,Watches &amp; Sport,Cutting edge matte black with round case,http://example.com/s7/na3457_Viewer,275,http://example.com/shop/en-us/na3457_RipCurl,24,0.27,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Black,44mm,RipCurl,"075340 01060 7"
```


## Google {#section_8EFA98B5BC064140B3F74534AA93AFFF}


>[!IMPORTANT]
>
>The Google Product Search feed type uses the Google format. This is different from the Adobe proprietary CSV upload format.



If you have an existing Google product feed, then you can use that as your import file. 


>[!NOTE]
>
>It is not required to use Google data. [!DNL  Recommendations] just uses the same format as Google. You can use this method to upload any data you have, and use the available scheduling features. However, you must retain Google's predefined attribute names when you set up the file. 



Most retailers upload products to Google, so when a visitor uses Google product search, their products will show up. [!DNL  Recommendations] follows Google's specification exactly for entity feeds. Entity feeds can be sent to [!DNL  Recommendations] via [!DNL  .xml], [!DNL  .txt], or [!DNL  .tsv], and can use the [ attributes defined by Google ](https://support.google.com/merchants/answer/188494?hl=en&topic=2473824&ctx=topic#US). The results are searchable on the [ Google shopping pages ](http://www.google.com/prdhp). 


>[!NOTE]
>
>The POST method must be allowed on the server that is hosting the Google feed content.



Because [!DNL  Recommendations] users already configure [!DNL  .xml] or [!DNL  .txt] feeds to send to Google either via URL or FTP, entity feeds accept that product data and use it to build out the recommendations catalog. Specify where that feed exists and the recommendations server retrieves the data. 

If you use Google Product Search for the entity feed upload, you still need to have a product page mbox on the page if you want to show recommendations there or track product views for algorithm delivery based on views. 

Google feeds do not support multiple values for a custom attribute. 

The feed runs at the time you save and activate it. It runs at the time you save the feed, then every day an hour later. 

The following is sample code for a Google Product Search feed .xml file: 


```
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
<feed xmlns="http://www.w3.org/2005/Atom" xmlns:ns2="http://base.google.com/ns/1.0" xmlns:ns3="http://base.google.com/cns/1.0"> 
    <title>Product Feed</title> 
    <link href="http://example.com"/> 
    <updated>2017-12-13T08:45:04.918-08:00</updated> 
    <author> 
        <name>Product Feed Author</name> 
    </author> 
    <id>http://example.com</id> 
    <entry> 
        <title>RipCurl Watch with Titanium Dial</title> 
        <description>Cutting edge Titanium with Round case</description> 
        <ns2:id>na3452</ns2:id> 
        <ns2:link>http://example.com/shop/en-us/na3452_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp;amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 01050 5</ns2:gtin> 
        <ns2:image_link>http://example.com/s7/na3452_Viewer</ns2:image_link> 
        <ns2:mobile_link>http://m.example.com/s7/na3452_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>425</ns2:price> 
        <ns2:product_review_average>5.0</ns2:product_review_average> 
        <ns2:product_review_count>30</ns2:product_review_count> 
        <ns2:product_type>Shop by Category &amp;gt; Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>375</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
    <entry> 
        <title>RipCurl Watch with Black Dial</title> 
        <description>Cutting edge matte black with Round case</description> 
        <ns2:id>na3453</ns2:id> 
        <ns2:link>http://example.com/shop/en-us/na3453_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp;amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 013450 5</ns2:gtin> 
        <ns2:image_link>http://example.com/s7/na3453_Viewer</ns2:image_link> 
        <ns2:mobile_link>http://m.example.com/s7/na3453_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>275</ns2:price> 
        <ns2:product_review_average>4.8</ns2:product_review_average> 
        <ns2:product_review_count>23</ns2:product_review_count> 
        <ns2:product_type>Shop by Category &amp;gt; Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>249</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
</feed> 
  
```


The following is sample code for a Google Product Search feed .tsv file: 


```
id    title    description    link    price    condition    availability    image_link    tax    shipping_weight    shipping    google_product_category    product_type    item_group_id    color    size    gender    age_group    pattern    brand    gtin    mpn 
na3454    RipCurl Watch with Titanium Dial    Cutting edge titanium with round case    http://example.com/shop/en-us/na3454_RipCurl    425    new    in stock    http://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches &amp; Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075380 01050 5    DZ1437 
na3455    RipCurl Watch with Black Dial    Cutting edge matte black with round case    http://example.com/shop/en-us/na3455_RipCurl    275    new    in stock    http://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches &amp; Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075340 01060 7    DZ1446
```


## Analytics Product Classifications {#section_79E430D2C75443BEBC9AA0916A337E0A}

The Analytics Product classification is the only classification available for recommendations. For more information about this classification file, see [ Classifications ](https://marketing.adobe.com/resources/help/en_US/reference/classifications.html) in the *Analytics Help and Reference* guide. It's possible that not all the information you need for recommendations will be available in your current implementation, so follow this user guide if you want to add to your classifications file. 



<table id="table_89809DC66C794DB69B9DB232C7E03B1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <p type="important">Note:  Before importing entity data into Recommendations using Analytics product classifications, be aware that this is not the preferred method. </p> </p> <p>Be aware of the following caveats: </p> <p> 
     <ul id="ul_9B6553CAD5DF4CBD83AC8F833441B1C7"> 
      <li id="li_8FD09B9E450947AEA5079C1DFE43BA9D"> <p> Updates to entity attributes incur an additional delay of up to 24 hours. </p> </li> 
      <li id="li_3024EA7D93AA4D3BA6354CE60DED69ED"> <p> Target supports Product Classifications only. The Analytics product SKU must map to the same level as the Recommendations <span class="codeph"> entity.id </span>. Custom Analytics Classifications can be engineered using Adobe Consulting Services. Please contact your Account Manager with questions. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Create Feed {#task_C6CD9EA905744C2CA0BB8259BB74C867}Create a feed to insert information about your products or services into Recommendations. 
<draft-comment otherprops="merge">
  recs/t_feeds_create.xml 
</draft-comment>
>1. From within the Target interface, click ** [!UICONTROL  Recommendations] ** > ** [!UICONTROL  Feeds] ** > ** [!UICONTROL  Create Feed] **.

>       ![Step Result](graphics/CreateFeed.png) 
>1. Specify a descriptive name for your feed.
>1. Select a ** [!UICONTROL  Source Type] **.

>       For information about Google Product Feed and CSV feed types, see [ Feeds ](c_products.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3). 
>1. Specify a Report Suite, or the URL or FTP location where the feed can be accessed.

>       If you select URL, specify the URL. 

>       If you select FTP, provide the FTP server information, the login credentials, the filename, and the FTP directory. You have the option to use FTP with SSL (FTPS) for more secure uploads. 
>1. Click the ** [!UICONTROL  Next] ** arrow to display the [!UICONTROL  Schedule] options.

>       ![Step Result](graphics/CreateFeedSchedule.png) 
>1. Select an update option:

>    
>    * Daily
>    * Weekly
>    * Biweekly
>    * Never Do not schedule an update. Choose this if you do not want this feed to run. 


>1. Specify the time you want your feed to run.

>       This option is based on the time zone used in your browser. If you want to use a time in a different time zone, you must calculate that time according to your time zone. 
>1. Click the ** [!UICONTROL  Next] ** arrow to display the [!UICONTROL  Mapping] options, then specify how you want to map your data to [!DNL  Target] definitions.

>       ![Step Result](graphics/CreatFeedMapping.png) 
>1. (Optional) If you want the feed to belong to an environment (host group), select the host group.

>       By default the feed belongs to all host groups. This ensures that items in this feed are available in any environment. 


>       >[!NOTE]
>       >
>       >For more information, see[ Hosts ](c_hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E). 

>1. Click ** [!UICONTROL  Save] **.
>## Feed Statuses and Indicators {#concept_7A9AC983AB584BA18A95F3B3E9D4C7D8}Information about the possible feed statuses and their indicators.
## Feed Statuses {#section_5DDC2DECF70A42FDAFF2235E91371537}

The following are possible statuses for a feed: 



<table id="table_0C54CB3B06DA419AB4A83789B09E531F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Status </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Syncing </p> </td> 
   <td colname="col2"> <p>Feed setup details are being saved to <span class="keyword"> Target </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>No Feed Run </p> </td> 
   <td colname="col2"> <p>You have created a feed but it has not been scheduled (frequency is set to Never). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scheduled at <i>date and time</i> </p> </td> 
   <td colname="col2"> <p>The feed has not been run, but is scheduled to run at the specified date and time. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Server Not Found </p> </td> 
   <td colname="col2"> <p>FTP or URL locations are invalid or otherwise unreachable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Waiting to Download </p> </td> 
   <td colname="col2"> <p>The feed is waiting to downloaded to <span class="keyword"> Target </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Preparing to Import </p> </td> 
   <td colname="col2"> <p>The feed is being prepared to import to <span class="keyword"> Target </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flushing Results </p> </td> 
   <td colname="col2"> <p>The results are being flushed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Waiting for Index Queue </p> </td> 
   <td colname="col2"> <p>The feed is in the index queue. </p> <p> <p>Note:  Once the feed status is "Waiting for Index Queue," the newly updated values are available in delivery and criteria processing. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Indexing since <i>date and time</i> </p> </td> 
   <td colname="col2"> <p>The feed is being indexed since the date and time indicated. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Indexed at <i>date and time</i> </p> </td> 
   <td colname="col2"> <p>The feed was successfully indexed at the date and time indicated. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Success </p> </td> 
   <td colname="col2"> <p>The feed was successfully saved to <span class="keyword"> Target </span> at the date and time indicated. </p> </td> 
  </tr> 
 </tbody> 
</table>

To update a feed (for example, to make changes to your feed configuration or feed file), open the feed, make any desired changes, and click ** [!UICONTROL  Save] **. 

## Feed Status Indicators {#section_3C8A236C5CB84C769A9E9E36B8BFABA4}

The following feed status indicators display in the [!UICONTROL  Status] column: 



<table id="table_396F6009016843E19F8F423A06B5B1E6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Status Indicator </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Green status indicator </p> </td> 
   <td colname="col2"> <p>When a feed successfully finishes indexing, a green status dot indicates that the feed is in a successful state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Yellow status indicator </p> </td> 
   <td colname="col2"> <p>When a feed or feed index is delayed by 25% of the feed frequency, a yellow status dot displays. For example, a yellow dot displays for a feed set to run daily if the index hasn't completed six hours after the scheduled time. </p> <p> <p>Note:  Once the feed status is "Waiting for Index Queue," the newly updated values are available in delivery and criteria processing. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>White status indicator </p> </td> 
   <td colname="col2"> <p>When a feed is not scheduled, a white status dot indicates that the feed has not run yet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Red status indicator </p> </td> 
   <td colname="col2"> <p>If the feed fails to upload data to server, a red status indicator is shown. </p> </td> 
  </tr> 
 </tbody> 
</table>

Consider the following examples: 

**Example 1:** 


* Day one: daily feed processes at 9:00 a.m. PST 

* Day two: it is 3:30 p.m. and the feed hasn't run since yesterday at 9:00 a.m. 



The status should be yellow because the index should have run roughly 6.5 hours ago. 6.5 hours +24 is 127% of the feed window. 

**Example 2:** 


* January 1: monthly feed processes at 9:00 a.m. PST 

* February 3: it is 10:00 a.m. and the feed hasn't run for one month, one day, and one hour ago 



The status should be yellow because the index should have run roughly one day and one hour ago. Although this is only (31+(1/25))/30 = 1.03% of frequency setting, it surpassed the maximum of one-day delay. 
>## Target Recommendations Web Tags {#concept_0069C0EFB56C4700BB33F2F35C2B9B17}Information about the various methods you can use to get data into Target Recommendations. Methods include entity parameters, in-page profile attributes, script profile attributes, the bulk profile update API, the single profile update API, and Customer Attributes.The following methods are available: 



<table id="table_40E09663B889424BA8E6D4D607FE241B"> 
 <tbody> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Entity parameters (also called "mbox parameters")</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Entity parameters are name/value pairs passed in directly through page code that define or update the Recommendations catalog data. </p> <p>Page parameters are useful to send additional page data to Target that does not need to be stored with the visitor's profile for future targeting use. These values are instead used to describe the page or the action the user took on the specific page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>Page parameters are passed into Target via a server call as a string name/value pair. Parameter names and values are customizable (although there are some "reserved names" for specific uses). </p> <p>Examples: </p> <p>page=productPage </p> <p>categoryId=homeLoans </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Product pages: Send information about the specific product viewed (this is how Recommendations works) </p> <p>Order details: Send order ID, orderTotal, and so forth for order collection </p> <p>Category affinity: Send category-viewed information to Target to build knowledge of the user's affinity to particular site categories </p> <p>3rd-party data: Send information from 3rd-party data sources, such as weather targeting providers, account data (for example, DemandBase), demographic data (for example Experian), and more. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>Data gets sent to Target in real-time, and can be used on the same server call the data on which it comes in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Requires page code update (directly or via a tag management system). </p> <p>If the data needs to be used for targeting on a subsequent page/server call, it needs to be translated to a profile script. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p> <span class="codeph"> targetPageParamsAll </span> (appends the parameters to all mbox calls on the page): </p> 
    <codeblock>
      function&nbsp;targetPageParamsAll()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;"param1=value1&amp;param2=value2&amp;p3=hello%20world"; 
     } 
    </codeblock> <p> <span class="codeph"> targetPageParams </span> (appends the parameters to the global mbox on the page): </p> 
    <codeblock>
      function&nbsp;targetPageParams()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;"param1=value1&amp;param2=value2&amp;p3=hello%20world"; 
     } 
    </codeblock> <p>Parameters in mboxCreate code: </p> 
    <codeblock>
      &lt;div&nbsp;class="mboxDefault"&gt; 
     &nbsp;&nbsp;default&nbsp;content&nbsp;to&nbsp;replace&nbsp;by&nbsp;offer 
     &lt;/div&gt; 
     &lt;script&gt; 
     &nbsp;&nbsp;mboxCreate('mboxName','param1=value1','param2=value2'); 
     &lt;/script&gt; 
    </codeblock> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p>Recommendations: <a href="../recs/c_recommendations.xml#reference_DE38BB07BD3C4511B176CDAB45E126FC" format="dita" scope="local"> Implementation According to Page Type </a> </p> <p>Order confirmation: <a href="c_target-atjs-implementation.xml#task_E85D2F64FEB84201A594F2288FABF053" format="dita" scope="local"> Create an Order Confirmation mbox - at.js </a> </p> <p>Category affinity: <a href="../ov/c_visitor_profile.xml#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local"> Category Affinity </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>In-page profile attributes (also called "in-mbox profile attributes)</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>In-page profile attributes are name/value pairs passed directly through page code that are stored in the visitor's profile for future use. </p> <p>In-page profile attributes allow user-specific data to be stored in Target's profile for later targeting and segmentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>In-page profile attributes are passed into Target via a server call as a string name/value pair with the prefix "profile." before the Attribute name. </p> <p>Attribute names and values are customizable (although there are some "reserved names" for specific uses). </p> <p>Examples: </p> <p> <span class="codeph"> profile.membershipLevel=silver </span> </p> <p> <span class="codeph"> profile.visitCount=3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Login information: Share non-PII (Personally Identifiable Information) data to Target based on the user's login. This could be membership status, order history, or more. </p> <p>Store info: Track which store is this user's preferred location. </p> <p>Previous interactions: Track what the user has done on the site previously to inform future personalization. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>Data gets sent to Target in real-time, and can be used on the same server call on which the data comes in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Requires page code updates (directly or via a tag management system). </p> <p>Attributes and values are visible in server calls, so a visitor can see the values. If sharing information such as credit ranges or other potentially private information, this might not be the best approach. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p> <span class="codeph"> targetPageParamsAll </span> (appends the attributes to all mbox calls on the page): </p> 
    <codeblock>
      function&nbsp;targetPageParamsAll()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;"profile.param1=value1&amp;profile.param2=value2&amp;profile.p3=hello%20world"; 
     } 
    </codeblock> <p> <span class="codeph"> targetPageParams </span> (appends the attributes to the global mbox on the page): </p> 
    <codeblock>
      function&nbsp;targetPageParams()&nbsp;{ 
     &nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;profile.param1=value1&amp;profile.param2=value2&amp;profile.p3=hello%20world"; 
     } 
    </codeblock> <p>Attributes in mboxCreate code: </p> 
    <codeblock>
      &lt;div&nbsp;class="mboxDefault"&gt; 
     &nbsp;&nbsp;default&nbsp;content&nbsp;to&nbsp;replace&nbsp;by&nbsp;offer 
     &lt;/div&gt; 
     &lt;script&gt; 
     &nbsp;&nbsp;mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); 
     &lt;/script&gt; 
    </codeblock> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p> <a href="../ov/c_visitor_profile.xml#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profile Attributes </a> </p> <p> <a href="../ov/c_visitor_profile.xml#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1" format="dita" scope="local"> Visitor Profiles </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Script profile attributes</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Script profile attributes are name/value pairs defined in the Target solution. The value is determined from executing a JavaScript snippet on Target's server per server call. </p> <p>Users write small code snippets that execute per mbox call, and before a visitor is evaluated for audience and activity membership. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>Script profile attributes are created in the Audiences section of Target. Any attribute name is valid, and the value is the result of a JavaScript function written by the Target user. The attribute name is automatically prefixed by " <span class="codeph"> user. </span>" in Target to distinguish them from in-page profile attributes. </p> <p>The code snippet is written in the Rhino JS language and can reference tokens and other values. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Cart Abandonment: When the visitor reaches the shopping cart, set the profile script to 1. When the visitor converts, reset it to 0. If the value =1, then the visitor has an item in the cart. </p> <p>Visit Count: On every new visit, increment the count by 1 to keep track of how often a visitor returns to the site. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>Requires no page code updates. </p> <p>Executes before audience and activity membership decisions, so these profile script attributes can affect membership on a single server call. </p> <p>Can be very robust. As many as 2,000 instructions can be executed per script. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Requires JavaScript knowledge. </p> <p>The execution order of profile scripts cannot be guaranteed, so they cannot rely on each other. </p> <p>Can be difficult to debug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p>Profile scripts are quite flexible: </p> 
    <codeblock>
      user.purchase_recency: 
     var&nbsp;dayInMillis&nbsp;=&nbsp;3600&nbsp;*&nbsp;24&nbsp;*&nbsp;1000; 
     if&nbsp;(mbox.name&nbsp;==&nbsp;'orderThankyouPage')&nbsp;{ 
     &nbsp;user.setLocal('lastPurchaseTime',&nbsp;new&nbsp;Date().getTime()); 
     } 
     var&nbsp;lastPurchaseTime&nbsp;=&nbsp;user.getLocal('lastPurchaseTime'); 
     if&nbsp;(lastPurchaseTime)&nbsp;{ 
     &nbsp;return&nbsp;((new&nbsp;Date()).getTime()-lastPurchaseTime)/dayInMillis; 
     } 
    </codeblock> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p> <a href="../ov/c_visitor_profile.xml#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profile Script Attributes </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Bulk profile update API</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Via API, send a .csv file to Target with visitor profile updates for many visitors. Each visitor profile can be updated with multiple in-page profile attributes in one call. </p> <p>This option is very similar to Customer Attributes with a few differences: </p> <p> 
     <ul id="ul_75EFDFD9534541E3BBB1A99228E5D0A2"> 
      <li id="li_2F36B7D3580D4AB7983A0EEBBEAD43F4"> <p>Customer Attributes use an FTP upload while the Target Bulk Profile Update API uses an HTTP POST API. </p> </li> 
      <li id="li_C1CB5D8CDB0C4F18AC08D3E506FFB38E"> <p>Customer Attributes data can be shared with Analytics. Bulk Profile Update is useable only in Target. </p> </li> 
      <li id="li_7AE2B90224C54ECE88BE807E2011141D"> <p>Customer Attributes support creating a profile for a user Target has not yet seen. The Bulk Profile Update API updates existing Target profiles only. </p> </li> 
      <li id="li_B7DDD5613526421CBA901B10E2DDAC2E"> <p>Customer Attributes require the use of the Experience Cloud ID (ECID). The Bulk Profile Update API requires either the TNT ID or the <span class="codeph"> mbox3rdPartyId </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>The .csv file must refer to each visitor via his or her Target PCID or <span class="codeph"> mboxThirdPartyId </span>. The Experience Cloud ID (ECID) is not supported. All profile attributes/values are created and updated via the API. Format details are available in the API documentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Your CRM or other internal system stores valuable data about your visitors that you want to consistently update into Target, without exposing the profile data in your page implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>No limit on the number of profile attributes. </p> <p>Profile attributes sent via the site can be updated via the API and vice versa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>The size of the batch file must be less than 50 MB. In addition, the total number of rows should not exceed 500,000 rows per upload. </p> <p>There is no limit on the number or rows you can upload over a period of 24 hours in subsequent batches. However, the ingestion process might be throttled during business hours to ensure that other processes run efficiently. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p>See <a href="http://developers.adobetarget.com/api/#updating-profiles" format="http" scope="external"> Updating Profiles </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p> <a href="http://developers.adobetarget.com/api/#updating-profiles" format="http" scope="external"> Updating Profiles </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Single profile update API</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Almost identical to the Bulk Profile Update API, but one visitor profile is updated at a time, in line in the API call instead of with a .csv file </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>The visitor must be identified via the Target <span class="codeph"> mboxPC </span> value or <span class="codeph"> mboxThirdPartyId </span> value. The Experience Cloud ID (ECID) is not supported. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>You want to update Target in real-time when a visitor performs some offline action, such as reaching a call center, a loan is funded, using a loyalty card in store, accessing a kiosk, and so forth. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>No limit on the number of profile attributes. </p> <p>Profile attributes sent via the site can be updated via the API and vice versa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Limit of 1,000,000 API calls (1 million) per 24-hour period </p> <p> Updates profiles only. Cannot create a profile for a potential user Target has yet to see. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p>GET and POST supported. 
     <codeblock>
       https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&amp;amp;profile.attr1=0&amp;amp;profile.attr2=1... 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <p> <a href="http://developers.adobetarget.com/api/#updating-profiles" format="http" scope="external"> Updating Profiles </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="6"> <p><b>Customer Attributes</b> </p> </td> 
   <td colname="col2"> <p><b>Definition/Details</b> </p> <p>Customer attributes let you upload visitor profile data via FTP to the Experience Cloud. Once uploaded, leverage the data in Adobe Analytics and Adobe Target. </p> <p>Target Standard customers can leverage 5 attributes, Target Premium customers can leverage 200 attributes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Format</b> </p> <p>A .csv file with Experience Cloud IDs (ECIDs) and attribute name/value pairs is uploaded via FTP or manually in the Experience Cloud UI. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Example Use Cases</b> </p> <p>Your CRM or other internal system stores valuable information you want to share with Adobe's Experience Cloud, including Target and Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Benefits of Method</b> </p> <p>Uploading customer data creates a profile entry for that visitor in Target, even if Target has yet to see the visitor. </p> <p>Same data is automatically available in Target and Analytics. </p> <p>FTP can be a simpler implementation method than API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Caveats</b> </p> <p>Target Standard customers can leverage 5 attributes, Target Premium customers can leverage 200 attributes </p> <p>Can only update values via Customer Attributes, not on page. </p> <p>Requires Experience Cloud ID (ECID) implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Code Examples</b> </p> <p>Details can be found in <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/t_crs_usecase.html" format="html" scope="external"> Create a Customer Attribute Source and Upload the Data File </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Links to Relevant Information</b> </p> <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/t_crs_usecase.html" format="html" scope="external"> Create a Customer Attribute Source and Upload the Data File </a> </td> 
  </tr> 
 </tbody> 
</table>

>## Entities API {#concept_E7DEC48F973A4F78A66938644FC494E4}Create, update, or delete entities.For more information, see [ Entities ](https://www.adobe.io/apis/marketingcloud/target/docs/reference/recommendations/Methods/entities.html) in the Adobe Target I/O documentation. 
>## Exclusions {#task_DD6D2F889E234F8C82B1604A3B315D81}Create an exclusion list to prevent items from being recommended. 
<draft-comment otherprops="merge">
  recs/t_exclusions.xml 
</draft-comment>
>[!IMPORTANT]
>
>Static and dynamic exclusion rules are powerful features that can help you with your marketing efforts. For detailed information, examples, and use-case scenarios, see[ Use Dynamic and Static Inclusion Rules ](t_create_recs_activity.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F). 



>1. Click ** [!UICONTROL  Recommendations] ** > ** [!UICONTROL  Exclusions] **.
>1. Click ** [!UICONTROL  Create Exclusion] **.

>       ![Step Result](graphics/CreateExclusion.png) 
>1. Type an exclusion ** [!UICONTROL  Name] **.

>1. Use the rule builder to create your exclusions.

>       Select a parameter in the Rules list, select an operator, and then enter one or more values to identify the products. Separate multiple values with commas. 
>1. Click ** [!UICONTROL  Save] **.
>## Entity Attributes {#reference_3BCC1383FB3F44F4A2120BB36270387F}Use entity attributes to pass product or content information to Recommendations. 
<draft-comment otherprops="merge">
  recs/r_entity_attributes.xml 
</draft-comment>
>The following table describes the available variables. 

><table id="table_2F24AB9862FE4D94BFD91F910F436BA9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Entity Attribute </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.id </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p>This required parameter identifies the product. This alphanumeric ID must be the same across all Adobe Marketing Cloud products that are used, including Analytics, for the various products to recognize the item and share data about it. </p> <p>You cannot use a comma in an entity ID, unless you escape it. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.id=67833' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.name </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p>The product name that is displayed on the Web site when the product is recommended. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.name=Giants&amp;nbsp;vs&amp;nbsp;Rockies&amp;nbsp;5/12' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.categoryId </span> </p> <p>Supports multi-value (comma-delimited list). </p> </td> 
   <td colname="col2"> <p> The product category used to organize products on your site. A product can have multiple categories, but only one category can be entered in this field, such as a cardigans sub-subsection (i.e. <span class="codeph"> womens </span>, <span class="codeph"> womens:sweaters </span>, <span class="codeph"> womens:sweaters:cardigans </span>). Multiple categories should be separated by commas. </p> <p> <span class="codeph"> categoryId </span>is limited to 250 characters. Multiple categories should be separated by commas. </p> <p> <p>Note:  To show a recommendation based on a category, only one <span class="codeph"> categoryId </span> can be passed into the mbox used to display that particular recommendation. </p> </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.categoryId=BASEBALL,&amp;nbsp;GIANTS,&amp;nbsp;SF&amp;nbsp;BAY&amp;nbsp;AREA', 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.brand </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p>Displays an item's brand name. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.brand=brandxyz' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.pageURL </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p>Defines the relative URL of the page where the item can be purchased. </p> <p>Example: </p> <p> 
     <codeblock> 
      'entity.pageURL=baseball/giants-tix/giantsvrockies5.12.2000-67833' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.thumbnailURL </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p>Defines the relative URL to the thumbnail image that displays with the item. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.thumbnailURL=baseball/giants-tix/giants-136px.gif' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.message </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p> A message about the product that is displayed in the recommendation, such as "on sale" or "clearance." The message is typically more verbose than the product name. Use to define additional information to display with the product in the template </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.message=Family&amp;nbsp;special' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.inventory </span> </p> <p>Single-value only. Requires an integer or long value. </p> </td> 
   <td colname="col2"> <p>Displays the inventory level of the item. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.inventory=1' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.value </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p>Defines the price or value of the item. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.value=15.99' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.margin </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p>The profit margin or other value of the item. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.margin=1.00' 
     </codeblock> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity. </span> <span class="varname"> &amp;lt;custom&amp;gt; </span> </p> <p>Supports multi-value (JSON array). </p> </td> 
   <td colname="col2"> <p>Define up to 100 custom variables that provide additional information about the item. You can specify any unused attribute name for each custom attribute. For example, you might create a custom attribute called <span class="codeph"> entity.genre </span> to define a book or movie. Or, a ticket vendor might create attributes for an event venue for a secondary performer, such as a visiting team in a sporting event or an opening act in a concert. </p> <p><b>Restrictions</b>: </p> 
    <ul id="ul_F0F102908B0142669AF3B74636C828F1"> 
     <li id="li_9271366EC1C34315B01D5BD919F5432A">You cannot use predefined entity attribute names for custom entity attributes. </li> 
     <li id="li_C765DE30512C4E99927E9810EAA822CF">The attribute <span class="codeph"> entity.environment </span> is reserved by the system and cannot be used for custom entity attributes. Attempts to pass <span class="codeph"> entity.environment </span> using <span class="codeph"> targetPageParams </span>, feed, or API will be ignored. </li> 
    </ul> <p>Examples: </p> <p> 
     <codeblock>
       'entity.venue=AT&amp;amp;T&amp;nbsp;Park' 
     </codeblock> </p> <p> 
     <codeblock>
       'entity.secondary=Rockies' 
     </codeblock> </p> <p>Custom entity attributes support multiple values. A multi-value entity attribute can include up to 100 values. Each value can be up to 100 characters. Values that exceed 100 characters are ignored. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.secondary=["band1",&amp;nbsp;"band2"]' 
     </codeblock> </p> <p> <p>Note:  Multi-value custom entity attributes require valid JSON arrays. For correct syntax information, see <a href="c_products.xml#concept_E5CF39BCAC8140309A73828706288322" format="dita" scope="local"> Custom Entity Attributes </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entity.event.detailsOnly </span> </p> <p>Single-value only. </p> </td> 
   <td colname="col2"> <p>Used to prevent an mbox call from incrementing behavioral data counters for an algorithm. </p> <p>Example: </p> <p> 
     <codeblock>
       'entity.event.detailsOnly=true' 
     </codeblock> </p> <p>In the examples below, the first mbox call will update the catalog and behavioral data. The second mbox call will update only the catalog. </p> <p> 
     <codeblock>
       mboxCreate('myMbox',&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'profile.geo.city&nbsp;=&nbsp;new&nbsp;york', 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'profile.geo.state&nbsp;=&nbsp;new&nbsp;york',&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.id&nbsp;=&nbsp;123', 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.inventory&nbsp;=&nbsp;4' 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;) 
     </codeblock> </p> <p> 
     <codeblock>
       mboxCreate('myMbox',&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'profile.geo.city&nbsp;=&nbsp;new&nbsp;york', 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'profile.geo.state&nbsp;=&nbsp;new&nbsp;york',&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.id&nbsp;=&nbsp;123', 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.inventory&nbsp;=&nbsp;4' 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'entity.event.detailsOnly=true' 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;) 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

>Recommendations sends the ` productId` or ` productPurchasedId` (referred to as ` entity.id` in the code) that is used in the algorithms. 


>>[!NOTE]
>>
>>` entity.id` must match the ` productPurchasedId` sent to the order confirmation page and the ` productId` used in Adobe Analytics product reports). 
>


>Most predefined parameters accept only a single value, with new values overwriting old values. The ` categoryId` parameter can accept a comma-delimited list of values for each category containing that product. New ` categoryId` values are appended (250-character limit). Custom entity attributes can accept multiple values passed as valid JSON arrays (see [ Custom Entity Attributes ](c_products.md#concept_E5CF39BCAC8140309A73828706288322)). 
>[!MORE_LIKE_THIS]* [ Custom Entity Attributes ](c_products.md#concept_E5CF39BCAC8140309A73828706288322)## Custom Entity Attributes {#concept_E5CF39BCAC8140309A73828706288322}Use single- and multi-value custom entity attributes to define additional information about items in your catalog. 
<draft-comment otherprops="merge">
  recs/c_custom_entity_attributes.xml 
</draft-comment>You can include up to 100 custom entity attributes to define additional information about items in your catalog. For example, you might create a custom attribute called ` entity.genre` to define a book or movie. Or, a ticket vendor might create attributes for an event venue to include a secondary performer, such as a visiting team in a sporting event or an opening act at a concert. 

## Custom Entity Attribute Values {#section_313331A9F8194A89B5EDD89363018651}

Custom entity attributes can contain a single value or multiple values. Entity attribute values are displayed in the product view. 

![](graphics/multi-value_product.png) 

A custom entity attribute with a single value is formed the same way as a single-value predefined entity attribute: 


```
entity.genre=genre1
```


A multi-value custom entity attribute must be sent as a valid JSON array: 


```
entity.genre=[“genre1”,&amp;nbsp;“genre2”]
```


Examples of valid JSON arrays supported by [!DNL  Recommendations]: 

* ` ["AB","BC"]` all values are strings
* ` [1,2]` all values are numeric

>[!NOTE]
>
>[!DNL  Recommendations] does not support mixed value types in multi-value entity attributes. For example, ` ["AB",1,true, [1,2,3]]` is a valid JSON array, but it is not supported in [!DNL  Recommendations] because it includes mixed value types (string, numeric, boolean, object). 



After a custom attribute is sent as a valid JSON array, the attribute is treated as a multi-value attribute for all products in the catalog. 


>[!NOTE]
>
>To change an attribute from multi-value to single-value, you must delete your catalog and upload corrected product data. Deleting your catalog does not delete the historical data associated with your product IDs. See[ Deleting All Items From the System ](https://marketing.adobe.com/resources/help/en_US/rec/r_Deleting_All_Items_From_the_System.html) in the *Adobe Recommendations Classic* documentation for more information. 



**Restrictions**: 

* You cannot use predefined entity attribute names for custom entity attributes. (See [ Entity Attributes ](c_products.md#reference_3BCC1383FB3F44F4A2120BB36270387F).) 

* The attribute ` entity.environment` is reserved by the system and cannot be used for custom entity attributes. Attempts to pass ` entity.environment` using ` targetPageParams`, feeds, or APIs will be ignored. 

* Arrays must contain a single value type. Mixed-value arrays ( ` ["AB",1,true]`) are not supported. 

* A multi-value attribute that includes a nested JSON array ( ` [10,12,[1,2,3]]`) is treated as a single-value attribute. 


## Implementing Multi-Value Attributes {#section_80FEFE49E8AF415D99B739AA3CBA2A14}

Multi-value custom entity attributes are supported when using feeds (CSV), ` targetPageParams`, Delivery API, and the Save entities API to upload products. New values replace current values; they are not appended. Empty arrays ( [] ) are treated as having no values. 

Double quotes must be escaped. For example, ` "[""test"", ""value""]"` is a valid JSON array that can be used in CSV. 

**Using targetPageParams** 

The following example shows how to use ` targetPageParams` 


```
function targetPageParams() { 
  return { 
    "entity.id":                    123, 
    "entity.categoryId":            ["A", "A:B", "A:B:C", "A:B:C:D"],        
    "entity.MultiValueAttribute":   ["X", "Y", "Z"], 
    "entity.event.detailsOnly":     true, 
    "excludedIds":                  [123, 3232, 2323, 4344], 
    "orderId":                      123456, 
    "orderTotal":                   195.32, 
    "productPurchaseId":            [001,002,003] 
  }; 
}
```


**Using CSV** 

You can manage your CSV files in raw form using a text editor, or you can use spreadsheet software. 

The raw CSV will look like this: 

![](graphics/multi-value_example_raw.png) 

The same catalog will look like this in a spreadsheet: 

![](graphics/multi-value_example_excel.png) 

When converting to [!DNL  .csv] format, the spreadsheet software adds double quotation marks around cell contents to prevent commas within the cell from acting as column separators. It also adds double quotation marks around JSON string values you include in custom multi-value attributes. This can make working directly with the raw file unwieldy. For example: 

* Spreadsheet: ["1","2","3"]
* Raw: ` "[""1"",""2"",""3""]"`
Use caution when editing a raw catalog CSV file directly. 

**Using APIs** 

See the [ Adobe Recommendation API documentation ](https://www.adobe.io/products/target/docs/reference/recommendations) for information about using the Delivery and Save entities APIs. 

## Using Operators with Multi-Value Attributes {#section_83C2288A805242D9A02EBC4F07DEE945}

When you apply operators to multi-valued custom attributes in algorithm inclusion rules, catalog rules, and exclusion rules, the result will be *true* if at least one value in the list passes the operation (boolean *or*). 

In the following example, the rule is . 

Case 1: . The result is false because no value contains . 

Case 2: . The result is true because one value contains . 

For negative operators, all attribute values must pass (boolean *and*). For example, if the operator is , the result will be *false* if any value matches. 

Refer to the table below for operator behavior in algorithm inclusion rules, catalog rules, and exclusion rules. 



<table id="table_C3A27644C92A4AC4A5703A30E5E87904"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Operator </th> 
   <th colname="col2" class="entry"> Behavior </th> 
   <th colname="col3" class="entry"> Example </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Equals </p> </td> 
   <td colname="col2"> <p> If any attribute value equals the input value, results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       genre equals abc 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.genre = ["ab", "bc", "de"] 
     </userinput>. The result is false because no value is equal to 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 2: 
     <userinput>
       entity.genre = ["abc", "de", "ef"] 
     </userinput>. The result is true because one value is equal to 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 3: 
     <userinput>
       entity.genre = ["abcde", "de", "ef"] 
     </userinput>. The result is false because 
     <userinput>
       abc 
     </userinput> is not equal to any element in the list. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Does not equal </p> </td> 
   <td colname="col2"> <p>If no attribute value equals the input value, results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       genre not equals abc 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.genre = ["ab", "bc", "de"] 
     </userinput>. The result is true because no value is equal to 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 2: 
     <userinput>
       entity.genre = ["abc", "de", "ef"] 
     </userinput>. The result is false because one value is equal to 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 3: 
     <userinput>
       entity.genre = ["abcde", "de", "ef"] 
     </userinput>. The result is true because 
     <userinput>
       abc 
     </userinput> is not equal to any element in the list. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Contains </p> </td> 
   <td colname="col2"> <p>If any value of attribute contains the input value, results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       genre contains abc 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.genre = ["ab", "bc", "de"] 
     </userinput>. The result is false because no value contains 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 2: 
     <userinput>
       entity.genre = ["abcde", "de", "ef"] 
     </userinput>. The result is true because one value contains 
     <userinput>
       abc 
     </userinput>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Does not contain </p> </td> 
   <td colname="col2"> <p>If no value of attribute contains the input value results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       genre does not contain abc 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.genre = ["ab", "bc", "de"] 
     </userinput>. The result is true because no value contains 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 2: 
     <userinput>
       entity.genre = ["abcde", "de", "ef"] 
     </userinput>. The rule will result in false as one value contains 
     <userinput>
       abc 
     </userinput>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Starts with </p> </td> 
   <td colname="col2"> <p>If any value of attribute starts with the input value results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       genre starts with abc 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.genre = ["ab", "bc", "de"] 
     </userinput>. The result is false because no value starts with 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 2: 
     <userinput>
       entity.genre = ["abcde", "de", "ef"] 
     </userinput>. The result is true because one value starts with 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 3: 
     <userinput>
       entity.genre = ["ab", "de", "abc"] 
     </userinput>. The result is true because one value starts with 
     <userinput>
       abc 
     </userinput> (not necessarily the first element in the list). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ends with </p> </td> 
   <td colname="col2"> <p>If any value of attribute ends with the input value results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       genre ends with abc 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.genre = ["ab", "bc", "de"] 
     </userinput>. The result is false because no value ends with 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 2: 
     <userinput>
       entity.genre = ["deabc", "de", "ef"] 
     </userinput>. The result is true because one value ends with 
     <userinput>
       abc 
     </userinput>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Greater than or equal to (numeric values only) </p> </td> 
   <td colname="col2"> <p>Attribute value is converted to double. Attributes that cannot be converted are skipped while running the rule. </p> <p>After processing, any attribute value greater than or equal to the input value results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       price greater than or equal to 100 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.price = ["10", "20", "45"] 
     </userinput>. The result is false because no value is greater than or equal to 100. The value <span class="codeph"> de </span> is skipped because it cannot be converted to double. </p> <p>Case 2: 
     <userinput>
       entity.price = ["100", "101", "90", "80"] 
     </userinput>. The result is true because as two values are greater or equal to 100. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Less than or equal to (numeric values only) </p> </td> 
   <td colname="col2"> <p>Attribute value is converted to double. Attributes that cannot be converted are skipped while running the rule. </p> <p>After processing, any attribute value less than or equal to the input value results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       price less than or equal to 100 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.price = ["101", "200", "141"] 
     </userinput>. The result is false because no value is less than or equal to 100. The value <span class="codeph"> de </span> is skipped because it cannot be converted to double. </p> <p>Case 2: 
     <userinput>
       entity.price = ["100", "101", "90", "80"] 
     </userinput>. The result is true because two values are less than or equal to 100. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamically matches (only available in item-based algorithms) </p> </td> 
   <td colname="col2"> <p>If any attribute value matches the input value results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       genre matches abc 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.genre = ["ab", "bc", "de"] 
     </userinput>. The result is false because no value matches 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 2: 
     <userinput>
       entity.genre = ["abc", "de", "ef"] 
     </userinput>. The result is true because one value matches 
     <userinput>
       abc 
     </userinput>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dynamically does not match (only available in item-based algorithms) </p> </td> 
   <td colname="col2"> <p>If any attribute value matches the input value results in <i>false</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       genre does not match abc 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.genre = ["ab", "bc", "de"] 
     </userinput>. The result is true because no value matches 
     <userinput>
       abc 
     </userinput>. </p> <p>Case 2: 
     <userinput>
       entity.genre = ["abc", "de", "ef"] 
     </userinput>. The rule will result in false as one value matches 
     <userinput>
       abc 
     </userinput>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dynamically ranges (only available in item-based algorithms, numeric values only) </p> </td> 
   <td colname="col2"> <p>If any numeric attribute value lies within specified range results in <i>true</i>. </p> </td> 
   <td colname="col3"> <p> 
     <userinput>
       price dynamically ranges in 80% to 120% of 100 
     </userinput> </p> <p>Case 1: 
     <userinput>
       entity.price = ["101", "200", "125"] 
     </userinput>. The result is true because 
     <userinput>
       101 
     </userinput> is in the range of 80% to 120% of 100. The value 
     <userinput>
       de 
     </userinput> is skipped because it cannot be converted to double. </p> <p>Case 2: 
     <userinput>
       entity.price = ["130", "191", "60", "75"] 
     </userinput>. The result is false because no value is in the range of 80% to 120% of 100. </p> </td> 
  </tr> 
 </tbody> 
</table>


>[!NOTE]
>
>*Double* is a Java data type. For operators that require numeric values, converting to double eliminates non-numeric values from consideration in the results. 



## Multi-Value Attributes in Designs {#section_F672E4F6E1D44B3196B7ADE89334ED4A}

Multi-value attributes will appear as a comma-separated list when referenced in a design. 

Example: 

When ` entity.genre=["genre1","genre2"]` is referenced in a design as ` $entity&amp;lt;N&amp;gt;.genre`, the result is ` genre1, genre2`. 
>[!MORE_LIKE_THIS]* [ Entity Attributes ](c_products.md#reference_3BCC1383FB3F44F4A2120BB36270387F)## Catalog Search {#concept_785E93EC06CE477CB3436404936F3C16}The catalog search helps you locate the products or content in your catalog. 
<draft-comment otherprops="merge">
  recs/c_catalog_search.xml 
</draft-comment>You can refine your search by selecting a search option from the options menu that displays when you click the down arrow in the search field. 

![](graphics/searchproductsmenu.png) 

** [!UICONTROL  ALL] ** searches across all of the other search criteria, using OR logic. 

In the search results, you click Settings to specify the production host group environment whose catalog you are displaying. An item can exist only once within an environment. You can also scroll through the items in the search results to view thumbnails and other product information. 

The number that displays next to "Products" is the number of products that match the search term, out of the total available in the specified environment. 

Click the refresh icon to re-index your catalog. Be aware that indexing can take some time, depending on the size of your feed. 

The catalog is automatically refreshed every hour. Click ** [!UICONTROL  Refresh] ** to reindex the catalog between automatic refreshes. 

You can create collections or exclusions using Advanced Search on the Catalog Search page (Recommendations &amp;gt; Catalog Search &amp;gt; Advanced Search). After creating a search using "id &amp;gt; contains," for example, you can then click Save As &amp;gt; Collection or Exclusion. 


>[!IMPORTANT]
>
>The Advanced Search functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.


>## Collections {#concept_671BEFFB997D4F1282665BF3CAC00AC5}A collection is an optional subset of entities based on filter rules that become eligible for a recommendation. 
<draft-comment otherprops="merge">
  recs/c_collections.xml 
</draft-comment>Recommendations displays items from your collections according to criteria you set up. 

Commonly, a collection is a set of similar or related items, such as a single [ entity ](c_products.md#concept_FD935A24D98745FFB2447933FCEB8062) collection. However, you can group whichever items into a category that makes sense to your business, such as products in a certain price range or color, or items that are likely to be interesting in a particular geographical area. For example if you work for a media company, you could create a collection for commonly recommended items such as TV episodes, movies, comedies, or documentaries. If you work for a retail company, you could create a collection for commonly recommended items such as women's clothing, men's clothing, shoes, or sporting goods. 

Use collections to organize your products in logical buckets. For example, if some items are available in one region but not another, you might want to create a collection that excludes items that are unavailable in the visitor's region. You can also use collections to organize seasonal items, or any other organizational parameters that apply to your business. 


>[!NOTE]
>
>Collections are optional, however, we recommend that you use them because they speed recommendations algorithm times by not generating recommendations for unrelated entities. Collections can be useful to narrow and improve the relevancy of the recommendations results.



The [ backup recommendations ](c_algorithms.md#concept_BC16005C7A1E4F1A87E33D16221F4A96) generated for each criteria within the recommendation also uses this collection, so only items in the collection are included in the backup recommendation. With collections, you can be sure that only products that make sense to show in a location are displayed. 

Collections are rebuilt or updated every time each criteria runs. 

You can group your items into catalogs, then create separate recommendations for each collection. 

Inclusion criteria allow you to do similar things as a collection, but they must be set up every time you create an activity. Collections allow you to create a set of items one time, then use it whenever it is appropriate to do so without having to set it up again. 

When you are creating or editing a [!DNL  Recommendations] activity, the collection name appears next to the [!UICONTROL  Criteria] label on the activity diagram. 


>[!NOTE]
>
>Collections are not applied when using the [!UICONTROL  Recently Viewed Items] recommendation key. 


>## Create a Collection {#task_1256DFF6842141FCAADD9E1428EF7F08}Create a collection to organize the products you want to show in your recommendations. 
<draft-comment otherprops="merge">
  recs/t_create_collection.xm 
</draft-comment>
>1. Click ** [!UICONTROL  Recommendations] ** > ** [!UICONTROL  Collections] **.
>1. Click ** [!UICONTROL  Create Collection] **.

>       ![Step Result](graphics/CreateCollection.png) 
>1. Type a ** [!UICONTROL  Name] ** for the collection.

>       You can also enter an optional ** [!UICONTROL  Description] **. 
>1. Set the rules used to build the collection.

>       For example, your collection might be built around a product ID or category, margin, or any other parameter in the list. 

>       You can add rules to use multiple parameters to define a collection. Multiple rules are joined with an AND. All specified rules must be matched for the collection to apply. 
>1. Click ** [!UICONTROL  Save] **.
