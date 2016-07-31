#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
** This week I was working on _ _ _ . (I will be doing personal programming projects following my completion of GA, so I'll have plenty to talk about)

* What excites or interests you about coding?
** Programming allows one to build almost anything. You get to use creativity and technical problem solving skills to bring ideas in to the world.

* What is a recent technical challenge you experienced and how did you solve it?
** We recently competed in a hackathon during class where we were tasked with building a MEAN stack app. Aside from the challenges of working together with version control system, we encountered problems getting some angular dependencies to work. The two of us working on this issue studied two different sets of docs and came together later to share what we learned. We ended up moving a directive to a different div to get our dependency to behave correctly...

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
** When it comes to UI, I prefer to make things as simple as possible. I find that when I am presented with too many choices or too much information that it becomes harder for me to make a decision. When presented with a clustered or unorganized UI, I am less likely to use the site or app. 
** Maintainability requires forethought. You should constantly be thinking about your future self and how other devs might see your work if they were to pick it up at some later point. I try to separate concerns in to appropriately named folders. I also try to write descriptive commit messages and meaningful comments throughout my code. Along with these things, I try write helpful README's in my repos.

* Talk about your preferred development environment.
** I like to work in a quiet cool place. I use Sublime text editor with minimal packages and/or default settings. I like using aliases to speed up my command line movement.
* Which version control systems are you familiar with?
** Git

* Can you describe your workflow when you create a web page?
** I define customer or personal goals, (user stories). I ask myself what tools would be appropriate for the proposed project. I sketch outlines and wireframe everything. I write some pseudo code, then jump in to programming.

* If you have 5 different stylesheets, how would you best integrate them into the site?
** I would keep them all in one folder but organize them based on speceficity. I'd link to them in my index.html in order of speceficity as well.

* Can you describe the difference between progressive enhancement and graceful degradation?
** Graceful degradation starts from the status quo of complexity and tries to fix for the lesser experience whereas progressive enhancement starts from a very basic, working example and allows for constant extension for future environments. Degrading gracefully means looking back whereas enhancing progressively means looking forward whilst keeping your feet on firm ground. (Taken from some article)

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
** I would create an array of image links. I'd write a function with set interval to loop through the array and display the image element in a div. Instead of appending image elements in the div I'd replace them.

* If you could master one technology this year, what would it be?
** I would master D3 or some kind of Geo location service.

* Explain the importance of standards and standards bodies.
** The importance of standards is to maintain organization and clarity. Standards bodies do the same thing on a wider scale. (Over simplified answer). Web development would be like the Wild West if people didn't adhere to some set of standards when building things.

## HTML Questions

* What does a `doctype` do?
** It tells the browser what kind of document to expect.

* What's the difference between HTML and XHTML?
** http://stackoverflow.com/questions/4153403/what-is-difference-between-xhtml-and-html
** XHTML document must have a DOCTYPE declaration at the top of the document.
** All XHTML tag and attribute names must be written in lower case.
** All the tags must be nested properly.
** End tags are required for non-empty elements.
** The start tag of an empty element must end with />.
** All the attribute values must be quoted.
** Attribute minimization is forbidden.

* What are `data-` attributes good for?
** Data attributes are good for adding additional selection parameters on elements.

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
** Cookies are objects containing information on the client side with a size limit under 5000 bytes.

** Local storage are objects containing information on the client side with a size limit of 5MB

** sessionStorage: Data stored in sessionStorage gets deleted when the page session ends. It will persist while you navigate to different pages on a site but will end when you open a new tab.

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
** http://stackoverflow.com/questions/436411/where-is-the-best-place-to-put-script-tags-in-html-markup
** Putting CSS links in the head allows for the styling to be applied to the HTML document as it is loaded. It's generally good practice to inlude JS files just before the end of the body because the page can continue to load before trying to load the JS files. 

** Modern browsers support async and defer tags on script elements so that a browser can load things in an order which is most helpful for the end user. All script tags can go in the head.

## CSS Questions

* What is the difference between classes and IDs in CSS?
** Classes are meant to apply to multiple elements while ID's are meant to be used once on a specific element.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
** http://stackoverflow.com/questions/6887336/what-is-the-difference-between-normalize-css-and-reset-css
** Normalize preserves useful defaults while reset unstyles everything, has better documentation, and is more modular.

* Describe Floats and how they work.
** https://developer.mozilla.org/en-US/docs/Web/CSS/float
** The float CSS property specifies that an element should be taken from the normal flow and placed along the left or right side of its container, where text and inline elements will wrap around it.

* Describe z-index and how stacking context is formed.
** https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context
** Positioning and assigning a z-index value to an HTML element creates a stacking context, (as does assigning non-full opacity).
** Stacking contexts can be contained in other stacking contexts, and together create a hierarchy of stacking contexts.
** Each stacking context is completely independent from its siblings: only descendant elements are considered when stacking is processed.
** Each stacking context is self-contained: after the element's contents are stacked, the whole element is considered in the stacking order of the parent stacking context.

* Have you ever used a grid system, and if so, what do you prefer?
** I've only used Bootstrap Flexbox. I like Flexbox more for no specific reason.

* Have you used or implemented media queries or mobile specific layouts/CSS?
** Hell yeah, it's awesome.

* How do you optimize your webpages for print?
** https://davidwalsh.name/optimizing-structure-print-css
** Create A Stylesheet For Print
** Of course you have at least one stylesheet to control the layout of the page and formatting of the content, but do you have a stylesheet to control how your page will look like in print? Add the print style sheet, with the media attribute set to "print", at the end of the list of stylesheets in the header. This will allow you to create custom CSS classes applied only at the time of print. Make sure your structure CSS file is given a media attribute of "all."
  
* What are the advantages/disadvantages of using CSS preprocessors?
** http://nosleepforsheep.com/using-a-css-preprocessor/
  * Describe what you like and dislike about the CSS preprocessors you have used.
  ** Sass looks and acts more like JavaScript.

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
** https://codepen.io/fightingtheboss/pen/BNajOr
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
