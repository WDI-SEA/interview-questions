
Chris Kenyon
Interview questions
WDI-09


GENERAL

1. Last week, the 24-hour hackathon was a tough time with 2 sick members and the 3rd not responding at night or showing up for the presentation. I scrambled to put together the functional pieces and offer some explanations in class, without accusing anyone else of being absent. I think the "judges" were happy with seeing something on the screen that worked. I focused on a distraction - the funny jobs that could result from searches. Coding isn't all about the code, sometimes the presentation matters. 

2. I enjoy coding because I'm creating something. Taxes were not about doing anything outside the guidelines, but there's naturally a lot of different ways to code a simple project. I also like the teamwork with everyone accepting each other taking some time to learn things or pass off tasks that are suited for someone else. Accounting work was rarely about teamwork, since WIP time was supposed to be shorter. 

3. During the hackathon, we struggled with a few problems. Early on, the database was not connecting with our program. It existed, it had info, but now it wasn't working. Sean looked and found the node_modules just needed an update. Later, the url wouldn't link up in a Href anchor tag, so I looked at some examples in Stack Overflow. I keep the working class copies active to quickly see examples. 

4. Considerations? Too many to write. 

5. Preferred dev environment? I'm not sure yet, beyond wanting to get away from coworker avoidance like accounting. I want real reviews, which are limited in accounting for many reasons. 

6. Version controls? (SEARCH)

7. Workflow - I like the quick wireframe and chart start that we learned but didn't use in class much. We used it in projects, and we did much more brainstorming early with tech needs & questions to make sure we didn't dive too far into the project to get away from a bad decision that couldn't be fixed within the 1 week deadline (or wherever we were on the timeline). We used trello boards to keep track of all tasks abd avoid conflicts. 

Order of tasks usually went by: function needs, then style. 

8. 5 Css partial stylesheets in a folder, if it gets larger then it's safest to keep them separate with a comparison top-level document (comments? control file with order of load priority?)

9. Progressive Enhancement is building a website with functionality on a low level to make sure that all or most browsers can handle it, and then building up from there. 

Graceful degredation is when a computer keeps limited functionality when something breaks down. One example is with operating systems "safe mode" - when the full OS has a problem, the safemode allows the user to take a look at basic functions to see what broke if it wasn't clear. 

10. Slideshow - caravel? That was an early bootstrap project. No frameworks? 
OK, make a slides folder to fill, your "projector" is the script that goes through those and controls timing, and the style (size, background) is also separate. 

11. Master a tech? Not sure.

12. Standards/Standard Bodies? Standards are stylistic tendencies - simple. modularized. 
Standards bodies are the organizations that oversee this??? 





HTML

1. Doctype gets 

2. HTML/XHTML (SEARCH)
XML syntax is more strict
XHTML includes the Ruby module

3. data-- attributes

4. Cookie- stored client side to re-open 
SessionStorage - client side, removed when session closes
localStorage - server side, saved not expiring

5. Link/Script positions depend on the dependencies (JS for Jquery, Angular for Angular Attachement scripts). After that, the other pages or modules may often depend on those being loaded before any body calls, and the connecting pages go above the body. Scripts can go at the bottom if they exempt from a lot of these cases, but it really shouldn't happen if there's good attention to test cases. 




CSS

1. Classes vs IDs - it's better for classes to apply to multiple instances, IDs for singles. 

2. Reset vs Normalize - reset wipes all the default browser styles, normalize provides a starting point for them. 

3. Floats - decimal numbers that take much more space than an int. Doublefloats. 


4. z-content

5. grid system? like bootstrap? 

6. Yes, media queries. 
Mobile-1st is often pushed as better in our class, but a lot of my current sites are made out of expediency. I'm always working on this, but styling is less than functionality at this point in my work. 

7. 







JS

1. Event delegation

2. "this" works by "$scope", IT ALLOWS CHANGES TO variables within an environment, with child layers going down. "this.number" can be passed along in the object that made it, or a parent object. 

3. Prototype inheritance - the constructor, not the objects, pass along info that is passed into the constructor (param differences)

4. Ternary expression - three parts

5. Null
Undef
Undeclared
How to tell/check? 

6. A closure is

7. Typical use case for anonymous functions? 

8. function Person(){} - this function creates Person-functions that probably create person objects. 
var person = Person() - this makes a person
var person = new Person()

9. .call
.apply

10. Function.protoype.bind ??

11. feature detection, 
feature inference
User Agent string

12. AJAX - database changing calls(sends - delete, post)
DETAIL

13. Templates - 

14. Hoisting ??

15. Event bubbling?

16. Attribute
Property

17. Why not extend built-in js objects? 

18. == vs === , it's about truthiness, the Stephen Colbert political meter. 

19. Same-origin policy in JS?

20. Promises and their polyfills? 

21. Promises - stuff.get(function() {
  
})
Multiple callback functions need to be nested. 


Promises - stuff.get().then(function() {
  
})

This is more prominent as a standard, and gets cleaner code with the .then
and chain on multiple promises instead of nesting them. 

22. Tools for debugging JS code? 

23. 









DATABASE

1. Facebook, 4 models, attributes, 1:M, M:M

User
Post
Comment
Messages





Ruby/Rails

1. Gems are installation dependencies

2. Symbol
String

3. Class method
Instance Method

4. Local
class
instance variables

5. Range

6. att_accessor

7. env files in config folder

8. application.rb file

9. define a constant

10. yield

11. storing API keys

12. send params through a url

13. MVC

14. before_action

15. controllers in rails? 

16. RESTful routing

17. polymorphic association

18. params

19. make a migration to add a column

20. CSRF, protect against? 

21. 







TESTING: 

1. Testing ADVANTAGES - lots. 
DISADS - not much, time, 

2. Tools for testing - this depends on the program. We used some in class


3. Unit test is for small pieces or modules of code. 
Function/integration test if for multiple scripts or holistic testing of links.  

4. Code style linting tool 

5. End-to-end testing applies to the whole app working. 









INDIVIDUAL CODE TECHNICAL

Var foo = 10 + '20';       // what is the value of foo



            //both return 7
add(2, 5)
add(2)(5)
          


"i'm a lasagna hog".split("").reverse().join("");



var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);





var foo = [];
foo.push(1);
foo.push(2);      //what is foo.length




var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};         ///what is foo.x



console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');       //what does this print





FUN QUESTIONS: 

1. Cool project - the stolen bike app - useful, teamwork, inspiring

2. 

3. Pet projects - phazermole, bike steal app connections, 

4. 











