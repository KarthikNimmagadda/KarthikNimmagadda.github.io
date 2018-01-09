---
layout: post
title: Reduce method complex example.
---
The purpose of this blog post is to give a sophisticated example of how to use reduce method.

Let's say You have a bookshop and you have customers that visit your library. For each customer, you have an order history of what books they have bought. The problem is to combine all the books from each customer into an array and create an unordered list.

I am using two reduces here, one will concatenate the arrays into a new array. The other will reduce the array to an unordered list.

```javascript
   var customers = [
   {
      name: 'Karthik',
      books: ['Light between oceans', 'Life of pi']
   }, {
      name: 'Ram',
      books: ['The Martian', 'Jonathan Livingston Seagull']
    }, {
      name: 'Krishna',
      books: ['Atlas Shrugged', 'The Fountainhead']
    }
];

var allBooks = customers.reduce(function(prev, curr) {
  return prev.concat(curr.books);
}, []);

var booksHtml = allBooks.reduce(function(prev, curr) {
  return prev + "<li>" + curr + "</li>";
}, "<ul>");

booksHtml += "</ul>"

document.getElementById("books").innerHTML = booksHtml;
```
[jsfiddle](https://jsfiddle.net/karthik1239/ndupn7nb/2/)

With this blog post, I conclude the series of blog posts on Reduce. 
In my next blog post, I will start a series of Arrays.map.
Reference:
[Documentation for reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce).
