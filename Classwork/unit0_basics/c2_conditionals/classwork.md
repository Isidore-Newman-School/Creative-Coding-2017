# 2. Conditionals

### if / else if / else
Define a function **max()** that takes two numbers as arguments and returns the larger one. If the numbers are the same, print to the console "numbers are equal!" and return that number.

```JavaScript

function setup() {
    createCanvas(400, 400);
    fill(0);
}

function draw() {
    background(150);
    console.log(max(50, 90));
    console.log(max(30, 30));
}

// max() function goes here

```


### compound conditions

Use the logical && operator to turn the background() green if mouseX is in the middle third of the canvas. Otherwise, set the background() to white.

```JavaScript
function setup() {
    createCanvas(400, 400);
}

function draw() {
   
   // check if **mouseX** is in the middle third of
   // the canvas **width**
   
}
```


### Challenge: 

Use conditional statements to get a ball to bounce on either side of the canvas. 

For an extra challenge, have the ball ricochet in random directions and bounce off of top, bottom, left, and right.


```JavaScript
// Position Variables
var x = 10;
var y = 150;
var velocityX = 5;
 

function setup() {
    createCanvas(400, 400);
    fill(0);
}

function draw() {
    background(150);
    ballMove();
    ellipse(x, y, 30, 30);
}

function ballMove() {
   x += velocityX;
   
    // your code goes here
    
}
```


