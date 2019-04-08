# Unit vs integration testing vs end-to-end testing

 ## unit test

##### A unit test runs some code over a segment of your program checking the input and output. These tests allow developers to check individual areas of a program to see where(and why) errors occur.
##### This comes with an inherent understanding of what you’re trying to test for and how the code should function. Checking for bugs and errors can only be useful when you know exactly what you’re looking for.
*What’s in a Good Unit Test?
OK, so TDD works. Write tests first.But how do you write a good unit test?
We’re going to use tape for the tests because of its crystal clarity and essential simplicity.*

##### How unit tests are used?
##### Design aid: written during design phase, prior to implementation.
##### Feature documentation & test of developer understanding: The test should provide a clear description of the feature being tested.
##### QA/Continuous Delivery: The tests should halt the delivery pipeline on failure and produce a good bug report when they fail.
![img](https://martinfowler.com/bliki/images/unitTest/sketch.png)

## integration test

##### Integration Testing is defined as a type of testing where software modules are integrated logically and tested as a group.
##### A typical software project consists of multiple software modules, coded by different programmers. Integration Testing focuses on checking data communication amongst these modules.
![img](https://martinfowler.com/bliki/images/integrationTesting/sketch.png)

## End to end test

##### End to End Testing, also called E2E or UI testing is one the many testing phases covering a web application.
##### By writing an End to End Test it is possible to assert whether a web application works as expected or not. Plus, with E2E you will test the user flow of your application. Starting from the signup process.
##### Is End to End Testing really important?
##### Yes it is. But nobody likes E2E tests. They can be slow, cumbersome and expensive.
##### Why end to end testing?
##### There are pros and cons to all testing methods. End to end testing is the closest to actual user testing which is one of its main advantages. The closer the test is to mimicking the user, the more likely it will catch issues that the user might experience.

![img](https://cdn.softwaretestinghelp.com/wp-content/qa/uploads/2015/08/end-to-end-testing-process.jpg)

## When would you use each kind of test?
##### Unit :Is when you test only a certain isolated unit of code.
#####  Integration :Is when you test an integration, some code you usually interact with but don't have control over.
#####  End-to-end :Is when you test the complete application, from one end to the other end.  
<br>  <br>
##### The key is to find the right balance between unit, integration and end-to-end tests:

![img](https://codeahoy.com/img/blogs/test_pyramid.png)

#####  To find the right balance between all three test types, the best visual aid to use is the testing pyramid.
#####  The bulk of your tests are unit tests at the bottom of the pyramid. As you move up the pyramid, your tests gets larger, but at the same time the number of tests (the width of your pyramid) gets smaller.
