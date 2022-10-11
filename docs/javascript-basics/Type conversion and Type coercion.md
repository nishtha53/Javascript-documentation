---
sidebar_position: 5
---

## What is type conversion?

- JavaScript variables can be converted to a new variable and another data type.

=> If want to convert string to number then `Number()` in built-in function used.

Let's take example:

```javascript
const inputYear = "1991";
console.log(Number(inputYear));

// input year which is variable declared in string by using 
// Number() it converted to number datatype.

```

=> If want to convert number to string then `String()` in built-in function used.

Let's take example:

```javascript
const inputYear = 1991;
console.log(String(inputYear));

// input year which is variable declared in string by using 
// Number() it converted to number datatype.
```


## What is type coercion?

=> It will direct convert number to string.

Example:

```javascript

console.log("I am " + 21 + " Year old!!");
```




