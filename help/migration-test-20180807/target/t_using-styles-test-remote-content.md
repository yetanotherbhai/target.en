---
description: You can test your remote content using styles.
keywords: remote offer;create remote offer;test remote content;test remote content using styles
seo-description: You can test your remote content using styles.
seo-title: Use Styles to Test Remote Content
solution: Target
title: Use Styles to Test Remote Content
topic: Standard
uuid: e91a48b1-c960-4e8f-ba4e-f8edf64076a9
index: y
internal: n
snippet: y
translate: y
---

# Use Styles to Test Remote Content

Ensure that you need a remote offer. See [Create Remote Offers](c_about-remote-offers.md#concept_657016A0E6174C22B89036E9C8A0170F) to help guide your decision. There are several methods for testing experiences with remote offers. 
Use styles if you plan to test only the appearance of your existing remote content. Use styles in an offer to hide, show, or reformat existing elements of your remote content.

>1. Create a stylesheet for each experience, which changes the formatting of elements, or makes some elements invisible.
>1. Create offers referring to the new stylesheets.
>1. Position an mbox in your dynamic page, to override any standard page styles.

>       The last style referenced will control the appearance of the elements after it.
>1. Now create an A/B or Multivariate activity or test, and load the offers into the mbox for each experience.
