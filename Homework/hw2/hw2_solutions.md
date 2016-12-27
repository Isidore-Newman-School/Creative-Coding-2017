
# Homework 2.
### Arrays, Objects Part 2

## Arrays of Objects
**(1)** Watch Daniel Shiffman (:heart_eyes:) [talk about arrays of literal objects](https://www.youtube.com/watch?v=pGkSHeEZLMU).

**(2)** Inside the setup, use a for loop to create an array- *justiceLeague* - of 5 superheroes (refer to HW1).
* The names of the superheroes should come from the array, superheroNames[].
* The health of the superheroes should be random, (use **random()** function).
* In of draw, use a for loop to check the health of the superheroes by calling the method, **checkHealth()**.

```javascript
var superheroNames = [ "Captain Planet", "Captain Earth", "Captain Climate Fighter" ];
var justiceLeague = [];

function setup() {
  createCanvas(400, 400);
  for(var i = 0; i < superheroNames.length; i++) {
    justiceLeague[i] = {
      name: superheroNames[i],
      health: Math.floor(random(100)),
      superpowers: [
        "clean water bazooka",
        "tree lasers"
      ],
      enemy: {
        name: "Captain Pollution",
        weakness: "carbon dioxide"
      },
      sustainHit: function(num) {
        this.health -= num;
      },
      checkHealth: function() {
        if(this.health < 20) {
          console.log(this.name + ", seek medical attention!");
        }
      }  
    };
  }  
}

function draw() {
  for (var i = 0; i < justiceLeague.length; i++) {
    justiceLeague[i].checkHealth();
  }
}
```


## Object Constructors
**(3)** Watch Daniel Shiffman (:heart_eyes:) [talk about object constructors](https://www.youtube.com/watch?v=F3GeM_KrGjI).

**(4)** What are object constructors? Better ways of creating objects! Object constructors are like blueprint functions that we can easily call (anywhere in the code) every time we want a new object.
* Save your current file in your HW2 folder and start a new one in the same folder. Alternatively, comment our your setup() and create a new one in the same file.
* Write a constructor function for our superhero objects: **Superhero()**. Instead of making an array of object literals, **use the constructor** to create an array of superheroes in the setup().
* This time in order to give the superheroes unique names from the superheroNames array, you will have to pass an argument to the object constructor referring to the index of the array... ask if that's confusing!

```javascript
var superheroNames = [ "Captain Planet", "Captain Earth", "Captain Climate Fighter" ];
var justiceLeague = [];

function setup() {
  for (var i = 0; i < superheroNames.length; i++) {
    justiceLeague[i] = new Superhero(i);
  }
}


function draw() {
  for (var i = 0; i < justiceLeague.length; i++) {
    justiceLeague[i].checkHealth();
  }
}

function Superhero(i) {
  this.name = superheroNames[i];
  this.health = Math.floor(random(100));
  this.superpowers = [
    "clean water bazooka",
    "tree lasers"
  ];
  this.enemy = {
    name: "Captain Pollution",
    weakness: "carbon dioxide"
  };
  this.sustainHit = function(num) {
    this.health -= num;
  };
  this.checkHealth = function() {
    if(this.health < 20) {
      console.log(this.name + ", seek medical attention!");
    }
  };  
}
```
