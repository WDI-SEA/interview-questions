#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.


## General Questions

* What did you learn yesterday/this week?
  * This week as all about Angular. I learned how to use Angular to bind data to front-end controllers that allow updates to be reflected immediately and without making another call to the server to refresh the page. 
---
* What excites or interests you about coding?
  * I am excited to be a builder. 
---
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
---
* Talk about your preferred development environment.
  * I would prefer a collaborative environment where creativity and input in the products is encouraged.
---
* Which version control systems are you familiar with?
  * Github is the version control system I use, I have experience working in teams and using githug to manage our project code. 
---
* Can you describe your workflow when you create a web page?
  * After mapping the idea out mentally, I use either paper, OneNote, or the prototype software Axure to start mapping out what the pages would look like, how they would connect, and why kind of data I would need on each page. I then think about if I need a database and the structure of tables I would need. I frequently draw a few test tables with rows of data and their relationships to test my ideas. After I think I have a solid plan, I go to my app directory and start mapping out my folders in an MVC format that makes sense for the tools I am going to use. 
---
* If you have 5 different stylesheets, how would you best integrate them into the site?
  * If i were using 5 different style sheets I would consider upgrading to SCSS and compiling all the stylesheets together when the app is run. SCSS would also allow me create and use variables that might be useful when you have to make changes across 5 stylesheets. 
---
* Can you describe the difference between progressive enhancement and graceful degradation?
* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.

## HTML Questions

* What does a `doctype` do?
* What's the difference between HTML and XHTML?
* What are `data-` attributes good for?
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

## CSS Questions

* What is the difference between classes and IDs in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
* Describe z-index and how stacking context is formed.
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* How do you optimize your webpages for print?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
---
* List as many values for the display property that you can remember.
  * block, inline, inline-block, inline-flex
---
* What's the difference between inline and inline-block?
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
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
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

`Answer: Facebook Database
Model 1: Users
|id   |Name   |email   |password|
|-----|-------|--------|--------|
|1    |Bob    |b@b.com |D3DNSJK4|
|2    |Sue    |su@e.com|NDK9SND3|

Model 2: Posts
|id   |Content|
|-----|-------|
|1    |"YoLo" |

Model 3: UsersPosts
|id   |user_id|post_id |
|-----|-------|--------|
|1    |1      | 1      |


Model 4: Friends
|id   |user1_id|user2_id|
|-----|--------|--------|
|1    |1       |2       |`

## Ruby/Rails
* What are ruby gems?
* What is the difference between a symbol and a string?
---
* What is the difference between a class method and an instance method?
  * Answer: A class method is available to any instance of the class. An instance method is only available to that one instance. 
---
* What is the difference between local variables, instance variables, and class variables?
  * Answer: *Local variables* cannot be used outside the method in which they are defined. *Instance variables* start with the @ symbol and are available outside the method in the class and available in associated view pages. *Class Variables* start with two @@ symbols are are availale in all methods of the class and can be called by all instances of the class.
---
* What is a range?
  * Answer: There are 2 types of ranges in Ruby, an inclusive range and an exclusive range. The inclusive range is written as 0..5 and will include number 5. en exclusive range is written as 0...5 and will not include number 5.
---
* In ruby, what does attr_accessor do?  
  * Answer: attr_accessor allows variables in a method to be overwritten and read. If you want your variables to only be read you use attr_reader, if you want your variables to only be written you use attr_writer. 
---
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
*Answer: foo = 1020;
---
*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```
---
*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
*Answer: returns "goh angasal a m\'i"
---
*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
*Answer: The function in parans is executed immediately and will alert the statement "Hello World". The second alert, however, will not run because bar is not defined outside of the function and is undefined for the second alert.
--- 
*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
*Answer: After the two push operations, foo = [1, 2] and the length is 2.
---
*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
*Answer: I didn't think this was correct code in javascript, but if it were, I at first i thought foo.x would eq {n:2}. After some testing, the = to = in one line makes foo.x undefined... and furthermore, even if it were separated on different lines, foo.x would still be undefined because we are overwriting the entire object again with {n:2}, therefore eliminating our x key. 
---
*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
*Answer: At first I thought because of the timeout is set to 0, two will print after one still. However, the function still has to be run, after testing I confirmed that one and three will print first and then two immediately afterwards. The print on the console will look like:
one
three
two
---
## Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Do you have any pet projects? What kind?
* How do you like your coffee?
