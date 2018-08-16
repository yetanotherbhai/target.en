---
description: To use Target Standard or Target Premium, add one line of code to call mbox.js.
keywords: Implementation;Mbox;download mbox.js;download api;mbox.js api
seo-description: To use Target Standard or Target Premium, add one line of code to call mbox.js.
seo-title: mbox.js Implementation
solution: Target
subtopic: Getting Started
title: mbox.js Implementation
topic: Standard
uuid: 64c43710-c9d3-4a04-b44b-ea1977a88899
index: y
internal: n
snippet: y
translate: y
---

# mbox.js Implementation

You can use either of two library references: [!DNL  mbox.js] or [!DNL  at.js]. [ Understanding the Target JavaScript Libraries ](../../../c_seting_up_target/c_implementing_target/c_target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB) explains the differences between the two libraries. 


>[!NOTE]
>
>The mbox.js library is still supported, but there will be no feature updates. All customers should migrate to at.js. For more information, see[ Migrate to at.js from mbox.js ](../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/t_target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA). 



The single reference to [!DNL  mbox.js] on each page provides the libraries needed for all of your activities. [!DNL  mbox.js] calls [!DNL  Target] from every page that references the [!DNL  mbox.js] file. This enables [!DNL  Target] to do the following: 


* Deliver Target activities
* Track clicks
* Track most success metrics



>[!TIP]
>
>To simplify implementation, you could reference [!DNL  mbox.js] in your global header. 



**mbox.js Implementation Overview (8:52)** 

This video explains how to implement [!DNL  mbox.js]. 


* Select the correct settings for your [!DNL  mbox.js] file 

* Implement [!DNL  Target] by adding the [!DNL  mbox.js] file to the &lt;head&gt; of your site 



>[!VIDEO](https://vimeo.com/f-A1zET6AwE) 

You do not need to maintain different activity-specific versions of the file. 

>1. Reference [!DNL  mbox.js] in the ` <head>` section of each page on your site.

>       ` <script src="/ *` directory`*/ *` scripts`*/mbox.js"></script>` 

>       Where ` *` directory`*/ *` scripts`*` is the directory where you saved your [!DNL  mbox.js] file after downloading it. 
