---
description: Adobe Target Standard operates as a simplified front end for Adobe Target. In order to operate correctly, what you do in Standard is synchronized with the Classic workflow.
seo-description: Adobe Target Standard operates as a simplified front end for Adobe Target. In order to operate correctly, what you do in Standard is synchronized with the Classic workflow.
seo-title: Syncing Between Target Standard and Classic
solution: Target
subtopic: Getting Started
title: Syncing Between Target Standard and Classic
topic: Standard
uuid: d3f2ab5f-52af-4f04-a685-d6f2b9b3f630
index: y
internal: n
snippet: y
translate: y
---

# Syncing Between Target Standard and Classic

This syncing makes possible the functionality of Target Standard.

>[!NOTE]
>
>Using Target Standard or Premium does not affect any Target Classic campaigns that might already be running.


Changes made in Target Classic can take several minutes to appear in Target Standard. For example, if you archive a campaign in Target Classic, that activity continues to display as active in Target Standard for approximately ten minutes.
**Activities** 
If you use both Standard and Classic, you will see the activities you create in Standard as read-only campaigns in the Campaigns list. This means you can view information about your activities, including reports, in the Classic interface, but you cannot make changes. The ** `Edit` ** button is disabled in Target Classic. 
Syncing activities with Target Classic is required, even for clients whose contract does not include access to the Target Classic workflow and functionality. If an activity does not sync correctly after you create it, a message displays, and the activity cannot be used. The syncing happens in the background without any action by the user.
As soon as an activity originally created in `Target Classic` is deactivated or deleted, it is deleted from `Target Standard/Premium`. Deleted activities originally created in `Target Classic` are not sent to `Archive` folder in `Target Standard/Premium`. The archived folder functionality applies only to activities created in `Target Standard/Premium`. 
**Audiences** 
Reusable segments created in Target Classic are available as audiences in Target Standard. This means that audiences that cannot be created at this time in Target Standard can be created as a segment in Target Classic and used in Target Standard. For example, you can create a geo-targeted segment in Target Classic and use it in Target Standard, although you cannot edit the synchronized audience in the Target Standard interface. Likewise, audiences created in Target Standard are available in Target Classic.
Segments created in Target Classic appear in Target Standard as read-only audiences. You can create a complex segment in Target Classic and use it as an audience in Target Standard. This was the intended use case.
Audiences created in Target Standard synchronize with Target Classic if you use the audience in an activity. However, the original definitions in the audience are not visible, and modifying them may cause them to disappear from Standard.
**Sync Errors** 
The following are common causes of synchronization errors:

* Special characters in the audience or activity name
* Exceeding Target activity limitations. See [Limitations](c_activities.md#section_049D4684403A4E07B998067EB8E9BE56). 

* Percentage defined for each experience does not add up to 100
* Lack of access to the specified report suite

Some mbox.js configurations in new accounts are out of synch between Target Standard and Target Classic. In Standard, the target-global-mbox is autocreated and target.js is downloaded by default. This is not the case in Classic. If implementing with DTM and using the Automatic library download, DTM pulls the file from Classic and so the auto-created global mbox will not fire, the VEC will not work, etc. The workaround is to go to Standard, click ** `Setup` **> ** `Implementation` **> ** `Edit mbox.js` ** and then click ** `Save` **. The Classic and Standard should synchronize as expected and DTM can be used to import the correct file. 
