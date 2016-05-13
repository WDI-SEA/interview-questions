#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
Yesterday we learned oAuth (authorization through a third party like Facebook). This week we covered M to M relationships between tables in Rails.

* What excites or interests you about coding?
I love being able to create any type of website and knowing how certain websites work. I spend all my time on the internet, so it's fun to make the switch from being a passive consumer, to actively create stuff for the internet.

* What is a recent technical challenge you experienced and how did you solve it?
For my last project, I was using webRTC to set up video chats online. webRTC required an https connection to operate, while the process of obtaining a caller id from PeerJS was through a http connection. In order to get the video up and running, I had to find a way to set up by own PeerJS server that served keys through https. 

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
My approach to building with a web application is to first make sure that everything works. I would do this by first deciding what the application is and what I want it to do. Then I would add the bare miminum to the site just to make sure it has a basic, working functionality. For performance, I would do my best to make sure that nothing in my code is redundant. Setting up easily understood variables and commenting every line of code to explain my thought process would also help with maintainability. Depending on the time and resources available for the project, I would be able to decide which technologies to incorporate. Node.js would take longer to set up than Ruby, but Node.js is much more efficient for large scale applications.

* Talk about your preferred development environment.
My preferred development environment is where I am sitting next to other devs that I would be able to talk to and bounce ideas off of while I'm working. Having someone immediately available to offer a second opinion or a new perspective is extremely valuable to my growth as a programmer.

* Which version control systems are you familiar with?
Git/github.

* Can you describe your workflow when you create a web page?
First decide what the web page is supposed to do, be it collect information or display images. Then I would set up the basic divs and important elements in the html. Then I would add the javascript functions that are necessary to get the page running. Then I would work on the styling and any other small features for the page.

* If you have 5 different stylesheets, how would you best integrate them into the site?
I would add a different folder labeled either static for a node.js app, or create more scss style pages under the assets folder for a ruby on rails app. I would call the appropriate stylesheets within the appropriate pages for the site.

* Can you describe the difference between progressive enhancement and graceful degradation?

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
Assuming that all of the images are url links, I could simply put them in an object and label each element with a key. Then I would create a function in the Javascript that would change the html depending on a button that would be clicked. The button would call a function that would change the url of the html element every few seconds or so, giving the effect of a slideshow.

* If you could master one technology this year, what would it be?
I would love to be able to master webRTC or anything to do with videos/streaming.

* Explain the importance of standards and standards bodies.
Standards are important as it ensures that code will looks the same and have similar formats no matter where you are. It allows people to expect the same set of standards when working in a new environment and subsequently allows programs and applications to scale.

## HTML Questions

* What does a `doctype` do?
Doctype determines the type of document used.

* What's the difference between HTML and XHTML?
XHTML is much more standardized and allows pages to be viewed the same across different browsers, while HTML pages often looked different depending on the user's browser.

* What are `data-` attributes good for?
They allow you to store data on html documents.

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
A cookie is something that stores data. A session storage is the memory stored in a session, while local storage is where that memory is stored.

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
This to ensure that the page is styled before anything else is processed on the page. If ther JS takes too long to process and the style tage is after it, then the page would appear plain until the JS is finished computing.


## CSS Questions

* What is the difference between classes and IDs in CSS?
A class can cover many different elements, while ID's only have one element.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
Reset removes default styling, while normalizing just makes the styling the same. Normalizing CSS would be my choice.

* Describe Floats and how they work.
Floats allow elements to be organized and separate with relative positioning.

* Describe z-index and how stacking context is formed.
Z-index determines the order of overlap for different elements.

* Have you ever used a grid system, and if so, what do you prefer?
Grid systems are useful for organizing content.

* Have you used or implemented media queries or mobile specific layouts/CSS?
I have implemented media queries before when using webRTC.

* How do you optimize your webpages for print?
Determining the most important content for the website and stlying the print pages as such.

* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
You might have to import the fonts first before using it.

* Explain how a browser determines what elements match a CSS selector.
It would depend on the the linked stylesheet and the html tags. If the tags also have classes or ids that are present in the stylesheet, they would be modified as such.

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
The box model gives each element margins, padding, content, and borders. They determine how the element is spaced out and separated on the page.

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
inline, inline-text
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
Relative changes depending on the positions of the other elements, fixed keeps the element from moving regardless of the browser size.
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
specificity. an id would be more important than a class.
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Explain some of the pros and cons for CSS animations versus JavaScript animations.

## JS Questions

* Explain event delegation
* Explain how `this` works in JavaScript
references the most immediately called element
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
