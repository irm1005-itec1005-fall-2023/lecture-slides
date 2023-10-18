---
title: JavaScript arrays
layout: intro
---

# JavaScript Arrays
Storing javascript things in arrays


---
title: JavaScript
level: 2
---

# Arrays in JavaScript
Arrays

* Up until now we've seen primitive data types and object literals, which deal with a single variable or a collection of single name and value pairs
* The Array onject allows us to store multiple items in a single variable

```js
  // Declares an empty array 
  let myEmptyArray = [];

  // Declares an array with string values 
  let myFavouriteColoursArray = ["purple", "blue", "hotpink", "green", "yellow"];

  // Declares an array of a different data types
  let myMixedArray = ["blue", 55, false, "green"];
 
  // Output the arrays 
  console.log(myEmptyArray);
  console.log(myFavouriteColoursArray);
  console.log(myMixedArray);
```


---
title: JavaScript
level: 2
---

# Arrays in JavaScript
Arrays

* Arrays in JavaScript can be resized and can contain a mix of datatypes 
* We use an index value, starting at zero (0) to access the items in an array

```js
  // Declares an empty array 
  let myColourArray = [];

  // Array is resized to now have three (3) items inside
  myColourArray = ["purple", "blue", "hotpink"];

  // Access the second array item using the index value of 1
  myColourArray[1] = "gold";

  // Access each element using the index to output the three array items
  console.log(myColourArray[0]);
  console.log(myColourArray[1]);
  console.log(myColourArray[2]);

```

---
title: JavaScript
level: 2
---

# Arrays in JavaScript
Arrays

* You can also use the `new Array()` and `Array()` function declerations to create array
* Though this style of creating arrays is not recommended
* Use the `[]` notation when declaring arrays instead 

```js
  // Declare an empty array 
  let myEmptyArray = new Array(); // the same as []

  // Declare an array with some values 
  let myFavouriteColoursArray = new Array("purple", "blue", "hotpink", "green", "yellow");

  // Declare an array of a bunch of things - not this also works without the new keyword 
  let myMixedArray = Array("blue", 55, false, "green");
 
  // Output the arrays 
  console.log(myEmptyArray);
  console.log(myFavouriteColoursArray);
  console.log(myMixedArray);

```

---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Arrays

* Open your JavaScript file
* Copy the following starter code
* Add seven (7) numbers to the `myLotteryNumbers` array
* Run the code and see what the output

```js
  // Declare an array with your seven values
  let myLotteryNumbers = []; // ADD CODE HERE
 
  // Output the array
  console.log('The winning numbers are ', myLotteryNumbers);

```


---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Arrays

* Continuing from where you left off, you should have 7 numbers in an array
* Add `10` to the first value in the array 
* Add `100` to the last value in the array 
* Multiply by `* 3` the third value in the array 
* Run the code and see what the output is

```js
  // Declare an array with your seven values
  let myLotteryNumbers = [];

  // Modify the first value in the array by adding 10 to it
  // Modify the last value in the array by adding 100 to it 
  // Modify the third value in the array by multiply it by 3
 
  // Output the array
  console.log('The modified numbers are ', myLotteryNumbers);

```



---
title: JavaScript
level: 2
---

# Properties and methods
Arrays

* Since an `array` is a JavaScript Object, it comes with a number of `properties` and `methods` that we can use 
* For example, we can use the `push()` method to add items to the end of an array

```js
  // Declare an empty array 
  let myFavouriteColours = [];

  // Add a string variable to the array 
  myFavouriteColours.push("purple");

  // Check out the contents of the array - - we should see ("purple")
  console.log(myFavouriteColours);

  // Add another string variable to the array
  myFavouriteColours.push("green");

  // Output the array - we should see ("purple, "green")
  console.log(myFavouriteColours);

```



---
title: JavaScript
level: 2
---

# Properties and methods
Arrays

* We can also use the `.length` property to tell us how many items are in the array

```js
  // Declare an empty array 
  let myFavouriteColours = [];

  // Add two string variables to the array
  myFavouriteColours.push("purple");
  myFavouriteColours.push("green");

  // Output the array - the length should be 2
  console.log('The amount of items in the array are:', myFavouriteColours.length);

```


---
title: JavaScript
level: 2
---

# Properties and methods
Arrays

* To access the first array item we can always use [0] as long as we know at least one item is in the array 
* We can use the `.length` property to tell us how many items are in the array
* To access the last array item we would need to take the `.length` property and subtract 1

```js
  // Declare an array of colours
  let myFavouriteColours = ["purple", "blue", "hotpink", "green", "yellow"];

  // Access the first array item and modify it
  myFavouriteColours[0] = "azure";

  // Access the last array item and modify it
  myFavouriteColours[myFavouriteColours.length-1] = "beige";

  // Output the array - "azure", "blue", "hotpink", "green", "beige"
  console.log(myFavouriteColours);

```





---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Arrays

* I've provided you with an array of starships used in Star Wars, but I mistakenly got the first item wrong, and forgot one really important starship, so I am hoping you can fix my array
* Remove the first element `"Luke Skywalked"` as he is clearly not a starship
* Add in `"X-Wing"` at the very end of the array 
* Add in `"TIE Advanced x1"` at the start of the array
* **HINT**: look up the `array.unshift()` menthod

```js
  // Declare an array with your seven values
  let starWarsShips = ["Luke Skywalker", "Star Destroyer", "Millennium Falcon", "CR90 corvette"];
  
  // ADD YOUR CODE HERE
 
  // Output the array - 
  // ("TIE Advanced x1", "Star Destroyer", "Millennium Falcon", "CR90 corvette", "X-Wing");
  console.log(starWarsShips);

```



---
title: JavaScript
level: 2
---

# Const and arrays
Arrays

* We can set an `array` as a `const` variable and JavaScript will allow us to change the items inside the array but JavaScript won't let reassign the variable.

```js
  // Declare a const array
  const myFavouriteColours = ["purple", "green", "blue"];

  // Adding an item using the push() method works
  myFavouriteColours.push("gold");
  
  // Output the array - the length or the array will be 4
  console.log('The amount of items in the array are now ', myFavouriteColours.length);

  // Reassigning the array should throw an error in your console 
  myFavouriteColours = ["hotpink", "orange"]; // This won't work

```


---
title: JavaScript
level: 2
---

# There's also a reverse method 
Arrays

* We can use the `reverse` method to reverse the order of the items in the array

```html
<script>

  // Declare const array
  const myLotteryNumbers = [1, 22, 34, 56, 83, 59, 23];

  // Output the array
  console.log("Original: ", myLotteryNumbers);

  // Reverse method
  myLotteryNumbers.reverse();
  
  // Output the array
  console.log("After reverse: ", myLotteryNumbers);

</script>
```


---
title: JavaScript
level: 2
---

# Copying an array
Arrays

* When copying primitive data types JavaScript uses pass by value, so no issues
* However, when it comes to arrays, JavaScript uses pass by reference, and that can create some issues

```js
  // Declare array
  let originalLotteryNumbers = [1, 22, 34, 56, 83, 59, 23];

  // Copy the orginal array into a new array
  let copyLotteryNumbers = originalLotteryNumbers;

  // Now we modify the copy
  copyLotteryNumbers[0] = 5;
  copyLotteryNumbers[1] = 12;

  // Output the original array
  console.log("Original: ", originalLotteryNumbers);
  
  // Output the copy array
  console.log("Copy: ", copyLotteryNumbers);

```


---
title: JavaScript
level: 2
---

# Copying an array
Arrays

* The easiest way to make an actual copy of an array is to use the spread `...` operator
* We won't go into what the spread operator does now, that will be for a later class, but for now know that the following works

```js
  // Declare array
  let originalLotteryNumbers = [1, 22, 34, 56, 83, 59, 23];

  // Shallow copy of the orginal array into a new array
  let realCopyLotteryNumbers = [...originalLotteryNumbers];

  // Now we modify the copy
  realCopyLotteryNumbers[0] = 5;
  realCopyLotteryNumbers[1] = 12;

  // Output the original array
  console.log("Original: ", originalLotteryNumbers);
  
  // Output the copy array
  console.log("Copy: ", copyLotteryNumbers);

```



---
title: JavaScript
level: 2
---

# Copying an array
Arrays

* What if we just want to copy a portion of an array. There's a method for that too!
* The `slice()` method takes in the starting point and optional end point of the copy
* So `array.slice(2)` will copy every element from index 2 to the end
* So `array.slice(2,4)` will copy every element from index 2 to index 4

```js
  // Declare array
  let originalLotteryNumbers = [1, 22, 34, 56, 83, 59, 23];

  // Shallow copy of the orginal array into a new array
  let portionOfLotteryNumbers = originalLotteryNumbers.slice(4);

  // Shallow copy of the orginal array into a new array
  let portionOfLotteryNumbers = originalLotteryNumbers.slice(-3);

  // Output the original array - ( 59, 23 )
  console.log(portionOfLotteryNumbers);
  
  // Output the copy array - ( 83, 59, 23 )
  console.log(portionOfLotteryNumbers);

```



---
title: JavaScript
level: 2
---

# Array methods
Arrays

* There are actually a tonne more really helpful `array` methods that JavaScript has which makes working with arrays a breeze. 
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array