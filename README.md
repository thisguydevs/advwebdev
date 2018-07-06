# advwebdev  

## Working through Colt's Steele's Advanced Web Developers Bootcamp  

__*Started June 25th, 2018.*__

___

### Section 2 - CSS Animations: Transforms and Transitions  

Started: 06.25.2018  
Completed: 06.27.2018  
  
__*What was covered*__

+ Pseudo-Classes  

  + `:hover`
  + `:focus`
  + `:active`  

+ Transforms  
  + translate
  + scale
  + transform-origin
  + rotate
+ Vendor Prefixes
+ Transitions
  + `transition-duration`
  + `transition-property`
  + `tranition-timing-function`
  + `transition-delay`
+ Vendor Prefixes
+ CSS Animation Performance  

+ [X]  Building an Animated Gallery

___

### Section 3 - CSS Animations: Keyframes  

Started: 06.27.2018  
Completed: 06.28.2018

__*What was covered*__

+ animation-name
  + naming the animation
+ animation-duration
  + how long the animation takes to complete
+ animation-timing-function
  + type of curve - `ease-in`, `ease-out`, `linear`, ect.
+ animation-delay
  + how long until the animation starts
+ animation-iteration-count
  + how many times the animation will repeat
+ animation-fill-mode
  + `forwards`, `backwards`, `both`
+ animation-direction
  + run animation in `reverse` or `alternate`
+ animation-play-state
  + specifies whether the animation is `running` or `paused`
+ [x] Rising and Setting Sun Animation
+ Animation Shorthand
  + Combining `animation` into a single line
+ [X] Build an Animated CSS Loading Icon

___

### Section 4 - Advanced CSS: Layout With Flexbox  

Started: 06.28.2018  
Completed: 07.02.2018

__*What was covered*__

+ Flexbox Container Properties
  + `flex-direction`
        +   specifies how items are placed in the flex container, defining the main axis and it's direction  
        +   default value is `row`
        +   `row-reverse` reverses the direction of the main axis
        +   `column` makes it go down starting with first item at the top
        +   `column-reverse` makes it go down starting with last item at the top
  + `justify-content`
        +   defines how space is distributed between items in flex container along the main axis
            +   `: flex end` moves all content to the right side
            +   `: center` centers content with spaces on both sides
            +   `: space-between` gives equal space between elements, no space on ends
            +   `: space-around` gives equal amount of space to both sides of an item
  + `flex-wrap`
        +   specifies whether items are forced into a single line OR can be wrapped into multiple lines
        +   `flex-wrap: wrap`
  + `align-items`
        +   defines how space is distributed between items in flex container along the corss axis
        +   `: flex-start` items aligned top of cross axis
        +   `: flex-end` items aligned bottom of cross axis
        +   `: stretch` items are stretched to fill entire cross axis (default value)
        +   `: center` items are centered along cross axis
        +   `: baseline` align items based on the baseline of the text/font
  + `align-content`
        +   defines how space is distrubuted BETWEEN ROWS in flex container along the cross axis
        +   `: flex-start` items aligned top
        +   `: flex-end` items aligned bottom
        +   `: space-between` first and last rows get pushed to top and bottom, equal space in between
        +   `: space-around` equal space between rows, 1/2 that amount of space between top and bottom
        +   `: center` aligns in the center with no space between rows, equal space top and bottom
+ Flexbox Flex Item Properties
  + `order` specifies the order used to layout items in their clex container
        +  all itmes by default have an order of '0', use negative
  + `flex` defines how a flex item will grow or shrink to fit the available space in a container
        +  shothand property for 3 other properties
            +  `flex-basis` sort of like width (rows) or height (columns), but not; specifies the ideal size of a flex item BEFORE it's palced into a flex container
            +  `flex-grow` dictates how the unused space should be spread amongst flex items
            +  `flex-shrink` dictates how items should shrink when there isn't enough space in container
                +  1 is default value
            +  `align-self` allows you to override align-items on individual items
+ `display: flex`
  + groups onto same line
+ [X] Flexbox Sidebar Exercise
+ [X] Building a Polygon.com Widget
+ [X] Holy Grail layout

___

### Section 5 - Project: Building a Startup Site  

Started: 07.03.2018  
Completed: 07.03.2018

__*What was covered*__

+ [X] Build Mountain Travel Starup Website

___

### Section 6 - Async Founations  

Started: 07.03.2018  
Completed:

__*What was covered*__  

+ Callback Functions
  + Define callback functions
        > a function that is passed into another function as a parameter then invoked by that other function
  + Define higher order functions
        > a function that accepts a callback as a parameter
  + Use a callback function to make your code more general
    + Create callbacks using anonymous functions
+ `forEach` Functions
  + Describe and use the `forEach` function
        > + invokes the callback function for each element in the array
        > + `forEach` will invoke your callback with **3** parameters everytime
        >   + currentElemnt, currentIndex, array
  + Implement the forEach function
  + `for` loop
      ```javascript
        var arr = [1,2,3,4,5,6];
        function double(arr) {
            for(var i = 0; i < arr.length; i++) {
                console.log(arr[i] * 2);
            }
        }
        double(arr);
      ```
  + refactored `forEach` loop
      ```javascript
        var arr = [1,2,3,4,5,6];
        forEach(arr, function(number) {
            console.log(number * 2);
      });
      ```
<dl>
	<dt>findIndex</dt>
	<dd>retruns the index of the first element in the array for which the callback returns a truthy value. -1 is retruned if the callback never returns a truthy value.</dd>
</dl>

```javascript
function findIndex(arr, callback) {
  for (var i = 0; i < arr.length; i++) {
    if (callback(arr[i], i, arr)) {
      return i;
    }
  }
  return -1;
}
```

+ The Stack and the Heap
  + Describe what the stack is
    + An ordered data structure
    + Keeps track of fucntion invocations
    + Part of the JavasScript runtime (you don't access it directly.)
  + Describe a stack frame
    + Information on the function that was invoked
    + The parameters that were passed to the function
    + Keeps track of the current line number
    + Stack Definition
       > + An ordered set of stack frames
       > + Most recently invoked function is on the top of the stack
       > + The bottom of the stack is the first function invoked
       > + The stack is processed from top to bottom
  + Describe the heap
    + An area in memory where the daya is stored

+ `setTimeout`
  + A function that asynchronously invokes a callback after a delay in milliseconds
  + ```javascript
    setTimeout(function() {
      console.log("Runs in approx. 2000ms);
    }, 2000);
    ```
  + Every time you invoke `setTimeout` you get back an ID
  + An Example of Canceling `setTimeout`
  + ```javascript
    var timeerId = setTimeout(function() {
      console.log("This function runs in 30 seconds"); 
    }, 30000);

    set Timeout(function() {
      console.log("Canceling the first setTimeout", timerId)
      clearTimeout(timerId);
    }, 2000);
    ```
+ `setInterval`
  + A function that continually invokes a callback after every 'X' milliseconds, where 'X' is provided to `setInterval`
  + An Example of Canceling `setInterval`
    ```javascript
    var num = 0;
    var intervalId = setInterval(function() {
      num++;
      console.log("num: ", num);
      if(num === 3) {
        clearInterval(intervalId);
      }
    }, 1000);
    ```
  + 