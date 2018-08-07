---
description: Modify the following code sample to open a targetLocation in your mobile app.
seo-description: Modify the following code sample to open a targetLocation in your mobile app.
seo-title: Open targetLocation in App
title: Open targetLocation in App
uuid: f8dab14f-bf61-4df3-b61b-cb2adde1364a
index: y
internal: n
snippet: y
translate: y
---

# Open targetLocation in App


>Place this code after the lifecycle metrics have been initiated. Replace the bold text with your own code to accomplish your use case.
>This example displays content in a dialog box.
>
>```
>ADBTargetLocationRequest * 
<span class="varname"> specialRequest </span> = [ADBMobile 
>targetCreateRequestWithName:@" 
<span class="varname"> 1.0_iOS_appDidFinishLaunchingWithOptions </span>" defaultContent:@" 
<span class="varname"> Default 
 >Content </span>" parameters: 
<span class="varname"> targetParams </span>]; 
> 
>[ADBMobile targetLoadRequest: 
<span class="varname"> specialRequest </span> callback:^(NSString *content) { 
>       
<b> <span class="varname"> UIAlertView *alert = [[UIAlertView alloc] initWithTitle:@"Adobe Target Content" message:content 
  >delegate:self cancelButtonTitle:@"Close" otherButtonTitles:@"Cancel", nil]; 
  >   [alert show]; </span></b> 
>      }];
>```



><table id="table_3E71F301D44644C7A60512C82DB41224"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> specialRequest </span> </span> </td> 
   <td colname="col2"> Specify the name of your <span class="codeph"> targetLocation </span> in the app. Used by developers in create and load calls. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 1.0_iOS_appDidFinishLaunchingWithOptions </span> </span> </td> 
   <td colname="col2"> <p>Create your own strong naming convention for <span class="codeph"> targetLocations </span>. It is suggested that you prefix the name with the app version #, platform, and method it is located in. This value is used when setting up the activity in Adobe Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Default Content </span> </span> </td> 
   <td colname="col2"> Specify the content the app uses if Target doesn’t deliver content. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetParams </span> </span> </td> 
   <td colname="col2"> Provide the dictionary of name value pairs to pass in to Target. </td> 
  </tr> 
 </tbody> 
</table>

