# 2. Notes on Conditionals

Additional resources / notes:
* Check out the section on conditionals in [JavaScript Basics](https://github.com/robynitp/networkedmedia/wiki/Javascript-Basics#conditionals)

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
Look up the boolean variable, mouseIsPressed, and the text() function in the <a href="https://p5js.org/reference/">reference</a>.

Replicate <a href="https://jennadeboisblanc.github.io/examples/c4e0/">this example</a>.
</pre>


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
   else if (val == 0) {
      console.log(val + " is Neither!");
   }
   else {
      console.log(val + " is Negative!");
   }
}
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
if (x == 3 || x == 5) {
  // execute some code!
}
```

### "===" operator
If we're testing if two numbers are equal we can use the "==" operator. If we want to compare the string "5" to the number 5, the "==" operator will convert the string to a number before comparison. In this case, it will say that "5" is equal to 5.

The "===" operator, on the other hand, tests if the two values are of the same value *and the same type*.

```JavaScript
5 == 5       // true
"5" == 5     // true
"5" === 5    // false
```

### Booleans
So far we've looked at two data types: numbers and strings ("hello!"). Booleans store **true** or **false**. We can create variables and assign them to booleans:

```javascript
var x = false;
if (x) {
  // execute code!
}
```

The following code snippet is equivalent to the previous :

```javascript
var x = false;
if (x == true) {
  // execute code!
}
```
