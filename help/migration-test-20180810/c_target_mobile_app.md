---
description: Target can be used for mobile app optimization and personalization
keywords: offer;prefetch;iOS;android
seo-description: Target can be used for mobile app optimization and personalization
seo-title: Target for Mobile Apps
solution: Target
title: Target for Mobile Apps
topic: Advanced,Standard,Classic
uuid: 067db943-3f65-451a-9712-82f7bb047013
index: y
internal: n
snippet: y
translate: y
---

# Target for Mobile Apps

## Target for Mobile Apps {#concept_80126FF457724DE788CE37264A047559}Target can be used for mobile app optimization and personalizationThe following video provides a basic understanding of how Target mobile optimization can help your organization's achieve its goals: 

>[!VIDEO](https://vimeo.com/XyJY7qvrjM8) 

## Process {#section_0BF7302CF75A4B52B6D9279E90582D78}

The mobile app targeting process includes the following steps: 


1. [ How Target Works in Mobile Apps ](c_target_mobile_app.md#concept_6D18304659854571B7A5A71C33CD974C).
1. [ Enable Target in the SDK ](c_target_mobile_app.md#task_FCA99AD0785A44E995468776AE76FE91).
1. [ Create a Target Location and Success Metric ](c_target_mobile_app.md#task_A372B1C4C1814788BBBEE06259A0103B).
1. [ Send Custom User Data ](c_target_mobile_app.md#task_779D60C519C04109A6C1FFA1ACFBA59E).

>## How Target Works in Mobile Apps {#concept_6D18304659854571B7A5A71C33CD974C}The Adobe Mobile SDK contacts the Target server to get the content along with other data points to show the right experience to the user. 
<draft-comment otherprops="merge">
  target/c_mobile-how-target-works-mobile-apps.xml 
</draft-comment>
## Target Locations and Success Metrics {#section_A08AAB0ABA9C4568A5AFD4D27EF1CE74}

A *target location* is also referred to as an [ mbox ](c_getting_started.md#concept_85E01D9DD0B64BD3A138C2D3DB83BD57). An identified location in the app is enabled for testing or personalization (for example, the welcome message on the home screen). These locations are identified during the test creation process. 

A * [ success metric ](r_success_metrics.md#reference_D011575C85DA48E989A244593D9B9924)* is an action performed by the user that identifies if a specific activity was successful (such as signing up, making a purchase, booking a ticket, and so on). 

![](../graphics/mobile-target-location.png) 


* **Target Location:** The content that shows below the register button. This particular user is offered free shipping until 6 PM. This location can be reused across multiple Target activities to run A/B tests and personalization. 

* **Success Metric:** The action performed by the user where the user taps the register button.


**Understand How Target Works in the SDK** 

![](../graphics/how-target-mobile-works.png) 
>## Enable Target in the SDK {#task_FCA99AD0785A44E995468776AE76FE91}Add the Adobe Mobile Services SDK to your app. 
<draft-comment otherprops="merge">
  target/t_mobile_enable_target_in_sdk.xml 
</draft-comment>
>1. If you haven't installed the Adobe Mobile Services SDK in your app, use your Analytics or Marketing Cloud credentials and download the SDK from the [ Adobe Mobile Services ](https://mobilemarketing.adobe.com) website.

>1. Add the Adobe Mobile Services SDK to your app.

>       You can find the instructions under [ Core Implementation and Lifecycle ](https://marketing.adobe.com/resources/help/en_US/mobile/ios/dev_qs.html). 
>1. Add client code, timeout and enable SSL.

>       In the Marketing Cloud, open Mobile Services, then go to ** [!UICONTROL  Manage App Settings] ** > ** [!UICONTROL  SDK Target Options] **. 

>       Add your Target clientcode and timeout. The clientcode is unique to your account or company. The timeout is the time in number of seconds until which Target will wait for a response before showing the default content. Make sure the ** [!UICONTROL  Use HTTPS] ** option is checked in the Manage App Settings page in Adobe Mobile Services. If HTTPS isn't enabled, all calls in iOS9+ will be blocked unless you whitelist the Target server. 

>       ![](../graphics/mobile-clientcode.png) 
>1. After you’ve created/located your app, find the app settings and download the desired SDK.

>       ![](../graphics/download-sdk.png) 
>## iOS - Create a Target Location and Success Metric {#task_A372B1C4C1814788BBBEE06259A0103B}To use Target in your mobile app, create a location and success metric. 
<draft-comment otherprops="merge">
  target/t_mobile-create-location-and-metric.xml 
</draft-comment>This section includes sample code that can be used as a template for your app. The samples in this section contain code for iOS. The same patterns apply to Android. Android-specific syntax can be found in the [ Android SDK 4.x for Marketing Cloud ](https://marketing.adobe.com/resources/help/en_US/mobile/android/target_main.html) Solutions guide. 


>[!NOTE]
>
>See the[ Mobile documentation ](https://marketing.adobe.com/resources/help/en_US/mobile/ios/c_target_methods.html) for a list of all the available Target methods. 



To create a Target location in your app and make a request, there are two primary methods: 


* ` targetCreateRequestWithName`
* ` targetLoadRequest`


>1. Create a Target location.

>       Here is a sample call to create a request: 

>    
>       ```
>       // make your request 
>       ADBTargetLocationRequest *myRequest = [ADBMobile targetCreateRequestWithName:@"heroBanner" 
>                                                        defaultContent:@"default.png" 
>                                                        parameters:nil];
>       ```




>       |  Parameter  | Description  |
>       |---|---|
>       |  ` ADBTargetLocationRequest *myRequest`  | Replace ` myRequest` with the name of your ` targetLocation` in the app.  |
>       |  ` targetCreateRequestWithName:@"heroBanner"`  | Replace ` heroBanner` with the name of your ` targetLocation` in Target. This is the same as the mbox name. This hero banner appears in the Target interface.  |
>       |  ` defaultContent:@"default.png"`  | Replace ` default.png` with the value the app uses if Target doesn't respond.  |
>       |  ` parameters:nil`  | Specify profile or mbox parameters. See more information in the 'Passing custom data' section.  |

>       Here is a sample call to load the request: 

>    
>       ```
>       // load your request 
>       [ADBMobile targetLoadRequest:myRequest callback:^(NSString *content) { 
>                                            // do something with content 
>                                            heroImage.image = [UIImage imageNamed:content]; 
>       }];
>       ```




>       |  Parameter  | Description  |
>       |---|---|
>       |  ` targetLoadRequest:myRequest`  | Replace ` myRequest` with the name of your ` targetLocation` in the app.  |
>       |  ` NSString *content`  | Replace content with the actual content coming back from Adobe. The string can be XML, JSON or a plain string. Use this section of the code to define variables, set image paths, view controller flows, transaction points, or anything else you want to do. Target will return the content entered in the UI in the exact same format.  |
>       |  ` heroImage.image = [UIImage imageNamed:content];`  | For example: Take content and set the path for a hero image.  |

>1. Create a success metric.

>       The method ` targetCreateOrderConfirmRequestWithName` can be used to track a conversion/success metric in your app. 

>    
>       ```
>       ADBTargetLocationRequest *req = [ADBMobile targetCreateOrderConfirmRequestWithName: "orderConfirm" 
>                                                  orderId: orderId 
>                                                  orderTotal: @"39.95" 
>                                                  productPurchasedId: _galleryItem.title 
>                                                  parameters: nil]; 
>       [ADBMobile targetLoadRequest: req callback: nil];
>       ```




>       |  Parameter  | Description  |
>       |---|---|
>       |  ` orderId`  | Replace with a dynamic variable representing a unique order ID.  |
>       |  ` @"39.95"`  | Replace with a dynamic variable representing a unique order total.  |
>       |  ` _galleryItem.title`  | Replace with a dynamic variable representing a comma-delimited list of products purchased.  |
>       |  ` parameters: nil`  | Optional dictionary of additional parameters.  |

>1. Build the app.

>## iOS - Send Custom User Data {#task_779D60C519C04109A6C1FFA1ACFBA59E}You can send additional information about the location or the user to Target as name-value pairs. 
<draft-comment otherprops="merge">
  target/t_mobile-custom-user-data.xml 
</draft-comment>This information can be used to build custom audiences (for example, users with greater than 25000 miles) and in reporting. 

There are two types of parameters that you can send with a Target call: 


* mbox parameters Mbox parameters are not persistent across sessions. 

* Profile parameters Profile parameters are stored in the visitor profile store and are persistent across sessions. Mbox parameters don't persist. While some keys are reserved, both profile and mbox parameters can be custom key-value pairs. 



Although there are some reserved keys, both profile and mbox parameters can contain custom key-value pairs. 

>1. Create dictionary.

>       First, create a dictionary with the values that you send to pass to Target. For the sake of convenience, add this inside the ` welcomeMessageCampaign` method so you don't have to worry about scope. 

>       Following is a sample dictionary. You can copy paste this inside ` (void)welcomeMessageCampaign`. The values for keys like ` userLevel` and ` userMiles` are hard-coded in this example. In general, you pass in the corresponding variables. 

>    
>       ```
>       NSDictionary *targetParams = [[NSDictionary alloc] initWithObjectsAndKeys: 
>                                     @"platinum",@"userLevel", 
>                                     @26500,@"userMiles", 
>                                     @"1067007",@"entity.id", 
>                                     @"dealsapp.qa", @"host", 
>                                     @"fashion",@"entity.categoryId", 
>                                     @"millenial", @"profile.persona", 
>                                     @"cohort_5", @"profile.cohort", 
>                                     nil];
>       ```


>    
>    * Keys with the prefix profile (for example, ` profile.persona`) are stored on the user's profile. These profile attributes can be used across different activities and channels. 

>    * Keys that don't have any prefix (for example, ` userMiles`) are mbox parameters. These parameters are available only during the session. 

>    * Keys with the prefix entity (for example, ` entity.category.id`) are used for product recommendations.

>1. Verify the data.
>   >1. In application ` didFinishLaunchingWithOptions`, uncomment or add ` [ADBMobile setDebugLogging:YES];`.

>   >       This prints detailed debug logs. 
>   >1. Build the app.
>   >1. Verify that the parameters are passed in the target call.

>   >       Search for your target location name in your debug console. You will see a call to ` YOUR-CLIENT-CODE.tt.omtrdc.net`with all the parameters that you just passed. 

>   >       ![](../graphics/mobile-debug.png) 

>       You can build audiences and restrict or target the display of content using these parameters in Target Standard. 
>## Send Activity Information to Adobe Analytics {#task_5891CCB6EA9A44358C5BEFEDCF1C7CFF}This section describes how to send Target mobile app activity information to Adobe Analytics for postAhoc segmentation. 
<draft-comment otherprops="merge">
  target/t_mobile-send-activity-information-analytics.xml 
</draft-comment>**Prerequisites** 


* This integration requires that Analytics and Target are implemented using the mobile SDK.
* Ensure that your report suite is enabled to receive Activity information from Target. This is usually done by adding the Target client code to the Analytics report suite. This might be enabled already if you are using the SiteCatalyst-Test&amp;amp;Target integration for web activities. Contact Adobe Client Care if you have any questions about this step. 



>1. Obtain the activity information.

>       If you include a string like the following in your experience content, Target returns the campaign information that you can send to Analytics: 

>    
>       ```
>       ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
>       ```


>       Replace the text in your experience json code with something like the following example: 

>    
>       ```
>       { 
>         "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
>         "title":"Welcome Message", 
>         "message":"Get Free Shipping Today!" 
>       }
>       ```


>       In this example, a node with the variable ' ` tntVal`' is added to obtain the Activity information. Add similar code for the other experiences, with an appropriate title and message. 

>       This string delivers a number (such as 115110:0:0) in the response from Target. This indicates the Activity ID, experience ID, and traffic Type. The following is a smple response from Target: 

>    
>       ```
>       { 
>         "tntVal": 115110:0:0", 
>         "title":"Welcome Message", 
>         "message":"Get Free Shipping Today!" 
>       }
>       ```

>1. Parse the JSON object.

>       Parse the response that came back from Target in the callback. You can use NSJSONSerialization to parse this response and store it in a dict or an array. 

>       Refer to the [ NSJSONSerialization documentation ](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) for more information. 
>1. Send the data to Analytics.

>       Add the parsed activity information (such as ` tntVal` in the above response) to your context data object in an analytics call. This Analytics call containing the context data can be fired immediately or it can wait until the next Analytics call is fired. 

>       For example, this call can be fired in the callback of the ` targetLoadRequest` call: 

>    
>       ```
>       [ADBMobile trackAction:@"Welcome Screen"  
>             data:@{@"&amp;&amp;tnt" : tntVal from response}];
>       ```



>       >[!NOTE]
>       >
>       >` &amp;amp;&amp;amp;tnt`is a reserved event key in the mobile SDK. The post-classification of the ` tntVal` variable in Analytics works in the same way in the mobile SDK as it does in on the web (JavaScript). Once the information is processed in Analytics, you should see activity and experience names in the Analytics interface. 

>## Target Mobile Preview {#concept_5FBF12C2FDFC42429FE4F5CFBD78E19D}Use the mobile preview link to perform easy end-to-end QA for mobile app activities and enroll yourself into different experiences right on your device without any special test devices. 
<draft-comment otherprops="merge">
  target/target-mobile-preview.xml 
</draft-comment>
>[!NOTE]
>
>This feature will be turned on in the UI for all customers after October 12, 2017. The mobile preview feature requires that you download and install the appropriate 4.14 (or later) version of the Adobe Mobile SDK.



## Overview {#section_981D6FA4AEE64098809EA606E89E4A5E}

The mobile preview functionality lets you fully test your Mobile app activities prior to launching them live. 

## Prerequisites {#section_A763C564C9E84B0EB448237B5B1E4068}


1. **Use a supported version of the SDK: **The mobile preview feature requires that you download and install the appropriate 4.14 (or later) version of Adobe Mobile SDK in your corresponding apps. 

   For instructions to download the appropriate SDK, see: 


    * **iOS: ** [ Before You Start ](https://marketing.adobe.com/resources/help/en_US/mobile/ios/requirements.html) in the *iOS SDK 4.x for Marketing Cloud Solutions* guide. 

    * **Android: ** [ Before You Start ](https://marketing.adobe.com/resources/help/en_US/mobile/android/requirements.html) in the Android SDK 4.x for Marketing Cloud Solutions guide. 



1. **Set up a URL scheme: ** The preview link uses a URL scheme to open your app. You must specify a unique URL scheme for the preview. 

   The following illustration is an example on iOS: 

   ![](graphics/mobile-preview-url-scheme-ios.png) 

   The following illustration is an example on Android: 

   ![](graphics/Android_Deeplink.png) 

1. **Track Adobe DeepLink** 

   **iOS: **In the app delegate, call ` [ADBMobile trackAdobeDeepLink:url` when the delegate is asked to open the resource with the URL scheme that was specified in the previous step. 

   The following code snippet is an example: 


   ```
   - (BOOL) application:(UIApplication *)app openURL:(NSURL *)url 
                options:(NSDictionary<NSString *,id> *)options { 
    
       if ([[url scheme] isEqualToString:@"com.adobe.targetmobile"]) { 
           [ADBMobile trackAdobeDeepLink:url]; 
           return YES; 
       } 
       return NO; 
   } 
   
   ```


   **Android: **In the app , call ` Config.trackAdobeDeepLink(URL);` when the caller is asked to open the resource with the URL scheme that was specified in the previous step. 


   ```
    private Boolean shouldOpenDeeplinkUrl() { 
        Intent appLinkIntent = getIntent(); 
        String appLinkAction = appLinkIntent.getAction(); 
        Uri appLinkData = appLinkIntent.getData; 
        if (appLinkData.toString().startsWith("com.adobe.targetmobile")) { 
            Config.trackAdobeDeepLink(appLinkData); 
            return true; 
        } 
        return false; 
     }
   ```


   To make Mobile Preview work for Android, you must also add the following code snippet in [!DNL  AndroidManifest.xml]: 


   ```
   &amp;lt;activity&amp;nbsp;android:name="com.adobe.mobile.MessageFullScreenActivity"&amp;nbsp;/&amp;gt;
   ```




## Generating a Preview Link {#section_D9D58173FFF34E9BB75EBF357273F128}


1. In the Target UI, click the ** [!UICONTROL  More Options] ** icon (  ![](../graphics/icon_more_options.png) ), then select ** [!UICONTROL  Create Mobile Preview] **. 

   ![](graphics/mobile-preview-create.png) 

1. Select the activities that you want to preview, then click ** [!UICONTROL  Generate Mobile Preview LInk] **. 


   >[!NOTE]
   >
   >Only form-based AB and XT activities can be selected.


   ![](graphics/mobile-preview-select-activities.png) 

1. Specify your app's URL scheme. 

   This needs to be the same as what is present in your iOS or Android app. Repeat this process separately for iOS and Android, if required. 

   ![](graphics/mobile-preview-enter-url-scheme.png) 

1. Click ** [!UICONTROL  Generate Mobile Preview Link] **, then copy the link. 

   ![](graphics/mobile-preview-generate-and-copy.png) 



## Preview on Your Device {#section_521F0D46F3DE4A2A98283A1B73FF69F6}

Open the link in a mobile browser on a device where you have your app installed. This app can be the production app that you downloaded from the Apple App store or the Google Play store. It doesn't have to be a special build. If you have an active preview link, you will be able to view the experiences on device. 


1. Open the link in your mobile browser. 

   Share the link that you copied in the previous step from the Target UI to your mobile device in a convenient way, for example using text, email, or Slack. 



<table id="table_F853E79832954A87850BDDAF36D88A7F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p style="text-align: center;"> <img id="image_D6C60AC753FA4296B440B8C5F6BB5603" href="graphics/mobile-preview-open-deeplink.png" /> </p> </td> 
   <td colname="col2"> <p style="text-align: center;"> <img id="image_F1459ADE032F4B12880385F0CF6218FA" href="graphics/mobile-preview-open-app.png" /> </p> </td> 
  </tr> 
 </tbody> 
</table>

   Your app opens and starts the Target Mobile Preview Mode. 

1. Select the combination of experiences that you want to see, then click ** [!UICONTROL  Launch Experiences] **. 



<table id="table_6123AAE2EE9D426CA477BD71B4361489"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p style="text-align: center;"> <img href="graphics/mobile-preview-experience-selection-1.png" id="image_C9AA4C0525A449AA91A253BDD177A1DC" /> </p> </td> 
   <td colname="col2"> <p style="text-align: center;"> <img id="image_CE9638C68F184AE1AA66A0CDE9AA3770" href="graphics/mobile-preview-experience-result-1-france.png" /> </p> </td> 
   <td colname="col3"> <p style="text-align: center;"> <img id="image_92CB96E9A4274216B7A328F2B49FAEF3" href="graphics/mobile-preview-experience-result-1-shipfree.png" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p style="text-align: center;"> <img id="image_E7117C66BA534B2B87F1BDBA20E9EC5A" href="graphics/mobile-preview-experience-selection-2.png" /> </p> </td> 
   <td colname="col2"> <p style="text-align: center;"> <img id="image_3E880BB6C6D34F1EAC64C21CE07A9267" href="graphics/mobile-preview-experience-result-2-aus.png" /> </p> </td> 
   <td colname="col3"> <p style="text-align: center;"> <img id="image_2B419DDBD58B4C0CB4E5A967FCA50922" href="graphics/mobile-preview-experience-result-2-10off.png" /> </p> </td> 
  </tr> 
 </tbody> 
</table>




## Limitations {#section_4E9BDED0F718485292527EFB508305BD}


* The view must load again for the new content to display after the [!UICONTROL  Launch Experiences] button is clicked. The easiest way is to switch to a different screen and then come back to the screen where you are expecting the change to happen. 

* Mobile preview is not supported for Android versions earlier than API-19 (KitKat). 


>## Prefetch Offer Content {#concept_A355D9D55E1C429AA31FA4055A1DDFAF}The Adobe Target prefetch feature uses the iOS and Android Mobile SDKs to fetch offer content as few times as possible by caching the server responses. 
<draft-comment otherprops="merge">
  target/c_prefetch-offer-content.xml 
</draft-comment>This process reduces the load time, prevents multiple network calls, and allows Adobe Target to be notified which mbox was visited by the mobile app user. All content will be retrieved and cached during the prefetch call, and this content will be retrieved from the cache for all future calls that contain cached content for the specified mbox name. 

Prefetch content does not persist across launches. The prefetch content is cached as long as the application lives or until the ` clearPrefetchCache()` method is called. 

For more information, including prefetch methods, public classes, and code samples, see: 


* **iOS: ** [ Prefetch Offer Content in iOS ](https://marketing.adobe.com/resources/help/en_US/mobile/ios/c_mob_target-prefetch_ios.html) in the* iOS SDK 4.x for Marketing Cloud Solutions* guide. 

* **Android: ** [ Prefetch Offer Content in Android ](https://marketing.adobe.com/resources/help/en_US/mobile/android/c_mob_target-prefetch_android.html) in the *Android SDK 4.x for Marketing Cloud Solutions* guide. 


