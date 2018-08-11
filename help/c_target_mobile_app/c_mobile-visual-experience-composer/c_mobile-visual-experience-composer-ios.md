---
description: Target's new SDK Library allows developers to do a one-time setup on their iOS mobile apps and enable marketers to use the capabilities of the Mobile Visual Experience Composer (VEC).
keywords: mobile vec;mobile visual experience composer;mobile experience composer options;setting up;ios;apple
seo-description: Target's new SDK Library allows developers to do a one-time setup on their iOS mobile apps and enable marketers to use the capabilities of the Mobile Visual Experience Composer (VEC).
seo-title: iOS - Setting Up the Mobile App
solution: Target
title: iOS - Setting Up the Mobile App
topic: Standard
uuid: fcc45ab1-a51a-4f9b-86c0-376e424d637a
index: y
internal: n
snippet: y
translate: y
---

# iOS - Setting Up the Mobile App


>[!NOTE]
>
>The Visual Experience Composer for Native Mobile Apps is currently offered as a Beta feature available to select customers to obtain feedback to help us improve the feature before making it available to all customers. Please talk to your Customer Success Manager or Adobe Client Care to participate in this Beta program.



This section contains the following information: 


* [ Include the Mobile SDK &amp;amp; the Target Library ](c_mobile-visual-experience-composer-ios.md#section_FD969A63C4F74603B2F31B82881422A4) 

* [ Set Up Target Views on Your Mobile App ](c_mobile-visual-experience-composer-ios.md#section_78600DB29862478E8DF2A5EC3CAC1CB0) 



## Include the Mobile SDK &amp; the Target Library {#section_FD969A63C4F74603B2F31B82881422A4}


1. Download and unzip the package (LINK, TBD), then place the ` AdobeTargetMobileLibrary` subdirectory into the same directory in which you put the source code. 

1. Open your Objective-C application project in XCode. 

1. Add the embedded libraries: 

    1. Find the subdirectory in the Finder where you've unzipped the package. Drag and drop following four files from [!DNL  AdobeTargetMobileLibrary] subdirectory in your project: 

    
<ul class="simplelist"> 
 <li> <span class="filepath"> ADBAdobeTargetMobile.h </span> </li> 
 <li> <span class="filepath"> AdobeTargetMobileLibrary_iOS.a </span> </li> 
 <li> <span class="filepath"> SocketRocket.framework </span> </li> 
 <li> <span class="filepath"> SocketCluster_ios_client.framework </span> </li> 
</ul>




       >[!NOTE]
       >
       >Make sure Copy Items if Needed is selected.


    1. Select your project in left pane, select the ** [!UICONTROL  General] ** tab in the ** [!UICONTROL  Embedded Binaries] ** section, then click the ** [!UICONTROL  Plus Sign ( + )] **. 

    1. Select the following files from the drop-down list: 

    
<ul class="simplelist"> 
 <li> <span class="filepath"> SocketRocket.framework </span> </li> 
 <li> <span class="filepath"> SocketCluster_ios_client.framework </span> </li> 
</ul>



    1. Click ** [!UICONTROL  Add] **. 

       The following image shows the final state of the General tab: 

       ![](../../assets/mobile-vec-ios 1.png) 


1. Add the required iOS system libraries (if not already present in your project): 

    1. In your application project settings, click ** [!UICONTROL  General] **, click ** [!UICONTROL  Linked Frameworks and Libraries] **, then click the ** [!UICONTROL  Plus Sign ( + )] **. 

    1. Select the system framework by searching for the following libraries, selecting them, then clicking the ** [!UICONTROL  Add] ** button. Repeat the previous step and this step for each of the other frameworks and C++ library. 

    
<ul class="simplelist"> 
 <li> <span class="filepath"> UIKit.framework </span> </li> 
 <li> <span class="filepath"> WebKit.framework </span> </li> 
 <li> <span class="filepath"> UserNotifications.framework </span> </li> 
 <li> <span class="filepath"> libstdc++.tbd </span> </li> 
</ul>



       The following image shows the final state of the build settings: 

       ![](../../assets/mobile-vec-ios 2.png) 


1. Change build settings for Mobile VEC: 

    1. In your application project settings, click ** [!UICONTROL  Build Settings] **. 

    1. In the search dialog, search for "Other Linker Flags." 

    1. In the column under your application, add the following string to the current linker options (ensure that you copy the string exactly as below): 

       ` -ObjC` 


1. Add the deeplink handler: 

    1. In your application project settings, click ** [!UICONTROL  Info] **. 

    1. Under ** [!UICONTROL  URL Types] **, click the triangle to open it, then click on the Plus Sign to add a new field. 

    1. Add the following information: 

    
<ul class="simplelist"> 
 <li> Identifier: <span class="codeph"> com.adobe.sdktest </span> </li> 
 <li> URL Schemes: <span class="codeph"> vectester </span> </li> 
 <li> Role: <span class="codeph"> Editor </span> </li> 
</ul>



    1. Click away from your application project settings > ** [!UICONTROL  General] **. 

    1. Click back on your application project settings > ** [!UICONTROL  Info] ** to ensure your settings were saved. 

       With the example URL type, the URL scheme for your app will be: 

    
       ```
       vectester://com.adobe.sdktest
       ```



1. In XCode, open your [!DNL  AppDelegate] file. 

1. At the top of the file, add the following line at the end of your imports. If you are using Swift, add this line to your bridge header file. 

   ` #import "ADBAdobeTargetMobile.h"` 

1. Get the following information from your SDK integration values. If you do not know of these values, talk directly with your Adobe customer representative. 


    * Your Target Client Code 

    * Your Marketing Cloud Organization ID 



1. In your [!DNL  AppDelegate] file, add the following line to ` AppDelegate::application:didFinishLaunchingWithOptions:`. If the delegate function is not defined, create it and add the following line for Objective-C or Swift application, respectively: 


   ```
   // CONFIGURATION LINE FOR OBJECTIVE C ONLY: 
    [ADBAdobeTargetMobile SDKV5_SHIM_initShimWithClientCode:@"ExampleTargetClientCode" 
                                         withMarketingOrgId:@"ExampleOrgID" 
                                withAuthoringClusterUrlBase:TARGET_AUTHORING_URL_CLUSTER_US]; 
     
     
   // CONFIGURATION LINE FOR SWIFT ONLY: 
   ADBAdobeTargetMobile.sdkv5_SHIM_initShim(withClientCode: "ExampleTargetClientCode", 
                                                    withMarketingOrgId: "ExampleOrgID", 
                                                    withAuthoringClusterUrlBase: TARGET_AUTHORING_URL_CLUSTER_US);
   ```


   As a example, the method should resemble the following sample: 


   ```
   // EXAMPLE OVERRIDE METHOD FOR OBJECTIVE C ONLY: 
   - (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions { 
        // Override point for customization after application launch. 
        [ADBMobile collectLifecycleData]; 
        [ADBMobile setDebugLogging:YES]; 
     
   [ADBAdobeTargetMobile SDKV5_SHIM_initShimWithClientCode:@"ExampleTargetClientCode" 
                                         withMarketingOrgId:@"ExampleOrgID" 
                                withAuthoringClusterUrlBase:TARGET_AUTHORING_URL_CLUSTER_US]; 
      return YES; 
   } 
     
   // EXAMPLE OVERRIDE METHOD FOR SWIFT ONLY: 
   func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey : Any]? = nil) 
   { 
        ADBAdobeTargetMobile.sdkv5_SHIM_initShim(withClientCode: "ExampleTargetClientCode", 
                                                    withMarketingOrgId: "ExampleOrgID", 
                                                    withAuthoringClusterUrlBase: TARGET_AUTHORING_URL_CLUSTER_US) 
   }
   ```


1. In [!DNL  AppDelegate] file, add the following line to your [!DNL  AppDelegate::applicationWillResignActive]. If the delegate function is not defined, create it and add the following line. 


   ```
   // RESIGNATION LINE FOR OBJECTIVE C ONLY: 
   [ADBAdobeTargetMobile SDKV5_SHIM_applicationWillResignActive:application]; 
     
   // RESIGNATION LINE FOR SWIFT ONLY: 
   ADBAdobeTargetMobile.sdkv5_SHIM_applicationWillResignActive(application)
   ```


   As a example, the method should resemble the following sample: 


   ```
   // EXAMPLE OVERRIDE METHOD FOR OBJECTIVE C ONLY: 
   - (void)applicationWillResignActive:(UIApplication *)application { 
       // Sent when the application is about to move from active to inactive state. This can occur for certain types of temporary interruptions (such as an incoming phone call or SMS message) or when the user quits the application and it begins the transition to the background state. 
       // Use this method to pause ongoing tasks, disable timers, and invalidate graphics rendering callbacks. Games should use this method to pause the game. 
       [ADBAdobeTargetMobile SDKV5_SHIM_applicationWillResignActive:application]; 
   } 
     
   // EXAMPLE OVERRIDE METHOD FOR SWIFT ONLY: 
   func applicationWillResignActive(_ application: UIApplication) { 
       ADBAdobeTargetMobile.sdkv5_SHIM_applicationWillResignActive(application) 
   }
   ```


1. Add the following line to ` AppDelegate::applicationDidBecomeActive`. If the delegate function is not defined, create it and add the following line: 


   ```
   // ACTIVATION LINE FOR OBJECTIVE C ONLY: 
   [ADBAdobeTargetMobile SDKV5_SHIM_applicationDidBecomeActive:application]; 
     
     
   // ACTIVATION LINE FOR SWIFT ONLY: 
   ADBAdobeTargetMobile.sdkv5_SHIM_applicationDidBecomeActive(application)
   ```


   As a example, the method should resemble the following sample: 


   ```
   // EXAMPLE OVERRIDE METHOD FOR OBJECTIVE C ONLY: 
   - (void)applicationDidBecomeActive:(UIApplication *)application { 
       // Restart any tasks that were paused (or not yet started) while the application was inactive. If the application was previously in the background, optionally refresh the user interface. 
       [ADBAdobeTargetMobile SDKV5_SHIM_applicationDidBecomeActive:application]; 
   } 
     
     
   // EXAMPLE OVERRIDE METHOD FOR SWIFT ONLY: 
   func applicationDidBecomeActive(_ application: UIApplication) { 
       ADBAdobeTargetMobile.sdkv5_SHIM_applicationDidBecomeActive(application) 
   }
   ```


1. Add the following line to the beginning of ` AppDelegate:application:openURL`. If the delegate function is not defined, create it and add the following line. 


   ```
   // URL HANDLER LINE FOR OBJECTIVE C ONLY: 
   [ADBAdobeTargetMobile SDKV5_SHIM_handleDeepLink:url]; 
     
     
   // URL HANDLER LINE FOR SWIFT ONLY: 
   ADBAdobeTargetMobile.sdkv5_SHIM_handleDeepLink(url)
   ```


   As a example, the method should resemble the following sample: 


   ```
   // EXAMPLE OVERRIDE METHOD FOR OBJECTIVE C ONLY: 
   - (BOOL)application:(UIApplication *)application openURL:(NSURL *)url options:(NSDictionary<NSString *, id> *)options { 
       [ADBAdobeTargetMobile SDKV5_SHIM_handleDeepLink:url]; 
       return YES; 
   } 
     
   // EXAMPLE OVERRIDE METHOD FOR SWIFT ONLY: 
   func open(_ url: URL, options: [UIApplication.OpenExternalURLOptionsKey : Any] = [:], completionHandler completion: ((Bool) -> Void)? = nil) { 
       ADBAdobeTargetMobile.sdkv5_SHIM_handleDeepLink(url) 
   }
   ```


1. Build and run your application and use it to test Mobile VEC capabilities. 



## Set Up Target Views on Your Mobile App {#section_78600DB29862478E8DF2A5EC3CAC1CB0}

In this section, we will first demonstrate how to properly insert these calls with two different demonstration applications and discuss general guidelines on how to properly insert the Target View API calls for any iOS app. In iOS, all the Target Views are defined relative to the ` UIViewController` in which they appear. So, unlike Android, the insertion of ` TargetViews` are limited to the following calls. 

The Adobe Mobile VEC Extension auto-generates names for your ` UIViewControllers` to interact within the Mobile VEC framework, based upon the class name of the subclassed ` UIViewController`. If you want to override these names, you can call following method in ` viewWillAppear` of the ` ViewController`. 


```
// TARGET VIEW LINE FOR OBJECTIVE C ONLY 
[ADBAdobeTargetMobile setTargetView:@"exampleViewController"]; 
  
  
// TARGET VIEW LINE FOR SWIFT ONLY 
ADBAdobeTargetMobile.setTargetView("exampleViewController")
```


The Adobe Mobile SDK also exposes an alternate method for developers to target custom views during runtime. As a developer, you must ensure that the views are named uniquely. Call following method before adding view to the ` superview`: 


```
// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN OBJECTIVE C 
CustomPopupView *popupView = [[CustomPopupView alloc] initWithFrame:CGRectMake(0, 0, 300, 200)]; 
[ADBAdobeTargetMobile setTargetView:@"myCustomPopupView" forView:popupView]; 
  
  
// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN SWIFT 
let popupView = CustomPopupView.init(frame: CGRect(x: 0, y: 0, width: 300, height: 200)) 
ADBAdobeTargetMobile.setTargetView("myCustomPopupView", for: popupView)
```

