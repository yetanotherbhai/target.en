---
description: List of frequently asked questions (FAQs) about recommendations designs.
keywords: recommendations;frequently asked questions;faq
seo-description: List of frequently asked questions (FAQs) about recommendations designs.
seo-title: Design FAQ
solution: Target
title: Design FAQ
title_outputclass: premium
topic: Premium
uuid: 1612ec23-5910-48b3-af56-83b767c75c1f
badge: assets/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Design FAQ

This section contains the following information: 


* [ Why isn't category showing in the design? I'm using $entity1.categoryId.](c_template_faq.md#section_073309B8051049C7953D396A93EA0713) 

* [ How should I change a design to get an instant...](c_template_faq.md#section_28EE35A5B10B47ECA4A332F0E5B2598F) 

* [ How can I capture key information for display in the...](c_template_faq.md#section_F08043B14BA24BC8815FEF25F4F84C39) 

* [ Which version of Velocity is used?](c_template_faq.md#section_28F00E15A4A54A768782A3F5BB0CDB21) 

* [ How do I replace an existing entity value with a...](c_template_faq.md#section_B88F2C2925DC4508974B2F8B13F961CB) 

* [ Can I use a profile script in a Recommendations design...](c_template_faq.md#section_6BD55203984A4D80A0C6F241AD7806DF) 



## Why isn't category showing in the design? I'm using $entity1.categoryId. {#section_073309B8051049C7953D396A93EA0713}

Category ID can't be displayed in the design. Because multiple categories can be stored, the system wouldn't know which category to display. 

## How should I change a design to get an instant update? {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

Altering the design that is currently in use takes a while to update. To change the design instantly, create a new design, select it in the campaign, and save the recommendation. 

## How can I capture key information for display in the design? Example: If we want to display the key product's category, how would I code that value in the velocity design? {#section_F08043B14BA24BC8815FEF25F4F84C39}

The `$key. * ` value` *` parameter captures most of the key product's information to display within the design. Example: If you want to display the key product's thumbnail, you would use ` $key.thumbnailURL`. 

## Which version of Velocity is used? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

Version 1.5 with no additional tools or libraries added in. Basic Velocity functionality is available. 

## How do I replace an existing entity value with a blank? For example, an item's entity.message needs to be cleared when a promotion ends. {#section_B88F2C2925DC4508974B2F8B13F961CB}

Sending in a JavaScript nonbreaking space seems to do this. Have the developers send in ` \u00A0` as the value. Example: ` entity.message=\u00A0`.You might consider having that be the default value when no value is present instead of a null. 

## Can I use a profile script in a Recommendations design? {#section_6BD55203984A4D80A0C6F241AD7806DF}

Yes. However, you must add a backslash (\) before the $ in the profile script name. 
