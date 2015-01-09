After importing the AdMob SDKs into your project (https://developers.google.com/mobile-ads-sdk/download);

# iOS

1. import libAdRallyAdMob.a to your project. This Library contains both the AdRally SDK as well as the AdMob adapter class for AdRally.

2. Add the following libraries to your project under “Build Phases” > “Link Binary With Libraries”
  * AdSupport.framework
  * AudioToolbox.framework
  * AVFoundation.framework
  * CoreGraphics.framework
  * CoreLocation.framework
  * CoreMedia.framework
  * CoreTelephony.framework
  * EventKit.framework
  * EventKitUI.framework
  * Foundation.framework
  * GameKit.framework
  * libsqlite3.dylib
  * libz.dylib
  * MediaPlayer.framework
  * MessageUI.framework
  * QuartzCore.framework
  * Social.framework (weak link)
  * StoreKit.framework
  * SystemConfiguration.framework
  * Twitter.framework
  * UIKit.framework

3. Add ```-ObjC``` to your project's linker flags under "Build Settings" > "Linking" > "Other Linker Flags"


# Android

1. import FuseSDK.jar to your project. This Jar contains both the AdRally SDK as well as the AdMob adapter class for AdRally.
2. In your manifest:

* Add the following permissions if not already included
```xml
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.GET_ACCOUNTS" />

<!-- The following permission is optional but can greatly improve ad performance. -->
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```
* Add a ```<meta-data>``` tag that references the Google Play Services version
```xml
<meta-data android:name="com.google.android.gms.version"
  android:value="@integer/google_play_services_version" />
```
* Add the following ```<activity>``` elements
```xml
<activity
   android:name="com.fusepowered.m2.mobileads.M2Activity"
   android:configChanges="keyboardHidden|orientation" />
<activity
   android:name="com.fusepowered.m2.mobileads.M2RActivity"
   android:configChanges="keyboardHidden|orientation" />
<activity
   android:name="com.fusepowered.m2.common.M2Browser"
   android:configChanges="keyboardHidden|orientation" />
<activity
   android:name="com.fusepowered.m2.mobileads.M2RvpActivity"
   android:configChanges="keyboardHidden|orientation" />
<activity
   android:name="com.fusepowered.m1.android.MMActivity"
   android:configChanges="keyboardHidden|orientation|keyboard"
   android:theme="@android:style/Theme.Translucent.NoTitleBar" />
<activity
   android:name="com.fusepowered.m1.android.VideoPlayer"
   android:configChanges="keyboardHidden|orientation|keyboard" />
<activity
   android:name="com.fusepowered.u1.U1InterstitialActivity"
   android:configChanges="keyboardHidden|orientation|screenLayout|screenSize|smallestScreenSize"
   android:hardwareAccelerated="true"
   android:theme="@android:style/Theme.NoTitleBar.Fullscreen" />
<activity
   android:name="com.fusepowered.s1.S1InterstitialActivity"
   android:hardwareAccelerated="true" />
<activity
   android:name="com.vungle.sdk.VungleAdvert"
   android:configChanges="keyboardHidden|orientation|screenSize"
   android:theme="@android:style/Theme.NoTitleBar.Fullscreen" />
<service android:name="com.vungle.sdk.VungleIntentService" />
<activity
   android:name="com.fusepowered.ads.adapters.FuseInterstitialActivity"
   android:configChanges="keyboardHidden|orientation|screenSize"
   android:noHistory="true"
   android:theme="@android:style/Theme.Translucent.NoTitleBar.Fullscreen" />
<activity
    android:name="com.fusepowered.l1.AdActivity"
    android:configChanges="orientation|keyboardHidden|screenSize"
    android:hardwareAccelerated="true" />
<activity
    android:name="com.fusepowered.l1.AdBrowserActivity" />
<activity
    android:name="com.fusepowered.l1.PlayerActivity"
    android:configChanges="orientation|keyboardHidden|screenSize"
    android:hardwareAccelerated="true" />
<activity
   android:name="com.fusepowered.ac.ACOActivity"
   android:configChanges="keyboardHidden|orientation|screenSize"
   android:theme="@android:style/Theme.Translucent.NoTitleBar.Fullscreen" />
<activity
   android:name="com.fusepowered.ac.ACFActivity"
   android:configChanges="keyboardHidden|orientation|screenSize"
   android:theme="@android:style/Theme.Black.NoTitleBar.Fullscreen" />
<activity
   android:name="com.fusepowered.ac.ACBActivity"
   android:configChanges="keyboardHidden|orientation|screenSize"
   android:theme="@android:style/Theme.Black.NoTitleBar.Fullscreen" />
<activity
   android:name="com.fusepowered.ads.adapters.LRActivity"
   android:configChanges="keyboardHidden|orientation|screenSize"
   android:theme="@android:style/Theme.Translucent.NoTitleBar.Fullscreen" />
<activity
   android:name="com.fusepowered.ads.adapters.MRaidActivity"
   android:hardwareAccelerated="true"
   android:configChanges="orientation|keyboard|keyboardHidden|screenLayout|screenSize"
   android:theme="@android:style/Theme.Translucent.NoTitleBar"
   android:windowSoftInputMode="adjustResize" />
<activity
   android:name="com.fusepowered.sa.android.publish.list3d.List3DActivity"
   android:theme="@android:style/Theme" />
<activity
   android:name="com.fusepowered.sa.android.publish.AppWallActivity"
   android:theme="@android:style/Theme.Black.NoTitleBar.Fullscreen"
   android:configChanges="orientation|keyboardHidden|screenSize" />
```
