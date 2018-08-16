---
description: You can choose to view reports by different counting methodologies to understand how your activities affect your users across their lifetimes or during a single session.
keywords: Targeting
seo-description: You can choose to view reports by different counting methodologies to understand how your activities affect your users across their lifetimes or during a single session.
seo-title: Counting Methodology
solution: Target
title: Counting Methodology
uuid: e94185d7-ed48-40f7-b70c-0f516c8adb63
index: y
internal: n
snippet: y
translate: y
---

# Counting Methodology

Counting methodology is supported for the following activity types: 


* A/B Test 

  As an exception, Auto-Target A/B activities support only the default "Visit" counting methodology. 

* Experience Targeting (XT) 

* Multivariate Test (MVT) 

  For the MVT Element contribution report, Target does not support Activity Impressions for Revenue Metric types. 

* Recommendations 



Only the default counting methodology (Visits) is currently supported for Automated Personalization (AP) activities. 

You can view reports by the following counting methodologies: 


* **Visitor:** A unique participant in the activity, for the life of the activity. A person will be counted as a new entrant if he or she visits the site from a new computer or a new browser; deletes the cookie; or converts and returns to the activity with the same cookie. An entrant is identified by the PCID in the visitor's mbox cookie. If the PCID changes, the person is considered a new visitor. 

* **Visit:** A unique participant in an experience during a single 30-minute browser session. If a conversion is achieved or a visitor comes back to the site after being away at least 30 minutes, a returning visitor counts as a new visit. A visit is identified by the ` sessionID` in the visitor's mbox cookie. When the ` sessionID` changes, the visit is considered new. 



* **Impression/Page View:** Counted each time a visitor loads any page of the activity. A single visit might include several impressions of, for example, your homepage. 




>[!NOTE] {class="- topic/note "}
>
>Usually, counts are determined by cookies and session activity. However, if you reach the final conversion point of an activity and then re-enter the activity, you are considered a new entrant and a new visit to the activity. This is true even if your PCID and ` sessionID` values do not change. 


