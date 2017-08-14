I decided to practice my CSS + HTML skills by recreating an impressive examples of good layout. My previous attempt was [Futurizmo](https://al1s.github.io/Futurismo/). Current project is the Jazz poster by Jen Simmons. Motivation behind - to repeat layout without CSS Grid, using only CSS Flexbox.

Lessons learned:

1. It's not semantically natural to do it with Flexbox. I had to lay many empty box elements to place a few boxes with content where they have to be. With the use of Grid, I don't need all these faux boxes.
2. How to integrate picture into the page in a responsive way? `background-size: cover;` fits the best, but it became obvious after I've scrutinized Jen's code. My attempt was `background-size: contain;`. And for quite long I've tried to specify height explicitly to `body` element and it broke the layout, making it shorter, then pile of boxes. Constructed [demo](http://codepen.io/alstof/pen/WpyGGo) to catch the difference. 
3. I had to set to initial `min-height` of boxes in media query section. Without it all boxes have the same height and it was more then content inside.
4. I've used `inline-flex` for copyright note in footer. Copyright sign set as background image and the box where it's contained have no real content. It brings quirk: flex container is shorter than content inside. Found workaround. All tests [here](http://codepen.io/alstof/pen/zZRZYX).
5. Made boxes squared by setting `min-height` equal to `flex-basis` value. Here is [demo](http://codepen.io/alstof/pen/xqzOKg) on codepen.
