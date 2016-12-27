
# Quiz 1. Arrays and Objects

To submit quiz:
* Save your p5 (or .js files) in a "Quiz1" folder (ideally inside of a "Quizzes" parent directory).
* To submit your quiz, push the changes to GitHub. Let me know if you have problems.

---

**(0)** How do we print, "Bernie was spotted in WalMart" using dot/array notation with the clowns array?

```javascript
var clowns = [{
      name: "Smitty",
      location: {
         current: "City Park",
         spotted: "CircleK"
      }
   }, {
      name: "Big Red",
      location: {
         current: "Uptown",
         spotted: "Mojo"
      }
   }, {
      name: "Bernie",
      location: {
         current: "Unknown",
         spotted: "WalMart"
      }
   }];

function setup() {
  console.log( /* your code here */);
}
```

**(1)** Write a function, **ratioSweetFruits()** that takes an array of fruit objects as an argument. The function returns the ratio of sweet to non-sweet fruits.

```javascript
var fruits = [{fruit: "apple", sweet: true},{fruit: "tomato", sweet: false},{fruit: "pear", sweet: true}, {fruit:"lemon", sweet: false}, {fruit:"grape", sweet: true}];

function setup() {
  console.log(ratioSweetFruits(fruits));  // prints 1.5 = 3/2
}

function ratioSweetFruits(arr) {
   // your code here
}
```

**(2)** Create an object constructor, Politician, that has takes three arguments and sets the object properties equal to these arguments:

1. name (String)
2. party (String)
3. rating (number - 0 to 100)

The object constructor should also have a method:

* oopsie()
  * approval rating decreases by 30 points.
  * approval rating should not get below 0.

**(3)** Use the object constructor from the previous question to create two politicians.

```javascript
var politicians = [];

function setup() {
  politicians[0] = // your code here
  politicians[1] = // your code here

  // random politician has an oopsie
  politicians[Math.floor(random(2))].oopsie();

  // print out politicians' ratings
  console.log(politicians[0].name + " " + politicians[0].rating + "%")
  console.log(politicians[1].name + " " + politicians[1].rating + "%")
}
```
