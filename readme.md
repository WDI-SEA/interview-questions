#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week? <br/>
  For the past 7 months I have taken two separate courses at General Assembly. My first course, Front-end Web-Development helped strengthen my skills within HTML, CSS, JavaScript and jQuery. After finishing this 10-week course, I decided to continue my education in web-development and signed up for a full-time, 12 week, web-development immersive course. This program not only teaches front-end frameworks but back-end frameworks as well. Throughout this course I have strengthened my skills in Node.js along with Express, as well as Ruby, Ruby on Rails, Angular.js, and React.js. This week specifically I focused on Angular.js and building responsive api's. <br/>
* What excites or interests you about coding? <br/>
  Coding to me is like working through a math problem and that’s what excites me the most about it. Each line of code is like an algorithm and you have to write the algorithm for a desired output. Ever since I was little math has always been my favorite subject. Coding is just like a math equation and will have a definitive answer with your given variables, you just have to figure out the right algorithm. It's like a puzzle to me and that’s what interests me the most, there is always a right answer or final output that you desire. <br/>
* What is a recent technical challenge you experienced and how did you solve it?<br/>
  A recent technical challenge that I experienced was within Ruby. A method that I was trying to write wasn't giving me the expected output. Taking things back to the basics, I went through the code line by line and just like a math problem, I went through my algorithm in segments to find where I went wrong. After some console.logs I was able to pin point the exact area within my code that was not giving me the expected output. The problem was a syntax error and I was thinking in terms of JavaScript and not ruby. <br/>
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?<br/>
There are many UI, Security, Performance, SEO, Maintainability or Technology considerations that you should think about while building a web application or site. This answer could be an extremely long essay, but I will give some of the basics. In terms of user interface, a website should be easy to navigate and aesthetically pleasing to your user. This is why it is very important to ask your self the most fundamental question, who is my consumer? Once you can pin point your consumer and there likes and dislikes, building a website geared towards that user will be much easier. For all consumers though, making sure that you have active components within your web page is something you should consider, so the user knows that the website is working. This could be simple animation while loading that lets the user know the website is active. It is also very important your website is mobile-first because 60% of Americans access the internet through their phone. If you don't build your website mobile first your losing over half of your potential consumers. <br/>
<br/>
In todays day and age, security is extremely important because of all the hackers that try and access people's information through your website. Keeping user information encrypted is vital to the success of your website. From a web-developers perspective it is also important to keep code that your do not want the user to access in your git ignore file. This way hackers don't have access to your api keys and then miss use them. When writing your code you also need to make sure that their are no loop holes that hackers can purposely access to gain information on how your website is set up. If a hacker has access to information showing how you set up the website they can hack the website further causing your website to crash. <br/>
<br/>
When trying to make website perform to it's optimum level there are many things which you should consider. One of the most basic ways to help your websites performance is make as few HTTP requests as possible. A first-time visitor to your page may have to make several HTTP requests, but using something like an expired header, you can make those components cacheable, helping your websites performance. Minifying the code which accesses your database can limit bandwidth usage, as well as minifying you JavaScript throughout the site. Putting your CSS at the top of your index and Scripts at the bottom, will help your computer read the code faster, helping your optimal performance of your site. Simple things such as reducing DNS lookups, avoiding redirects, and removing duplicate scripts be very beneficial as well.<br/>
<br/>
Search Engine Optimization is very powerful for companies today. Search Engine's like Google, have 40,000 search queries a minute which translates to 3.5 billion searches a day. Google is such a main part in every persons life, that SEO should be a major consideration when building a website. The golden rule for SEO is that content is king, make sure you have great content that users will enjoy and learn from. Writing as much meta descriptions for each page description can help you site populate higher on Google. Other things such as having relevant headers, use Google’s keyword tool to find out that your content is hitting the right search terms. Getting your title right is a major part of this as well. You get 65 characters to create an on-topic incentive for the user to click. When dealing with search engine optimization, it is also important to not duplicate content, http://example.com, http://example.com/, http://www.example.com, and http://www.example.com/ are all considered different URLS. Manage your redirect rules so this does not happen. Use Really Simply Syndication (RSS) feeds, take advantage of those 255 character alerts as Google pulls them as part of the blog search engine.<br/>
<br/>
Another thing to also keep in mind when developing a website and SEO, is maintainability. Make sure the your website is current and does not have old information. As mentioned before, content is king, the more current the information the better chances a user will come to your website. Having a maintained website will also help market your website through word of mouth marketing. Users will enjoy your current information and tell other people about, that’s the cheapest form of marketing there is. Making sure your website keeps up with the current trends and technology online can also encourage users to come look at your material. These are just few details about UI, Security, Performance, SEO, Maintainability or Technology considerations you should make while building a web application or site.<br/>
<br/>
* Talk about your preferred development environment.<br/>
My preferred development environment is a friendly encouraging work environment where people not only work on their own code but works as a team as well. I believe a team atmosphere is very important, because as they say two brains is better then one. I may have an idea of how my code should be written but getting input form others, will only make my code that much better and thus making the whole group stronger and vice versa. Having close communication between departments and groups is also very important when creating or maintaining a product.<br/>
* Which version control systems are you familiar with?<br/>
The version control system that I am most familiar with is Github. <br/>
* Can you describe your workflow when you create a web page?<br/>
My workflow when creating a web page usually begins with asking the fundamental question, Who is my consumer? Once I am able to identify my consumer, I come up with their needs and how my website could satisfy those needs. Once I know my consumer better through market research, I can then start writing down user-stories and draw wireframes to build a blue print of my website and its functionality. Market research is very important in identifying your consumer because you can get a better idea of how the website should be layer out. Drawing wireframes allows you to make your website easy to navigate form the users perspective. Testing these blueprints by having a potential user look at them first, can help give insight on further designs. From there I would start constructing backend components and make sure my database is correctly setup for how I want to use it. Making sure my app/website is correctly organized will help future people go through my code. After writing all the code for the backend and making sure all of my routes are correct, I would then start working on the frontend. Making sure the website is styled correctly for my intended user and set up mobile first, as I mentioned before 60% of Americans access the internet through there phone. I would make sure that my website is fully responsive to satisfy those Americans. Once I have the base of my website built, I would then go back through and make my code as dry as possible. Next I would test out my websites performance to see where it is slow and how I could change it to make it faster. After making perform to it's optimum level I would run through the website as many times as possible to find bugs.<br/>
* If you have 5 different stylesheets, how would you best integrate them into the site?<br/>
If I had 5 different stylesheets I would compress them into 1 large CSS stylesheet and also make sure that I have a CSS folder within my site to hold the stylesheet.<br/>
* Can you describe the difference between progressive enhancement and graceful degradation?<br/>
When thinking about development approaches their are two development approaches you can take, graceful degradation and progressive enhancement. Graceful degradations the practice of building your web functionality so that it provides a certain level of user experience in more modern browsers, but will also degrade gracefully to a lower level in older browsers. This lower level is not as nice to use for your site visitor, but does provide them with basic functionality. Progressive enhancement establishes a basic level of user experience that all browsers will be able to provide when rendering you web sit, but you also build in more advanced functionality that will automatically be available to browsers that can use it.<br/>
* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).<br/>
I would create a simple slideshow page, without any frameworks by building a single page application. This means that all html elements are rendered on the page, but you use CSS/JavaScript to hide the html until the user wants to view it by clicking a button. For a slide show, I would implement each page as a section within my html and giving it the id of page1, page2, page3 and so on. When you render the home page, page 1 will be display: block or inline, all of the other pages will have a CSS class called hide, which se the display on none. When you click on the next arrow/button JavaScript will then add the class hide to the first page, and then set the display to block or inline for the second. At this point page3 and so on will still be hidden. By clicking the next arrow/button again it will then add the class "hide" to page2 and set display for page3 to block or inline to show it.<br/>
* If you could master one technology this year, what would it be?<br/>
If I could master a technology this year it would be mastering the python framework, due to its versatility and wide use across many organizations.<br/>
* Explain the importance of standards and standards bodies.<br/>
The use of standards automatically makes every page you build genuinely cross-browser and cross-platform. With the use of web standards web designer developers and engineers will be able to achieve a more stable web despite the ongoing introductions of new hardware and software. With the use of standards, both development and maintenance time become reduced as a result of faster debugging and troubleshooting when it comes to handling the code we create. Standards allow backwards compatibility and validation since they are written to be compliant with older browser versions. This compliant code can be validated through validation service which makes the developer's work a lot easier resulting in less production time. The use of standards can also increase search engine success while also allowing for the certainty of graceful degradation.<br/>

## HTML Questions

* What does a `doctype` do?<br/>
doctype lets the browser know what type of language you are writing in so that it can properly render the pages on the web.<br/>
* What's the difference between HTML and XHTML?<br/>
The difference between HTML and XHTML, is that HTML is Hyper Text Markup Language, where XHTML is Extensible Hypertext Markup Language, it is HTML written as XML. XHTML is almost identical to HTML with so minor differences. XHTML DOCTYPE is mandatory. html, head, title, and body are also mandatory. XHTML elements must be properly nested. XHTML elements must always be closed, they must be in lowercase, and XHTML documents must have one root element. Within attributes in XHTML, they must also be in lowercase, must be quoted, and attribute minimization is forbidden.<br/>
* What are `data-` attributes good for?<br/>
Data- attributes are good for letting the browser know what Data- your script includes. This could be to store the initial height or opacity of an element which might be required in later JavaScript animations. Data- can store parameters for a flash movie that is loaded via JavaScript. Data- allows you to store custom web analytics tagging data. It can be used to store data about an element that can be accessed by JavaScript later.<br/>
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.<br/>
The difference between cookie, sessionStorage and localStorage are ways to store information about the user but each is a different from the next. localStorage and sessionStorage are relatively new API's and are nearly identical with the sole exception of persistence. sessionStorage is only available for the duration of the browser session meaning it is deleted when the browser is closed, it does however survive page reloads. If the data you are storing needs to be available on an ongoing basis then localStorage is preferred to sessionStorage, although both can be cleared by the user and should not be relied on the continuing existence of data in either case. localStorage and sessions Storage are perfect for persisting non-sensitive data needed within client scripts between page(ex: preferences, scores in game). localStorage and sessionStorage can easily be read or changed from within the client/bowser and should not be relied upon for storage of sensitive or security related data. Cookies are used for authentication purposes and persistence of user data, all cookies valid for a page are sent from the browser to the server every request to the same domain. This includes the original page request, any subsequent Ajax request, all images, stylesheets, scripts and fonts. For this reason cookies should not be used to store large amounts of information.<br/>
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?<br/>
It is generally a good idea to position CSS links between head and JavaScript and just before body because you want the stylsheets to render on the page before your JavaScript renders incase your JavaScript changes any of the styling with the users interaction with the website. Often you want script tags to be before the closing body tag so that way all of the DOM elements are loaded before your script incase you JavaScript affects any of the DOM elements as well. <br/>

## CSS Questions

* What is the difference between classes and IDs in CSS?<br/> Classes and ID's are given to DOM elements to organize and minimize your stylesheet. ID's are only to be used once on a specific element, because the styles are intended for that element and that element only. If you want styles to act on multiple elements you want to give those DOM elements the same class.<br/>
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?<br/>
Resetting CSS means that you remove all styling from every element including margins, padding.. etc. All elements will have the same font-size, same line height and no spacing. Normalize CSS makes every element render consistently across browsers. Normalize CSS is the one that I would prefer because it does not make sense to reset everything only to style it again.<br/>
* Describe Floats and how they work.<br/>
Floats are when you want an element to float to either the right or the left depending on where it's parent element is located. Floating elements will take the element and float it to the top of its parent element to either the left or right. When you float elements the browser no longer knows the height of the element, which is why it is important to clearfix elements after they have been floated, so that way the browser knows the height of the element.<br/>
* Describe z-index and how stacking context is formed.<br/>
When you look at a web page it is two-dimensional. Meaning that there is a x-axis and a y-axis. Z-index introduces a third dimension to DOM elements and brings it to the front or back. Your normal browser view has a z-index of 0, stacking context is important when you want a desired look and to do so make sure the elements you want in the background have negative z-index and the elements you want in the front have positive z-index's greater then 0 <br/>
* Have you ever used a grid system, and if so, what do you prefer?<br/>
Grid systems are very beneficial and make responsive designs easy. I often use the bootstrap grid system to take advantage of the different view-ports rather then having multiple media queries. The bootstrap grid system allows you to give an element a certain width based on a 12-column scale ranging from extra-small device(cell-phones),to small devices which are in-between cell-phones and tablets, to medium devices(tablets), to large devices such as laptops and computers.<br/>
* Have you used or implemented media queries or mobile specific layouts/CSS?<br/>
Yes, I have implemented pure CSS media queries for full responsive design without using a grid system like bootstrap. This requires more lines code but allows you to be more custom with your design. My media queries were in 200px increments starting at a minimum px-width of 350px and going all the way to 2500+px for large screens and projectors.<br/>
* How do you optimize your webpages for print?<br/>
You optimize your webpages for print by adding a CSS link for printing your webpage, this will be just like any other stylesheet just labeled print.css. Within this print.css you first set @media print then you can set you the width to a specific number for when you want to print the page(600-900px recommended). By adding a class called .no-print to display: none and attaching this class to elements on your page that you wouldn't want printed like navigation bars, side bars, and footers that way when people want to print your page they just want the information, so take out all the other stuff they don’t need by giving is a class call .no-print <br/>
* What are the advantages/disadvantages of using CSS preprocessors?<br/>
One of the advantages of preprocessors like Sass or Scss is that they keep your CSS organized for developers to read after you. Mixins within these preprocessors have their advantages and disadvantages. They make it easy to use classes of CSS over multiple elements, although this is a strength it can also be a weakness. For large projects and websites you might change these mixins for a desired output, but you don't realize all of the other elements that you are affecting on accident.<br/>


  * Describe what you like and dislike about the CSS preprocessors you have used.<br/>
  Things that I like about the CSS preprocessors like Scss and Sass are they keep your CSS organized. When your projects get larger though it is often inconvenient because the mixins that you use will affect multiple element styles and sometime that can do weird things with your CSS if you are not careful.<br/>


* How would you implement a web design comp that uses non-standard fonts?<br/>
I would implement a web design comp that uses non-standard fonts by having them stored in my local directory and then linking to them within my CSS. This is when the font you are using is not apart of Google fonts or a paid web font repository.<br/>


* Explain how a browser determines what elements match a CSS selector.<br/>
A browser determines what elements match a CSS selector through classes and id's.<br/>

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.<br/>
Every element in the page is considered a box. The box model refers to the specification of the box attributes such as the width, padding, border and margin. You can change the box model by setting the box-sizing property such as content-box, padding-box and border-box. content-box includes width and height but not padding and border. Padding-box includes up to the padding and border-box includes up to the border.<br/>
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?<br/> Box-sizing: border-box allows you to set the width and add padding and borders without having to worry about the total width of the box increasing. This is handy when you just want to mess with the borders and padding and no have to worry about the width.<br/>

* What's the difference between inline and inline-block? <br/>
Inline-block basically means that dimensions don’t apply and vertical margins no longer work. Vertical padding can be added but cannot increase the height of the element greater than it's line height and so may overlap subsequent lines. Inline styles have the highest precedence, which means they are going to be applied no matter what <br/>
* What's the difference between a relative, fixed, absolute and statically positioned element?<br/>
Relative position of element means that it is positioned relative to its parent element. This means that it will not go passed the upper bounds of the box that it is in. Absolute position is position absolutely on the page, meaning that no matter what box it is in, absolute will override everything and put the box exactly where you want it. Fixed positioning means that the element is fixed on the even if you scroll it will still be in the same place, often good for navbar's and things like that. Elements are positioned static by default. Static positioned elements are not affected by the top bottom, left, and right properties. Static elements are always positioned according to the normal flow of the page.<br/>
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?<br/>
The C in CSS stands for cascading meaning that styles cascade downwards and any styling that comes after the first styling will take place. You can take advantage of this by keeping elements that are constant throughout pages on the top of your style sheet. If you need to override the style just place the new CSS underneath the previous element, but make sure that it is equal to or has higher specificity<br/>
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?<br/>
CSS frameworks that I have used include Bootstrap, Materialize, and Angular. I really like bootstrap and taking advantage of the grid system but besides that bootstrap websites tend to look very similar. I would change a lot of the default styling that comes with bootstrap to make it unique and look different form other bootstrap sites. Materialize allows more custom styling which makes it look a little different from site to site, but once again I would change the default styling to make it truly unique. Angular is a great CSS framework, I really enjoy the data-binding that comes along with it. That said there are some limitations to angular because it can often override other frameworks which you don't want to. I would improve angular to be more adaptive with other frameworks.<br/>
* Have you played around with the new CSS Flexbox or Grid specs?<br/>
I have played around with Flexbox for CSS layouts. I don't really have a problem with CSS layouts so I don't use it as much. <br/>
* Have you ever worked with retina graphics? If so, when and what techniques did you use?<br/>
* Explain some of the pros and cons for CSS animations versus JavaScript animations.

## JS Questions

* Explain event delegation<br/>
Event delegation is when you need to delegate events that occur before running your JavaScript. In other words event delegation is the idea that something other than the target of an action resolves the event raised by that action. For instance when you do not want to refresh the page after a button has been clicked you can pass event in as parameter into a function and then run event.preventDefualt, this will override the rendering of the page so that JavaScript can run. Event capturing and event bubbling are two phrases in a three phase flow. Any event occurs, such as clicking a button, the browser moves down the DOM hierarchy until it finds the element raising the event, then it moves into the targeting phase. Once the targeting phase is complete the browser bubbles up to the DOM back to the topmost container to see if anything else needs to use the same event.<br/>
* Explain how `this` works in JavaScript<br/>
The object that 'this' refers to in JavaScript is predetermined every time control enters a new execution context and remains fixed until a control shifts to a different context. By default, this refers to the global object. When a function is called as property on a parent object, this refers to the parent object inside that function. When a function is called with the new operator, this refers to the newly created object inside that function.<br/>
* Explain how prototypal inheritance works<br/>
Prototypal inheritance is an internal object which other objects inherit properties. Its main purpose is to allow multiple instances of an object to share a common property. Thus, object properties which are defined using the protype object are inherited by all instances which reference it.
* Why is it called a Ternary expression, what does the word "Ternary" indicate? <br/> the word ternary indicates the amount of inputs the operand accepts, in Ternary’s case it is 3. In programming the ternary operand is used to rewrite an if statement. It is written by first writing a conditional with a space and question mark at the end. Depending whether the result of that conditional is true or false run the rest of the code. The on the left is the code that runs if it is truth : the code on the right of the colon is the code that is executed if it is falsey.<br/>
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?<br/>
A variable is undeclared when it does not use the var keyword, it gets created on the global object, thus it operates in a different space as the declared variable. Something is undefined when it hasn't been defined yet. If you call a variable or function without having actually created it yet the parser will give you an 'not defined'. Null is a variable that is defined to have a null value, 0 or empty.<br/>
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?<br/>
Closures keep access to the variables which means they can be used to save state. For instance if you have a function closure(longlivedvariable){ pass in var innerFunction = function inner(){return longlivedvariable}return inner function}. Notice that the closure function doesn't return longlivedvariable, but rather inner, this means there's a reference hanging around to inner and because inner has a reference to longlivedvariable, that variable continues to exist.<br/>
* What's a typical use case for anonymous functions? The typical case for anonymous functions is to pass the result of another function into that function by not declaring a specific parameter. This allows the function execute what ever code that it is given.
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`? Function Person(){} is creating a new function called person, where var person = Person() is calling the person function and then assigning it to a variable, and the last function is creating new instance of the person function and setting to variable person.<br/>
* What's the difference between `.call` and `.apply`?<br/>
The difference between .call and .apply is that .apply lets you invoke the function with arguments as an arrays where .call requires the parameters be listed explicitly.<br/>
* Explain `Function.prototype.bind`.<br/>
The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called, when calling .prototype after a function, it then inherits all objects within that function.<br/>
* What's the difference between feature detection, feature inference, and using the User Agent string?<br/>
When you check to see if a certain feature exists, that is feature detection. It’s important to write code that checks if features exist in JS since different browsers have different implementations. Feature inference is when you make an assumption that one feature is present another one also should be present. Since your not checking for the feature you’re using you’re more likely to have inconsistences.<br/>
* Explain AJAX in as much detail as possible.<br/>
AJAX stands for Asynchronous JSON and Xml. It is when you send a requests for information or a JSON object from another site. Since AJAX is done Asynchronously there is going to be a little delay before that JSON object comes back
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
```JavaScript
var foo = 10 + '20';
```

*Question: How would you make this work?*
```JavaScript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```JavaScript
"i'm a lasagna hog".split("").reverse().join("");
```

*Question: What is the outcome of the two alerts below?*
```JavaScript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

*Question: What is the value of `foo.length`?*
```JavaScript
var foo = [];
foo.push(1);
foo.push(2);
```

*Question: What is the value of `foo.x`?*
```JavaScript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

*Question: What does the following code print?*
```JavaScript
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

