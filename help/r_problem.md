---
description: Client Care is prepared to help you solve any issues that might arise. This page contains the information you need when contacting Client Care to expedite a resolution.
seo-description: Client Care is prepared to help you solve any issues that might arise. This page contains the information you need when contacting Client Care to expedite a resolution.
seo-title: Contacting Adobe
solution: Target
title: Contacting Adobe
topic: Advanced
uuid: 39134e36-2f12-4649-bb63-cd228072099c
index: y
internal: n
snippet: y
translate: y
---

# Contacting Adobe


## Basic Information {#section_CC8B206F58D6495C9372D5C0D4055CF6}

If you encounter issues or have questions when using Target, you have a number of options 

For questions, you can ask the Adobe Target experts in the [ Experience Cloud community](https://forums.adobe.com/community/experience-cloud/marketing-cloud/target) ( [!DNL  https://forums.adobe.com/community/experience-cloud/marketing-cloud/target]) or ask us on Twitter at [ @AdobeExpCare](http://twitter.com/adobeexpcare) ( [!DNL  http://twitter.com/adobeexpcare]). 

For technical issues or to log a bug you can contact Customer Care. To contact Customer Care by telephone, call 1-800-497-0335. Toll free numbers outside the United States can be found on the [ Adobe Digital Marketing Customer Care Regional Phone Numbers](https://helpx.adobe.com/contact/dma-external/DMACustomeCareRegionalPhoneNumbers.html) page ( [!DNL  https://helpx.adobe.com/contact/dma-external/DMACustomeCareRegionalPhoneNumbers.html]). When asked to select an option for your product, press 3 to contact the Target team. 

E-mail Customer Care at [!DNL  tt-support@adobe.com]. 

For the quickest triage of your issue, please have the following basic information ready when you are contacting us: 



<table id="table_6D7C22189503440CB76720C632E479C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Summary </p> </td> 
   <td colname="col2"> <p> Brief summary of the overall issue </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Account information </p> </td> 
   <td colname="col2"> <p>Company Name </p> <p>Admin Number </p> <p>Campaign Name </p> <p> Type of Campaign </p> <p> Report Suite/Report Suite ID (if regarding a Target to SiteCatalyst integration) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Steps to reproduce </p> </td> 
   <td colname="col2"> <p>Include as much detail as possible, including any URLs needed to duplicate as well as the expected result. </p> <p> Include enough detail that somebody unfamiliar with Target should be able to follow the directions and reproduce the problem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Priority </p> </td> 
   <td colname="col2"> <p>P1 (most important) to P4 (least important). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Business impact </p> </td> 
   <td colname="col2"> <p> What is the impact to your business? For example, is this issue causing revenue loss or rendering the product unusable, and is there a viable workaround? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Expectations </p> </td> 
   <td colname="col2"> <p>What do you expect to happen? </p> </td> 
  </tr> 
 </tbody> 
</table>

Also prepare information related to the specific issue. For example, one of the most common problems received by Client Care is that mboxes load too slowly. For this issue, helpful data includes: 


* A Firebug trace showing the repeatable slowness to a URL or host. A gomez report with one or two outlying requests is not enough data to analyze or troubleshoot the issue. 

* A screenshot of a traceroute from the machine running the firebug TO 70.42.13.100. This is very important. The EDGE networks are worldwide so it is very difficult to determine where the client is being sent. For example, if you can reproduce the issue from your desktop in your office, say "I can reproduce this from my desktop and I am homed to EDGE 20." 

* Your client code and the mbox name (if you have it).
* The number of mboxes embedded in the page. Is it a single mbox of many on the page that is slow? 

* How repeatable is the slowness with the given mbox on the given page? Providing a Firebug trace shows Client Care a one-time case scenario. If you can provide statistical data, such as "the lowest I've seen is 300ms, highest I've seen is 1.1 seconds and I've tested 50 times," it will help to facilitate a solution. 

* Information regarding anything unusual about your campaigns. Is there a high number of segments? (For example, do you update segments 3 to 4 times per hour in the admin interface?) This information helps Client Care understand the interaction between the admin interfaces and the edges for this campaign. Frequent updates to the campaign mean frequent reloads from the central server, which can force more remote calls or cache reloads. 

* Any other data you think might be helpful.


## In Case of an Outage {#section_2CB3BC53E4C641F38D50949E2E7A2886}

If you suspect there is an outage, first check the [ Experience Cloud System Status page](http://status.adobe.com) ( [!DNL  http://status.adobe.com]) This has a record of all outages, incidents and maintenance for Experience Cloud Solutions, including Target, and includes latest updates from our Tech Ops team. If you still require assistance, please ensure you know the following in addition to the information listed above when you contact Customer Care: 


* Time outage started
* Explanation of what is occurring
* Scope
* Expectation of resolution (ETA, severity, and so on)

