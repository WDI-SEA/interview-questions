#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
Yesterday we learned about OAuth for facebook integration into Ruby on Rails by using the Facebook API foreign key. This continued to help us understand the database of authorization (username and password). 
* What excites or interests you about coding?
I love the felxibility and creativity involved in coding. There is creativity in every choice made, not only in front end but in the choice and approach in solving problems with methods / functions in various languages. How you approach those changes directly impacts the scale and speed of the page loading while also providing insight into your approach
* What is a recent technical challenge you experienced and how did you solve it?
Recently, in the deployment of the second project on Heroku, I had a lot of issues with the API key for Google places. It kept throwing an error for the authorization of the page.

It took several stages of troubleshooting where I first started out with the heroku app authoriazation with designated URLS then the corresponding URLs in the API key authorizations. This was very tedious, but I first started more broad (generic vs specific paths) as well as slowly altering my concatincation / hard coding of my API key into my script (which is usually frowned upon). 

Stack overflow had many entries with similar authorization errors so I used that resource to eliminate various possible sorces (such as the env file). Ultimately it was a lot of general trial and error based around peer feedback. 

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?

UI is crucial in the success of a website; it is the most high level success of the site or app because ultimately people will not use it if it exhibits lags / glitches or has a flawed/ hard to understand user experience. (If you bring a horse to water, you can't get them to drink if they don't know where the water is or if they don't trust that it is safe to drink). This leads to Security. If users are supposed to create an account with a password and other personal inforation(SS or credit card information), you want to make sure that you have proper encryption processes (like bcrypt) to ensure that the user database can not be compromised. Performance is also very important and linked to the UI as people will not be inclined to use your site if it uses a lot of RAM or noticable lags in page loads. 


* Talk about your preferred development environment.

Due to the aforementioned issues with deployment on Heroku with my API, I much prefer using GitHub pages for deplopment. Working on a seperate branch is easily integrated into my already regular commits and pushes. 

That being said, I have not yet used GitHub Pages with the backend so I am curious as to that expereince. I am very curious how this will go with the third Project and will likely help me better decide my preferred development environment.

* Which version control systems are you familiar with?

Revision control manages changes to a set of data over time. These changes can be structured in various ways. I am familiar with Git and Github as a VCS. 

* Can you describe your workflow when you create a web page?

When creating a web page, the first thing that I determine is the MVP which I then wireframe so that I have a basic understanding of the UI, and basic pages and technologies needed. From there I do the basic forms, scripts, routes to get the flow of the site and the database integraiton is working before I then move into styling and optimization of my code (with DRY & CRUD).


* If you have 5 different stylesheets, how would you best integrate them into the site?

When determining the order of styleheets there are several things to consider:


If you aren't dynamically loading scripts or marking them as defer or async, then scripts are loaded in the order encountered in the page. It doesn't matter whether it's an external script or an inline script - they are executed in the order they are encountered in the page. Inline scripts that come after external scripts have are held until all external scripts that came before them have loaded and run.

Async scripts (regardless of how they are specified as async) load and run in an unpredictable order. The browser loads them in parallel and it is free to run them in whatever order it wants.

Therefore it is important to identify what needs to be loaded first and have that as the first stylesheet. 

Generally speaking we can say that all the styles will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:

  1.Inline style (inside an HTML element)
  2.External and internal style sheets (in the head section)
  3.Browser default





* Can you describe the difference between progressive enhancement and graceful degradation?

Graceful Degradation starts at a ideal user experience level and decreases depending on user agent capabilities down to a minimum level, catering for agents that don't support certain features used by the baseline.

Progressive Enhancement starts at a broad minimum user experience and increases depending on user agent capabilities up to a more capable level, catering for agents that support more advanced features than the baseline.

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).

  Similar to when I created the Reddit slideshow, I would use an AJAX call with Javascript to pull the images (much easier than having to integrate a search query) and then set a time interval for when the images will be alternated on the page creating the slideshopw effect. 


* If you could master one technology this year, what would it be?

  I think I would like to fully master Javascript by the end of this year becuase it is the most universal language for a Full stack developer. It also seems to be optimized for many browsers and represents a syntax very useful and adaptable in many languages -- the concept of  seeing all data on a page as an object with various attributes that can be accessed, changed, etc. 


* Explain the importance of standards and standards bodies.

## HTML Questions

* What does a `doctype` do?

The doctype declaration should be the very first thing in an HTML document, before the tag. The doctype declaration is not an HTML tag; it is an instruction to the web browser about what version of the markup language the page is written in. The doctype declaration refers to a Document Type Definition (DTD)


* What's the difference between HTML and XHTML?
XHTML is stricter than HTML and XHTML is supported by all major browsers.

Unique elements of XHTML:
  XHTML DOCTYPE is mandatory
   The xmlns attribute in <html> is mandatory
    <html>, <head>, <title>, and <body> are mandatory
  XHTML elements must be properly nested
  XHTML elements must always be closed
  XHTML elements must be in lowercase
  XHTML documents must have one root element
  XHTML Attributes
  Attribute names must be in lower case
  Attribute values must be quoted
  Attribute minimization is forbidden


* What are `data-` attributes good for?


* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.

LocalStorage and sessionStorage are relatively new APIs (meaning not all legacy browsers will support them) and are near identical (both in APIs and capabilities) with the sole exception of persistence. sessionStorage (as the name persists) is only available for the duration of the browser session (and is deleted when the window is closed) - it does however survive page reloads. 

Cookies, these can be trivially tampered with by the user, and data can also be read from them in plain text - so if you are wanting to store sensitive data then session is really your only option. If you are not using SSL, cookie information can also be intercepted in transit, especially on an open wifi.


* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

Generally speaking, it is a good idea to have the CSS link / stylesheet to be in the head of the HTML document before the body tag so that the page styling first and before any of the other content on the page. 

The only exception to the rule of thumb that CSS stylesheets are placed in the head of the page is:

Besides the validation point, one caveat that might interest you when using style on the body is the flash of unstyled content. The browser would get elements that would be styled after they are displayed, making them shift on size/shape/font and/or flicker. It is generally a sign of bad craftsmanship. Generally you can get away with putting style anywhere you want, but try to avoid it whenever it is possible.

HTML5 however introduces a scoped attribute, which allows style tags to be included everywhere in the body. The impact of those styles is restricted to the style's parent-element and all it's child-elements.

## CSS Questions

* What is the difference between classes and IDs in CSS?

  Unlike the id selector defined by # in the CSS, the class selector is most often used on several elements. This allows you to set a particular style for many HTML elements with the same class. The class selector uses the HTML class attribute, and is defined with a "." A simple way to look at it is that an id is unique to only one element.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

Here are the notable differences between Reset and Normalize CSS:

  1. Normalize.css preserves useful defaults rather than "unstyling" everything. For example, elements like sup or sub "just work" after including normalize.css (and are actually made more robust) whereas they are visually indistinguishable from normal text after including reset.css. So, normalize.css does not impose a visual starting point (homogeny) upon you. This may not be to everyone's taste. The best thing to do is experiment with both and see which gels with your preferences.
  2. Normalize.css corrects some common bugs that are out of scope for reset.css. It has a wider scope than reset.css, and also provides bug fixes for common problems like: display settings for HTML5 elements, the lack of font inheritance by form elements, correcting font-size rendering for pre, SVG overflow in IE9, and the button styling bug in iOS.
  3. Normalize.css doesn't clutter your dev tools. A common irritation when using reset.css is the large inheritance chain that is displayed in browser CSS debugging tools. This is not such an issue with normalize.css because of the targeted stylings.
  4. Normalize.css is more modular. The project is broken down into relatively independent sections, making it easy for you to potentially remove sections (like the form normalizations) if you know they will never be needed by your website.
  5. Normalize.css has better documentation. The normalize.css code is documented inline as well as more comprehensively in the GitHub Wiki. This means you can find out what each line of code is doing, why it was included, what the differences are between browsers, and more easily run your own tests. The project aims to help educate people on how browsers render elements by default, and make it easier for them to be involved in submitting improvements.

  Therefore I would use Normalize for the documentation as well as the fact that it doesn't have the common bugs that Reset does.


* Describe Floats and how they work.

  Floats are part of the CSS box model. The float property specifies whether or not a box (or an element) should float; essentially, it determines whether text will be wrapped around the element.

  Floated elements remain a part of the flow of the web page. This is distinctly different than page elements that use absolute positioning.

  There are four valid values for the float property. "Left" and "right" float elements those directions, respectively. "None" (the default) ensures the element will not float and "inherit" which will assume the float value from that elements parent element.

  The clear property is used to control the behavior of floating elements.

  Elements after a floating element will flow around it. To avoid this, use the clear property.

* Describe z-index and how stacking context is formed.

The z-index property in CSS controls the vertical stacking order of elements that overlap. As in, which one appears as if it is physically closer to you. z-index only effects elements that have a position value other than static (the default).


* Have you ever used a grid system, and if so, what do you prefer?

Yes, I have used a Grid system with Bootstrap. This is a great shortcut if you have a complex page with many elements to be styled relationally on the page (several images / buttons, headers, etc).


* Have you used or implemented media queries or mobile specific layouts/CSS?

I have implemented several media queries, specifically with images / thumbnails or links with a AJAX call. This allows whatever query is entered into a search box, ran and pulling any objects meeting that criteria. 

I implemented a mobile specific layout in my second project because my primary user stories were people on the go, likely to access the app on their mobile device. Thus, the page and UX was oriented to the much smaller screen size. 



* How do you optimize your webpages for print?


* What are the advantages/disadvantages of using CSS preprocessors?

  Disadvantages:

  1. One thing you can find with preprocessors is that you end up with vast outputs of css due to the nesting. On a small project it is easy to keep under control, on a large project with multiple developers it takes discipline to keep the amount of css generated under control.

  2. Due to having a compilation step, the browser is not interpreting the source files, meaning the CSS line numbers are now irrelevant when trying to debug. This makes debugging a lot harder.


  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?

    I would make sure to provide a detailed font family so that if a user accesses the website on a browser that doesnt have the font, there is at least one similar option to avoide defalting to the stand font. 

* Explain how a browser determines what elements match a CSS selector.


* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

  All HTML elements can be considered boxes. Even if you see a circle, it's living within a box.
  The CSS box model describes this principal - a box wraps around all HTML elements, and it consists of: margins, borders, padding, and the actual content. This model allows us to place a border around elements and space elements in relation to other elements.
  With CSS properties and values, it is possible to apply specific styles to each of these elements, and change the way they behave and/or display on the page.

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?


* List as many values for the display property that you can remember.


* What's the difference between inline and inline-block?

  An inline element has no line break before or after it. This makes the element sit on the same line as another element, but without formatting it like a block. It only takes up as much width as it needs (not the whole line). Inline places all your elements on a single line. The bad news is that it doesn't maintain their "box"ness

  An inline-block element is placed as an inline element (on the same line as adjacent content), but it behaves as a block element. This makes the element a block box but will allow other elements to sit next to it on the same line.


* What's the difference between a relative, fixed, absolute and statically positioned element?
  A page element with "relative positioning" gives you the control to "absolutely position" children elements inside of it.

  The "absolutely positioned" elements are positioning themselves in relation to the body element, instead of their direct parent. So if the browser window grows, that element in the bottom left is going to stick with the browser window, not hang back inside, like it was the case in the previous example.

  Declaring position:relative allows you to position the element top, bottom, left, or right relative to where it would normally occur.

  A "static positioned" element is always positioned according to the normal flow of the page and are not affected by the top, bottom, left, and right properties.
  
  Again, the default positioning for all elements is static. This means that no positioning has been applied and the elements occurs where they normally would in the document.

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?


* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?

  I have used Bootstrap framework for several websites and apps (locally and in production).

  I love its built in widgets (modals, flash messages) and the grid system makes it much easier to quickly create responsive websites with the grid system. I would like it to be a little bit more customizeable, it is a little limited in the styling options of its page elements and widgets. 


* Have you played around with the new CSS Flexbox or Grid specs?

  No I have not but plan on learning it soon. 

* Have you ever worked with retina graphics? If so, when and what techniques did you use?

  No I have not worked with Retina Graphcis. 

* Explain some of the pros and cons for CSS animations versus JavaScript animations.
  There are two primary ways to create animations on the web: with CSS and with JavaScript. Which one you choose really depends on the other dependencies of your project, and what kinds of effects you're trying to achieve

  Use CSS animations for simpler “one-shot” transitions, like toggling UI element states.
  Use JavaScript animations when you want to have advanced effects like bouncing, stop, pause, rewind or slow-down.

## JS Questions

* Explain event delegation

  JavaScript event delegation is a simple technique by which you add a single event handler to a parent element in order to avoid having to add event handlers to multiple child elements.

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
