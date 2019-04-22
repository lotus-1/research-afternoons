# Engineering #

Modules
--------

1. Why should you modularise your code?  

Good authors divide their books into chapters and sections; good programmers divide their programs into modules.  

*Modules in javascript* refers to small units of independent, reusable code. They are the foundation of many JavaScript design patterns and are critically necessary when building any JavaScript-based application.
Good modules, however, are highly self-contained with distinct functionality, allowing them to be shuffled, removed, or added as necessary, without disrupting the system as a whole.

 + *Maintainability*
By definition, a module is self-contained. A well-designed module aims to lessen the dependencies on parts of the codebase as much as possible, so that it can grow and improve independently. Updating a single module is much easier when the module is decoupled from other pieces of code.

+ *Namespacing*
In JavaScript, variables outside the scope of a top-level function are global (meaning, everyone can access them). Because of this, it’s common to have “namespace pollution”, where completely unrelated code shares global variables.
Sharing global variables between unrelated code is a big no-no in development.
As we’ll see later in this post, modules allow us to avoid namespace pollution by creating a private space for our variables.

+ *Reusability*
we’ve all copied code we previously wrote into new projects at one point or another. For example, let’s imagine you copied some utility methods you wrote from a previous project to your current project.  


2. What are require and module.exports?

*The module object* has a special property, called exports, which is responsible for defining what a module makes available for other modules to use. In Node.js terminology, module.exports defines the values that the module exports.
Therefore, we can export any value or function or other object we would like to export by attaching it as a property of the module.exports object. For example, if we would like to export a variable named temperature, we could make it available for use outside the module by simply adding it as a new property of module.exports as follows:

 `module.exports.temperature = temperature;`

In order to import the module, we need to use a special keyword used to import things, and it is called require. Where module.exports lets us set things for export, require lets us specify modules to be imported into the current module.  
The module require is a function to which we pass the path of the module we would like to import. For instance, to import a module defined in `music.js`, we would `require('./music')`, where we have specified the relative path.

click [For more details](https://stackabuse.com/how-to-use-module-exports-in-node-js/) .

3. Why can't you use them in the browser?  

Both the browser and Node use JavaScript as their programming language.
Building apps that run in the browser is a completely different thing than building a Node.js application.
In the browser, most of the time what you are doing is interacting with the DOM, or other Web Platform APIs like Cookies. Those do not exist in Node, of course.
For example you don’t have the `(document), (window)` and all the other objects that are provided by the browser.
In Node.js you control the environment. Unless you are building an open source application that anyone can deploy anywhere, you know which version of Node you will run the application on. Compared to the browser environment, where you don’t get the luxury to choose what browser your visitors will use, this is very convenient.
Another difference is that Node uses the CommonJS module system, while in the browser we are starting to see the ES Modules standard being implemented.
This means that for the time being you use `require()` in Node and `import` in the browser.
4. How might you modularise client-side code - what does webpack do?

we can modularise it in many ways like browserify , babel and converting our code from Es5 to Es6, and using `webpack` which is a module bundler. Its main purpose is to bundle JavaScript files for usage in a browser, yet it is also capable of transforming, bundling, or packaging just about any resource or asset.

![](https://survivejs.com/538c4af0d21e375d6d252d38cbb8a993.png)

`Webpack` begins its work from entries. Often these are JavaScript modules where webpack begins its traversal process. During this process, `webpack` evaluates entry matches against loader configurations that tell `webpack` how to transform each match.

 Asyncronous functions :  
 -----------------
 ![](http://blogs.quovantis.com/wp-content/uploads/2015/08/Asynchronous-Programming-understanding.jpg)

1. Why should you use asyncronous forms of functions wherever possible in Node?  
*asynchronous* programming is that while your code waits for something to be done (like an API call or a response from a mystic and far away database) it can do something else. In other words, your code doesn’t get blocked when a process is taking a long time. This is actually the main reason why Node.js was even created; servers running synchronous code spend a lot of time waiting. If servers can process requests while they are waiting for I/O, stuff gets done faster.  
```
 This is synchronous:
function processData() {
   let data = fetchDataInAFarAwayAndMysticDatabase();
   data += 1;
   return data;
}
 //This is asynchronous:
function processData(callback) {
   fetchDataInAFarAwayAndMysticDatabase(function (err, data) {
      if (err) {
          return callback(err);
       }
       data += 1;
       callback(null, data);
   });
}
```
2. What are error-first callbacks, and why is it important to follow that pattern in your own code?  

There’s really only two rules for defining an error-first callback:
- The first argument of the callback is reserved for an error object. If an error occurred, it will be returned by the first err argument.  
- The second argument of the callback is reserved for any successful response data. If no error occurred, err will be set to null and any successful data will be returned in the second argument.
 a real-life example with the basic method `fs.readFile()`:
```
fs.readFile('/foo.txt', function(err, data) {
 // TODO: Error Handling Still Needed!
 console.log(data);
});
```
`fs.readFile()` takes in a file path to read from, and calls your callback once it has finished. If all goes well, the file contents are returned in the data argument. But if somethings goes wrong (the file doesn’t exist, permission is denied, etc) the first err argument will be populated with an error object containing information about the problem.  

3. Why should you avoid using throw in callbacks?  

Throw really does two things: it stops the program, and it finds a catch to execute. Let’s examine these ideas one at a time.

When JavaScript finds a throw keyword, the first thing it does is stop dead in its tracks, which prevents any more functions from running. By stopping like this, it mitigates the risk of any further errors occurring and helps us not to get the state of our program all twisted.

4. When might you use the syncronous form of a function instead?

`Synchronous` means one at a time. one line of code is being executed at time in order the code appears. So when we want things to happen one at the time we use synchronous form .
also like when we want to excute each code line by line.

Input/output (the fs and path modules):
------------------------------
![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT8LxK_in_9mV5yp8AuMiR0zdry-I2E-0m7KdAAKo8KB-Lab7iVTQ)

1. What kind of tasks does the fs module enable you to perform that you wouldn't be able to in the browser?  

 + filesystem access functionality.
 + control of your enviroment  [unless you're building an open source], you know which version of Node.js you'll run the app on, compared to the browser which you can't choose what browser the visitor will use.
 + Node.js we use `require()` in browser we use `import`
 + Another difference is that Node.js uses the `CommonJS` module system, while in the browser we are starting to see the ES Modules standard being implemented.  


2. What are some of the issues of working with paths when accessing a file system?   
 + `_dirname` provides the absolute path to the working directory where the file being executed is located.   
 + `_filename` variable provides the absolute path to the file that is currently executing;   

3. How does the path module help, and why should you use it instead of manually writing file paths as strings?  

The `path` module provides a way of working with directories and file paths.

for example `path.join()` will add the "/" between the files name like this :
```
var path = require('path');

var x = path.join('Users', 'Refsnes', 'demo_path.js');

console.log(x);
// will return Users\Refsnes\demo_path.js
```  

 more info [here](https://www.w3schools.com/nodejs/ref_path.asp)

Working with URLs (the url and querystring modules)
-------------------  
![](https://i0.wp.com/www.dignited.com/wp-content/uploads/2018/09/url_istock_nicozorn_thumb800.jpg?fit=640%2C360&ssl=1)

1. What is a urlObject and how is it structured?

a URL string is a structured string containing multiple meaningful elements, when parsed a *urlObject* is returned containing properties of each one of these elements.  

2. Why is it important to be able to turn JavaScript objects into querystrings and back again?  

When working with the query string, it is usually best to grab it once, and then be done with that task. This will prove substantially helpful if you need to refer to the query string more than once in your code. If we do the work once, and do it right, then we have created a nice little tool that we can use over and over throughout our code.
So perhaps the best way to accomplish this task is to turn the query string into a JavaScript object.

3. Why is it a bad idea to build a query string manually from other strings (think about URL encoding and escape characters)?

Web pages can be requested with query strings. The QueryString in ASP.NET accesses this information. When you load file.html?x=y, it parses "x" and "y". Most examples show one way of using this NameValueCollection. There is a faster way.
Because we only access the first key and value, this code doesn't work for more than one key value pair.
