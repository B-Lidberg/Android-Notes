# AbstractComposeView

Used to share custom Android [[View]] Classes or [[Composable]] functions across different parts of our app.

#### Why use it? 
[[ComposeView]] can also get more complex when working with other parts of Compose such as [[State]], more complex composables, or even views that contain a lot of configurable information.

Cannot be placed directly into a layout BECAUSE it is an [[Abstract Class]]. This means a custom view needs to extend from it
```kts
abstract class AbstractComposeView
@JvmOverloads
constructor(
	context: Context,
	attrs: AttributeSet? = null,
	defStyleAttr: Int = 0
) : ViewGroup(...)
```
Custom ComposeView [[Extension]]:
```kts
abstract class MyCustomView
@JvmOverloads
constructor(
	context: Context,
	attrs: AttributeSet? = null
	defStyleAttr: Int = 0
) : AbstractComposeView(...)
```

A composable body is static and we don't have a way to call external callers to provide values for the content within our composables. 
An internal variable reference that can be manipulated and used to control the content of our composable.
We can do so by adding an internal property such as mutable state to our view. This means that our custom view can still be inflated and placed inside of existing layouts, but offers the ability to support some form of internal state.

It's best practice in these scenarios to utilize mutable state objects to ensure the property is thread-safe for [[Jetpack Compose]]
```kts
var text by mutableStateOf("")

@Composable
override fun Content() {
	MyCustomComposable(text)
}
```

```kts
binding.myCustomView.apply {
	text = "Sample text"
}
```

This customview can be used to hold logic around our composable without it being bloated by the ComposeView. There may also be times we want to reuse composables inside of both composable UI and the [[Android UI Toolkit]]. In these scenarios we can split out the body of our content function into it's own composable function.
```kts
@Composable
fun MyCustomComposable(
	text: String
) {
	Text(title)
}
```
We have the custom view class which can be inflated into existing android layouts and a custom composable that can be used in our Compose UI
```kts
@Composable
fun myComposable() {
	MyCustomComposable(text)
}
```

Being able to add this component as a composable or an android view via XML or programmatically with Kotlin means we can abstract out the contents of Compose from our existing classes.

[Migrating to Compose: AbstractComposeView](https://www.youtube.com/watch?v=YxV-PPJ2DrE&list=PLMj-9x9aTqPq3dLyed3vKPn1p2zheenFD&index=2)