---
sidebar_position: 7
---

## What is sets in JavaScript;
- Sets is a collection of new values. Duplicate are already deleted.

- Set are iterable. That means, we can use for.. of and spread/rest operators.

- Orders are irrelevant as we can’t retrieve any element.

- Can be declared using new Set( )

- Spread operator can be used to convert it into array. [...new Set(set-name)].

## Methods in sets

- .has('element-name') => finds if element is present.

- .add('element-name') => adds element

- .delete => deletes element.

- .clear( ) => clears the set. Makes it blank, deletes the data inside.

- .size => tells no. of elements.

## Example

```js
// SETS Data Structure
const orderSet = new Set([
  'Pasta',
  'Pizza',
  'Pizza',
  'Risotto',
  'Pasta',
  'Pizza',
]);
console.log(orderSet); // ['Pasta', 'Pizza', 'Risotto']
console.log(orderSet.size); // 3
console.log(orderSet.has('Pizza')); // true
console.log(orderSet.has('Bread')); // false
orderSet.add('Garlic Bread'); // false
console.log(orderSet.add('Garlic Bread'));
orderSet.delete('Pizza');
console.log(orderSet);
console.log(new Set('Jagrut Sharma')); // Splits the string ['J', 'A', 'G', 'R', 'U', 'T', 'S', 'H', 'M']

for (const ele of orderSet) console.log(ele);
console.log(orderSet[0]);

const staff = ['waiter', 'chef', 'manager', 'waiter', 'chef', 'waiter'];
console.log(staff);
// const uniqueStaff = new Set(staff);
const uniqueStaff = [...new Set(staff)];
console.log(uniqueStaff); // ['waiter', 'chef', 'manager']
console.log(new Set(staff).size);
 
// orderSet.clear()
// console.log(orderSet);
```