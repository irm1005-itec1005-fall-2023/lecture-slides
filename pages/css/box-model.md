---
layout: intro
title: CSS box model
level: 1
---

# CSS Box Model

Everything is a box in CSS


---
title: What is the CSS box model
level: 2
layout: image-right
image: /images/slides/css/box-model/stack.jpg
---


# Box model
So many boxes

Every single HTML element rendered on the screen is a rectangular box. These boxes can be nested (have other boxes inside them) or they can sit on their own. 

Understanding these boxes is key to being able to create more complex layouts with CSS.

The following slides go through the box model and how to size a box using `margin`, `padding` and `border`.

<!-- 

Slide notes: 

Photo by BERK OZDEMIR: https://www.pexels.com/photo/people-reading-books-in-library-3779187/

-->




---
title: CSS box model
level: 2
---

# Block and inline boxes
Everything is a box

There are two categories of boxes in CSS, **block** boxes and **inline** boxes.

The difference between the two are that block boxes will break onto a new line and will take up all available width to fill up the space available in its container. Whereas inline elements won't break onto a new line or take up more width than they need.

You can set the type of box using the `display` CSS property, though by default most HTML elements are block. Some HTML elements, such as `<a>`, `<span>`, `<em>` and `<strong>` use inline as their display type by default.

<!-- 

Slide notes: 

-->


---
title: CSS box model
level: 2
---

# Block and inline boxes
Everything is a box

Here is an example of block and inline elements. 

<div class="border border-gray-300 p-2">
    <div class="mb-10 pl-2 border border-5 border-red-200">
        <p>This is a block box <span class="text-xs text-gray-500">(like a <code>p</code> tag)</span></p>
    </div>
    <div class="mb-10">
        <p class="p-2 inline border border-5 border-blue-200">Inline <span class="text-xs text-gray-500">(like a <code>span</code> tag)</span></p>
        <p class="ml-2 p-2 inline border border-5 border-blue-200">Inline</p>
        <p class="ml-2 p-2 inline border border-5 border-blue-200">Inline</p>
        <p class="ml-2 p-2 inline border border-5 border-blue-200">Inline</p>
    </div>
    <div class="mb-2 pl-2 border border-5 border-red-200">
        <p>And we're back to block box <span class="text-xs text-gray-500">(like a <code>p</code> tag)</span></p>
    </div>
</div>


<!-- 

Slide notes: 

-->


---
title: CSS box model
level: 2
---

# Parts of a box
Everything is a box

* **Content:**  The area where your content is displayed; size it using properties like `width` and `height`.
* **Padding:** The padding sits around the content as white space; size it using `padding` and related properties.
* **Border:** The border box wraps the content and any padding; size it using `border` and related properties.
* **Margin:** The margin is the outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements; size it using `margin` and related properties.


<!-- 

Slide notes: 

-->


---
layout: center
title: CSS box model
level: 2
---

<img src="/images/slides/css/box-model/model.png" alt="" />

<!-- 

Slide notes: 

-->


---
title: Margin
level: 2
---

# Margin
Everything is a box


<!-- 

Slide notes: 

-->



---
title: Padding
level: 2
---

# Padding
Everything is a box


<!-- 

Slide notes: 

-->



---
title: Border
level: 2
---

# Border
Everything is a box


<!-- 

Slide notes: 

-->


---
title: CSS box model
level: 2
---

# The two sizing models
Everything is a box

The `box-sizing` CSS property allows us to include the padding and boarder in the calculation of an element’s height and width.


<!-- 

Slide notes: 

-->



---
title: CSS box model resources
level: 2
layout: image-right
image: /images/slides/css/selectors/books.jpg
---


# Box model resources
Guides and cheatsheets

* [Box model - Odin project](https://www.theodinproject.com/lessons/foundations-the-box-model)
* [Box model - Learn the web](https://learntheweb.courses/topics/box-model/)
* [Box sizing - Prof3ssorSt3v3](https://www.youtube.com/watch?v=EfCE-a31OiM&list=PLyuRouwmQCjl4wTSNbb8RTKZuyMhoIxBe&index=52) 
* [Box model - MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
* [Box model - Code academy](https://www.codecademy.com/resources/docs/css/box-model)

<!-- 

Slide notes: 

Credit: 


-->
