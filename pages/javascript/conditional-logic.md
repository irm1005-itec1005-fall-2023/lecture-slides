---
title: JavaScript conditional logic
layout: intro
---

# JavaScript Conditional Logic
The programming language everyone loves and absolutely hates



---
title: JavaScript
level: 2
---

# Making Decisions in JavaScript
Conditional logic

* All programming languages provide some way to make decisions and carry out actions based on those decisions
* In JavaScript this is done through Conditional statements which are code structures used to test if an expression returns true or not. 
* Code is then executed based on the results of the expression

```js
// The most basic if...else conditional statement
if (condition) {
// Code runs if condition is true
} 
else {
// Code runs if condition is false 
}
```


---
title: JavaScript
level: 2
---

# If...Else example 
Conditional logic

* Let's consider a more realistic example 

```js
// Declare my variables
let minutesBusLate = 25;
let isStartedRunning = null;

// The most basic if...else conditional statement
if (minutesBusLate > 30) {
  // Code runs if condition is true
  isStartedRunning = true;
} 
else {
  // Code runs if condition is false 
  isStartedRunning = false;
}
```


---
title: JavaScript
level: 2
---

# Comparison operators
Conditional logic

|Operator|Description|
|--------|-----------|
|!=|Not equal to|
|==|Equal to|
|===|Strictly equal to|
|!==|Not strictly equal to|
|<|Less than|
|>|Greater than|
|>=|Less than or equal to|
|>=|Greater than or equal to|


---
title: JavaScript
level: 2
---

# Comparison operators
Conditional logic

* All comparison operators return a boolean value
* `true` means yes, correct, or "the truth"
* `false` means no, wrong, or "not the truth"

```js
console.log( 10 > 8); // true (correct)
console.log( 2 == 1); // false (wrong)
console.log( 2 != 1); // true (correct)
console.log( 99 <= 99); // true (correct)
console.log( 50 <= 100); // false (wrong)

```

<!-- 
    
    Slide notes: 


    Credit: https://javascript.info/comparison

-->




---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Arrays

* Open your JavaScript file and copy this code
* We haven't looked at `functions` yet but for now don't worry about that
* Modify **line 2** only by adding a conditional that checks if the variable **`num`** is even or odd
* **HINT**: Google how to calculate an even number with JavaScript

```js
function isEven(num) {
  if (/* ADD YOUR CONDITIONAL STATEMENT HERE */) {
    console.log("Even");
  }
}

isEven(300); // Even
isEven(55); // (Blank)
isEven(44); // Even
isEven(99); // (Blank)
isEven(22); // Even
isEven(2400); // Even

```


---
title: JavaScript
level: 2
---

# Else if example 
Conditional logic

* We can use else if logic to test a number of scenarios
* The code sample below is testing different age values to determine the cost the person should pay based on their age

```js
let age = 16;
let cost = null;

if (age > 18) {
cost = 20;
} else if (age > 10) {
cost = 10;
} else if (age > 5) {
cost = 5;
} else {
cost = 0;
}
```


---
title: JavaScript
level: 2
---

# Nested conditionals
Conditional logic

* We can also test a condition based on a result of another condition
* Say we wanted to test that a user was a certain age and from a certain location

```js
let age = 19;
let stateOrProvince = "Ontario";

if (stateOrProvince === "California") {
  if (age >= 21) {
    console.log("Hello Vegas");
  } else {
    console.log("Sorry");
  }
} else if (stateOrProvince === "Ontario") {
  if (age >= 19) {
    console.log("Hello Toronto");
  } else {
    console.log("Sorry");
  }
}
```


---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Arrays

* Open your JavaScript file 
* Write conditional logic for a rating system that console logs a message based on the users rating

```js
const rating = 4;

/* If rating is 5 */ 
console.log("Excellent job");
/* If rating is 4 */ 
console.log("That's really wonderful");
/* If rating is 3 */ 
console.log("Great job");
/* If rating is 2 */ 
console.log("Awh no, that was a good try");
/* If rating is 1 */ 
console.log("Ummm, so this is awkward");

```



---
title: JavaScript
level: 2
---

# Logical operators
Conditional logic

* There are four logical operators in JavaScript
* `||` OR 
* `&&` AND 
* `!` NOT
* `??` Nullish Coalescing 



---
title: JavaScript
level: 2
---

# Logical operators - OR
Conditional logic

* The `||` OR operator tests two values or conditional statements and returns true if either are truthy

```js
let isLoggedIn = false;
let isLocalUser = true; 

if (isLoggedIn || isLocalUser) {
    console.log("The user is either local OR logged in");
}
else {
    console.log("The user is not local nor logged in");
}
```


---
title: JavaScript
level: 2
---

# Logical operators - AND
Conditional logic

* The `&&` AND operator tests two values or conditional statements and returns true if both are truthy

```js
let isLoggedIn = false;
let isLocalUser = true; 

if ( isLoggedIn && isLocalUser) {
    console.log("The user is both local AND logged in");
}
else {
    console.log("The user is either not local or not logged in, or not both");
}
```


---
title: JavaScript
level: 2
---

# Logical operators - NOT
Conditional logic

* The `!` NOT operator converts the operand to a boleant value and then returns the opposite

```js
let isLoggedIn = false;

if (!isLoggedIn) {
    console.log("The user is not logged in");
}

```

<!-- 

    Credit: https://javascript.info/logical-operators

-->



---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Arrays

* Open your JavaScript file and copy this code
* Please change the value of the `mystery` variable until your browser says "You got it" in the console
* **HINT**: Google "string indexOf" to see what it does

```js
const mystery = ''; 

if (mystery[0] === 'S' && mystery.length > 4 && mystery.indexOf('A') !== -1 ){
  console.log("YOU GOT IT!");
}
else {
  console.log("Keep trying, you can do it!")
}

```

<!-- 

    Credit: 
    
    Colt Steele
    Developer and Bootcamp Instructor

-->


---
title: JavaScript
level: 2
---

# Switch Statement
Conditional logic

* The switch statement is equivalent nesting multiple if statements

```js
let rating = 3;

switch (rating) {
  case 5: 
    console.log("Well done");
    break;
  case 4: 
    console.log("Good job");
    break;
  case 3:
    console.log("That\'s okay");
    break;
  default:
    console.log("See me after");
}

```

<!-- 

    Credit: https://javascript.info/logical-operators

-->