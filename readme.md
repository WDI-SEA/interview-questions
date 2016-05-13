#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
Single page applications.

* What excites or interests you about coding?
I enjoy problem solving. I love the open source community.

* What is a recent technical challenge you experienced and how did you solve it?
Earlier this week I was struggling with modals so I got help from a peer.

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?

* Talk about your preferred development environment.
* Which version control systems are you familiar with?
Github!

* Can you describe your workflow when you create a web page?
First I wireframe, then I set up my basic routes and work on functionality. After I have achieved the desired functionality, I begin to style.

* If you have 5 different stylesheets, how would you best integrate them into the site?

* Can you describe the difference between progressive enhancement and graceful degradation?
no!

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).


* If you could master one technology this year, what would it be?
 C++

* Explain the importance of standards and standards bodies.



## HTML Questions

* What does a `doctype` do?
The doctype is at the top of the HTML page and it declares the page as HTML.

* What's the difference between HTML and XHTML?




* What are `data-` attributes good for?
Data attributes are good for storing information that does not have a visual representation.

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.



* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
When you put CSS links in the head so the page loads the CSS before the rest is loaded. This way the page is styled. 

You put the JS at the end of the body so that the scripts are the last thing loaded on the page. This way the scripts can properly interact with elements on the page. 



## CSS Questions

* What is the difference between classes and IDs in CSS?
Id's only apply to one particular element. Classes can be applied to many elements. #ID .Class

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
Normalize sets defaults like font. Resetting CSS literally resets all styling. 


* Describe Floats and how they work.
Floats affect the layers of elements on a page.

* Describe z-index and how stacking context is formed.


* Have you ever used a grid system, and if so, what do you prefer?
Yes I have and Bootstrap 3.


* Have you used or implemented media queries or mobile specific layouts/CSS?

* How do you optimize your webpages for print?

* What are the advantages/disadvantages of using CSS preprocessors?

  * Describe what you like and dislike about the CSS preprocessors you have used.

* How would you implement a web design comp that uses non-standard fonts?

* Explain how a browser determines what elements match a CSS selector.

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?

* List as many values for the display property that you can remember.
inline, inline-block, flex, block, inline-flex, table, initial, inherit.

* What's the difference between inline and inline-block?
Inline block allows you to set a width and height for each block.

* What's the difference between a relative, fixed, absolute and statically positioned element?

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?

* Have you ever worked with retina graphics? If so, when and what techniques did you use?

* Explain some of the pros and cons for CSS animations versus JavaScript animations.

## JS Questions

* Explain event delegation
* Explain how `this` works in JavaScript

* Explain how prototypal inheritance works
When an object inherits from another object. IE matt.__proto__=human

* Why is it called a Ternary expression, what does the word "Ternary" indicate?
Ternary is a conditional operator. It is the only operator that takes in 3 operands. If the condition is true then the operator returns the value of the 1st expression, if false, operator returns the value of the 2nd expression. 


* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
null-
undefined-
undeclared- Undeclared variables 



  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?
* Explain `Function.prototype.bind`.
* What's the difference between feature detection, feature inference, and using the User Agent string?
* Explain AJAX in as much detail as possible.
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What tools and techniques do you use debugging Javascript code?
* What language constructions do you use for iterating over object properties and array items?

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

foo = '1020'
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
function add(a, b) {
  var ans = a + b
  return ans
}
add(2)(5); // 7

```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");

'goh angasal a m\'i'

```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
"Hello World"

alert(foo + bar);
Bar is not defined
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
foo.length = 2


*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
foo.x = {n: 2}

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
one
three
two



## Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Do you have any pet projects? What kind?
* How do you like your coffee?
