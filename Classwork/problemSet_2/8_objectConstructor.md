# 8. Object Constructors

Topics
* [I. Object Constructors](#i-object-constructors)
* [II. Passing Values to Object Constructors](#ii-passing-values-to-object-constructors)
* [III. Methods in Object Constructors](#iii-methods-in-object-constructors)
* [IV. Arrays of Objects](#iv-arrays-of-objects)

Exercises
* [Exercise 0. new Bubbles](#ex0)
* [Exercise 1. Bubble isPopped?](#ex1)
* [Exercise 2. Pokemon()](#ex2)
* [Exercise 3. sustainHit()](#ex3)
* [Exercise 4. Tacos](#ex3)

---

## I. Object Constructors
Sometimes we want to create many different objects quickly and easily. This is where object constructors come in. Unlike object literals, object constructors are functions that can be called multiple times to make multiple copies or "instances" of the object. You can think of an object constructor as an object *literal* factory.

**NOTE** by convention object constructors are capitalized, e.g. `Bubble()`

For example, to create a bubble object constructor that randomly assigns x, y, and diameter values when the constructor is called:

```javascript
function setup() { }

function draw() { }

// bubble constructor
function Bubble() {
  this.x = random(0, width);
  this.y = random(0, height);
  this.diameter = random(10, 30);
}
```

#### new Keyword
Now that we have an object constructor, let's use it to create some bubbles.

1. Declare empty variables above the setup() so that our bubbles have [global scope](../problemSet_0/2_variables.md#iii-variable-scope)
2. Set these variables equal to bubble objects by calling the `Bubble()` constructor with the **new** keyword

Once the bubbles are created, we can draw them by getting their coordinates with dot notation:

```javascript
// declare bubbles
var bubble0;
var bubble1;

function setup() {
  // create bubbles
  bubble0 = new Bubble();
  bubble1 = new Bubble();
}

function draw() {
  background(255);
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
  background(255);
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

---

<a name="ex1"></a>
<pre>
<b>Exercise 1:</b>
1. Add a fourth parameter to the Bubble object constructor: isPopped (boolean).
2. Set the isPopped field equal to the parameter
3. Account for this new parameter when you create the bubbles
4. Only draw the bubbles if they are not popped.
</pre>


```javascript
var bubble0;
var bubble1;

function setup() {
  bubble0 = new bubble(100, 200, 50, /* your code here */ );
  bubble1 = new bubble(200, 200, 100, /* your code here */ );
}

function draw() {
  background(255);

  // only draw them if they are not popped
  if (bubble0.isPopped == false) {
    ellipse(bubble0.x, bubble0.y, bubble0.diameter);
  }
  if (bubble1.isPopped == false) {
    ellipse(bubble1.x, bubble1.y, bubble1.diameter);
  }
}

// bubble constructor with parameters
function Bubble(x, y, diameter /* your code here */ ) {
  this.x = x;
  this.y = y;
  this.diameter = diameter;

  // code here
}
```
---

## III. Methods in Object Constructors
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
  bubble0 = new Bubble();
  bubble1 = new Bubble();
}

function draw() {
  background(255);
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

Now let's add a **move()** method that adds a random number to the x and y coordinates every time the method is called.

```javascript
// declare bubbles
var bubble0;
var bubble1;

function setup() {
  createCanvas(400, 400);
  // create bubbles
  bubble0 = new Bubble();
  bubble1 = new Bubble();
}

function draw() {
  background(255);
  bubble0.display();
  bubble1.display();
  bubble0.move();
  bubble1.move();
}

// bubble constructor
function Bubble() {
  this.x = random(0, width);
  this.y = random(0, height);
  this.diameter = random(10, 30);

  this.display = function() {
    ellipse(this.x, this.y, this.diameter, this.diameter);
  };

  this.move = function() {
    this.x += random(-5, 5);
    this.y += random(-5, 5);
  };
}
```
---

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

<a name="ex3"></a>
<pre>
<b>Exercise 3:</b>
Add a method to the Pokemon object constructor, <b>sustainHit()</b>, that has a parameter- hitAmount.
1. When this method is called, decrease the pokemon's hp (measure of its health) by the hitAmount.
2. If the health is less than 0, print to the console, "[insert name] is dead."

</pre>


```javascript
var pokemon;

function setup() {
  pokemon = // create a new object here with object constructor

  pokemon.sustainHit(30);
  pokemon.sustainHit(200);
}


function Pokemon(name, hp, bestMove) {
  // define object constructor fields here

  // sustainHit() method goes here
}
```


## IV. Arrays of Objects
As we've seen, objects can contain arrays as a property, but the reverse is also true! Sometimes we want to keep track of an ordered list of objects, which is where arrays come in handy.

Let's create an object constructor for a taco object, and then let's add 10 tacos to an array called "tacos".

```javascript
var tacos = [];

function setup() {
  createCanvas(600, 600);
  for (var i = 0; i < 10; i++) {
    tacos[i] = new Taco("pork");
  }
  console.log(tacos);
}

function draw() {
  background(255);

}

function Taco(type) {
  this.type = type;

  this.x = random(0, width);
  this.y = random(0, height);

  this.display = function() {
    fill(255, 255, 0);
    arc(this.x, this.y, 80, 80, 0, PI+QUARTER_PI, CHORD);
    fill(0);
    text(this.type, this.x, this.y);
  }
}
```

---

<a name="ex4"></a>
<pre>
<b>Exercise 4:</b>
1. In the example above, begin by calling display() for all of the taco objects in the draw().

2. The only type of taco in the tacos[] array will be "pork." How can we use the array,
  tacoTypes[] (below) to quickly create 10 different types of tacos?
</pre>

```javascript
var tacoTypes = ["pork", "chicken", "bean", "shrimp", "fish", "carnitas", "cheese", "beef", "vegetable", "breakfast"];
```
