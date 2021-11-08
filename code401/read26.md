# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 26 -->

[comment]: <> (https://developer.android.com/guide/components/fundamentals)
## Android Fundamentals
### General
- Android apps can be written using Kotlin, Java, and C++ languages. The Android SDK tools compile your code along with any data and resource files into an APK or an Android App Bundle.

- An Android package, which is an archive file with an .apk suffix, contains the contents of an Android app that are required at runtime and it is the file that Android-powered devices use to install the app.

- An Android App Bundle, which is an archive file with an .aab suffix, contains the contents of an Android app project including some additional metadata that is not required at runtime. An AAB is a publishing format and is not installable on Android devices, it defers APK generation and signing to a later stage. When distributing your app through Google Play for example, Google Play's servers generate optimized APKs that contain only the resources and code that are required by a particular device that is requesting installation of the app.

The Android system implements the principle of least privilege.

### App components
- These are the essential building blocks of an Android app. Each component is an entry point through which the system or a user can enter your app. Some components depend on others.

There are four different types of app components:

#### Activity
An activity is the entry point for interacting with the user. It represents a single screen with a user interface. For example, an email app might have one activity that shows a list of new emails, another activity to compose an email, and another activity for reading emails
#### Services
A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. It is a component that runs in the background to perform long-running operations or to perform work for remote processes. A service does not provide a user interface. For example, a service might play music in the background while the user is in a different app, or it might fetch data over the network without blocking user interaction with an activity.

Extends `Service`
#### Broadcast Receivers
A broadcast receiver is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements. Because broadcast receivers are another well-defined entry into the app, the system can deliver broadcasts even to apps that aren't currently running. So, for example, an app can schedule an alarm to post a notification to tell the user about an upcoming event... and by delivering that alarm to a BroadcastReceiver of the app, there is no need for the app to remain running until the alarm goes off.

Although broadcast receivers don't display a user interface, they may create a status bar notification to alert the user when a broadcast event occurs. More commonly, though, a broadcast receiver is just a gateway to other components and is intended to do a very minimal amount of work.

A broadcast receiver is implemented as a subclass of `BroadcastReceiver` and each broadcast is delivered as an `Intent` object.
#### Content Providers
A content provider manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access. Through the content provider, other apps can query or modify the data if the content provider allows it. 

For example, the Android system provides a content provider that manages the user's contact information.

Content providers are also useful for reading and writing data that is private to your app and not shared.

A content provider is implemented as a subclass of `ContentProvider`

### Useful
A unique aspect of the Android system design is that any app can start another app’s component. For example, if you want the user to capture a photo with the device camera, there's probably another app that does that and your app can use it instead of developing an activity to capture a photo yourself. You don't need to incorporate or even link to the code from the camera app. Instead, you can simply start the activity in the camera app that captures a photo. When complete, the photo is even returned to your app so you can use it. To the user, it seems as if the camera is actually a part of your app.

There are separate methods for activating each type of component:

- You can start an activity or give it something new to do by passing an `Intent` to `startActivity()` or `startActivityForResult()` (when you want the activity to return a result).
- With Android 5.0 (API level 21) and later, you can use the `JobScheduler` class to schedule actions. For earlier Android versions, you can start a service (or give new instructions to an ongoing service) by passing an `Intent` to `startService()`. You can bind to the service by passing an `Intent` to `bindService()`.
- You can initiate a broadcast by passing an `Intent` to methods such as `sendBroadcast()`, `sendOrderedBroadcast()`, or `sendStickyBroadcast()`.
- You can perform a query to a content provider by calling `query()` on a `ContentResolver`.

[BACK TO HOME](../README.md)