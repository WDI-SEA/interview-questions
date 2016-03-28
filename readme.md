#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
	* Yesterday we had our first practice with white boarding, covering JS and Ruby problems.  Then we learned how to build custom filters and directives in Angular.  This week we've mainly focused on Angular, learning to incorporate it with Node, Express and MongoDB to build a full-stack MEAN app.
* What excites or interests you about coding?
	* A few different things - first, there is so much to learn and it's always continuing to grow and evolve.  After working in the same field for 9 years, diving headfirst into development has me eagerly absorbing everything I can find.  Also, you can be creative in any way that appeals to you.  Visually with front end design, back end designing complicated backend schemas, combining both or finding totally new areas that you haven't yet experienced.  Finally, the excitement and passion of the development community - I have yet to talk to a developer who hasn't been excited to talk to me about what they do and enthusiastic to encourage me to continue to learn.
* What is a recent technical challenge you experienced and how did you solve it?
	* Bankly DB schema - after a day of reviewing, getting feedback, and setting up - having to revert back after realizing that homepage data wasn't accessible with current schema.  Would walk through each step and trace through the schema before building to ensure it's accessible.
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
	* Hide API keys using .env files.  Hash passwords using a program like Bcrypt, and use Auth to ensure that only authorized users can see protected content.  Think about designing mobile first and building up from there, to ensure experience is great for lowest common denominator.  Use semantic code for both ease of reading and SEO optimization - ex: h1 should say what that page is about.
* Talk about your preferred development environment.
	* I prefer to develop on a Mac system, utilizing Sublime as my text editor and Chrome as my tools of choice.  Version control is performed through Git and Github, and interfaced with through the Bash terminal on Mac.
	* Follow-up: How do I create snippets in Sublime Text?
* Which version control systems are you familiar with?
	* Familiar with Git and Github to both manage personal work as well as coordinate on group projects.  Experienced acting as gitmaster for group work to manage and resolve conflicts on multiple feature branches for a 4-person project.
* Can you describe your workflow when you create a web page?
	* Before coding, it's important to have a wireframe or outline of what you're building, why, and what you want to achieve.  Small details aren't so important yet as they are likely to change, but having an idea of what content will be included and generally where it will go is a good start.  I like to start with a basic HTML structure, load in any scripts and stylesheets and then test each individually to ensure there are no problems from the start.  From there, filling out the content with first any static HTML to start to see the structure take shape.  If a full-stack app, this is a good time to build out and populate the databases as needed, so that you can load any content from the backend into the front end.  With content in place, working on javascript interaction and finishing with styling.
* If you have 5 different stylesheets, how would you best integrate them into the site?
	* Take advantage of the cascade by loading any custom/over-arching styles last, and work backwards from there to ensure any styles that are dependent on previous stylesheets are loaded in after those.  If none of the above apply, I would organize them in a way that makes the most sense to the site - following the contextual flow of the site.
* Can you describe the difference between progressive enhancement and graceful degradation?
	* Progressive enhancement is mobile-first programming, making the best possible experience for smaller screens and adding to this to expand upon this experience for desktop.  This ensures that no essential features are left out for some users, and that no experience is an afterthought.  Graceful degredation is the opposite approach, desktop-first, which designs a website/app to take full advantage of and look best on a full screen, and then removes features and design as needed in order to work on mobile.  This leaves a subpar experience for mobile users and can lead to unexpected consequences when trying to scale things down.
* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
	* Create an html <div> as a placeholder element for the images, use CSS to position and size it as needed, as well as to set several different classes with the slideshow images as a different background-image for each class.  Finally, use JS to either set up a click event listener or to set an interval to cycle through an array of the different CSS classes and set the class property of the div from one class to the next.
* If you could master one technology this year, what would it be?
	* Vanilla javascript - it can be applied to front end and back end development, and allows you to implement and fully understand features made easier through libraries like jQuery.
	* Show enthusiasm, a desire to learn this anyways on your own
* Explain the importance of standards and standards bodies.
	* Standards help foster progression by ensuring people are using the same best practices and identifying room for improvement.  They help teamwork by making it easier for someone to pick up another developer's code and understand what they were doing and why they did it that way.  They help to keep code clean by reducing the need for extra explanations in the notes.
	* Ex: Internet Explorer not following the standard norms other browsers use

## HTML Questions

* What does a `doctype` do?
	* This tells the browser which type of HTML to render.
* What's the difference between HTML and XHTML?
	* XHTML is the older version of HTML, standing for 'extended HTML' - XHTML was an attempt to make HTML and XML parse the same way, and it has largely been dropped
* What are `data-` attributes good for?
	* A way to attach custom data to HTML elements for the front end
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
	* A cookie is a token stored on a user's computer which allows websites to remember things about the user so that certain information on a page does not need to be loaded again - it is sent to the server with every request.  Session storage is remembering a user's log-in state, and is a temporary token that can be deleted to log out the user.  Local storage is memory that persists between page loads, allowing a website to remember information such as variables even if a page is refreshed.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
	* CSS typically loads quickly and affects the look of a page, so you want that to render before the content loads so the page looks correct when it loads up.  Scripts can take longer to load, especially on slow connections or if there is lots of code, and so you don't want a user waiting to see anything on the page while JS loads - they can see the content and if need be proceed without the javascript.  An exception in Angular, as it does affect the way a page looks and the content of the page - in this case, the script tags are moved into the head to load before the content.

## CSS Questions

* What is the difference between classes and IDs in CSS?
	* Classes can apply to many elements, whereas IDs are unique to one element only.  Elements are the most specific when applying styling, so targeting an element by its ID will overwrite any styling the element may have inherited by its class.
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
	* Resetting removes all default styling, whereas normalizing sets the styling to a default setting regardless of the browser.  I would use normalize as it ensures a more consistent experience for the user regardless of the browser they're using and allows you to keep the useful normal styling settings.  http://codepen.io/zachwolf/details/bdZMZj 
* Describe Floats and how they work.
	* Floats take an element out of it's normal position and push it all the way to one side or the other, until it hits another floated element.  It also allows content to flow around it, similar to a photo with text flowing around it in a newspaper column.
* Describe z-index and how stacking context is formed.
	* Z-index allows you to layer content on top of each other, with a base of 0 - elements with higher number will be displayed in front of/on top of elements with smaller numbers.
* Have you ever used a grid system, and if so, what do you prefer?
	* I have used grid systems with Bootstrap, Materialize, Flexbox, and very briefly with the 960 grid system.  I do like using grids as they make it quick and easy to position elements accurately, and provide responsive sizing automatically.
* Have you used or implemented media queries or mobile specific layouts/CSS?
	* I have used media queries for my own projects to ensure the design remains clean for smaller screens down through mobile.  
* How do you optimize your webpages for print?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
	* Utilize Google fonts by linking to the CDN in the head of the file and implementing the font in the CSS file
* Explain how a browser determines what elements match a CSS selector.
	* Browser goes through each CSS file in the order that they're linked, attaching styles to tagged elements, classes, and IDs
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
	* The box model is a way of splitting up then content of a page into separate sections such as the Head, Main, Aside, Footer.  
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
	* block, inline, inline-block
* What's the difference between inline and inline-block?
	* Inline puts the element right next to the previous and following elements, inline-block does the same but also keeps properties of a block element such as margin and padding
* What's the difference between a relative, fixed, absolute and statically positioned element?
	* Relative takes an item out of normal flow and moves it relative to where it would normally go, 
	 * fixed makes an item stay in the same place on a page even when scrolled,
	 * absolute positions an item relative to the containing parent element (or the Body tag)
	 * Static is the default, usually not specified - it is normal placement
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
	* Styles are assigned in order that they appear in a CSS file, in the order that the CSS files are linked in the HTML, and in order of element-class-ID.  You can use them to your advantage by 
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
	* I have used Bootstrap and Materialize several times in production as well, as well as Foundation in production.  
* Have you played around with the new CSS Flexbox or Grid specs?
	* No
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
	* No
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
	* Pros - CSS animations are quick and allow you to group style and animation effects together in the CSS. They are less customizable than Javascript.

## JS Questions

* Explain event delegation
	* Event delegation is the practice of adding an event listener to a parent element and identifying any element inside that parent that is clicked, rather than having to add individual event listeners to each child element.
* Explain how `this` works in JavaScript
	* This is a keyword that lets you reference the item you're currently working with inside of a function.
* Explain how prototypal inheritance works
	* Every item is a type of object and inherits certain properties and methods from this prototype.  For instance, all arrays have a method of .length() 
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
	* It is called ternary because it has three parts - the test variable, a result if true and a result if false.
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
  * How would you go about checking for any of these states?
  	* Undeclared variables don't exist yet
  		* typeof var === undeclared
  	* undefined variables exist but don't have anything assigned to them
  		* var varName === undefined
  	* null values do exist with a value of null.
  		* var varName === null
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
	* Anonymous functions can be called immediately in order to protect data - they do not exist outside of the function.
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
	* The first defines a function called Person that doesn't do anything yet.
	* The second creates a variable called person and sets it to the return value of a function called Person.
	* The third is treating Person as a constructor and setting person to that object.
* What's the difference between `.call` and `.apply`?
	* apply lets you call a function and pass arguments in an array, call requires each argument passed explicitly
* Explain `Function.prototype.bind`.
	* Let's you keep the value of "this" from one function to reference elsewhere
* What's the difference between feature detection, feature inference, and using the User Agent string?
	* Feature detection means writing out a JS test that tests for the presence or absence of that particular feature.  EX: not all browsers have localStorage
	* Feature inference tries to make logical deductions for what features are available
	* User Agent string looks at this and makes a guess at what's available
* Explain AJAX in as much detail as possible.
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
  	* EJS tags?
* Explain "hoisting".
	* Javascript by default "hoists" any declared variables to the top of their scope, so if a variable is declared later than it is defined javascript will know of the variable already. Similarly, calling a function at the top of the code but defining the function later down in the code will work due to the hoisting.
* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* What is the difference between `==` and `===`?
	* Strict equals === will check for the same data type and not just the same value
* Explain the same-origin policy with regards to JavaScript.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
	* Promises organize things a little better and avoid callback hell.  That said, promises require a promise library - otherwise you're stuck using callbacks.
* What tools and techniques do you use debugging Javascript code?
* What language constructions do you use for iterating over object properties and array items?
	* for _ in _ loop will iterate through objects and array to find key/value pairs

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.
	* Users (id, email, password, name) -= 

## Ruby/Rails
* What are ruby gems?
* What is the difference between a symbol and a string?
	* symbol : takes up less memory as it is created once and then referenced each time it comes up in the code.  String "" is recreated each time and so is duplicated in memory.
* What is the difference between a class method and an instance method?
	* An instance method @ can be passed through to the view
* What is the difference between local variables, instance variables, and class variables?
	* Local variables do not exist outside of the function, instance variables @ can be passed through the controller to the view, and class variables exist within the entire class so all methods can reference them
* What is a range?
	* Range is a way to tell Ruby to include numbers from the first number up to the second number [1..10] or up to & including the second number [1...10]
* In ruby, what does attr_accessor do?  
	* This gives access to both read and write values of an object
* What is the purpose of environment files under the config folder in Rails? (development, test, production)
	* These let you set up your environments separately for running code locally vs what will actually be pushed to deployment 
* What is the purpose of the application.rb file in Rails?
* How can you define a constant?
	* @@
* What is the purpose of `yield`?
* How do you store API keys when creating an app?
	* save them in the .env file and then simply put the reference to them in your app
* How do I send parameters through a url?
* Explain MVC
	* Model/View/Controller is a way to split and organize code that deals with what the user sees, the actual database in the backend, and the code connecting the two
* What is a `before_action`? When would you use it?
	* This runs before any of the routes are even accessed - useful for protecting data with restricted access so that someone cannot go directly to a URL and access it
* What do controllers do in rails?
	* Pass data through to the view
* What is RESTful routing?
	* standard of organizing an app with routes to show all items, show a certain item, edit & delete, etc
* What is a polymorphic association?
* What are params?
	* 
* How do I make a migration to add a column in Rails?
	* rails g add_something_to_table user:string, rake db:migrate
* What is CSRF? How does Rails protect an app against this?
	* Cross Site Request Forgery - server gives the client a one-use-only token that changes every time the server serves up a new page, so that harmful servers can't inject code without having the token.
* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
	* First finds the user with the id of 1, second finds the first user
* What's are classes in Ruby? What are modules? And what's the difference?

## Testing Questions

* What are some advantages/disadvantages to testing your code?
	* Advantages - break code down into small verified pieces that you build up on, knowing that each piece works so you don't have to go back to find an error after writing a big chunk of code.  Also keeps a trail for later developers to follow and test at any point.
	* Disadvantages - doubles the amount of work as you first need to write the tests, then solve and run them, before moving onto the next code.
* What tools would you use to test your code's functionality?
	* Mocha is what I'm most familiar with.
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?
	* To highlight potential errors/bugs in your code
* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

* 1020

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

* var add = function(a, b) {
	return a + b;
  }

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

 * "hoglasagnaai'm"

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

* Hello World / Hello bar

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

* 2 [1, 2]

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

* {n: 2}
* ACTUALLY returns undefined -?

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

* one three two

## Fun Questions:

* What's a cool project that you've recently worked on?
	* AdventureTo - it really got me excited about front end design, pushing my creative eye, but also about traveling and planning out my trips for the year!
* What are some things you like about the developer tools you use?
	* syntax highlighting - coming into coding it seems like it's a bunch of senseless letters, but even just adding color instantly helps to make sense of it all.  I don't know how people could code without this!
* Do you have any pet projects? What kind?
	* I love photography, and am always looking to improve my photo portfolio.  I've used a few different sites, currently hosting my pictures on SmugMug with one of their templates but am looking forward to rebuilding it from the ground up to not only showcase my images but also my developer skills.
* How do you like your coffee?
	* Vanilla latte, for here in the biggest mug you've got.
