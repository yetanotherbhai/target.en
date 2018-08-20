---
description: After you create a custom algorithm name , you can upload a list of the recommended items to display for a specific key item when you use that custom algorithm.
seo-description: After you create a custom algorithm name , you can upload a list of the recommended items to display for a specific key item when you use that custom algorithm.
seo-title: Uploading Custom Algorithm Data
solution: Target
title: Uploading Custom Algorithm Data
topic: Recommendations
uuid: 2d16e96e-3f48-48ce-ad7f-afcbfb0b0087
index: y
internal: n
snippet: y
translate: y
---

# Uploading Custom Algorithm Data



>>[!NOTE]
>>
>>If you try to upload recommendations data to a custom algorithm that has not yet been created, you receive an error stating that the algorithm does not exist.
>


>The syntax for the Upload API is: 



><table id="table_853ED10367174FB281CC451DAA3B1ED6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <codeblock>
       https://recommendations.omniture.com/rest?action=entity.recommendations.upload 
      &amp;client=clientCode&amp;environmentId=184868&amp;clientToken=51dafdf4-f825-4581-a7c0-8ce9db31bd31 
      &amp;algorithmName=sampleCustomAlgorithm&amp;recommendations=&lt;recommendations&gt;&lt;recommendation&gt; 
      &lt;key&gt;1&lt;/key&gt;&lt;entityId&gt;2&lt;/entityId&gt;&lt;entityId&gt;3&lt;/entityId&gt; 
      &lt;entityId&gt;4&lt;/entityId&gt;&lt;/recommendation&gt;&lt;/recommendations&gt;&nbsp; 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

>Where: 

>**recommendations.omniture.com** is the domain for the current recommendations environment you are using. 

>**clientCode** is your client code. 

>**environmentId** is the ID of the environment you want to use. You can specify a valid ID ( ` environmentId=8`), or ` ALL` to use all host groups ( ` environmentId=ALL`). If ` environmentId` is not included then it defaults to the default Production environment. 

>**51dafdf4-f825-4581-a7c0-8ce9db31bd31** is the client token that is displayed on the [!UICONTROL  Settings] page. The token shown is a sample; yours will be different. 

>**sampleCustomAlgorithm** is the name of the algorithm created in [ Naming a Custom Algorithm ](../../c_rec_mng_recs/c_Creating_a_Custom_Algorithm/r_Naming_a_Custom_Algorithm.md#reference_EFEF6E3495F746948AEF178875B87CCB). 

>**<key>...</key>** is what the recommendation is based on. This can either be an entity/product id or a category value. These values must be known ` entity.id` and ` entity.categoryId` values, meaning that Recommendations already has display data for the entities. The key values can also be left blank for non-keyed recommendations such as overall top sellers or top viewed. 

>** <entityId>...</entityId>** is the entity to be recommended for the specified key. This setting must be a known ` entity.id` value, meaning that the recommendations server already has display data for the entities. 

>**<recommendations>. ..</recommendations>** is the XML representation of the recommendations that will display. A ` <recommendation>` must be included for each key. The ` <entityId>` values are the recommended items for the specified key. In proper XML syntax, the recommendation might look similar to the following: 

>
>```
><recommendations> 
> 
><recommendation> 
> 
><key>1</key> 
> 
><entityId>4</entityId> 
> 
><entityId>2</entityId> 
> 
><entityId>3</entityId> 
> 
></recommendation> 
> 
><recommendation> 
> 
><key>2</key> 
> 
><entityId>5</entityId> 
> 
><entityId>3</entityId> 
> 
><entityId>6</entityId> 
> 
></recommendation> 
> 
>... 
> 
></recommendations> 
>```

>[!MORE_LIKE_THIS]
>
>* [ Naming a Custom Algorithm ](r_Naming_a_Custom_Algorithm.md#reference_EFEF6E3495F746948AEF178875B87CCB)
>* [ Deleting a Custom Algorithm ](r_Deleting_a_Custom_Algorithm.md#reference_B54C085BEAFB47B383DF127C06777D1F)
