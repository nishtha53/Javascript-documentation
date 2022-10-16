---
sidebar_position: 1
---


## Let's understand what is array?

- In simple words, array is collection of data with similar data type.
- An array can hold many values under a single name, and you can access the values by referring to an index number.

## Example

```javascript
const cars = ["Saab", "Volvo", "BMW"];
console.log(cars);
```

**Also we can create array using new keyword**

```javascript
const cars = new Array('Saab', 'Volvo', 'BMW');
console.log(cars);
```

## How to access single element from array?

- Array elements are access by it's index number. Index number start with 0.
- To access last element of array we need to do ``n-1``.

```javascript
const cars = new Array('Saab', 'Volvo', 'BMW');
console.log(cars[0]);
console.log(cars[1]);
console.log(cars[2]);

//output
Saab
Volvo
BMW
```

## How to change element of array?

- Value can be changes by its index number.

```javascript
const cars = ["Saab", "Volvo", "BMW"];
car[2] =  "Gets";
console.log(cars);

//new array
["Saab", "Volvo", "Gets"]
```