---
description: Target uses the criteria you set up for your activity to determine who sees what content, based on a specific order of operations.
seo-description: Target uses the criteria you set up for your activity to determine who sees what content, based on a specific order of operations.
seo-title: How Target Decides Who Sees What Content
solution: Target
title: How Target Decides Who Sees What Content
topic: Standard
uuid: cca19ae3-c5c4-4881-953d-f8e5e4ce4381
index: y
internal: n
snippet: y
translate: y
---

# How Target Decides Who Sees What Content

Target does not automatically split traffic if you have two experiences with the same rules-based targeting. If the visitor qualifies for Experience B and Experience C based on the targeting, then 100% of those users go into the first experience (in this case, Experience B). 

The same is true for experiences with no targeting. In the following example, if the user does not qualify for Experience A or B, then they are always placed into Experience C (in other words, no one will make it to Experience D): 


* Experience A - 10% of visitors 

* Experience B - Only show Fri/Sat/Sun 

* Experience C - (not targeting) 

* Experience D - (not targeting) 



One way around this is to create a profile script that generates a random number from 1...100 and then set up the targeting this way: 


* Experience A - 10% of visitors 

* Experience B - Only show Fri/Sat/Sun 

* Experience C - (random number profile has value 1..50) 

* Experience D - (random number profile has value 51..100) 



You can add percentage targeting to Experience C (set Experience C to 50% of traffic and leave Experience D without any targeting) to make sure visitors get into all experiences. 

If your activity has multiple experiences that are set up with specific percentage targets, for example four experiences each configured to receive 25% of the traffic, a random number is generated and that number determines the experience shown to a visitor. In this example, if the random number is 30, the visitor would receive the second experience because 30 is between 25 and 50, the second range when dividing 100 into 25% chunks. 
