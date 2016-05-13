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
It gets added in to the top of my sublime snippets for the basic head/body html structure, and I've always assumed it tells browsers that the following content is an html document.

**What's the difference between HTML and XHTML?**
Honestly I'm not familiary with XHTML.  Maybe it was some sort of dynamically capable HTML before HTML5?

**What are `data-` attributes good for?**
I'm not sure on that one either.

**Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.**
I've not actually used cookies or sessionStorage manually, and I have used localStorage but that was just to mess around with it.  It seems to me that localStorage is best used for data larger than what you would put in a cookie, and maybe something you wanted to access only on the client side so you wouldn't persist it in a database.  I have used helper libraries in both Node and Rails apps that allowed me to store user session states on the server, and I wonder if these were using either sessionStorage or cookies in order to make that happen.

**Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?**
You want your CSS to load before your content so that your page loads cleanly (i.e. so your text doesn't load before you set styles to it.  The JS is running actions on the content of the page, so it's both faster and avoids some errors if you load it at the bottom of the body.  I don't know of any specific exceptions, but I could potentially see some cases where I might want to load content before styling for a slow connection, or maybe there's some case where you are dynamically generating content with JS and want to load it in the head.

## CSS Questions

**What is the difference between classes and IDs in CSS?**
IDs are used only once, and classes are used multiple times.

**What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?**
Using a reset stylesheet removes all default browser styling, and a normalize stylesheet ensures a uniform default styling across all browsers.  I would always use normalize unless there is something in the default styling that I specifically want to avoid.  And of course it is built into bootstrap already.

**Describe Floats and how they work.**
Floats slide an element in a given direction until they reach a boundary (such as a sister block element or a containing element.

**Describe z-index and how stacking context is formed.**
Z-index lets you manually configure the order of layering elements, with the lowest indexes appearing on top.

**Have you ever used a grid system, and if so, what do you prefer?**
The only grid system I've used is bootstrap, and I use it pretty standardly.

**Have you used or implemented media queries or mobile specific layouts/CSS?**
Yes, mainly I use bootstrap classes to manage mobile layouts, but I do have some practice writing media queries and moving from a mobile first perspective with mobile as default and progressively larger min-width media queries.

**How do you optimize your webpages for print?**
Ohhhh, to be printed out?  I haven't taken that into account with any projects yet.  That is something I'll start adding to my requirements list.

**What are the advantages/disadvantages of using CSS preprocessors?**
I don't have a lot of experience with SASS or LESS, but by precompiling your CSS they speed up page load, but they add another small layer of complexity to the development prcess.

**Describe what you like and dislike about the CSS preprocessors you have used.**
The only experience I have is a little experimenting with SASS I did a while ago and it seemed fine.

**How would you implement a web design comp that uses non-standard fonts?**
Include a link to the stylesheet containing the font, either through google fonts or a propietary one.

**Explain how a browser determines what elements match a CSS selector.**
It does a depth-first search of the markup tree, filtering elements that match progressively more specific parameters in the query.  For example, if you query '.content', it will return all elements in the document with class 'content'.  If you query 'div .content', it will return all elements with class 'content' that are within a div.  And finally, if you query 'div.content' it will only return divs that are of class 'content'.  This last type of selector is good practice to speed up your queries, so if you're searching for a specific ID, you can skip all elements that aren't of the type you're searching for.

**Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.**
So every element in an html doc is a box, from the body on down, and all are nested within other boxes and potentially siblings of other boxes.  So starting with the body box, we nest boxes inside, and position them based on their css position attribute.  They can be positioned absolutely in the window, as if they were not nested at all, or relative to other parent and sibling boxes.  By default they all float to the top and then the right, but we can controll that behavior.

**What does ```* { box-sizing: border-box; }``` do? What are its advantages?**
I don't remember...

**List as many values for the display property that you can remember.**
Block, inline-block, inline, and none.

**What's the difference between inline and inline-block?**
To be honest, I just know that inline-block is better for making divs inline.  I generally only use inline for elements like list items.

**What's the difference between a relative, fixed, absolute and statically positioned element?**
Relative: moves in block or inline position within a containing element and relative to siblings.
Fixed: positioned absoultely and will not move on scroll.
Absolute: positioned by coordinates in window.

**The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?**
The style assigned to an element deeper in the markup tree will override the style of those above it.  For example, if you set color for text in the body to blue, all text will be blue, except for text in an element within the body that set the color for.

**What existing CSS frameworks have you used locally, or in production? How would you change/improve them?**
Bootstrap.  I woud love an easy way plug and play with color schemes.

**Have you played around with the new CSS Flexbox or Grid specs?**
Not yet.

**Have you ever worked with retina graphics? If so, when and what techniques did you use?**
No I haven't.

**Explain some of the pros and cons for CSS animations versus JavaScript animations.**
Hmm, just offhand I would go to CSS animations for things I want to happen on load, and JS for things I want to be event-controlled.  There might be some good reasons to use a JS event listener to activate a CSS animation though.

## JS Questions

**Explain event delegation**
Is this part of its asynchronous functionality?  As in, you set up an event listener, it delegates listening for that to an event loop, and then executes a callback funtion upon the event...?

**Explain how `this` works in JavaScript**
'This' refers to the object that is calling a function.  It is most commonly used in OOP for getting and setting attributes and methods.

**Explain how prototypal inheritance works**
Every class has a prototype object

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
