---
sidebar_position: 2
---

# Basic Operators

- Operator means to perfom some operations between two values.


1) **Arithmetic operator**

- Arithmetic operator are as follows:

<table >
  <tr>
        <th>Operator</th>
        <th>Meaning</th>
  </tr>
  <tr>
      <td>+</td>
      <td>Addition</td>
  </tr>
    <tr>
      <td>-</td>
      <td>Subtraction</td>
  </tr>
    <tr>
      <td>*</td>
      <td>Multiplication</td>
  </tr>
    <tr>
      <td>**</td>
      <td>Exponentiation </td>
  </tr>
    <tr>
      <td>/</td>
      <td>Division</td>
  </tr>
    <tr>
      <td>%</td>
      <td>Mdulas</td>
  </tr>
    <tr>
      <td>++</td>
      <td>Increment</td>
  </tr>
    <tr>
      <td>--</td>
      <td>Decrement</td>
  </tr>
</table>

**Example :**

```javascript
const age = 2037;
const ageNishtha = age - 2019;
console.log(ageNishtha);

console.log(ageNishtha *2 / 10, 2 ** 3);

const firstName = "Nishtha";
const lastName = "Thakkar";
console.log(firstName + '   ' +lastName);

let a = 10;
a++;
console.log(a);
a--;
console.log(a);
```

2) **Assignment operator**

<table >
  <tr>
        <th>Operator</th>
        <th>Meaning</th>
  </tr>
  <tr>
      <td>=</td>
      <td>x=y</td>
  </tr>
    <tr>
      <td>+=</td>
      <td>x=x+y</td>
  </tr>
    <tr>
      <td>-=</td>
      <td>x=x-y</td>
  </tr>
    <tr>
      <td>*=</td>
      <td>x=x*y </td>
  </tr>
    <tr>
      <td>/=</td>
      <td>x=x/y</td>
  </tr>
    <tr>
      <td>%</td>
      <td>x=x%y</td>
  </tr>
</table>

**Example :**

```javascript
let b=5;
b+=5;
console.log(b);

let b=5;
b-=4;
console.log(b);

let b=5;
b*=4;
console.log(b);

let b=20;
b/=4;
console.log(b);

let b=20;
b%=4;
console.log(b);
```

3)**Comparison operator**

| Operator      | Meaning |
| ----------- | ----------- |
| <      | Less than       |
| >   | Greater than        |
| >=   | Greater than  or equal      |
| !=   | Not equal to      |
| ==   | Returns true if the operands are equal.   |
| ===   | Returns true if the operands and data type are equal.      |


**Example:**

```javascript
let c = 12;
let d = 14;
console.log(c>d);  //false

let c = 12;
let d = 14;
console.log(c<d);  //false

let c = 12;
let d = 12;
console.log(c<=d);   //true

let c = 12;
let d = 12;
console.log(c>=d);   //true

let c = 12;
let d = 14;
console.log(c!=d);  //true
```

## Equality Operator (== and ===)

- The main difference between the == and === operator in javascript is that the == operator does the type conversion of the operands before comparison, whereas the === operator compares the values as well as the data types of the operands.


## Boolean Logic(And Or and NOT operators)

**1) AND operator:**

- If there is two statement, if both of them are correct then it will print true otherwise else condition will be executed.

```javascript
const haveDrivingLicence = true;
const hadGoodVision = true;

console.log(haveDrivingLicence && hadGoodVision);   //true
```


**2) OR operator:**

- If there is two statement, if one of them are correct then it will print true otherwise else condition will be executed.
- Atleast one statement should be true for printing true statement.

```javascript
const haveDrivingLicence = true;
const hadGoodVision = true;

console.log(haveDrivingLicence || hadGoodVision);    // true
```

**3) NOT operator:**

- If there is two statement, if both of them are correct then it will print true otherwise else condition will be executed.
-  If there is two statement, if both of them are incorrect then it will print true otherwise else condition will be executed.

```javascript
const haveDrivingLicence = true;
const hadGoodVision = true;

console.log(!haveDrivingLicence);    // false
```











