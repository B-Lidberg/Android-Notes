# Migrating From XML to Compose


## Advice:
Jetpack Compose is designed to work with the established view-based UI approach. If you're building a new app, the best option might be to implement your entire UI with Compose. But if you're modifying an existing app, you might not want to fully migrate your app all at once. Instead, you can combine Compose with your existing UI design implementation.

There are two main ways you can **integrate Compose with a view-based UI**:

-   You can add Compose elements into your existing UI, either by creating an entirely new Compose-based screen, or by adding Compose elements into an existing activity, fragment or view layout.

-   You can add a view-based UI element into your composable functions. Doing so lets you add Android views into a Compose-based design.

**Migrating the entire app to Compose** is best achieved step by step with the granularity the project needs. You can migrate one screen at a time, or even one fragment or any other reusable UI element at a time. You can use several different approaches:

-   The _bottom-up_ approach starts migrating the smaller UI elements on the screen, like a `Button` or a `TextView`, followed by its `ViewGroup` elements until everything is converted to composable functions.
    
-   The _top-down_ approach starts migrating the fragments or view containers, like a `FrameLayout`, `ConstraintLayout`, or `RecyclerView`, followed by the smaller UI elements on the screen.
    

These approaches assume each screen is self-contained, but it's also possible to migrate shared UI, like a design system, to Jetpack Compose.

#### Documentation:
[Adopting Compose in your app](https://developer.android.com/jetpack/compose/interop)

#### Codelab:
- [Migrating To Jetpack Compose](https://developer.android.com/codelabs/jetpack-compose-migration#0)


#Jetpack-Compose