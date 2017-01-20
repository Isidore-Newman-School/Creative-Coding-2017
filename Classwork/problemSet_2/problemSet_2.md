# Problem Set 2

Problem sets should be completed **individually**, but *if you have questions, don't hesitate to ask Ms. deBB* for help. Problems sets are meant to cement your understanding of Javascript concepts.

**BEFORE BEGINNING ASSIGNMENT**

1. Create a new copy of the p5 project template or copy an existing p5 project
2. Copy the code [in this template](../templates/ps2_template.md) into the sketch.js file
3. Put all problem set answers into this sketch.js script

**SUBMISSION**

* Save your project in your `Github folder > Problem Sets > PS2`
* Make sure you have pushed your Git repo to GitHub
* To review submitting assignments via GitHub, [checkout Git Instructions](https://github.com/Isidore-Newman-School/Creative-Coding-S2017/blob/master/Git%20Instructions/3_submitting.md)

---

## Object Dot Notation

**(0)** Use dot notation to print "pine" to the console. For the quiz, be prepared to answer this question with paper and pencil.

```javascript
var myPlants = [
  {
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }  
];

function setup() {
    console.log( /* your code here */ );
}
```

## Arrays

**(1)** Write a function **getLastElement()** that takes an array as an argument and *returns* the last element. If the array is empty, return -1.

```javascript
function setup() {
    console.log(getLastElement([1, 0, 1, 2, 3]));  // prints 3
    console.log(getLastElement([]));  // prints -1
}

function getLastElement( /* your code here */) {
  // your code here
}
```


**(2)** Write a function **getTimesOccurring()** that has two parameters:
1. a number
2. an array of numbers

The function looks for the number (first parameter) inside of the array (second parameter) and counts how many times that number occurs in the array. The function *returns* the total count.

See below for an example.

```javascript
function setup() {
    console.log(getTimesOccurring(6, [1, -5, 6, 9, 6]));   // prints 2
    console.log(getTimesOccurring(3, [-1, -5, -6]));       // prints 0
}

function getTimesOccurring(num, arr) {
    // your code here
}
```


## Object Constructor

**(3)** Create an object constructor, **Superhero{}**, that has a single parameter - name - as well as a field for name. It also has the following fields:

1. health (randomly-generated number between 0 and 100)
2. array of superpowers
3. an object containing info about the enemy (name and weakness)
4. a method **checkHealth()** that prints to the console ("[insert superhero name here], seek medical attention!") if health is below 20.

```javascript
var superhero;

function setup() {
    createCanvas(500, 500);
    superhero = new Superhero("Spiderman");
    superhero.checkHealth();  
}

function Superhero( /* your code here */ ) {
  // your code here
}
```

## Array of Objects

**(4)** Write a function, **ratioSweetFruits()** that takes an array of fruit objects as an argument. The function returns the ratio of sweet to non-sweet fruits.

```javascript
var fruits = [{fruit: "apple", sweet: true},{fruit: "tomato", sweet: false},{fruit: "pear", sweet: true}, {fruit:"lemon", sweet: false}, {fruit:"grape", sweet: true}];

function setup() {
  console.log(ratioSweetFruits(fruits));  // prints 1.5 = 3/2
}

function ratioSweetFruits(arr) {
   // your code here
}
```
