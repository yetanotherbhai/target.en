---
description: Feeds provide methods to get product or content information into your recommendations. Item details can be sent using the Google Product Search feed format and CSV files.
keywords: recommendations feed;feed;SAINT;ftp;csv
seo-description: Feeds provide methods to get product or content information into your recommendations. Item details can be sent using the Google Product Search feed format and CSV files.
seo-title: Feeds
solution: Target
title: Feeds
topic: Premium
uuid: 9d732a97-68c5-4246-9314-43b4e7d3385b
index: y
internal: n
snippet: y
translate: y
---

# Feeds

Feeds allow you to bypass complex mbox implementation or augment your mbox data with information that is either unavailable on the page or unsafe to send directly from the page, such as margin, COGS, and so on.
You can select which columns from your SAINT product classifications file or Google Product Search file you want to send to the `Recommendations` server. These pieces of data about each item can then be used in template display and for controlling recommendations. 
If data is collected by both an entity feed and an mbox, the most recent data wins. Usually, the most recent data comes from an mbox, because it is viewed more often. In the rare event that entity feed data and mbox data hit at the same time, the mbox data is used.
The `Feeds` list ( ** `Recommendations` ** > ** `Feeds` **) provides information about any feeds you have created. To edit the name of a feed, you must edit the feed itself. When you save with the new name, the feed is refreshed. 

>[!NOTE]
>
>If the `Last Updated` feed says "undefined," then the feed is coming in from `Recommendations Classic` and cannot be changed from within `Target Premium Recommendations`. 


The following sections contain more information:

* [Feed Statuses](c_feeds.md#section_5DDC2DECF70A42FDAFF2235E91371537)
* [Feed Status Indicators](c_feeds.md#section_3C8A236C5CB84C769A9E9E36B8BFABA4)
* [Google](c_feeds.md#section_EECB1AA1B91B412AABE1CB7FDFCA3AE7)
* [CSV](c_feeds.md#section_06DA64915E2D461496E9BFD54220916F)


## Feed Statuses {#section_5DDC2DECF70A42FDAFF2235E91371537}

The following are possible statuses for a feed:


<table id="table_0C54CB3B06DA419AB4A83789B09E531F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Status</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Syncing</p> </td> 
   <td colname="col2"> <p>Feed setup details are being saved to <span class="keyword">Target</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>No Feed Run</p> </td> 
   <td colname="col2"> <p>You have created a feed but it has not been scheduled (frequency is set to Never).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scheduled at <i>date and time</i> </p> </td> 
   <td colname="col2"> <p>The feed has not been run, but is scheduled to run at the specified date and time.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Server Not Found</p> </td> 
   <td colname="col2"> <p>FTP or URL locations are invalid or otherwise unreachable.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Waiting to Download</p> </td> 
   <td colname="col2"> <p>The feed is waiting to downloaded to <span class="keyword">Target</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Preparing to Import</p> </td> 
   <td colname="col2"> <p>The feed is being prepared to import to <span class="keyword">Target</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flushing Results</p> </td> 
   <td colname="col2"> <p>The results are being flushed.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Waiting for Index Queue</p> </td> 
   <td colname="col2"> <p>The feed is in the index queue.</p> <p> <p>Note: Once the feed status is "Waiting for Index Queue," the newly updated values are available in delivery and criteria processing.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Indexing since <i>date and time</i> </p> </td> 
   <td colname="col2"> <p>The feed is being indexed since the date and time indicated.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Indexed at <i>date and time</i> </p> </td> 
   <td colname="col2"> <p>The feed was successfully indexed at the date and time indicated.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Success</p> </td> 
   <td colname="col2"> <p>The feed was successfully saved to <span class="keyword">Target</span> at the date and time indicated. </p> </td> 
  </tr> 
 </tbody> 
</table>

To update a feed (for example, to make changes to your feed configuration or feed file), open the feed, make any desired changes, and click ** `Save` **. 

## Feed Status Indicators {#section_3C8A236C5CB84C769A9E9E36B8BFABA4}

The following feed status indicators display in the `Status` column: 


<table id="table_396F6009016843E19F8F423A06B5B1E6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Status Indicator</th> 
   <th colname="col2" class="entry">Description</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Green status indicator</p> </td> 
   <td colname="col2"> <p>When a feed successfully finishes indexing, a green status dot indicates that the feed is in a successful state.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Yellow status indicator</p> </td> 
   <td colname="col2"> <p>When a feed or feed index is delayed by 25% of the feed frequency, a yellow status dot displays. For example, a yellow dot displays for a feed set to run daily if the index hasn't completed six hours after the scheduled time.</p> <p> <p>Note: Once the feed status is "Waiting for Index Queue," the newly updated values are available in delivery and criteria processing.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>White status indicator</p> </td> 
   <td colname="col2"> <p>When a feed is not scheduled, a white status dot indicates that the feed has not run yet.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Red status indicator</p> </td> 
   <td colname="col2"> <p>If the feed fails to upload data to server, a red status indicator is shown.</p> </td> 
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

## Google {#section_EECB1AA1B91B412AABE1CB7FDFCA3AE7}


>[!IMPORTANT]
>
>The Google Product Search feed type uses the Google format. This is different from the Adobe proprietary CSV upload format.



>[!NOTE]
>
>It is not required to use Google data. `Recommendations` just uses the same format as Google. You can use this method to upload any data you have, and use the available scheduling features. However, you must retain Google's predefined attribute names when you set up the file. 


Most retailers upload products to Google, so when a visitor uses Google product search their products will show up. `Recommendations` follows Google's specification exactly for entity feeds. Entity feeds can be sent to `Recommendations` via `.xml`, `.txt`, or `.tsv`, and can use the [attributes defined by Google](https://support.google.com/merchants/answer/188494?hl=en&topic=2473824&ctx=topic#US). The results are searchable on the [Google shopping pages](http://www.google.com/prdhp). 

>[!NOTE]
>
>The POST method must be allowed on the server that is hosting the Google feed content.


Because `Recommendations` users already configure `.xml` or `.txt` feeds to send to Google either via URL or FTP, entity feeds accept that product data and use it to build out the recommendations catalog. Specify where that feed exists and the recommendations server retrieves the data. 
If you use Google Product Search for the entity feed upload, you still need to have a product page mbox on the page if you want to show recommendations there or track product views for algorithm delivery based on views.
Google feeds do not support multiple values for a custom attribute.
The feed runs at the time you save and activate it. It runs at the time you save the feed, then every day an hour later.

## CSV {#section_06DA64915E2D461496E9BFD54220916F}

You can create a `.csv` file that contains display information for your products, then bulk upload it to the `Recommendations` server. 

>[!IMPORTANT]
>
>Do not enclose values in double quotes ( " ) in your `.csv` file unless they are intentional. If you enclose values in double quotes you must escape them by enclosing them in another set of double quotes. Double quotes that are not escaped will prevent the recommendations feed from loading properly. 


For example, the following syntax is incorrect:
`"Apples "Bananas" Grapes"",` 
The following syntax is correct:
"Apples ""Bananas"" Grapes""",
Use the bulk upload method to send display information if you don't have mboxes on your page, or you want to supplement your display information with items that are not available on your site. For example, you might want to send inventory information that might not be published on your site.
Any data uploaded using the upload template file overwrites that value in our database, so if you send price information in JavaScript and then send different price values in the file, the values in the file override the information sent with JavaScript.

>[!NOTE]
>
>You can't overwrite an existing value with a blank value. You have to pass another value in its place to overwrite it. In the case of sale price, a common solution is to either pass in an actual "NULL" or some other message. You can then write a template rule to exclude items with that value.


The product is available in the admin interface approximately two hours after successfully uploading its entity.
