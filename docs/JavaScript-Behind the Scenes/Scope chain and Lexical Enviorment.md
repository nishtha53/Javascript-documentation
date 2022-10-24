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


## Example:


```Javascript
'use strict';

function calcAge(birthyear)
{
    const age = 2022 - birthyear;

    function printAge()
    {
        const output = `your age is ${age}, Born in ${birthyear}`
        console.log(output)
    }
    printAge();

    return age;
}

const firstName = "Nishtha";
console.log(firstName);
calcAge(2002);

//output
Nishtha
your age is 20, Born in 2002
```

In above example `firtName` variable is global scope so it is printed first and then `calcAge` function is called execution will go to function scope and calculate age and then `printAge` function will printed and ouput varibale will be printed.


## Scope chain VS Call Stack

![diff](./diff.jpg)

## Summary of Scope chain

![summary](./summary.jpg)



