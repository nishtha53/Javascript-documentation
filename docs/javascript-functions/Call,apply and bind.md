---
sidebar_position: 3
---

## Call()

- Since functions are objects in JS and objects have methods so functions can also have methods. These methods are .name, .call( ), .apply( ), .bind( )

- These methods are used to point this towards the desired direction rather than what it would originally point at.

- The call() method calls the function with a given this value and allows passing in arguments one by one separating them with commas.

**Syntax:**

`functionName.call(’position for this to point’, argument1. argument2, …….)`

## Apply()

- It is similar to call method. Only difference is that here, values/parameters are passed in an array. 

- Due to introduction of spread operator, it isn’t used much. It also calls the function.

**Syntax:**

`functionName.apply(’position for this to point’, [argument1. argument2, …….])`


## bind()

- The bind() method returns a new function and allows passing in a this array and any number of arguments.



**Syntax:**

`const varName = functionName.bind('position to pint this at')`




## Example:
```js
//call method
let p1 = {
  firstName: 'John',
  lastName: 'Smith'
};
let p2 = {
  firstName: 'Ann',
  lastName: 'Brown'
};
function sayWelcome(greeting) {
  console.log(greeting + ' ' + this.firstName + ' ' + this.lastName);
}
sayWelcome.call(p1, 'Welcome'); // Welcome John Smith
sayWelcome.call(p2, 'Welcome'); // Welcome Ann Brown

//apply method

let p1 = {
  firstName: 'John',
  lastName: 'Smith'
};
let p2 = {
  firstName: 'Ann',
  lastName: 'Brown'
};
function sayWelcome(greeting) {
  console.log(greeting + ' ' + this.firstName + ' ' + this.lastName);
}
sayWelcome.apply(p1, ['Welcome']); // Welcome John Smith
sayWelcome.apply(p2, ['Welcome']); // Welcome Ann Brown

//bind method

let p1 = {
  firstName: 'John',
  lastName: 'Smith'
};
let p2 = {
  firstName: 'Ann',
  lastName: 'Brown'
};
function sayWelcome() {
  console.log('Welcome ' + this.firstName + ' ' + this.lastName);
}
let sayWelcomeJohn = sayWelcome.bind(p1);
let sayWelcomeAnn = sayWelcome.bind(p2);
sayWelcomeJohn(); // Welcome John Smith
sayWelcomeAnn(); // Welcome Ann Brown
```