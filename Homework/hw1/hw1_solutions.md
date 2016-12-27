
# Homework 1.
### Arrays, Objects


## Review

**(0)** The [modulo ("%") operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators) comes in very handy in computer science. It is used to calculate the remainder after dividing two numbers. E.g.:

    5%2 = 1;
    4%2 = 0;
    3%2 = 1;
    2%2 = 0;
    1%2 = 1;
    0%2 = 0;

Use the modulo operator to write a function **isEven()** that *returns* true if the number is even and false if odd.

```javascript
function isEven(val) {
    if (val%2 === 0) {
        return true;
    }
    else {
        return false;
    }
}
```

## Arrays
**(1)** Write a function **sumEvenOdd()** that *returns* an array of two elements: the first element is the sum of all even numbers in the array, and the second is the sum of all odd numbers in the array. Use the **isEven()** function.

```javascript
function draw() {
    console.log(sumEvenOdd([1, 0, 1, 2, 3]));  // prints [2, 5]
    console.log(sumEvenOdd([1, 2, 1, 2, 0]));  // prints [4, 2]
}

function sumEvenOdd(arr) {
    var newArr = [];
    // your code here

    return newArr;
}
```

**(2)** Write a function **findMax()** that takes an array as an argument and *returns* the largest element in the array. Use a for loop. Do not use Math.max().

```javascript
function draw() {
    console.log(findMax([1, -5, 9, 6]));   // prints 9
    console.log(findMax([-1, -5, -9, -6]));   // prints -1
}

function findMax(arr) {
  var maxNum = arr[0];
  for(var i = 1; i < arr.length; i++) {
    if(arr[i] > maxNum) {
      maxNum = arr[i];  
    }
  }
  return maxNum;
}
```


## Objects

**(3)** Use dot notation to print "pine" to the console. For the quiz, be prepared to answer this question with paper and pencil.

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
    console.log(myPlants[1].list[1]);
}
```


**(4)** Create an object, **superhero{}**, with the following properties:
* name
* health (number between 0 and 100)
* a list of superpowers
* an object containing info about the enemy (name and weakness)
* a method **sustainHit()** that takes an argument (a number) and reduces the health points by that amount.  
* a method **checkHealth()** that prints to the console ("[insert superhero name here], seek medical attention!") if health is below 20.

```javascript
var superhero = {
  name: "Captain Planet",
  health: 35,
  superpowers: [
    "clean water bazooka",
    "tree lasers"
  ],
  enemy: {
    name: "Captain Pollution",
    weakness: "carbon dioxide"
  },
  sustainHit: function(num) {
    this.health -= num;
  },
  checkHealth: function() {
    if(this.health < 20) {
      console.log(this.name + ", seek medical attention!");
    }
  }  
};

function setup() {
    createCanvas(400, 400);
    superhero.sustainHit(85);
    superhero.checkHealth();   // mine prints, "Captain Planet, seek medical attention!"
}
```
