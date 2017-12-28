---
layout: post
title: Reduce example travel time
---
Purpose of this blog post is to provide an example to show how to use reduce method with an array of objects.

Last week I had an urge to note down the time taken for me to travel to the office.  As an engineer, I always had this call to optimize stuff. The more I measure it became apparent to me that I am spending more time in commute. Maybe I have to move closer to the office.

In this example, I will reduce an array of times to total time and finally find the average time taken for the commute.

```javascript
var timesOfTravel = [{
        "day": "Monday",
        "time": 20
    },
    {
        "day": "Tuesday",
        "time": 21
    },
    {
        "day": "Wednesday",
        "time": 22
    }
];
var totalTime = timesOfTravel.reduce(function(a, b) {
    return a + b.time;
}, 0);
alert("Total time spent traveling: " + totalTime);
alert("Average time spent on road: " + totalTime / 3);
```
[jsfiddle](https://jsfiddle.net/karthik1239/vLkuk8um/4/)

In my next post, I will provide another way of using reduce method.
Reference:
[Documentation for reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce).
