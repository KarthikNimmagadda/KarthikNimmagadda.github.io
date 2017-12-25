---
layout: post
title: Javascript Reduce Method
---

The other day while I was browsing through a code review, a comment about using Array.prototype.reduce() caught my eye. The ease and simplicity of its usage blew me away. Reduce method can be used to apply a function to a collection and get a final value. Let us consider an example.
Let's say you have 4 bank accounts.

```javascript
var bankBalances = [100.9, 200.1, 300.0, 400.0];
```

The given array will only have the bank balances. Find the total money you have.

The following code finds the total sum using a for loop.

```javascript
var totalMoney = 0;
var bankBalances = [100.9, 200.1, 300.0, 400.0];
for (var i = 0; i < bankBalances.length; i++) {
	totalMoney += bankBalances[i];
}
alert("Amount of money you have: " + totalMoney);//1001
```

[jsfiddle](https://jsfiddle.net/karthik1239/gxy9h054/)

The same output can be attained using a reducer.

```javascript
var bankBalances = [100.9, 200.1, 300.0, 400.0];
var totalMoney = bankBalances.reduce(
function(accumulator, currentValue) {
	return accumulator + currentValue
});
alert("Amount of money you have: " + totalMoney);//1001
```

[jsfiddle](https://jsfiddle.net/karthik1239/u03s1aLr/)

The accumulator accumulates the total amount of money. The current element is the element being processed in the array.

In my next post, I will provide reduce methods parameters description.
Reference:
[Documentation for reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce).
