## CSS Questions

* What is the difference between classes and IDs in CSS?
You would apply an id to a specific element that you will only be manipulating styling individually where you apply classes to multiple objects that will be styled the same. 

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

Resetting: removing all styling from an element
Normalizing: making elements render consistently across browsers

* Describe Floats and how they work.

Float is a css positioning property that will take an element and float it to the left or right of the screen. To use a float you in your css you would call it float: left or float:right

* Describe z-index and how stacking context is formed.

The z-index allows you to overlap or stack elements on one another using css. If an element has a larger element than the element below it that larger element will appear "stacked" on top of the element with the lower z-index.

* Have you ever used a grid system, and if so, what do you prefer?
The only grid system I have used is bootstrap built in grid system. I would like to learn other grid systems and how to position everything perfectly using css alone. 

* Have you used or implemented media queries or mobile specific layouts/CSS?

Yes, I have used media queries to make sure my applications are following a responsive design. They are very easy to use as you just include them in your css.

<!-- * How do you optimize your webpages for print? -->
* What are the advantages/disadvantages of using CSS preprocessors?

Advantages: organization, nested elements, mixins, makes your css more DRY as it is less repetitive, is easily integrated into other frameworks like bootstrap.

Disadvantages: Need to learn and fully understand the framework, could inherit bugs and mistakes

* Describe what you like and dislike about the CSS preprocessors you have used.

I love using SASS. I love that you can nest your css and use mixins. I have no downsides with SASS.

* How would you implement a web design comp that uses non-standard fonts?

Google fonts

* Explain how a browser determines what elements match a CSS selector.

The browser reads them right to left, the program reads the key selector first(the class/id) then where it is being applied. 

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?

box-sizing tells the browser what the sizing properties, height and width, should include. It does not include the margin. This property helps with layout because it takes into account a fixed width and height along with padding. 

* List as many values for the display property that you can remember.

inline, block, inline-block, none, initial, inherit.

* What's the difference between inline and inline-block?

inline: do not respect top and bottom margin, cannot have a set height/width, allow elements to sit to their right and left

inline-block: allow elements to sit to their right and left, respect top/bottom padding/margin, respect height and width.

* What's the difference between a relative, fixed, absolute and statically positioned element?

Relative: positioned relative to it's normal position, it will be adjusted away from it's static position

Fixed: positioned relative to the viewport, it will remain in the same spot even if the page is scrolled

Absolute: positioned relative to the nearest ancestor

Static: elements are not affected by the top, bottom, left, or right properties, it is the default property and is positioned based on the flow of the page.

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?

Beacuse the program reads from top to bottom if you overwrite I style you wrote previosly the last change will be the change that appears on the screen. p {color: blue, font-size: 30em} p{color:pink,} The text color of p will be pink.

You can use this system to your advantage by nesting elements if you are using SASS or making your code more organized.

* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?

I have not, but note to self, CHECK THESE OUT 

* Have you played around with the new CSS Flexbox or Grid specs?

Yes, I have played around with CSS Flexbox.

* Have you ever worked with retina graphics? If so, when and what techniques did you use?

* Explain some of the pros and cons for CSS animations versus JavaScript animations.

CSS animations are superior to js animations. CSS gives you more control over your animation and JS tends to be more buggy. You have more artistic freedom with css animations as well as avoiding writing long functions by using @keyframe.
