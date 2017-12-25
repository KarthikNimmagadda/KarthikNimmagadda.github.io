---
layout: post
title: Reduce method callback parameters
---
This post explains the four parameters of reduce method callback function. The call back function is applied to each element in the array.
The callback function takes in 4 parameters.
    1. accumulator - The value accumulated so far. In other words, it is callback functions return value during the prior invocation.It is initialized using the optional initialValue as discussed in the previous post. 
If no initial value is provided the first element in the array is used as the accumulator.
   2. currentValue - The current value of the array element.
   3. currentIndex - The current index of the array element.
  4. array - Array on which reduce method is applied.
CurrenctValue and currentIndex are optional parameters.

Let's say reincarnation is real. These are my last five incarnations Horse, Ulysses Butterfly, Monkey, Ant, and NeedleFish. Let's assume because of the excellent Karma in those past lives I am "reduced" to human.

```javascript
var lifes = ["Horse", "Ulysses Butterfly", "Monkey", "Ant","NeedleFish"];
alert("Going into Reduce");
var currentLife = lifes.reduce(
  function (
    accumulator,
    currentValue, 
    currentIndex, 
    array
  ) {
  	alert("life " + currentIndex + " -> " + 		array[currentIndex] + "\ncurrentValue -> " + currentValue  + "\ncurrentIndex -> " + currentIndex + " \nAccumulated Karma so far " + accumulator );

    return accumulator + " " + currentValue.charAt(0);
  }, ""
);
alert("Current Life -> " + currentLife);
```
[jsfiddle](https://jsfiddle.net/karthik1239/mmsvL5o5/22/)

In my next post, I will provide more examples of using reduce method.
Reference:
[Documentation for reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce).

