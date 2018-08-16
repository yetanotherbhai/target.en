---
description: Mobile viewports help you preview how your activities appear on screens of various sizes.
keywords: mobile viewports;responsive sites;responsive;viewport;CSS breakpoints;breakpoint;Responsive experience
seo-description: Mobile viewports help you preview how your activities appear on screens of various sizes.
seo-title: Mobile Viewports for Responsive Experiences
solution: Target
title: Mobile Viewports for Responsive Experiences
topic: Advanced,Standard,Classic
uuid: 3ff3f9ec-0655-4509-a401-6a4a108c2353
index: y
internal: n
snippet: y
translate: y
---

# Mobile Viewports for Responsive Experiences

The mobile viewport preview feature is designed for responsive sites. Use mobile viewports if your site is responsive and the same elements in your desktop page are used on your mobile page in a different configuration. If you have a separate mobile site with a separate structure, such as [!DNL  m.mysite.com], use a [ multipage activity ](../../c_experiences/c_multipage_activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48). 


>[!NOTE]
>
>Mobile viewports are not available if overlapped by a redirect offer overlay.



A viewport is defined by the size of the rectangle filled by a web page on your screen. It is the size of the browser window, minus the scrollbars and toolbars. Browsers use "CSS pixels." For many devices, such as those with retina screens, the viewport is smaller than the advertised device resolution. 

Below are the viewports and resolutions for some popular devices. Remember to use the viewport size in Target. 

|  Device  | Viewport Size  | Device Resolution  |
|---|---|---|
|  iPhone X  | 375w x 812h  | 1125w x 2436h  |
|  iPhone 8 Plus  | 414w x 736h  | 1080w x 1920h  |
|  iPhone 8  | 375w x 667h  | 750w x 1334h  |
|  iPhone 7 Plus  | 414w x 736h  | 1080w x 1920h  |
|  iPhone 7  | 375w x 667h  | 750w x 1334h  |
|  iPhone 6  | 375w x 667h  | 750w x 1334h  |
|  iPhone 6s  | 414w x 736h  | 1080w x 1920h  |
|  iPad Pro  | 1024w x 1366h  | 2048w x 2732h  |
|  iPad Third &amp;amp; Fourth Generation  | 768w x 1024h  | 1536w x 2048h  |
|  iPad Air 1 &amp;amp; 2  | 768w x 1024h  | 1536w x 2048h  |
|  iPad Mini  | 768w x 1024h  | 768w x 1024h  |
|  iPad Mini 2 &amp;amp; 3  | 768w x 1024h  | 1536w x 2048h  |
|  Nexus 6P  | 411w x 731h  | 1440w x 2560h  |
|  Nexus 5X  | 411w x 731h  | 1080w x 1920h  |
|  Google Pixel  | 411w x 731h  | 1080w x 1920h  |
|  Google Pixel XL  | 411w x 731h  | 1440w x 2560h  |
|  Google Pixel 2  | 411w x 731h  | 1080w x 1920h  |
|  Google Pixel 2 XL  | 411w x 731h  | 1440w x 2560h  |
|  Samsung Galaxy Note 5  | 480w x 853h  | 1440w x 2560h  |
|  LG G5  | 480w x 853h  | 1440w x 2560h  |
|  One Plus 3  | 480w x 853h  | 1080w x 1920h  |
|  Samsung Galaxy S9  | 360w x 740h  | 1440w x 2960h  |
|  Samsung Galaxy S9+  | 360w x 740h  | 1440w x 2960h  |
|  Samsung Galaxy S8  | 360w x 740h  | 1440w x 2960h  |
|  Samsung Galaxy S8+  | 360w x 740h  | 1440w x 2960h  |
|  Samsung Galaxy S7  | 360w x 640h  | 1440w x 2560h  |
|  Samsung Galaxy S7 Edge  | 360w x 640h  | 1440w x 2560h  |
|  Nexus 7 (2013)  | 600w x 960h  | 1200w x 1920h  |
|  Nexus 9  | 768w x 1024h  | 1536w x 2048h  |
|  Samsung Galaxy Tab 10  | 800w x 1280h  | 800w x 1280h  |
|  Chromebook Pixel  | 1280w x 850h  | 2560w x 1700h  |

Various websites list viewport sizes for popular devices. For example, see [ http://mediag.com/news/popular-screen-resolutions-designing-for-all/ ](http://mediag.com/news/popular-screen-resolutions-designing-for-all/) or consult the device maker's website. 

**Visual Experience Composer (2 of 2) (7:29)** 

The following demo video includes information about using the Visual Experience composer to work with mobile viewports: 


* Rename and duplicate an experience
* Create a redirect experience
* Target an activity to a single URL or a group of URLs
* Create a multi-page activity
* Preview and build experience for responsive websites
* Use overlays to highlight types of elements


>[!VIDEO](https://vimeo.com/qwUKEp8en_k) 

If you want to deliver an activity to people on a particular device, choose the appropriate audience for that device in the activity diagram. Use the Mobile Web Composer to edit the page in the activity for that device. If you want to run an activity across your entire digital experience and make sure it looks good across all devices, don't apply targeting, and use mobile viewports to preview the activity on each screen size. 

If you have a responsive site, typically your site is designed to open in a different view when accessed by a device with a specific screen size. Those screen sizes that trigger the new views are known as *CSS breakpoints*. Save your CSS breakpoints in Target so you can preview your experiences for each view you define. Each of these experiences is displayed in a mobile viewport in the Target interface. Open the view for each screen size by clicking that viewport along the top of the display. 

If your site is not responsive, you can still use the Mobile Web Composer to view a site if your activity is targeted to a specific device. 


>[!NOTE]
>
>While you can edit an experience from within mobile viewports, these changes apply to all viewports and devices, not just the viewport that you're working in. Similarly, editing an experience in the normal desktop view changes the page for all screen sizes, not just the desktop view. Currently, we don't support viewport-specific page changes.


