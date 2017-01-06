# 2. Built-in Variables, Strings, Operators

Topics
* [I. Built-in variables](#built-in-variables)
* [II. The "+" Operator](#the--operator)
* [III. Other Operators](#other-operators)

Exercises
* [Exercise 0. background()](#ex0)
* [Exercise 1. mouseX and mouseY](#ex1)
* [Exercise 2. Concatenation](#ex2)
* [Exercise 3. Operators](#ex3)

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
Answer the question in the comment below:
</pre>

```javascript
/*
In the code below, test the placement of background(). How does the placement affect the output? Why?



*/

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
Write a sketch that exhibits the behavior <a href="https://jennadeboisblanc.github.io/examples/c0d2e1/">in this example</a>.

Ask Ms. deBB if you need hints.
</pre>

[![alt text](images/bar.png)](https://jennadeboisblanc.github.io/examples/c0d2e1/)

## II. The "+" Operator

So far we've only looked at variables that are numbers. Strings are variables that store text.

```JavaScript
var firstName = "Jenna";
var lastName = "deBoisblanc";
```

Just like with numbers, we can use the "+" operator on strings. In this case, the operator *concatenates* the strings.

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

## III. Other Operators
Check out some of the other math operators in [JavaScript Basics](https://github.com/robynitp/networkedmedia/wiki/Javascript-Basics).

We will go over some of the more common operators, beginning with the "=" or "assignment" operator. Unlike in math, the following statement is valid:

```javascript
var x = 3;
x = x + 5;
console.log(x);
```
We are NOT saying "x is *equal to* x + 5," because that is invalid. Rather, we are "*assigning*" the value of x plus 5 (which happens to equal 8) to the variable x. Subtle difference.

The following code is shorthand for `x = x + 5`:

```javascript
x += 5;
```

There are several other operators that work in the same way:

```javascript
var x = 10;
x -= 8;        // x = 2
x *= 3;        // x = 6
x /= 2;        // x = 3
```

The following code is shorthand for `x = x+1` and `x = x-1` respectively:

```javascript
var x = 5;
x++;        // x = 6
x--;        // x = 6
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
