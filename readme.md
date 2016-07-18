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

I like to work with node over rails because I don't like the "magic" of rails. I like to know why what I am doing is working.

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

use css animations for transitions using opacity to show and hide elements.
keep an array with all of the image urls.

attach a click handler to the image so users can click on it and go to the next one. Also, we can set up an interval with JavaScript to automatically transition through the pictures.

make some divs with prev and next text


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

'This' is used in classes and functions. Each instance of an object or class will have a this property where its own data and properties are stored.
When we create a point object, we can refer to this.x, this.y and different instances can have their own values. In this case 'this' refers to the instance of the point.

* Explain how prototypal inheritance works

Prototypal inheritance is when an object inherits from another object.

This is used to create abstractions of what is being built. For example, you can create an animal object which you can use to build a dog object, which you can use to build a specific instance of a dog.

* Why is it called a Ternary expression, what does the word "Ternary" indicate?

Ternary implies "three."

var meal = isPhilly ? 'cheesesteak' : 'burger';

is the same as:

var meal:
if(isPhilly) {
  meal = 'cheesesteak';
} else {
  meal = 'burger';
}

* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?

Null is an empty value that we can set.
Undefined is something that the language sets.

var x;
x = undefined

If we just write 'var x,' the value is undefined.

* How would you go about checking for any of these states?

* What is a closure, and how/why would you use one?

Annonymousfunction that is called right away to keep variables out of the global scope.

A closure is a function that has scope that regers to variables. We can use closures to save the scope of variables and their values at a certain point in time.

Closures can be used to encapsulate a module of code. They wrap up the scope and make it unavailable to code that exists outside the closure.


* What's a typical use case for anonymous functions?

- for creating click handlers
- for creating closures
- keep your variables out of the gloabal scope.

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

function Person(){} is a function named Person. it is not executed yet.
var person = Person() This is declaring a variable called person, it will be equal to the return value of the 'Person' function.
var person = new Person() is a new instance of a person using a constructor.

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
Yes

* If so, what libraries have you used?
EJS and ERB

* Explain "hoisting".

Hoisting is the act of declaring a variable and then assigning it a value later on in your code. This is useful in creating variables with values that change such as a scoreboard.


Javascript hoists variables declared with var to the top of the function. Variables will be undefined until their value is actually set. Variables with the same name of a var outside a function as inside can interfere with each other surprisingly.

* Describe event bubbling.

Event bubbling is firing an event to a nested element and the having it fire to the parent elements which it is nested.

* What's the difference between an "attribute" and a "property"?

Attributes are in your HTML text document/file, whereas properties are in HTML DOM tree.


* Why is extending built-in JavaScript objects not a good idea?
Lack of specification
Host objects have no rules
Chance of collisions
Performance overhead


* What is the difference between `==` and `===`?
  == is less strict than ===, === compares what type of value it is.

  0 === '0' returns false
  0 == '0' returns true

* Explain the same-origin policy with regards to JavaScript.
This is a security policy that  prevents JS from accessing sites outside the current domain.

* What is the extent of your experience with Promises and/or their polyfills?

* What are the pros and cons of using Promises instead of callbacks?
Promises prevent callbacks being nested in other callbacks, and can make the code more readable.

* What tools and techniques do you use debugging Javascript code?
I console.log my console.log's with more console.log's. Also setting breakpoints in your code and stepping through it via Chrome dev tools.

Debugger keyword.

* What language constructions do you use for iterating over object properties and array items?

loops!
- for
- for each
- while
- do while
- .map, .filter, .reduce, .forEach

For in loops are good for iterating over the properties in an object and accessing their key.

for loops are good for arrays. For in loops with arrays include the length property and cause problems.

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

User
id
friends - many to many
posts - many to one
wall
likes - many to one

Wall
id
user id
posts

Apps
id
user id

fan pages
id
posts
likes
posts







## Ruby/Rails
* What are ruby gems?
A ruby file designed to easily manage the installation.

Its a module you can add in the can be used for additional functionality. For example you can have a gem that provides a library with functions for OAuth.

SASS is a css preprocessor gem. There are many OAuth gems, voting gems, etc.

Carrierwave is good for uploading files.

* What is the difference between a symbol and a string?

We use symbols in hash maps. Symbols all reference one single value, there may be many instances of strings.
A symbol cannot be changed vs strings which can be changed at any time.

* What is the difference between a class method and an instance method?
A class method exists once for all instances of a class. An instance methods acts on instances individually.
A class is a description of a thing. An instance is an actual thing.

* What is the difference between local variables, instance variables, and class variables?
instance variable: a variable that has an idependant value that pertains to this instance of a class.
local variable: typically used in a method, and has only local scope, not associated with any classes.

class variable: Class variables are shared among all instances of a class. Each instance of the class can read the same value.

* What is a range?
Range is the all of the numbers between two numbers. You can also use these for letters.

* In ruby, what does attr_accessor do?
attr_accessor is used to define an attribute for object of Model which is not mapped with any column in database.

* What is the purpose of environment files under the config folder in Rails? (development, test, production)
development is meant for the configuration of rails while it is being creates,
test is meant for the configuration while it is being tested before being launched,
production is for the configuration of the code that will go live.

* What is the purpose of the application.rb file in Rails?
Application.rb configures settings for your whole rails app.

* How can you define a constant?
in the application module

* What is the purpose of `yield`?

  We use the yield keyword when we create our layout template.
  The rest of our site will dill in wherever we put the yield keyword.

  <body>
    <% yield :nav %>
    <% yield %>
  </body>



* How do you store API keys when creating an app?
In an .env file to hide it from view

* How do I send parameters through a url?

* Explain MVC

MVC stands for Model View Controller. Model handles the data, View is what is shown to the user, and controller handles the interaction and flow of the data to the view or model.

* What is a `before_action`? When would you use it?
before_action is a hook that you can use to run some code before you do another block of code.

* What do controllers do in rails?
In rails we have views that define pages in our app, we have models that define how our data exists in the database and in the app.

We can pair controllers with CRUD methods to control how our models are Created, read, updated, and destroyed.

In rails, controllers store your methods.

* What is RESTful routing?

Representational
State
Transer

Using GET,PUT, POST, DELETE to serve pages rather than relying only on different URLs.

Restful routing is a standard convention that serves as a guide for us to create our CRUD routes.

GET - Gets info about something
POST - creates info about something
PUTS - Updates info about something
DELETE - Deletes something

* What is a polymorphic association?
An association that can change between being a 1 to 1 and many to one association.

* What are params?
params are parameters that can be passed in from the front end from the user to be stored in the backend.

* How do I make a migration to add a column in Rails?
db:migrate

* What is CSRF? How does Rails protect an app against this?
CSRF stands for Cross-site request forgery. It is a technique hackers use to hack into a web application.
In order to prevent such things from happening Rails uses authenticity_token.

* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
User.find_by_id grabs a specific user and User.find grabs the first of a description.

If the id of the user doesn't matter, then the database can return us any old match much more quickly.

* What's are classes in Ruby? What are modules? And what's the difference?
Modules are self contained pieces of code that you're able to export and import into other places.

## Testing Questions

* What are some advantages/disadvantages to testing your code?
Advantage - catching bugs right away before they become an issue.
Disadvantage - Tedious, not fun, might fall into the trap of writing code that just passes the test but doesn't have the correct functionality. The tests are only as good as the programmer writing them. Sometimes its hard to write a test when the code youre trying to test has many dependencies and is tightly coupled to other parts of the application. For example, how to test someone scrolling down a site and clicking a delete button in the middle of a long list?

* What tools would you use to test your code's functionality?

You can assign someone to manually test the site. Manual testing is expensive and tedious but its necessary.

in QA, testing testers create test plans to test different portions of an app. Someone is given a very loose set of instructions to follow.

Eventually, manual tests are converted into automated tests.


Unit tests test small parts of code like calling a method and checking a return value.

There are also great tools that allow us to script user interactions like typing things into a form, clicking buttons, navigating to pages.

PhantomJs, Selenium, Angular has built in libraries.
Mocha / Chai, Jasmine

* What is the difference between a unit test and a functional/integration test?
Functional Testing - Is carried out without any knowledge of the internal working of the system.The tester will try to use the system by just following requirements, by providing different inputs and testing the generated outputs.

Unit Testing - As the name suggests, this method tests at the object level. Individual software components are tested for any errors. Knowledge of the program is needed for this test and the test codes are created to check if the software behaves as it is intended to.

* What is the purpose of a code style linting tool?
Linting is the process of running a program that will analyse code for potential stylistic errors. A linter is a nice tool to have to enforce consistent coding patterns througout an app.

- improper indentation
- inconsisten snake_case vs camelCase
- consistent single or double quote usage
- non-matching brackets, quotes, curly braces
- long lines past 80 or 100 characters

teams can config linters to detect any stylistic conventions they care about.

code repos can prevent code from being commited until they pass a linter.

* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

End to end testing refers to testing everything from the client end to the server end. Angular provides its own end to end framework.

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
