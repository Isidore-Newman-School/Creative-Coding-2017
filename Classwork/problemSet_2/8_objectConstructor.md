# 8. Object Constructors

Topics
* [I. Built-in variables](#i-built-in-variables)
* [II. Operators](#ii-operators)
* [III. Variable Scope](#iii-variable-scope)

Exercises
* [Exercise 0. background()](#ex0)
* [Exercise 1. mouseX and mouseY](#ex1)
* [Exercise 2. Concatenation](#ex2)
* [Exercise 3. Operators](#ex3)

---

## I. Object Constructors
Sometimes we want to create many different objects quickly and easily. This is where object constructors come in. Unlike object literals, object constructors are functions that can be called multiple times to make multiple copies or "instances" of the object.

```javascript
// declare bubbles
var bubble0;
var bubble1;

function setup() {
  // create bubbles
  bubble0 = new bubble();
  bubble1 = new bubble();
}

function draw() {
  ellipse(bubble0.x, bubble0.y, bubble0.diameter);
  ellipse(bubble1.x, bubble1.y, bubble1.diameter);
}

// bubble constructor
function Bubble() {
  this.x = random(0, width);
  this.y = random(0, height);
  this.diameter = random(10, 30);
}

```


#### new Keyword
Now that we have an object constructor, let's use it to create some bubbles.

1. Declare empty variables above the setup() so that our bubbles have [global scope](../problemSet_0/2_variables.md)
We create copies of the objects by calling the constructor with the **new** keyword.

For example, to create two bubbles with random positions and diameters:

```javascript
// declare bubbles
var bubble0;
var bubble1;

function setup() {
  // create bubbles
  bubble0 = new bubble();
  bubble1 = new bubble();
}

function draw() {
  ellipse(bubble0.x, bubble0.y, bubble0.diameter);
  ellipse(bubble1.x, bubble1.y, bubble1.diameter);
}

// bubble constructor
function Bubble() {
  this.x = random(0, width);
  this.y = random(0, height);
  this.diameter = random(10, 30);
}

```

---

<a name="ex0"></a>
<pre>
<b>Exercise 0:</b>
Create two more bubbles using the bubble object constructor above. Display these bubbles on the screen.
</pre>

---

## II. Passing Values to Object Constructors
In the previous example the bubble constructor sets the x and y values of the bubbles to random values. What if instead we'd like to *pass* values to x and y? We can pass values just like we passed values to other functions.

1. When we create the bubble object with *new*, that's when we pass in values.
2. In our object construction declaration (`function bubble( /* values here */)`) we must declare parameters in the parentheses
3. We use these same parameters inside of the object constructor to define fields

```javascript
// declare bubbles
var bubble0;
var bubble1;

function setup() {
  // create bubbles with arguments
  bubble0 = new bubble(100, 200, 50);
  bubble1 = new bubble(200, 200, 100);
}

function draw() {
  ellipse(bubble0.x, bubble0.y, bubble0.diameter);
  ellipse(bubble1.x, bubble1.y, bubble1.diameter);
}

// bubble constructor with parameters
function Bubble(x, y, diameter) {
  this.x = x;
  this.y = y;
  this.diameter = diameter;
}

```


## II. Methods in Object Constructors
Now let's add a *method* **display()** that draws the bubble at the current x and y values.

1. When we declare the method below, we have to use the *this* keyword in order to specify the x and y that are specific to **this** particular bubble.
2. We call the method in the `draw()` using dot notation.

```javascript
// declare bubbles
var bubble0;
var bubble1;

function setup() {
  createCanvas(400, 400);
  // create bubbles
  bubble0 = new bubble();
  bubble1 = new bubble();
}

function draw() {
  bubble0.display();
  bubble1.display();
}

// bubble constructor
function Bubble() {
  this.x = random(0, width);
  this.y = random(0, height);
  this.diameter = random(10, 30);

  this.display = function() {
    ellipse(this.x, this.y, this.diameter, this.diameter);
  };
}

```


<a name="ex2"></a>
<pre>
<b>Exercise 2:</b>
Create an object constructor, Pokemon(), that has three parameters:
1. name
2. hp
3. bestMove

and sets fields in the object constructor equal to these parameters.
</pre>


```javascript
var pokemon;

function setup() {
  pokemon = // create a new object here with object constructor
  console.log(pokemon);
}


function Pokemon(name, hp, bestMove) {
  // define object constructor fields here
}
```

---

**(4)** Now add a **move()** method to the object that increments the x value by 1 if movingPositive is true; otherwise, it decrements x by 1. If the ball reaches the edge, the value of movingPositive is flipped so that the ball begins to move in the opposite direction. Test out this method in the draw function.

```javascript
function draw() {
  ball.display();
  ball.move();
}
```
