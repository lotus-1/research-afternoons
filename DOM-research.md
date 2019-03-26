(1) How can you use JavaScript to create an HTML element and then add it to your webpage? How would you replace an existing element with it?
--------------------------------------------------------------

To create an HTML element using JavaScript, use createElement() method which creates an Element Node with the specified name, you can also use the createTextNode() method to create a text node.
 After the element is created, use the element.appendChild() or element.insertBefore() method to add it to the document.

 If you want to replace an existing element to an element that has been created, follow these steps:
 To add a new element to the HTML DOM, you must create the element (element node) first, and then append it to an existing element.
 Then you must append the text node to the element.
 Finally you must append the new element to an existing element.

 For more examples [click here](https://www.w3schools.com/js/js_htmldom_nodes.asp)



2.What is the difference between using the HTML attribute onClick() and using an event handler in javascript?
--------------------------------------------------------------
A JavaScript can be executed when an event occurs, like when a user clicks on an HTML element.

To execute code when a user clicks on an element, add JavaScript code to an HTML event attribute.

The onclick attribute fires on a mouse click on the element.

 (3) How would you add a `<li>` element to the start of a `<ul>` ?
 ---------------------------------------------------------------
 The insertBefore() method inserts a node as a child, right before an existing child, which you specify.
 Example [here](https://www.w3schools.com/jsref/met_node_insertbefore.asp)


 (4) What is a JavaScript Event? What does event.preventDefault() do and why might you use it?
 --------------------------------------------------------------
 - HTML events are "things" that happen to HTML elements.

 - When JavaScript is used in HTML pages, JavaScript can "react" on these events.
 - An HTML event can be something the browser does, or something a user does.
 - JavaScript lets you execute code when events are detected.
 Event.preventDefault():
 - The preventDefault() method cancels the event if it is cancelable, meaning that the default action that belongs to the event will not occur.

 - For example, this can be useful when:

 Clicking on a "Submit" button, prevent it from submitting a form
 Clicking on a link, prevent the link from following the URL
 - Note: Not all events are cancelable. Use the cancelable property to find out if an event is cancelable.
 Click here for more information(https://www.w3schools.com/jsref/event_preventdefault.asp)  


 (5) What is a NodeList? How is it different from an Array?
 -----------------------------------------------------------

 A NodeList object is a list of nodes extracted from a document. Most browsers return a NodeList object for the method querySelectorAll().
 The NodeList has a length as an array, but it is not an array! (explaination later). The length property defines the number of nodes in a node list, it is useful when you want to loop through the nodes in a node list.
EXAMPLE:
 1.Create a list of all <p> elements
 2.Display the length of the list

Change the background color of all <p> elements in a node list:

var myNodelist = document.querySelectorAll("p");
var i;
for (i = 0; i < myNodelist.length; i++) {
  myNodelist[i].style.backgroundColor = "red";
}

The difference between an array and a NodeList:
A node list may look like an array, but it is not.
An array is a special variable, which can hold more than one value at a time.You can loop through the node list and refer to its nodes like an array.
However, you cannot use Array Methods, like valueOf(), push(), pop(), or join() on a node list.


(6) What are the security concerns around Element.innerHTML and what could you use instead?
 ---------------------------------------------------------------
You can insert HTML into this. But the disadvantage of this method that it has cross site security attacks. For adding text, its better to avoid this for security reasons.
So its better to use textContent:
This will also achieve the same result but it doesn’t have security issues like innerHTML as it doesn’t parse HTML like innerText.
