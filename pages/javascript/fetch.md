---
title: JavaScript fetch
layout: intro
---

# JavaScript Fetch
Grabbing data from APIs 


---
title: JavaScript fetch
level: 2
---

# Introduction 
JavaScript fetch 

The `fetch()` method provides an easy way for JavaScript developers to get data asynchronously. `fetch()` returns a Promise. 

```js
// Address of the API 
const API_URL = "https://pokeapi.co/api/v2/pokemon/8"

// Running the fetch method
fetch(API_URL);

```


---
title: JavaScript fetch
level: 2
---

# Introduction 
JavaScript fetch 

Since `fetch()` returns a Promise, we have to use the `then()` method to handle a successful resolution.

```js
// Address of the API 
const API_URL = "https://pokeapi.co/api/v2/pokemon/8"

// Running the fetch method
fetch(API_URL)
  .then((result) => {
    // Handle the response
  })

```


---
title: JavaScript fetch
level: 2
---

# Introduction 
JavaScript fetch 

Since `fetch()` returns a Promise, we have to use the `catch()` method to handle any error situations.

```js
// Address of the API 
const API_URL = "https://pokeapi.co/api/v2/pokemon/8"

// Running the fetch method
fetch(API_URL)
  .then((response) => {
    // Handle the response
  })
  .catch((response) => {
    // Whoops, something went wrong
  });

```



---
title: JavaScript fetch
level: 2
---

# Introduction 
JavaScript fetch 

`fetch()` has two steps to accessing the response data. 

The first step sends the request. In the second step we need to "unpack" the response using the `json()` method (assuming the API is sending us data back in JSON).

```js
// Address of the API 
const API_URL = "https://pokeapi.co/api/v2/pokemon/8"

// Running the fetch method
fetch(API_URL)
  .then((response) => {
    // We need to "unpack" the response object using the json() method
    return response.json();
  });
```



---
title: JavaScript fetch
level: 2
---

# Introduction 
JavaScript fetch 

Lastly, we deal with the result of that second Promise and finally have access to the data that came back from the API.

```js
// Address of the API 
const API_URL = "https://pokeapi.co/api/v2/pokemon/8"

// Running the fetch method
fetch(API_URL)
  .then((response) => {
    // We need to "unpack" the response object using the json() method
    return response.json();
  })
  .then((data) => {
    console.log("Data from fetch", data);
  })
```


---
title: JavaScript fetch
level: 2
---

# Introduction 
JavaScript fetch 

We then add our `catch()` method to deal with any errors that might have occured

```js
// Address of the API 
const API_URL = "https://pokeapi.co/api/v2/pokemon/8"

// Running the fetch method
fetch(API_URL)
  .then((response) => {
    // We need to "unpack" the response object using the json() method
    return response.json();
  })
  .then((data) => {
    console.log("Data from fetch", data);
  })
  .catch((response) => {
    // Whoops, something went wrong
    console.log("ERROR");
  });
```


---
title: JavaScript fetch
level: 2
---

# Async and await 
JavaScript fetch 

Another way to use `fetch()` without the `then()` method is to use async and await key words

```js
// Address of the API 
const API_URL = "https://pokeapi.co/api/v2/pokemon/8"

// The function that has await inside it MUST have the async keyword 
async function fetchPokemon() {
    const response = await fetch(API_URL);
    const data = await response.json();
    console.log("Data from fetch using async await", data);
}

// Run the async function
fetchPokemon(); 
```


---
title: JavaScript fetch
level: 2
---

# Error handling with async await
JavaScript fetch 

Since we don't have a `catch()` method with async await, we need to use a different way to cover error handling

```js
// Address of the API 
const API_URL = "https://pokeapi.co/api/v2/pokemon/8"

// The function that has await inside it MUST have the async keyword 
async function fetchPokemon() {
  try {
    const response = await fetch(API_URL);
    const data = await response.json();
    console.log("Data from fetch using async await", data);
  }
  catch(error) {
    console.log("Error occured: ", error);
  }  
}
// Run the async function
fetchPokemon(); 
```
