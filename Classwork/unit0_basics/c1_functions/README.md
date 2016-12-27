# c1. Functions

### Abstraction
Functions are important in computer science for:
* making code easier to read and understand
* preventing code repetition

*Abstraction* in computer science is the process of organizing complex procedures into discrete, simple units. Writing functions is one example of abstraction at play: by grouping lines of code under the heading of a function name, we abstract away some of the complexity of code. 

As an example, the function **newmanColors()** is an easy way to designate that we'll apply newman colors to shapes. It sets the stroke to Newman green and the fill to white. 

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

### Passing Arguments
To pass arguments to functions, we must declare parameters (the variables in the parentheses of the function definition). For example, to pass two variables to the function **add()**:

```javascript
function setup() {
    createCanvas(400, 400);
}

function draw() {
    add(100, 20);
}

function add(val1, val2) {
    console.log(val1 + val2);
}
```


**EXERCISE**: Write a function **madLib()** that takes 4 strings (noun, adjective, verb, noun), creates a story, and prints the story to the console. 

```javascript

function setup() {
    createCanvas(400, 400);
}

function draw() {
    madLib( /* noun, adjective, verb, noun*/ );
}

// define madLib() function here

```

### Returning Values

We can use *return* to specify that functions should store a value in memory after they are called. Returning values is useful if you'd like a function to perform a calculation and use that calculation in your code.

For example, instead of printing the sum of two values, we can define our **add()** function to return the sum:

```javascript
function setup() {
    createCanvas(400, 400);
}

function draw() {
    add(100, 20);
}

function add(val1, val2) {
    console.log(val1 + val2);
}
```

**EXERCISE:** Write a function **multiply()** that takes two arguments and returns their product. Use the **multiply()** function inside of the text() function to display the product of two values on the canvas.

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