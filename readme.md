#Interview Prep 

## General Questions

* What did you learn yesterday/this week?
  We leanred about Angular witch is a Javascript framework. We also learned how to use it along with Mongo. Mongo is a database oragnizer that uses JSON esque "document" items instead of tables. 

* What excites or interests you about coding?
  I particularly love front end development. Being the creative visual person that I am , I really feel like I can express myself in this art form. 
  I also am keen to the fast paced environment coding falls into. There is ALWAYS something new on the horizon for us all to learn.

* What is a recent technical challenge you experienced and how did you solve it?
  I would have to say this whole General Assembly experience was a challenge. Before this coarse I had minimal tech experience, and jumping head first into this immersive has been quite the task. I have learned that there are multiple ways to get answers to MOST things, and a wide variety of resources to do so. Best tip? It's OK to not know. Figuring it out is the fun part. 

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
  I'd partner with a back end developer to ensure my site as safe and all bases we're covered. Learning along the way areas of importance. 


* Talk about your preferred development environment.
  I would want to be in a learning environment. With plenty of mentors who are patient and understanding. I would also love to be in a team oriented environment as well, I thoroghly enjoy working with others. 

* Which version control systems are you familiar with?
  We have utilized GIT througout the entire coarse. 

* Can you describe your workflow when you create a web page?
  First I come up with the idea, if it hasn't been provided with me. Really get into who it it for, what will it do, when ( time frame, launch time) , and most specifically all the Why's. This creates the user stories and then I can wire frame all views and database schema if needed.
  Then I start coding the bare bones of the page(s) testing along the way to make sure everything is working correctly. After the bare bones is set up I'll initatie the basic functionality of each site and work on styling along with it.  (Styling is importmant to me and can move around a lot on the page once there are moving parts.)
  I map out tasks that need to be done and think of any things to add/ fix and put them on the list, and error catch along the way. 
  Constant commits, and pushes to save my work.
  Lots of assistance when I need help. 

* If you have 5 different stylesheets, how would you best integrate them into the site?
  (ASK THIS IN CLASS how to link many different pages for complex sites)
  I would combine the CSS into one folder and have it very organized with comments, etc for reference. (Todd mentioned an program that can eaily combine files for you.)

* Can you describe the difference between progressive enhancement and graceful degradation? 
  Nope. But let me goole! Hold please...
  Progressive enhancement is a strategy for web design that emphasizes accessibility, semantic HTML markup, and external stylesheet and scripting technologies.
  Graceful degradation is the ability of a computer, machine, electronic system or network to maintain limited functionality even when a large portion of it has been destroyed or rendered inoperative. The purpose of graceful degradation is to prevent catastrophic failure.
  --With that being said I really don't understand. I can kinda grasp that that progressive enhancement is slowly adding features and staying organized?

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
 I would use the Bootstrap carosel! 

* If you could master one technology this year, what would it be?
  Hands down JavaScript, seems to be the grandaddy of all languages and once you have that, others can come easily. 

* Explain the importance of standards and standards bodies.
  By folowing these standards websites can display things correctly and unformly across different platforms.
  Helps de-bug, and makes the lagnuage universal to all who look at the code. 

## HTML Questions

* What does a `doctype` do?
  Tells the web browser what language the page is using.

* What's the difference between HTML and XHTML?
  

* What are `data-` attributes good for?
  It's good for storing a variable within an html element. (ASK MORE DURING CLASS, NOT FAMILIAR)

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
  Have no clue review below:
  Definition of: cookie. cookie. A small text file (up to 4KB) created by a Web site that is stored in the user's computer either temporarily for that session only or permanently on the hard disk (persistent cookie). Cookies provide a way for the Web site to recognize you and keep track of your preferences.

  sessionStorage is similar to Window.localStorage , the only difference is while data stored in localStorage has no expiration set, data stored in sessionStorage gets cleared when the page session ends. A page session lasts for as long as the browser is open and survives over page reloads and restores

  The localStorage property allows you to access a local Storage object. localStorage is similar to sessionStorage . The only difference is that, while data stored in localStorage has no expiration time, data stored in sessionStorage gets cleared when the browsing session ends—that is, when the browser is closed.

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
  It's better for page loading.

## CSS Questions

* What is the difference between classes and IDs in CSS?
  Classes can apply to multiple html tags. Ids are one intance. 

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
  I don't know this question but found a good asnwers for review here:

  http://stackoverflow.com/questions/6887336/what-is-the-difference-between-normalize-css-and-reset-css

* Describe Floats and how they work.
   A float takes an element and puts it left or right of it's container where other elements will wrap around it. 

* Describe z-index and how stacking context is formed.
  It's the stack order of elements on a page.
* Have you ever used a grid system, and if so, what do you prefer?
   I haven't used a grid system.
   (ASK IN CLASS is BOOTSTRAP COLUMNS A GRID SYSTEM?)

* Have you used or implemented media queries or mobile specific layouts/CSS?

* How do you optimize your webpages for print?

* What are the advantages/disadvantages of using CSS preprocessors?
  Study source: https://drupalize.me/videos/what-css-preprocessor?p=1175
  It is an extension of CSS? 

  * Describe what you like and dislike about the CSS preprocessors you have used.
  I have used SASS and locating the documentation I needed for easy things was difficult.

* How would you implement a web design comp that uses non-standard fonts?
Study source: http://stackoverflow.com/questions/7717734/using-non-standard-font-in-web-pages
  @font-face {
    font-family: MyFont;
    src: url('MyFont.otf');
}
 Download the font, and provide source, not always supported. 

* Explain how a browser determines what elements match a CSS selector. (ex: Id, class)

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
The CSS Box Model. All HTML elements can be considered as boxes. In CSS, the term "box model" is used when talking about design and layout. The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.
(DOesn't the browser automatically render things in boxes, it's default.)

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
The box-sizing property is used to tell the browser what the sizing properties (width and height) should include.
 
http://www.w3schools.com/cssref/css3_pr_box-sizing.asp

Should they include the border-box? Or just the content-box (which is the default value of the width and height properties)?
 It depends doesn't it? 

* List as many values for the display property that you can remember. SOURCE: http://www.w3schools.com/cssref/pr_class_display.asp`
Inherit 
inline
block
inline-block 
flex

* What's the difference between inline and inline-block?
   inline-block displays an element as an inline-level block container. The inside of this block is formatted as block-level box, and the element itself is formatted as an inline-level box

   inline  is Default value. Displays an element as an inline element (like <span>)

   block  Displays an element as a block element (like <p>)

* What's the difference between a relative, fixed, absolute and statically positioned element?
source: http://www.w3schools.com/css/css_positioning.asp

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
(WHAT?)

* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
I have not. Check this out :
http://www.noupe.com/essentials/freebies-tools-templates/5-popular-css-frameworks-tutorials-tools-for-getting-started.html

* Have you played around with the new CSS Flexbox or Grid specs?
Flex box has come in handy. 
https://css-tricks.com/snippets/css/a-guide-to-flexbox/

* Have you ever worked with retina graphics? If so, when and what techniques did you use?
Say WHAT?

* Explain some of the pros and cons for CSS animations versus JavaScript animations.
   I personally am more comfortable with CSS animations.
   https://developers.google.com/web/fundamentals/design-and-ui/animations/css-vs-javascript?hl=en

## JS Questions

* Explain event delegation
  https://learn.jquery.com/events/event-delegation/

* Explain how `this` works in JavaScript 
  (don't know)
  In JavaScript, the thing called this, is the object that "owns" the JavaScript code. The value of this, when used in a function, is the object that "owns" the function. The value of this, when used in an object, is the object itself. The this keyword in an object constructor does not have a value.
  (from W3 schools)

* Explain how prototypal inheritance works
  (don't know)
  Prototype-based programming is a style of object-oriented programming in which behaviour reuse (known as inheritance) is performed via a process of cloning existing objects that serve as prototypes. This model can also be known as prototypal, prototype-oriented, classless, or instance-based programming.

* Why is it called a Ternary expression, what does the word "Ternary" indicate?
  A ternary operator is an operator that takes three arguments. 
  Because the word itself means three parts

* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
   null is no value
   Undefined means you haven't declared a variable
   Undeclared means you have a vaiable that isn't defined

  * How would you go about checking for any of these states?
    use the console.log function

* What is a closure, and how/why would you use one?
  don't know
  http://javascriptissexy.com/understand-javascript-closures-with-ease/

* What's a typical use case for anonymous functions?
  don't know
  http://www.w3schools.com/js/js_function_definition.asp

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
  don't know

* What's the difference between `.call` and `.apply`?
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/call
  The call() method calls a function with a given this value and arguments provided individually.

  The apply() method calls a function with a given this value and arguments provided as an array (or an array-like object).
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/apply

* Explain `Function.prototype.bind`.
  The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/bind

* What's the difference between feature detection, feature inference, and using the User Agent string?

* Explain AJAX in as much detail as possible.
  
  Ajax is a client-side script that communicates to and from a server/database without the need for a postback or a complete page refresh. The best definition I've read for Ajax is “the method of exchanging data with a server, and updating parts of a web page - without reloading the entire page.”

  http://www.seguetech.com/blog/2013/03/12/what-is-ajax-and-where-is-it-used-in-technology

* Have you ever used JavaScript templating?
  I don't think so?

* If so, what libraries have you used?

* Explain "hoisting".
  don't know

Hoisting is JavaScript's default behavior of moving declarations to the top.

http://www.w3schools.com/js/js_hoisting.asp


* Describe event bubbling.
  don't know

  Event bubbling and capturing are two ways of event propagation in the HTML DOM API, when an event occurs in an element inside another element, and both elements have registered a handle for that event. The event propagation mode determines in which order the elements receive the event.
  
  http://stackoverflow.com/questions/4616694/what-is-event-bubbling-and-capturing

* What's the difference between an "attribute" and a "property"?
  http://lucybain.com/blog/2014/attribute-vs-property/

* Why is extending built-in JavaScript objects not a good idea?

* What is the difference between `==` and `===`?
I know one! The == is an equals with a little bit of lee-way the === is strict equals with no "wiggle room."
For instance with a strict equals the data types MUST be the same, ie: string to sting, integer to integer.

* Explain the same-origin policy with regards to JavaScript.
  don't know
  The same-origin policy restricts how a document or script loaded from one origin can interact with a resource from another origin. It is a critical security mechanism for isolating potentially malicious documents.

  https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy

* What is the extent of your experience with Promises and/or their polyfills?
  (ASK IN CLASS MORE INFO ON POLYFILLS)
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise

* What are the pros and cons of using Promises instead of callbacks?

  http://blog.parse.com/learn/engineering/whats-so-great-about-javascript-promises/

* What tools and techniques do you use debugging Javascript code?
  console.log CONSOLE.LOG
  I know certain tests cab be written, but I don't unerstand those. 

* What language constructions do you use for iterating over object properties and array items?
  For loops?

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators


## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

## Ruby/Rails
* What are ruby gems?
  RubyGems is a package manager for the Ruby programming language that provides a standard format for distributing Ruby programs and libraries (in a self-contained format called a "gem"), a tool designed to easily manage the installation of gems, and a server for distributing them.

  http://guides.rubygems.org/what-is-a-gem/

* What is the difference between a symbol and a string?
  The truth of the matter is that Symbols are Strings, just with an important difference, Symbols are immutable. Mutable objects can be changed after assignment while immutable objects can only be overwritten. Ruby is quite unique in offering mutable Strings, which adds greatly to its expressiveness.

  http://www.reactive.io/tips/2009/01/11/the-difference-between-ruby-symbols-and-strings

* What is the difference between a class method and an instance method?
  http://culttt.com/2015/06/10/understanding-class-methods-verses-instance-methods-in-ruby/

* What is the difference between local variables, instance variables, and class variables?
  http://www.railstips.org/blog/archives/2006/11/18/class-and-instance-variables-in-ruby/

* What is a range?
  A Range represents an interval—a set of values with a beginning and an end. 
  (-5..-1).to_a      #=> [-5, -4, -3, -2, -1]
  http://ruby-doc.org/core-2.2.0/Range.html

* In ruby, what does attr_accessor do? 
  Allows you to read and write certain content?
  http://stackoverflow.com/questions/4370960/what-is-attr-accessor-in-ruby

* What is the purpose of environment files under the config folder in Rails? (development, test, production)

* What is the purpose of the application.rb file in Rails?

* How can you define a constant?

* What is the purpose of `yield`?

* How do you store API keys when creating an app?
  In a .env folder. (.env is hidden) and it's referenced with a variable in app

* How do I send parameters through a url?

* Explain MVC
  Model, View, Controller

* What is a `before_action`? When would you use it?
  Before an action is run, do this... 

* What do controllers do in rails?

* What is RESTful routing?
  BEST PRACTICE! 
* What is a polymorphic association?

* What are params?

* How do I make a migration to add a column in Rails?

* What is CSRF? How does Rails protect an app against this?

* What's the difference between `User.find_by_id(1)` and `User.find(1)`?

* What's are classes in Ruby? What are modules? And what's the difference?

## Testing Questions

* What are some advantages/disadvantages to testing your code?
  I honestly see no DIS advantages for testing one's code. Perhaps other that it being time consuming and arduous. 

* What tools would you use to test your code's functionality?
  A developer who specialized in test driven coding. :)
  (Separate folder
  )
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
})(); <--- what dat?
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
  Our hackathon was quite fun actually. I love working in groups. We were assigned  to create a M.E.A.N. app in one day. I as assigned the style of the app, and got to really focus on what I enjoy doing. It was a Spring/ Summer festival search app with a "Futurama" theme. I enjoyed being comical and quirky with my design.

* What are some things you like about the developer tools you use?
 Not sure what these are... examples?

* Do you have any pet projects? What kind?
  Pet projects?

* How do you like your coffee?
  Funny story, I didn't drink coffee till I moved here. I enjoy the Mexican Mocha from Diablo, and the White Mocha from Cafe le Fournil in Greenlake. Of coarse with an extra shot or two :)
