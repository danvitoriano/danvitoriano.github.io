---
published: true
title: JavaScript difference between .call and .apply
layout: post
---
The difference is that `apply` lets you invoke the function with arguments as an array; 

`call` requires the parameters be listed explicitly. 

A useful mnemonic is "A for array and C for comma."

Example with Backbone.js:

// call the doStuff function

`container.call("doStuff", 1, 2);`

// apply the doStuff function

`container.apply("doStuff", [1, 2]);`