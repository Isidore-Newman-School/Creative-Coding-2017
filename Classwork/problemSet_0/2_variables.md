# 2. Built-in Variables, Strings, Operators

Topics
* [I. Built-in variables](#i-built-in-variables)
* [II. Operators](#ii-operators)
* [III. Variable Scope](#iii-variable-scope)

Exercises
* [Exercise 0. background()](#ex0)
* [Exercise 1. mouseX and mouseY](#ex1)
* [Exercise 2. Concatenation](#ex2)
* [Exercise 3. Operators](#ex3)
* [Exercise 4. Scope](#ex4)

---

## I. Built-in variables
So far we've looked at how to create our own variables, but there are a variety of "environment" variables that come with the p5 library (check the [p5 reference](https://p5js.org/reference/) under environment).

What happens when you put the following line of code inside of your draw()?

```JavaScript
ellipse(mouseX, mouseY, 50, 50);
```

What do `width` and `height` represent?

```JavaScript
ellipse(width/2, height/2, 50, 50);   
```

---

<a name="ex0"></a>
<pre>
<b>Exercise 0:</b>
In the code below, test the placement of background(). How does the placement affect the output? Why?

</pre>

```javascript
function setup() {
  createCanvas(600, 600);
  // background(200);
}

function draw() {
  // background(200);
  ellipse(mouseX, mouseY, 30, 30);
}
```

<a name="ex1"></a>
<pre>
<b>Exercise 1:</b>
1. Use the built-in variables: mouseX, mouseY, width, and height.
2. Write a sketch that exhibits the behavior <a href="https://jennadeboisblanc.github.io/examples/c0d2e1/">in this example</a>.

Ask Ms. deBB if you need hints.
</pre>

[![alt text](images/bar.png)](https://jennadeboisblanc.github.io/examples/c0d2e1/)

---

## II. Operators

So far we've only looked at variables that are numbers. Strings are variables that store text.

```JavaScript
var firstName = "Jenna";
var lastName = "deBoisblanc";
```

Just like with numbers, we can use the "+" operator on strings. In this case, the addition operator *concatenates* the strings.

```javascript
var firstName = "Jenna";
var lastName = "deBoisblanc";
console.log(firstName + " " + lastName + " rocks!");  // Jenna deBoisblanc rocks!
```
---

<a name="ex2"></a>
<pre>
<b>Exercise 2:</b>
It's also possible to use the "+" operator to concatenate strings with numbers,
although the order of the terms matters.

In the code below, answer question 1-6 in the comments below.

Check answers with Ms. deBB before moving forward.
</pre>

```javascript
console.log(7 + 7 + 7);         // 1. what is the output?
console.log(7 + 7 + "7");       // 2. what is the output?
console.log("7" + 7 + 7);       // 3. what is the output?
console.log("7" + (7 + 7));     // 4. what is the output?

/*

5. How does the placement of the strings impact the result?


6. How/why do you think the result changes when there are parentheses?


*/
```
---

Check out some of the other math operators in [JavaScript Basics](https://github.com/robynitp/networkedmedia/wiki/Javascript-Basics).

We will go over some of the more common operators, beginning with the "=" or "assignment" operator. Unlike in math, the following statement is valid:

```javascript
var x = 3;
x = x + 5;
console.log(x);
```
We are NOT saying "x is *equal to* x + 5," because that is invalid. Rather, we are "*assigning*" the value of x plus 5 (which happens to equal 8) to the variable x. Subtle difference.

The following code is shorthand for `x = x + 5`, or *add 5 to the existing value of x*:

```javascript
x += 5;
```

There are several other operators that work in the same way:

```javascript
var x = 10;
x -= 8;        // x = 2 (subtract 8 from the existing value of x)

var x = 10;
x *= 3;        // x = 30 (multiply the existing value of x times 3)


var x = 10;
x /= 2;        // x = 5  (divide the existing value of x by 2)
```

The following code is shorthand for `x = x+1` and `x = x-1` respectively:

```javascript
var x = 5;
x++;        // x = 6 (increment x by 1)

var x = 5;
x--;        // x = 4 (decrement x by 1)
```

---

<a name="ex3"></a>
<pre>
<b>Exercise 3:</b>
Fill out the comments below. Be prepared to answer questions like these with pencil and paper on quizzes.
</pre>

```javascript       
var x = 5;              
var y = 1;              
x = x + x + y;          // 1. x = ?
y = x * 2;              // 2. y = ?    
x = 5;  
x *= 2;                 // 3. x = ?
y++;                    // 4. y = ?
console.log(x + "6" + (x + y));     // 5.  = ?   
```

---

## III. Variable Scope
In JavaScript, "scope" is the set of variables, objects, and functions that you can access. JavaScript has two scopes:

1. **global scope** - global variables are declared *outside of functions* (i.e. at the top) and are therefore available to be used *anywhere* in your sketch. Notice that `a` is logged in both the `setup()` and `loop()`.

  ```javascript
  var a = 10;     // global variable

  function setup() {
    console.log(a)      // 10
    a = 5;
  }

  function draw() {
    console.log(a);     // 5
  }
  ```

2. **local (or function) scope** - local variables are declared *inside of functions* (which is why it's also function scope). These variables are only available to be used in the function where they are declared.

  ```javascript
  function setup() {
    var a = 5;        // local variable
    console.log(a);   // 5
  }

  function draw() {
    console.log(a);   // undefined
  }
  ```


**NOTE** It is good programming process to *avoid the use of global variables* if you can.

---

<a name="ex4"></a>
<pre>
<b>Exercise 4:</b>
Fill in the comments below:
</pre>

```javascript
var x = 10;           // global or local?

function setup() {
  var y = 3;          // global or local?
  console.log(x);     // what do x, y, and z equal?
  console.log(y);
  console.log(z);
  doStuff();
  console.log(x);     // what do x, y, and z equal?
  console.log(y);
  console.log(z);

}

function draw() {
  console.log(x);     // what do x, y, and z equal?
  console.log(y);
  console.log(z);
}

function doStuff() {
  var z = 5;          // global or local?
  x = z;              // global or local?
  var y = z;          // global or local?

  console.log(x);     // what do x, y, and z equal?
  console.log(y);
  console.log(z);
}
```
