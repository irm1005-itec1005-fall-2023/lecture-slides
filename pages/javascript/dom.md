---
title: JavaScript dom
layout: intro
---

# JavaScript DOM
The Document Object Model


---
title: JavaScript dom
level: 2
---

# Introduction 
JavaScript dom 

The Document Object Model (DOM) is a representation of the objects that make up the structure and content of a web page.

For example, the paragraph below on our HTML page would have a corresponding JavaScript Object that we can access, modify, or remove.

The `document` object gives us a programatic way to access all of the properties, methods, elements, and events on our web page.

```html
<!-- Paragraph on our page in HTML -->
<p>This is a paragraph</p>

```

---
title: JavaScript dom
level: 2
---

# Introduction 
JavaScript dom 

For example, here is how we could access the paragraph in JavaScript

```html
<!-- Paragraph on our page in HTML -->
<p>This is a paragraph</p>

```

```js
/* Select all of the paragraphs on the page */
const paragraphs = document.querySelectorAll("p");

// The first paragraph
console.log(paragraphs[0]);

```


---
title: JavaScript dom
level: 2
---

# Introduction 
JavaScript dom 

The main dom methods we're looking at (con't):

```js
/* Get an element by an id */
const myH1 = document.getElementByID("h1ID");

/* Get elements by a class name */ 
const collectionOfElements = document.getElementById("classname");

/* Get an element using a CSS selector (you can use an css selector pattern in here) */ 
const oneElement = document.querySelector(".container");

/* Select a collections of elements that match the query pattern */
const paragraphs = document.querySelectorAll("p");

/* Select a collections of elements that match the query pattern */
const newParagraph = document.createElement("p");

```


---
title: JavaScript dom
level: 2
---

# Introduction 
JavaScript dom 

The main dom methods we're looking at:

```js
/* Add child node to parent */ 
const mainSection = document.getElementById("main");
mainSection.appendChild(newParagraph);

/* Modify a style property */ 
newParagraph.style.transform = "rotate(10deg)";

/* Set text content */ 
const myLink = document.getElementById("a");
myLink.textContent = "This is a link!";

/* Set attribute */ 
const myLink = document.getElementById("a");
myLink.setAttribute("href", "#");


```


---
title: JavaScript dom
level: 2
---

# Introduction 
JavaScript dom 

The main dom methods we're looking at:

```js
/* Add child node to parent but as the first thing in the parent */ 
const mainSection = document.getElementById("main");
mainSection.prepend(newParagraph);
```