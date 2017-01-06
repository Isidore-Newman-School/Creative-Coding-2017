# 0. Variables and Drawing

Modify the **sketch.js** file to create a snowman using 3 ellipses. Use variables correctly so that the snowman:

1. moves as a unit when the variables "x" and "y" are changed
2. scales appropriately when the "multiplier" variable is adjusted

```javascript
/**
* When these values are modified,
* the snowman must be preserved
*/

var x = 400;
var y = 400;
var multiplier = 1.0;


function setup() {
  createCanvas(500,500);
}

function draw() {
  background(200);

  // build the snowman!

}
```

## Extra Challenge

If you finished the basic snowman during class, experiment with other drawing functions like [line()](https://p5js.org/reference/#/p5/line) or [rect()](https://p5js.org/reference/#/p5/rect) to give the snowman arms, a hat, or nose! Check out [beginShape()](https://p5js.org/reference/#/p5/beginShape) for creating custom shapes!

![alt text](https://github.com/Isidore-Newman-School/Creative-Coding-F2016/blob/master/Classwork/c0_variables/snowmen.png)
