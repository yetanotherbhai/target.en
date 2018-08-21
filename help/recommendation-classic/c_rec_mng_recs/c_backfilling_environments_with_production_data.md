---
description: Backfilling other environments with entity recommendations from your production data is available as a setting update request through Adobe Client Care.
seo-description: Backfilling other environments with entity recommendations from your production data is available as a setting update request through Adobe Client Care.
seo-title: Backfilling Environments with Production Data
solution: Target
title: Backfilling Environments with Production Data
topic: Recommendations
uuid: 2774922d-8715-4c89-bba7-5aabb4fc6029
index: y
internal: n
snippet: y
translate: y
---

# Backfilling Environments with Production Data

This setting is useful for when you don't have sufficient behavioral data in lower environments (or host groups) to generate recommendation results. One consideration is you won't be able to deliver results from the lower environments as they will now show the chosen production environment results. Lower environment results can still be checked in the Recommendation CSV download. 

The backfill setting switches between using environment-specific product databases and replacing non-production environment results with production environment database results. Separate product and traffic databases are maintained for each environment determined by the Target host group and environment-specific data continues to be collected for each host group irrespective of this setting. 

The backfill setting doesn't affect any product or traffic data in the backend, it just affects the runtime, effectively overwriting the lower environment id at request time with the chosen environment id. Ingestion will still send the lower environment products to the lower environment while the backfill is set. As it's not affecting any data you can switch back and get the lower env results as if it had been set to the lower environment all along. 

The two options are: 


* No backfill. This is the default configuration. In this configuration, entity recommendation delivery will be according to the product relationship traffic in each host group / environment. Products seen in QA might not be seen in production (and vice versa). 

* Backfill set for production data to backfill to other environments. In this configuration your production entity recommendation delivery results will be "mirrored" to all other environments. This means you're only using production data and is useful when you don't have enough traffic to generate entity recommendation results in lower environments. 


