#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

**What did you learn yesterday/this week?**
Lately I have been working within the Rails framework, and most recently I tried to turn one of my old Rails-based apps into a Single Page Application.  It was really cool trying to figure out how to send responses just in JSON data and dynamically render the page with that data on the client side.  It was made a little more interesting because I was doing all the client-side work with jQuery, so there was some fun manual DOM manipulation involved.

**What excites or interests you about coding?**
Coding to me feels like a paintbrush, a simple tool that you can dip into lots of different colors and use to create anything you want, whether it be useful or simply fun.  In particular I love to look at things at a low level and try to grasp the inner workings of them - sometimes I just put tiny dots of paint next to each other to see how their colors mix.

**What is a recent technical challenge you experienced and how did you solve it?**
I've been working on this web tool for construction general contractors and subcontractors to post and submit bids back and forth on projects, and one part of it involved a form where I wanted to dynamically add new fields to the form.  I went through a few different approaches trying to use ajax, but in the end I discovered that if I used the same name attribute for each element the post request would send the data as an array that I could manipulate.  The solution in the end turned out to be pretty simple.

**What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?**
I first start thinking about a project by looking at the requirements that I'm given or that I want to achieve, and then I start to organize my thoughts into how I can best implement this in a given amount of time, and how those choices are going to affect the user experience.  For example, I was asked about making an app for a local business group that involved storing some simple data about small businesses.  I thought about whether to use a SQL or noSQL database, and this case was simple enough that a noSQL database would probably be more efficient, but in the end I thought the efficiency gains wouldn't be significant on a small scale and it might be more maintainable in the long run to use a SQL database.

**Talk about your preferred development environment.**
As far as IDE's go, I used to use eclipse in college and I appreciated the debugging tools for larger java and python projects, but lately I have been using Sublime for web projects and I love how lightweight it is.

**Which version control systems are you familiar with?**
Git.

**Can you describe your workflow when you create a web page?**
If it is a bigger project, I'll start by sketching out a basic wireframe of it and try to think through potential workflows.  From there, I'll start to build the basic structure of the page.  If the page is going to need some persistent data, then I'll build out the basics of the back end and test out the models and tables before putting skin on it with the pages and routes.   For the client-side I'll add in basic css and javascript directories and dependencies like bootstrap and jquery, and then build structure from the basic elements on up.  Finally I'll add required features one at a time until I get to some minimum viable product.

**If you have 5 different stylesheets, how would you best integrate them into the site?**
If for example I had multiple templates that I wanted to use color schemes or elements from, I would stack them in my page so that they only over-rode each other the way I wanted them to.  So for example I would most likely have bootstrap as the first style sheet and a style sheet with any of my own tweeks as the very last one, and I would have to decide how I wanted to order any other third party sheets I wanted in between.

**Can you describe the difference between progressive enhancement and graceful degradation?**
I'm just going to take a shot and say that these terms sound like they describe best practices for dealing with older browsers or maybe various screen sizes.  They sound almost like approaching the issue from either the top down or the bottom up.

**Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).**
I think my first approach would be to use a bootstrap carousel, and maybe set a timeout event to switch the picture automatically on a timer.  I would try to look and see if anyone else has done it in a way that I like too and see if there is anything I can learn from that.

**If you could master one technology this year, what would it be?**
Either neural networks, or sockets.

**Explain the importance of standards and standards bodies.**
Honestly my thoughts on this subject aren't that deep, but I do find standards to be helpful because they give us predictability and consistency in how code will be run.

## HTML Questions

**What does a `doctype` do?**
I

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
* List as many values for the display property that you can remember.
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
