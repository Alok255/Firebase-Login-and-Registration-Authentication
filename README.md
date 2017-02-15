# Firebase-Login-and-Registration-Authentication
With the latest news from Google I/O comes the new and upgraded Firebase. To demonstrate how simplified and easy to use firebase is, we will build a simple login / register (Firebase Authentication) demo using the Firebase Email &amp; Password authentication.


# Why Use Firebase?

 Super easy and quick to implement.
 No server side configuration needed. No PHP Scripts and No Database Designs.
 Realtime update without using GCM.
    
 # Creating a Firebase Application 

    First you need to create a firebase account.
    Just go to Firebase and Signup for a free plan. You can simply sign in with google.
    After signing in you will see your dashboard. Here you need to create an app. Just click on create a new app put the app name and URL and click on Create a New App.
    
#Now click on the app you created and you will see your app’s dashboard. Here you will see your data.
#From the Address Bar copy the URL, you will need this in Your Android Project.

#Creating an Android Project##

  Go to Android Studio and create a new project. I just created FirebaseExample.
  Now first you need Internet Permission, as the backend is in Firebase we need internet. So go to manifest and add internet permission.
  
  Java
    <uses-permission android:name="android.permission.INTERNET" />
    
 #First, add rules to your root-level build.gradle file, to include the google-services plugin:

buildscript {
    // ...
    dependencies {
        // ...
        classpath 'com.google.gms:google-services:3.0.0'
    }
}

#Then, in your module Gradle file (usually the app/build.gradle), add the apply plugin line at the bottom of the file to enable the Gradle plugin:#
        
      apply plugin: 'com.android.application'

android {
  // ...
}

dependencies {
  // ...
  compile 'com.google.firebase:firebase-core:10.0.1'
  
  // Getting a "Could not find" error? Make sure you have
  // the latest Google Repository in the Android SDK manager
}

// ADD THIS AT THE BOTTOM
apply plugin: 'com.google.gms.google-services'

goto link:-https://firebase.google.com/docs/android/setup

##You need to add some more lines in this gradle file. After the buildTypes block add the following code.##

buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }
    
    //Add the following block
    packagingOptions{
        exclude 'META-INF/LICENSE'
        exclude 'META-INF/LICENSE-FIREBASE.txt'
        exclude 'META-INF/NOTICE'
 
    }
    
   
   
 #Now sync your project and Firebase is added to your current project.
    
#So are you surprised how simple it is. No PHP, No MySQL Database, No large coding. Super Cool right? Firebase is a great option for the backend for your application. We can do many other things with firebase we will try some more complex thing in my upcoming posts of Firebase Android Tutorial. Thank You 






    
