# 2. Notes on Conditionals

Additional resources / notes:
* Check out the section on conditionals in [JavaScript Basics](https://github.com/robynitp/networkedmedia/wiki/Javascript-Basics#conditionals)

---

### if / else

We can use conditionals to make an ellipse blue if the mouse is on the left half of the canvas, and red if it's on the right side of the canvas:

```JavaScript
function setup() {
    createCanvas(400, 400);
}

function draw() {

   if (mouseX < width/2) {
      fill(0, 0, 255);
   }
   else {
      fill (255, 0, 0);
   }

   ellipse(width/2, height/2, 100, 100);

}
```

---

<a name="ex0"></a>
<pre>
<b>Exercise 0:</b>
So far we've looked at two data types: numbers and strings ("hello!"). <b>Booleans</b> store <b>true</b>
or <b>false</b>. We can create variables and assign them to booleans:
</pre>

  ```javascript
  var b1 = false;
  var b2 = true;
  ```
<pre> On the <a href="https://p5js.org/reference/">reference</a> page under "Events", look for
<b>two built-in variables</b>- one under keyboard and one under mouse- that are booleans.
</pre>

<a name="ex1"></a>
<pre>
<b>Exercise 1:</b>
Look up the boolean variable, mouseIsPressed, and the text() function in the <a href="https://p5js.org/reference/">reference</a>.

Replicate <a href="https://jennadeboisblanc.github.io/examples/c4e0/">this example</a>.
</pre>

![click me image](images/clickme.png)

---

### if / else if / else

If we want to write a function printSign() that takes a single argument and that prints whether the value is positive, neither (zero), or negative:

```JavaScript
function setup() {
    createCanvas(400, 400);
}

function draw() {
   printSign(50);
   printSign(0);
   printSign(-10);
}

function printSign(val) {
   if (val > 0) {
      console.log(val + " is Positive!");
   }
   else if (val === 0) {
      console.log(val + " is Neither!");
   }
   else {
      console.log(val + " is Negative!");
   }
}
```

---

<a name="ex1"></a>
<pre>

Write a simple program that changes the location of a rectangle on the screen when
the arrow keys are pressed. <a href="https://jennadeboisblanc.github.io/examples/c4e1/">Here's an example</a>.

1. use the code below
2. read the <a href="https://p5js.org/reference/#/p5/keyPressed">keyPressed()</a> reference
3. write an if / else if / else statement

</pre>


```javascript
var x = 0;
var y = 0;

function setup() {
    createCanvas(400, 400);
}

function draw() {
    background(150);
    rect(x, y, 30, 30);
}

function keyPressed() {
    // your code here
}
```

---

### "===" operator
If we're testing if two numbers are equal we can use the "==" operator. If we want to compare the string "5" to the number 5, the "==" operator will convert the string to a number before comparison. In this case, it will say that "5" is equal to 5.

The "===" operator, on the other hand, tests if the two values are of the same value *and the same type*.

```JavaScript
5 == 5       // true
"5" == 5     // true
"5" === 5    // false
```


### multiple conditions
We can use [logical operators](https://github.com/robynitp/networkedmedia/wiki/Javascript-Basics#operators) to make compound conditional statements.

For example, we can use the logical "&&" operator to test if x is between -5 **AND** 5:

```JavaScript
// from JavaScript Basics (see link above)
var x = 1;
if (x > -5 && x < 5) {
  // execute some code!
}
```

To check if x equals 5 **OR** 3:

```javascript
var x = 3;
if (x === 3 || x === 5) {
  // execute some code!
}
```

<a name="ex2"></a>
<pre>
<b>Exercise 2:</b>
Use the || operator  
</pre>
