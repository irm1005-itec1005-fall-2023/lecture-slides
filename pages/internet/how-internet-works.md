---
layout: intro
title: How the internet works
level: 1
---

# How the internet works

The very basics of how the web works


---
title: Table of Contents for How the internet works
level: 2
---

# What's covered in this section
Going from computer connection to loaded website

* How the magic happens 
* Example HTTP Request and Response
* HTTP Status Codes

<!-- 

Slide notes: 

-->

---
title: Process for how the web works
level: 2
---

# How the magic happens
Going from computer connection to loaded website

1. The Internet
2. Browser sends a request
3. Server responds 
4. Response is processed
5. Page is displayed


<!-- 

Slide notes: 

-->


---
layout: two-cols
title: The Internet
level: 2
---

# The Internet
Step 1

* Worldwide system of computer networks 
* No one owns the internet, or controls who can connect to it
* TCP/IP is a networking standard that is used to standardize the way computers connect to each other and exchange information
* An IP address is used to uniquely identify every device. An example of an IP is `216.146.46.20`
* A packet of data is the basic unit of information transmitted over the internet
* DNS servers are used to find out what the real IP address of a domain name is

::right::
<div class="ml-10 bg-zinc-100">
<div class="flex justify-center">
    <img alt="" class="place-content-end h-120" src="/images/slides/internet/how-internet-works/map-01.png" />
</div>
</div>

<!-- 

Slide notes: 

Credit: 

https://thenounproject.com/icon/laptop-5407776/

-->

---
layout: two-cols
title: Client sends a request
level: 2
---

# Client sends a request
Step 2

* HTTP(s) is a protocal for fetching resources such as HTML documents
* HTTP(s) defines what the request and response should look like, which data may be included and how the request is submitted
* A client (such as browser) sends an HTTP request to the server asking it for a web page, or data, or some other asset file
* Web pages are also, but not commonly referred to as a "Hyper Text" documents, thus the name "Hyper Text Transfer Protocol (HTTP)"

::right::
<div class="ml-10 bg-zinc-100">
<div class="flex justify-center">
    <img alt="" class="place-content-end h-120" src="/images/slides/internet/how-internet-works/map-02.png" />
</div>
</div>



<!-- 

Slide notes: 

-->


---
layout: two-cols
title: Server responds
level: 2
---

# Server responds 
Step 3

* Server receives the request, processes it, and then sends back a response
* Web server software (e.g. IIS, Apache, Nginx) runs on the server, constantly listening for requests, and when one comes in it responds accordingly
* The response includes an HTTP Status Code, to indicate to the browser if the request was successful or not
* If the server approves the client's request, the server will respond with a "200 OK" status message and the web page that was requested


::right::
<div class="ml-10 bg-zinc-100">
    <div class="flex justify-center">
        <img alt="" class="place-content-end h-120" src="/images/slides/internet/how-internet-works/map-03.png" />
    </div>
</div>


<!-- 

Slide notes: 

-->



---
layout: two-cols-header
title: Client processes the response
level: 2
---

# Client processes the response
Step 4

::left::

* The client (browser) receives the response and then starts working through it
* If the response is a web page, the client will go through the HTML code and look for any links to other asset files (CSS, JavaScript, Fonts, Images, etc.) 
* The client will then send seperate requests for those files as well

::right::

* Server Response:

```html
HTTP/1.1 200 OK
Date: Sun, 23 Oct 2022 14:28:02 GMT
Server: Apache
Last-Modified: Tue, 01 Dec 2009 20:18:22 GMT
ETag: "51142bc1-7449-479b075b2891b"
Accept-Ranges: bytes
Content-Length: 29769
Content-Type: text/html

<!DOCTYPE html>… (the requested web page)
```


<!-- 

Slide notes: 

-->


---
title: Page is displayed
level: 2
layout: image-right
image: /images/slides/internet/how-internet-works/screen-01.png
---

# Page is displayed
Step 5

* As soon as the client starts receiving "chunks" of the web page it will start to put it together for the user
* The client "paints" the page on the screen by applying the styles (CSS), interactivity (JavaScript), and any images or other assets. 
* The user sees the page content and can begin to interact with it

<!-- 

Slide notes: 

-->



---
title: Example HTTP Request and Response
level: 2
---

# HTTP flow
Client / Server request and response

Client Request 

```html
GET / HTTP/1.1
Host: imd1005.ca
Accept-Language: en
```

Server Response 

```html
HTTP/1.1 200 OK
Date: Sun, 23 Oct 2022 14:28:02 GMT
Server: Apache
Last-Modified: Tue, 01 Dec 2009 20:18:22 GMT
ETag: "51142bc1-7449-479b075b2891b"
Accept-Ranges: bytes
Content-Length: 29769
Content-Type: text/html

<!DOCTYPE html>… (here come the 29769 bytes of the requested web page)
```

<!-- 

Slide notes: 

Credit: 

https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview

-->


---
title: HTTP Status Codes
level: 2
---

# HTTP Status Codes
A note about codes 

* 1xx (Informational): Request received, continuing process.
* 2xx (Successful): The action was successfully received, understood, and accepted.
* 3xx (Redirection): Further action needs to be taken in order to complete the request.
* 4xx (Client Error): The request contains bad syntax or cannot be fulfilled.
* 5xx (Server Error): The server failed to fulfil an apparently valid request.

<!-- 

Slide notes: 

Credit: 

https://dev.opera.com/articles/http-response-codes/

-->