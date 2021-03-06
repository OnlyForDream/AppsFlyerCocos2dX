<img src="https://www.appsflyer.com/wp-content/uploads/2016/11/logo-1.svg"  width="200">

# Cocos2dX Android Integration Guide


##  Integration:
How to integrate the AppsFlyer SDK into your Cocos2d-x Android project.

###1.  Add the SDK to your project
Throughout this guide, we assume that you are using `Android Studio` for development.

Take the files from the `AppsFlyer` [folder](/Classes/AppsFlyer) and add them to your Android project under `Classes` folder.

![add-to-android-mk](https://github.com/AppsFlyerSDK/AppsFlyerCocos2dX/blob/development/Resources/add-android-files.png?raw=true)

###2.  Add the C++ source file definitions
Add the paths of the AppsFlyer C++ files to the `LOCAL_SRC_FILES` section in your `Android.mk` file.
```mk
../../../Classes/AppsFlyer/AppsFlyerXAndroid.cpp \
../../../Classes/AppsFlyer/AppsFlyerProxyX.cpp \
../../../Classes/AppsFlyer/AppsFlyerX.cpp
```

![add-android-files](https://github.com/AppsFlyerSDK/AppsFlyerCocos2dX/blob/development/Resources/add-to-android-mk.png?raw=true)

###3. Add the AppsFlyer library to your project

Take the latest `appsflyer-SDK.jar` library and copy it to your project's `libs` folder.

###4. Add permissions

In the Package Explorer, open the `AndroidManifest.xml` file of your Android project. Add the `uses-permission` tag for `INTERNET` if it's not already present.

```xml
<uses-permission android:name="android.permission.INTERNET" />
```