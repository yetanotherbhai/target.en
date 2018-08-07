---
description: Each visitor is counted as either a new or returning visitor.
keywords: Overview and Reference
seo-description: Each visitor is counted as either a new or returning visitor.
seo-title: New or Returning Visitor
solution: Target
title: New or Returning Visitor
topic: Standard
uuid: 3ccc095e-e958-4989-941f-01c8c8e6a0cc
index: y
internal: n
snippet: y
translate: y
---

# New or Returning Visitor

A visitor is included in the "Visitor: New" segment if it is the visitor's first time visiting the site, the first time since clearing cookies, or if the visitor's profile lifetime has expired since their last visit. For information about profile lifetime, see [Visitor Profile Lifetime](c_visitor_profile_lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD). 
The visitor is included in the "Visitor: Returning" segment if the user previously visited the site, left for at least 30 minutes, and returned to the site again with the same cookies. As long as a visitor returns within their profile lifetime, they will be a returning visitor.
If these two segments are applied to an activity, the "new visitor" segment and the "return visitor" segment do not always add up to the total number of visitors. A visitor can be counted as new, and then return and get counted as a return visitor. That visitor is still counted as only a single visitor in the activity's overall visitor count.

