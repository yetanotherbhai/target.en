---
description: Activities can be targeted in many different ways to achieve different results.
keywords: target levels;levels of targeting;targeting levels;activity level target;experience level target;location level target;mbox level target;target mbox;conversion level target;target success metric;target execution order;execution order
seo-description: Activities can be targeted in many different ways to achieve different results.
seo-title: Levels of Targeting
solution: Target
subtopic: Multivariate Test
title: Levels of Targeting
topic: Standard
uuid: 124eef1a-33eb-4376-ae16-1ceff13b653c
index: y
internal: n
snippet: y
translate: y
---

# Levels of Targeting

You can target an activity so only certain people enter the activity, or you can include everyone in an activity and direct them to different experiences based on the targeting criteria. You can also add targeting criteria to locations to show content only some of the times that a location is loaded on a page.
Activity-level and experience-level targeting are the most commonly used.
Details on each type, as well as the order in which targets are executed, are provided below.

* [Activity-Level Target](c_target_levels.md#section_8303EF718F724346ABCBB16790933BF4)
* [Experience-Level Target](c_target_levels.md#section_615AFDBD0D2E4C1ABF35F3903077795F)
* [Location/Mbox-Level Target](c_target_levels.md#section_B1E8CCF14F5E4E69AA71D70D295DBAC9)
* [Other Target Levels](c_target_levels.md#section_CAA76CDA663446DFBEB1DC81909FBAAA)
* [Order of Targeting Execution](c_target_levels.md#section_8E073D372D9F4A7CA49364C013CA5FE1)


## Activity-Level Target {#section_8303EF718F724346ABCBB16790933BF4}

Target at the activity level to determine which people to allow or disallow into the entire activity. Users have equal opportunity to see any experience if no other targeting conditions are set.
If not allowed in, the visitor sees default content or can be included in other activities approved for the same locations. See the [Campaign Entry Process flowchart](http://marketing.adobe.com/resources/help/en_US/tnt/pdf/campaign_entry_process.png) for information about how visitors are chosen for an activity. 
Activity-Level Target Options:
Choose `**display mboxes**` to allow a visitor to enter the activity at any display mbox in the entire activity. The visitor's first view of any display mbox in the activity causes the user to be counted as a visitor in reports. A display mbox is any mbox that displays offer content in the activity. 
Choose an individual mbox to require a visitor's first visit to the activity to be this mbox. If the visitor does not view this mbox, he or she is not accepted into the activity.
Targeting to multiple mboxes at the activity level creates an "or condition" for entry into the activity. You can target to multiple mboxes by first choosing an mbox from the drop-down list, then clicking `add targeting location` under the set of targeting categories. 
**Warning!** Do not use success metric targeting at the activity level. The result is an infinite loop that locks the visitor out of the activity. 

## Experience-Level Target {#section_615AFDBD0D2E4C1ABF35F3903077795F}

Target at the experience level to allow everyone into the activity but deliver different experiences based on specified rules.
Experience-level targeting is typically used with a landing page (and is called a "landing page campaign" in `Target Classic`). With targeting rules on each experience, you can show relevant content to different groups in the same mbox on your site. For example, you might want to "welcome" visitors from each of your affiliates. You can set up an experience targeting activity that shows a different welcome message in an mbox based on which affiliate a visitor reached your site from. This can all be managed in one activity. As your list of affiliates changes, you can remove or add new experiences targeted to that affiliate source (using the Traffic Sources category) and choose an offer for each experience that uses that affiliate's logo or special offer. 
You can also choose to target a percentage of your traffic to an experience. At the experience level, click the population target icon. An option to choose percentage appears.
Targeting experiences to specific visitor segments overrides the default randomization that shows each experience an equal number of times.
**Tip:** It is recommended that, if you want to change percentages or greatly affect the flow of people into each experience, you should create or copy a new activity. Otherwise, if you change the percentages on different experiences, it will take a few days for the data to normalize again if many purchasers are return visitors. For example, if your A/B test is split 50/50, and then you change the split to 80/20, for the first few days after that change, the results might look skewed. If the average time to conversion is high, meaning it takes someone several hours or even days to make a purchase, these delayed conversions can affect the reports. So, in that first experience where the number went from 50 to 80, and the average time to conversion is two days, only people from the 50% of the population are converting on the first day of the test, although today 80% of the population is entering the experience. This makes it look like the conversion rate plummeted, but it will normalize again after these 80% of people have the two days to convert. 

## Location/Mbox-Level Target {#section_B1E8CCF14F5E4E69AA71D70D295DBAC9}

Target at the mbox level to determine whether to show specific content to visitors who are allowed into the activity and who get to see this experience. If the visitor does not meet the targeting conditions for a given mbox, default content is shown.
Mbox-level targeting gives you the ability to show content in an mbox only when the visitor meets certain real-time conditions. This is most often used when an mbox is on every page of a site (the logo for example) or on a templated page like a category or product page. You can uniquely identify specific instances of those mboxes (one instance of an mbox on a template page, or one instance of the global mbox) so that you can display specific content in it. For example, if you wanted to promote a special offer on all women's products but not on any men's products, you would either need a specially named mbox on the women's pages, or you can use mbox-level targeting to limit when the content in the campaign actually displays. For example, if the women's pages all share the same URL structure, you could target on the word "women" existing in the current page URL.
Mbox-level targeting is checked first. In other words, a visitor must match the mbox-level targeting before being considered to see a display mbox, and therefore be eligible for the activity.
When you target at the mbox level, targeting criteria is evaluated each time the mbox is requested. So, if a visitor navigates to category 1, 5, and 20, in that order, the visitor would see content for category 1, the special offer for category 5, and then the default content for category 20. Browsing to category 5, enters the visitor into the campaign, so even if default content is displayed for category 20 next, the visitor is still in this activity.
Targeting at the mbox level is not used nearly as often as targeting at the activity or experience level, but is useful for situations in which you want to ensure that certain visitors continue to see content that makes sense, in the context of global mboxes.

>[!NOTE]
>
>Mbox-level targeting takes precedence over other levels, For example, if there is a conflict between an experience-level target and an mbox-level target, the mbox-level target will win.



## Other Target Levels {#section_CAA76CDA663446DFBEB1DC81909FBAAA}


* **Conversion Level Target :** Target on conversion if you want to limit what counts as a conversion beyond merely reaching an mbox. Conversion-level targeting could be used for something like only tracking conversions if the user spent over $100, or signed up for a particular offer or product. 

* **Target Display to a Success Metric:**Target display to a success metric if you want to only count visitors who might have, or have not seen a previous success metric. By default, success metrics are not consecutive, meaning you do not have to reach success metric 1 to be counted on success metric 2. This targeting allows you to override that default. This can be used to track people's progress through a strict order or registration funnel. For example, people are only counted on a "billing page" success metric if they have first gone through the "shipping page" success metric. In the targeting widget, select `success metrics`, the name of the previous success metric, and then `has been seen` from the next drop-down list. 



## Order of Targeting Execution {#section_8E073D372D9F4A7CA49364C013CA5FE1}

An activity can have targeted experiences and non-targeted experiences. To determine which experience a visitor sees, `Target` first tries to match the visitor to one of the targeted experiences. Each experience is attempted in order: the one listed top in the activity is attempted first, and so on. The visitor sees the first experience that matches. If the visitor does not match any experience's targeting criteria, then that visitor sees a non-targeted experience, if there is one. If there is more than one non-targeted experience, the non-targeted traffic is split evenly across all of the experiences. If there is no non-targeted experience, then the visitor is not included in the test. 
See [How Target Decides Who Sees What Content](c_target_whoseeswhat.md#concept_014AB6795D2D4B6EB5E45A226A4FF7E9). 
