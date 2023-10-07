---
layout: intro
title: CSS flexbox 
level: 1
---

# CSS Flexbox

💪 flex your skills and build layouts like a boss


---
title: So what is Flexbox
level: 2
layout: image-right
image: /images/slides/css/flex-box/boxes.jpg
---


# Flexbox basics
Introduction to CSS Flexbox

## What is it? 

Flexbox allows you to control the flow of the elements in a container by placing items in rows and columns.


## Why "Flex"?

Flexbox allows us to distribute space dynamically across elements of an unknown size, hence the term "flex"



<!-- 

Slide notes: 

Credit: 

Photo by Ayrat: https://www.pexels.com/photo/photograph-of-brown-cardboard-boxes-12354555/

-->


---
title: Flexbox
level: 2
layout: center
---

<p>Flex box container</p>
<div class="border-dotted border-4 border-gray w-3xl">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

    display: flex;
}

ul.flex-demo li {
    margin: 0px;
    padding: 30px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Start with a flex container

We’re making a flex container and all the children of that container become flex items.

```html

<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

```


```css

ul {
    display: flex;
}

```


<!-- 

Slide notes: 


-->



---
title: Flexbox
level: 2
---

# Flex direction

```css

ul {
    display: flex;
    flex-direction: row;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

    display: flex;
}

ul.flex-demo li {
    margin: 0px;
    padding: 30px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->



---
title: Flexbox
level: 2
---

# Flex direction

```css

ul {
    display: flex;
    flex-direction: row-reverse;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

    display: flex;
    flex-direction: row-reverse;
}

ul.flex-demo li {
    margin: 0px;
    padding: 30px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->



---
title: Flexbox
level: 2
---

# Flex direction

```css

ul {
    display: flex;
    flex-direction: column;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

    display: flex;
    flex-direction: column;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Justify content
We can distribute the elements along the axis that the flex items are arranged using the `justify-content` property.

```css

ul {
    display: flex;
    flex-direction: row;
    justify-content: center;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

   display: flex;
    flex-direction: row;
    justify-content: center;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Justify content
We can distribute the elements along the axis that the flex items are arranged using the `justify-content` property.

```css

ul {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

   display: flex;
    flex-direction: row;
    justify-content: flex-end;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Justify content
We can distribute the elements along the axis that the flex items are arranged using the `justify-content` property.

```css

ul {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

   display: flex;
    flex-direction: row;
    justify-content: flex-start;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->



---
title: Flexbox
level: 2
---

# Justify content
We can distribute the elements along the axis that the flex items are arranged using the `justify-content` property.

```css

ul {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

   display: flex;
    flex-direction: row;
    justify-content: space-around;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Justify content
We can distribute the elements along the axis that the flex items are arranged using the `justify-content` property.

```css

ul {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

   display: flex;
    flex-direction: row;
    justify-content: space-between;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Flex wrap

```css

ul {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
}

```

<div class="border-dotted border-4 border-gray w-lg">
<ul class="flex-demo w-xl">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

   display: flex;
    flex-direction: row;
    justify-content: flex-start;
}

ul.flex-demo li {
    width: 200px;
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Flex wrap

```css

ul {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
}

```

<div class="border-dotted border-4 border-gray w-lg">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

   display: flex;
    flex-direction: row;
    justify-content: flex-start;
    flex-wrap: wrap;
}

ul.flex-demo li {
    width: 200px;
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->





---
title: Flexbox
level: 2
---

# Aligning items
We can distribute the elements along the cross axis that the flex items are arranged using the `align-items` property.

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: center;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;
    height: 150px;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->



---
title: Flexbox
level: 2
---

# Aligning items
We can distribute the elements along the cross axis that the flex items are arranged using the `align-items` property.

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;
    height: 150px;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-end;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->




---
title: Flexbox
level: 2
---

# Aligning items
We can distribute the elements along the cross axis that the flex items are arranged using the `align-items` property.

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;
    height: 150px;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Aligning items
We can distribute the elements along the cross axis that the flex items are arranged using the `align-items` property.

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: stretch;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;
    height: 150px;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: stretch;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->



---
title: Flexbox
level: 2
---

# Aligning items
We can distribute the elements along the cross axis that the flex items are arranged using the `align-items` property.

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
}

ul li:nth-child(3) { 
    align-self: stretch; 
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;
    height: 100px;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(3) { align-self: stretch; }

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->




---
title: Flexbox
level: 2
---

# Flex grow
We can use the `flex-grow` property to have flex items take up more space

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
}

ul li:nth-child(1) { 
    flex-grow: 1;
}



```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { 
    flex-grow: 1;
}


ul.flex-demo li:nth-child(1) { background-color: #f72585; }

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox
level: 2
---

# Flex grow
We can use the `flex-grow` property to have flex items take up more space

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
}

ul li:nth-child(1) { 
    flex-grow: 2;
}

ul li:nth-child(2) { 
    flex-grow: 1;
}


```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
}

ul.flex-demo li:nth-child(1) { 
    flex-grow: 2;
}

ul.flex-demo li:nth-child(2) { 
    flex-grow: 1;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->




---
title: Flexbox
level: 2
---

# Flex basis
We can use the `flex-basis` to request the flex item be a certain width (or height in column mode)

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
}

ul li { 
    flex-basis: 250px;
}

```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
    flex-basis: 250px;
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->



---
title: Flexbox
level: 2
---

# Gap
We can use the `gap` property to add a gap between the flex items in the direction of the main axis.

```css

ul {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    gap: 60px;
}
```

<div class="border-dotted border-4 border-gray w-full">
<ul class="flex-demo">
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>
</div>

<style>
ul.flex-demo {
    padding: 0px !important;
    margin: 10px !important;
    list-style: none;
    background-color: white;

    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
    gap: 60px;
}

ul.flex-demo li {
    margin: 0px;
    padding: 10px;
   
}

ul.flex-demo li:nth-child(1) { background-color: #f72585; }

ul.flex-demo li:nth-child(1) { background-color: #f72585; }
ul.flex-demo li:nth-child(2) { background-color: #b5179e; }
ul.flex-demo li:nth-child(3) { background-color: #7209b7; }


</style>


<!-- 

Slide notes: 


-->


---
title: Flexbox Resournces
level: 2
layout: image-right
image: /images/slides/css/flex-box/fallen-boxes.jpg
---


# Flexbox resources
Guides and cheatsheets

* [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* [Flexbox cheat sheet](https://yoksel.github.io/flex-cheatsheet/)
* [Flexbox Froggy](https://flexboxfroggy.com)
* [Another Flexbox cheat sheet](https://www.sketchingwithcss.com/samplechapter/cheatsheet.html)
* [Article on sizing flexbox items](https://www.smashingmagazine.com/2018/09/flexbox-sizing-flexible-box/)

<!-- 

Slide notes: 

Credit: 

Photo by cottonbro studio: https://www.pexels.com/photo/person-in-black-leather-boots-sitting-on-brown-cardboard-boxes-4553277/

-->
