---
description: List of frequently asked questions (FAQs) about global mboxes.
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;global;global mbox
seo-description: List of frequently asked questions (FAQs) about global mboxes.
seo-title: Global mbox Frequently Asked Questions
solution: Target
title: Global mbox Frequently Asked Questions
topic: Standard
uuid: c3667bdb-1fea-4562-b1e9-1a3309e99809
index: y
internal: n
snippet: y
translate: y
---

# Global mbox Frequently Asked Questions

The following sections contain more information: 


* [ Can I have more than one global mbox if my...](../../../c_seting_up_target/c_implementing_target/c_understanding-global-mbox/c_global-mbox-frequently-asked-questions.md#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD) 

* [ How do I pass revenue data on a Target global...](../../../c_seting_up_target/c_implementing_target/c_understanding-global-mbox/c_global-mbox-frequently-asked-questions.md#section_17AEA933BADA4D169CCEDF5833C41306) 



## Can I have more than one global mbox if my Target account is set across multiple domains? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

Only one global mbox is supported across your account. 

You can limit where your activities run by adding URL rules to your activities. For more information, see [ Include the Same Experience on Similar Pages](../../../c_experiences/t_temtest.md#task_2539D51A18044F82B0D9895636546781). 

You could also pass a parameter on the page using `[ targetPageParams()](../../../c_seting_up_target/c_implementing_target/c_target-atjs-implementation/cmp_at.js_Functions.md#reference_B235C9F6DA79449ABE3E23F914FEABAE)` and then select those parameters in the "configure URL" section in the [!UICONTROL  Visual Experience Composer] (VEC) or by adding the parameters as "refinements" in the Form-Based Experience Composer. 

## How do I pass revenue data on a Target global mbox? {#section_17AEA933BADA4D169CCEDF5833C41306}

To collect revenue and order information on the target-global-mbox, "mbox parameters" must be sent to Target. These parameters are name/value pairs used to send more information to Target. Target automatically looks for these parameters (reserved names) to populate revenue data. 

For the ` orderConfirmPage`, you should pass in ` orderTotal`, ` orderId`, and ` productPurchasedId`. For more information, see [ Create an Order Confirmation mbox - mbox.js](../../../c_seting_up_target/c_implementing_target/t_mbox_download/t_orderconfirm_create.md#task_0036D5F6C062442788BB55E872816D82). 

These same parameters must be sent to the target-global-mbox via ` targetPageParams()`. For more information, see [ Passing Parameters to a Global mbox](../../../c_seting_up_target/c_implementing_target/c_understanding-global-mbox/c_pass_parameters_to_global_mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5). 

You'll also want to add targeting to the conversion piece so that Target only counts conversions on the target-global-mbox when the order confirmation page has been viewed, as shown below: 

![](../../../assets/revenue1.png) 

The Site Pages section illustrated above contains the following selections: Current Page, URL, contains, orderconfirm. 

![](../../../assets/revenue2.png) 

The options in the above illustration include the following settings: 


* **What do you want to measure with this activity: **Revenue 

* **Default View for Reporting: **Revenue Per Visitor (RPV) 

* **What action was taken by your audience to indicate your goal has been reached? **Viewed an mbox, target-global-mbox 


