---
layout: intro
title: CSS grid 
level: 1
---

# CSS Grid

🏢 another way to layout your boxes


---
title: So what is Grid
level: 2
layout: image-right
image: /images/slides/css/grid/layout.jpg
---


# Grid basics
Introduction to CSS Grid

## What is it? 

CSS Grids are a two-dimensional grid-based layout framework that were created to specifically solve the layout challenges using both columns and rows.


## Why "Grid"?

Flexbox is one-directional in nature, while grid gives us a bit more options being able to layout elements on a two-dimensional plane.

<!-- 

Slide notes: 

Credit: 

Photo by Karolina Grabowska: https://www.pexels.com/photo/a-man-posting-a-schedule-reminder-5882583/

-->



---
title: How to use Grid
level: 2
---


# Grid overview
Introduction to CSS Grid

Grid layouts have the following characteristics

* Grids are defined with rows and columns. 
* You can define the size of the rows and columns.
* Similiar to flexbox, grids have a container, and direct children (or items) that are placed into the grid container.
* Children can be placed into the container automatically or you can specify a precise location.
* Lines and areas on the grid can be named to make placement easier.
* Grid items can be aligned within their area. 


<!-- 

Slide notes: 

-->

---
title: Grid lines
level: 2
---


# Grid lines
Introduction to CSS Grid

A grid is made up of lines, which run horizontally and vertically. If your grid has four columns, it will have five column lines including the one after the last column.

Line numbers start at one (1) and follow the writing mode (generally from from left to right).

<ul class="grid-demo">
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
  <li>Item D</li>
  <li>Item E</li>
  <li>Item F</li>
  <li>Item G</li>
  <li>Item H</li>
</ul>


<style>
ul.grid-demo {
    padding: 0px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    display: grid;
    grid-template-columns: repeat(4, 1fr);

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 1px solid #cce3de;

    background-color: #eaf4f4;
}

ul.grid-demo li:nth-child(2), 
ul.grid-demo li:nth-child(6) { border-left: 5px solid #6b9080;  }


/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>


<!-- 

Slide notes: 

-->



---
title: Grid tracks
level: 2
---


# Grid tracks
Introduction to CSS Grid

A track is the space between two grid lines. Row tracks run across the rows, and column tracks run between the columns.

<ul class="grid-demo">
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
  <li>Item D</li>
  <li>Item E</li>
  <li>Item F</li>
  <li>Item G</li>
  <li>Item H</li>
</ul>


<style>
ul.grid-demo {
    padding: 0px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    display: grid;
    grid-template-columns: repeat(4, 1fr);

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 1px solid #cce3de;

    background-color: #eaf4f4;
}

ul.grid-demo li:nth-child(1), 
ul.grid-demo li:nth-child(2), 
ul.grid-demo li:nth-child(3), 
ul.grid-demo li:nth-child(4) { background-color: #a4c3b2;  }


/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>


<!-- 

Slide notes: 

-->


---
title: Grid cell
level: 2
---


# Grid cell
Introduction to CSS Grid

A grid cell is the smallest space on a grid defined by the intersection of row and column tracks. It's just like a table cell or a cell in a spreadsheet. If you define a grid and don't place any of the items they will automatically be laid out one item into each defined grid cell.

<ul class="grid-demo">
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
  <li>Item D</li>
  <li>Item E</li>
  <li>Item F</li>
  <li>Item G</li>
  <li>Item H</li>
</ul>


<style>
ul.grid-demo {
    padding: 0px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    display: grid;
    grid-template-columns: repeat(4, 1fr);

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 1px solid #cce3de;

    background-color: #eaf4f4;
}

ul.grid-demo li:nth-child(2) { background-color: #a4c3b2;  }

/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>


<!-- 

Slide notes: 

-->



---
title: Grid area
level: 2
---


# Grid area
Introduction to CSS Grid

Several grid cells together. Grid areas are created by causing an item to span over multiple tracks.

<ul class="grid-demo">
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
  <li>Item D</li>
  <li>Item E</li>
  <li>Item F</li>
  <li>Item G</li>
  <li>Item H</li>
</ul>


<style>
ul.grid-demo {
    padding: 0px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    display: grid;
    grid-template-columns: repeat(4, 1fr);

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 1px solid #cce3de;

    background-color: #eaf4f4;
}

ul.grid-demo li:nth-child(2),
ul.grid-demo li:nth-child(3),
ul.grid-demo li:nth-child(6),
ul.grid-demo li:nth-child(7) { background-color: #a4c3b2;  }

/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>


<!-- 

Slide notes: 

-->




---
title: Grid area
level: 2
---


# Gap
Introduction to CSS Grid

A gutter or alley between tracks. For sizing purposes these act like a regular track. You can't place content into a gap but you can span grid items across it.

<ul class="grid-demo">
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
  <li>Item D</li>
  <li>Item E</li>
  <li>Item F</li>
  <li>Item G</li>
  <li>Item H</li>
</ul>


<style>
ul.grid-demo {
    padding: 0px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>


<!-- 

Slide notes: 

-->




---
title: Grid container
level: 2
---


# Grid container
Introduction to CSS Grid

The HTML element which has `display: grid` applied, and therefore creates a new grid formatting context for the direct children (the grid items).

Here we create a class called `.grid-container` which sets the `display` to `grid`.

```css
.grid-container {
  display: grid;
}
```

And we apply the class to an `ul` to make the children render in the `grid` container.

```html 
<ul class="grid-container">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>

```

<!-- 

Slide notes: 

-->


---
title: Grid container
level: 2
layout: center
---


Adding `display: grid` doesn't actually change very much on it's own. 

We need to specify columns.

<ul class="grid-demo">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>


<style>
ul.grid-demo {
    padding: 5px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    border: 5px solid #6b9080;

    display: grid;

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>

<!-- 

Slide notes: 

-->



---
title: Grid container
level: 2
---


# Setting the columns
Introduction to CSS Grid

We define rows and columns on our grid with the `grid-template-rows` and `grid-template-columns` properties.

```css
.grid-container {
  display: grid;
  grid-template-columns: 200px 200px 200px;
}
```

```html 
<ul class="grid-container">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>

```

<!-- 

Slide notes: 

-->


---
title: Grid container
level: 2
layout: center
---


Adding `grid-template-columns: 200px 200px 200px;` gives us three columns of `200px` each.

Additional items automatically wrap down to the next row and maintain their column width.

The remaining space in the container (if available) is left unused. 

<ul class="grid-demo">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>


<style>
ul.grid-demo {
    padding: 5px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    border: 5px solid #6b9080;

    display: grid;
    grid-template-columns: 200px 200px 200px;

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>

<!-- 

Slide notes: 

-->


---
title: Grid container
level: 2
---


# The fr unit
Introduction to CSS Grid

In the previous example we setup our grid to have three columns of `200px` each. 

Now we're introducing a new css unit called `fr`. These can only be used with grids and they stand for the term "fraction". The code below would create three equal columns in our grid.

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

```html 
<ul class="grid-container">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>

```

<!-- 

Slide notes: 

-->


---
title: Grid container
level: 2
layout: center
---


Adding `grid-template-columns: 1fr 1fr 1fr;` gives us three equal sized columns.

<ul class="grid-demo">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>


<style>
ul.grid-demo {
    padding: 5px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    border: 5px solid #6b9080;

    display: grid;
    grid-template-columns: 1fr 1fr 1fr;

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>

<!-- 

Slide notes: 

-->



---
title: Grid container
level: 2
---


# The fr unit
Introduction to CSS Grid

The `fr` units don't need to be even and can be of unequal sizes.

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}
```

```html 
<ul class="grid-container">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>

```

<!-- 

Slide notes: 

-->


---
title: Grid container
level: 2
layout: center
---


Adding `grid-template-columns: 1fr 2fr 1fr;` set the middle column to be twice the size as the first and last columns.

<ul class="grid-demo">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>


<style>
ul.grid-demo {
    padding: 5px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    border: 5px solid #6b9080;

    display: grid;
    grid-template-columns: 1fr 2fr 1fr;

}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>

<!-- 

Slide notes: 

-->




---
title: Grid container
level: 2
---


# The repeat notation 
Introduction to CSS Grid

If we had a lot of columns, it would get really annoying to keep writing `1fr` over and over. So we can use the `repeat()` notation to repeat the directives. 

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
}
```

Is equivalent to the following:

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
}
```

<!-- 

Slide notes: 

-->





---
title: Grid container
level: 2
---


# Placing items
Introduction to CSS Grid

Let's look at positioning items in the grid we created. We use the grid lines to set start and end points, and then the item will stretch to fill the available space in between the lines.

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: repeat(2, 50px 75px);
}

.item {
  grid-column-start: 2; /* start at column line 2 */
  grid-column-end: 4; /* end at column line 4 */
  grid-row-start: 2; /*start at row line 2 */
  grid-row-end: 5; /* end at row line 5 */
}
```

```html 
<ul class="grid-container">
  <li class="item">Item 1</li>
</ul>

```

<!-- 

Slide notes: 

-->


---
title: Grid container
level: 2
layout: center
---

What's happening here is that our Item 1 starts at the column line 2 and goes until column line 4.

And our item starts on the second row line and extents all the way down to the last line which is row line 5.

<ul class="grid-demo">
  <li class="item">Item 1</li>
</ul>


<style>
ul.grid-demo {
    padding: 5px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    border: 5px solid #6b9080;

    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: repeat(2, 50px 75px);
}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

ul.grid-demo li.item {
  grid-column-start: 2; /* start at column line 2 */
  grid-column-end: 4; /* end at column line 4 */
  grid-row-start: 2; /*start at row line 2 */
  grid-row-end: 5; /* end at row line 5 */
}

/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>

<!-- 

Slide notes: 

-->



---
title: Grid container
level: 2
layout: center
---

What's happening here is that our Item 1 starts at the column line 2 and goes until column line 4.

And our item starts on the second row line and extents all the way down to the last line which is row line 5.

<ul class="grid-demo">
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>


<style>
ul.grid-demo {
    padding: 5px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    border: 5px solid #6b9080;

    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: repeat(2, 50px 75px);
}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

ul.grid-demo li:nth-child(7), 
ul.grid-demo li:nth-child(8),
ul.grid-demo li:nth-child(12),
ul.grid-demo li:nth-child(13),
ul.grid-demo li:nth-child(17), 
ul.grid-demo li:nth-child(18) { background-color: #6b9080;  }


/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>

<!-- 

Slide notes: 

-->



---
title: Grid container
level: 2
---


# Grid template areas
Introduction to CSS Grid

If using row and column numbers are a bit annoying, grid allows us to specificy the shape of our grid using name template areas and use our own derived names for each area in our grid. 

The following code creates a four column by three row grid and then defines which areas go into each section.

```css
.grid-container {
  display: grid;
  grid-template-columns: 1.5em 2fr 1fr 1.5em;
  grid-template-areas:
    "header header  header header"    /* layout your grid using your own strings */
    ".      content side   ."         /* this still has to be a grid shape */
    "footer footer  footer footer"    /* the footer spans all four columns */
}

.header { grid-area: header; }
.content { grid-area: content; }
.side { grid-area: side; }
.footer { grid-area: footer; }

```


<!-- 

Slide notes: 

-->


---
title: Grid container
level: 2
---


# Grid template areas
Introduction to CSS Grid

And this is the `HTML` that would implement that grid css

```html 
<div class="grid-container">
  <header class="header">...</header>
  <main>
    <div class="content">...</div>
    <div class="side">...</div>
  </main>
  <footer class="footer">...</footer>
</div>

```

<!-- 

Slide notes: 

-->



---
title: Grid container
level: 2
layout: center
---

And here is our Grid Layout implemented using named templates.

The header and footer span the whole row, and the content and side areas have two small columns on either side for padding.

<ul class="grid-demo">
  <li class="header">Header</li>
  <li class="content">Content</li>
  <li class="side">Side</li>
  <li class="footer">Footer</li>
</ul>


<style>
ul.grid-demo {
    padding: 5px !important;
    margin: 0px !important;
    list-style: none;
    background-color: white;

    border: 5px solid #6b9080;

    display: grid;
    grid-template-columns: 1.5em 2fr 1fr 1.5em;
    grid-template-areas:
    "header header  header header"    /* layout your grid using your own strings */
    ".      content side ."         /* this still has to be a grid shape */
    "footer footer  footer footer"    /* the footer spans all four columns */
}

ul.grid-demo li {
    margin: 0px;
    padding: 25px;

    border: 5px solid #a4c3b2;

    background-color: #eaf4f4;
}

.header { grid-area: header; }
.content { grid-area: content; }
.side { grid-area: side; }
.footer { grid-area: footer; }



/* 
  https://coolors.co/palette/6b9080-a4c3b2-cce3de-eaf4f4-f6fff8
*/

</style>

<!-- 

Slide notes: 

-->


---
title: Grid Resournces
level: 2
layout: image-right
image: /images/slides/css/flex-box/fallen-boxes.jpg
---


# Grid resources
Guides and cheatsheets

These slides have barely scratched the surface of Grid. Please consider reviewing the following resources for additional information on CSS Grid.

* [Grid Garden game](https://cssgridgarden.com)
* [Basic concepts of grid layout - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
* [Named template areas - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Grid_Template_Areas)
* [CSS Grid - web.dev](https://web.dev/learn/css/grid/)
* [CSS Grid - CSS-tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)
* [CSS Grid cheatsheet - yoksel](https://yoksel.github.io/grid-cheatsheet/)

<!-- 

Slide notes: 

Credit: 

Photo by cottonbro studio: https://www.pexels.com/photo/person-in-black-leather-boots-sitting-on-brown-cardboard-boxes-4553277/

-->