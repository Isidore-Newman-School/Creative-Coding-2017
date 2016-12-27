# C3. Interactivity

Check out the [p5.js reference page on events](https://p5js.org/reference/#group-Events). What are some examples of variables or functions used to capture events from the following inputs?
* mouse
* key
* touch
* acceleration

Read the reference page and use the [keyPressed()](https://p5js.org/reference/#/p5/keyPressed) function to write a simple program that changes the location of a rectangle on the screen.

```javascript
var x = 0;
var y = 0;

function setup() {
    createCanvas(400, 400);
}

function draw() {
    background(150);
    ellipse(x, y, 30, 30);
}

function keyPressed() {
    // your code here
}
```