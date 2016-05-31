General Questions

- What did you learn yesterday/this week?
- What excites or interests you about coding?

     That I have the ability to create/design beautiful websites and applications that can solve problems.

- What is a recent technical challenge you experienced and how did you solve it?


- What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?

- Talk about your preferred development environment.

- Which version control systems are you familiar with?

          Git

- Can you describe your workflow when you create a web page?



- If you have 5 different stylesheets, how would you best integrate them into the site?

- Can you describe the difference between progressive enhancement and graceful degradation?

- Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).

- If you could master one technology this year, what would it be?

          Javascript

- Explain the importance of standards and standards bodies.

HTML Questions

- What does a doctype do?

     it is an instruction to the web browser about what version of the markup language the page is written in.

- What's the difference between HTML and XHTML?

     XHTML follows the conventions of XML and is more strict.

- What are data- attributes good for?

         HTML element attribute that doesn’t display visually, and allows data to be stores in the DOM on elements. Bootstrap uses it.

- Describe the difference between a cookie, sessionStorage and localStorage.

     localStorage persists when the browser is closed.
     sessionStorage is reset when the browser is closed.
     Cookies are older, they can’t store as much info and they can only store strings, and are sent to the server.

- Why is it generally a good idea to position CSS <link>s between <head></head> and JS <script>s just before</body>? Do you know any exceptions?


     This has to do with the order things are loaded.
     CSS styles are loaded before elements appear and are displayed on the page.
     Javascript is placed at the bottom because the page needs to be loaded before things like click handlers are set up.

CSS Questions

- What is the difference between classes and IDs in CSS?

     Classes are not unique - you can use the same class on multiple elements. You can use multiple classes on the same element.
     ID’s are unique- each element can only have one. Each page can only have one element with that ID.

- What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?


     Resetting removes styling from all elements.
     Normalizing makes elements consistently across browsers.

- Describe Floats and how they work.

     Float is a CSS property that allows us to pull items left and right. and can be used to wrap text around images.

- Describe z-index and how stacking context is formed.

     defines how elements are “stacked” on the page.
     an element with a higher z-index will appear on top of an element with a lower z-index.

- Have you ever used a grid system, and if so, what do you prefer?

          Yes, I have used Bootstrap and Foundation 6. Both are similar in grid systems.

- Have you used or implemented media queries or mobile specific layouts/CSS?

          We have used @media min-width and max-width queries to set breakpoints to have our page appear differently on different screens.

- How do you optimize your webpages for print?

     Create a separate CSS file specifically designed for printing. Use high res photos with a 300dpi or higher. Media

- What are the advantages/disadvantages of using CSS preprocessors?

              they allow us to write fancier syntax and add logic to our CSS.

    - Describe what you like and dislike about the CSS preprocessors you have used.



- How would you implement a web design comp that uses non-standard fonts?

      using @font-face and font service links, like google fonts.

- Explain how a browser determines what elements match a CSS selector.

- Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

          Refers to margin, border, padding, content.

          The box model refers to margin, border padding and content. The display property allows us to set elements to be block elements, inline-block elements sit next to each other on a page.

- What does * { box-sizing: border-box; } do? What are its advantages?

           Browsers can measure the width and height of elements in different ways. Each browser interprets bow sizing differently. Specifying a specific box-sizing allows us to know how things are measured.

     The border-box value will measure elements including their borders. The content-box value will measure only the content, not the margin or border.

- List as many values for the display property that you can remember.

     none, inherit, inline, inline-block, block, table, table-cell

- What's the difference between inline and inline-block?

     Inline - respects left/right margins and padding, does not respect top/bottom margin. does not have width and height.  allows other elements to sit left/right of it.

     Block- respects all margins and padding. respects width and height.

     inline-block - placed in an inline element, but behaves like a block. respects all margin and padding. respects width and height. allows other elements to sit left/right of it.

- What's the difference between a relative, fixed, absolute and statically positioned element?

          Fixed: elements stay fixed, no matter if scrolling occurs.
          absolute: elements stay put relative to the entire document.
          relative:

- The 'C' in CSS stands for Cascading. How is priority determined in assigning styles (a few examples)? How can you use this system to your advantage?

          CSS works from top to bottom.

- What existing CSS frameworks have you used locally, or in production? How would you change/improve them?

     Bootstrap, Foundation 6, Materialize. I think that there could be one more universal framework that has most components combined.

- Have you played around with the new CSS Flexbox or Grid specs?

          Yes

- Have you ever worked with retina graphics? If so, when and what techniques did you use?

          Retina refers to displays to with an extremely high pixel density.

         The problem with high density displays, is that images built for low res screens will show up tiny. One way to deal with this is to have 2 sets of images. One for low density displays, and one for high density displays.

- Explain some of the pros and cons for CSS animations versus JavaScript animations.

JS Questions

- Explain event delegation
- Explain how this works in JavaScript

     It is used inside of a function and contains the value of the object that invokes that function. Used in classes, and functions. Each instance of an object or class will have a this property, where it’s own data and properties are stored.  When we create a point object, we can refer to this.x or this.y, and different instances of the point can have their own values.

- Explain how prototypal inheritance works

     javascript inherits from other objects

- Why is it called a Ternary expression, what does the word "Ternary" indicate?


     Ternary implies 3.
     var meal = isPhilly ? ‘cheesesteak’ : ‘burger’;

     var meal;
     if (isPhilly) {
     meal = ‘cheesesteak'
} else  {
     meal = ‘burger'
}

- What's the difference between a variable that is: null, undefined or undeclared?

          A variable is undeclared when it does not use the var keyword.
          Undefined is when something has not been defined yet.
          null is an empty value that we can set.

-  How would you go about checking for any of these states?

- What is a closure, and how/why would you use one?

     It makes it possible for a function to have private variables.

- What's a typical use case for anonymous functions?

- Difference between: function Person(){}, var person = Person(), and var person = new Person()?

- What's the difference between .call and .apply?

- Explain Function.prototype.bind.
- What's the difference between feature detection, feature inference, and using the User Agent string?
- Explain AJAX in as much detail as possible.
- Have you ever used JavaScript templating?

    - If so, what libraries have you used?
- Explain "hoisting".

     Javascript hoists variables declared with var to the to of a function. Variables will be undefined until their value is actually set. Variables with the same name of a variable outside a function as inside a function can interfere with each other.

- Describe event bubbling.
- What's the difference between an "attribute" and a "property"?
- Why is extending built-in JavaScript objects not a good idea?
- What is the difference between == and ===?

          === is a more strict definition of equality, checks the type of the 2 operands

          == performs type coercion.

     0 === ‘0’ returns false
     0 == ‘0’ returns true

- Explain the same-origin policy with regards to JavaScript.

          This is a security policy that prevents Javascript from accessing sites outside the current domain.

- What is the extent of your experience with Promises and/or their polyfills?
- What are the pros and cons of using Promises instead of callbacks?
- What tools and techniques do you use debugging Javascript code?

          Chrome developer tools, console.log, break points, debugger keyword.


- What language constructions do you use for iterating over object properties and array items?

          For loop, For each loop, For in loop, .forEach, while loops, do while loops, map, filter, .reduce functions.

for in loops are good for iterating over the properties in an object and accessing their key.

for  loops are good for arrays. for in loops with arrays may include the ‘length’ property and cause problems.


Database Questions

- Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

Ruby/Rails

- What are ruby gems?


- What is the difference between a symbol and a string?

          We use symbols in hash maps. Symbols all reference one single value.
          There may be many instances of strings.


- What is the difference between a class method and an instance method?

          A class method is exists once for all instances of a class, an instance mother acts on instances individually.
          Local variables are not associated with any variables, they’re only associated wth their own scope of what function they are in.

          Instance variables are attached to instamnes of classes.
          At a point class may have many instances if itself, each with their own X, Y, instance variables with many different values.

          we could also create a class variable (num_point)

- What is the difference between local variables, instance variables, and class variables?
- What is a range?
- In ruby, what does attr_accessor do?


    class Point
               attire_accessor :x, :y

- What is the purpose of environment files under the config folder in Rails? (development, test, production)
- What is the purpose of the application.rb file in Rails?
- How can you define a constant?
- What is the purpose of yield?


- How do you store API keys when creating an app?

     Keys are stored in a separate .env file.
     Add to .gitignore

- How do I send parameters through a url?
- Explain MVC
- What is a before_action? When would you use it?
- What do controllers do in rails?
- What is RESTful routing?
- What is a polymorphic association?
- What are params?
- How do I make a migration to add a column in Rails?
- What is CSRF? How does Rails protect an app against this?
- What's the difference between User.find_by_id(1) and User.find(1)?
- What's are classes in Ruby? What are modules? And what's the difference?

Testing Questions

- What are some advantages/disadvantages to testing your code?
- What tools would you use to test your code's functionality?
- What is the difference between a unit test and a functional/integration test?
- What is the purpose of a code style linting tool?
- What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

Coding Questions:

Question: What is the value of foo?


var foo = 10 + '20';




Question: How would you make this work?


add(2, 5); // 7
add(2)(5); // 7





Question: What value is returned from the following statement?


"i'm a lasagna hog".split("").reverse().join("");




Question: What is the outcome of the two alerts below?


var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);




Question: What is the value of foo.length?


var foo = [];
foo.push(1);
foo.push(2);




Question: What is the value of foo.x?


var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};




Question: What does the following code print?


console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');




Fun Questions:

- What's a cool project that you've recently worked on?
- What are some things you like about the developer tools you use?
- Do you have any pet projects? What kind?
- How do you like your coffee?