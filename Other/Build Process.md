# The Build Process
The build process involves many tools and processes that convert your project into an Android Application Package (APK) or Android App Bundle (AAB). The build process is very flexible, so it's useful to understand some of what is happening under the hood.

![Build Process](media/build-process_2x.png)

The build process for a typical Android app module, as shown in figure 1, follows these general steps:

1.  The compilers convert your source code into DEX (Dalvik Executable) files, which include the bytecode that runs on Android devices, and everything else into compiled resources.
2.  The packager combines the DEX files and compiled resources into an APK or AAB, depending on the chosen build target. Before your app can be installed onto an Android device or distributed to a store, such as Google Play, the APK or AAB must be signed.
3.  The packager signs your APK or AAB using either the debug or release keystore:
    1.  If you are building a debug version of your app, that is, an app you intend only for testing and profiling, the packager signs your app with the debug keystore. Android Studio automatically configures new projects with a debug keystore.
    2.  If you are building a release version of your app that you intend to release externally, the packager signs your app with the release keystore that you need to configure. To create a release keystore, read about [signing your app in Android Studio](https://developer.android.com/studio/publish/app-signing#studio).
4.  Before generating your final APK, the packager uses the [zipalign](https://developer.android.com/studio/command-line/zipalign) tool to optimize your app to use less memory when running on a device.

At the end of the build process, you have either a debug or release APK or AAB of your app that you can use to deploy, test, or release to external users.


See Source to learn more

---

### Source
https://developer.android.com/studio/build