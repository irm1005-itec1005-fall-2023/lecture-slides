---
title: JavaScript promises
layout: intro
---

# JavaScript Promises
Doing two things at once in JavaScript


---
title: JavaScript promises
level: 2
---

# Introduction 
JavaScript promises 

Promises are like a contract, but in JavaScript. 

JavaScript is, by default, single threaded, so all of our code is executed in sequence, one line after another. 

Unfortunetly, if one line of code, or one function for example, takes too long to execute, our application would get stuck, and sit and wait until that line completed it's operation. 

This would create a horrible user experience - imaging if your app completely froze everytime it had to fetch data or run a complicated calculation. 

Enter Promises. Promises are a way for us to handle asynchronous operations in JavaScript.

We can insert code that could potentially take a long time to run into a Promise, and then be notified by JavaScript when that Promise has completed execution (resolved).



---
title: JavaScript promises
level: 2
---

# The four different states of a Promise 
JavaScript promises 

* **fulfilled**: Action related to the promise succeeded
* **rejected**: Action related to the promise failed
* **pending**: Promise is still pending i.e. not fulfilled or rejected yet
* **settled**: Promise has fulfilled or rejected




---
title: JavaScript promises
level: 2
---

# Setting up our first promise
JavaScript promises 

For example, here is how we setup a promise and identify resolved and rejected values


```js
// Create a promise using the Promise object
const myFirstPromise = new Promise((resolve, reject) => {
  // Set a max for our random number 
  const MAX = 10;
  // Returns a random number from 0 to MAX
  const random = Math.floor(Math.random() * 10);
  // Check the value of the random number is greater than 5
  if (random > 5) {
    // Success!
    resolve("Hooray");
  }
  else {
    // Not so successful
    reject("Not High Enough");
  }
});
```



---
title: JavaScript promises
level: 2
---

# Consuming our promise
JavaScript promises 

And here is how we execute our promise, and handle a successful resolved case

```js
// We execute the promise using the "then" method
// and pass in an function to handle the response
myFirstPromise
  .then((result) => {
    console.log("Resolved response from Promise: " , result);
});

// You can name the result argulment variable anything you want - this works
myFirstPromise
  .then((message) => {
    console.log("Resolved response from Promise: " , message);
});
```




---
title: JavaScript promises
level: 2
---

# Consuming our promise
JavaScript promises 

And here is we use a catch method to deal with a rejected state from our promise

```js
// We execute the promise using the "then" method
// and pass in an function to handle the response
myFirstPromise
  .then((result) => {
    console.log("Resolved response from Promise: " , result);
  })
  .catch((result) => {
    console.log("Rejected response from Promise: " , result);
  });


```




---
title: JavaScript promises
level: 2
---

# Consuming our promise
JavaScript promises 

And here is we use the finally method to run some code after our promise either resolves or was rejected

```js
// We execute the promise using the "then" method
// and pass in an function to handle the response
myFirstPromise
  .then((result) => {
    console.log("Resolved response from Promise: " , result);
  })
  .catch((result) => {
    console.log("Rejected response from Promise: " , result);
  });
  .finally(() => {
    console.log("Promise has finally completed");
  });


```



---
title: JavaScript promises
level: 2
---

# Waiting for multiple promises 
JavaScript promises 

What if we had multiple Promises that we needed to execute and wait for before doing something. No problem. Let's setup three promises. 

```js
const myFirstPromise = new Promise((resolve,reject) => {
  resolve("My First Promise Resolved Response");
})

const mySecondPromise = new Promise((resolve,reject) => {
  resolve("My Second Promise Resolved Response");
})

const myThirdPromise = new Promise((resolve,reject) => {
  resolve("My Third Promise Resolved Response");
})

```



---
title: JavaScript promises
level: 2
---

# Waiting for multiple promises 
JavaScript promises 

What if we had multiple Promises that we needed to execute and wait for before doing something. No problem. Let's setup three promises. 

```js
// This will wait for all of the promises to be executed
Promise.all([
  myFirstPromise,
  mySecondPromise,
  myThirdPromise
])
  .then((results) => {
    // We get an array of all of the resolved responses
    console.log(results)
  })

```

