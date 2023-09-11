---
layout: intro
title: HTML essentials
level: 1
---

# HTML Essentials

Everything you need to know about Hypertext Markup Language

---
title: So what is HTML
level: 2
---

# So what is HTML
The essentials

HTML is a markup language we use to define the structure of the content of our web pages. 

We use tags to define the content's purpose and give an element semantic meaning.

For example, the following text: 

```html
Buster is hungry 
```

If we wanted to identify that line as a paragraph of text, we would write the following: 

```html
<p>Buster is hungry</p>
```

`<p>` refers to the HTML tag, and "Buster is hungry" refers to the content within the tag.

<!-- 

Slide notes: 

-->


---
title: Anatomy of an HTML Element
level: 2
---

# Some common terms to understand
The essentials

```html
<p class="text-red">Buster is hungry</p>
```


* `<p>` - opening tag — the part to an element that defines where this type of content starts
* `</p>` - closing tag — the part of an element that defines where this type of content ends
* `class="text-red"` - attribute — a piece of metadata that isn’t usually visible in the browser but defines extra information about the element
* element — the combination of an open tag, the content, and a close tag

<!-- 

Slide notes: 

-->


---
title: Anatomy of an HTML Element
level: 2
---

# A note about nesting 
The essentials

You can put elements inside other elements. This is referred to as nesting. We also sometimes refer to these elements as having a parent-child relationship. 

Keep in mind that the elements have to be nested properly. 

```html
<p class="text-red">Buster is <strong>very</strong> hungry</p>
```

The element above will work fine.


```html
<p class="text-red">Buster is <strong>very hungry</p></strong>
```

The element above is not structured properly because the `<p>` tag is closed before the `<strong>` tag. 


<!-- 

Slide notes: 

-->




---
title: Comments
level: 2
---

# HTML Comments
The essentials

HTML comments are visible in the code of the page, but are not displayed in any way in the browser when the page is rendered. 

An HTML comment begins with a \<!-- and then ends with a -->. 


```html
<!-- This is a single line comment that will  not be displayed in the browser -->

<p>This is a paragraph <!-- This is an inline comment --> and nothing to see here</p>
```

<!-- 

Slide notes: 

Note: the code styling used currently makes the comment tags look silly 

-->

---
title: HTML Document
level: 2
---

# HTML Document
The essentials

Here is what the code for an empty basic HTML document looks like: 

```html
<!DOCTYPE html>
<html lang="en-ca">
<head>
  <meta charset="utf-8">
  <title>Title of the page</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta http-equiv="X-UA-Compatible" content="ie=edge" />
</head>
<body>
    <h1>Hello world</h1>
</body>
</html>
```

<!-- 

Slide notes: 

-->


---
title: HTML Document
level: 2
---

# HTML Document (con't)
The essentials

And here is a breakdown of every element: 

```html
<!DOCTYPE html>                     <!-- Tells the browser this is an HTML5 page -->
<html lang="en-ca">                 <!-- Opens the HTML tag and Sets the language of the page -->
<head>                              <!-- Container for metadata we declare information about the page -->
  <meta charset="utf-8">            <!-- Set's the character set to UTF-8 -->
  <title>Title of the page</title>  <!-- In the head we declare the title of the page -->
  <meta name="viewport" content="width=device-width, initial-scale=1" />
                                    <!-- Sets the zoom level (used for mobile)-->
  <meta http-equiv="X-UA-Compatible" content="ie=edge" />
                                    <!-- Addresses a compatibility issue with IE 11 -->
</head>
<body>                              <!-- The body section is where our page content goes -->
    <h1>Hello world</h1>
</body>
</html>                             <!-- Closes the html tag -->
```

<!-- 

Slide notes: 

-->
