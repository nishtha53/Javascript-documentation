---
sidebar_position: 2
---

## What is Arrow Function?

- Arrow function was introduced in ES6 conepts.
- It gets shorter! If the function has only one statement, and the statement returns a value, you can remove the brackets and the return keyword.


**Example:**

```javascript
const hello = sayHello =>{
    console.log("hello world!");
}
hello();
```

## Regular functions v/s Arrow functions.

- In regular function, this changes according to the way that function is invoked whereas Arrow functions don't have their own “this”, and they don’t redefine the value of “this ”within the function.

**Let's understand with an example:**

```javascript
const details = {
    firstName : 'nishtha',
    year : 2002,

    calcAge : function(){
        console.log(this);
        console.log(2022 - this.year);
    },

    greet: () => console.log(`hey ${this.firstName}`),
};
details.greet();
```

**//output**

=> Shows hey undefined because as said arrow functions can't be accessed any value using `this` keyword.

## Example:

```javascript
var firstName = 'Matilda';
const jonas = {
  firstName: 'Jonas',
  year: 1991,
  calcAge: function () {
    // console.log(this);
    console.log(2037 - this.year);
    
    const isMillenial = function(){
        console.log(this);
        console.log(this.year >= 1981 && this.year <= 1996);
    };
    isMillenial();
  },
  greet: () => {
    console.log(this);
    console.log(`Hey ${this.firstName}`);
  },
};
jonas.greet();
jonas.calcAge();
```
=> Above example shows year as undefined because there is clear rule that in regular function call. this keyword will be under regular function will give undefined.

Two solutions for this to solve this problem.

<h4>Solution 1 </h4>

```javascript
var firstName = 'Matilda';
const jonas = {
  firstName: 'Jonas',
  year: 1991,
  calcAge: function () {
    // console.log(this);
    console.log(2037 - this.year);
    
    const self = this;
    const isMillenial = function(){
        console.log(self);
        console.log(self.year >= 1981 && self.year <= 1996);
    };
    isMillenial();
  },
  greet: () => {
    console.log(this);
    console.log(`Hey ${this.firstName}`);
  },
};
jonas.greet();
jonas.calcAge();
```

```
\\output
46
(4) {firstName: "Jonas", year: 1991, cal...}
true
```

=> Solution one was just created one variable as self and assign value self to this and in console instead of this used self everywhere and result is  true. 

<h4> Solution 2 </h4>

```javascript
var firstName = 'Matilda';
const jonas = {
  firstName: 'Jonas',
  year: 1991,
  calcAge: function () {
    // console.log(this);
    console.log(2037 - this.year);
    
  const isMillenial = () => {
      console.log(this);
      console.log(this.year >= 1981 && this.year <= 1996);
    };
    isMillenial();
  greet: () => {
    console.log(this);
    console.log(`Hey ${this.firstName}`);
  },
};
jonas.greet();
jonas.calcAge();
```

```
\\output
46
(4) {firstName: "Jonas", year: 1991, cal...}
true
```

=> Solution 2 was to use arrow function ans access the year which results true.


