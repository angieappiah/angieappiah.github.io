---
layout: post
title:      "Asynchronous Fetch Process"
date:       2021-03-04 00:02:13 +0000
permalink:  asynchronous_fetch_process
---



Asynchronous code takes statements outside of the main program flow and allows the code after the asynchronous call to be executed immediately without waiting.

Fetch API interface on the other hand allows the browser to make HTTP requests to web servers.
Example: fetch('http://localhost:3000/api/v1/galleries/1/pieces')

The code below will be used as an example, to explain the asynchronous flow.
```


    handleClick = (piece) => {
        console.log('a')
        fetch('http://localhost:3000/api/v1/galleries/1/pieces')
        .then(res => {
            console.log('b')
            return res.json()})
        .then(data => console.log('c', data))
        .catch(err => console.log('d', err))
        console.log('e')
    }

```

Fetch request is called, In this case fetch('http://localhost:3000/api/v1/galleries/1/pieces')
The fetch request returned a promise, that resolved to a response object. A promise represents the future result of the asynchronous operation. Promise objects can be: Pending, Fulfilled/Resolved or Rejected. 


OUTPUT
In the example above the output will be 
a
e
b
c

 


 


EXPLAINING THE OUTPUT

console.log(‘a’): The code before the asynchronous call is console.log('a') it does not have to wait for a promise to be resolved. JavaScript executes from top to bottom, in order with which the code appears, the first to be logged is “a”

console.log (‘e’): “e” is also the next, the code after the asynchronous call to be executed immediately without waiting is console.log (‘e’).  This was logged because it also did not have to wait for a promise, the next inline of the order was e.

console.log(‘b’): “b” on the other hand waited for the fetch request, that returned a promise, 

 console.log (‘c’): was the last to be logged. When the promise resolved, the response was passed 'c'. which rendered the array of objects with galleries and pieces that are associated with the gallery. 


console.log (‘d’, err) was not logged because no error occurred.  When a Promise object is "rejected", the result is the corresponding error.

The content of your blog post goes here.
