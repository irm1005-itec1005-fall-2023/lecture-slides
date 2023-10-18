---
title: JavaScript loops
layout: intro
---

# JavaScript Loops
Looping through things


---
title: JavaScript
level: 2
---

# We often need to repeat actions
Loops

* Loops provide us with a way to repeatedly run code
* This section covers `for` and `while` and `do..while` loops
* JavaScript also provides an endless way to loop and iterate over arrays and objects, which we will cover later on

```js
while (condition) {
  // Code block that repeats
}

do {
  // Code block that repeats
} while (condition);

for (begin; condition; step) {
  // Code block that repeats
}
```


---
title: JavaScript
level: 2
---

# While
Loops

* While the condition is truthy or evaluates to true, the code block will execute 
* Watch out for infinite loops 
* Don't forget to increment a counter in your code block 

```js
// Declare a value that we can use for the condition
let i = 0; 

// Execture the loop while i is less than 100 
while (i < 100) {
  console.log(i);
  // Increment the counter 
  i = i + 1; 
}

```


---
title: JavaScript
level: 2
---

# Do...While
Loops

* The loop is executed once no matter what the condition set in the while statement is
* After the loop runs once, the while condition is evaluated and if it is truthy or evaluates to true, the code block will execute again
* Watch out for infinite loops 
* Don't forget to increment a counter in your code block 

```js
// Declare a value that we can use for the condition
let i = 0; 

// Execture the loop while i is less than 100 
do {
  console.log(i);
  // Increment the counter 
  i = i + 1;
} while (i < 100);

```



---
title: JavaScript
level: 2
---

# For
Loops

* More complete, but less prone to coding errors, and more commonly used 

```js
for (let i = 0; i < 5; i++) {
    console.log("Counter at", i);
}
```


---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Variables

* Open your JavaScript file and copy this code 
* Add a `for` or `while` loop to walk through the array 
* Use the console to log each colour name inside that array index, except if the colour is "hotpink" then console log "NOPE"

```js
  // Declare an array
  let favouriteColours = ["purple", "blue", "hotpink", "green", "yellow"];

  // Loop through the array of favourite colours 

  // Inside the loop, use an if statement to check if a value is "hotpink"
  
  // If it's hotpink then log to the console "NOPE"
  
  // Otherwise just print the colour that is in the array index

  // Output should be ("purple", "blue", "NOPE", "green", "yellow")
```