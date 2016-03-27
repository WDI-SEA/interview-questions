## CSS Questions

* What is the difference between classes and IDs in CSS?
You would apply an id to a specific element that you will only be manipulating styling individually where you apply classes to multiple objects that will be styled the same. 

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

Resetting: removing all styling from an element
Normalizing: making elements render consistently across browsers

* Describe Floats and how they work.

Float is a css positioning property that will take an element and float it to the left or right of the screen. To use a float you in your css you would call it float: left or float:right

* Describe z-index and how stacking context is formed.

The z-index allows you to overlap or stack elements on one another using css. If an element has a larger element than the element below it that larger element will apear "staked" on top of the element with the lower z-index.

* Have you ever used a grid system, and if so, what do you prefer?
The only grid system I have used is bootstaps built in grid system. I would like to learn other grid systems and how to position everything perfectly using css alone. 

* Have you used or implemented media queries or mobile specific layouts/CSS?

Yes, I have used media queries to make sure my applications are following a responsive design. They are very easy to use as you just include them in your css.

<!-- * How do you optimize your webpages for print? -->
* What are the advantages/disadvantages of using CSS preprocessors?

Advantages: organization, nested elements, mixins, makes your css more DRY as it is less repetitive, is easily integrated into other frameworks like bootstrap.

Disadvanteges: Need to learn and fully understand the framework, could inherit bugs and mistakes

* Describe what you like and dislike about the CSS preprocessors you have used.

I love using SASS. I love that you can nest your css and use mixins. I have no downsides with SASS.

* How would you implement a web design comp that uses non-standard fonts?

Google fonts

* Explain how a browser determines what elements match a CSS selector.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.

* What's the difference between inline and inline-block?

inline: do not respect top and bottom margin, cannont have a set height/width, allow elements to sit to their right and left

inline-block: allow elements to sit to their right and left, repsect top/bottom padding/margin, respect height and width.

* What's the difference between a relative, fixed, absolute and statically positioned element?
Relative: 

Fixed: 

Absolute:

Starically:

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?

* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?

I have not, but note to self, CHECK THESE OUT 

* Have you played around with the new CSS Flexbox or Grid specs?

Yes, I have played around with CSS Flexbox.

* Have you ever worked with retina graphics? If so, when and what techniques did you use?

* Explain some of the pros and cons for CSS animations versus JavaScript animations.

CSS animations are superior to js animations. CSS gives you more control over your animation and JS tends to be more buggy. You have more artistic freedom with css animations as well as avoiding writing long functions by using @keyframe.