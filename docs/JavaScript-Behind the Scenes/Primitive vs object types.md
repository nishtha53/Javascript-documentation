---
sidebar_position: 7
---

- Primitive values can be stored in variables directly. Objects, on the other hand, are stored as references. A variable that has been assigned an object does not store that object directly, it stores the memory address of the location that the object exists at.

Example:

```javascript
const me = {
  name: 'Jonas',
  age: 30,
};
const friend = me;
friend.age = 27;
console.log('Friend:', friend);
console.log('Me', me);
```
**=> In above example for object me age value assigns to 27 and friend name object is also created and age value is 27.**