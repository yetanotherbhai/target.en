---
title: Privacy
description: Processes and settings that allow you to use Target in compliance with applicable data privacy laws.
seo-description: Adobe Target has enabled processes and settings that allow you to use Target in compliance with applicable data privacy laws.
seo-title: Privacy compliance in Adobe Target
product: Target
uuid: b064c997-a76d-4670-b4d0-830eb631a4f4
index: y
internal: n
snippet: y
translate: y
---

# Privacy

Adobe Target has enabled processes and settings that allow you to use Target in compliance with applicable data privacy laws.

## Collection of IP Address

The IP address of a visitor to your website is transmitted to an Adobe Data Processing Center (DPC). Depending on the network configuration for the visitor, the IP address does not necessarily represent the IP address of the visitor’s computer. For example, the IP address could be the external IP address of a Network Address Translation (NAT) firewall, HTTP proxy, or Internet gateway. Target doesn't store any IP addresses of the user or any Personally Identifiable Information (PII). IP addresses are used only by Target for the duration of the session (in-memory, never persisted). 

## Replacement of Last Octet of the IP Address

Adobe has developed a new “privacy by design” setting that can be enabled by Adobe Customer Care for Adobe Target. When this setting is enabled, the last octet (the last portion) of the IP address is immediately hidden when the IP address is collected by Adobe. This anonymization is performed prior to any processing of the IP address, including before an optional geo-lookup of the IP address. 

When this feature is enabled, the IP address is made sufficiently anonymous so it is no longer identifiable as personal information. As a result, Adobe Target can be used in compliance with data privacy laws in countries that do not permit the collection of personal information. Obtaining city-level information will likely be significantly impacted by the obfuscation of the IP address. Obtaining region- and country-level information should only be slightly impacted. 

There is also a setting available to obfuscate the entire IP address. 

Contact [Adobe Customer Care](https://helpx.adobe.com/contact/enterprise-support.ec.html#target) to enable the IP obfuscation feature. 

## GeoSegmentation

If you enable the replacement of the last octet of the IP address, the remaining values of the IP address can be analyzed using reports in Adobe Target. If the last octet of the IP address has not been obfuscated, then the full IP address can be analyzed in Adobe Target. You can use the GeoSegmentation feature to map out visitor location by geographic area. GeoSegmentation data is granular only to the city level or zip code level, and not to the individual level. 

If IP addresses are completely obfuscated, GeoSegmentation and geo targeting is not available. 

## Opt-Out Link

You can add an opt-out link to your sites to enable visitors to opt-out of all counting and content delivery. 

1. Add the following link to your site: `href="http://clientcode.tt.omtrdc.net/optout">Your Opt Out Language Here</>` 

1. Replace the `clientcode` text with your client code, and add the text or image to be linked to the opt-out URL.
Any visitor who clicks this link is not included in any mbox requests called from their browsing sessions until they delete their cookies, or for two years, whichever comes first. This works by setting a cookie for the visitor called `disableClient` in the `clientcode.tt.omtrdc.net` domain. 

Even if you use a first-party cookie implementation, the provided opt-out is set via a 3rd-party cookie. If the client is using a first-party cookie only, Target checks whether an opt-out cookie is set. 
