#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

What did you learn yesterday/this week?
Today my group focused git workflow and managing conflicts from multiple sources. // Angular Authentication, Routing, and many other things Angular!

What excites or interests you about coding?
I enjoy the problem solving and being able to always learn new languages and technologies, so there’s always something new and exciting to learn.

What is a recent technical challenge you experienced and how did you solve it?
The most recent technical challenge I experienced was more of a UX one: how to display images for users to select from in a way that’s appealing. I’m still working through diff Bootstrap layouts and regular CSS that’s responsive.

What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
I use bcrypt, in Ruby limit ability to view pages, use closures, etc.

Talk about your preferred development environment.
Git on my laptop with some Sublime Text.

Which version control systems are you familiar with?
Git

Can you describe your workflow when you create a web page?
I start by discussing MVP, expected databases (users, passwords, word content, etc) then generally ask for layout feelings before mocking up and then begin coding, trying to keep in contact with the client throughout.

If you have 5 different stylesheets, how would you best integrate them into the site?
Depends on the site. If it was a Ruby site, I’d use the different assets stylesheets on different controllers. If it were Node, I’d included it depending on the page, probably in partials.

Can you describe the difference between progressive enhancement and graceful degradation?
Progressive enhancement starts from a low level MVP and then build up to a better product depending on what environment you work with. Graceful degradation is building a great product first but also allowing some basic functionality on other browsers (IE).

Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
I’d use the Dom and pull in an API or do some data scraping to find images, then iterate over them in a loop triggered by an AJAX button

If you could master one technology this year, what would it be?
If it was infinitely possible to memorize anything, I’d be interested in learning about machine learning/AI.

Explain the importance of standards and standards bodies.
They establish a communal expectation around how webpages and software is created.

## HTML Questions

What does a `doctype` do?
Doctype establishes the language a file’s written in, used mainly for web pages.

What's the difference between HTML and XHTML?
XHTML is more standard and allows for mobile or other browsers to run code more easily. Many standards are mandatory including DOCTYPE etc.

What are `data-` attributes good for?
Storing information that’s needed in a web pages when there’s no visual representation on the page.

Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
Local storage stores until a user deletes them. Session lasts for logins or authentications/ends when you close your browser. Cookies store less information and are good for older browsers, can only store strings, and are sent to the server.

Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
Load order: CSS is loaded at the beginning of the page before content. Scripts pause the loading of content, and can't apply click handlers when elements haven't been loaded. Document onload. 
https://developers.google.com/speed/docs/best-practices/rtt#PutStylesBeforeScripts

## CSS Questions

What is the difference between classes and IDs in CSS?
Ids are unique and only one element can have one on each page. Classes can be used on multiple elements, and multiple on the same.Ids are stored on the user end, whereas classes are serverside.

What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
Resetting removes browser styling whereas normalizing creates consistency across all browsers. It depends on the project. 
http://stackoverflow.com/questions/6887336/what-is-the-difference-between-normalize-css-and-reset-css

Describe Floats and how they work.
Floats pull elements left, center, or to the side and are also clearable. It pulls elements in that particular direction and lets other elements warp around it. //FLOATS don't have a height.

Describe z-index and how stacking context is formed.
z-index is used to stack elements on the page along a z axis that’s related to the user standpoint, so it lets us specify if images lay over divs for example. Higher z-index appears on top of lower z-index.
https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context

Have you ever used a grid system, and if so, what do you prefer?
I’m familiar with bootstrap and have worked with Formation, which I enjoyed a lot. I’ve looked into Skeleton too.

Have you used or implemented media queries or mobile specific layouts/CSS?
I have, with my Project The Artr and another project Flowered Significance, where I still need to troubleshoot a particular library’s display on mobile. min-width and max-width.

How do you optimize your webpages for print?
Separate CSS file designate the media type. High resolution files. 

What are the advantages/disadvantages of using CSS preprocessors?
It’s good for big and complex webpages. //SEE STEVE'S A 
+: Allow fancier syntax. Exceptional amoutn of files. Add variables. Nested query syntax.
-: Harder to debug, compiled code isn't ours, extra step to workflow, whole team has to know it

Describe what you like and dislike about the CSS preprocessors you have used.
I like Sass for it’s ability to make my stylesheets more modular.

How would you implement a web design comp that uses non-standard fonts?
The most common non-standard fonts I’ve used are Google fonts, and I pull them in in the head.

Explain how a browser determines what elements match a CSS selector.
They read through the HTML from left to right for matches.
Selectors are ids, classes, and tags.
https://programmerinnervoice.wordpress.com/2013/12/18/how-does-browser-read-css-selector/

Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
The box model is the padding, margin, border that surround each element. The display property allows us to set elements to be block, inline-block, inline, flex. 

What does ```* { box-sizing: border-box; }``` do? What are its advantages?
It includes borders in an element’s size. It allows you to add borders and styling without worrying if those things will upset the layout of your page.

List as many values for the display property that you can remember 
inline (inline together, no heigth by line height), inline-block (includes a height and a break between elements, still side by side), flex, inline-table, inline-flex, run-in, list-item, table, inherit, intial, none, grid etc
 
What's the difference between inline and inline-block?
Inline: display element the way a span would aka without moving to a new line. Inline block moves things to the next line.

What's the difference between a relative, fixed, absolute and statically positioned element?
Defines how elements are positioned on the page.
Relative allows elements to be positioned relative to where they'd appear normally.
Fixed keeps things in place even when scrolling. 
Absolute: stay put relative to entire document.
and statically positioned.

The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
Type selector (i e p), class selector, ID selector. You can assign by specificity, only using IDs for edge cases.

What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
I’ve used Bootstrap, which awesomely includes a lot of built in styles that are sadly overused. That’s part of the appeal of Formation: same grid and similar built ins, but more ability to choose which animations are included. 

Have you played around with the new CSS Flexbox or Grid specs?
I have! Froggy Flex.

Have you ever worked with retina graphics? If so, when and what techniques did you use?
I have not, but I’d be interested in learning more. Extremely high pixel density. You can have two sets of images, one for low and one for high density displays.
http://www.sitepoint.com/css-techniques-for-retina-displays/

Explain some of the pros and cons for CSS animations versus JavaScript animations.
I enjoy CSS animations - they’re more controllable on the front end side of things. CSS is dealt with by the GPU. Simple = CSS. Intricate/specific = Javascript.
https://css-tricks.com/myth-busting-css-animations-vs-javascript/


## JS Questions

Explain event delegation
Takes advantage of event bubbling and targeting elements to allow events to bubble to the top of the DOM. Allows you to determine where an Event came from.

Explain how `this` works in JavaScript
The ‘this’ keyword is useful for when manipulating a particular element with the dom, and can be used much in the way “me” or “my” is used. It's self referential. Binds itself to the current scope your content exists in. Each instance of object or class will have a 'this' property where its own data and properties are stored. Has different contexts.

When we create a Point object we can refer to
this.x
this.y
and different instance of the point can have their own values. In this case, 'this' refers to the instance of the Point.

Explain how prototypal inheritance works
A prototype object is created that allows newly created objects to inherit a set of methods or properties from that original prototype.

Why is it called a Ternary expression, what does the word "Ternary" indicate?
It takes three properties and tests them, returning either the first or second (separated by : ) depending on whether that test is true or false.

What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
Undeclared: doesn’t use var. 
Undefined: has been created but has no set value.
Null: a variable with no set value, comes from programmers.

How would you go about checking for any of these states?
//RETURN

What is a closure, and how/why would you use one?
//STEVE'S A: A function that has scope that refers to variables.

An anonymous function you call right away which helps keep your namespaces clean. Closures are used to restrict some data accessibility when working in different functions. They’re useful in keeping a particular variable isolated from the rest of the document. I’d use them to make sure that I could return only the data I wanted to.

Closures can be used to encapsulate a module of code.
They wrap up the scope and make it unavailable to code that exists outside the closure.

What's a typical use case for anonymous functions?
They’re commonly used for callback functions, closures, click handlers, setting time outs, and writing code that won't be invoked from many places.

Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
The way the function is substantiated and allow for being called differently thanks to hoisting. 

function(){} defines a function called Person. It's not executed yet.

var person = Person() is an instance of a person with a capital. Equal to the return of the 'Person' function.

The last is a constructor. Makes an object rather than a string.

What's the difference between var foo = function(){} and function foo(){}?
These are both function definitions. function foo() is callable from anywhere. Even if it is defined below where you're claling it.

var foo = function isn't callable until after the line where it's created.


What's the difference between `.call` and `.apply`?
They allow different types of arguments. Call is good for constructors, and allows you to inherit to another object. Apply can use an array, or //RETURN

Explain `Function.prototype.bind`.
Creates a new function where this can be replaced with a particular value (for ex an object with a defined arg in common)

What's the difference between feature detection, feature inference, and using the User Agent string?
Feature detection detects features based on browser implementations. Future inference checks for one feature and assumes something about another feature from that. UA string is how the browser identifies itself.

Explain AJAX in as much detail as possible.
Obviously it’s an asynchronous Javascript and HTML. Allows interaction with server side script and can receive information, allowing for updating portions of a page based on the user input.

Have you ever used JavaScript templating?
I have not.
  * If so, what libraries have you used?
//RETURN

Explain "hoisting".
Variables and functions may be able to be called before they’re declared. Especially relevant to scoping.

Describe event bubbling.
When an event is captured by an innermost element and then passed to outermost elements.

What's the difference between an "attribute" and a “property"?
attribute pulls an HTML attribute and property pulls the DOM property.

Why is extending built-in JavaScript objects not a good idea?
Browsers may override your specific method.

What is the difference between `==` and `===`?
Triple equals is a more strict definition of equality.
Double equals is the evil cousin which will return technically true results.

Triple equals will check the type of the two operands.
Double equals will performs type coersion.

0 === '0' returns false.
0 == '0' returns true.

http://stackoverflow.com/questions/359494/does-it-matter-which-equals-operator-vs-i-use-in-javascript-comparisons

Explain the same-origin policy with regards to JavaScript.
A security policy that prevents javascript from accessing sites outside the current domain.
Allows multiple scripts to access data across other page six both have the same origin. 
  
What is the extent of your experience with Promises and/or their polyfills?
Created many promises for Async actions with AJAX. Allows to write code for a value that will exist sometime in the future.

What are the pros and cons of using Promises instead of callbacks?
Promises allow fewer nested anonymous functions and is easier to read. But don’t allow for specific values.

What tools and techniques do you use debugging Javascript code?
I use the chrome developer tools, 'debugger' keyword in Javascript, and console.logs.

What language constructions do you use for iterating over object properties and array items?
Loops: For, for…in, .forEach, 
Functions: .map, .filter, .reduce 


## Database Questions

Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

User
id
email
password

Profile
user_id
About
Wall
Posts
Comments

Messages
user_id(s)
Message content

Posts
user_id
profile_id
content
timestamp


## Ruby/Rails

What are ruby gems?
Gems are much like libraries in Javascript or Node Modules - others’ scripted code you can include in your Ruby file to improve functionality.

What is the difference between a symbol and a string?
Symbols refer to the same value, strings are all different. // The main difference is that multiple symbols representing a single value are identical whereas this is not true with strings. // reference the value but aren’t the value itself

What is the difference between a class method and an instance method?
Class methods can be called with the class name where instances are one particular case of a class. // Instance methods use an instance of a class, whereas a class method can be used with just the class name. // class method exists for all instances/ instances are for that one alone.

What is the difference between local variables, instance variables, and class variables?
Local variables reference an object. Instance is a little similar to this in that it refers to a particular value for each different instance. Class variables are instances. // It's a matter of scope. 
A local variable is only visible/usable in the method in which it is defined (i.e., it goes away when the method returns). Not associated with classes, only with their own scope of what function they’re in.
An instance variable, on the other hand, is visible anywhere else in the instance of the class in which it has been defined 
This is different from a class variable, which is shared between all instances of a class.

What is a range?
Ranges are a series of numbers between a minimum and maximum designated inside parentheses. // Sequences have a start point, an end point, and a way to produce successive values in the sequence. In Ruby, these sequences are created using the ".." and "..." range operators. The two dot form creates an inclusive range, and the three-dot form creates a range that excludes the specified high value.

In ruby, what does attr_accessor do?  
Allows you to read and write to a particular instance variable.

What is the purpose of environment files under the config folder in Rails? (development, test, production)
They make it easier to deploy.

What is the purpose of the application.rb file in Rails?
Ties together all the requirements and pulls in Active Record along with setting up the Application class.

How can you define a constant?
All caps at the top of a page. // Constants begin with an uppercase letter.

What is the purpose of `yield`?
When you write a method that takes a block, you can use the yield keyword to execute the block.

How do you store API keys when creating an app?
.env file {also can store as a constant} // Alternative is to create a yaml file, then read it when your app signs in to an api. This is the style used by rails itself with the config/databse.yml file // You can also store as a constant using a hash or nested hash.

How do I send parameters through a url?
Create a helper function in your controller (typically a user_params would be in a user controller for example) that allows a particular param with particular named parameters attached. // f you use helper methods for routes (for example company_path), then you can add hash of params, so this two should be similar.

Explain MVC
Model View Controller - allows you to set up object-database relationships, display pages, and routing in a simple way. // http://stackoverflow.com/questions/1931335/what-is-mvc-in-ruby-on-rails

What is a `before_action`? When would you use it?
It’s useful when checking if a user is authenticated, to limit availability to particular pages. // "Before" actions may halt the request cycle. A common "before" action is one which requires that a user is logged in for an action to be run.

What do controllers do in rails?
They make for clean routing. // They create actions based off of different routes that enable CRUD capabilities/different views.

What is RESTful routing?
Representational State Transfer. 

Using different methods for different actions, i.e. post for put. Verb + url
http://stackoverflow.com/questions/2441962/what-is-restful-routing

What is a polymorphic association?
Allows models to belong to more than one model, as in votes or comments. Lets you call on a given "belongs to" with multiple classes. // One table for many things

What are params?
Used for post data, or from the URL. // You will probably want to access data sent in by the user or other parameters in your controller actions. There are two kinds of parameters possible in a web application. The first are parameters that are sent as part of the URL, called query string parameters. The query string is everything after "?" in the URL. The second type of parameter is usually referred to as POST data. This information usually comes from an HTML form which has been filled in by the user. It's called POST data because it can only be sent as part of an HTTP POST reques

How do I make a migration to add a column in Rails? change_column :products, :part_number, :text // If you have already run your original migration (before editing it), then you need to generate a new migration (rails generate migration add_email_to_users email:string will do the trick). Then do a rake db:migrate and it'll run the new migration.

What is CSRF? How does Rails protect an app against this?
There are built in security measures that require a valid token and protect from forgeries. Rails is smarter than I am. // Sessions that never expire extend the time-frame for attacks such as cross-site request forgery (CSRF), session hijacking and session fixation. An attacker maintaining a session every five minutes can keep the session alive forever, although you are expiring sessions. A simple solution for this would be to add a created_at column to the sessions table. Now you can delete sessions that were created a long time ago. 

What's the difference between `User.find_by_id(1)` and `User.find(1)`?
They return different things if there’s a nonexistent record. .find is the exception or 404 response vs nil for find_by_id. // Find is less specific and returns just one user.

What's are classes in Ruby? What are modules? And what's the difference?
Classes makes it easy to collect a series of functions or variables and make them easily accessible.  Modules are similar but a little closer to hashes. Classes are more easy to multiply. // Modules are about providing methods that you can use across multiple classes - think about them as "libraries" (as you would see in a Rails app). Classes are about objects; modules are about functions.


## Testing Questions

What are some advantages/disadvantages to testing your code?
Advantages: you know as you build that there’s basic functionality. Disadvantages is building a less functional or useful script just to pass some test. Test suite maintainment, hard to write, slows dev.
https://www.quora.com/What-are-the-Pros-and-Cons-of-Test-Driven-Development

What tools would you use to test your code's functionality?
I use RSPEC mainly, although E2E is appealing and I'd like to learn it.

What is the difference between a unit test and a functional/integration test?
Testing one isolated part versus the whole code.

What is the purpose of a code style linting tool?
Lints analyze code for stylistic errors - like misspellings -  useful for Javascript to make sure your code looks as good as possible.

What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?
Checking if every part of the code works from the user end as expected from beginning to final part of the page. Can vary between seeded data and using a real server. Angular provides its own E2E testing
https://medium.com/how-we-build-fedora/e2e-testing-with-angular-protractor-and-rails-725fbefb8149#.kfonznidd

## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
1020

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```
var add = function(x) {
  return function(y) {
    return x + y;
  }
}


*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
“goh angasal a m’i”

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
“Hello World”

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
2

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
undefined

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
one three two

## Fun Questions:

What's a cool project that you've recently worked on?
The Artr - a fun social media experiment that I enjoy fiddling with still. A Program Manager app with an awesome group.
What are some things you like about the developer tools you use?
I like that git saves things. I like that Sublime Text has a bunch of functionality.
Do you have any pet projects? What kind?
I like turning stories into functional webpages, which I have fun with! Currently working on a simple JQuery text based story.
* How do you like your coffee?
No coffee, more of a chai person. Caffeine combines badly with a bad ticker.