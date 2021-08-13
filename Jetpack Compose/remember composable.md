Composable functions can store a single object in memory by using the [`remember`](https://developer.android.com/reference/kotlin/androidx/compose/runtime/package-summary#remember(kotlin.Function0)) composable. A value computed by `remember` is stored in the Composition during initial composition, and the stored value is returned during recomposition. `remember` can be used to store both mutable and immutable objects.

**Note:** `remember` stores objects in the Composition, and forgets the object when the composable that called `remember` is removed from the Composition.

[`mutableStateOf`](https://developer.android.com/reference/kotlin/androidx/compose/runtime/package-summary#mutableStateOf(kotlin.Any,androidx.compose.runtime.SnapshotMutationPolicy)) creates an observable [`MutableState<T>`](https://developer.android.com/reference/kotlin/androidx/compose/runtime/MutableState), which is an observable type integrated with the compose runtime.

```kts
interface MutableState<T> : State<T> {
	override var value: T
}
```


There are three ways to declare a `MutableState` object in a composable:

-   `val mutableState = remember { mutableStateOf(default) }`
-   `var value by remember { mutableStateOf(default) }`
-   `val (value, setValue) = remember { mutableStateOf(default) }`


While `remember` helps you retain state across recompositions, the state is not retained across configuration changes. For this, you must use `rememberSaveable`. `rememberSaveable` automatically saves any value that can be saved in a `Bundle`. For other values, you can pass in a custom saver object.

Use [`rememberSaveable`](https://developer.android.com/reference/kotlin/androidx/compose/runtime/saveable/package-summary#rememberSaveable(kotlin.Array,androidx.compose.runtime.saveable.Saver,kotlin.String,kotlin.Function0)) to restore your UI state after an activity or process is recreated. `rememberSaveable` retains state across recompositions. In addition, `rememberSaveable` also retains state across activity and process recreation.