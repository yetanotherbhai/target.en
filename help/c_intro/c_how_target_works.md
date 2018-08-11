---
description: Adobe Target integrates with websites by means of a JavaScript library.
keywords: Overview and Reference
seo-description: Adobe Target integrates with websites by means of a JavaScript library.
seo-title: How Adobe Target Works
solution: Target
subtopic: Getting Started
title: How Adobe Target Works
topic: Standard
uuid: 7e407e3e-610d-4900-87ef-5fe9444d07c8
index: y
internal: n
snippet: y
translate: y
---

# How Adobe Target Works

[!DNL  Target Standard] updates and supplements the [!DNL  mbox.js] with a reference to a new [!DNL  target.js] file. The [!DNL  target.js] file is hosted by Adobe. [!DNL  Target.js] makes it possible to edit content on any page using the Visual Experience Composer, even if the page does not contain predefined mboxes. You must also reference this file on every page on your site. For example, you might add it to your global header. 

Each time a visitor requests a page that has been optimized for Target, a request is sent to the targeting system to determine what content to serve to a visitor. This process occurs in real-time—every time a page is loaded, a request for the content is made and fulfilled by the system. The content is governed by the rules of marketer-controlled activities and experiences and is targeted to the individual site visitor. Content is served that each site visitor is most likely to respond to, interact with, and ultimately purchase, to maximize response rates, acquisition rates, and revenue. 

The content that displays in a basic A/B test is randomly chosen from the assets you assign to the activity, according to the percentages you choose for each experience. As a result of this random splitting of traffic, it can take a lot of initial traffic before the percentages even out. For example, if you create two experiences, the starting experience is chosen randomly. If there is little traffic, it's possible that the percentage of visitors can be skewed toward one experience. As traffic increases, the percentages should become more equal. 

You can specify percentage targets for each experience. In this case, a random number is generated and that number is used to choose the experience to display. The resulting percentages might not exactly match the specified targets, but more traffic means that the experiences should be split closer to the target goals. 


1. A customer requests a page from your server and it displays in the browser.
1. A first party cookie is set in the customer's browser to store customer behavior.
1. The page calls the targeting system.
1. Content displays based on the rules of your campaign.


In Target Standard, each element on the page is part of a single experience for the entire page. Each experience includes multiple elements on the page. A page is optimized with a single line of code in the ` &amp;lt;head&amp;gt;` of each page you want to track. 

In Target Classic, a single page might contain multiple optimized content areas, called *mboxes*. An mbox is a ` div` tag that wraps around existing content on a Web page. The ` div` tag is followed by a single line of JavaScript to create the mbox instance. An mbox can encompass a single element, multiple elements, or an entire page. A single campaign (A/B, multivariate, or targeting) can use multiple mboxes to control multiple elements across multiple pages. Each mbox is uniquely named, and is immediately available for testing or targeting. In addition, an mbox that is used to serve content for one campaign can also be used to track conversions or log visitor behavior for another. You could use a multi-page campaigns to create a funnel analysis and track a number of different conversions based on their KPIs or specific business criteria. 
