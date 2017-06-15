#Social Itegration GuideLines

  ## Step by step Facebook Integration

        1. Go to Android Studio | New Project | Minimum SDK
        2. Select "API 15: Android 4.0.3" or higher and create your new project.
        3. In your project, open
        your_app | Gradle Scripts | build.gradle

        4. Add the Maven Central Repository to build.gradle before dependencies:

        repositories {
        mavenCentral()
        }

        5. Add compile `'com.facebook.android:facebook-android-sdk:[4,5)'` to your build.gradle dependencies.

        6. Build your project.

        7. Import Facebook SDK into your app:

        import com.facebook.FacebookSdk;

        Add Facebook App ID

        Add your Facebook App ID to your app and update your Android manifest.
        8. Open your strings.xml file, for example: /app/src/main/res/values/strings.xml.
        9. Add a new string with the name facebook_app_id containing the value of your Facebook App ID:

        <string name="facebook_app_id">329343964167110</string>

        10. Open AndroidManifest.xml.

        11. Add a uses-permission element to the manifest:

        `<uses-permission android:name="android.permission.INTERNET"/>`

        12. Add a meta-data element to the application element:

        <meta-data android:name="com.facebook.sdk.ApplicationId" android:value="@string/facebook_app_id"/>

        13. Tell us about your Android project

        Your package name uniquely identifies your Android app.
        We use this to let people download your app from Google Play if they don't have it installed.
        You can find this in your Android Manifest

        com.app.socialintegration

        14. Default Activity Class Name
        This is the fully qualified class name of the activity that handles deep linking. 
        We use this when we deep link into your app from the Facebook app. You can also find this in your Android Manifest

        com.app.socialintegration.MainActivity

        15. Add your development and release key hashes:

        Android apps must be digitally signed with a release key before you can upload them to the store.
        To generate a hash of your release key, run the following command on Mac or Windows substituting your release key alias and the path to your keystore:


        To generate Hash key:
   ##   keytool -exportcert -alias YOUR_RELEASE_KEY_ALIAS -keystore YOUR_RELEASE_KEY_PATH | openssl sha1 -binary | openssl base64
        This will generate a 28-character string that you should copy and paste into the field below. Also, see the Android documentation for signing your apps.

        Key Hashes
        `zY00cczs2SG28RTn1bZQvsCftvI=`


        16. Select Login Option:

        Facebook Login for Android - Quickstart

        17. Select an App or Create a New App

        18. Verify that you have sync facebook sdk and entries in manifest file.

        19. Add it to manifest:

         <activity android:name="com.facebook.FacebookActivity"
        android:configChanges=
                "keyboard|keyboardHidden|screenLayout|screenSize|orientation"
        android:label="@string/app_name" />

         <activity
        android:name="com.facebook.CustomTabActivity"
        android:exported="true">
        <intent-filter>
            <action android:name="android.intent.action.VIEW" />
            <category android:name="android.intent.category.DEFAULT" />
            <category android:name="android.intent.category.BROWSABLE" />
            <data android:scheme="@string/fb_login_protocol_scheme" />
        </intent-filter>
        </activity>

         20. Associate Your Package Name and Default Class with Your App

         21. Enable Single Sign On for Your App(if you want)

         22. Add the Facebook Login Button in your xml:

         <com.facebook.login.widget.LoginButton
        android:id="@+id/login_button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/> 

        23. Then add java code inyour activity.


        Done.



  ## Step by Step GuileLines for Google+ Integration

        1. Get a configuration file

        2. Enter app name

        3. Enter package name

        4. Continue to Choose and configure services

        will show a message:
        done You are configuring the SocialIntegration app with package name `com.app.socialintegration`.

        5. To use Google Sign-In, you'll need to provide the SHA-1 of your signing certificate so we can create an OAuth2 client and API key for your app. 

        Android Signing Certificate SHA-1
  ##    SHA1: B8:8E:E1:9A:4E:44:1E:F0:2C:BB:66:E4:99:5F:36:DB:06:65:9B:2D

        6. ENABLE GOOGLE SIGN-IN

        7. Add this your project level build.gradle
        classpath 'com.google.gms:google-services:3.0.0'

        8. Add this to your app level build.gradle
         compile 'com.google.android.gms:play-services-auth:9.8.0'


        9. Add code in your Activity.java


        Done.




   ##Step by Step GuideLines for Twitter Integration

        1. Join the community of Twitter.

        2. Go to Twitter Fabric account:
        https://fabric.io/onboard

        3. Select Anddroid follow steps and plugin and install Fabric in android Studio  and Restart.

        4. Fill the form of Application management to cerate an application.		
                https://apps.twitter.com/app/new
                Name, Description, website, Callback URL, Developer Agreement.
                Create your Twitter application.

        5. There are four tab:

        i. Details:
                All details what you have filled about created app.

        1i. Settings:
                Application Details.

        iii. Keys and Access Tokens:

                 Consumer Key (API Key) mr2cO9Nz2xN9zWF9TFPiYrbjz 
                 Consumer Secret (API Secret) DXDFcyseN2L9GxjMcY67LbDVIM1qq5gtrCh7oXSGCG8l4ofBUm 
                        Access Level Read and write (modify app permissions)
                        Owner pkvarnwal
                        Owner ID 2989391617 

                  Access Token:  2989391617-eEW3Z2ixcH0CQZOQvMDKnbjcRlalUV8bqiLW83t
                   Access Token Secret zfJOtvbhD6rXAZ3IKFtI34vy8xWfHnwnn65pZrGuvCB9d 


        6. Twitter sold Fabric to Google and Google removed Twitter from Fabric.
        So need to follow new documentation to integrate Twitter:
        https://dev.twitter.com/twitterkit/android/installation

        7. Add dependencies in build.gradle file.

        8. Initialize code by doc.

        9. To initialize what you want to get from Twitter follow this link:
   ##    https://dev.twitter.com/twitterkit/android/log-in-with-twitter


         Done.


  ## Step by Step GuideLines for LinkedIn Integration

        Client ID: 81kcjrkm7g8i1s
        Client Secret: RswzCekhQLnzJ3xe

        1. Create a new app in LinkedIn Developer Account
        i. Provide application name
        ii. Provide description
        iii. Add logo for app
        iv. add website url
        v. Application use: Travel
        vi. Website URL: http://crownstack.com
        vii. Business Email: contact@crownstack.com
        viii. Business Phone: 8459693420
        ix. Accept
        x. Subimt

        2. After creating an app on LinkedIn
        Setting: 
                Application Status: Development
                Legal Agreement Language: English

        3. Roles: Developers: Aashish Dhawan, Prinsu Kumar, Ashutosh Singh

        To generate HashKey:- keytool -exportcert -keystore ~/.android/debug.keystore -alias androiddebugkey | openssl sha1 -binary | openssl base64
        Generated hashKey using above command did not work for LinkedIn.
        Use below type code to generate hashKey and use it.
        MessageDigest md = MessageDigest.getInstance("SHA");

        4. Mobile -> Android Settings -> 

        ##      Package Name- `com.app.socialintegration`
        ##      Package Hash- `uI7hmk5EHvAsu2bkmV822wZlmy0=`

        5. Authentication: Provide Application Permissions:
         `r_basicprofile`
         `r_emailaddress`
         `rw_company_admin`
         `w_share`
         after check all boxes, Update.


        6. Download Mobile SDk(1.1.4)
        add it as module add a line in app/build.gradle:
         `compile project(':linkedin-sdk')`

         and add a line in settings.gradle:
         `include ':app', ':linkedin-sdk'`


        7. In downloaded SDK there is a sample project, open and follow code and use it.


        Done.


