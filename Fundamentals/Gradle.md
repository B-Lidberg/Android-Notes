# Gradle
Gradle is a build automation tool for multi-language software development. It controls the development process in the tasks of compilation and packaging to testing, deployment, and publishing.

Creating custom build configurations requires you to make changes to one or more build configuration files, or `build.gradle` files. These plain text files use Domain Specific Language (DSL) to describe and manipulate the build logic using [[Groovy]] or [[Kotlin]]

Android Studio uses [Gradle](http://www.gradle.org/), an advanced build toolkit, to automate and manage the build process, while allowing you to define flexible custom build configurations. Each build configuration can define its own set of code and resources, while reusing the parts common to all versions of your app. The Android plugin for Gradle works with the build toolkit to provide processes and configurable settings that are specific to building and testing Android applications.

Gradle and the Android plugin run independent of Android Studio. This means that you can build your Android apps from within Android Studio, the command line on your machine, or on machines where Android Studio is not installed (such as continuous integration servers). If you are not using Android Studio, you can learn how to [build and run your app from the command line](https://developer.android.com/studio/build/building-cmdline). The output of the build is the same whether you are building a project from the command line, on a remote machine, or using Android Studio.

>**Note:** Because Gradle and the Android plugin run independently from Android Studio, you need to update the build tools separately. Read the release notes to learn how to [update Gradle and the Android plugin](https://developer.android.com/studio/releases/gradle-plugin#updating-plugin).


### TestImplementation vs Implementation
_Groovy Example_
```groovy
dependencies { 
	... 
	testImplementation 'junit:junit:4.13.2' 
}
```
`testImplementation` instead of `implementation` when you’ll use a dependency only for testing. This means that it won’t be bundled into the application (APK) that your device or emulator will run.

---
### Source
https://developer.android.com/studio/build