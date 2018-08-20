---
description: Delete a custom algorithm name with the Delete Algorithm API call.
seo-description: Delete a custom algorithm name with the Delete Algorithm API call.
seo-title: Deleting a Custom Algorithm
solution: Target
title: Deleting a Custom Algorithm
topic: Recommendations
uuid: f49ac3ab-8f00-4901-b5c3-c9e80ed18df7
index: y
internal: n
snippet: y
translate: y
---

# Deleting a Custom Algorithm



>>[!NOTE]
>>
>>If you try to delete a custom algorithm that has not yet been created, you receive an error stating that the algorithm does not exist.
>


>Syntax: 

>
>```
>https://recommendations.omniture.com/rest?action=algorithm.delete 
>&client=clientCode&clientToken=51dafdf4-f825-4581-a7c0-8ce9db31bd31 
>&algorithmName=sampleCustomAlgorithm
>```


>Where: 

>**recommendations.omniture.com** is the domain for the current recommendations environment you are using. 

>**clientCode** is your client code. 

>**51dafdf4-f825-4581-a7c0-8ce9db31bd31** is the client token that is displayed on the settings page. The token shown is a sample; yours will be different. 

>**sampleCustomAlgorithm** is the name of the algorithm created in [ Naming a Custom Algorithm ](../../c_rec_mng_recs/c_Creating_a_Custom_Algorithm/r_Naming_a_Custom_Algorithm.md#reference_EFEF6E3495F746948AEF178875B87CCB). 
>[!MORE_LIKE_THIS]
>
>* [ Naming a Custom Algorithm ](r_Naming_a_Custom_Algorithm.md#reference_EFEF6E3495F746948AEF178875B87CCB)
>* [ Uploading Custom Algorithm Data ](r_Uploading_Custom_Algorithm_Data.md#reference_F905A439D6034D15AAE171CD69909742)
