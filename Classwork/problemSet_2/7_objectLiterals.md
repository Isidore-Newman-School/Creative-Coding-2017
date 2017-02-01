# 7. Objects (literals)

Topics
* [I. For Loops](#i-for-loops)
* [II. Nested Loops](#ii-nested-loops)
* [III. While Loops](#iii-while-loops)

Exercises
* [Exercise 0](#ex0)
* [Exercise 1](#ex1)
* [Exercise 2](#ex2)
* [Exercise 3](#ex3)
* [Exercise 4](#ex4)

---

 "Numbers, Booleans, and strings are the bricks that data structures are built from. But you can’t make much of a house out of a single brick. Objects allow us to group values—including other objects—together and thus build more complex structures."

 [*- Eloquent JavaScript*](http://eloquentjavascript.net/04_data.html)


## I. Creating Object Literals

We will be discussing object literals- "a comma-separated list of name-value pairs wrapped in curly braces. Object literals encapsulate data, enclosing it in a tidy package" ([citation](http://www.dyn-web.com/tutorials/object-literal/)).

Like an array, an object is used to store a variety of information. But unlike arrays, the data in the object does not have to be *ordered* in a list. Instead, objects have fields with values.

Let's consider an example. To initialize an object, we use curly brackets:

```javascript
var yoda = {};
```

We can also define properties- including arrays and other objects- when we create objects:

```javascript
var yoda = {
   name: "Yoda",
   age: 657,
   planet: "Dagobah",
   quotes: ["Me so silly!", "Me Jedi!"],
   friend: {
      name: "Luke",
      relationship: "padawan"
   }
};
```
---

<a name="ex0"></a>
<pre>
<b>Exercise 0:</b>
Create an object, sportsTeam, and populate it with the following key-value pairs
(e.g. name: "Greenies", ...):

1. a name (string)
2. a coach <em>object</em> with two fields: first name and last name
3. an array with three elements representing wins, ties, and losses

Check with Ms. deBB before moving forward.
</pre>

---

## II. Dot Notation
It's possible to add or change properties of an object using *dot notation* once the object has been created:

```javascript

var yoda = {
   name: "Yoda",
   age: 657,
   planet: "Dagobah",
   quotes: ["Me so silly!", "Me Jedi!"],
   friend: {
      name: "Luke",
      relationship: "padawan"
   }
};

var setup() {
  yoda.lightSaberColor = "green"; // added new property
  yoda.age = 748;                 // updated age

  console.log(yoda.age);
}

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

---

<a name="ex1"></a>
<pre>
<b>Exercise 1:</b>
In the pokemon object below, use dot notation to:
1. Add a field called "level" to each pokemon. Set level equal to 1.
2. Use dot notation (i.e. anywhere you see [] below) to print to the console:

  "[Bulbasaur] has an hp of [45], and its most powerful grass move is [seed bomb]."

</pre>

```javascript
var pokemon = {
  name: "Bulbasaur",
  type: ["grass", "poison"],
  stats: {
    hp: 45,
    attack: 49
  }
  moves: {
    normal: ["tackle", "growl"],
    grass:  ["vine whip", "sleep powder", "razor leaf", "seed bomb"]
  }
}

function setup() {}

function draw() {}
```

---

## III. Adding Methods

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

And finally, it's possible to *pass arguments* to methods:

```javascript
var yoda = {
   name: 'Yoda',
   age: 957,
   planet: 'Dagobah',
   fly: function(distance){
     if (distance > 100) {
       console.log("uh, this is the force, not a magic carpet.")
     }
      else {
        console.log("Zooming " + distance + " feet!");
      }
   }
};

function setup() {
  yoda.fly(50);
  yoda.fly(500);
}
```

---

<a name="ex2"></a>
<pre>
<b>Exercise 2:</b>
Add a method to Yoda, <b>talkToJedi()</b>, that takes an argument- a Jedi's name. The method prints,
"[Name], may the force be with you!"

Call this method in the setup with at least two Jedi names.
</pre>

---

## IV. this Keyword
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

function setup() {
  console.log(yoda.planet);         // prints "Dagobah"
  yoda.travelingTo("Death Star");
  console.log(yoda.planet);         // prints "Death Star"
}

```

---

<a name="ex3"></a>
<pre>
<b>Exercise 3:</b>
Write a method, <b>attack()</b>. When this method is called, the Pokemon's name and attack stat are printed
to the console. For example:

"[insert name] has an attack power of [insert attack stat]."

</pre>

```javascript
var pokemon = {
  name: "Bulbasaur",
  type: ["grass", "poison"],
  stats: {
    hp: 45,
    attack: 49
  }
  moves: {
    normal: ["tackle", "growl"],
    grass:  ["vine whip", "sleep powder", "razor leaf", "seed bomb"]
  }
  // your method here
}

function setup() {
  // call methods here
}

function draw() {}
```
