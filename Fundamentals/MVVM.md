# Model-View-ViewModel (MVVM)

![MVVM image](media/mvvm-architecture.png)

MVVM is a commonly used architectural pattern and the recommended [[Architecture]] for Android by Google.

> _**Note:** It's impossible to have one way of writing apps that works best for every scenario. That being said, this recommended architecture is a good starting point for most situations and workflows. If you already have a good way of writing Android apps that follows the [common architectural principles](https://developer.android.com/jetpack/guide#common-principles), you don't need to change it._

-   **Model**: Same as the Model layer from MVC/MVP.
    
-   **View**: Notifies the ViewModel about user actions. Subscribes to streams of data exposed by the ViewModel.
    
-   **ViewModel**: Retrieves data from the Model and updates it accordingly. Exposes streams of data ready to be displayed, but it doesn’t know and doesn’t care about who is subscribed to the streams.

---

 _A [[ViewModel]] object provides the data for a specific UI component, such as a fragment or activity, and contains data-handling business logic to communicate with the model. For example, the **[`ViewModel`](https://developer.android.com/topic/libraries/architecture/viewmodel)** can call other components to load the data, and it can forward user requests to modify the data. The `ViewModel` doesn't know about UI components, so it isn't affected by configuration changes, such as recreating an activity when rotating the device._

---
### Source:
[Guide to app architecture](https://developer.android.com/jetpack/guide)


