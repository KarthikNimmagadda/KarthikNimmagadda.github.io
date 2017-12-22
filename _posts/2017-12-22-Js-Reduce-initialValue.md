---
layout: post
title: Reduce method parameters!
---

The callback functions first argument is called Accumulator.It is initialized using the optional initial value.If no initial value is provided the first element in the array is used as the first argument(Accumulator) of the call back function.

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