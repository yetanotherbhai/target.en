---
description: There are several frequently asked questions about templates.
seo-description: There are several frequently asked questions about templates.
seo-title: Template FAQ
solution: Target
title: Template FAQ
topic: Recommendations
uuid: e7bfea49-1c38-4d39-8cf6-70b6dc04c35d
index: y
internal: n
snippet: y
translate: y
---

# Template FAQ

**Why isn't category showing in the template? I'm using ` $entity1.categoryId`.** 

Category ID can't be displayed in the template. Since multiple categories can be stored, the system wouldn't know which category to display. 

**How should I change a template to get an instant update?** 

Altering the template that is currently in use takes a while to update. To change the template instantly, create a new template, select it in the campaign, and save the recommendation. 

**How can we capture key information for display in the template? Example: If we want to display the key product's category, how would we code that value in the velocity template? ** 

The `$key. *` value`*` parameter captures most of the key product's information to display within the template. Example: If you want to display the key product's thumbnail, you would use ` $key.thumbnailURL`. 

**Which version of Velocity is used?** 

Version 1.5 with no additional tools or libraries added in. Basic Velocity functionality is available. 

**How do I replace an existing entity value with a blank? For example, an item's entity.message needs to be cleared out when a promotion ends.** 

Sending in a JavaScript nonbreaking space seems to do this. Have the developers send in ` \u00A0` as the value. Example: ` entity.message=\u00A0`.You might consider having that be the default value when no value is present instead of a null. 
