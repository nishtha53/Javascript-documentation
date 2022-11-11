---
sidebar_position: 4
---

## Short Circuiting (&& and ||)

- It basically means, terminating further evaluation of a statement because the condition proved to be false.

=> 3 things about OR operator: 

1.) It can take ANY data type. 

2.) It can return ANY data type. 

3.) Short Circuiting in OR operator: If first value is truthy value, it returns the first value and doesn't even evaluate second value. If both are falsy values, last value is returned. (Can't use for 0 as it is a falsy value)

## Example

```js
console.log(`-------------- OR ---------------`);
console.log(3 || 'A String'); // 3
console.log(0 || 'A String again'); // 'A String Again ==> Will return second value
console.log(null || undefined); // Both falsy, returns last value ==> undefined
console.log(3 || 0); // Returns 3 as it short circuited

console.log(null || undefined || 0 || '' || 46 || 'abc' || NaN); // 46 => truthy value => shortcircuit => 46

restaurant.numGuests = 0;
const guests1 = restaurant.numGuests ? restaurant.numGuests : 10;
console.log(guests1); // 10 

const guests2 = restaurant.numGuests || 15;
console.log(guests2); // 15

// If numGuest = 0, above condition doesn't work. Use nullish coalescing operator in that case.

const guests3 = restaurant.numGuests ?? 15; // Nullish Coalescing Operator
console.log(guests3); // 0

console.log(`----------- AND -----------`);
console.log(7 && 'ABC'); // ABC
console.log(0 && 'DEF'); // 0
console.log(7 && 'ABC' && null && 78); // null

// instead of multiple line function => single line can be used

if (restaurant.orderPizza) {
  restaurant.orderPizza('Tomato', 'cheese', 'Paneer');
}

restaurant.orderPizza &&
  restaurant.orderPizza('Black-Olives', 'Cheese', 'Red Paprika'); // called in single line -> checks if it exists and then calls. 
```

## Nullish Coalescing Operator

- In above example OR operator doesn’t work with 0 integer value or empty string, in such case Nullish Coalescing Operator is used. 

- For this operator, only **null and undefined** are **falsy values**, rest all are truthy values.

- Nullish Coalescing Operator is written as `??`.

**Example**

```js
restaurant.numGuests = 0;
const guests1 = restaurant.numGuests ? restaurant.numGuests : 10;
console.log(guests1); // 10 

const guestCorrect = restaurant.numGuests  ?? 10;
console.log(guestCorrect)  //0
```