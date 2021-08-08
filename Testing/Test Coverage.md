# Test Coverage

You can measure how many lines of code of your app have been executed when you run your tests. An app with a high test coverage percentage “suggests” that it works as expected and has a lower chance of containing bugs.

You may have asked yourself how many tests should you write. As mentioned before, you should at least write those that cover the most common scenarios.

![test-coverage](media/test-coverage.png)

-   **Function/method coverage**: How many functions have been called?
-   **Statement coverage**: How many statements of each function have been executed?
-   **Branch coverage**: Has each branch in an `if` or a `when` statement been executed?
-   **Condition coverage**: Has each subcondition in an `if` statement been evaluated to `true` and also to `false`?


### Coverage Tools
- **JaCoCo** (Java Code Coverage Library) 
	- This library generates a report for you to check which lines were covered by your tests (green) and which ones were not (red or yellow). _(Works with Kotlin)_
- **Android Studio**
	- comes with a **built-in feature** to run tests with Coverage.