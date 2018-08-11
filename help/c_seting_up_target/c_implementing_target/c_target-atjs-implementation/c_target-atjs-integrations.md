---
description: Information about common integrations with Target and their support status with at.js.
keywords: at.js integration;supported integrations;unsupported integrations;third party integrations
seo-description: Information about common integrations with Target and their support status with at.js.
seo-title: at.js Integrations
solution: Target
title: at.js Integrations
topic: Standard
uuid: fbe37263-6fcf-4205-84b0-a8d4c4bbdcb0
index: y
internal: n
snippet: y
translate: y
---

# at.js Integrations

If there are additional integrations you use or if you have a compelling need for an integration that is not supported, please contact your account representative or consultant. 

This section contains the following information: 


* [ Supported Integrations ](c_target-atjs-integrations.md#section_3B44A970D3FB42D1973701452C868B55)
* [ Unsupported Integrations ](c_target-atjs-integrations.md#section_8EFCAED418DC42E0B07F95924819EAC2)
* [ Third-Party Integrations ](c_target-atjs-integrations.md#section_EE599839CCAD49DD97640E5EDAD9082E)


## Supported Integrations {#section_3B44A970D3FB42D1973701452C868B55}


<table id="table_3C9C2D0A88004D5D9708347B85DE5A7E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Integration </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Analytics for Target (A4T) </p> </td> 
   <td colname="col2"> 
    <!-- link to section in tnt--> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Profiles &amp;amp; Audiences (P&amp;amp;A) </p> </td> 
   <td colname="col2"> 
    <!--link to mcloud help Audiences--> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>VisitorId Service </p> </td> 
   <td colname="col2"> 
    <!-- link to mcloud help Experience Cloud ID Service--> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Tag Management (DTM) </p> </td> 
   <td colname="col2"> 
    <!--link to dtm--> <p>Consider the following when using a DTM integration: </p> <p> 
     <ul id="ul_8B7BF60E14554C7B863E434180D409C7"> 
      <li id="li_EF8BC216C6A04FAA8E214ADC59CC7724">Library Management: Use the "Custom" hosting option. <p>"Automatic" management is not currently supported. </p> </li> 
      <li id="li_AB3B3ED75C634846914A8DE9B96FEB76">Global Mbox Parameters work </li> 
      <li id="li_E048B9DCDA8A4BD68600218F2D653963">Wrapping Mboxes in page-load rules now fire immediately instead of at the end of page load. </li> 
      <li id="li_8017C0CE60D64860AED299B134E5C465">JavaScript/Third Party Tags: Mbox creation and parameter passing methods can be used in the JavaScript/Third Party Tag sections of Page Load Rules, Event-based Rules, and Direct Call Rules. For example, many customers already trigger view change mboxes using the "pushState or hashChange" or "custom event" conditions in DTM's Event-based Rules. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Experience Manager (AEM) Cloud Service </p> </td> 
   <td colname="col2"> <p> The AEM Cloud Service enables access to Target capabilities from within the AEM workflow. </p> <p> <span class="keyword"> Adobe Experience Manager </span> 6.2 with FP-11577 (or later) now supports <span class="filepath"> at.js </span> implementations with its <span class="wintitle"> Adobe Target Cloud Services </span> integration. For more information, see <a href="https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html" format="html" scope="external"> Feature Packs </a> and <a href="https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html" format="html" scope="external"> Integrating with Adobe Target </a> in the <i>Adobe Experience Manager 6.2</i> documentation. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Unsupported Integrations {#section_8EFCAED418DC42E0B07F95924819EAC2}


<table id="table_4CF1738CF06B43A784EE783D3FAED3C8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Integration </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Legacy Target to SiteCatalyst Integration </p> </td> 
   <td colname="col2"> <p>This was the integration that sent campaign and recipe ids to <span class="keyword"> SiteCatalyst </span> via the page call so you could do reporting in the <span class="keyword"> SiteCatalyst </span> UI. This functionality is replaced by A4T. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Legacy Target to SiteCatalyst Integration </p> </td> 
   <td colname="col2"> <p>This was the integration that made mbox calls named "SiteCatalyst: Event" and "SiteCatalyst: Purchase" so you could build success metrics and user profiles based on evars and props. This functionality is replaced by A4T and P&amp;amp;A. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Legacy Audience Manager (AAM) to Target Integration </p> </td> 
   <td colname="col2"> <p>This was the integration that made a front-end API call to retrieve AAM segments and then sent them as mbox parameters on every mbox call on the page. It's possible to replicate this integration using the <span class="codeph"> adobe.target.registerExtension() </span> method in <span class="filepath"> at.js </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Third-Party Integrations {#section_EE599839CCAD49DD97640E5EDAD9082E}


<table id="table_8139E0696BAD436588224AEC2AEE0852"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Integration </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Other Tag Managers </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> at.js </span> should work with non-Adobe tag management platforms, but be careful using custom integration features that other vendors have developed. Their integrations might be dependent on internal <span class="filepath"> mbox.js </span> functions that no longer exist in <span class="filepath"> at.js </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Third-party data providers (e.g. Demandbase, Bluekai, weather APIs) </p> </td> 
   <td colname="col2"> <p>Many third-party data providers used to supplement Target's user profiling can be replicated using <a href="cmp_at.js_Functions.xml#reference_B3ACC004D45E460C8DD94C1476D2625C" format="dita" scope="local"> registerExtension() </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

