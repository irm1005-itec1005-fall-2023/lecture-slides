---
title: JavaScript variables
layout: intro
---

# JavaScript Variables
Learning about primitives, object literals, and variables

---
title: JavaScript
level: 2
---

# Working with variables
Variables

There are three ways to declare a variable `var`, `let`, and `const`.

```js
/* NEVER USE VAR */ 
var myFirstVariable = "Hello";

/* Then we have let */ 
let mySecondVariable = "World";

/* And finally we have const - for variables that need to be constant */ 
const myConstVariable = true;

```


---
title: JavaScript
level: 2
---

# So many Variables 
Variables

* String 
* Number 
* BigInt
* Boolean
* Null 
* Undefined
* Object 
* Symbol



---
title: JavaScript
level: 2
---

# String
Variables

String type is used to store textual data, or a sequence of characters.

```js
  // This is a string 
  // Note the quotation marks around the value
  let messageOne = "Hello World";

  // Single quotes also work as well
  let messageTwo = 'Hello World';

```



---
title: JavaScript
level: 2
---

# Number
JavaScript variables

As the name imples, you can store numeric values in a number. 

```js
// this is a number
let numberOfElephants = 33;

// The console will display 33
console.log(numberOfElephants);

```

---
title: JavaScript
level: 2
---

# Number
JavaScript variables

This is the largest numerical value that can be stored safely in  a `number` 9007199254740991.

If you think your app will need to store a bigger number, than you should use a `BigInt`.

```js
// this is a number
let numberOfElephants = 9007199254740991;

// The console will display 9007199254740991
console.log(numberOfElephants);

// This value comes from the number object 
Number.MAX_SAFE_INTEGER; // 9007199254740991

```


---
title: JavaScript
level: 2
---

# BigInt
Variables

This is the largest numerical value that can be stored in  a `number` 9007199254740991. 

If you think your app will need to store a bigger number, than you should use a `BigInt`.

```js
  // this is how we use a BigInt
  let numberOfElephants = BigInt(9007199254740992);

```



---
title: JavaScript
level: 2
---

# Boolean
Variables

Booleans can be set to `true` or `false`.

While you can name your variables almost anything you want (there are some rules that JS applies), when it comes to `Boolean` values, you should try to name your variables with an `is` prefix. 

For examples, `isEnabled`, `isPaidFor`, `isUserLoggedIn`. Also, avoid negative names, such as `isNotActive` or `isNotDone` as this can cause major confusion when reading code. 

```js
  // this is a boolean
  let isElephantPresent = false;

  // The console will display false
  console.log(isElephantPresent);
```



---
title: JavaScript
level: 2
---

# Null
Variables

This is an assigned value that means nothing, nada. 

We generally use this value to setup a variable and flag that nothing is set in the variable yet. 

```js
  // this is a null value
  let numElephants = null;

  // The console will display null
  console.log(numElephants);
```



---
title: JavaScript
level: 2
---

# Undefined
Variables

The value `undefined` is set on a variable before an actual value is provided to the variable.

```js
  // Whoops - declared a variable but didn't set it to anything
  let numElephants;

  // The console will display undefined
  console.log(numElephants); 
```



---
title: JavaScript
level: 2
---

# Objects literals
Variables

Objects literals in JavaScript are a collection of name and value pairs. 

The following is a really simple example of an object literal, though they can get very complex. 

```js
  // Declare an object literal
  const elephant = {
    name: "Jimbo",
    age: 200,
    isMarried: false,
  };

  // Access the whole object literal 
  console.log(elephant)

  // Access a property using the dot notation and something called chaining 
  console.log(elephant.name)

  // Access a property using the dot notation and something called chaining 
  console.log(elephant.age)

```


---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Variables

* Open your JavaScript file
* Type this code in and check out the browser's console message

```js
  // Declare an wage variable 
  let wage = 33; 

  // Declare another value 
  let bonus = 22;

  // Manipulate the wage by adding the bonus to it 
  wage = wage + bonus; 

  // Console log the contents of the variable 
  console.log("The updated wage is set to", wage);

```


---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Variables

* Open your JavaScript file
* Type this code in and check out the browser's console message
* Figure out how to add a space in your console log to seperate the two messages

```js
  // Declare the start of message
  let beginMessage = "Hello how are"; 

  // Declare the end of the message
  let endMessage = "you doing?";

  // Add both of the strings and display using the console log
  console.log(beginMessage + endMessage);

  // Add a space to seperate the two messages?

```


---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Variables

* Open your JavaScript file
* Type this code in 
* Define a `const` called `boilingPoint` and set it to `100`
* Run this code in your browser and check out the browser's console message

```js
  // Declare a const and set it to 100

  // Try to assign the const a new value
  boilingPoint = 105;
 
  // Add both of the strings and display using the console log
  console.log("The boiling point is:" , boilingPoint);

```


---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Variables

* Okay this one is sneaky
* Open your JavaScript file
* Define a constant variable called `quote` and put a `string` in the variable 
* Set the value of the string to be `You had me at "Hello"` (note the included double quotation marks)
* Console log the `quote` variable

```js
  // Declare a const and set it to - You had me at "Hello"
  const quote = ; // ADD CODE HERE
 
  // Add then display using the console log
  console.log(quote);

```



---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Variables
 
* Create an object literal named `product` and add the following properties 
  * `price` set to `4.99`
  * `name` set to `Nacho Cheese Doritos`
  * `isInStock` set to `true`
* Console log the `product` variable

```js

  // Declare a const called product
  // Set the following properties 
  //   price to 4.99 (Number)
  //   name to Nacho Cheese Doritos (String)
  //   isInStock to true (Boolean)
  const product = {}; 
 
  // Add then display using the console log
  console.log(product);

```


---
title: JavaScript
level: 2

---

# Template literals 
Variables

Template literals (also known as template strings) are enclosed by backticks [ ` ] and not quotation marks.

Inside template literals you are able to execute expressions by using the `${...}` notation.

```js
  // Declare a const called price and set it
  const price = 4.99; 

  // Declare a const called quantity and set it
  const quantity = 7 
 
  // Console log will display - You can buy 7 elephants for $34.93
  console.log(`You can buy ${quantity} elephants for $${price * quantity}`);

  // Note the two dollar signs - the first is just the regular dollar sign
  //  and the second one activates the expression within the curly braces

```



---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Variables

* Let's practice using a template literal 
* I've created three variables that you will need to reference
* Using template literals and the console log, display the following by referencing the three variables 
* `My phone number is (613) 825-6849`

```js
  // Declare some attributes 
  let areaCode = 613;
  let telephonePrefix = 825;
  let lineNumber = 6849;
 
  // Use a string template literal 
  // to display: "My phone number is (613) 825-6849"
  console.log(`ADD_YOUR_CODE_HERE`);

```

