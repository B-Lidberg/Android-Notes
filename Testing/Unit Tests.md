# Unit Tests

**Unit tests** are the quickest, easiest to write and cheapest to run. They generally test one outcome of one method at a time. They are independent of the Android framework.

The **System Under Test** (SUT) is one class and you focus only on it. All dependencies are considered to be working correctly — and ideally have their own unit tests — so they are mocked or stubbed. This way, you have complete control of how the dependencies behave during the test.

These tests are the fastest and least expensive tests you can write because they don’t require a device or emulator to run. They are also called **small tests**. 

When you want to ensure that a class or method is working as intended in isolation — this means with no other dependent classes — you write unit tests.

Every test has three phases: set up, assertion and teardown.


## Popular Libraries for Unit Testing
- [[JUnit]]
- [[Mockito]]
- [[Robolectric]] _(also considered an integration testing tool)_