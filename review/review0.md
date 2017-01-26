# Review 0

## Variables

Let's do this one as a group:

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

---

**(0)** What is the value of x after the draw() has run three times? Put a comment next to each line of code with the value of x or y at that line.

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

**(1)** Name 4 built-in variables that we've explored so far.

---

## Functions

Let's do this one as a group. Write  a function, **makeSuper()**, that takes an argument, *name*, and prints to the console, "[name] is super!"

Call this function inside of the text() function in order to draw the super text to the screen.


```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {

}

// makeSuper() {

```

---

**(0)** Forgot how old you are? Calculate it!

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
