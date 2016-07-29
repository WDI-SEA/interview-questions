#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?

OAuth using facebook

* What excites or interests you about coding?

Learning of new technologies and being able to solve problems

* What is a recent technical challenge you experienced and how did you solve it?

In creating a spa app, I had to be able to be able to handle multiple forms. I had to hide them in modals and use jQuery to only get what I want.

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?

I think about user password encryption, but not much else.

* Talk about your preferred development environment.

I really liked Node.js and express for ease of debugging. Rails is not easy to debug, but quick to use.

* Which version control systems are you familiar with?

git/github, source depot, team foundation server

* Can you describe your workflow when you create a web page?

Specs are important. I need to decide what is the MVP.
Modeling the database interactions for me is next.
Wireframing to decide what views are needed.
Create the skeleton of Models, Migrations, Routes, and views.
Test my routes.
Create forms for POST and PUT actions, display info in GET views.
Get my views fixed.
Deploy and bug fix.

* If you have 5 different stylesheets, how would you best integrate them into the site?

If they're not my stylesheet, I would put them in loading order in the HTML head.
My stylesheets would be below and would only be used to tweak to what I need.

* Can you describe the difference between progressive enhancement and graceful degradation?

Nope.

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).

If I can't use an external library, I'd have an image tag and two buttons.
The buttons would trigger js functions that would change the src of the image tag.
CSS to make sure each image will fit okay.

* If you could master one technology this year, what would it be?

I wanna know how to use d3js. I think it would look nice in a spa app.

* Explain the importance of standards and standards bodies.

Nope.


## HTML Questions

* What does a `doctype` do?

It informs the browsers what kind of data they're about to recieve.

* What's the difference between HTML and XHTML?

XHTML is a stricter version of HTML

* What are `data-` attributes good for?

Stores data in elements that isn't displayed visually

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.

sessionStorage is information saved in the server side for a specific time.
localStorage is information saved on a client's server.
cookie is a client side data. It's much smaller than localStorage and is considered an old way.

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

Putting css styles in the head means it is loaded before the html elements are drawn by the browser. This means things are loaded sooner in the browser. Exceptions are when you need to style specific elements completely differently (still not recommended) or when you want to control the load order so something comes up much sooner (only for really slow clients).

## CSS Questions

* What is the difference between classes and IDs in CSS?
Both are identifiers for elements that live in the html. In CSS, IDs are considered more specific (usually only one element) and styles applied to elements via class are usually overwritten by styles applied to elements via ID. The exception being the use of the !important option in css.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

Browsers have user-agent defined prebuilt css styles that it applies to websites. Resetting tries to remove all of the prebuilt styles so developers have more control over them. Normalizing makes it so prebuilt styles look the same across browsers.

* Describe Floats and how they work.

Floats are numbers. Specifically, they have a value and a magnitude field so you can represent big numbers (like 5x10^30) or small numbers (like 0.0001).

* Describe z-index and how stacking context is formed.

Nope.

* Have you ever used a grid system, and if so, what do you prefer?

The only one I've worked with is Bootstrap. I don't like all of the prebuilt styles, so I will look for better ones.

* Have you used or implemented media queries or mobile specific layouts/CSS?

Yes, it was on our pre-interview assignment. Bootstrap technically does it, too.

* How do you optimize your webpages for print?

Nope.

* What are the advantages/disadvantages of using CSS preprocessors?

Preprocessors allow for more complex control of styles by allowing formulas and variables built in.

* Describe what you like and dislike about the CSS preprocessors you have used.

I haven't used one, so I have not formed opinions on them.

* How would you implement a web design comp that uses non-standard fonts?

You have to import a stylesheet link (like css) in the head of HTML document and call it directly with css font-family style.

* Explain how a browser determines what elements match a CSS selector.

Styles are applied in a "cascading" way, meaning the broader selections are applied first then more specific selections are applied over it. Tag type(e.g. p-tag, div-tag, image-tag) is applied first, then classes, then IDs.

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

All elements are rendered in boxes. Boxes have a height, width, content, padding (space between content and border), border, and margin (space between elements).

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?

The css command makes browsers render element heights and widths than include the padding and border. It's useful for sizing elements when you need a big border.

* List as many values for the display property that you can remember.
inline, inline-block, block, none, flex

* What's the difference between inline and inline-block?

Inline doesn't really use the block model. It puts content next to each other. Inline block, you can still specify height and width regardless of the content.

* What's the difference between a relative, fixed, absolute and statically positioned element?

Static elements are positioned based on their display property and load order in the html. Relative positioning would move it from the static positioning based on a position property (e.g. left: 10px). Absolute puts the element exactly where you specify on a page. Fixed is the same, but not where on the page, but rather the viewport.

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?

Tag-type to element-class to element-id, also parent to child. This is useful for applying styles to a lot of common elements, but fine tuning things for particular elements.

* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?

Does bootstrap count? I know there are versions of it out there with less specific styles. I like the grid, but sticking to their styles makes my site look like a lot of other people's.

* Have you played around with the new CSS Flexbox or Grid specs?

I have used Flexbox. It's not a responsive as one would expect.

* Have you ever worked with retina graphics? If so, when and what techniques did you use?

Nope, I have not.

* Explain some of the pros and cons for CSS animations versus JavaScript animations.

CSS animations are quicker than redrawing elements with JS. Control is better with JS, though.

## JS Questions

* Explain event delegation

Nope.

* Explain how `this` works in JavaScript

Javascript instance variables need the 'this' to be bound to an instance of a class/constructor.

* Explain how prototypal inheritance works

Constructor's instances have multiple copies of the same thing. For variables, it's perfect, but for functions, the same code being repeated is cumbersome and unneccesary. Attaching it to the prototype means the constructor's instances will all have access to that code and so will constructor's sub classes.

* Why is it called a Ternary expression, what does the word "Ternary" indicate?

A ternary expression is called that because it takes three values (condition, case1 and case2).

* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?

Null means there is no value. Usually this means it was removed. Undefined means a value was not set. Undeclared means the pointer or name wasn't even set.

* How would you go about checking for any of these states?

If you check for the value, it should return that state. If it's not in that state, it will return some sort of Primitive value.

* What is a closure, and how/why would you use one?

Putting code inside of an anonymous function is a closure. It lets the scope of the variables stay within the closure making it more private and not able to collide with other variables for namespace.

* What's a typical use case for anonymous functions?

Anonymous functions can be used as closures or as a variable for a callback function that you want to pass parameters to. If you try to pass parameters to a named function, the parenthesis will call the function right away.

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

1st - declaration of a function named Person
2nd - declaration of a variable with the value of the return of the function Person()
3rd - new instance of the class based on the constructor Person()

* What's the difference between `.call` and `.apply`?

Nope.

* Explain `Function.prototype.bind`.

Nope.

* What's the difference between feature detection, feature inference, and using the User Agent string?

Nope.

* Explain AJAX in as much detail as possible.

AJAX is a jQuery function that can make HTTP requests from within the front-end.

* Have you ever used JavaScript templating?
  * If so, what libraries have you used?

 No.

* Explain "hoisting".

Nope.

* Describe event bubbling.

Async functions produce events/results that have to be passed to the next function in order to decide what to do. Because Async functions are often anonymous or scoped, it's important to create a path for the events rather than just 'return' the result.

* What's the difference between an "attribute" and a "property"?

Nope.

* Why is extending built-in JavaScript objects not a good idea?

It could mess with other people's code and it's easy enough to create your own constructors.

* What is the difference between `==` and `===`?

One checks if the values are the same (e.g. 2 == '2') and the other checks that both are even of the same type (2 === 2 but 2 != '2').

* Explain the same-origin policy with regards to JavaScript.

Nope.

* What is the extent of your experience with Promises and/or their polyfills?

Dunno what polyfills are.

* What are the pros and cons of using Promises instead of callbacks?

Promises will run based on what result you get from an async function. Callbacks will run when called. Both are able to do the same thing, but promises are easier to use when you know what you're expecting and callbacks are useful for getting out multiple async functions.

* What tools and techniques do you use debugging Javascript code?

repl to check quick functions, Chrome console, console.log, and breakpoints when necessary.

* What language constructions do you use for iterating over object properties and array items?

for loops, for in loops, for each loops?

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

User(ID),friends list(M:M to other users), photos(1:M), email
Photo(ID), timestamps, tags list(M:M to users)
Posts(ID), comments (1:M or polymorphic)
Comments, users (1:1)


## Ruby/Rails
* What are ruby gems?

Packets of code published by rubygems.org. The packages also contain info of dependencies to other code packages.

* What is the difference between a symbol and a string?

A string is a set of characters. A symbol is a named pointer to a particular spot of memory.

* What is the difference between a class method and an instance method?

A class method is shared by all instances of that class. An instance method is for that instance only. Some methods can be both through inheritance.

* What is the difference between local variables, instance variables, and class variables?

Nope.

* What is a range?

It's a ruby primary that has a start and an end.

* In ruby, what does attr_accessor do?

It allows instance variables to be directly writable or readable.

* What is the purpose of environment files under the config folder in Rails? (development, test, production)

It sets up the configuration for your app when it's being developed, being tested, or deployed.

* What is the purpose of the application.rb file in Rails?

Nope.

* How can you define a constant?

Variables set with a name that's all caps are immutable and constant in ruby.

* What is the purpose of `yield`?

Nope.

* How do you store API keys when creating an app?

Store them in a private .env file.

* How do I send parameters through a url?

Attach it to the :params symbol.

* Explain MVC
* What is a `before_action`? When would you use it?

It's a hook/middleware used 

* What do controllers do in rails?

They're what controls the actions in the back end and what the response will be.

* What is RESTful routing?



* What is a polymorphic association?

It's an data relation table that holds the same data for whatever it's related to, but it can be related to different things.

* What are params?

parameters to a request

* How do I make a migration to add a column in Rails?

I would undo a migration, edit it or recreate it with rails generator, then re-migrate.

* What is CSRF? How does Rails protect an app against this?



* What's the difference between `User.find_by_id(1)` and `User.find(1)`?

The first one finds a specific user by ID of 1. The other one finds the first user it can find, but no guarantee that it'll be the User of ID 1.

* What's are classes in Ruby? What are modules? And what's the difference?

## Testing Questions

* What are some advantages/disadvantages to testing your code?

It slows development, but you have a better, more robust product.

* What tools would you use to test your code's functionality?

Assert, Mocha/Chai

* What is the difference between a unit test and a functional/integration test?

A unit test can be applied to a specific feature or part while a functional/integration test tests how the features interact or possibly conflict.

* What is the purpose of a code style linting tool?



* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
'1020'

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

function add(num1, num2){
	if num2 === undefined {num2 = 0};

	return function(num1, num2){(num1 + num2)};
}

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

goh angasal a m'i

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

the first is an error, (foo not defined in the scope?), the second is an error (bar is not defined at all).

*Question: What is the value of `foo.length`?*
```javascript
var foo = []; // 0
foo.push(1); // 1
foo.push(2); // 2
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2}; // {n: 2}
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

onetwothree

## Fun Questions:

* What's a cool project that you've recently worked on?

SPA

* What are some things you like about the developer tools you use?

Chrome can show you the actual element and play with it.

* Do you have any pet projects? What kind?

Nope.

* How do you like your coffee?

With soy milk or not at all.