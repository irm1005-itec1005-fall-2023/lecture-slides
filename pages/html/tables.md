---
layout: intro
title: HTML tables
level: 1
---

# HTML Tables

Marking up HTML Tables



---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

Consists of one `<table>` element and one or more `<tr>`, `<th>`, and `<td>` elements inside `<thead>` and `<tbody>` elements.


```html
<table>
  <thead>
    <tr>
      <th>Month</th>
      <th>OC Transpo Ridership</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>300000</td>
    </tr>
    ...
  </tbody>
</table>
```

<!-- 

Slide notes: 

-->




---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

Let's build the HTML markup for the following table:

<table>
  <thead>
    <tr>
      <th><strong>Month</strong></th>
      <th><strong>OC Transpo Ridership</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>300000</td>
    </tr>
    <tr>
      <td>February</td>
      <td>320000</td>
    </tr>
    <tr>
      <td>March</td>
      <td>330000</td>
    </tr>
    <tr>
      <td>April</td>
      <td>340000</td>
    </tr>
    <tr>
      <td>May</td>
      <td>290000</td>
    </tr>
    <tr>
      <td>June</td>
      <td>250000</td>
    </tr>
  </tbody>
</table>

<!-- 

Slide notes: 

-->




---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

We start by adding our `<table>` element


```html
<table>
  <!-- Table content will go in here -->
</table>
```

<!-- 

Slide notes: 

-->


---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

We then add our `<thead>` and `<tbody>` elements to our our `<table>` element


```html
<table>
  <thead>
    <!-- Our table headings will go in here -->
  </thead>
  <tbody>
    <!-- And our table content will go in here -->
  </tbody>
</table>
```

<!-- 

Slide notes: 

-->



---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

We then add our table row `<tr>` to our heading section in our `<thead>`


```html
<table>
  <thead>
    <tr>
      <!-- table row -->
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
```

<!-- 

Slide notes: 

-->


---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

We then add a table heading `<th>` for each column in our table row heading


```html
<table>
  <thead>
    <tr>
      <!-- The heading for the month column -->
      <th>Month</th>
      <!-- The heading for the ridership column -->
      <th>OC Transpo Ridership</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
```

<!-- 

Slide notes: 

-->



---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

Now we can add a `<tr>` to our `<tbody>` section 


```html
<table>
  <thead>
    <tr>
      <th>Month</th>
      <th>OC Transpo Ridership</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <!-- Our table data will go here -->
    </tr>
  </tbody>
</table>
```

<!-- 

Slide notes: 

-->




---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

Then we can add in our table data `<td>` to our table rows in our `<tbody>` section 


```html
<table>
  <thead>
    <tr>
      <th>Month</th>
      <th>OC Transpo Ridership</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <!-- Table data for the month column -->
      <td>January</td>
      <!-- Table data for the ridership column -->
      <td>300000</td>
    </tr>
  </tbody>
</table>
```

<!-- 

Slide notes: 

-->


---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

Finally we add in our remaining table data `<td>` to our table


```html
<table>
  <thead>
    <tr>
      <th>Month</th>
      <th>OC Transpo Ridership</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>300000</td>
    </tr>
     <tr>
      <td>February</td>
      <td>320000</td>
    </tr>
    ...
  </tbody>
</table>
```

<!-- 

Slide notes: 

-->

---
layout: two-cols-header
title: Semantic elements
level: 2
---

# Tables
Used when you need to display tabular data

::left::

```html
<table>
  <thead>
    <tr>
      <th>Month</th>
      <th>OC Transpo Ridership</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>300000</td>
    </tr>
     <tr>
      <td>February</td>
      <td>320000</td>
    </tr>
    ...
  </tbody>
</table>
```

::right::

<table>
  <thead>
    <tr>
      <th><strong>Month</strong></th>
      <th><strong>OC Transpo Ridership</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>300000</td>
    </tr>
    <tr>
      <td>February</td>
      <td>320000</td>
    </tr>
    <tr>
      <td>March</td>
      <td>330000</td>
    </tr>
    <tr>
      <td>April</td>
      <td>340000</td>
    </tr>
    <tr>
      <td>May</td>
      <td>290000</td>
    </tr>
    <tr>
      <td>June</td>
      <td>250000</td>
    </tr>
  </tbody>
</table>


---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

Other table elements include `<caption>`, `<colgroup>`, `<tfoot>`. Since these elements aren't used very frequently we don't cover them here.

While beyond the scope of this course, for more complex tables, you may run into `rowspan` and `colspan` attributes. These attributes help you layout tables that have a high degree of complexity. 



---
title: Table Resources
level: 2
layout: image-right
image: /images/slides/html/tables/you-got-this.jpg
---


# Table resources
Guides and cheatsheets

* [The Table element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)
* [Learning about HTML Tables](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)
* [Building and Styling HTML Tables - Prof3ssorSt3v3](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)
* [HTML Tables - W3C](https://www.w3.org/TR/html401/struct/tables.html)
* [HTML Tables Cheatsheet](https://www.codecademy.com/learn/learn-html/modules/learn-html-tables/cheatsheet)

<!-- 

Slide notes: 

Credit: 

Photo by Prateek Katyal: https://www.pexels.com/photo/black-and-white-laptop-2740956/ 

-->
