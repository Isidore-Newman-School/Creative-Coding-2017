
# Homework 2.
### Arrays, Objects Part 2

To submit this assignment:
* You may submit answers using text file(s), p5 project, or README.md.
* Save your document(s) in a folder **HW2, which should be a subdirectory of your Git repo.**
* Make sure you have **pushed your Git repo to GitHub**.
* To review submitting assignments via GitHub, checkout [Git Instructions](https://github.com/Isidore-Newman-School/Creative-Coding-F2016/tree/master/Git%20Instructions)

---

## Arrays of Objects
**(1)** Watch Daniel Shiffman (:heart_eyes:) [talk about arrays of literal objects](https://www.youtube.com/watch?v=pGkSHeEZLMU).

**(2)** Inside the setup, use a for loop to create an array- *justiceLeague* - of 5 superheroes (refer to HW1).
* The names of the superheroes should come from the array, superheroNames[].
* The health of the superheroes should be a random number between 0 and 100, (use **random()** function).
* In of draw, use a for loop to check the health of the superheroes by calling the method, **checkHealth()**.

```javascript
var superheroNames = [ /* I wonder who Ms. deBB would put here */ ];
var justiceLeague = [];

function setup() {
  createCanvas(400, 400);
  // setup code for superheroes
}

function draw() {
  // check health of superheroes
}
```


## Object Constructors
**(3)** Watch Daniel Shiffman (:heart_eyes:) [talk about object constructors](https://www.youtube.com/watch?v=F3GeM_KrGjI).

**(4)** What are object constructors? Better ways of creating objects! Object constructors are like blueprint functions that we can easily call (anywhere in the code) every time we want a new object.
* Save your current file in your HW2 folder and start a new one in the same folder. Alternatively, comment our your setup() and create a new one in the same file.
* Write a constructor function for our superhero objects: **Superhero()**. Instead of making an array of object literals, **use the constructor** to create an array of superheroes in the setup().
* This time in order to give the superheroes unique names from the superheroNames array, you will have to pass an argument to the object constructor referring to the index of the array... ask if that's confusing!


```javascript
var superheroNames = [ /* I wonder who Ms. deBB would put here */ ];
var justiceLeague = [];

function setup() {
  createCanvas(400, 400);
  // setup code using object constructors
}

function draw() {
  // check health of justice league
}

function Superhero() {
  // constructor code goes here
}
```
