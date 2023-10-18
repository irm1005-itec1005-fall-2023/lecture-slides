---
title: JavaScript events
layout: intro
---

# JavaScript Events
Handling all sorts of events


---
title: JavaScript events
level: 2
---

# Introduction 
JavaScript events 

Events are actions that occur in the browser that you can listen to and then respond accordingly. There are many different types of events that we can listen to.

For example: 

* When the browser detects a network connection has been disconnected 
* When the web page finishes loading 
* When a button is clicked 
* When the browser window is resized 
* When a key on the keyboard is tapped 

We can respond to specific events by adding an event handler to the event. This is usualy in the form of a named or anonymous function that runs when the event is "fired". This is referred to as "registering an event handler". 


---
title: JavaScript events
level: 2
---

# Introduction 
JavaScript events 

For example, here is how we register a function to run when the button is clicked

```html
<!-- Button on our page in HTML -->
<button id="btn-1">Click me</button>

```

```js
// Select the button
const btn = document.querySelector("#btn-1");

// Function to run 
function buttonHandler(e) {
    console.log("I am clicked!");
}

// Register the event handler on the button
btn.addEventListener("click", buttonHandler);
```



---
title: JavaScript events
level: 2
---

# Other types of events 
JavaScript events 

Though we mostly look at `click` or `submit` events, there are tonnes of different types of events that we can register and listen to. 

For example `dblclick` events occur when the user double clicks their mouse. And `mouseover` and `mouseout` can give us the state of the user's mouse and if it is over a specific element. 



---
title: JavaScript events
level: 2
---

# Event object
JavaScript events 

An event object is passed into our event handler function. Common practice is to call this object `e` or `event`.

The event object has a standard set of properties and methods available that can help us determine what was triggering the event and where on the screen the event occured.  

```js
// Select the button
const btn = document.querySelector("#btn-1");

// Register the event handler on the button
btn.addEventListener("click", buttonHandler);

// Function to run 
// Note the event object that is sent to the console.log
function buttonHandler(event) {
    console.log("Event object", event);
}
```

[Event Object Reference](https://developer.mozilla.org/en-US/docs/Web/API/Event)



---
title: JavaScript events
level: 2
---

# Events and forms
JavaScript events 

HTML forms by default have an associated behavior to them. And so, if we are listening to, and working with events related to HTML forms, we need to disable the default browser behaviour. 

Thankfully, this can be done easily with one function call. 


```html
<!-- Form on our page in HTML -->
<form id="form-1">...</form>

```

```js
// Select the form
const form = document.querySelector("#form-1");

// Register the event handler on the form when the form is submitted
form.addEventListener("submit", formHandler);

// Function to run 
function formHandler(e) {
    e.preventDefault(); // prevents the browser from submitting the form
    console.log("I am clicked!");
}


```


---
title: JavaScript events
level: 2
---

# Event bubbling
JavaScript events 

Event bubbling describes how an event is passed from the lowest child up the tree of parents.

While this may seem counterintuitive, consider a `<button>` inside two nested parent `div`s. Technically, when the user clicks the `<button>`, that button resides in the two parents, and so JavaScript sends the events up the dom (know as "bubbling events").



---
title: JavaScript events
level: 2
layout: center
---

<img src="/images/slides/javascript/events/bubbling.png" alt="" />



---
title: JavaScript events
level: 2
---

# Event bubbling
JavaScript events 

If event bubbling is having unintended consequnces in your application, you can turn it off easily with the `.stopProrogation()` method. 


```js
// Select the button
const btn = document.querySelector("#btn-1");

// Register the event handler on the button
btn.addEventListener("click", buttonHandler);

// Function to run 
// Note the event object that is sent to the console.log
function buttonHandler(event) {
    event.stopProrogation(); // Stop the event from bubbling further up
    console.log("Event object", event);
}
```




---
title: JavaScript events
level: 2
---

# Event delegation
JavaScript events 

The following pattern allows us to add one event handler and listen to all of the child events. 

In the example below, on line 9, we are filtering out any clicks that weren't made by `<button>` elements.

```html
<!-- Button on our page in HTML -->
<ul id="list-1">...</ul>

```

```js
// Select the button
const list = document.querySelector("#list-1");

// Register the event handler on the button
list.addEventListener("click", listClickHandler);

// Function to run 
function listClickHandler(event) {
    if (event.target.nodeName !== "BUTTON") { 
        return; 
    }
    console.log("Event object", event.target.nodeNmae);
}
```
