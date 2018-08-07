---
description: Create a feed to insert information about your products or services into Recommendations.
keywords: ftps;ftp;csv;Google product feed;ftp with ssl
seo-description: Create a feed to insert information about your products or services into Recommendations.
seo-title: Create Feed
solution: Target
title: Create Feed
topic: Premium
uuid: 43689475-82fa-4aaa-8244-a2bce4321aee
index: y
internal: n
snippet: y
translate: y
---

# Create Feed


>1. From within the Target interface, click ** `Recommendations` ** > ** `Feeds` ** > ** `Create Feed` **.

>       ![Step Result](graphics/CreateFeed.png) 
>1. Specify a descriptive name for your feed.
>1. Select a ** `Source Type` **.

>       For information about Google Product Feed and CSV feed types, see [Feeds](c_feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3). 
>1. Specify a Report Suite, or the URL or FTP location where the feed can be accessed.

>       If you select URL, specify the URL.
>       If you select FTP, provide the FTP server information, the login credentials, the filename, and the FTP directory. You have the option to use FTP with SSL (FTPS) for more secure uploads.
>1. Click the ** `Next` ** arrow to display the `Schedule` options.

>       ![Step Result](graphics/CreateFeedSchedule.png) 
>1. Select an update option:

>    
>    * Daily
>    * Weekly
>    * Biweekly
>    * Never Do not schedule an update. Choose this if you do not want this feed to run.


>1. Specify the time you want your feed to run.

>       This option is based on the time zone used in your browser. If you want to use a time in a different time zone, you must calculate that time according to your time zone.
>1. Click the ** `Next` ** arrow to display the `Mapping` options, then specify how you want to map your data to `Target` definitions.

>       ![Step Result](graphics/CreatFeedMapping.png) 
>1. (Optional) If you want the feed to belong to an environment (host group), select the host group.

>       By default the feed belongs to all host groups. This ensures that items in this feed are available in any environment.

>       >[!NOTE]
>       >
>       >For more information, see[Hosts](c_hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E). 

>1. Click ** `Save` **.
