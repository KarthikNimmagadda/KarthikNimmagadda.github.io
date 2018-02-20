---
layout: post
title: Javascript Map Method
---
Map method can be used to apply a function to a collection and return a new array. Let us consider an example.
Let's say you have four credit card accounts and all your banks want to double the credit limit because of your excellent credit score. Let's see how this can be achieved.

```javascript
var creditLimits = [100.9, 200.1, 300.0, 400.0];
```
The given array will have all the credit limits. The idea here is to double each limit and create a new array out of it.

The following code does it.

```javascript
var creditLimits = [100.9, 200.1, 300.0, 400.0];
var newCreditLimits = [];
for (var i = 0; i < creditLimits.length; i++) {
    newCreditLimits[i] = creditLimits[i]*2;
}
alert("Array with old credit limits: " + creditLimits);
alert("Array with doubled credit limits: " + newCreditLimits);
```

[jsfiddle](https://jsfiddle.net/karthik1239/69p4bvk7/12/)

The same output can be attained using a map.

```javascript
var creditLimits = [100.9, 200.1, 300.0, 400.0];
var newCreditLimits = creditLimits.map(
function(creditLimit) {
    return creditLimit * 2;
});
alert("Array with old credit limits: " + creditLimits);
alert("Array with doubled credit limits: " + newCreditLimits);
```
[jsfiddle](https://jsfiddle.net/karthik1239/L4fat8qd/5/)

The array "newCreditLimits" will contain double the amount of credit limits. 'creditLimit' is the current element in the collection.

In my next post, I will provide map methods parameters description.
Reference:
[Documentation for map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map).
