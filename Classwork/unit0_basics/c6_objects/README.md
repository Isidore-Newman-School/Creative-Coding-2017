# c6. Objects

> "Numbers, Booleans, and strings are the bricks that data structures are built from. But you can’t make much of a house out of a single brick. Objects allow us to group values—including other objects—together and thus build more complex structures."
>
> [*Eloquent JavaScript*](http://eloquentjavascript.net/04_data.html)

## Creating Object Literals
We will be discussing object literals- "a comma-separated list of name-value pairs wrapped in curly braces. Object literals encapsulate data, enclosing it in a tidy package" ([citation](http://www.dyn-web.com/tutorials/object-literal/)).

Like an array, an object is used to store a variety of information. To initialize an object, we use curly brackets:

```javascript
var yoda = {};
```

We can also define properties- including arrays and other objects- when we create objects:

```javascript
var yoda = {
   name: "Yoda",
   age: 957,
   planet: "Dagobah",
   quotes: ["Me so silly!", "Me Jedi!"],
   friend: {
      name: "Luke",
      relationship: "padawan"
   }
};
```

## Dot Notation
It's possible to add or change properties using *dot notation* once the object has been created:

```javascript
yoda.lightSaberColor = "green"; // added new property
yoda.age = "invincible";        // updated age
```

You also use *dot notation* to access properties, even nested objects, in the object:

```javascript
console.log(yoda.age);        // prints "invincible"
console.log(yoda.friend.name) // prints "Luke"
```

Or to access items inside of nested arrays:

```javascript
console.log(yoda.quotes[0]);  // prints "Me so silly!"
```

## Adding Methods

Methods are functions inside of objects. It's useful sometimes to have functions specific to an object:

```javascript
var yoda = {
   name: 'Yoda',
   age: 957,
   planet: 'Dagobah',
   useTheForce: function(){
      console.log("Using the force, I AM!");
   }
};
```

To use a method associated with an object, we employ dot notation with the function:

```javascript
yoda.useTheForce();   // "Using the force, I AM!"
```

It's also possible to add methods to existing objects:

```javascript
yoda.callItLikeItIs() = function() {
  console.log("The fear of loss is a path to the dark side.");
}

yoda.callItLikeItIs();  // prints "The fear of loss is a path to the dark side."
```

## this keyword
If you'd like your method to operate on the object's own properties (for example, if you'd like to write a method to change Yoda's planet when he travels), you have to use the *this* keyword:

```javascript
var yoda = {
   name: "Yoda",
   age: 957,
   planet: "Dagobah",
   travelingTo: function(destination) {
      this.planet = destination;
   }
};

console.log(yoda.planet);       // prints "Dagobah"
yoda.travelingTo("Death Star");
console.log(yoda.planet);       // prints "Death Star"
```

## Object Constructors
Sometimes we want to create many different objects quickly and easily. This is where object constructors come in. Unlike object literals, object constructors are functions that can be called multiple times to make multiple copies or "instances" of the object. We create copies of the objects by calling the constructor with the **new** keyword. For example:

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
  // draw and move bubbles
  bubble0.move();
  bubble1.move();

  bubble0.display();
  bubble1.display();
}

// bubble constructor
function bubble() {
  this.x = random(0, width);
  this.y = random(0, height);
  this.diameter = random(10, 30);
  this.speed = 1;

  this.move = function() {
    this.x += random(-this.speed, this.speed);
    this.y += random(-this.speed, this.speed);
  };

  this.display = function() {
    ellipse(this.x, this.y, this.diameter, this.diameter);
  };
}

```

## Array of Objects
As we've seen, objects can contain arrays as a property, but the reverse is also true! Sometimes we want to keep track of an ordered list of objects, which is where arrays come in handy.

Let's create an object constructor for a taco object, and then let's add 10 tacos to an array called "tacos".

```javascript
var tacos = [];

function setup() {
  for (var i = 0; i < 10; i++) {
    tacos[i] = new Taco();
  }
  console.log(tacos);
}

function draw() {}

function Taco() {
  this.yummy = true;
  this.type = "pork";
  this.eatMe = function() {
    console.log("I taste so yummy.");
  }
}
```

---

## Exercises
**(1)** Create an object **ball{}** that has the following number properties: x, y, diameter. It also has a boolean property- movingPositive - set to true.

**(2)** Check out [**keyPressed()**](https://p5js.org/reference/#/p5/keyPressed). Use the arrow keys to increment or decrement the values of x and y so that the ball moves when the keys are pressed.

**(3)**Now add a *method* **display()** that draws the ball at the current x and y values. Make sure to use the *this* keyword. Test out the method:

```javascript
// declare object here

function setup() {
  createCanvas(400, 400);
}

function draw() {
  ball.display();
}
```

**(4)** Now add a **move()** method to the object that increments the x value by 1 if movingPositive is true; otherwise, it decrements x by 1. If the ball reaches the edge, the value of movingPositive is flipped so that the ball begins to move in the opposite direction. Test out this method in the draw function.

```javascript
function draw() {
  ball.display();
  ball.move();
}
```
