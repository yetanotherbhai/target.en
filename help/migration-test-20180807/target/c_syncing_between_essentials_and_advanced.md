---
description: Adobe Target Standard operates as a simplified front end for Adobe Target. In order to operate correctly, what you do in Standard is synchronized with the Classic workflow.
seo-description: Adobe Target Standard operates as a simplified front end for Adobe Target. In order to operate correctly, what you do in Standard is synchronized with the Classic workflow.
seo-title: Syncing Between Target Standard and Classic
solution: Target
title: Syncing Between Target Standard and Classic
topic: Advanced,Standard,Classic
uuid: 66da7108-3b87-490c-8774-35ae754bb666
index: y
internal: n
snippet: y
translate: y
---

# Syncing Between Target Standard and Classic

This syncing makes possible the functionality of Target Standard.
**Activities** 
If you use both Standard and Classic, you will see the activities you create in Standard as read-only campaigns in the Campaigns list. This means you can view information about your activities, including reports, in the Classic interface, but you cannot make changes. The ** `Edit` ** button is disabled in Classic. 
Syncing activities with Target Classic is required, even for clients whose contract does not include access to the Target Classic workflow and functionality. If an activity does not sync correctly after you create it, a message displays, and the activity cannot be used. The syncing happens in the background without any action by the user.
**Audiences** 
Reusable segments created in Target Classic are available as audiences in Target Standard. This means that audiences that cannot be created at this time in Target Standard can be created as a segment in Target Classic and used in Target Standard. For example, you can create a geo-targeted segment in Target Classic and use it in Target Standard, although you cannot edit the synchronized audience in the Target Standard interface. Likewise, audiences created in Target Standard are available in Target Classic.
Segments created in Target Classic appear in Target Standard as read-only audiences. You can create a complex segment in Target Classic and use it as an audience in Target Standard. This was the intended use case.
Audiences created in Target Standard synchronize with Target Classic if you use the audience in an activity. However, the original definitions in the audience are not visible, and modifying them may cause them to disappear from Standard.
