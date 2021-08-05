# ComposeView

ComposeView is an AndroidView that is an empty placeholder for a view inside of XML

There are no custom attributes & uses `setContent` to compose the UI 
```kts
androidx.compose.ui.platform.ComposeView
	android:id="@+id/composeView"
	android:layout_width="wrap_content"
	android:layout_height="wrap_content"
```

```kts
composeView.setContent {
	Text(text = "Sample")	
}
```

```kts
container.addview(
	ComposeView(this).apply {
		setContent {
			Text(text = "Sample")
		}
	}
)
```

If we want to return a [[Composable]] as the [[View]] for a [[Fragment]] instead of inflating a layout
```kts
override fun onCreateView(
	...
): View {
	return ComposeVew(requireContext())
		.apply {
			setContent {
				Text(text = "Sample")
			}
		}
}
```
Sample of `class ComposeView`
```kts
class ComposeView @JvmOverloads
constructor(
	context: Context,
	attrs: AttributeSet? = null,
	defStyleAttr: Int = 0
)
```


[Migrating to Compose: ComposeView](https://www.youtube.com/watch?v=BarlWza2QXY&list=PLMj-9x9aTqPq3dLyed3vKPn1p2zheenFD&index=1)