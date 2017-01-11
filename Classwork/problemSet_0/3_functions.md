# c1. Functions

Topics
* [I. Abstraction](#i-abstraction)
* [II. Passing Arguments](#ii-passing-arguments)
* [III. Returning Values](#iii-returning-values)

Exercises
* [Exercise 0. goGreenies()](#ex0)
* [Exercise 1. madLib()](#ex1)
* [Exercise 2. multiply()](#ex2)

---

## I. Abstraction
Functions are important in computer science for:
* making code easier to read and understand
* preventing code repetition

*Abstraction* in computer science is the process of organizing complex procedures into discrete, simple units. Writing functions is one example of abstraction at play: by grouping lines of code under the heading of a function name, we abstract away some of the complexity of code.

As an example, the function **newmanColors()** is an easy way to designate that we'll apply Newman colors to shapes. It sets the stroke to Newman green and the fill to white.

```javascript
function setup() {
    createCanvas(400, 400);
}

function draw() {
    newmanColors();
    ellipse(100, 100, 50, 50);
}

function newmanColors() {
    stroke(0, 255, 0);
    fill(255);
}
```

---

<a name="ex0"></a>
<pre>
<b>Exercise 0:</b>
Write a function, <b>goGreenies()</b>, that prints to the console, "Go Greenies!" and draws a green ellipse where the cursor is. Call this function in the draw().
</pre>

```javascript
function setup() {
    createCanvas(400, 400);
}

function draw() {
    // call your function here
}

// define your function here
```

---

## II. Passing Arguments
To pass arguments to functions, we must declare **parameters** (the variables in the parentheses of the function definition). For example, to pass two variables to the function **add()**:

```javascript
function setup() {
    createCanvas(400, 400);
}

function draw() {
    add(100, 20);   // 100 and 20 are arguments
}

function add(val1, val2) {  // val1 and val2 are parameters
    console.log(val1 + val2);
}
```

---

<a name="ex1"></a>
<pre>
<b>Exercise 1:</b>
Write a function <b>madLib()</b> that takes 4 strings as arguments (noun, adjective, verb, noun), creates a story, and prints the story to the console.
</pre>

```javascript

function setup() {
    createCanvas(400, 400);
}

function draw() {
    madLib( /* noun, adjective, verb, noun*/ );
}

// define madLib() function here

```

---

## III. Returning Values

We can use *return* to specify that functions should store a value in memory after they are called. Returning values is useful if you'd like a function to perform a calculation and use that calculation in your code.

For example, instead of printing the sum of two values, we can define our **add()** function to return the sum:

```javascript
function setup() {
    createCanvas(400, 400);
}

function draw() {
    var sum = add(100, 20);   // we can set sum equal to add() b/c it returns a value
    console.log(sum);
}

function add(val1, val2) {
    return(val1 + val2);
}
```

---

<a name="ex2"></a>
<pre>
<b>Exercise 2:</b>
Write a function <b>multiply()</b> that has two parameters and <em>returns</em> their product.
Use the <b>multiply()</b> function inside of the text() function to
display the product of two values on the canvas.

</pre>

```javascript

function setup() {
    createCanvas(400, 400);
}

function draw() {
    var v1 = 5;
    var v2 = 3;
    text(v1 + " * " + v2 + " = ", 100, 80);
    text( /* code goes here */ );
}

// define multiply function here

```
