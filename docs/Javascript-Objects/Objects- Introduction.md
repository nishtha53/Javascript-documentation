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
