## JS Questions

* Explain event delegation

+ Event delegation is when a listener is added to a parent elements vs specific nodes.

* Explain how `this` works in JavaScript

* Explain how prototypal inheritance works

+ Inheritance is prototype based, meaning it inherits from objects instead of classes.

* Why is it called a Ternary expression, what does the word "Ternary" indicate?

+ Ternary expression takes in three arguments and it can act as a replacement for an if statement, the word ternary has the prefix of three and the suffix of relating to, so ternary literally means relating to three.

* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?

Null: Variable is explicitly set to have no value, it has been initialized to zero

Undefined: This variable has never been initialized

Undeclared: This variable does not have a type, this var does not exist so you cannot access it

* How would you go about checking for any of these states?

+ if (a === null/undefined/undelcaraed) return true;

* What is a closure, and how/why would you use one?

+ Closure: inner function that has access to to the outer functions scope change. It has access to inner/outer variables as well as global variables.

* What's a typical use case for anonymous functions?

+ Can be more flexible because it can be valid to use an anonymous function whenever you can use an expression.

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

+ The first one the name of the function is Person, the second, the variable person is being set equal to a function called Person, and the third the var person is setting the function Person to a new person.

* What's the difference between `.call` and `.apply`?

+ A is for array, C is for coma, apply is used for array, call is used for specifically listed parameters

* Explain `Function.prototype.bind`.

+ The bind() function creates a new function (a bound function) with the same function body (internal call property in ECMAScript 5 terms) as the function it is being called on (the bound function's target function) with the this value bound to the first argument of bind(), which cannot be overridden.

* What's the difference between feature detection, feature inference, and using the User Agent string?

+ Feature detection: Checks a feature for existence
	if (window.XMLHttpRequest) {
    new XMLHttpRequest();
}

+ Feature inference: checks like feature detection but also assumes that the inference does exists.
	if (document.getElementsByTagName) {
    element = document.getElementById(id);
}

+ User agent string:if (navigator.userAgent.indexOf("MSIE 7") > -1){
    //do something
}

* Explain AJAX in as much detail as possible.

+ AJAX stands for Asynchronous JavaScript and XML. In a nutshell, it is the use of the XMLHttpRequest object to communicate with server-side scripts. It can send as well as receive information in a variety of formats, including JSON, XML, HTML, and even text files.

* Have you ever used JavaScript templating?

+ Yes, I have worked with AngularJS

* Explain "hoisting".

+ JS default of moving declarations to the top of the document.

* Describe event bubbling.

+ Event bubbling directs an event to its intended target, it works like this: A button is clicked and the event is directed to the button. If an event handler is set for that object, the event is triggered. If no event handler is set for that object, the event bubbles up (like a bubble in water) to the objects parent.

* What's the difference between an "attribute" and a "property"?

+ Attribute: defined by HTML

+ Property: defined by DOM

* Why is extending built-in JavaScript objects not a good idea?

+ The browser may implement its own version of the method and silently override yours, so to future proof your code you should not extend built in JS objects.

* What is the difference between `==` and `===`?

+ == lenient tries to convert values of different types before deciding equality.

+ === strict, only compares values that have the same type.

* Explain the same-origin policy with regards to JavaScript.

+ The same-origin policy helps prevent malicious attacks by stopping code from another site executing on your site.

* What is the extent of your experience with Promises and/or their polyfills?

+ Polyfill: In web development, a polyfill (or polyfiller) is downloadable code which provides facilities that are not built into a web browser. It implements technology that a developer expects the browser to provide natively, providing a more uniform API landscape.

+ Promises: The Promise object is used for deferred and asynchronous computations. A Promise represents an operation that hasn't completed yet, but is expected in the future.
	new Promise(executor);
	new Promise(function(resolve, reject) { ... });
* What are the pros and cons of using Promises instead of callbacks?

???????????????

* What tools and techniques do you use debugging Javascript code?

+ console.log
+ setting breakpoints
+ debugger keyword (http://www.w3schools.com/js/js_debugging.asp)

* What language constructions do you use for iterating over object properties and array items?

+for Loops, for in, for each


