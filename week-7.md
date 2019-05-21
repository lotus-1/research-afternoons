# Security and Authentication

# Web Storage

1. What are local storage and session storage and what is the difference between the two?

LocalStorage:
<li> Web storage can be viewed simplistically as an improvement on cookies, providing much greater storage capacity. Available size is 5MB which considerably more space to work with than a typical 4KB cookie.</li>
<li> The data is not sent back to the server for every HTTP request (HTML, images, JavaScript, CSS, etc) - reducing the amount of traffic between client and server.</li>
<li> The data stored in localStorage persists until explicitly deleted. Changes made are saved and available for all current and future visits to the site.</li>
<li> It works on same-origin policy. So, data stored will only be available on the same origin. </li>
If you're building a static site (like a single page app, for instance), using something like local storage means your web pages can run independently of any web server. They don't need any backend language or logic to store data in the browser: they can just do it as they please.

sessionStorage:

<li> It is similar to localStorage. </li>
<li> Changes are only available per window (or tab in browsers like Chrome and Firefox). Changes made are saved and available for the current page, as well as future visits to the site on the same window. Once the window is closed, the storage is deleted. </li>
<li> The data is available only inside the window/tab in which it was set.</li>
<li> The data is not persistent i.e. it will be lost once the window/tab is closed. Like localStorage, it works on same-origin policy. So, data stored will only be available on the same origin.</li>

2. Why would you use cookies vs local/session storage?

Cookies are small text files that websites place in a browser for tracking or login purposes. Meanwhile, localStorage and sessionStorage are new objects, both of which are storage specifications but vary in scope and duration. Of the two, localStorage is permanent and website-specific whereas sessionStorage only lasts as long as the duration of the longest open tab.

3. Think of use cases where local/session storage could be useful.

localStorage: searching for a name/ event, next time when searching the same thing it will appear as the first option.

sessionStorage: store the state of the interface, so when coming back to a page, you can restore the screen the way the user was looking at it.

4. Demo a simple usage of localStorage and sessionStorage: setting, getting and removing an item in storage.

Syntax
```
//To store the data:
localStorage.setItem(“key”,”value”);

//To retrieve the data:
localStorage.getItem(“key”);

//To update the data (the same as to store the data):
localStorage.setItem(“key”,”value”);

//To remove one entry:
localStorage.removeItem(“key”);

//To clear all the data:
localStorage.clear();
```
