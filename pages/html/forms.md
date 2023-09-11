---
layout: intro
title: HTML forms
level: 1
---

# HTML Forms

Marking up HTML Forms



---
title: Forms
level: 2
layout: image-right
image: /images/slides/html/forms/form.jpg
---

# We want your inputs
Forms enable users to provide input data

The `<form>` HTML element represents a document section containing interactive controls for submitting information.


Forms are a very powerful tool for interacting with users — most commonly they are used for collecting data from users, or allowing them to control a user interface. 

In this section we will cover all the essential aspects of HTML forms including properly marking up their structure, validating form data, and submitting data to the server.


<!-- 

Slide notes:

Credit: Photo by Cytonn Photography: https://www.pexels.com/photo/close-up-photography-of-person-writing-on-white-paper-955392/

-->

---
layout: two-cols-header
title: Forms
level: 2
---


# Example form

::left::

We're going to learn about forms by building a simple contact us form.

Our form will contain three text fields, one range field, and one button. 

We are asking the user for:

* their name, 
* their email,
* the level of urgency of their message, and 
* the message they want to send

Hitting the button will send their data to a web server.

::right::

<div class="border p-3 bg-gray-50 ml-10 shadow-xl">

<p><strong>Contact Form:</strong></p>

<label>Name:</label>
<input type="text" class="ml-4 border border-gray-300" placeholder="Chris Rogers"/>

<label>Email:</label>
<input type="text" class="ml-4 border border-gray-300" placeholder="chris@avengers.com"/>

<label>Urgency:</label>
<input type="range" class="ml-4 border border-gray-300" />

<label>Message:</label>
<textarea class="ml-1 border border-gray-300" rows="5"></textarea>

<button class="border border-gray-300 bg-white p-2" type="sybmit">Submit</button>

</div>


<!-- 

Slide notes: 

-->



---
title: Forms
level: 2
---

# Forms
Forms enable users to provide input data

We start by adding a `<form>` element and in most cases add an `action` and a `method` attribute.

```html
<form action="/server-page-handling-form-data" method="post">
  <!-- Form elements go in here -->
</form>
```

**Notes:** 

* The `action` attribute defines the location (URL) where the form's collected data should be sent when it is submitted.
* The `method` attribute defines which HTTP method to send the data with (usually `get` or `post`).


<!-- 

Slide notes: 

-->



---
title: Forms
level: 2
---

# Forms
Forms enable users to provide input data

Our contact form requires the following input elements as well as a `label` for each

* An input field for the name as a single line of text (`input` type `text`)
* An input field for the email as a single line of text that should only accept email addresses (`input` type `email`)
* An input field for the urgency range that accepts a number based on how urgent the issue is (`input` type `range`)
* An input field for the message text that has multiple lines (`textarea` element)



<!-- 

Slide notes: 

-->


---
title: Forms
level: 2
---

# Forms
Forms enable users to provide input data

We add our first `input` element of type `text` as well as the `label`


```html
<form action="/server-page-handling-form-data" method="post">
  <ul>
    <li>
      <label for="fullname">Name:</label>
      <input type="text" id="fullname" name="fullname" placeholder="Chris Rogers"/>
    </li>
  </ul>
</form>
```

**Notes:** 

* Take a look at the `for` `id` and `name` attributes that are used to wire up the label and the `input` element
* The `placeholder` attribute allows us to put helper text in the form element


<!-- 

Slide notes: 

-->



---
title: Forms
level: 2
---

# Forms
Forms enable users to provide input data

Next we add our form elements to capture the users' email address


```html
<form action="/server-page-handling-form-data" method="post">
  <ul>
    ...
    <li>
      <label for="email">Email:</label>
      <input type="email" id="email" name="email" placeholder="chris@avengers.com"/>
    </li>
  </ul>
</form>
```

**Notes:** 

* The `type` value is now set to `email`


<!-- 

Slide notes: 

-->



---
title: Forms
level: 2
---

# Forms
Forms enable users to provide input data

Next we add our form elements to capture the urgency value using the slider


```html
<form action="/server-page-handling-form-data" method="post">
  <ul>
    ...
    <li>
      <label for="urgency">Urgency:</label>
      <input type="range" id="urgency" name="urgency" />
    </li>
  </ul>
</form>
```

**Notes:** 

* The `type` value is now set to `range`


<!-- 

Slide notes: 

-->



---
title: Forms
level: 2
---

# Forms
Forms enable users to provide input data

We then use the `textarea` element to capture multiple lines of text


```html
<form action="/server-page-handling-form-data" method="post">
  <ul>
    ...
    <li>
      <label for="message">Message:</label>
      <textarea id="messsage" rows="5"></textarea>
    </li>
  </ul>
</form>
```

**Notes:** 

* The `rows` attribute sets the number of rows that are visible for the `textarea` input. Users may type more than 5 rows of text.


<!-- 

Slide notes: 

-->



---
title: Forms
level: 2
---

# Forms
Forms enable users to provide input data

Lastly we add a submit button using the `<button>` element 


```html
<form action="/server-page-handling-form-data" method="post">
  <ul>
    ...
    <li>
      <button type="submit">Submit</button>
    </li>
  </ul>
</form>
```

**Notes:** 

* We have to put a `type=submit` attribute on our `<button>` to make it work with the form
* The `<button>` doesn't require a label


<!-- 

Slide notes: 

-->



---
title: Forms
level: 2
---

# Full form code:

```html
<form action="/server-page-handling-form-data" method="post">
  <ul>
    <li>
      <label for="fullname">Name:</label>
      <input type="text" id="fullname" name="fullname" placeholder="Chris Rogers"/>
    </li>
    <li>
      <label for="email">Email:</label>
      <input type="email" id="email" name="email" placeholder="chris@avengers.com"/>
    </li>
    <li>
      <label for="urgency">Urgency:</label>
      <input type="range" id="urgency" name="urgency" />
    </li>
    <li>
      <label for="message">Message:</label>
      <textarea id="messsage" rows="5"></textarea>
    </li>
    <li><button type="submit">Submit</button></li>
  </ul>
</form>
```

<!-- 

Slide notes: 

-->


---
title: Forms
level: 2
---

# Client side validation 
Forms enable users to provide input data

HTML has some attributes that we can use to validate input that the client is providing. 

Not only can we make specific form fields required, we can also validate that numbers are a specific range, or text input follows a specific pattern.

The code sample below shows how to use the `required` attribute to make an input mandatory.

```html 
<form>
  ...
  <label for="password">Name (required)</label>
  <input id="fullname" name="fullname" type="text" required="required" />
  ...
</form>
```

<!-- 

Slide notes: 

-->



---
title: Forms
level: 2
---

# Other types of inputs
Forms enable users to provide input data

The `<input>` element has a many of different types so that we can collect different types of data from a user. We have seen `text` and `range`, and there in total 22 different types available. 

Some examples of these are `date`, `time`, `tel`, `password`, `number`, `checkbox` to name a few.

We also have the `select` element which allows us to add drop down lists to our forms.

```html 
<form>
  ...
  <label for="password">Password (required)</label>
  <input id="password" name="password" type="password" required="required" />
  ...
</form>
```

[List of input types and examples](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

[The select element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select)

<!-- 

Slide notes: 

-->


---
title: Forms
level: 2
---

# Form accessibility
Forms enable users to provide input data

* It is absolutely critical that your form elements all have a `<label>` and the `<label>` has a `for` attribute that matches an `<input>` field
* If you click on the form `<label>` the browser will transfer focus to the `<input>` element. If this doesn't happen it's possible that something is wrong with your form.
* You must have the `<form>` element wrap all of your `<input>` elements.
* The `id` attributes that you use in your form elements must be unique and cannot start with a number

<!-- 

Slide notes: 

-->


---
title: Forms Resources
level: 2
layout: image-right
image: /images/slides/html/forms/confused.jpg
---


# Forms resources
Guides and cheatsheets

* [The Form element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)
* [Working with web forms](https://developer.mozilla.org/en-US/docs/Learn/Forms)
* [HTML Forms and JavaScript - Prof3ssorSt3v3](https://www.youtube.com/watch?v=ikR9DsGMUMc&list=PLyuRouwmQCjncCz8JChyPNRBvm2ONGYa2)
* [Mobile Keyboards and HTML Forms - Prof3ssorSt3v3](https://www.youtube.com/watch?v=WGk-2_dD6L0&list=PLyuRouwmQCjncCz8JChyPNRBvm2ONGYa2&index=28)
* [HTML Forms - Marksheet](https://marksheet.io/html-forms.html)
* [HTML Forms - W3C](https://www.w3.org/TR/html401/interact/forms.html)

<!-- 

Slide notes: 

Credit: 

Photo by Andrea Piacquadio: https://www.pexels.com/photo/a-man-in-red-shirt-covering-his-face-3760043/

-->
