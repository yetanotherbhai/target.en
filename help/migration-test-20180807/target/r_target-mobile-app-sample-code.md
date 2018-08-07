---
description: This section includes sample code that can be used as a template for your app.
keywords: mobile app;mobile app sample code;target mobile app;mobile app base code;mobile app make request;mobile app load request
seo-description: This section includes sample code that can be used as a template for your app.
seo-title: Mobile App Sample Code
title: Mobile App Sample Code
topic: Target
uuid: 59e3ff6a-f7c9-48ae-a527-049c3fcf513e
index: y
internal: n
snippet: y
translate: y
---

# Mobile App Sample Code


The samples in this section contain code for iOS. The same patterns apply to Android. Android-specific syntax can be found in the [ Android SDK 4.x for Marketing Cloud Solutions ](https://marketing.adobe.com/resources/help/en_US/mobile/android/) guide. 

## Base Code {#section_C28B32AAAD28418E8A1B1A200B2CA7FE}


```
// make your request 
ADBTargetLocationRequest *myRequest = [ADBMobile targetCreateRequestWithName:@"heroBanner" 
defaultContent:@"default.png" 
parameters:nil]; 
 
// load your request 
[ADBMobile targetLoadRequest:myRequest callback:^(NSString *content) { 
// do something with content 
heroImage.image = [UIImage imageNamed:content]; 
}];
```


## Make Request {#section_0562BB3FE40E48F9A889883EC55775D6}


```
// make your request 
ADBTargetLocationRequest * 
<span class="varname"> myRequest </span> = [ADBMobile targetCreateRequestWithName:@ 
<span class="varname"> "heroBanner" </span> 
defaultContent:@ 
<span class="varname"> "default.png" </span> 
parameters: 
<span class="varname"> nil </span>];
```



<table id="table_A365058D16C54516994AA85BEECC5E13"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ADBTargetLocationRequest * <span class="varname"> myRequest </span> </span> </td> 
   <td colname="col2"> Replace <span class="varname"> myRequest </span> with the name of your <span class="codeph"> targetLocation </span> in the app. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> targetCreateRequestWithName:@" <span class="varname"> heroBanner </span>" </span> </td> 
   <td colname="col2"> <p>Replace <span class="varname"> heroBanner </span> with the name of your <span class="codeph"> targetLocation </span> in Target. </p> <p>This is the same as the mbox name. This hero banner appears in the Target interface.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> defaultContent:@" <span class="varname"> default.png </span>” </span> </td> 
   <td colname="col2"> Replace <span class="varname"> default.png </span> with the value the app uses if Target doesn’t respond. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> parameters: <span class="varname"> nil </span> </span> </td> 
   <td colname="col2"> Specify profile or mbox parameters. </td> 
  </tr> 
 </tbody> 
</table>

For more information, see [ iOS SDK 4.x for Marketing Cloud Solutions ](https://marketing.adobe.com/resources/help/en_US/mobile/ios/target.html). 

## Load Request {#section_FA4DBC18FC79436CA524925D4CD7992E}


```
// load your request 
[ADBMobile targetLoadRequest: 
<span class="varname"> myRequest </span> callback:^(NSString * 
<span class="varname"> content </span>) { 
// do something with content 
 
<span class="varname"> heroImage.image = [UIImage imageNamed:content] </span>; 
}];
```



<table id="table_29FF9213B6414945B1F7C54E2D55C6C2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> targetLoadRequest: <span class="varname"> myRequest </span> </span> </td> 
   <td colname="col2"> Replace <span class="varname"> myRequest </span> with the name of your <span class="codeph"> targetLocation </span> in the app. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> NSString * <span class="varname"> content </span> </span> </td> 
   <td colname="col2"> <p>Replace <span class="varname"> content </span> with the actual content coming back from Adobe. </p> <p> The string can be any of the following: 
     <ul id="ul_708C909B55EC48C7969A379EC7891165"> 
      <li id="li_BFB442C8AA7446FE8D4FE2EB263F94F1">XML</li> 
      <li id="li_E06C7493A47D47AC837E5F4C9A2EBD5D">JSON</li> 
      <li id="li_3E33A0FC56B64248B79D36D8E1D74292">A plain string</li> 
     </ul> </p> <p>Use this section of the code to define variables, set image paths, view controller flows, transaction points, or anything else you want to do.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> heroImage.image = [UIImage imageNamed:content]; </span> </span> </td> 
   <td colname="col2"> For example: Take content and set the path for a hero image </td> 
  </tr> 
 </tbody> 
</table>

For more information, see [ iOS SDK 4.x for Marketing Cloud Solutions ](https://marketing.adobe.com/resources/help/en_US/mobile/ios/target.html). 
