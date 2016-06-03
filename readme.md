#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
* What excites or interests you about coding?
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.
* Which version control systems are you familiar with?
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.

## HTML Questions

* What does a `doctype` do?
Tells the web browser what language the page is using.
* What's the difference between HTML and XHTML?
XHTML is not so much different from HTML 4.01 standard. The major differences are:

XHTML elements must be properly nested.
XHTML elements must always be closed.
XHTML elements must be in lowercase.
XHTML documents must have one root element.

XHTML is HTML (all the html tags are found in XHTML) that follows the rules of XML (because it is a family of XML).

* What are `data-` attributes good for?
Store variable within HTML element.
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
cookie. A small text file (up to 4KB) created by a Web site that is stored in the user's computer either temporarily for that session only or permanently on the hard disk (persistent cookie). Cookies provide a way for the Web site to recognize you and keep track of your preferences.

sessionStorage is similar to Window.localStorage , the only difference is while data stored in localStorage has no expiration set, data stored in sessionStorage gets cleared when the page session ends. A page session lasts for as long as the browser is open and survives over page reloads and restores

The localStorage property allows you to access a local Storage object. localStorage is similar to sessionStorage . The only difference is that, while data stored in localStorage has no expiration time, data stored in sessionStorage gets cleared when the browsing session ends—that is, when the browser is closed.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
We want to load all the stylesheets and load the all the contents of the body before running javascript files.
## CSS Questions

* What is the difference between classes and IDs in CSS?
Classes can apply to multiple html tags. Ids are one intance. 
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
Normalize preserves user defaults rather than unstyling them. Normalize corrects some bugs that are out of scope for css reset. 
* Describe Floats and how they work.
A float takes an element and puts it left or right of it's container where other elements will wrap around it. 
* Describe z-index and how stacking context is formed.
It's the stack order of elements on a page.
* Have you ever used a grid system, and if so, what do you prefer?
Bootstrap.
* Have you used or implemented media queries or mobile specific layouts/CSS?
Yes
* How do you optimize your webpages for print?
Create a separate CSS file specifically designed for printing. Use high resolution pictures
* What are the advantages/disadvantages of using CSS preprocessors?
The main advantage is its better for making your code reusable using includes and its also makes nesting possible. You can also add logic for your CSS. downside is that CSS that the preprocessor output is not dry.
* Describe what you like and dislike about the CSS preprocessors you have used.
I like using SASS, which is the only preprocessor that I have used, I wish that the browser could compile the CSS so that it would not be less dry.
* How would you implement a web design comp that uses non-standard fonts?
You would want to import the fonts.
* Explain how a browser determines what elements match a CSS selector.
A browser determines what elements are a match to a CSS selector by specificity
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
The box model refers to everything on a page being blocks. Each element is a block that has margin, border, padding, and content to dictate position.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
The border box will measure elements including their borders. The content box value will measure only the conent, not the margin or border.
* List as many values for the display property that you can remember.
block, inline-block, inline
* What's the difference between inline and inline-block?
Inline-block can have a height. An inline element only occupys the length of the content.
* What's the difference between a relative, fixed, absolute and statically positioned element?
Fixed: things stay put no matter if scrolling occurs relative: things stay put relative to the entire doc. Good for footers thats dont appear until you scroll to the bottom of the page. absolute:
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
The most recent styles override your previously written styles. This allows us to load in resets or declare layouts that will be generally true on our sites, and modifying them in the instances when they need to be modified.
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
I have used Bootstrap.
* Have you played around with the new CSS Flexbox or Grid specs?
No
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
Retina refers to displays with a higher pixel density. The problem with high res displays is the images built for low res images will show up very small. One way to deal with this is to have multiple two sets of images, one for low res display and some for high res.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
CSS loads before JavaScipt, so your animations are not dependent on your JS loading. CSS is also easier to implement. JS can be quicker than CSS IF you aren't using jQuery. Some animations that you are able to make in JS are impossible in CSS. JS annimations is also more widely supported.


## JS Questions

* Explain event delegation
Event delegation is assigning a parent element a event handler rather than assigning event handlers to each child element.
* Explain how `this` works in JavaScript
'This' is used in classes and functions. Each instance of an object or class will have a this property where its own data and properties are stored. When we create a point object, we can refer to this.x, this.y and different instances can have their own values. In this case 'this' refers to the instance of the point.
* Explain how prototypal inheritance works
Prototypal inheritance is a way of creating objects that contain abstractions of what they are building. For example, if you make a human object - it can have a name, age, location, and family members as properties.
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
Ternary implies "three."

var meal = isPhilly ? 'cheesesteak' : 'burger';

is the same as:

var meal: if(isPhilly) { meal = 'cheesesteak'; } else { meal = 'burger'; }

* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
Null is an empty value that we can set. Undefined is something that the language sets.

var x; x = undefined

If we just write 'var x,' the value is undefined.

* How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
Annonymousfunction that is called right away to keep variables out of the global scope.

A closure is a function that has scope that regers to variables. We can use closures to save the scope of variables and their values at a certain point in time.

Closures can be used to encapsulate a module of code. They wrap up the scope and make it unavailable to code that exists outside the closure.

* What's a typical use case for anonymous functions?
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
function Person(){} is a function named Person. it is not executed yet. var person = Person() This is declaring a variable called person, it will be equal to the return value of the 'Person' function. var person = new Person() is a new instance of a person using a constructor.

* What's the difference between `.call` and `.apply`?
The difference is that apply lets you invoke the function with arguments as an array; call requires the parameters be listed explicitly.

* Explain `Function.prototype.bind`.
Bind creates a new function that will have this set to the first parameter passed to bind()

* What's the difference between feature detection, feature inference, and using the User Agent string?
Feature Detection is to verify if a feature works in a particular browser or not. The feature can be either a CSS property or a Java Script Method.

Feature Inference is to assume that a CSS property/ JS method is available in all the browsers, by verifying it in a single browser. The fact is it can or it cannot be available. For ex. the text( ) function is implemented in Chrome , but it is not implemented in Firefox which will give out an error eventually when used. So we have to be careful.

The User Agent is a software which identifies your operating system, browser and its version. When you a visit a particular webpage, the browser sends a user-agent string to the host, implying that only the content/data related to that particular browser should be displayed.

* Explain AJAX in as much detail as possible.
Ajax is a method of exchanging data with a server, and updating the web page without having to reloading the page.

* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
Hoisting is the act of declaring a variable and then assigning it a value later on in your code. This is useful in creating variables with values that change such as a scoreboard.

Javascript hoists variables declared with var to the top of the function. Variables will be undefined until their value is actually set. Variables with the same name of a var outside a function as inside can interfere with each other surprisingly.

* Describe event bubbling.
Event bubbling is firing an event to a nested element and the having it fire to the parent elements which it is nested.

* What's the difference between an "attribute" and a "property"?
Attributes are in your HTML text document/file, whereas properties are in HTML DOM tree.

* Why is extending built-in JavaScript objects not a good idea?
* What is the difference between `==` and `===`?
0 === '0' returns false 0 == '0' returns true

* Explain the same-origin policy with regards to JavaScript.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What tools and techniques do you use debugging Javascript code?
debugger keyword, chrome dev tools

* What language constructions do you use for iterating over object properties and array items?
Loops

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

## Ruby/Rails
* What are ruby gems?
* What is the difference between a symbol and a string?
* What is the difference between a class method and an instance method?
* What is the difference between local variables, instance variables, and class variables?
* What is a range?
* In ruby, what does attr_accessor do?  
* What is the purpose of environment files under the config folder in Rails? (development, test, production)
* What is the purpose of the application.rb file in Rails?
* How can you define a constant?
* What is the purpose of `yield`?
* How do you store API keys when creating an app?
* How do I send parameters through a url?
* Explain MVC
* What is a `before_action`? When would you use it?
* What do controllers do in rails?
* What is RESTful routing?
* What is a polymorphic association?
* What are params?
* How do I make a migration to add a column in Rails?
* What is CSRF? How does Rails protect an app against this?
* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
* What's are classes in Ruby? What are modules? And what's the difference?

## Testing Questions

* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?
* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

## Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Do you have any pet projects? What kind?
* How do you like your coffee?
