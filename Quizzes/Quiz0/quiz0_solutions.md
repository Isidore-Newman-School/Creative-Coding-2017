# Quiz 0. Solutions
### Variables, Functions, Conditionals, Loops

**(1)** In the following code, what is printed to the console?  

```javascript
var x = 4;
var y = 2;
var z = x + y;    // z = 6
x = x + x + z;    // x = 4 + 4 + 6 = 14
y = z * 2;        // y = 6 * 2 = 12
z--;              // z = 5
console.log(x + z - y); // 14 + 5 - 12 = 7
```

**(2)** What are the three types of variables we've explored so far?

* numbers
* booleans
* strings
* arrays
* objects

---

**(3)** Write a function, **didGreeniesWin()**, that takes three arguments- Newman's opponent, Newman's score, and the opponent's score. If Newman won, print to the console, "Greenies are victorious!". If the Greenies tied, print "Greenies tied with [insert opponent]." Otherwise print, "Sad day indeed. [Insert opponent] won."

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  didGreeniesWin("Pope John Paul II", 21, 14);
  didGreeniesWin("Jesuit", 3, 40);
}

function didGreeniesWin(opponent, newmanScore, opponentScore) {
  if (newmanScore > opponentScore) {
    console.log("Greenies are victorious!");

  } else if (newmanScore === opponentScore) {
    console.log("The Greenies tied with " + opponent + ".");

  } else {
    console.log("Sad day indeed. " + opponent + " won.");
  }
}
```

**(4)** Write a function, **sumRange()**, that takes two arguments- a start and an end- and *returns* the sum of the range beginning with the start and (including) the end.

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  console.log(sumRange(1, 3));  // prints 6 = 1 + 2 + 3
}

function sumRange(start, end) {
  var range = 0;
  for (var i = start; i <= end; i++) {
    range += i;
  }
  return range;
}
```


**(5)** Write a function, checker(), that uses a for loop and conditional logic to create the following image:

![alt text](checker.png)    

```javascript
function setup() {
  createCanvas(400, 400);
  colorMode(HSB, 10);
}

function draw() {
  checker();
}

function checker() {
  for (i = 0; i < 10; i++) {
    if(i%2 === 0){             
      fill(0);
    }
    else{
      fill(10);       
    }
    stroke(i, 10, 10);
    rect(i*40, 200, 40, 40);
  }
}
```    
