---
description: If you use certain Target Classic advanced features, be aware of the considerations in this topic when transitioning to Target Standard/Premium.
keywords: advanced feature;expression target;Monitoring Campaigns;plug-ins;plug in;plugins;migration;migrate from target classic to target standard
seo-description: If you use certain Target Classic advanced features, be aware of the considerations in this topic when transitioning to Target Standard/Premium.
seo-title: Advanced Feature Considerations
solution: Target
title: Advanced Feature Considerations
topic: Premium
uuid: 5936fed6-9ae0-46ce-a2f8-9518deebe725
index: y
internal: n
snippet: y
translate: y
---

# Advanced Feature Considerations

The advanced feature considerations phase is complete when you have either:


| Step |Task |
|---|---|
|  ![](../a4t/graphics/step1_icon.png)  |Migrated the advanced features you use. |
|  ![](../a4t/graphics/step2_icon.png)  |Deemed the advanced features unnecessary for migration. |

This section contains the following information:

* [Target Classic Advanced Feature Considerations](c_trans-advanced-feature-considerations.md#section_4FD5C0D0E39F42B884C27B5FB1445A29)
* [Recently Added Features](c_trans-advanced-feature-considerations.md#section_62F97EE4775C45ED8719E6D227361982)
* [Next Step](c_trans-advanced-feature-considerations.md#section_12FA2E28030C4D4CB174E5C74962D4C4)


## Target Classic Advanced Feature Considerations {#section_4FD5C0D0E39F42B884C27B5FB1445A29}

***I use Expression Targets*** 
Consider any of the following alternatives:

* Migrate your Expression Targets to [Profile Scripts](c_script_profile_attributes.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)
* Use the [customized audiences capabilities](t_create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558) in Target Standard/Premium to re-create your audiences
* Use [Analytics](https://marketing.adobe.com/resources/help/en_US/reference/) or [Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/c_aam_home.html)

***I use Monitoring Campaigns*** 
Similar to plugins, in Target Standard/Premium, content from multiple activities can be returned to a single mbox call. In Target Standard/Premium, the `Monitoring Campaign` you would have set up in Target Classic can be set up as an A/B or Experience Targeting activity with a low activity priority to ensure that content from other activities is seen by visitors. Visitors will still be incremented appropriately in the low-priority activities' reports. For more information, see [Priority](c_priority.md#concept_1780C11FEA57440499F0047DD6900E0F). 

## Recently Added Features {#section_62F97EE4775C45ED8719E6D227361982}

The following features have been recently added to Target Standard/Premium:

* [Target by Latitude and Longitude](c_geo.md#concept_5B4D99DE685348FB877929EE0F942670) 

* [Response Tokens](c_response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4) (Plug-ins in Target Classic) 

* [Remote Offers](c_about-remote-offers.md#concept_657016A0E6174C22B89036E9C8A0170F) 

* [Host group management](c_hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E) 



## Next Step {#section_12FA2E28030C4D4CB174E5C74962D4C4}

[Managing the Transition](c_trans-operational-milestones.md#concept_E0415E44D209458DA30D8A207D08048E) 
