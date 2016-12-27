
# Quiz 1 Solutions. Arrays and Objects

---

TOTAL POINTS = 45

**(0) 5pts** How do we print, "Bernie was spotted in WalMart" using dot/array notation with the clowns array?

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
  console.log(clowns[2].name + " was spotted at " + clowns[2].location.spotted);
}
```

**(1) 15pts** Write a function, **ratioSweetFruits()** that takes an array of fruit objects as an argument. The function returns the ratio of sweet to non-sweet fruits.

```javascript
var fruits = [{fruit: "apple", sweet: true},{fruit: "tomato", sweet: false},{fruit: "pear", sweet: true}, {fruit:"lemon", sweet: false}, {fruit:"grape", sweet: true}];

function setup() {
  console.log(ratioSweetFruits(fruits));  // prints 1.5 = 3/2
}

function ratioSweetFruits(arr) {
  var sweet = 0;
  for (var i = 0; i < arr.length; i++) {
     if (fruits[i].sweet) {
        sweet++;
     }
  }
  return sweet/(arr.length-sweet);
}

```

**(2) 15pts** Create an object constructor, Politician, that has takes three arguments and sets the object properties equal to these arguments:

1. name (String)
2. party (String)
3. rating (number - 0 to 100)

The object should also have a method:

* oopsie()
  * approval rating decreases by 30 points.
  * approvalRating should not get below 0.

**(3) 10pts** Use the object constructor to create two politicians.

```javascript
var politicians = [];

function setup() {
  politicians[0] =  new Politician("Hillary", "Democrat", 50);
  politicians[1] = new Politician("Trump", "Republican", 50);

  // random politician has an oopsie
  politicians[Math.floor(random(2))].oopsie();

  // print out politicians' ratings
  console.log(politicians[0].name + " " + politicians[0].rating + "%")
  console.log(politicians[1].name + " " + politicians[1].rating + "%")
}

// your object constructor here
function Politician(name, party, rating) {
   this.name = name;
   this.party = party;
   this.rating = rating;

   this.oopsie = function() {
      this.rating -= 30;
      if (this.rating < 0) this.rating = 0;
   }
}
```
