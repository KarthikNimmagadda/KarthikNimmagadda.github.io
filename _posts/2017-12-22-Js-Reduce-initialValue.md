---
layout: post
title: Reduce method parameters
---
Reduce method takes two parameters. 
1. Callback Function: Function to apply on each element of the array.
2. InitialValue(optional): The callback functions first argument is called Accumulator.It is initialized using the optional initial value.If no initial value is provided the first element in the array is used as the first argument(Accumulator) of the call back function.

Example code to show when provided no initial value, accumulator value is the first element of the array.
```javascript
var fruits = ["banana", "mango"];
alert("Going into Reduce");
var fruitsNoApple = fruits.reduce(
  function (
    accumulator,
    currentValue
  ) {
  	alert("accumulator -> " + accumulator + "\ncurrentValue -> " + currentValue);
    return accumulator + " " + currentValue;
  }
);
alert("Fruits as string ->" + fruitsNoApple);
```
[jsfiddle](https://jsfiddle.net/karthik1239/ycm76t0r/8/)

Example code to show when provided an initial value, accumulator value is the value provided.

```javascript
var fruits = ["banana", "mango"];
var initialValue = "apple"
alert("Going into Reduce");
var fruitsWithApple = fruits.reduce(
  function (
    accumulator,
    currentValue
  ) {
  	alert("accumulator -> " + accumulator + "\ncurrentValue -> " + currentValue);
    return accumulator + " " + currentValue;
  }, initialValue
);
alert("Fruits as string ->" + fruitsWithApple);
```
[jsfiddle](https://jsfiddle.net/karthik1239/61p0nyv0/2/)

In my next post, I will provide callback functions parameters description.
Reference:
[Documentation for reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce).
