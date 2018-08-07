---
description: The category affinity feature automatically captures the categories a user visits and then calculates the user's affinity for the category so it can be targeted and segmented on. This helps to ensure that content is targeted to visitors who are most likely to act on that information.
keywords: affinity;category affinity
seo-description: The category affinity feature automatically captures the categories a user visits and then calculates the user's affinity for the category so it can be targeted and segmented on. This helps to ensure that content is targeted to visitors who are most likely to act on that information.
seo-title: Category Affinity
solution: Target
title: Category Affinity
topic: Standard
uuid: aaa31eaa-d299-4494-9d8c-b68bb3230792
index: y
internal: n
snippet: y
translate: y
---

# Category Affinity

This section contains the following information.

* [Passing Category Affinity Information into Target](c_category_affinity.md#section_B0C8E46EEBAC4549AD90352A47787D04)
* [Business Case for Category Affinity](c_category_affinity.md#section_D6FF913E88E6486B8FBCE117CA8B253B)
* [Example of Using Category Affinity](c_category_affinity.md#section_A4AC0CA550924CB4875F4F4047554C18)
* [Category Affinity Algorithm](c_category_affinity.md#section_8B86C7FF50294208866ABF16F07D5EB9)


## Passing Category Affinity Information into Target {#section_B0C8E46EEBAC4549AD90352A47787D04}

Whenever a user visits your site, profile parameters specific to the visitor are recorded in the `Target` database. This data is tied to the user's cookie. One particularly useful parameter is `categoryId`, an mbox parameter assigned on a product page. As the visitor continues to browse, or returns for another session, the categories of products a particular user views can be recorded. You can also record category information by passing it as the mbox parameter `user.categoryId` in any mbox (including a nested mbox), as a URL parameter `user.categoryId`, or in Target page parameters with a global mbox. See your account representative for more details. 
Separate categories with a comma to create separate categories. For example:

* `categoryId=clothing,shoes,nike,running,shox,nike shox turbo,nike shox turbo VI`
* `entity.categoryId=clothing,shoes,nike,running,shox,nike shox turbo,nike shox turbo VI`

Based on the frequency and recency of visits to your product categories, the category affinity (if any) a user has is recorded. Category affinity can be used to target populations for your activities.
You can use `user.categoryAffinities[]` in a profile script to return an array of the affinities that a visitor has populated. 

## Business Case for Category Affinity {#section_D6FF913E88E6486B8FBCE117CA8B253B}

A visitor's activity in one session, such as which category he or she views the most often, can be used for targeting in subsequent visits. Each category page a visitor views during a session is captured, and his or her "favorite" category is calculated based on a recency and frequency model. Then, every time the visitor returns to the home page, the hero image area can be targeted to show content related to that user's favorite category.

## Example of Using Category Affinity {#section_A4AC0CA550924CB4875F4F4047554C18}

Suppose you sell musical instruments online and want to target sales promotions on bass guitars to visitors who have already expressed interest in guitars in the past. Using category affinity, you can create offers that display only to visitors with this category affinity.

## Category Affinity Algorithm {#section_8B86C7FF50294208866ABF16F07D5EB9}

The category affinity algorithm works as follows:

* 10 points for first view
* 5 points for every one after
* At end of session divide all values by 2

For example, viewing categoryA then categoryB in one session results in A: 10, B: 5. When the session ends, you will have A: 5, B: 2.5. If you view the same items in the next session, the values change to A: 15 B: 7.5.
