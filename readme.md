# Flutter Connectivity Package Permissions


```xml
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.johnwargo.connectivitypermissions">
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
    <application
        android:name="io.flutter.app.FlutterApplication"
        android:label="connectivitypermissions"
        android:icon="@mipmap/ic_launcher">
        <activity
            android:name=".MainActivity"
            android:launchMode="singleTop"
            android:theme="@style/LaunchTheme"
            android:configChanges="orientation|keyboardHidden|keyboard|screenSize|smallestScreenSize|locale|layoutDirection|fontScale|screenLayout|density|uiMode"
            android:hardwareAccelerated="true"
            android:windowSoftInputMode="adjustResize">
            <!-- Specifies an Android theme to apply to this Activity as soon as
                 the Android process has started. This theme is visible to the user
                 while the Flutter UI initializes. After that, this theme continues
                 to determine the Window background behind the Flutter UI. -->
            <meta-data
              android:name="io.flutter.embedding.android.NormalTheme"
              android:resource="@style/NormalTheme"
              />
            <!-- Displays an Android View that continues showing the launch screen
                 Drawable until Flutter paints its first frame, then this splash
                 screen fades out. A splash screen is useful to avoid any visual
                 gap between the end of Android's launch screen and the painting of
                 Flutter's first frame. -->
            <meta-data
              android:name="io.flutter.embedding.android.SplashScreenDrawable"
              android:resource="@drawable/launch_background"
              />
            <intent-filter>
                <action android:name="android.intent.action.MAIN"/>
                <category android:name="android.intent.category.LAUNCHER"/>
            </intent-filter>
        </activity>
        <!-- Don't delete the meta-data below.
             This is used by the Flutter tool to generate GeneratedPluginRegistrant.java -->
        <meta-data
            android:name="flutterEmbedding"
            android:value="2" />
    </application>
</manifest>
```

When you launch the app on Android API 29, it looks like this

![Permissions Prompt](images/permission-prompt-1.png)

On older devices, it looks like this:

![Permissions Prompt](images/permission-prompt-2.png)

And here's the Wi-Fi settings results

![Wi-Fi Settings](images/wi-fi-settings.png)
