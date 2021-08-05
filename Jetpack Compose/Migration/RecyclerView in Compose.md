# RecyclerView in Compose
Jetpack Compose uses the [`DisposeOnDetachedFromWindow`](https://developer.android.com/reference/kotlin/androidx/compose/ui/platform/ViewCompositionStrategy.DisposeOnDetachedFromWindow) as the default [`ViewCompositionStrategy`](https://developer.android.com/reference/kotlin/androidx/compose/ui/platform/ViewCompositionStrategy). That means that the [Composition](https://developer.android.com/jetpack/compose/lifecycle) is disposed whenever the view is detached from the window.

When using a [`ComposeView`](https://developer.android.com/reference/kotlin/androidx/compose/ui/platform/ComposeView) as part of a `RecyclerView` view holder, the default strategy is inefficient as the underlying Composition instances will remain in memory until the `RecyclerView` is detached from the window. Disposing the underlying Composition when the `ComposeView` is no longer needed by the `RecyclerView` is a good practice.

The [`disposeComposition`](https://developer.android.com/reference/kotlin/androidx/compose/ui/platform/AbstractComposeView#disposeComposition()) function allows you to manually dispose of the underlying Composition of a `ComposeView`. You can call this function when the view is recycled like so:

```kts

import androidx.compose.ui.platform.ComposeViewclass 

MyComposeAdapter : RecyclerView.Adapter<MyComposeViewHolder>() {    
	override fun onCreateViewHolder(parent: ViewGroup, viewType: Int
	): MyComposeViewHolder {        
		return MyComposeViewHolder(ComposeView(parent.context))    
	}    
	
	override fun onViewRecycled(holder: MyComposeViewHolder) {
	
	// Dispose of the underlying Composition of the ComposeView        
	// when RecyclerView has recycled this ViewHolder    
	
		holder.composeView.disposeComposition()    
	}    
	/* Other methods */
}
	class MyComposeViewHolder(val composeView: ComposeView
	) : RecyclerView.ViewHolder(composeView) {    
	/* ... */}

```

As covered in the _ViewCompositionStrategy for ComposeView_ section of the [Interoperability APIs guide](https://developer.android.com/jetpack/compose/interop/interop-apis#composition-strategy), to make the Compose view holder work in all scenarios, it's necessary to use the [`DisposeOnViewTreeLifecycleDestroyed`](https://developer.android.com/reference/kotlin/androidx/compose/ui/platform/ViewCompositionStrategy.DisposeOnViewTreeLifecycleDestroyed) strategy.

```kts

import androidx.compose.ui.platform.ViewCompositionStrategy

class MyComposeViewHolder(val composeView: ComposeView
) : RecyclerView.ViewHolder(composeView) {
	init { 
		composeView.setViewCompositionStrategy(
			ViewCompositionStrategy.DisposeOnViewTreeLifecycleDestroyed)
	}
	fun bind(input: String) {
		composeView.setContent {            
			MdcTheme {                
				Text(input)            
			}        
		}    
	}
}
```










#### Documentation:
[Compose in RecyclerView](https://developer.android.com/jetpack/compose/interop/compose-in-existing-ui#compose-recyclerview)


#Jetpack-Compose