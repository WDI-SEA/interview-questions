#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
  * This week I was working on _ _ _ . (I will be doing personal programming projects following my completion of GA, so I'll have plenty to talk about)

* What excites or interests you about coding?
  * Programming allows one to build almost anything. You get to use creativity and technical problem solving skills to bring ideas in to the world.

* What is a recent technical challenge you experienced and how did you solve it?
  * We recently competed in a hackathon during class where we were tasked with building a MEAN stack app. Aside from the challenges of working together with version control system, we encountered problems getting some angular dependencies to work. The two of us working on this issue studied two different sets of docs and came together later to share what we learned. We ended up moving a directive to a different div to get our dependency to behave correctly...

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
  * When it comes to UI, I prefer to make things as simple as possible. I find that when I am presented with too many choices or too much information that it becomes harder for me to make a decision. When presented with a clustered or unorganized UI, I am less likely to use the site or app. 
  * Maintainability requires forethought. You should constantly be thinking about your future self and how other devs might see your work if they were to pick it up at some later point. I try to separate concerns in to appropriately named folders. I also try to write descriptive commit messages and meaningful comments throughout my code. Along with these things, I try write helpful README's in my repos.

* Talk about your preferred development environment.
  * I like to work in a quiet cool place. I use Sublime text editor with minimal packages and/or default settings. I like using aliases to speed up my command line movement.
* Which version control systems are you familiar with?
  * Git

* Can you describe your workflow when you create a web page?
  * I define customer or personal goals, (user stories). I ask myself what tools would be appropriate for the proposed project. I sketch outlines and wireframe everything. I write some pseudo code, then jump in to programming.

* If you have 5 different stylesheets, how would you best integrate them into the site?
  * I would keep them all in one folder but organize them based on specificity. I'd link to them in my index.html in order of specificity as well.

* Can you describe the difference between progressive enhancement and graceful degradation?
  * Graceful degradation says build something for the newest technologies and try to work backwards to accomodate
  older browsers
  * Graceful degradation starts from the status quo of complexity and tries to fix for the lesser experience whereas progressive enhancement starts from a very basic, working example and allows for constant extension for future environments. Degrading gracefully means looking back whereas enhancing progressively means looking forward whilst keeping your feet on firm ground. (Taken from some article)

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
  * I would create an array of image links. I'd write a function with set interval to loop through the array and display the image element in a div. Instead of appending image elements in the div I'd replace them.

* If you could master one technology this year, what would it be?
  * I would master D3 or some kind of Geo location service.

* Explain the importance of standards and standards bodies.
  * The importance of standards is to maintain organization and clarity. Standards bodies do the same thing on a wider scale. (Over simplified answer). Web development would be like the Wild West if people didn't adhere to some set of standards when building things.
  * Some examples of web standards are to include alt tags on images so blind people can understand what an image shows
  * Think about cross browser compatability, IE support


## HTML Questions

* What does a `doctype` do?
  * It tells the browser what kind of document to expect.

* What's the difference between HTML and XHTML?
  * Uses XMl, a stricter lang
  * http://stackoverflow.com/questions/4153403/what-is-difference-between-xhtml-and-html
  * XHTML document must have a DOCTYPE declaration at the top of the document.
  * All XHTML tag and attribute names must be written in lower case.
  * All the tags must be nested properly.
  * End tags are required for non-empty elements.
  * The start tag of an empty element must end with />.
  * All the attribute values must be quoted.
  * Attribute minimization is forbidden.

* What are `data-` attributes good for?
  * Data attributes are good for adding additional selection parameters on elements. Stores extra data. 

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
  * Cookies are objects containing information on the client side with a size limit under 5000 bytes.

  * Local storage are objects containing information on the client side with a size limit of 5MB

  * sessionStorage: Data stored in sessionStorage gets deleted when the page session ends. It will persist while you navigate to different pages on a site but will end when you open a new tab.

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
 
  * http://stackoverflow.com/questions/436411/where-is-the-best-place-to-put-script-tags-in-html-markup
 
  * Putting CSS links in the head allows for the styling to be applied to the HTML document as it is loaded. It's generally good practice to inlude JS files just before the end of the body because the page can continue to load before trying to load the JS files. 

  * Modern browsers support async and defer tags on script elements so that a browser can load things in an order which is most helpful for the end user. All script tags can go in the head.

## CSS Questions

* What is the difference between classes and IDs in CSS?
  * Classes are meant to apply to multiple elements while ID's are meant to be used once on a specific element.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
  * http://stackoverflow.com/questions/6887336/what-is-the-difference-between-normalize-css-and-reset-css
  * Normalize preserves useful defaults while reset unstyles everything

* Describe floats and how they work
  * https://developer.mozilla.org/en-US/docs/Web/CSS/float
  * The float CSS property specifies that an element should be taken from the normal flow and placed along the left or right side of its container, where text and inline elements will wrap around it.

* Describe z-index and how stacking context is formed.
  * https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context
  * Positioning and assigning a z-index value to an HTML element creates a stacking context, (as does assigning non-full opacity).
  * Stacking contexts can be contained in other stacking contexts, and together create a hierarchy of stacking contexts.
  * Each stacking context is completely independent from its siblings: only descendant elements are considered when stacking is processed.
  * Each stacking context is self-contained: after the element's contents are stacked, the whole element is considered in the stacking order of the parent stacking context.

* Have you ever used a grid system, and if so, what do you prefer?
  * I've only used Bootstrap and Flexbox. I dislike Bootstrap because so much of the web looks Bootstrappy.

* Have you used or implemented media queries or mobile specific layouts/CSS?
  * Hell yeah, they're awesome.

* How do you optimize your webpages for print?
  * https://davidwalsh.name/optimizing-structure-print-css
  * Create A Stylesheet For Print
  * You can add a style sheet with the media attribute set to "print" at the end of the element in the header. This will allow you to create custom CSS classes applied only at the time of print. Make sure your structure CSS file is given a media attribute of "all."
  
* What are the advantages/disadvantages of using CSS preprocessors?
  * http://nosleepforsheep.com/using-a-css-preprocessor/

* Describe what you like and dislike about the CSS preprocessors you have used.
  * Sass looks and acts more like JavaScript, which is great. You can keep your CSS a lot more organized.

* How would you implement a web design comp that uses non-standard fonts?
  * http://www.w3schools.com/cssref/css3_pr_font-face_rule.asp
  * Use the @font-face CSS rule
  * This allows you to define your font name and link to the font file.

* Explain how a browser determines what elements match a CSS selector.
  * http://stackoverflow.com/questions/5797014/why-do-browsers-match-css-selectors-from-right-to-left
  * If you start by just matching the rightmost part of the selector against your element, then chances are it won't match and you're done. If it does match, you have to do more work, but only proportional to your tree depth, which is not that big in most cases.

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
  * The box model is a set of squares that surround an HTML element. Every HTML element has padding, border, and margin.

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
  * The box-sizing CSS property is used to alter the default CSS box model used to calculate widths and heights of elements. It is possible to use this property to emulate the behavior of browsers that do not correctly support the CSS box model specification.

* List as many values for the display property that you can remember.
  * block, inline-block, none, flex, table, and one

* What's the difference between inline and inline-block?
  * Inline: The element will act as an inline element like span if the display value is set to inline
  * Inline-block: Displays an element as an inline-level block container. The inside of this block is formatted as block-level box, and the element itself is formatted as an inline-level box

* What's the difference between a relative, fixed, absolute and statically positioned element?
  * https://css-tricks.com/absolute-relative-fixed-positioining-how-do-they-differ/
  * http://www.webdevbydoing.com/whats-the-difference-between-static-relative-absolute-and-fixed-positioning/
  * Relatively positioned elements can be given attributes that will move them relative to the position they would have been in if they were static
  * A fixed position element is positioned relative to the viewport, or the browser window itself.
  * An absolutely positioned element is actually removed from the DOM and positioned based on its nearest relatively positioned parent element

* The 'C' in CSS stands for Cascading. How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?

  * https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity
  * Priority is defined by specificity and inheritance 
    * Inheritance is a way of propagating property values from parent elements to their children.
  * Specificity: ID > class, psuedo-class > element, psudo-element
    * The quickest way to calculate specifictiy is to do the following. Add 1 for each element and pseudo-element (for example, :before and :after); add 10 for each attribute (for example, [type=”text”]), class and pseudo-class (for example, :link or :hover); add 100 for each ID; and add 1000 for an inline style.
  * Specified value
    * The user agent determines whether the value of the property comes from a style sheet, is inherited or should take its initial value.
  * Computed value
    * The specified value is resolved to a computed value and exists even when a property doesn’t apply. The document doesn’t have to be laid out for the computed value to be determined.
  * Used value
    * The used value takes the computed value and resolves any dependencies that can only be calculated after the document has been laid out (like percentages).
  * Actual value
    * This is the value used for the final rendering, after any approximations have been applied (for example, converting a decimal to an integer).

* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
  * I've used materialize, bootstrap, and flexbox grid.

* Have you played around with the new CSS Flexbox or Grid specs?
  * Not a lot.

* Have you ever worked with retina graphics? If so, when and what techniques did you use?
  * No, but here is some information about retina graphics
    * “Retina” describes really sharp and clear screens that can cram in lots and lots of pixels.
    * The basic concept of a Retina image is that your taking a larger image, with double the amount of pixels that your image will be displayed at (e.g 200 x 200 pixels), and setting the image to fill half of that space (100 x 100 pixels). This can be done manually by setting the height and width in HTML to half the size of your image file.

* Explain some of the pros and cons for CSS animations versus JavaScript animations
  * Use CSS animations for simpler “one-shot” transitions, like toggling UI element states.
  * Use JavaScript animations when you want to have advanced effects like bouncing, stop, pause, rewind or slow-down.
  * If you choose to animate with JavaScript, go with the Web Animations API or a modern framework you are comfortable with.

## JS Questions

* Explain event delegation
  * https://learn.jquery.com/events/event-delegation/
  * https://davidwalsh.name/event-delegate
  * Event delegation refers to the process of using event propagation (bubbling) to handle events at a higher level in the DOM than the element on which the event originated. It allows us to attach a single event listener for elements that exist now or in the future.

* Explain how `this` works in JavaScript
  * http://unschooled.org/2012/03/understanding-javascript-this/
  * Refers to the current context of 'this'
    * There are three types of executable code: Global code, function code, and eval code. Roughly speaking, global code is code at the top level of your program that’s not inside any functions, function code is code that’s inside the body of a function, and eval code is global code evaluated by a call to eval.

    * The object that this refers to is redetermined every time control enters a new execution context and remains fixed until control shifts to a different context. The value of this is dependent upon two things: The type of code being executed (i.e., global, function, or eval) and the caller of that code.
      
* Explain how prototypal inheritance works

  * Every object has a prototype...
  * http://javascript.info/tutorial/inheritance

* Why is it called a Ternary expression, what does the word "Ternary" indicate?

  * It's an expression that if true, will evaluate to the first of two choices. If false, it will evaluate to the latter of the two.

* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?

  * How would you go about checking for any of these states?
  
  * http://lucybain.com/blog/2014/null-undefined-undeclared/

* What is a closure, and how/why would you use one?

  * A closure is a function that has access to private variables. You would use one when you wanted some variables to be private but you still wanted to be able to use them. jQuery makes use of closures.

* What's a typical use case for anonymous functions?

  * Singletons; when you only need to run something once.

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

  * 1st is a function expression, which is available at the top of the code. 2nd is a function declaration, which is available after it is declared. 3rd is an object declaration, this is setting a variable equal to a new instance of the Person object.

* What's the difference between `.call` and `.apply`?

  * http://stackoverflow.com/questions/1986896/what-is-the-difference-between-call-and-apply

* Explain `Function.prototype.bind`.
  
  * http://lucybain.com/blog/2014/function-prototype-bind/

* What's the difference between feature detection, feature inference, and using the User Agent string?

  *http://lucybain.com/blog/2014/feature-detection-vs-inference/

* Explain AJAX in as much detail as possible.
  
  * Asynchronus JavaScript and XML is the process of making asynch calls to resources outside of the current domain using jQuery. You make a http request with certain parameters sent along with it. You then run callback functions upon a successful or fault request.

* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
  * I've used handblebars and EJS.
* Explain "hoisting".
  * Variable declarations are brought to the top of the current scope.
  * http://www.w3schools.com/js/js_hoisting.asp
* Describe event bubbling.

  * Events propogate up to their parents.
  * https://codepen.io/fightingtheboss/pen/BNajOr

* What's the difference between an "attribute" and a "property"?

  * http://stackoverflow.com/questions/258469/what-is-the-difference-between-attribute-and-property

* Why is extending built-in JavaScript objects not a good idea?

  * http://lucybain.com/blog/2014/js-extending-built-in-objects/

* What is the difference between `==` and `===`?

  * == only compares values
  * === compares values + type

* Explain the same-origin policy with regards to JavaScript.

  * The same-origin policy restricts how a document or script loaded from one origin can interact with a resource from another origin. It is a critical security mechanism for isolating potentially malicious documents.
  * The essence of the Same Origin policy can be formulated as: windows can work in contexts of each other only if they are from same protocol://domain:port, or, shortly, from same origin.

* What is the extent of your experience with Promises and/or their polyfills?

  * The Promise object is used for asynchronous computations. A Promise represents an operation that hasn't completed yet, but is expected in the future.
  * Polyfils
  * http://stackoverflow.com/questions/7087331/what-is-the-meaning-of-polyfills-in-html5

* What are the pros and cons of using Promises instead of callbacks?
  * Promises are more composable, often easier to read.
  * https://www.quora.com/Whats-the-difference-between-a-promise-and-a-callback-in-Javascript

* What tools and techniques do you use debugging Javascript code?

  * I use the Chrome Debugger and I put break points in my code. Linting packages and modules also help.

* What language constructions do you use for iterating over object properties and array items?

  * The for - in loop for objects and array methods like map, filter, reduce, and for loops for array items.

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

  * Will link to imgur later.

## Ruby/Rails
* What are ruby gems?

  * Packages for Ruby/Rails

* What is the difference between a symbol and a string?

  * Symbols are only stored once and referenced by pointers. Strings do not share a single memory space.

* What is the difference between a class method and an instance method?
  
  * https://railsforum.com/topic/1523-what-are-the-differences-between-class-and-instance-methods/

* What is the difference between local variables, instance variables, and class variables?

  * http://www.tutorialspoint.com/ruby/ruby_variables.htm

* What is a range?

  * A set of numbers between to points

* In ruby, what does attr_accessor do?

  * Gives read write abilties to variables from outside of the class declaration

* What is the purpose of environment files under the config folder in Rails? (development, test, production)
  
  * To allow for configs in different 'modes'

* What is the purpose of the application.rb file in Rails?

  * To configure and initialie the project.

* How can you define a constant?

  * A Ruby constant is like a variable, except that its value is supposed to remain constant for the duration of the program.

* What is the purpose of `yield`?
  
  * http://www.tutorialspoint.com/ruby/ruby_blocks.htm

* How do you store API keys when creating an app?

  * .environment.rb

* How do I send parameters through a url?

  * http://stackoverflow.com/questions/2124862/link-to-send-parameters-along-with-the-url-and-grab-them-on-target-page

* Explain MVC

  * http://www.tutorialspoint.com/ruby-on-rails/rails-framework.htm

* What is a `before_action`? When would you use it?

  * It's like a hook, you'd use it to do something like check if a user is logged in.

* What do controllers do in rails?

  * http://guides.rubyonrails.org/action_controller_overview.html

* What is RESTful routing?

  * http://stackoverflow.com/questions/2441962/what-is-restful-routing

* What is a polymorphic association?
  
  * https://launchschool.com/blog/understanding-polymorphic-associations-in-rails

* What are params?

  * Places to put arguments, placeholders.

* How do I make a migration to add a column in Rails?

  * http://edgeguides.rubyonrails.org/active_record_migrations.html

* What is CSRF? How does Rails protect an app against this?

  * http://blog.bigbinary.com/2012/05/10/csrf-and-rails.html

* What's the difference between `User.find_by_id(1)` and `User.find(1)`?

  * Returns by matching ID vs returns the first in a list

* What's are classes in Ruby? What are modules? And what's the difference?

  * http://learnrubythehardway.org/book/ex40.html

## Testing Questions

* What are some advantages/disadvantages to testing your code?

  * Pros; know if it works before the program becomes unmanagable.
  * Cons; takes time

* What tools would you use to test your code's functionality?

  * Rspec, because it's so readable

* What is the difference between a unit test and a functional/integration test?

  * http://stackoverflow.com/questions/4904096/whats-the-difference-between-unit-functional-acceptance-and-integration-test

* What is the purpose of a code style linting tool?

  * https://www.quora.com/What-is-the-purpose-of-a-code-style-linting-tool

* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?
  
  * e2e or end-to-end or UI testing is a methodology used to test whether the flow of an application is performing as designed from start to finish. In simple words, it is testing of your application from the user endpoint where the whole system is a blackbox with only the UI exposed to the user.

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
add = function(number1, number2) {
  return number1 + number2;
};

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
alert Hello
then alert bar is undefined

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
{n: 2};

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
'one'
'three'
'two'
## Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Do you have any pet projects? What kind?
* How do you like your coffee?
