---
title: JavaScript functions
layout: intro
---

# JavaScript Functions
The fundamental building blocks of JavaScript


---
title: JavaScript
level: 2
layout: center
---

Keep things Dry

* **D**o not
* **R**epeat
* **Y**ourself



---
title: JavaScript
level: 2
---

# Let's say we had an array of ages
Functions

* We have an array of ages and want to know if they are allowed to consume alcohol in Las Vegas
* If Las Vegas every changes the minimum age, or if we change our array, this code will be super annoying to maintain

```js
let listOfAges = [12, 34, 28, 21, 44, 90, 18, 20, 25];

if ( listOfAges[0] >= 21) {
  console.log('Age at Index 0 is of age')
}

if ( listOfAges[1] >= 21) {
  console.log('Age at Index 1 is of age')
}

if ( listOfAges[2] >= 21) {
  console.log('Age at Index 2 is of age')
}

...

```



---
title: JavaScript
level: 2
---

# Let's add a function to do the age check
Functions

* We can simplify this code by creating and adding a function to do our check

```js
let listOfAges = [12, 34, 28, 21, 44, 90, 18, 20, 25];

function canConsumeAlcoholInVegas(age) {
  if (age >= 21) {
    return true;
  } else {
    return false;
  }
}

if (canConsumeAlcoholInVegas(listOfAges[0])) {
  console.log('Age at Index 0 is of age')
}

if (canConsumeAlcoholInVegas(listOfAges[1])) {
  console.log('Age at Index 1 is of age')
}
...
```


---
title: JavaScript
level: 2
---

# Finally, we can make this even better for loop
Functions

* We can further simplify this code by adding a for loop

```js
let listOfAges = [12, 34, 28, 21, 44, 90, 18, 20, 25];

function canConsumeAlcoholInVegas(age) {
  if (age >= 21) {
    return true;
  } else {
    return false;
  }
}

for (let i = 0; i <= listOfAges.length; i++) {
  if (canConsumeAlcoholInVegas(listOfAges[i])) {
    console.log(`Age at Index ${i} is of age`);
  }
}
```



---
title: JavaScript
level: 2
---

# Anatomy of a function
Functions

* Functions consist of three items:
* The function keyword and the name of the function
* The parameters that are passed into the function, seperated by commas
* The code block that executes enclosed in curly braces

```js

function canConsumeAlcoholInVegas(age) {
    if (age >= 21) {
        return = true;
    } else {
        return = false; 
    }
}

console.log(canConsumeAlcoholInVegas(25)); // true

```

---
title: JavaScript
level: 2
---

# Local variables
Functions

* Function variables are "scoped", so local variables won't be available outside the function 
* In the example below, when we try to read `allowed` JavaScript will throw an error

```js

function canConsumeAlcoholInVegas(age) {
  let allowed = null; 
    
  if (age >= 21) {
    allowed = true;
  } else {
    allowed = false; 
  }
  return allowed
}

console.log(allowed); // Error!

```



---
title: JavaScript
level: 2
---

# Outer variables
Functions

* Variables declared outside of a function (in the direct parent) are made available to the function 
* In the example below, 

```js
let age = 21;

function canConsumeAlcoholInVegas() {
    let allowed = null;
    
    if (age >= 21) {
        
        allowed = true;
    } else {
        allowed = false; 
    }
    return allowed
}

console.log(canConsumeAlcoholInVegas()); // true!

```



---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Basics

* Open your JavaScript file and copy this code 
* There is an outer variable called `age` (21) and an inner variable called `age` (16)
* Try to guess which `age` variable will be used and what the output will be in the console

```js
let age = 21;

function canConsumeAlcoholInVegas() {
  let age = 16

  if (age >= 21) {
    return true;
  } else {
    return false;
  }
}

console.log(canVisitVegas()); // ????
```



---
title: JavaScript
level: 2
---

# A word about Global Variables
Functions

* Variables declared outside of a function are called "global" variables and given a global scope 
* This means that they are visible from any function, which is considered bad practice 
* Now that you know this, a much better practice is to put all of your logic and variables inside a function 



---
title: JavaScript
level: 2
---

# Function parameters 
Functions

* We can pass in any number of parameters to the function
* Order of parameters is extremely important when calling the function

```js
function displayTodoItem(title, done) {
    console.log(`ToDo Title: ${title}, Todo Done Status: ${done}`)
}

displayTodoItem("Buy Groceries", false);
displayTodoItem("Order Uber Eats", true);
displayTodoItem("Call Mom", false);
displayTodoItem("File taxes", false);

```



---
title: JavaScript
level: 2
---

# Setting default parameters 
Functions


* We can set the `done` parameter to have a default value of `false` so if someone calls the function with only one parameter we can set `done` to `false`

```js
function displayTodoItem(title, done = false) {
  console.log(`ToDo Title: ${title}, Todo Done Status: ${done}`)
}

displayTodoItem("Buy Groceries");
displayTodoItem("Order Uber Eats");
displayTodoItem("Call Mom");
displayTodoItem("File taxes");

```


---
title: JavaScript
level: 2
---

# Checking parameters
Functions


* Here is another way to check incoming parameters

```js
function displayTodoItem(title, done) {
  // Check the value of done before using it in the console.log
  if (done === undefined) {
    done = false;
  }
  console.log(`ToDo Title: ${title}, Todo Done Status: ${done}`)
}

displayTodoItem("Buy Groceries");
displayTodoItem("Order Uber Eats");
displayTodoItem("Call Mom");
displayTodoItem("File taxes");

```




---
title: JavaScript
level: 2
---

# Returning values
Functions


* A function can return a value back into the calling code as the result.

```js
function addNumbers(a, b) {
  return (a+b);
}

let result = addNumbers(300,400);

console.log(result);
```


---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try!
Functions

* Add code to the `screamMessage` below which loops for the amount of times as defined by count 
* For each loop, make the `message` that was provided completely uppercase 
* So your code below would result in "I DON'T LIKE HOTPINK" (x3) and 
"I DON'T WANT TO FILE MY TAXES" (x5)
* Hint: string methods toUpperCase is your friend 

```js
function screamMessage(count, message) {
    // Add your logic here
}

console.log(screamMessage(3,"I don't like HotPink"));
console.log(screamMessage(5,"I don't want to file my taxes"));

```
