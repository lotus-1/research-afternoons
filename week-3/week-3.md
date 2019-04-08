
# ****Testing methodologies****

# The most 5 popular testing frameworks
<br>
### Jasmine

![](https://raygun.com/blog/wp-content/uploads/2017/05/Front-end-development-frameworks.png)

Jasmine is one of the most popular Javascript unit testing frameworks. It’s use is wide. It has test runners for Python and Ruby too. It is described as “a behavior-driven development framework for testing JavaScript code“.
It is very easy to get started in Jasmine. If your developer is new to  JavaScript unit testing, the authors conveniently have standalone distributions of Jasmine that can be run in a browser. Jasmine is one of the most preferred test runners all across. Here are some key features of Jasmine:

* Simple to setup
<br>
* Supported by many CIs (Codeship, Travic, etc.)
<br>
* Descriptive syntax for BDD testing
<br>
* Lots of extendability – 3th party libraries
like jasmine-jquery, jasmine-dom, jasmine-react etc.

### Mocha

![](https://raygun.com/blog/wp-content/uploads/2017/05/Front-end-development-frameworks-3.png)

Mocha is an all-rounder testing tool that allows your developer to choose the preferred taxonomy (assert, expect, should), and a long list of features including coverage reporting, notifications, and more. It’s easily installed with npm, the node package manager, and you can install it globally to get some extra helpers. Here are some key features of Mocha

* Easy to setup
<br>
* Allow use of any assertion library – Must.js, Chai, expect.js,  etc.
<br>
* CI support
<br>
* Highly extensible
<br>
* Easy async testing

### Karma

![](https://i.ytimg.com/vi/bJc078szrZA/maxresdefault.jpg)

A “spectacular” test runner for Java-Script (the project was initially called Testacular), Karma is very easy to get up and running to do your JavaScript testing. Your test runner is important for your process, so hopefully you are or plan to eventually run your tests in a continuous integration environment to ensure the code quality. Here are some key points of Karma.

* CI support
<br>
* Highly extensible
<br>
* Easy async testing

### Wrapping Up

![](https://static.frontendmasters.com/assets/courses/2019-04-03-deep-javascript-v3/thumb.jpg)

Overall, out of hundreds of testing tools in JavaScript, these are the most used Javascript testing frameworks. However, if you are mostly focused on Node.JS then Mocha can be Magical for you. Then, if you’re interested in end-to-end testing or integration testing, we recommend checking out CasperJS for browser scripting. You can also keep your eye on Protractor if AngularJS interests you.

### AVA

![](https://github.com/avajs/ava/raw/master/media/header.png)
AVA helps you get it done. AVA is a test runner for Node.js with a concise API, detailed error output, embrace of new language features and process isolation that let you write tests more effectively. So you can ship more awesome code. <br>
why is ava ?
* Minimal and fast
<br>
* Simple test syntax
<br>
* Runs tests concurrently
<br>
* Enforces writing atomic tests
<br>
* No implicit globals
<br>
* Includes TypeScript & Flow type definitions
<br><br>

# Test method
A test method is a method for a test in science or engineering,
such as a physical test, chemical test, or statistical test.
It is a definitive procedure that produces a test result.
In order to ensure accurate and relevant test results,
a test method should be "explicit, unambiguous, and experimentally feasible.",
as well as effective and reproducible.

#### Black Box Testing	:
A software testing method in which the internal structure/design/implementation of the item being tested is not known to the tester. These tests can be functional or non-functional, though usually functional. Test design techniques include Equivalence partitioning, Boundary Value Analysis, Cause-Effect Graphing.
This method is named so because the software program, in the eyes of the tester, is like a black box; inside which one cannot see. This method attempts to find errors in the following categories:

* Incorrect or missing functions
* Interface errors
* Errors in data structures or external * * database access
Behavior or performance errors
Initialization and termination errors

#### White Box Testing:
A software testing method in which the internal structure/design/implementation of the item being tested is known to the tester. Test design techniques include Control flow testing, Data flow testing, Branch testing, Path testing.
The tester chooses inputs to exercise paths through the code and determines the appropriate outputs. Programming know-how and the implementation knowledge is essential. White box testing is testing beyond the user interface and into the nitty-gritty of a system.

This method is named so because the software program, in the eyes of the tester, is like a white/transparent box; inside which one clearly sees.
#### Gray Box Testing:
A software testing method which is a combination of Black Box Testing method and White Box Testing method.
In Gray Box Testing, the internal structure is partially known. This involves having access to internal data structures and algorithms for purposes of designing the test cases, but testing at the user, or black-box level.
#### Agile Testing:
A method of software testing that follows the principles of agile software development.
#### Ad Hoc Testing:
A method of software testing without any planning and documentation.

# The difference between equal and deepEqual

### t.equal(actual, expected, msg):

Actual and expected are equal, and (optional) a description can be added in msg (compares whether the references pointing to same object or not).

### t.deepEqual(actual, expected, msg):

Actual and expected have the same structure and nested values using nodes deepEqual() algorithim with (===) on leaf nodes and an optional description of the assertion msg.
deepEqual goes deeper into the object when it reaches the address. It compares the strings for actual and expected with === and decides that the two objects are equal.

# A JavaScript Unit Testing framework.

*`QUnit`*

QUnit is a powerful, easy-to-use JavaScript unit testing framework. It's used by the jQuery, jQuery UI and jQuery Mobile projects and is capable of testing any generic JavaScript code

For example:<br>
QUnit.test( "hello test", function( assert ) { <br>
assert.ok( 1 == "1", "Passed!" );
});

*`Jest`*

Jest is a delightful JavaScript Testing Framework with a focus on simplicity.

It works with projects using: Babel, TypeScript, Node, React, Angular, Vue and more!

*`tape`*

Tap-producing test harness for node and browsers.
![](https://catonmat.net/images/testling/testling-ci-test-example-badge.png);<br>
You always need to require('tape') in test files, you can also run tests using the tape binary to utilize globbing.<br>
Additionally, it is possible to make tape load one or more modules before running any tests.
