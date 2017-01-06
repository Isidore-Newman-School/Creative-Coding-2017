# 0. Notes on Variables and Drawing

Additional resources:  
* [**p5.js reference**](http://p5js.org/reference/)
* Check out the the section on variables and data types in [JavaScript Basics](https://github.com/robynitp/networkedmedia/wiki/Javascript-Basics)
* [Daniel Shiffman explains variables](https://www.youtube.com/watch?v=RnS0YNuLfQQ)
* [Daniel Shiffman makes his own variables](https://www.youtube.com/watch?v=Bn_B3T_Vbxs)


### Assigning numbers to variables
There are six different types of variables in JavaScript: numbers, strings, booleans, objects, functions, and undefined values. 

```JavaScript
var x = 100;
var y = 70.7;                
```

JavaScript is **loosely-typed**, which (if you're familiar with languages like Java or C++) means that you don't need to declare a variable "type"; all types of variables are declared with "var." For example:

```JavaScript
var x = 10;
var message = "Hello World!";     // string
var isHappy = true;               // boolean
```

Why use variables? To make code more readable and portable (easy to change).

### Built-in variables
```JavaScript
// mouseX and mouseY are automatically assigned the coordinates of the cursor
ellipse(mouseX, mouseY, 50, 50);

// width and height are automatically assigned the height/width of the canvas
ellipse(width/2, height/2, 50, 50);   
```

### Arithmetic with variables

We'll use **console.log()** to print values to the console so that we can test arithmetic on variables.

```JavaScript
var x = 5;
console.log(x + 5);     // 10
console.log(x * 5);     // 25
```

The "+" operator can be used to concatenate strings or numbers:

```JavaScript
var name = "Jenna";
console.log(name + " rocks!");

// concatenating with numbers and strings
console.log(7 + 7 + 7);          // 21
console.log(7 + 7 + "7");        // 147
console.log("7" + 7 + 7);        // 777
```

### Operators
Check out some of the other math operators in [JavaScript Basics](https://github.com/robynitp/networkedmedia/wiki/Javascript-Basics).
