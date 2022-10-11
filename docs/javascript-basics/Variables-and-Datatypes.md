---
sidebar_position: 1
---

##  Variable and Datatypes

- In simple language, variables is used to store some data.
- Variables can store number, character, array, string, boolean.
- And data type is a type what kind of date is stored. Value which is assign to a variable is a which kind of data type.


## Some rules of declaring variable

- Variable can't be start from number.
- Reserved keywords of JavaScript can't be used for variable name.
-  ' _ ' and ' $ ' is only allowed as special character for declaring varibale.
- While creating varibale is it good practice to follow camel case i.e firstName.

=> Variables can be used with var let and const.

## Let's see  examples of declaring a variable

```javascript
/* Problem statement: Declare variables called 
'country', 'continent' and 'population' and 
assign their values according to your own country 
Log their values to the console */

//Varibles are declared and value is assigned.
var country = "India";
var continent = "Asia";
var population = "138 crores";

// console the values of country,continent and population.
console.log(country);
console.log(continent);
console.log(population);
```

Output: 
```
India
Asia
138 crores
```

## Now let's understand what is data type?

- Data types describe the different types or kinds of data that we’re gonna be working with and storing in variables. 

=>  Primitive kind of data types are as follow:

- String 
- Boolean
- Undefined
- Null
- Symbol
- Number
- BigInt

Let's see each data type with small example.

1) **String**

- Sequence of characters.

```javascript
let firstName = "Nishtha";
console.log(typeof(firstName));   //string
```

2) **Boolean**

- Boolean will only take two values either true or false.

```javascript
let isFemale = true;
console.log(typeof(isFemale));   //boolean
```
3) **Undefined**

- Value taken by variable is not yet defined. (Empty value)

```javascript
let children;
console.log(typeof(children));  //undefined
```
4) **Null**

- Also means empty value.

```javascript
let a = null;
console.log(typeof(a));   //object but it will define as null
```

5) **Symbol**

- Symbol is introduced in ES2015.
- It is not so usefull but value which is unique and cannot be changed.

6) **Number**

- Floating point number which is used for decimals and integers

```javascript
let age = 21;
console.log(typeof(age));    //number
```

7) **BigInt**

- In ES2020, one more data type is introduced that is "BigInt" which means it holds larger integers than Number data type holds.


=> JavaScript has dynamic typing, We dont have to manually define the data type of the value stored in variable. Instead, data type are determined automatically.

## Let's see  examples of Variable and datatypes.

```javascript
/* Problem statement: Declare a variable called 'isIsland' and set its value according to 
your country. The variable should hold a Boolean value. Also declare a variable
'language', but don't assign it any value yet. Log the types of 'isIsland', 
'population', 'country' and 'language' to the console */

//Varibles are declared and value is assigned.
let isIsland = true;
let language;
let country = "India";

// console the type of datatypecountry,continent and population.
console.log(typeof(isIsland));
console.log(typeof(language));
console.log(typeof(country));
```

Output

```
boolean
object
string
```

## Let's understand difference between var,let and const

- First there was only 'var' to declare varibale whereas in ES6 let and const is introduced.

**Difference between var,let and const**

=> var

- With “var” there are only two types of scope for a variable.There is global scope which is where we would place a variable if we define the variable with “var” outside of any function. And then there is function scope for variable defined inside of a function. But there is no block scope and this is a source of confusion and occasional bugs.

- Because variable declarations (and declarations in general) are processed before any code is executed, declaring a variable anywhere in the code is equivalent to declaring it at the top. This also means that a variable can appear to be used before it’s declared. This behavior is called “hoisting”, as it appears that the variable declaration is moved to the top of the function or global code.

=> let
- let allows us to define variables.Previously we declare our variables using “var” keyword. But it has some limitations when it comes to scope as it does not offer block scope.But now using “let” keyword we can declare truly block-scoped variables.

- Hosting is not allowed.

- let can reassign the value but redecalration of variable can be done using let.

- let is mutuable it means the variable only can be just declared but value is not assign and it won't give any error.

=> const

- “ const” keyword to create and initialize a read-only variable that will hold a constant value and something that we can never change. In ES6 “const” will have block scoping just like the “let” keyword. The value of a constant cannot change through re-assignment, and it can’t be redeclared. A constant cannot share its name with a function or a variable in the same scope.

**Which is best practice to declare varibale**

- If you are pretty sure that value is fixed of variable it is best practice to use const.
- And if need to change value then you can use let.










