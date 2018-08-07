---
description: Information to help you integrate email with recommendations using a rawbox email template or using the download-only template.
seo-description: Information to help you integrate email with recommendations using a rawbox email template or using the download-only template.
seo-title: Integrating Recommendations with Email
solution: Target
title: Integrating Recommendations with Email
topic: Recommendations
uuid: 53fa6bd1-0f55-4396-b67e-585ea4ba697f
index: y
internal: n
snippet: y
translate: y
---

# Integrating Recommendations with Email


>The email service provider's capabilities determine which method to use.

>>[!NOTE]
>>
>>It is suggested that you talk with your account manager before implementing either of these options.
>

>**Option 1: Using a "Rawbox" Email Template** 
>This is the preferred option.
>Set up a recommendation as usual, using a template that has the desired look and feel for the email. Instead of choosing an mbox on your site to show the recommendations, select a "rawbox" that is in the email template in your ESP system. At email build time, ESP makes a call for each rawbox in each email that is being generated. A rawbox call is very similar to an adbox, but instead of returning an image, the recommendations server returns raw HTML.
>The ESP needs a way to take this HTML and include it in the email when it is sent. This approach allows us to track performance of recommendations in emails, test them in the normal way with a recommendation, and continue tracking on the site.
>Sample rawbox URL:
>
>```
>http://CLIENT_CODE.tt.omtrdc.net/m2/CLIENT_CODE/ubox/raw?mbox=myAreaName&amp;mboxContentType=text/html&amp;mboxPC=UNIQUE_ID_PER_EMAIL&amp;mboxSession=UNIQUE_ID_PER_EMAIL&amp;mboxXDomain=disabled&amp;entity.id=productId&amp;mboxDefault=DEFAULT_URL&amp;mboxHost=MBOX_HOST
>```

>Change the uppercased values per client/recommendation combination.


>| Parameter |Value |Example |
>|---|---|---|
>| mbox |MY_EMAIL_NAME |back-to-school-email |
>| mboxContentType |text|html |text|html |
>| mboxPC |UNIQUE_ID_PER_EMAIL |228722993 |
>| mboxSession |UNIQUE_ID_PER_EMAIL |387873-3878783 |
>| mboxXDomain |disabled |disabled |
>| entity.id |PRODUCT_ID |1298-3989 |
>| mboxDefault |DEFAULT_URL |http://www.domain.com/welcome.html |
>| mboxHost |MBOX_HOST |http://domain.com/ |

>**Option 2: Using the Download-Only Template** 
>Set up a recommendation as usual, but choose **download only** in the presentation section instead of a template and mbox combination. Then in the ESP, tell the ESP what recommendation ID you created. The ESP accesses the recommendation data via API. This data shows which items should be recommended for a particular category or key item, such as the item abandoned in the cart. The ESP then stores this data, connects it with their own look and feel, displays information about each item, and then delivers that in the emails. With this option, the recommendations server cannot directly track the performance of a recommendation or split traffic across multiple algorithm/template combinations. 
>For more information about the download API, see [Using the Recommendations Download API](r_Using_the_Recommendations_Download_API.md#reference_09DA9D1AB3884CEC9144C7BDD07AB30A). 
