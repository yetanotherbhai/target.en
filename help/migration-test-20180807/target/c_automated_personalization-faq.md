---
description: List of frequently asked questions (FAQs) about Automated Personalization (AP).
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;automated personalization
seo-description: List of frequently asked questions (FAQs) about Automated Personalization (AP).
seo-title: Automated Personalization FAQ
solution: Target
title: Automated Personalization FAQ
topic: Premium
uuid: 394469a0-db31-460d-97c5-91bc067c0af3
index: y
internal: n
snippet: y
translate: y
---

# Automated Personalization FAQ

This section contains the following information:

* [ How can I compare Automated Personalization to a default experience... ](c_automated_personalization-faq.md#section_46C1A620A2384C2C8392D6716DD18495)
* [ What are best practices to set up an Automated Personalization... ](c_automated_personalization-faq.md#section_E155B26282BE49B58EA2683413D11DE6)
* [ What are some limits in Automated Personalization? ](c_automated_personalization-faq.md#section_08BA09ED51B547299963C94FE6417CFA)


## How can I compare Automated Personalization to a default experience? {#section_46C1A620A2384C2C8392D6716DD18495}

There is no turn-key option of comparing AP to a default experience. However, as a workaround, if a default offer or experience exists as part the overall activity, to understand its baseline performance you can click the “Control” segment in the reports and locate that particular offer in the resulting offer-level report. The conversion rate recorded for this offer can be used to compare with the conversation rate of the entire “Random Forest” segment. This helps to compare how the machine is doing compared to the default offer.

## What are best practices to set up an Automated Personalization activity? {#section_E155B26282BE49B58EA2683413D11DE6}

In general, when the models have been built as indicated by the checkmarks on all of the offers, it is time to start cutting back on the random percentage.
If you want the best information as to how well Automated Personalization is performing, you should first scale back to a 50% random - 50% targeted setting. This will give the most accurate estimate of the lift.
However, if you are already happy with the lift, you can scale the random component down to an amount that depends on the time scale over which you expect things to change. For example, if it takes one week to build a good model using 90% random traffic, if you scale the random traffic to 90% / 2 weeks = 45%, it will take two weeks to fully incorporate changes into the models. If you do not expect that the offers or response to the campaign will change on a one-month, time-scale then you, in the above example, can scale the traffic down to 90% / 4 weeks = 22.5% random.

## What are some limits in Automated Personalization? {#section_08BA09ED51B547299963C94FE6417CFA}


* Target has a hard limit of 30,000 experiences. This is crucial.

* In our empirical understanding of Automated Personalization, we have never observed or understood more than 17 or so modeling groups. Consider this when designing reporting groups.


