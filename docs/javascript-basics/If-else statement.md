---
sidebar_position: 4 

---

# If-else statement


## What is if-else statement

- If-else condition is used to check whether the statement executed is true or false.
- If statement execute is true then if condition will be executed if false then else statement will be executed.


**Syntax**

```
if(condition)
{
    statements //statement can be true
}
else
{
    statement //statement can be false
}
```

**Example**

```javascript

//checking age is eligible for driving or not.

const age = 18;

if(age>=18)
{
    console.log("Eligible for driving!");
}
else
{
    console.log(" Not eligible for driving!");
}

```

**Example**

```javascript

// //If your country's population is greater that 33 million, log a string like this to the
// console: 'Portugal's population is above average'. Otherwise, log a string like
// 'Portugal's population is 22 million below average' (the 22 is the average of 33
// minus the country's population)

var population = 33;

if(population <= 33)
{
  console.log("Portugal's population is above average");
}
else
{
  console.log("Portugal's population is below average");
}
```

## Switch Statement

- The switch statement executes a block of code depending on different cases. The switch statement is a part of JavaScript's "Conditional" Statements, which are used to perform different actions based on different conditions. Use switch to select one of many blocks of code to be executed.

**Example**

```javascript
const day = "Monday";

switch(day){
    case 'Monday':
        console.log("Work on project");
        break;
    case 'tuesday':
        console.log("Work on design");
        break;
    case 'wednesday':
    case 'thursday':
        console.log("Work on homework");
        break;
    case 'friday':
        console.log("Dinner party");
        break;
    default:
    console.log("Enter valid day");
}
```

## How to write Ternary Operator

- Ternary operator works same like If-else condition but it is shorten to write if-else condition.

```javascript
const age = 23;
age>= 18 ? console.log("I can drive") : console.log("I can't drive");
```

