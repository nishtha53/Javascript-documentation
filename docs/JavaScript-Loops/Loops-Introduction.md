---
sidebar_position: 1
---

## What are loops?

- Loops are handy, if you want to run the same code over and over again, each time with a different value.

## Syntax

```javascript
for (initialExpression; condition; updateExpression) {
    // for loop body
}

// The initialExpression initializes and/or declares variables and executes only once.
// The condition is evaluated.
// If the condition is false, the for loop is terminated.
// If the condition is true, the block of code inside of the for loop is executed.
// The updateExpression updates the value of initialExpression when the condition is true.
// The condition is evaluated again. This process continues until the condition is false.
```

## Example

```javascript
for(i=1 ; i<=10;i++)
{
    console.log("Hello World!");
}

/*i value will be initialized with 1  and in second expression 
it is given i will be go to 10 so I i is 1 and i<10 
then print hello world then i++ means i value 
will be 2 as 2<10 again it will print hello world 
same thing will go till i value will be 10 once
 I value will be 11 loop will be terminated 
 and execution stops. */
```

**Example**

```javascript
const details = {
    "firstName" : "nishtha",
    "lastName" : "thakkar",
    "age" : 21,
    "birthyear" : 2002,
    "study" :"MCA",
}

for (let i=0; i<details.length ;i++)
{
    console.log(details[i]);
}
```

## Continue and Break

**Continue:** skips the current iteration of the loop and continuously starts the next one.

**break:** completely terminates the whole loop.


