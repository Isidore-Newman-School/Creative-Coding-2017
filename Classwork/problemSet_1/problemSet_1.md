# Problem Set 1

Problem sets should be completed **individually**, but *if you have questions, don't hesitate to ask Ms. deBB* for help. Problems sets are meant to cement your understanding of Javascript concepts.

**BEFORE BEGINNING ASSIGNMENT**

1. Create a new copy of the p5 project template or copy an existing p5 project
2. Copy the code [in this template](../templates/ps1_template.md) into the sketch.js file
3. Put all problem set answers into this sketch.js script

**SUBMISSION**

* Save your project in your `Github folder > Problem Sets > PS0`
* Make sure you have pushed your Git repo to GitHub
* To review submitting assignments via GitHub, [checkout Git Instructions](https://github.com/Isidore-Newman-School/Creative-Coding-S2017/blob/master/Git%20Instructions/3_submitting.md)

---

## Conditionals

**(0)** Write a function, **didGreeniesWin()**, that takes three arguments- Newman's opponent, Newman's score, and the opponent's score. If Newman won, print to the console, "Greenies are victorious!". If the Greenies tied, print "Greenies tied with [insert opponent]." Otherwise print, "Sad day indeed. [Insert opponent] won."

```javascript
function setup() {
  createCanvas(400, 400);
  didGreeniesWin("Pope John Paul II", 21, 14);
  didGreeniesWin("Jesuit", 3, 40);
}

function draw() {}

// didGreeniesWin() goes here
```


**(1)** Fill in the missing code in bounceEllipse() to make the ball bounce like in [this example](https://jennadeboisblanc.github.io/examples/ps1/).

```JavaScript
var x = 0;
var speed = 10;
var direction = 1;

function setup() {
  createCanvas(600, 600);
  colorMode(HSB, windowHeight);
}

function draw() {
  background(100, 0, 100);
  bounceEllipse();
}

function bounceEllipse() {
  // some code here

  x += speed * direction;
  ellipse(x, width/2, 50, 50);
}

```

## Loops

**(2)**

##

**(3)**
