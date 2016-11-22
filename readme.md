#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
* *This week I learned a lot of patience with learning a new framework. The first two days were some of the hardest days I've had lately. But, after some perseverence and a full day hackathon, I felt like I had a much better grip on it as a whole.*
* What excites or interests you about coding?
* *I love the constantly changing landscape of frameworks and technologies. While it is near impossible to stay 100% on top of them as tools to utilize, I like to know what is out there that I could use to bring new products to market. Emerging tech and the ever-increasing relationship between tech and sports excites me most.*
* What is a recent technical challenge you experienced and how did you solve it?
* *The most recent challenge I experienced was with deploying a Mongo database to Heroku. Despite reading the docs and attempting to deploy on my own, I simply couldn't get it to work. After reading some more I was able to dump the local DB, but it still wouldn't push due  to some authentication issues. My instructor and I looked through some docs to deciper the automatically generated auth keys and pushed up correctly.*
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* *My first considerations are always 'what does the customer need' and 'what is the minimum needed to achieve this goal'. Ultimately, we are always trying to appease some sort of internal or external customer and we need to be sure to keep that consideration in mind at all times. We can build as many features as we want, but if it doesn't serve the primary purpose, it's all for none.*
* Talk about your preferred development environment.
* *My prefered dev environment consists of Mac OS X, Sublime Text, Chrome and various extensions including the built-in inspector. I've also played around with Visual Code Studio and Atom for code editing. For SQL I am most comfortable with PostgreSQL and MongoDB for NoSQL. I always like to have the documentation open for whatever language or framework I am using. I use Dash.app on OS X to keep documentation locally and various versions as well dependent individual projects. Slack, Telegram, Grape, Lync, TeamViewer, Gmail, and Outlook for team collaboration and communication. Git/Github for version control.*
* Which version control systems are you familiar with?
* *I am familiar with Git through Github and Heroku logs for deployment.*
* Can you describe your workflow when you create a web page?
* *I create a basic file structure for javascript and css files along with a basic html index. I setup a basic HTML structure then begin working in javascript files by setting up a basic function to verify that the structure is being read by the browser. From there I dive deeper into Javascript and use HTML as needed to check any on-page functionality. The last thing that I focus on is CSS for styling or implement as needed for any javascript related functionality.*
* If you have 5 different stylesheets, how would you best integrate them into the site?
* *More files results in more HTTP requests to the file server which, in turn, results in slower/heavier websites. I would focus on reducing any redundancies across the stylesheets and combining them into as few sheets as possible. This could break whatever pages they are tied to. Having consistent naming conventions across all pages the reduce the number of variations needed with similar styling. Last, focusing on a system of views with a consistent layout to further reduce the need for redundant code.*
* Can you describe the difference between progressive enhancement and graceful degradation?
* *Progressive Enchancement focuses on a basic user experience that is functional across all browsers and builds more advanced features for modern browsers on top of that. Graceful degradation focuses on building functionality for modern browsers and attempting to implement a lower level of user experience in older broswers.*
* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
* **
* If you could master one technology this year, what would it be?
* *I would like to master Angular. I love how flexible, lightweight, and powerful it is. It is going to be an in-demand framework for the future and I want to not only put myself forward, but my customers as well.*
* Explain the importance of standards and standards bodies.
* *Standards and standards bodies seek to ensure that technologies are able to be easily maintained cross-platform and cross-browser. In reality, they make our lives easier when jumping into projects that we are unfamiliar with. With standards, we can easiliy gather what the structure and capabilities of the site. These standards not only assist with graceful degradation, but ensure that future technologies are easily adapted to known standards.*

## HTML Questions

* What does a `doctype` do?
* *Doctype informs the browser what version of HTML is being used and is required at the top of all HTML documents.*
* What's the difference between HTML and XHTML?
* *XHTML does not have good browser support and has very strict code formatting requirements. HTML...*
* What are `data-` attributes good for?
* *Data attributes are good for embedding custom data attributes on HTML elements without making AJAX or server side calls.*
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* *These are are storage types that live on the client. LocalStorage can be used to store non-sensitive data like user preferences or game scores across multiple pages. sessionStorage is localStorage that is only good for the duration of the browser being open. These options are accessible by the user and potentially others. Cookies are small plain-text files that are typically used for encrypted authentication tokens since they can be flagged as not accessible to scripts.*
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
* *We load the CSS files first so that the browser knows how elements should be styled as they are loaded to prevent any default styling from showing to the user. We load the scripts at the end of the body to prevent the scripts from stopping the page loading content.*

## CSS Questions

* What is the difference between classes and IDs in CSS?
* *IDs can only be used on one element for specific styling. Classes can be used on multiple elements to style them all the same.*
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* *Resetting sets everything to zero/none. Normalizing takes care of differences between browsers.*
* Describe Floats and how they work.
* *Unicorns. Actually Floats force an element to one side and float any content around it if possible.*
* Describe z-index and how stacking context is formed.
* *Z-index allows you to create nested or stacked elements by having a same starting point, but different alternate points to draw elements that appear stacked.*
* Have you ever used a grid system, and if so, what do you prefer?
* *I've used both Bootstrap and Materialze. While I really like some of the new design that Materialize can offer, I find the Bootstrap system of columns and rows to be very friendly for creating mobile-first and responsive layouts.*
* Have you used or implemented media queries or mobile specific layouts/CSS?
* *Yes I have both in class projects and personal projects. Typically when grid systems aren't getting the exact results that I would like or if I don't want to use a grid system on a project.*
* How do you optimize your webpages for print?
* *Create a specific print-friendly CSS, link it with other stylesheets and add a media="print" to the link attribute.*
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
  *CSS preprocessors provide a specific syntax to provide what could be considered an advanced CSS. The preprocessor will then convert to regular CSS to render the page styling. Preprocessors typically provide some additional functionality that vanilla CSS does not provide. A disadvantage is additional language and markup that another developer may not know. Also mixins and extensions could harm maintainability of the code if you do not know the original style.*
* How would you implement a web design comp that uses non-standard fonts?
* *I would call the @font-face style and import the source and set the font-family by name. I could also import a font via a cdn like Google Fonts and call it in CSS as well.*
* Explain how a browser determines what elements match a CSS selector.
* *It checks the CSS selector against elements, IDs, classes, DOM, etc.*
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* *Padding adjusts the spacing inside of the element. Margin adjusts the spacing outside the element. Border can set and adjust the size/type of the border around the element.*
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* *This is used to change the default CSS box model used to calculate height and width. It can also be used to incorporate the CSS box model in browsers that don't support it.*
* List as many values for the display property that you can remember.
* *None, flex, block, inline, inline-block, grid, table.*
* What's the difference between inline and inline-block?
* *An inline element will always be inline while an inline-block element can take block like properties while still behaving like an inline element.*
* What's the difference between a relative, fixed, absolute and statically positioned element?
* *Static is the default and has no real affect on the element. Relative the elements default position with whatever position is defined as the value compared to other elements. Fixed does not leave space for the element and positions it in a fixed position relative to viewport and does not move when scrolled. Absolute also does not leave space for the element and positions it in a specific position relative to surrounding elements*
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* *It is first come first serve and any changes down the sheet will override any previous styling.*
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* *Bootstrap and Materialize. I would make the entire thing easier to style with CSS. Maybe adding element listings for each feature in the documentation so they can be more easily found by the end user.*
* Have you played around with the new CSS Flexbox or Grid specs?
* *Flexbox Froggy! I have also used it a bit in homework for GA to play around with it more.*
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* *I work on a retina screen so I am aware of some of the issues that come up when designing on high resolution screens and rendering them on smaller resolutions, but I have not specifically designed for both retina and non-retina screens. I have found some tools to create images for both resolution classes and tags to identify them and swap them in as needed.*
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* *CSS animations are very lightweight and can provide some basic animations that do not weigh heavy like JS animations do. But, the JS animations are more complex and provide more appealing animations.*

## JS Questions

* Explain event delegation
* *DOM event delegation is the mechanism of responding to child UI events through parent elements. It is known as bubbling.*
* Explain how `this` works in JavaScript.
* *"This" refers to the owner of the function that is being executed. If you write a funciton involving an HTML element, your "this" call would relate directly to that element.*
* Explain how prototypal inheritance works.
* *Prototypal inheritance involves objects inheriting from other objects instead of Classical in which a class inherits from another class.*
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* *It's a three part expression. Do this if True, do else if false.*
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
* *Null is when a declared variable has no value. Undefined is when a variable has no data type associated with it. Undeclared is when a variable is used but not defined.*
  * How would you go about checking for any of these states?
  * *Use if statements to check for them.*
* What is a closure, and how/why would you use one?
* *A closure is the local variable for a function. We would want to use one if we want to call or use variables within the function outside of the function.*
* What's a typical use case for anonymous functions?* 
* *To run a function that you only need once. For instance, a specific function once the page loads.*
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* *The first creates the function called person. The second sets a variable person to the Person function. The third creates a new instance of the Person function.*
* What's the difference between `.call` and `.apply`?
* *Apply allows you to invoke the function with arguments that you pass. Call requires the arguments to be listed explicitly.*
* Explain `Function.prototype.bind`.
* *The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.*
* What's the difference between feature detection, feature inference, and using the User Agent string?
* *Feature detection checks to see if a given feature exists. Inference assumes the feature exists since you've used another feature that includes or is releated to other features. User Agent strings pass along useful information about browser, OS, etc. that the client is using. With this information you know what features are supported.*
* Explain AJAX in as much detail as possible.
* *AJAX involves asynchronous queries to the server from the client. This allows queries to run in the background without inturrupting the page from loading/being functional and to load content dynamically as it becomes available.*
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
  *Yes, I have used it in Angular*
* Explain "hoisting".
* *It is Javascripts default behavior to move all declarations to the top of the current scope.*
* Describe event bubbling.
* *See event delegation answer.*
* What's the difference between an "attribute" and a "property"?
* *An attribute is a quality or object that we give something. A property is the default value of the object that doesn't require attribution.*
* Why is extending built-in JavaScript objects not a good idea?
* *It could result in event collisions with other built-in functions resulting in a messy heap to clean up. A standardized version fo your extension could also come out or a change to the current standard resulting in a break of your extension. Just use the built-in objects.*
* What is the difference between `==` and `===`?
* *== checks for equality of value. === checks for equality in value and type.*
* Explain the same-origin policy with regards to JavaScript.
* *Same origin policy limits the access of one domain to another. Don't want your slightly nefarious torrent site to have access to that bank tab you have open, right?*
* What is the extent of your experience with Promises and/or their polyfills?
* *Promises can be chained together to process after the previous process has finished. If it doesn't finish, the next process won't run. It promised you that.*
* What are the pros and cons of using Promises instead of callbacks?
* *Promises have error checking built in. Callbacks may not give you the return you're looking for resulting in user confusion.*
* What tools and techniques do you use debugging Javascript code?
* *Console logs and Chrome dev tools*
* What language constructions do you use for iterating over object properties and array items?
* *Conditional loops. For, for in, until, while.*

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

## Ruby/Rails
* What are ruby gems?
* *Packages for ruby/rails.*
* What is the difference between a symbol and a string?
* *A symbol has one occurance in memory. Strings can be repeated.*
* What is the difference between a class method and an instance method?
* *Class methods can only be called on a class. Instance methods can be called  on a specific instance of that class.*
* What is the difference between local variables, instance variables, and class variables?
* *Local variables are availble from the current environment, but not outside that environment (Like a function). Instance variables are only available within that instance like multiple functions in an instance. Class variables are accessible anywhere in a a specific class.*
* What is a range?
* *A way to count through a specific set of data. (1..10)*
* In ruby, what does attr_accessor do?
* *Sets the accessibility of a symbol variable. Write and/or Read only.*  
* What is the purpose of environment files under the config folder in Rails? (development, test, production)
* *They allow you to set specific gems for different environment. Your live site has no need for testing files that you should only be using in development. Less for the client to load results in leaner/quicker sites.*
* What is the purpose of the application.rb file in Rails?
* *Tells rails how to configure the application as a whole including all development environments.*
* How can you define a constant?
* *With an uppercase character and that constant should only be used once. Ruby will warn you when you've used it twice and the most recent version will be used creating potentially undesired effects.*
* What is the purpose of `yield`?
* *Yield allows you to branch from within a method to execute code outside of that method and then return to the method.*
* How do you store API keys when creating an app?
* *With ENV variables called from a .env file.*
* How do I send parameters through a url?
* *Key value pairs passed through an object.*
* Explain MVC
* *Model View Controller. Separating specific code into specific files to keep concise, specific action files that are tightly knitted to their specific functionality.*
* What is a `before_action`? When would you use it?
* *Action that occurs before the process is finalized. Encrypting a password before storing it as an encrypted version in your database.*
* What do controllers do in rails?
* *The controller gets objects from the database using the model to pass through to the view.*
* What is RESTful routing?
* *Routing to actions and views. Get, Show, Post, Updtate, Delete.*
* What is a polymorphic association?
* *Allow an association betwen a single attribute of the model to be drawn from for multiple other models.*
* What are params?
* *Data passed from the client to the server. Like a specific database ID for a REST request.*
* How do I make a migration to add a column in Rails?
* *rails g migration add_column*
* What is CSRF? How does Rails protect an app against this?
* *Cross Site Request Forgery. This attack method works by including malicious code or a link in a page that accesses a web application that the user is believed to have authenticated. If the session for that web application has not timed out, an attacker may execute unauthorized commands. To protect against forged requests, we use a security token that our site knows but other sites don't know. We include the security token in requests and verify it on the server. This is a one-liner in your application controller, and is the default for newly created rails applications. protect_from_forgery with: :exception*
* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
* *Find_by_id(1) will find the user with the id of 1. User.find(1) will find the first user listed in the database. This could be any user in the entire database.*
* What's are classes in Ruby? What are modules? And what's the difference?
* *A module cannot be instantiated. When a class includes a module, a proxy superclass is generated that provides access to all the module methods as well as the class methods. A module can be included by multiple classes. Modules cannot be inherited.*

## Testing Questions

* What are some advantages/disadvantages to testing your code?
* *Tests add additional development time to your project and are typically longer than your actually code to check for all potential errors. The benefit is much better written code.*
* What tools would you use to test your code's functionality?
* *Test driven development. Mocha, Chai, Rspec.*
* What is the difference between a unit test and a functional/integration test?
* *Unit testing is to test a unit in isolation. Functional/integration tests individual units in conjunction with other units.*
* What is the purpose of a code style linting tool?
* *Linting checks a written program for potential errors.*
* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?
* *End-to-end testing is a methodology used to test whether the flow of an application is performing as designed from start to finish. The purpose of carrying out end-to-end tests is to identify system dependencies and to ensure that the right information is passed between various system components and systems. It can be done in Angular using Protractor.*

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
* *The coolest project I recently worked on was a group project at General Assembly for a social ride-sharing app to leverage transport services like Lyft and Uber to split the ride and the fare. While we did not complete all functions that we aimed for, we all learned a lot and had fun working as a team dealing with new challenges we hadn't encountered before. I also served as the Repo Master and Project Manager allowing me to learn more skills that I believe suit my previous experiences.*
* What are some things you like about the developer tools you use?
* *I like that for the most part they are either open source or highly customizable with community developed plugins or extensions so that each user can create their own custom environment to suit their own needs.*
* Do you have any pet projects? What kind?
* *I've been tinkering around with Raspberry Pi off and on. Before I had kids I was an avid photographer. I love playing with my kids, craft breweries, Seattle Sports, and International Soccer.*
* How do you like your coffee?
* *I don't drink coffee any longer. I previous drank way too much. I now prefer Black tea. Market Spice is my local favorite souce. Usually straight black, but occasionally with a bit of sugar and lemon and/or honey.*
