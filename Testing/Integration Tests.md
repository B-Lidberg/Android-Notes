# Integration Tests

**Integration tests** move beyond isolated elements and begin testing how things work together. You write these type of tests when you need to check how your code interacts with other parts of the Android framework or external libraries. Usually, you’ll need to integrate with a database, filesystem, network calls, device sensors, etc. These tests may or may not require a device or emulator to run; they are a bit slower than unit tests. They are also called **medium tests**.


You can still use **[[JUnit]]**, **[[Mockito]]** and **[[Robolectric]]** in integration tests to verify state and behavior of a class and its dependencies as you’ll see in later chapters.

Google, in its testing fundamentals documentation, also suggests **[[Espresso]]** for medium tests. For example, to perform validation and stubbing of intents or to perform actions on view objects. However, some may consider these kind of tests as UI tests because you would be interacting with UI elements.