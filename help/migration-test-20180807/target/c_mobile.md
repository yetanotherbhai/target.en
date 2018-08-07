---
description: Target mobile devices based on parameters such as mobile device, type of device, device vendor, screen dimensions (by pixels), and more.
keywords: targeting;mobile;target mobile;deviceatlas;iphone;iphone models;device atlas;displaywidth;display width;display height;type of device;displayheight;phone;tablet;device model
seo-description: Target mobile devices based on parameters such as mobile device, type of device, device vendor, screen dimensions (by pixels), and more.
seo-title: Mobile
solution: Target
title: Mobile
topic: Standard
uuid: d0b477f6-5d07-4267-b1e0-c0a1f4d5a1a6
index: y
internal: n
snippet: y
translate: y
---

# Mobile

For example, you might want to show different content to users who enter your page from a phone than you would if they visit from a computer. In that case, you could select the Mobile audience, then select the ** ` Is Mobile Phone` ** option, then add any specific details that are important to you, such as the type of phone, size of the screen (in pixels), and so on. 
Mobile targeting is delivered by [ DeviceAtlas ](https://deviceatlas.com/device-data/user-agent-tester), a service of DotMobi. DeviceAtlas is a comprehensive database of mobile devices built on data compiled from numerous sources, including manufacturers and network operators. This data is then verified, cross-referenced, and validated to build a large and accurate mobile device database available. 

>[!NOTE]
>
>Device detection is accomplished by analyzing User-Agent strings. Some device manufacturers, such as Apple, disable this functionality by not providing enough information in the UA. For example, Apple devices don’t share device model-specific tokens in the UA. The result is that it is not possible to detect iPhone models (such as iPhone 5S, iPhone SE, iPhone 6, and so forth) using a simple keyword-based method. For more information and possible methods to work around this issue, see[ How DeviceAtlas Detects iPhone Models ](https://deviceatlas.com/blog/how-deviceatlas-detects-iphone-models) in the DeviceAtlas documentation. 


You can choose more than one mobile device parameter. Multiple selections are joined with an OR.
"displayWidth" is the name of the attribute you can use in profile scripts. The value is a number. This is not available directly for token replace in an offer; instead, it must first be set as a profile script.

1. In the ` Target` interface, click ** ` Audiences` ** > ** ` Create Audience` **. 

1. Name the audience.

1. Click ** ` Add Rule` ** > ** ` Mobile` **. 
   ![](../graphics/target_mobile.png) 

1. Click ** ` Select` **, then select one of the following options: 

    * Device Marketing Name
    * Device Model
    * Device Vendor
    * Is Mobile Device
    * Is Mobile Phone
    * Is Tablet
    * OS
    * Screen Height (px)
    * Screen Width (px)


   >[!NOTE]
   >
   >You can target by mobile device carrier using the[ Geo settings ](c_geo.md#concept_5B4D99DE685348FB877929EE0F942670). 


1. (Optional) Click ** ` Add Rule` ** and set up additional rules for the audience. 

1. Click ** ` Save` **. 


This video includes information about using audience categories.

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Creating Audiences </th> 
   <th colname="col3" class="entry"> 9:58 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/wV9lVTSOxMk/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/wV9lVTSOxMk/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Create audiences</li> 
      <li id="li_8529CB01E80B4C89B74287882AE0DA9D">Define audience categories</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

