---
sidebar_position: 1
---


## What is javascript objects?

- Object is used to store various keyed collections and more complex entities. Objects can be created using the Object() constructor or the object initializer / literal syntax.

## How to declare Objects?

```javascript
const object = {
    "name": "nistha",
    "age": 21,
}
```

## How to access object values?

- Object values can be access using (.) operator.
- Object values can be access using [] notation too.

Let's see example:

```javascript
const object = {
    "name": "nistha",
    "age": 21,
}
console.log(object);
console.log(object.name)  // to access name from object
console.log(object.age) //to access age from object
```

```
//output
nistha
21
```

```javascript

//using bracket notation
const object = {
    "name": "nistha",
    "age": 21,
}
console.log(object);
console.log(object['name'])  // to access name from object
console.log(object['age']) //to access age from object
```

**=> Big difference between dot operation and  bracket notation is we can write any expression we like, we no need to write explicitly in string here instead we can computed from some expression.**

Lets see example:

```javascript
const object = {
    "firstName": "nistha",
    "age": 21,
}
const nameKey = "Name";
console.log(object['first' + nameKey])

//output
nistha
```

## Object Literals

- If you need to add another object in a object, just write its name that is declared earlier and it will be included.

- For variables i.e. properties names, we can compute values: “ [`day-${2+3}`] “ => this will give variable name as day-5. Just use [   ].



## Looping objects: Object keys, values and Entries

- We can't use for of for direct looping because objects are not iterable.

- To print three property names we can use `Object.keys()`which gives array of key of objects.

- Using `Object.values` which gives array of values of object.

- Using `Object.entries` ( In arrays, object.entries it gives an array that says [index, element] ). —> Destructuring can be done in for of loop as well.


**Example**

```js

const weekdays = ['Mon', 'Tue', 'wed', 'Thurs', 'Fri','Sat', 'Sun'];

const openingHours = {
  [weekdays[3]]:{
    open:15,
    close:22,
  },
  [weekdays[4]]:{
    open:14,
    close:20,
  },
  [weekdays[5]]:{
    open:15,
    close:30,
  },
}
// Iterating objects

// 1. Using keys
const propertiesObject = Object.keys(openingHours);
console.log(propertiesObject); // Gives only key values from openingHours object

let openStr = `We are open on ${propertiesObject.length} ${
  propertiesObject.length > 1 ? 'days' : 'day'
}: `;
for (const ele of propertiesObject) openStr += `${ele}, `;
console.log(openStr);

// 2. Using values
const valuesObject = Object.values(openingHours);
console.log(valuesObject);

for (const { open, close } of valuesObject) console.log(open, close);

// 3. Entries
const entriesObject = Object.entries(openingHours);
console.log(entriesObject);
for (const [key, { open, close }] of entriesObject)
  console.log(`Timings for ${key} are ${open} : ${close}`);
```