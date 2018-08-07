---
description: Modify the following code sample to add a custom data dictionary to your mobile app.
keywords: mobile app;mobile app data dictionary;target mobile app;mobilecustom dictionary;nsdictionary
seo-description: Modify the following code sample to add a custom data dictionary to your mobile app.
seo-title: Add a Custom Data Dictionary
title: Add a Custom Data Dictionary
topic: Target
uuid: f84c5a73-83cb-4195-9a01-2cf0dcfff0df
index: y
internal: n
snippet: y
translate: y
---

# Add a Custom Data Dictionary


>
>```
>NSDictionary * 
<span class="varname"> targetParams </span> = [[NSDictionary alloc] initWithObjectsAndKeys: 
>          @"true", @"loyaltyAccount", @"Adobe - San Francisco", 
>          @"office", 
<span class="varname"> @"prod",@"host" </span>,  
<span class="varname"> @"1067007",@"entity.id",@"fashion",@"entity.categoryId" </span>, nil]; 
>//nil to signify end of objects and keys. 
> 
>     ADBTargetLocationRequest *specialRequest = [ADBMobile 
>targetCreateRequestWithName:@"rulewisBanner" defaultContent:@"Default Message" 
>parameters: 
<span class="varname"> targetParams </span>];
>```



><table id="table_C562C47FA4F94FFFB5ECB4D7A6732052"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameters </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> NSDictionary * <span class="varname"> targetParams </span> </span> </p> <p> <span class="codeph"> parameters: <span class="varname"> targetParams </span> </span> </p> </td> 
   <td colname="col2"> Specify the object of name value pairs submitted with the <span class="codeph"> targetRequest </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> @"prod",@"host" </span> </span> </td> 
   <td colname="col2"> <p>Specify the name value pair for identifying QA vs Production. Use "dev" or "staging" as the value for the host in development or staging builds respectively.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> @"1067007",@"entity.id",@"fashion",@"entity.categoryId" </span> </span> </td> 
   <td colname="col2"> <p>Specify any parameters prefixed with " <span class="codeph"> entity. </span>" that are used in Adobe Recommendations. Talk to your consultant for more information. </p> </td> 
  </tr> 
 </tbody> 
</table>

