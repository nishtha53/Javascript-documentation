---
sidebar_position: 4
---

## What is scoping?

- How our programs variable are organized and accessed. "Where do variables live?" or "Where we can access certail variables or where not?"


## What is lexical scoping?

- Scoping is controlled by where we exactly write our functions and code blocks.


## What is scope?

- Space or enviorment in which certain variables are declared. There is global scope, function scope and block scope.

## What is scope of variable?

- Region of our code where a certain variable can be accessed.


### Three types of Scope

1) Global Scope

2) Function Scope

3) Block Scope(ES6)

![scope](./scope.jpg)


<h1>Let's see details Example</h1>

**=> In this Example, const `myname ="jonas"` is Global Scope.
then function `first()` and `second()` is having their own function scope.
and under first function there is if condtion and varaibles `decade` is block scope where `var millenial = true` is function scope because block scope only works for `let` and `const`.**

![image](./detail%20example.jpg)


## Scope chain VS Call Stack

![diff](./diff.jpg)

## Summary of Scope chain

![summary](./summary.jpg)



