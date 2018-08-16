---
description: Adobe Target aligns with search engine guidelines for testing.
keywords: Overview and Reference;SEO;search engine optimization
seo-description: Adobe Target aligns with search engine guidelines for testing.
seo-title: Search Engine Optimization (SEO) Friendly Testing
solution: Target
subtopic: Getting Started
title: Search Engine Optimization (SEO) Friendly Testing
topic: Standard
uuid: 23374315-cc91-4723-937c-f39f03fe29f0
index: y
internal: n
snippet: y
translate: y
---

# Search Engine Optimization (SEO) Friendly Testing

Google encourages user testing and has stated in its documentation that A/B and multivariate testing will not harm organic search engine rankings as long as a few simple guidelines are followed. 

For more information, see the following Google resources: 


* [ Website testing and Google Search ](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [ Experiments and Cloaking ](https://support.google.com/analytics/answer/2576845?hl=en&ref_topic=1745207)


Guidelines were presented in a [ Google Webmaster Central Blog ](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) post. Although the post dates back to 2012, it remains Google's most recent statement on the matter and the guidelines remain relevant. 

* ** No cloaking** - Cloaking is showing one set of content to your users and a different set of content to search engine bots by specifically identifying them and purposely feeding them different content. 

  Target, as a platform, has been configured to treat search engine bots the same as any user. This means that the bots might get included in tests you are running, if they are randomly selected, and "see" the test variations. 

* ** Use rel="canonical"** - Sometimes an A/B test needs to be set up using different URLs for the variations. In these instances, all variations should contain a ` rel="canonical"` tag that references the original (control) URL. For instance, if Adobe were testing its home page using different URLs for each variation, the following canonical tag for the home page would go in the ` <head>` tag for each of the variations: 

  ` <link rel="canonical" href="http://www.adobe.com" />` 

* ** Use 302 (temporary) redirects** - In the instances where separate URLs are used for the variation pages in a test, Google recommends using a 302 redirect to direct traffic into the test variations. This tells the search engines that the redirect is temporary and will only be active as long as the test is running. 

  A 302 redirect is a server-side redirect, and Target, along with most optimization providers, uses client-side capabilities. Therefore, this is an area where Target is not fully compliant with Google's recommendations. This, however, impacts only a small fraction of tests. The standard approach for running tests through Target calls for changing content within a single URL, so no redirects are necessary. There are instances when clients need to use multiple URLs to represent their test variations. In these instances, Target uses the JavaScript ` window.location` command to direct users to test variations, which does not explicitly signify whether the redirect is a 301 or 302. 

  Although we continue to look for viable solutions to completely align with search engine guidelines, for those clients that must use separate URLs for testing, we are confident that proper implementation of the canonical tags mentioned above mitigates the risk associated with this approach. 

* ** Run experiments only as long as necessary** - We believe "as long as necessary" to be as long as it takes to reach statistical significance. Target [ provides best practices ](https://docs.adobe.com/content/target-microsite/testcalculator.html) to determine when your test has reached this point. We recommend that you incorporate the hardcoded implementation of winning tests into your testing workflow and allot the appropriate resources. Using the Target platform to "publish" winning tests is not recommended as a permanent solution, but as long as the winning test is published for 100% of users 100% of the time, this approach can be used while the process of hardcoding the winning test is completed. 

  It's important to consider what your test has changed as well. Simply updating the color of buttons or other minor non-text-based items on the page will not have any influence over your organic rankings. Changes to text should be hardcoded, however. 

  It's also important to consider the accessibility of the page you're testing. If the page is not accessible to the search engines and was never designed to rank in organic search in the first place, such as a dedicated landing page for an email campaign, then none of the considerations above apply. 

Googles states that following these guidelines "should result in your tests having little or no impact on your site in search results." 

In addition to these guidelines, Google also provides one more guideline in the documentation to their Content Experiments tool: 


* "Your variation pages should maintain the spirit of the content on your original pages. Those variations shouldn't change the meaning of or your user's general perception of that original content." 



Google states as an example that "if a site's original page is loaded with keywords that don't relate to the combinations being shown to users, we may remove that site from our index." 

We feel that it would be difficult to unintentionally change the meaning of the original content within test variations, but we do recommend being aware of the keyword themes on a page and maintaining those themes. Changes to page content, especially adding or deleting relevant keywords, can result in ranking changes for the URL in organic search. We recommend that you engage with your SEO partner as part of your testing protocol. 
