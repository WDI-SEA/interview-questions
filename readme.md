#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?

This week I have been expanding my understanding of rails. Yesterday I focused specifically on active records. Last weekend I started learning D3.js and Three.js.

* What excites or interests you about coding?

The creative element of building a well designed website.

* What is a recent technical challenge you experienced and how did you solve it?

A recent challenge technical challenge that I had was styling an erb element in rails. I solved it by googling "how to add a class on an erb tag" and found a stack overflow post.

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?

UI - UX based decisions for user flow. Are my photos high quality or pixelated? Is the page responsive?

Performance - How many files are in my HTML, if they are plugins - are they minified files? Is my JS file located at the bottom of the page? How large are my site images and have I compressed them?

Maintainability -Is my CSS or SASS as dry as possible? Is it easy to read and well documented with comments? Is my code reusable?

* Talk about your preferred development environment.


* Which version control systems are you familiar with?

Git


* Can you describe your workflow when you create a web page?

 - Basic HTML structure
 - Minimal CSS styles
 - Work on the more technical aspects of the modules functionaility.
 - Repeat the last three steps for other parts modules on the page.
 - Complete and fine tune CSS styles.


* If you have 5 different stylesheets, how would you best integrate them into the site?

- reset
- base styles - if there is a company style guide, those styles would go here
- layout - for example, default height of a section or padding between sections
- module styles specific styles to get the page looking as I want it to look
- state styles  - what does a link look like what its being hovered over, after its been visited, etc...


* Can you describe the difference between progressive enhancement and graceful degradation?

Progressive enhancement is using the newest technologies as they are released.

Graceful degradation is making sure that the technologies that you are using are compatible with older browsers so that the page is more accessible.

Ideally you want to strike a balance between the two and make sure that if you are using a new technology that has limited support -  you want to have a fallback for older browsers.

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).


* If you could master one technology this year, what would it be?

React.js

* Explain the importance of standards and standards bodies.

## HTML Questions

* What does a `doctype` do?
DOCTYPE tells the browser which version of HTML you are using.

* What's the difference between HTML and XHTML?
XHTML follows conventions of XML and is more strict.
* What are `data-` attributes good for?
Stores data that doesn't have any visual representation.
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
Cookie is older tech can only store strings, session storage ends when you close your browser, local storage persists.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

It is good to put your JS file at the bottom of your body so that your page is not waiting to for the JS file to load to show the page. Its also good to store the CSS files at the top of the page so that the user sees colors load on the page quicker rather than having a longer wait to see anything load.

## CSS Questions

* What is the difference between classes and IDs in CSS?

Classes target multiple items, Id's target one. Since Id's are more specific, they override class styles.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

Normalize preserves user defaults rather than unstyling them.
Normalize corrects some bugs that are out of scope for css reset.
For these reasons, I would choose normalize.

* Describe Floats and how they work.
Floats are ways to style different elements to different positions on your webpage.
For example, if you have two paragraphs and you want them next to each other, you would float on left, and the other one right.

Floating elements don't have a height.Use clear to get things below the floats.

* Describe z-index and how stacking context is formed.

Z index determines the layer of elements. An element with a higher z index is layered over an element with a lower z index.

* Have you ever used a grid system, and if so, what do you prefer?

I have used both Bootstrap's grid and skeleton. I prefer bootstrap.

* Have you used or implemented media queries or mobile specific layouts/CSS?

I have implemented media queries and mobile layouts.

* How do you optimize your webpages for print?
Create a separate CSS file specifically designed for printing. Use high resolution pictures, at least 300 dpi.

* What are the advantages/disadvantages of using CSS preprocessors?

 The main advantage is its better for making your code reusable using includes and its also makes nesting possible. You can also add logic for your CSS.

 - One downside is that CSS that the preprocessor output is not dry.
 - Harder to debug.
 - Adds some steps in the workflow.

* Describe what you like and dislike about the CSS preprocessors you have used.

I like using SASS, which is the only preprocessor that I have used, I wish that the browser could compile the CSS so that it would not be less dry.


* How would you implement a web design comp that uses non-standard fonts?

You would want to import the fonts.

* Explain how a browser determines what elements match a CSS selector.

A browser determines what elements are a match to a CSS selector by specificity.
Ordered least to most specific:
 - element tags
 - classes
 - id's
 - inline styles

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

The box model refers to everything on a page being blocks. Each element is a block that has margin, border, padding, and content to dictate position.

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
Browsers can measure the width and height of elems in different ways. Each browser interprets box sizing differently. Specifying a specific border box allows us to know how things are measured.

The border box will measure elements including their borders. The content box value will measure only the conent, not the margin or border.

* List as many values for the display property that you can remember.

block, inline-block, inline

* What's the difference between inline and inline-block?

Inline-block can have a height. An inline element only occupys the length of the content.

* What's the difference between a relative, fixed, absolute and statically positioned element?

Fixed: things stay put no matter if scrolling occurs
relative: things stay put relative to the entire doc. Good for footers thats dont appear until you scroll to the bottom of the page.
absolute:


* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?

The most recent styles override your previously written styles. This allows us to load in resets or declare layouts that will be generally true on our sites, and modifying them in the instances when they need to be modified.

* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?

I have used bootstrap and skeleton.


* Have you played around with the new CSS Flexbox or Grid specs?

Not yet.

* Have you ever worked with retina graphics? If so, when and what techniques did you use?

Retina refers to displays with a higher pixel density. The problem with high res displays is the images built for low res images will show up very small. One way to deal with this is to have multiple two sets of images, one for low res display and some for high res.

* Explain some of the pros and cons for CSS animations versus JavaScript animations.

CSS loads before JavaScipt, so your animations are not dependent on your JS loading.
CSS is also easier to implement.
JS can be quicker than CSS IF you aren't using jQuery.
Some animations that you are able to make in JS are impossible in CSS.
JS annimations is also more widely supported.

## JS Questions

* Explain event delegation
Event delegation is assigning a parent element a event handler rather than assigning event handlers to each child element.

* Explain how `this` works in JavaScript


* Explain how prototypal inheritance works
Prototypal inheritance is a way of creating objects that contain abstractions of what they are building. For example, if you make a human object - it can have a name, age, location, and family members as properties.

* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?

A null varible is a variable without a value.
An undefined variable is a variable that has not been created. An undeclared variable is a variable that has not been declared with the keyword var.

* How would you go about checking for any of these states?

* What is a closure, and how/why would you use one?

* What's a typical use case for anonymous functions?
A typical use for an anonymous function is to keep your variables out of the gloabal scope.

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

function Person(){} is a function named Person
var person = Person() is a function inside a variable named person.
var person = new Person() is a new instance of a person using an constructor.

* What's the difference between `.call` and `.apply`?

* Explain `Function.prototype.bind`.

* What's the difference between feature detection, feature inference, and using the User Agent string?

* Explain AJAX in as much detail as possible.

Ajax is a method of exchanging data with a server, and updating the web page without having to reloading the page.

* Have you ever used JavaScript templating?
No.

* If so, what libraries have you used?

* Explain "hoisting".

Hoisting is the act of declaring a variable and then assigning it a value later on in your code. This is useful in creating variables with values that change such as a scoreboard.

* Describe event bubbling.

Event bubbling is firing an event to a nested element and the having it fire to the parent elements which it is nested.

* What's the difference between an "attribute" and a "property"?


* Why is extending built-in JavaScript objects not a good idea?

* What is the difference between `==` and `===`?
  == is less strict than ===, === compares what type of value it is.

* Explain the same-origin policy with regards to JavaScript.

* What is the extent of your experience with Promises and/or their polyfills?

* What are the pros and cons of using Promises instead of callbacks?

Promises prevent callbacks being nested in other callbacks, and can make the code more readable.

* What tools and techniques do you use debugging Javascript code?

I console.log my console.log's with more console.log's. Also setting breakpoints in your code and stepping through it.

* What language constructions do you use for iterating over object properties and array items?

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

## Ruby/Rails
* What are ruby gems?
A ruby file designed to easily manage the installation.
* What is the difference between a symbol and a string?
A symbol cannot be changed vs strings which can be changed at any time.
* What is the difference between a class method and an instance method?
A class is a description of a thing. An instance is an actual thing.
* What is the difference between local variables, instance variables, and class variables?
* What is a range?
Range is the all of the numbers between two numbers. You can also use these for letters.
* In ruby, what does attr_accessor do?

* What is the purpose of environment files under the config folder in Rails? (development, test, production)
* What is the purpose of the application.rb file in Rails?
* How can you define a constant?
* What is the purpose of `yield`?
* How do you store API keys when creating an app?
In an .env file to hide it from view
* How do I send parameters through a url?
* Explain MVC
Model View Controller
* What is a `before_action`? When would you use it?
before_action is a hook that you can use to run some code before you do another block of code.
* What do controllers do in rails?
In rails, controllers store your methods.
* What is RESTful routing?
Using GET,PUT, POST, DELETE to serve pages.
* What is a polymorphic association?
An association that can change between being a 1 to 1 and many to one association.
* What are params?
params are parameters that can be passed in from the front end from the user to be stored in the backend.
* How do I make a migration to add a column in Rails?
* What is CSRF? How does Rails protect an app against this?
* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
User.find_by_id grabs a specific user and User.find grabs the first of a description.
* What's are classes in Ruby? What are modules? And what's the difference?

## Testing Questions

* What are some advantages/disadvantages to testing your code?
Advantage - catching bugs right away before they become an issue.
Disadvantage - The tests are only as good as the programmer writing them.

* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?
* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

foo = 30

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
"goh angasal a m'i"

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
"Hello World"
Undeclared variable


*Question: What is the value of `foo.length`?*
```javascript
var foo = []; => null
foo.push(1); => 1
foo.push(2); => 2
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
'one' 'three'

## Fun Questions:

* What's a cool project that you've recently worked on?

D3 graphs plotting total snow fall in different regions over the last decade.

* What are some things you like about the developer tools you use?

* Do you have any pet projects? What kind?

Currently developing a site for my friend who is a photographer.

* How do you like your coffee?

Chemex && light half and half && light sugar || nitro cold brew black || machiatto && light sugar. Hold the script please.
