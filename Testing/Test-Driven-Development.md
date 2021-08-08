# Test Driven Development (TDD)


TDD is a process in which you write the tests for the code you are going to add or modify _before_ you write the actual code. Because it’s a process and not a library, you can apply it to any project, be it Android, iOS, web or anything else.


## Why is TDD important?

-   **Write intentionally**: Well-written tests describe what your code should do. From the start, you will focus on the end result. Writing these specifications as tests can keep the result from deviating from the initial idea.
   
-   **Automatically document**: When coming to a piece of code, you can look at the tests to help you understand what the code does. Because these are tests — and, again, a process — rather than a static document, you can be sure that this form of documentation is likely up-to-date.
   
-   **Keep maintainable code**: When practicing TDD, it encourages you to pay attention to the structure of your code. You will want to architect your app in a testable way, which is generally cleaner and easier to maintain and read. For example, decoupled classes are easier to set up test classes for, encouraging you to structure your classes this way. Refactoring is also built into this development process. By having this refactoring step built-in, your code can stay squeaky clean!
   
-   **Have confidence in your code**: Tests ensure that your code works the way it should. Because of this, you can have greater confidence that what you wrote is “complete.” In addition, with any changes that you make in the future, you can know that you didn’t break that functionality as long as the tests you wrote pass.
   
-   **Develop faster**: Using a process that promotes more readable and maintainable code and that acts as self-documentation means you can spend less time trying to understand what the code does when revisiting it and use that time for solving your problem instead. Also, the code you write using the TDD process is less error-prone from the start, so you will need to spend less time on fixing the code down the road.

-   **Higher test coverage**: If you’re writing tests alongside your code, you’re going to have more test coverage over the code. This is important to many organizations and developers.

---



## Key points

-   TDD is a process of writing tests before you write your actual code. You can apply TDD to any sort of programming.
-   Practicing TDD helps you to code quickly and with intent, document automatically, have confidence your code is maintainable, and have better test coverage.
-   TDD follows the [[Red Green Refactor]] steps.
-   This process always starts with writing a failing test. No matter what, you always want to see the test fail.
-   Only after you write your test and see it fail do you write your new code or change your existing code.
-   You only ever write enough code to make your test pass. If there’s more code you need to write, you need another test first.
-   You follow up with refactoring to make your code clean and readable.
-   Learning to write good tests takes practice.