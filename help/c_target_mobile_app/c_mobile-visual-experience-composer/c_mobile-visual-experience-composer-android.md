---
description: Target's new SDK Library allows developers to do a one-time setup on their Android mobile apps and enable marketers to use the capabilities of the Mobile Visual Experience Composer (VEC).
keywords: mobile vec;mobile visual experience composer;mobile experience composer options;setting up;android
seo-description: Target's new SDK Library allows developers to do a one-time setup on their Android mobile apps and enable marketers to use the capabilities of the Mobile Visual Experience Composer (VEC).
seo-title: Android - Setting Up the Mobile App
solution: Target
title: Android - Setting Up the Mobile App
topic: Standard
uuid: c4801de5-918f-4a53-8ed0-86d9f103689f
index: y
internal: n
snippet: y
translate: y
---

# Android - Setting Up the Mobile App


>[!NOTE]
>
>The Visual Experience Composer for Native Mobile Apps is currently offered as a Beta feature available to select customers to obtain feedback to help us improve the feature before making it available to all customers. Please talk to your Customer Success Manager or Adobe Client Care to participate in this Beta program.



This section contains the following information: 


* [ Include the Mobile SDK &amp;amp; the Target Library ](c_mobile-visual-experience-composer-android.md#section_481F9644C71B4CB7AE3FC526D281D1D2) 

* [ Set Up Target Views on Your Mobile App ](c_mobile-visual-experience-composer-android.md#section_93AE7797B603465BBFBEC34E5A0A91E3) 



## Include the Mobile SDK &amp; the Target Library {#section_481F9644C71B4CB7AE3FC526D281D1D2}


1. Get the packaged mobile demo zip file from your Adobe Beta representative, then unzip the package in a local directory. 

1. In Android Studio, follow the directions to add the [!DNL  .AAR] file in the [!DNL  android-lib] subdirectory: [ https://stackoverflow.com/questions/16682847/how-to-manually-include-external-aar-package-using-new-gradle-android-build-syst ](https://stackoverflow.com/questions/16682847/how-to-manually-include-external-aar-package-using-new-gradle-android-build-syst). (Shortened directions for Android Studios are added below for completeness.) 

    1. Click ** [!UICONTROL  File] ** > ** [!UICONTROL  New] ** > ** [!UICONTROL  New Module] **. 

    1. Select ** [!UICONTROL  Import .JAR/.AAR Package] **, then click ** [!UICONTROL  Next] **. 

    1. Specify the path to the [!DNL  .AAR] file, then click ** [!UICONTROL  Finish] **. 

    1. Click ** [!UICONTROL  File] ** > ** [!UICONTROL  Project Structure] ** (Ctrl+Shift+Alt+S). 

    1. Under ** [!UICONTROL  Modules] ** in left menu, select ** [!UICONTROL  app] **. 

    1. Click the ** [!UICONTROL  Dependencies] ** tab. 

    1. Click the green "+" in the upper right corner. 

    1. Select ** [!UICONTROL  Module Dependency] **. 

    1. Select the new module from the list. 


1. From your Mobile SDK integration in the [!DNL  ADBMobileConfig.json] file, determine the following information: 

    * The Marketing Cloud ID for your organization 

    * The Target clientCode for your organization 


1. Add another intent filter in your [!DNL  AndroidManifest.XML] file, choosing a unique deep-link scheme for Mobile VEC authoring (for example, ` sdkbetabus://com.adobe.sdkbetabus`): 


   ```
   <activity 
       android:name=".listing.MoviesListingActivity" 
       android:launchMode="singleTask"> 
       <intent-filter> 
           <action android:name="android.intent.action.VIEW" /> 
     
           <category android:name="android.intent.category.DEFAULT" /> 
           <category android:name="android.intent.category.BROWSABLE" /> 
     
           <data 
               android:host="com.adobe.sdkbetabus" 
               android:scheme="sdkbetabus" /> 
       </intent-filter> 
   </activity> 
   
   ```


1. In your [!DNL  build.gradle] file of your application project, add the following lines to the dependencies section: 


   ```
   dependencies { 
       // PUT PREVIOUS PROJECT DEPENDENCIES HERE 
       implementation('commons-beanutils:commons-beanutils-core:1.8.3') { 
           exclude group: 'commons-logging', module: 'commons-logging' 
       } 
       implementation 'io.github.xdex:SocketclusterClientJava:1.7.5' 
       implementation 'com.google.code.gson:gson:2.8.2' 
       implementation 'com.squareup.picasso:picasso:2.5.2' 
       implementation 'com.google.android.gms:play-services-location:15.0.0' 
       implementation project(':target-client-platform-release') 
   }
   ```


1. Go to your mobile project and insert the following lines at the end of ` Application::onCreate override`: 


   ```
   public class SDKTest extends MultiDexApplication { 
     
       @Override 
       public void onCreate() { 
           /* Put Your App's implementation */ 
     
     
           /* BEGIN_ADDED_CODE */ 
           Map<String, String> configData = new HashMap<>(); 
     
           configData.put("marketingCloud.org", "99EF0AB653FB5437GARBAGE@AdobeOrg");  // Please replace with your MarketingCloudID 
           configData.put("target.clientCode", "my_client_code");  // Please replace with your own client code 
           configData.put("target.authoringUrl", AdobeTargetMobile.TARGET_AUTHORING_URL.US.getUrl()); 
               // OR Choose a different closer cluster: AdobeTargetMobile.TARGET_AUTHORING_URL.EU.getUrl(), AdobeTargetMobile.TARGET_AUTHORING_URL.APAC.getUrl() 
           AdobeTargetMobile.attachVisualEditor(this, configData); 
           /* END_ADDED_CODE */    
       } 
     
     
   /* Rest of Application test goes here ... */
   ```


1. If your build is not working, review the example projects provided below that should build out-of-the-box and review changes in the following locations: 

    1. ` Application::OnCreate override` 

    1. [!DNL  AndroidManifest.XML] 

    1. ` build.gradle` of the Android Application 




## Set Up Target Views on Your Mobile App {#section_93AE7797B603465BBFBEC34E5A0A91E3}

The Adobe Mobile SDK exposes a new method for developers to trigger whenever a new View is rendered. As a developer, you must ensure that the views are named uniquely, and the ` targetView` call is on the UI main thread. In this section, we will first demonstrate how to properly insert these calls with two different demonstration applications and discuss general guidelines on how to properly insert the Target View API calls for any Android app. 

The integration of the Target Views on your mobile app is straight forward. There's only one call to be made: 


```
public class AdobeTarget { 
  
   /** 
    * Marks a view hierarchy for editing in Mobile VEC.  Call must insert when the view hierarchy 
    * is memory and committed to being shown, but not yet shown on the screen. 
    * 
    * @param viewName the unique Target View Name 
    */ 
   public static void targetView(String viewName); 
}
```


Our first example project is a simple mock-up of simple bus schedule application. To set up this application for use in the Mobile VEC: 


1. In Android Studio, open the project with the [!DNL  build.gradle] file in the package subdirectory [!DNL  BusBooking]. 

1. In the method ` DemoApplication::OnCreate` change the ` configData` to your Marketing Cloud ID and clientCode from the Adobe SDK v4 [!DNL  ADBConfig.json] file 

1. Build and run the application. 

1. To enter the Mobile VEC authoring mode, use the [!DNL  sdkbetabus://com.adobe.sdkbetabus] as its URL scheme, and open the generated deep link on the device (see directions below). 



From this simple bus-booking application, we use all the automatically generated Target Views associated with the activity lifecycle. Furthermore, we demonstrate the flexibility of the API by calling the Target View API on a custom view element that is dynamically added, when a hidden button is clicked (the offer image on the screen). This new Target View is implemented by inserting an API call in the code at ` OfferDetailsActivity.java:40`. When the hidden button is clicked, a new Target View event called " ` SURPRISE_VIEW`" is fired, allowing the marketer to more precisely target change on the application experience. 

Targeted Dynamic View Insertion: 


```
package com.adobe.target.examples.bus; 
  
import android.app.DialogFragment; 
import android.os.Bundle; 
import android.os.Handler; 
import android.support.v7.app.AppCompatActivity; 
import android.support.v7.widget.Toolbar; 
import android.view.View; 
import android.view.ViewGroup; 
import android.widget.LinearLayout; 
import android.widget.Toast; 
  
import com.adobe.target.mobile.AdobeTargetMobile; 
  
/** 
 * This activity class is responsible to show offer details 
 */ 
public class OfferDetailsActivity extends AppCompatActivity { 
    @Override 
    protected void onCreate(Bundle savedInstanceState) { 
        super.onCreate(savedInstanceState); 
        setContentView(R.layout.activity_offer_details); 
        setUpToolBar(); 
        final Handler mainHandler = new Handler(getApplicationContext().getMainLooper()); 
  
        final View surpriseView = getLayoutInflater().inflate(R.layout.suprise_layout, 
                (ViewGroup) findViewById(android.R.id.content), false); 
  
        final View imagePresentView = this.findViewById(R.id.image_present); 
        final LinearLayout currentLayout = this.findViewById(R.id.offer_layout); 
  
        imagePresentView.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                Toast.makeText(getApplicationContext(),"Surprise!", Toast.LENGTH_SHORT).show(); 
                mainHandler.post(new Runnable() { 
                    @Override 
                    public void run() { 
                        currentLayout.addView(surpriseView); 
                        AdobeTargetMobile.targetView("SURPRISE_VIEW"); 
                        currentLayout.invalidate(); 
                    } 
                }); 
                // One-shot.  Remove clicker afterwards. 
                imagePresentView.setOnClickListener(null); 
            } 
        }); 
    } 
  
    private void setUpToolBar() { 
        Toolbar toolbar = findViewById(R.id.toolbar); 
        toolbar.setNavigationIcon(R.drawable.abc_ic_ab_back_material); 
        toolbar.setTitle("Buy 1 Get 1"); 
        toolbar.setNavigationOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                onBackPressed(); 
            } 
        }); 
    } 
  
    @Override 
    protected void onPause() { 
        super.onPause(); 
    } 
  
    @Override 
    protected void onResume() { 
        super.onResume(); 
    } 
}
```


Our second example project is a instrumentation of a well-known, open-source and realistic movie application called MovieGuide ( [ https://github.com/esoxjem/MovieGuide ](https://github.com/esoxjem/MovieGuide)). 

To set up this application for use in the Mobile VEC: 


1. In Android Studio, open the project with the [!DNL  build.gradle] file in the package subdirectory [!DNL  MovieGuide]. 

1. Follow to directions on [ https://github.com/AshishKayastha/Movie-Guide ](https://github.com/AshishKayastha/Movie-Guide) to get your API key and enable access to its movie database. Modify the [!DNL  local.properties] files as per the instructions. 

1. In the ` BaseApplication::OnCreate` method, change the ` configData` to your Marketing Cloud ID and clientCode from the Adobe SDK v4 ` ADBConfig.json` file. 

1. Build and run the application. 

1. To enter the Mobile VEC authoring mode, use the [!DNL  sdkbeta://com.adobe.sdkbeta] as its URL scheme, and open the generated deep link on the device (see directions below). 



All activity starts/resumes are already automatically marked as Target Views by the Target Mobile library extension. Moreover, our first example inserts the ` TargetView` call into the application open source movie guide application. In our test application, we insert a Target View directly after a movie listing is about to appear ( ` com/esoxjem/movieguide/listing/MovieListingFragment.java:90`) for the first time. 

Target View Call Insertion: 


```
public class MoviesListingFragment extends Fragment implements MoviesListingView { 
    /* ... */ 
  
    @Override 
    public void onViewCreated(View view, Bundle savedInstanceState) { 
        super.onViewCreated(view, savedInstanceState); 
        if (savedInstanceState != null) { 
            movies = savedInstanceState.getParcelableArrayList(Constants.MOVIE); 
            adapter.notifyDataSetChanged(); 
            moviesListing.setVisibility(View.VISIBLE); 
        } else { 
            AdobeTargetAPIPlaceholder.targetView("MOVIE_LISTINGS"); 
            moviesPresenter.setView(this); 
        } 
    } 
  
    /* ... */ 
}
```


Our second example inserts the ` TargetView` call onto a unique view element, so that we can directly target a screen associated with that view element ( [!DNL  com/esoxjem/movieguide/details/MovieDetailsFragment.java:108]). Because this element is used only once in unique layout inflation, the label can be used to represent the layout as a whole and can target the screen for reviews inside of Android Fragment. 

Unique View Tagging: 


```
public class MovieDetailsFragment extends Fragment implements MovieDetailsView, View.OnClickListener 
  
{ 
   /* ... */ 
    @Override 
    public View onCreateView(LayoutInflater inflater, ViewGroup container, 
                             Bundle savedInstanceState) 
    { 
        View rootView = inflater.inflate(R.layout.fragment_movie_details, container, false); 
        unbinder = ButterKnife.bind(this, rootView); 
        setToolbar(); 
  
        /* Added AdobeTargetMobile Code */ 
        View reviewerLabel =  rootView.findViewById(R.id.reviews_label); 
        if(reviewerLabel != null) { 
            reviewerLabel.addOnAttachStateChangeListener(new View.OnAttachStateChangeListener() { 
                @Override 
                public void onViewAttachedToWindow(View v) { 
                    AdobeTargetMobile.targetView("REVIEW_LABEL_SHOWN"); 
                } 
  
                @Override 
                public void onViewDetachedFromWindow(View v) { 
  
                } 
            }); 
        } 
  
        return rootView; 
    } 
  
   /* ... */ 
} 
 
 

```

