# Red Green Refactor
Red-Green-Refactor describes the steps that you follow when practicing the TDD process.

![Red-Green-Refactor](media/redgreenrefactor.png)

**Red**: Start any new task by writing a failing (red) test. This is for any new feature, behavior change, or bug fix that doesn’t already have a test for what you will be doing. You only write the tests and the bare minimum code to make it compile. Make sure you run the test and see it fail.

**Green**: Write the minimum code to make the test pass (green). You’re not worried about making it pretty or adding any additional functionality at this step. Write the requirements for that test, then run the test to see it pass. Stay here at this step until your test is green.

**Refactor**: Now is when you can prettify your code, and make any other changes to make sure your code is clean. You know that your changes are safe and correct as long as your tests stay green. Having these tests to ensure the code meets the specifications helps you refactor with confidence.