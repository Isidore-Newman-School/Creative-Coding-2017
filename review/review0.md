# Review 0
Functions and variables

## Drawing

**(0)** Draw a blue rectangle with a green background.

**(1)** Name 4 built-in variables that we've explored so far.

**(2)** Draw a line that begins at x1, y1 and ends at the cursor.
Challenge: draw a second line that is parallel to the first.

```javascript
var x1 = 100;      
var y1 = 50;

function setup() {
  createCanvas(600, 600);
}

function draw() {
  // your code here
}
```

## Variables

**(3)** Let's do this one as a group:

```javascript
var x = 4;      
var y = 2;
var z = x + y;    // z =
x = x + x + z;    // x =
y = z * 2;        // y =
z--;              // z =
z *= 2;           // z =
console.log(x + z - y);   // =
```

**(4)** What is the value of x after the draw() has run three times? Put a comment next to each line of code with the value of x or y at that line.

```javascript
var x = 4;

function setup() {
  var y = x;         // y =
  x = x * 4;         // x =
  x += y;            // x =
  x *= 1;            // x =
}

function draw() {
 x++;              // after 3 runs of draw(), x =
}

```

## Functions

**(5)** Let's do this one as a group. Write  a function, **makeSuper()**, that takes an argument, *name*, and prints to the console, "[name] is super!"

Call this function inside of the text() function in order to draw the super text to the screen.

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {

}

// makeSuper() {

```

**(6)** Forgot how old you are? Calculate it!

Write a function named calculateAge that takes 2 arguments: birth year, current year, calculates the 2 possible ages based on those years, and outputs the result to the screen like so: "You are either NN or NN"

Call the function three times with different sets of values.


```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {

}

// calculateAge()

```

**(7)** Let's do this one as a group. Write a function, **getRectanglePerimeter()** that takes two arguments: side1 and side2. The function *returns* the perimeter.

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {

}

// getRectanglePerimeter()

```


**(8)** The equation for converting a temperature in Fahrenheit to Celsius is
`T(°C) = (T(°F) - 32) × 5/9`

Write a function, **fah2cel()**, that takes an argument (temperature in Fahrenheit) and *returns* the temperature in Celsius.


```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  var freezingC = fah2cel(32);
  var boilingC = fah2cel(212);
  console.log("Water freezes at " + freezingC + " degrees Celsius");
  console.log("Water boils at " + boilingC + " degrees Celsius");
}

// fah2cel()

```
