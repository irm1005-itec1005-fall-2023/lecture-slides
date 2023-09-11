---
layout: intro
title: HTML content tags
level: 1
---

# HTML Content

📖 Marking up content like `<p>`, `<h1>`, and `<img>` tags


---
title: Content Elements
level: 2
---

# Content tags
Marking up content

Here are a few of the main content tags that we use when building pages. There are some more obscure tags that have been left off this list for brevity.

* `<p>`
* `<h1>` - `<h6>`
* `<ul>` - `<ol>` - `<dl>`
* `<a>`
* `<br />`
* `<strong>`
* `<em>`
* `<blockquote`

---
title: Paragraphs
level: 2
---

# Paragraphs
Marking up content

Paragraph tag for, you guessed it, paragraphs of text.

```html
<p>Meatloaf andouille bacon alcatra short ribs. Salami meatball spare ribs,
     shankle ribeye burgdoggen bacon pork. Beef andouille pig biltong.</p>

<p>Drumstick andouille boudin, shankle jowl pork chop chuck picanha
     short loin pork loin kevin chicken fatback.</p>
```

<div class="text-sm">

[\<p> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)

</div>


<!-- 

Slide notes: 

-->



---
title: Headings
level: 2
---

# Headings
Marking up content

Heading elements allow you to specify what content on your page is a heading or sub heading.

* There should only be one `<h1>` on the page
* Do not skip heading levels

```html
<!-- 6 heading levels: -->
<h1>Earth</h1>
  <h2>North America</h2>
    <h3>Canada</h3>
      <h4>Ontario</h4>
        <h5>Ottawa</h5>
          <h6>Kanata</h6>
    <h3>United States</h3>
      <h4>California</h4>
  <h2>Africa</h2>
    <h3>Egypt</h3>
      <h4>Cairo</h4>
```

<div class="text-sm">

[\<h1>-\<h6> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements)

</div>

<!-- 

Slide notes: 

* Although HTML allows it, you should only have one <h1> on the page

-->



---
title: Lists
level: 2
---

# Lists
Marking up content

There are three types of lists that can be marked up. 

`<ul>` Unordered lists - for when the order of the items in the list don't matter, such as a list of things to buy at the grocery store 

```html
<ul>
    <li>Milk</li>
    <li>Eggs</li>
    <li>Chips</li>
    <li>Bananas</li>
</ul>
```

<div class="text-sm">

[\<ul> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)

</div>

<!-- 

Slide notes: 

-->


---
title: Lists
level: 2
---

# Lists
Marking up content

There are three types of lists that can be marked up. 

`<ol>` Ordered lists - for when the order of the items is important, like instructions in a recipe

```html
<ol>
    <li>Add Milk</li>
    <li>Beat the eggs and add to the milk</li>
    <li>Smash the bananas and set aside</li>
</ol>
```

<div class="text-sm">

[\<ol> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)

</div>

<!-- 

Slide notes: 

-->


---
title: Definition lists
level: 2
---

# Lists
Marking up content

There are three types of lists that can be marked up. 

`<dl>` Description lists - for defining data and value pairs

```html
<dl>
    <dt>Length</dt>
    <dd>12 metres</dd>

    <dt>Mass</dt>
    <dd>5.4 metric tons</dd>
</dl>
```

<div class="text-sm">

[\<dl> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl)

</div>

<!-- 

Slide notes: 

-->



---
title: Links
level: 2
---

# Links
Marking up content

Links are the key to the whole web! Here's how to make a link. 

First identify the text that you want to make a link.

```html
<p>Buster likes to go the groomer name <a>Martin</a></p>
```

Then add an `href` attribute to the `<a>` tag. 

```html
<p>Buster likes to go the groomer name <a href="">Martin</a></p>
```

Finally, add the web address to the `href` attribute 

```html
<p>Buster likes to go the groomer name <a href="https://martin.cutshair.com">Martin</a></p>
```

<div class="text-sm">

[\<a> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)

</div>

<!-- 

Slide notes: 

-->


---
title: Images
level: 2
---

# Images
Marking up content

The `<img>` tag is used to display images on a web page.

* Images need two attributes to specify extra details about the image: 
  * `src` - the location of the image and;
  * `alt` - the description of the meaningful information in the image (or empty if the image is decorative)

```html
<img src="buster.jpg" alt="Photo of Buster" />
```

<div class="text-sm">

[\<img /> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img)

</div>

<!-- 

Slide notes: 

-->


---
title: Line break
level: 2
---

# Line break
Marking up content

If you ever need to force a line break (enter / new line) in your content you can use the `<br />` tag to acheive this.

  * `br />` - Self closing tag and must have the trailing slash `/` 
  * `<br/>` - Can also be written without the space 

```html
<p>This is a paragraph<br />
   And this is on a new line<br />
   Also this is on a new line<br />
   And one more new line for good luck</p>
```

<div class="text-sm">

[\<br /> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br)

</div>

<!-- 

Slide notes: 

-->


---
title: Strong
level: 2
---

# Strong tag
Marking up content

The strong importance element

The `<strong>` element indicates that its contents have strong importance, seriousness, or urgency. 

* Browsers typically render the contents in bold type.
* **Note:** Do not use the `<b>` tag to add emphasis or importance to content

```html
<p>... the most important rule, the rule you can never forget, 
    no matter how much he cries, no matter 
    how much he begs: <strong>never feed him 
    after midnight</strong>.</p>
```

<div class="text-sm">

[\<strong> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong)

</div>

<!-- 

Slide notes: 

-->


---
title: Emphasis
level: 2
---

# Emphasis tag
Marking up content

The `<em>` element marks text that has stress emphasis. 

* Browsers typically render the contents in italics.

```html
<p>Something something something<em>this is important</em> something</p>
```

<div class="text-sm">

[\<em> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em)

</div>

<!-- 

Slide notes: 

-->


---
title: Blockquote
level: 2
---

# Blockquote
Marking up content

The `<blockquote>` element indicates that the enclosed text is an extended quotation. 

* Usually, this is rendered visually by indentation (see Notes for how to change it). 

```html
<blockquote>
    <p>The truth may be puzzling. It may take some work to grapple with.
  It may be counterintuitive. It may contradict deeply held
  prejudices. It may not be consonant with what we desperately want to
  be true. But our preferences do not determine what's true.</p>
</blockquote>
```

<div class="text-sm">

[\<blockquote> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote)

</div>

<!-- 

Slide notes: 

-->
