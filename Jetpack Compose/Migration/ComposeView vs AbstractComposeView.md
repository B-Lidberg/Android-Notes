# ComposeView vs. AbstractComposeView

Both allow use of composables directly inside of existing [[Android UI Toolkit]] classes

[[ComposeView]] can be placed directly into an existing layout and used to compose the UI from the hosting Android class

- **Great for switching out existing views for composables or house composables for the layout of a parent class such as viewholders or fragments**

[[AbstractComposeView]] needs to be extended from the CustomView class which can then be used to contain any composable UI and it's logic before being hosted inside of the Android class.

- **Great when needing to promote reuse of composables between composable ui and the Android UI Toolkit. It also helps to abstract configurable information for a component helping to keep a clear line between composable UI and Android UI Toolkit with in existing classes.**

- If a view is complex and may contain many mutable properties or holds internal logic, you should use **AbstractComposeView**. It will also allow more control over the composable we are providing.

- Eases the sharing between both android classes and composable ui. 

- Can be used to simplify the reuse of composables between the Android UI Toolkit & Composables

---

### Advice:
If new to both:

Start with using a ComposeView. After placing a ComposeView inside of an existing Android Layout, you can evaluate how the changes feel in your codebase. This allows avoiding over optimizing and over extracting code when it's not needed. Keeping it as simple as it needs to be. 

If it starts becoming a bit complex or having to reuse composable, then the AbstractComposeView would be a good subsitute.

[Migrating to Compose: ComposeView Comparisons](https://www.youtube.com/watch?v=X5o79Mvr7vo&list=PLMj-9x9aTqPq3dLyed3vKPn1p2zheenFD&index=3)