---
description: Use the Algorithm Name API to create a name for a custom algorithm.
seo-description: Use the Algorithm Name API to create a name for a custom algorithm.
seo-title: Naming a Custom Algorithm
solution: Target
title: Naming a Custom Algorithm
topic: Recommendations
uuid: 424f3e5c-5112-4d09-a1d2-84c10e9cac78
index: y
internal: n
snippet: y
translate: y
---

# Naming a Custom Algorithm


>The syntax for the Algorithm Name API is: 



><table id="table_422B676A4D4143DC9BFC0C72E3D606BF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <codeblock>
       https://recommendations.omniture.com/rest?action=algorithm.upload 
      &amp;client=clientCode&amp;clientToken=51dafdf4-f825-4581-a7c0-8ce9db31bd31 
      &amp;algorithmName=sampleCustomAlgorithm&amp;keyType=currentitem 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

>Where: 

>** recommendations.omniture.com** is the domain for the current recommendations environment you are using. 

>**clientCode** is your client code. 

>**51dafdf4-f825-4581-a7c0-8ce9db31bd31** is the client token that is displayed on the settings page. The token shown is a sample; yours will be different. 

>**sampleCustomAlgorithm** is the name of the algorithm as it will be displayed in the algorithm selection dropdown when you create or edit a recommendation. You can name it whatever you like, but it has a 255 character limit. This name is used when you upload the recommendation data, as shown in [ Uploading Custom Algorithm Data ](../../c_rec_mng_recs/c_Creating_a_Custom_Algorithm/r_Uploading_Custom_Algorithm_Data.md#reference_F905A439D6034D15AAE171CD69909742). 

>**keyType** is an optional parameter that allows users to specify their own key for custom algorithms. If no value is passed, it is assumed to be the current item. The value can be changed to any ` user.attribute` or ` profile.attribute` defined in the A/B and multivariate testing and targeting interfaces, or to one of the following (case and space sensitive): 

>
>* ` currentitem`
>* ` lastvieweditem`
>* ` lastpurchaseditem`
>* ` mostvieweditem`
>* ` favoritecategory`
>* ` currentcategory`


>For example, if the profile script was named ` abandonedCartItem`, the parameter for this API would be ` keyType=user.abandonedCartItem`. 

>After you use this API, the new name appears immediately as an algorithm type. 
>[!MORE_LIKE_THIS]
>
>* [ Uploading Custom Algorithm Data ](r_Uploading_Custom_Algorithm_Data.md#reference_F905A439D6034D15AAE171CD69909742)
>* [ Deleting a Custom Algorithm ](r_Deleting_a_Custom_Algorithm.md#reference_B54C085BEAFB47B383DF127C06777D1F)
