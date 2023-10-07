---
layout: intro
title: CSS essentials
level: 1
---

# CSS Essentials

Starting out with CSS


---
title: What is CSS
level: 2
layout: image-right
image: /images/slides/css/essentials/css-logo.jpg
---


# What is CSS?
Adding style to substance

Cascading Style Sheets (CSS) is the code that styles web content. 

It is a stylesheet language used to describe the presentation of a document written in HTML. CSS describes how elements should be rendered on screen, on paper, in speech, or on other media.

<!-- 

Slide notes: 

Photo by RealToughCandy.com: https://www.pexels.com/photo/man-love-people-woman-11035386/

-->



---
title: CSS syntax
level: 2
---

# Basic syntax
Adding style to substance

CSS works by selecting an HTML element (like a paragraph `<p>`) and then altering properties of the element (like the colour) and applying a specific value to that property (like red). 

```css
p {
    color: red;
}

```

**Notes:**

* `p` - selector
* `color` - property
* `red` - value
* `color: red` - declaration 


<!-- 

Slide notes: 

-->


---
title: CSS syntax
level: 2
---

# Basic syntax
Adding style to substance

* **Selector:** This is the HTML element name at the start of the ruleset. It defines the element(s) to be styled (in this example, `<p>` elements). To style a different element, change the selector
* **Properties:** These are ways in which you can style an HTML element. (In this example, color is a property of the `<p>` elements.) In CSS, you choose which properties you want to affect in the rule.
* **Property value:** To the right of the property—after the colon—there is the property value. This chooses one out of many possible appearances for a given property. (For example, there are many color values in addition to red.)
* **Declaration:** This is a single rule like color: red;. It specifies which of the element's properties you want to style.

<!-- 

Slide notes: 

-->



---
title: CSS syntax
level: 2
---

# CSS ruleset
Adding style to substance

* Apart from the selector, each ruleset must be wrapped in curly braces. (`{}`)
* Within each declaration, you must use a colon (`:`) to separate the property from its value or values.
* Within each ruleset, you must use a semicolon (`;`) to separate each declaration from the next one.


<!-- 

Slide notes: 

-->



---
title: CSS syntax
level: 2
---

# Adding CSS to HTML
Adding style to substance

## External CSS 

External CSS contained in one or many CSS files is the most common method used to add CSS to a HTML content. To do this we create seperate CSS files and then link to them from inside an HTML file in the `<head>` tag with a self closing `<link>` elemnent. 

```html 
<!-- index.html -->
<head>
  <link rel="stylesheet" href="style.css" />
</head>
```

```css
/* style.css */
body {
  background-color: #eeeeee;
}

```


<!-- 

Slide notes: 

-->




---
title: CSS syntax
level: 2
---

# Adding CSS to HTML
Adding style to substance

## Internal CSS 

Internal CSS (or embedded CSS) involves adding CSS directly to the HTML page within the `<head>` element inside a `<style>` tag. This way of including CSS is much less popular because you can't reuse your CSS across multiple HTML pages.

```html 
<!-- index.html -->
<head>
  ...
  <style>
    /* styles */
    body {
      background-color: #eeeeee;
    }
  </style>
  ...
</head>
```


<!-- 

Slide notes: 

-->



---
title: CSS syntax
level: 2
---

# Adding CSS to HTML
Adding style to substance

## Inline CSS 

Inline CSS makes it possible to add styles directly to HTML elements, though this method isn’t as recommended or widely used. One key difference in syntax here is that you don't use a selector, since the styles are directly applied to the element.

```html 
<!-- index.html -->
<body>
  <main>
    <h1 style="color: red;background-color: black;">...</h1>
  </main>
</body>
```


<!-- 

Slide notes: 

-->




---
title: CSS basics
level: 2
---

# Cascade of CSS
Adding style to substance




<!-- 

Slide notes: 

-->



---
title: CSS basics
level: 2
---

# Specificity
Adding style to substance




<!-- 

Slide notes: 

-->



---
title: CSS basics
level: 2
---

# Inheritence
Adding style to substance




<!-- 

Slide notes: 

-->




---
title: CSS basics
level: 2
---

# Color
Adding style to substance




<!-- 

Slide notes: 

-->



---
title: CSS basics
level: 2
---

# CSS Units
Adding style to substance




<!-- 

Slide notes: 

-->





---
title: CSS Resources
level: 2
layout: image-right
image: /images/slides/css/essentials/css-books.jpg
---


# CSS resources
Guides and cheatsheets

* [CSS values and units - MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)
* [CSS - Odin project](https://www.theodinproject.com/lessons/foundations-css-foundations)
* [CSS - Code academy](https://www.codecademy.com/resources/docs/css)
* [Introduction to CSS - Prof3ssorSt3v3](https://www.youtube.com/watch?v=KFKScNHa-8M&list=PLyuRouwmQCjl4wTSNbb8RTKZuyMhoIxBe)
* [CSS Basics - MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics)
* [CSS Tricks](https://css-tricks.com)
* [CSS - Learn the web](https://learntheweb.courses/topics/using-css/#start)

<!-- 

Slide notes: 

Credit: 

Photo by KOBU Agency: https://unsplash.com/photos/ipARHaxETRk?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText

-->
