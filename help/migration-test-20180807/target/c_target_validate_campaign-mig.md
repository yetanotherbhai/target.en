---
description: After you create a targeted campaign, you should verify that it works as expected. target/c_target_validate_campaign.xml
keywords: Targeting
seo-description: After you create a targeted campaign, you should verify that it works as expected. target/c_target_validate_campaign.xml
seo-title: Validating a Targeted Campaign
solution: Target
title: Validating a Targeted Campaign
topic: Premium
uuid: 7f64fec4-0987-46e4-94d9-3c4b60de8f87
index: y
internal: n
snippet: y
translate: y
---

# Validating a Targeted Campaign

## Validating a Targeted Campaign {#concept_804F9A67161447579091BF818BDF0A5E}After you create a targeted campaign, you should verify that it works as expected. 
<draft-comment otherprops="merge">
 target/c_target_validate_campaign.xml
</draft-comment>## Validate Targeting to URL or Referring URL Parameters {#task_378FB18E8C7244CDA8C1D029DBACBAEE}Follow these steps to validate targeting to a URL or referring URL parameters. 
<draft-comment otherprops="merge">
 target/t_target_validate_url.xml
</draft-comment>
>1. Append the targeting parameters and values to the end of the URL, or referring page URL.

>       The example below shows an appended target condition where your targeting condition is met when the keyword equals "chairs":
>       `http://www.yourcompany.com/asp/feature_item.asp?keyword=chair&amp;categoryId=45` 
>1. Confirm that you see the correct content for the targeting condition.
>1. Delete cookies and confirm you do not see the content when you do not meet the targeting condition.
>1. If segments filters are set, confirm reports correctly capture the URL parameter values.
>## Validate Targeting to New or Returning Visitors {#task_C9BF77B62B4943A7BF1DC37AA752001C}Follow these steps to validate targeting to new or returning users. 
<draft-comment otherprops="merge">
 target/t_target_validate_visitors.xml
</draft-comment>
>1. In your browser, delete all mbox cookies.

>       This allows you to appear as a new user (new visitor).
>1. Browse to the targeted campaign, experience or mbox, or conversion mbox.
>1. Verify you see the expected content for a new user.
>1. Test the expected content (or lack of content ) shows for a returning visitor.

>       Close your browser, and reopen it. Do not delete your mbox cookies. Confirm that as a returning visitor, you see the expected content.
>       A "returning visitor" is someone who is on the website for at least their second session.
>       **Tip:** To imitate being a return visitor for testing purposes, there must be at least 30 minutes of inactivity between site views. When a second session has started, a new `sessionID` appears in the `mboxDebug` popup utility. 
>1. If segments filters are set, confirm reports correctly capture the parameter values.
>## Validate Targeting to Profile Parameters {#task_FEE3A70A4F944B35958CF4B5DA82EB0D}Follow these steps to validate targeting to profile parameters. 
<draft-comment otherprops="merge">
 target/t_target_validate_profile.xml
</draft-comment>
>1. Perform any action that sets the required profile value.
>1. Close and reopen your browser.

>       Do not delete any files. The profile value is connected to your browser cookie.
>1. Return to the page where the campaign should display.
>1. Confirm that the correct offer content is shown to you.
>1. If segments filters are set, that reports correctly capture the parameter values.
