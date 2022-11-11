---
sidebar_position: 5
---

- Logical OR Assignment operator ( ||= ) : Assigns value if its a falsy value.

- Logical nullish assignment operator ( ??= ) : Assigns value if its a falsy value. For nullish, falsy values: null and undefined.

- Logical AND assigment operator( &&= ): Assigns a value if it is truthy. 



**Example**


```js
const rest1 = {
  name: 'Capri',
  numGuests: 0,
};

const rest2 = {
  name: 'La Piazza',
  owner: 'Giovanni Rossi',
};

rest2.numGuests = rest2.numGuests || 10; 
console.log(rest2)  //// numGuests value 10 added to object rest2

rest1.numGuests = rest1.numGuests || 10;
console.log(rest1)  // rest1 numGuests value remains same

// with logical operator
rest2.numGuests ||= 10;
console.log(rest2)  // numGuests value 10 added to object rest2

rest1.numGuests ||= 30;
console.log(rest1) // rest1 numGuests value remains same

// nullish arguments

rest2.numGuests ??= 10; // Same as rest2.numGuests = rest2.numGuests ?? 10;
rest1.numGuests ??= 30; // // Same as rest2.numGuests = rest2.numGuests ?? 30;
console.log(rest2.numGuests);
console.log(rest1.numGuests);

// AND logical assigment operator
// rest2.owner = rest2.owner && 'Anonymous';
// rest1.owner = rest1.owner && 'Anonymous';
rest2.owner &&= 'Anonymous'; // Same as above
rest1.owner &&= 'Anonymous';
console.log(rest1);
console.log(rest2);
```


