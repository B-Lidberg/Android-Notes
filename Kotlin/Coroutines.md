# Coroutines

A _coroutine_ is a concurrency design pattern that you can use to simplify code that executes asynchronously.

[[Kotlin]] Coroutines are based on established concepts from other languages

On Android, coroutines help to manage long-running tasks that might otherwise block the main thread and cause your app to become unresponsive.


### Features
-   **Lightweight**: You can run many coroutines on a single thread due to support for [_suspension_](https://kotlinlang.org/docs/reference/coroutines/basics.html), which doesn't block the thread where the coroutine is running. Suspending saves memory over blocking while supporting many concurrent operations.
-   **Fewer memory leaks**: Use [_structured concurrency_](https://kotlinlang.org/docs/reference/coroutines/basics.html#structured-concurrency) to run operations within a scope.
-   **Built-in cancellation support**: [Cancellation](https://kotlinlang.org/docs/reference/coroutines/cancellation-and-timeouts.html) is propagated automatically through the running coroutine hierarchy.
-   **Jetpack integration**: Many Jetpack libraries include [extensions](https://developer.android.com/kotlin/ktx) that provide full coroutines support. Some libraries also provide their own [coroutine scope](https://developer.android.com/topic/libraries/architecture/coroutines) that you can use for structured concurrency.


[Kotlin Coroutines Overview](https://kotlinlang.org/docs/coroutines-overview.html)
[Coroutines on Android](https://developer.android.com/kotlin/coroutines)