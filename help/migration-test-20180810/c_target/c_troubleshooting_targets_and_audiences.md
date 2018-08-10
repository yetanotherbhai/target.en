---
description: List of frequently asked questions (FAQs) about experience targeting and audiences.
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;targets;audiences
seo-description: List of frequently asked questions (FAQs) about experience targeting and audiences.
seo-title: Targets and Audiences Frequently Asked Questions
solution: Target
title: Targets and Audiences Frequently Asked Questions
topic: Standard
uuid: 47143a9e-d1db-4dbb-9667-e1459bb2a24c
index: y
internal: n
snippet: y
translate: y
---

# Targets and Audiences Frequently Asked Questions


## When building audiences, why are pre-built audiences under Target Library found under other categories? {#section_9EBF5B0F9DF94168A15B92B905CCF7E0}

The pre-built audiences in the Target Library category are legacy audiences and exist in other categories. As an example, the legacy Target Library &amp;gt; New Visitors audience has an updated counterpart: Visitor Profile &amp;gt; New Visitor. 

Best practice is to use the newer audiences because they have improved performance. Some customers might be using legacy, pre-built audiences, so they have not been removed from the Target interface. 

## How do I know how traffic will be split between audiences? {#section_067EEFB956E7465CBF77EC86834470AB}

By default, traffic is split evenly between experiences. However, you can specify [ percentage targets ](c_target_rulebased.md#concept_9D0C47368EB942C9A66CE03C6BD92412) for each experience. In this case, a random number is generated and that number is used to choose the experience to display. The resulting percentages might not exactly match the specified targets, but more traffic means that the experiences should be split closer to the target goals. 

## Which experience displays if a user qualifies for an activity that contains multiple experiences with multiple qualifying audiences? {#section_94A60B11212D48FD8AB0803C6C7E7253}

The user qualifies for the first experience/audience that displays on the activity's [!UICONTROL  Target] page. 

For example, in the following illustration, a user from California using a Windows device qualifies for both Experience A (Windows audience) and Experience C (California audience). This user would be shown Experience A because it displays in the list above Experience C on the Targets page. 

![](../graphics/audiences_order.png) 

## Why do names for the same audience in Target , Adobe Audience Manager (AAM), and the Audience Library in core services differ? {#section_F67E61A607B6444C8DAA4F99C3E95AED}

Audience names in [!DNL  Target] are unique; however, in [!DNL  AAM] and the [!DNL  Audience Library], you can have the same name for multiple audiences (if they are in different folders).When [!DNL  Target] encounters an audience name that corresponds to an [!DNL  AAM] or [!DNL  Audience Library] audience, [!DNL  Target] appends "#&lt;number&gt;" to the name. 

For example, you might see the following audiences: "PC Users" (in [!DNL  AAM]) and "PC Users #1" (in [!DNL  Target]). 

## Why can't I rename an audience? {#section_54E420556F534D20836E261E253D8B97}

Some Target audiences are predefined, such as "New Visitors" and "Returning Visitors." These predefined audiences cannot be renamed by users. 

## Why are all profile parameters not showing in the Target user interface? {#section_3CD947D15C984EE9AD19550220E0E8BD}

[!DNL  Target] has a limit of 50 unique profile attributes per mbox call. If you need to pass more than 50 profile attributes to [!DNL  Target], you can pass them using the [!UICONTROL  Profile Update] API method. For more information, see [ Profile Update ](https://www.adobe.io/apis/marketingcloud/target/docs/reference/profiles/profile-update.html) in the Adobe Target API documentation. 
