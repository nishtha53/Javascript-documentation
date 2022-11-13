---
sidebar_position: 8
---

- Maps are more useful than sets. Map is a data structure that is used to map values to the keys.

- Just like object, data in “key: value” type, where key is of string type ⇒ In maps, key can be of any data type. Key can be even objects, arrays and other maps data.

- This assigining value through new keyword is called as constructor.

- Easiest way to create is through const varName = new map( ); and then set properties through var_name.set('Key',  'value'). Key can also be boolean value i.e. true or false.

- var_name.set( ) returns value and hence can be used in series.

- To acquire value var_name.get('key') is used.

- .has('key'), .delete('key'), .clear( ), .size methods are also used.

- We can even use an array and object(even DOM objects) as a key. This helps us in some very advanced functionality.

- For setting value in single line: Arrays inside arrays in which 1st is key, 2nd is value. new Map([ ['key', 'value'], ['key-1', 'value-1'], ['key-2', 'value-2'], ['key-3', 'value-3'],  ])

- We can use spread operator for printing arrays from maps. “Object.keys, Object.values“ exist and can be used.

```js
// MAPS Data structure

const rest = new Map();
rest.set('hello', 'world');
console.log(rest);
console.log(rest.set('name', 'Classico Italiano')); // It returns value will print the set
rest.set(1, 'Bangalore, India');
rest.set(2, 'Hyderabad, India');
rest
  .set('categories:', ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'])
  .set('open', 11)
  .set('close', 23)
  .set(true, 'We are open :)')
  .set(false, 'We are closed :(');

console.log(rest);

console.log(rest.get('hello'));
console.log(rest.get('name')); // Classico Italiano
console.log(rest.get(1)); // 'Bangalore, India'
console.log(rest.get(true)); // 'We are open'
console.log(rest.get('true')); // SHows value only for boolean and not 'true' will return undefined

// This true and false can be useful a lot of times
// const currTime = 8;
const currTime = 12;
console.log(
  rest.get(currTime >= rest.get('open') && currTime <= rest.get('close'))
);

// Methods available
console.log(rest.has('categories:')); // true
console.log(rest.delete(2)); // Deletes the key with value 2
console.log(rest);
console.log(rest.size); // We have 8 keys
// rest.clear();
// console.log(rest);
// rest.set([1, 2], "Where's the food");
const arr = [1, 2];
rest.set(arr, "Where's the food");
console.log(rest);
console.log(rest.get([1, 2])); // Gives undefined because of reference type. Does not refer to same memory location
console.log(rest.get(arr)); // For getting same you need to define a variable, that way we will refer to the object at the same memory location

rest.set(document.querySelector('h1'), 'This is a heading'); // Can even be used to select a DOM element
console.log(rest);
```
