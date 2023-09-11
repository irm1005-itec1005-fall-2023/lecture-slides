---
layout: intro
title: HTML semantic tags
level: 1
---

# HTML Semantics

Semantic - What purpose or role does this HTML element have 


---
title: Semantic elements
level: 2
---

<img class="h-full" src="/images/slides/html/semantics/semantic-no-tags.png" alt="" />

<!-- 

Slide notes: 

-->


---
title: Semantic elements
level: 2
---

<img class="h-full" src="/images/slides/html/semantics/semantic-tags.png" alt="" />

<!-- 

Slide notes: 

-->

---
title: Semantic elements
level: 2
---

# Semantic elements
The elements that think they are cooler

* `<header>` — for more important information, like the masthead of the website, where the name and logo and navigation are
* `<nav>` — navigation, defining the navigation of the website
* `<footer>` — for less important information, like the footer of the website, usually includes the copyright statement, social icons, etc.
* `<main>` — for defining the primary content
* `<aside>` — for secondary information, stuff that’s not required to understand the primary content, like sidebars, pull quotes, etc.
* `<section>` — the generic section element



---
title: Semantic elements
level: 2
---

# HTML page sample

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
  <header>...</header>

  <!-- The <main> content of the website: what your user came to see -->
  <main>
    <h1>All of the dogs</h1>
    ...
  </main>

  <aside>...</aside>

  <footer>...</footer>
</body>
</html>
```


---
title: Semantic elements
level: 2
---

# Simplified header / nav bar example

```html
...
<body>
  <header>
    <h2>Site title</h2> <!-- Your document sections must have a header -->

    <img src="/images/logo.png" alt="Company Logo" />

    <nav>
      <ul>
        <li><a href="home.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>

  </header>
    ...
</body>
</html>
```


---
title: Semantic elements
level: 2
---

# Simplified header / nav bar example

* Have an `<h2>` heading in your `<heading>` section to give your document proper heading structure 
* Use the `<nav>` element with an unordered list for any site navigation
* Do not put an `<h1>` in any document section other than `<main>`



---
title: Semantic elements
level: 2
---

# Main content area

```html
...
<body>
  ...
  <main>
    <h1>Page heading</h1> <!-- Your document sections must have a header -->

    <section>
      <h2>Chapter one</h2>
      ...

        <section>
          <h3>Sub chapter one alpha</h3>
          ...
        </section>

    </section>
    ...
  </main>
    ...
</body>
</html>
```


---
title: Semantic elements
level: 2
---

# Main content area

* Have an `<h1>` heading in your `<main>` content area to give your document proper heading structure 
* Use the `<section>` or `<article>` elements to further organise the content 
* `<section>` elements should be wrapped around every heading (except for the `<h1>`)


---
title: Semantic elements
level: 2
---

# Simplified footer with navigation example

```html
...
<body>
  ...
  <footer>
    <h2>Site footer information</h2> <!-- Your document sections must have a header -->

    <img src="/images/logo.png" alt="Company Logo" />

    <nav>
      <ul>
        <li><a href="home.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>

  </footer>
</body>
</html>
```


---
title: Semantic elements
level: 2
---

# Simplified footer with navigation example

* Have an `<h2>` heading in your `<footer>` section to give your document proper heading structure 
* Use the `<nav>` element with an unordered list for any site navigation within the footer
* Do not put an `<h1>` in any document section other than `<main>`
