---
layout: intro
title: CSS selectors
level: 1
---

# CSS Selectors

Target HTML elements using CSS selectors


---
title: What are CSS selectors
level: 2
layout: image-right
image: /images/slides/css/selectors/library.jpg
---


# Targeting our HTML
Adding style to substance

We use CSS selectors to find specific elements on our HTML page so that we can apply CSS rules to that element. 

The latest version of CSS brings us a multitude of CSS selectors that allow us to be very specific when selecting HTML elements. 

The following slides go through all of the different types of selectors available.

<!-- 

Slide notes: 

Photo by DS stories: https://www.pexels.com/photo/pile-of-colorful-boxes-7679762/

-->




---
title: CSS Selectors
level: 2
---

# What is a selector
Adding style to substance

CSS selectors are the first part of our CSS Rules. They are a pattern of elements and other terms that tell the browser which HTML elements should be selected to have the CSS property values inside the rule applied to them. The element or elements which are selected by the selector are referred to as the subject of the selector.

In the example below, `body` and `p` are our selectors.

```css
body {
  background-color: red;
}

p {
  color: #eeeeee;
}
```

<!-- 

Slide notes: 

-->


---
title: CSS Selectors
level: 2
---

# Selector lists
Adding style to substance

If you have more than one element which uses the same CSS declarations, you are able to list out your selectors, seperated by a `,` and the CSS properties will be applied to all of the HTML elements targetted by the selectors in the list. 

```css
h1 {
  color: #333333;
}

h2 {
  color: #333333;
}

/* Can be combined and written as */

h1 , h2 {
    color: #333333;
}

```


<!-- 

Slide notes: 

-->



---
title: CSS Selectors
level: 2
---

# Universal selector
Adding style to substance

All markup and every element on the page can be selected using the `*` selector. 

In the example below, every element on a web page will get a 1px solid red border applied to them. 

```css
* {
  border: 1px solid red;
}
```

<!-- 

Slide notes: 

-->



---
title: CSS Selectors
level: 2
---

# Type selector
Adding style to substance

A type selector (or element selector) selects all HTML elements of the given element type, and the syntax is just the name of the element.

```css
h1 {
  color: #333333;
}

ul {
  color: #eeeeee;
  background-color: #333333;
}

p {
 color: #333333;
}
```

<!-- 

Slide notes: 

-->



---
title: CSS Selectors
level: 2
---

# Class selector
Adding style to substance

We can be more specific about what element we select by assigning a name to the HTML tag — called a class. Classes are just an attribute on your HTML tags. 

You can use a class selector by adding a `.` infront of a class name in your CSS code.

```html 
<!-- index.html -->
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li class="selected">Item 3</li>
  <li>Item 4</li>
</ul>
```

```css
/* style.css */
.selected {
  color: red;
}
```

<!-- 

Slide notes: 

-->



---
title: CSS Selectors
level: 2
---

# ID selector
Adding style to substance

ID selectors are similar to class selectors. They select an element with the given ID, which is another attribute you place on an HTML element:

You can use an id selector by adding a `#` infront of a id in your CSS code.

```html 
<!-- index.html -->
<ul>
  <li id="unique-item">Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>
```

```css
/* style.css */
#unique-item {
  color: red;
}
```

<!-- 

Slide notes: 

-->


---
title: CSS Selectors
level: 2
---

# Chaining selector
Adding style to substance

You can also target a specific HTML elements that have two or more specific classes applied to them. This is known as the chaining selector.

The chaining selector is used by not putting any spaces in between the class name.

```html 
<!-- index.html -->
<ul>
  <li class="active first">Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>
```

```css
/* style.css */
.active.first {
  color: red;
}
```

<!-- 

Slide notes: 

-->




---
title: CSS Selectors
level: 2
---

# Descendant combinator
Adding style to substance

Combinators are CSS selectors that are used to style elements that have a certain relationship with other selected elements. 

The descendant combinator selector allows us to match all descendants of a specific element. 

```html 
<!-- index.html -->
<section class="parent">
  <p>lorem ipsum dolar</p>
  <p class="child">lorem ipsum dolar</p> <!-- would be styled as has parent and child class -->
</section>
<section>
  <p class="child">lorem ipsum dolar</p> <!-- would not be selected since not a child of a parent class -->
</section>
```

```css
/* style.css */
.parent .child {
  color: red;
}
```

<!-- 

Slide notes: 

-->




---
title: CSS Selectors
level: 2
---

# Attribute selectors
Adding style to substance

This group of selectors gives you different ways to select elements based on the presence of a certain attribute on an element.


```html 
<!-- index.html -->
<p data-course="IMD1005">lorem ipsum dolar</p>
```

```css
/* style.css */
p[data-course] {
  font-size: 3rem;
  color: red;
}
```

<!-- 

Slide notes: 

-->


---
title: CSS Selectors
level: 2
---

# Psuedo-class 
Adding style to substance

This group of selectors style certain states of an element. The `:hover` pseudo-class for example selects an element only when it is being hovered over by the mouse pointer.

```html 
<!-- index.html -->
<a href="https://google.ca">Visit Google</a>
```

```css
/* style.css */
a:hover {
  background-color: #eeeeee;
  color: #333333;
}
```

<!-- 

Slide notes: 

-->




---
title: CSS Selectors
level: 2
---

# Psuedo-elements
Adding style to substance

Pseudo-elements refer to a certain part of an element rather than the element itself. For example, `::first-letter` always selects the first letter of text inside an element (a `<p>` in the below case).

In the example below, the psuedo-element selector would target just the letter `L` in the `<p>` and give it a background colour, font colour, and set the text size to `3rem`.


```html 
<!-- index.html -->
<p>Lorem ipsum dolar</p>
```

```css
/* style.css */
p::first-letter{
  background-color: #eeeeee;
  color: #333333;
  font-size: 2rem;
}
```


<!-- 

Slide notes: 

-->



---
title: CSS Selector Resources
level: 2
layout: image-right
image: /images/slides/css/selectors/books.jpg
---


# Selector resources
Guides and cheatsheets

* [Combining and Chaining CSS Selectors - Prof3ssorSt3v3](https://www.youtube.com/watch?v=6VGKD7p4p-w&list=PLyuRouwmQCjl4wTSNbb8RTKZuyMhoIxBe&index=4)
* [C in CSS Means Cascading - Prof3ssorSt3v3](https://www.youtube.com/watch?v=PigxOyVDIQg&list=PLyuRouwmQCjl4wTSNbb8RTKZuyMhoIxBe&index=2)
* [Nth Child - Prof3ssorSt3v3](https://www.youtube.com/watch?v=4NsJtaaC0qI&list=PLyuRouwmQCjl4wTSNbb8RTKZuyMhoIxBe&index=15)
* [Psuedo classes - Prof3ssorSt3v3](https://www.youtube.com/watch?v=0VDx1570X3U&list=PLyuRouwmQCjl4wTSNbb8RTKZuyMhoIxBe&index=14)
* [Selectors - MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)
* [Selectors - Odin project](https://www.theodinproject.com/lessons/foundations-css-foundations#selectors)
* [Selectors - web.dev](https://web.dev/learn/css/selectors/)
* [Selectors - Learn the web](https://learntheweb.courses/topics/using-css/#targeting-things-in-html)
* [Combinators - Code academy](https://www.codecademy.com/resources/docs/css/combinators)

<!-- 

Slide notes: 

Credit: 

Photo by Greg Rakozy: https://unsplash.com/photos/vw3Ahg4x1tY?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText

-->
