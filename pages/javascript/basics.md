---
title: JavaScript basics
layout: intro
---

# JavaScript
The programming language everyone loves and absolutely hates


---
title: JavaScript
level: 2
---

# How to run JavaScript code
Basics

Running code in the `head` tag. Meh. 

```html
<html>
  <head>
    ...
    <script>
      /* 
        This is a multiline 
        JavaScript comment 
      */

      // And this is a single line comment
      console.log("Hello World");
    
    </script>
  </head>
  ...
</html>
```



---
title: JavaScript
level: 2
---

# How to run JavaScript code
Basics

Running code in the `body` tag. Better. 

```html
<html>
  ...
  <body>
    ...
    <script>
      /* 
        This is a multiline 
        JavaScript comment 
      */

      // And this is a single line comment
      console.log("Hello World");
    
    </script>
  </body>
</html>
```




---
title: JavaScript
level: 2
---

# How to run JavaScript code
Basics

Running code in the `body` from a seperate `js` file. Best. 

```html
<html>
  ...
  <body>
    ...
    <script src="javascript.js"></script>
  </body>
</html>
```




---
title: JavaScript
level: 2
---

# Statements
Basics

A statement is an instruction written in javascript code that the browser interprets and then does a thing. 

**Always put in semi-colons at the end of a line of code**. 

JavaScript is loosely typed and may work without them but you will get unexpected behaviour. 

```js
  let age = 300;
```


---
title: JavaScript
level: 2
---

# Code blocks
Basics

Code blocks are sections of code bound by a `{` and a `}`

**Never put a semi-colon at the end of a code block, they don't need them**. 

```js
let age = 300;

if (age > 50) {
  console.log("Damn that's old");
}

/* Note: there isn't a semi-colon at the end of line 6 */

```

---
title: JavaScript
level: 2
---

# Naming conventions
Basics

The hardest thing to do in development, apart from everything, is to name your variables. 

There are three different naming conventions `pascal case`, `camel case`, and `snake case`. 

(Note: there is a fourth - `kebab-case` but that doesn't work in JavaScript)

```js
// Camel case 
let numTodoItems = 41;

// Pascal case 
let NumTodoItems = 44;

// Snake case 
let num_todo_items = 32; 


```



---
title: JavaScript
level: 2
---

# The most important line of code in JavaScript:
Basics

The `console` object provides access to the browser's debugging console. 

You can use the `console` object anywhere in your JavaScript code. 

The easiest way to print something to the browsers console is to use the `console.log()` function shown below. Later on we'll look at some other `console` functions available to us. 

```js
// This is the border: 1px solid red; of JavaScript 
console.log(numTodoItems);

```

---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Basics

* Create an HTML page
* Add a script element to the bottom of the page
* Add the following code to your page 
* Open up the inspector tools in your browser 
* View the console output

```js
  // Declare a variable
  let message = "Hello World";

  // Console log the contents of the variable 
  console.log(message);

```


---
title: JavaScript
level: 2
---

# Other useful `console` functions
Basics

```js
// Clear the console 
console.clear();

// General logging output
console.log("Hello world");

// Logging information
console.info("Some useful information");

// Outputs a warning message
console.warn("Uh oh, this is a warning"); 

// Outputs an error message
console.error("Magor error occured");

// Outputs tabular data. The argument may be an array or object
console.table(["Elephant", "Lion", "Tiger"]);

// Outputs the stack trace, or the function path that was executed
console.trace();
```