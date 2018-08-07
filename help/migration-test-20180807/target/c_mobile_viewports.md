---
description: Mobile viewports help you preview how your activities appear on screens of various sizes.
keywords: responsive;mobile viewports;viewport;devices;mobile example;iphone
seo-description: Mobile viewports help you preview how your activities appear on screens of various sizes.
seo-title: Mobile Viewports for Responsive Experiences
solution: Target
title: Mobile Viewports for Responsive Experiences
topic: Premium
uuid: bd6447fd-0b79-45dc-8735-46398d709d49
index: y
internal: n
snippet: y
translate: y
---

# Mobile Viewports for Responsive Experiences

## Mobile Viewports for Responsive Experiences {#concept_8E45527C4ABC41D59AA3553BEDC76FA5}Mobile viewports help you preview how your activities appear on screens of various sizes.The mobile viewport preview feature is designed for responsive sites. Use mobile viewports if your site is responsive and the same elements in your desktop page are used on your mobile page in a different configuration. If you have a separate mobile site with a separate structure, such as `m.mysite.com`, use a [multipage activity](c_experiences.md#concept_277E096063E14813AC5D8EDFA1D2ED48). 

>[!NOTE]
>
>Mobile viewports are not available if overlapped by a redirect offer overlay.


A viewport is defined by the size of the rectangle filled by a web page on your screen. It is the size of the browser window, minus the scrollbars and toolbars. Browsers use "CSS pixels." For many devices, such as those with retina screens, the viewport is smaller than the advertised device resolution.
Below are the viewports and resolutions for some popular devices. Remember to use the viewport size in Target. 

| Device |Viewport Size |Device Resolution |
|---|---|---|
| iPhone6 |375w x 667h |750w x 1334h |
| iPhone6s |414w x 736h |1080w x 1920h |
| iPad |768w x 1024h |1536w x 2048h |
| Samsung Galaxy S4 |360w x 640h |1080w x 1920h |
| Samsung Galaxy Note 3 |360w x 640h |1080w x 1920h |

For more information about viewports, see [http://viewportsizes.com/](http://viewportsizes.com/). 
The following demo video includes information about using the Visual Experience composer to work with mobile viewports:


<table id="table_C56F4BE9B867463380013C584D97DAD2"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2">Visual Experience Composer (2 of 2)</th> 
   <th colname="col3" class="entry">7:29</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> <p> 
     <div width="550" class="video-iframe"> 
      <iframe src="https://www.youtube.com/embed/qwUKEp8en_k/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/qwUKEp8en_k/</iframe>
     </div> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_B17C3EFA4B664415AE0159E418FF45C4"> 
      <li id="li_916224D2105348BE93D60015B2F43D4F">Rename and duplicate an experience</li> 
      <li id="li_0FED234A3A054DEAB62C4F58BAB47F7F">Create a redirect experience</li> 
      <li id="li_79866ECECA2D4ACB9AE991B2922ADA84">Target an activity to a single URL or a group of URLs</li> 
      <li id="li_67ED273861FC493785AC049CC0B37E6A">Create a multi-page activity</li> 
      <li id="li_F4646D966373499DA6A32ED62411DF57">Preview and build experience for responsive websites</li> 
      <li id="li_4CA9280B227C4ACBB3EDDC23AB8ECCC3">Use overlays to highlight types of elements</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

If you want to deliver an activity to people on a particular device, choose the appropriate audience for that device in the activity diagram. Use the Mobile Web Composer to edit the page in the activity for that device. If you want to run an activity across your entire digital experience and make sure it looks good across all devices, don't apply targeting, and use mobile viewports to preview the activity on each screen size.
If you have a responsive site, typically your site is designed to open in a different view when accessed by a device with a specific screen size. Those screen sizes that trigger the new views are known as *CSS breakpoints*. Save your CSS breakpoints in Target so you can preview your experiences for each view you define. Each of these experiences is displayed in a mobile viewport in the Target interface. Open the view for each screen size by clicking that viewport along the top of the display. 
If your site is not responsive, you can still use the Mobile Web Composer to view a site if your activity is targeted to a specific device.

>[!NOTE]
>
>While you can edit an experience from within mobile viewports, these changes apply to all viewports and devices, not just the viewport that you're working in. Similarly, editing an experience in the normal desktop view changes the page for all screen sizes, not just the desktop view. Currently, we don't support viewport-specific page changes.


>## Mobile Viewport Configuration {#task_B4B161499DC0470584ED922A4D20FCAB}Configure any mobile viewports you want to make available when creating your experiences. 
<draft-comment otherprops="merge">
 target/t_mobile_viewport_configuration.xml
</draft-comment>This video includes information about setting up mobile viewports in the account preferences, beginning at 4:40 in the video.

<table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2">Account Preferences</th> 
   <th colname="col3" class="entry">7:33</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div width="550" class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/MJXhgxlP-KI/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/MJXhgxlP-KI/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Describe the account settings available in Target Standard</li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>


>1. Click ** `Setup` ** > ** `Preferences` **.
>1. In the Mobile Viewports Configuration section of the Account Preferences page, click ** `Add new` ** to add a mobile viewport.

>       To change the configuration of an existing mobile viewport, select that viewport, then click the Edit (pencil) icon.
>       ![](../graphics/viewpoert_add.png) 
>1. Type a name for the mobile viewport.

>       Give your mobile viewport a descriptive name that is easy to recognize. The name can be up to 36 characters long.
>1. Enter the screen size of the mobile device, both width and height.

>       The width can be between 150 and 968 pixels. The height can be between 150 and 1280 pixels.

>       >[!NOTE]
>       >
>       >For more information about viewports, see[http://viewportsizes.com/](http://viewportsizes.com/). 

>1. (Optional) Select the operating system of the device.

>       Options:
>    
>    * Android
>    * iOS
>    * Windows
>    * Symbian
>    * Blackberry

>       If you use the [Enhanced Experience Composer](c_experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) and choose an operating system, Target emulates that device when you view the page. If, for example, there is a different look and feel for Android than iOS on your responsive site, Target mimics that behavior. 
>1. Click ** `Save` **.
>## Create Responsive Experience {#task_D6332438B5EE48CCA8AF199270F1CAEF}Add mobile viewports to your Target activities to create responsive experiences for mobile screens. 
<draft-comment otherprops="merge">
 target/t_responsive_experience.xml
</draft-comment>
>1. Create an activity.
>1. In the Visual Experience Composer, click the ** `Settings` ** gear icon, then select ** `Add Mobile Viewports` **.
>1. Click the ** `Devices` ** icon, then enable each device that should have a mobile viewport.

>       ![](../graphics/MobileViewPorts.jpg) 
>       The mobile viewports are listed from smallest to largest according to width.
>1. Edit the mobile viewports as desired.

>       Any changes you make to the experience (for example, if you change the text in a heading) are applied to the experience on all devices.
>       Mouse over the name of a viewport to see the viewport's size.
>1. If desired, toggle between portrait and landscape modes by clicking the orientation icon.



>    <table id="table_63B970F1125A4577B87F8092DF5456F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Mode</th> 
   <th colname="col2" class="entry">Icon</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Portrait</p> </td> 
   <td colname="col2"> <p style="text-align: center;"><img href="../graphics/viewport_portrait.png" id="image_2BECFE10C51547759A3B4D95801F7155" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Landscape</p> </td> 
   <td colname="col2"> <p style="text-align: center;"><img href="../graphics/viewport_landscape.png" id="image_6E00C2EEA45B478484D9FD22776BE0BF" /> </p> </td> 
  </tr> 
 </tbody> 
</table>

>## Use Case: Target Two iPhone Versions {#task_CC3144BF5BA54034996E1D3DB0BC1A35}This use case shows how to configure experiences for two iPhone versions, iPhone 6 and iPhone 6 Plus, using the Mobile Viewports feature of Target Standard. 
<draft-comment otherprops="merge">
 target/t_viewports-two-iphones.xml
</draft-comment>
>1. In Target Standard, click ** `Setup` ** > ** `Preferences` **.
>1. In the Mobile Viewport Configuration section of the Preferences page, create mobile viewports for iPhone 6 and iPhone 6 plus.

>       Use the following settings for each viewport:


>       | Name |Width |Height |Operating System |
>       |---|---|---|---|
>       | iPhone 6 |375 |667 |iOS |
>       | iPhone 6 Plus |414 |736 |iOS |

>       ![](../graphics/iphoneviewportconfig.png) 
>1. Create an activity with the experience you would like to Target.
>1. Select the experience you want to target to visitors who access your site from an iPhone 6 or iPhone 6 Plus.
>1. When selecting your target, click ** `Create Audience` **, then configure an audience as shown in the image below:


>       ![](../graphics/iphoneaudiences.png) 
>       Because the phone could be rotated to landscape, requiring both height and width to be greater than 320 simultaneously creates a condition that only the 6 and 6 Plus would be able to meet, when combined with the iPhone Device Model.
>1. Click ** `Save` **.
>1. Continue setting up your activity as you normally would.
