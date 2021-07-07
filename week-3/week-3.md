Test Coverage
-------------

![](https://cdn.softwaretestinghelp.com/wp-content/qa/uploads/2015/09/test-coverage.jpg)  

*What is Test Coverage?*
It is defined as a metric in Software Testing. It measures the amount of testing performed by a set of test. Wherever we can count things and can tell whether or not each of those things has been tested by some test, then we can measure coverage and is known as test coverage.

*Why it is useful?*  
1-To find the areas which are in the requirements document but not covered in the test cases.  
2-It help to take decision about quality of product.   
3- It help us to bridge the gap between requirement and test cases.  
4- To calculate the percentage of coverage items that were tested by a set of tests.  
5-To report coverage items that have not been tested yet.

*What are Istanbul and NYC?*  
**Istabul** is a JS code coverage tool that written in JS.  
* All-javascript instrumentation library that tracks statement, branch, and function coverage and reverse-engineers line coverage with 100% fidelity.

* Command line tools to run node unit tests "with coverage turned on" and no cooperation whatsoever from the test runner.

* Ability to use as middleware when serving JS files that need to be tested on the browser.

**NYC** is it's the NEW Istanbul command line interface, which have replaced the old Istanbul tool bin, in NYC, you can get reports on different scopes by using different command line flags.

*How would you use them to improve your testing?*  
It's a tool to support JavaScript programmers to keep tracking their code testing and know how well they have done it.

*Use Istanbul/nyc to calculate your code coverage for the TDD workshop.*  
by these commands:

-Install istanbul from NPM: `npm install istanbul -D`  
-get a coverage report:
`node_modules/.bin/istanbul cover node_modules/.bin/tape ./test/*.test.js`  
-run the coverage by: `istanbul cover test.js`

*Does 100% coverage mean you have tested everything correctly?*  
No, It means that :  
**Statements**: How many of the statements in you code are executed.  
**Branches**: Conditional statements create branches of code which may not be executed (e.g. if/else). This metric tells you how many of your branches have been executed.  
**Functions**: The proportion of the functions you have defined which have been called.  
**Lines**: The proportion of lines of code which have been executed.
