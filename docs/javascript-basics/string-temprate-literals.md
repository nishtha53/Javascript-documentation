---
sidebar_position: 3
---

# String and Temprate Literals



## String

- String is used to add multiple line and concatenate two strings number 

**Example:**

```javascript

const firstName = "Nishtha";
const lastName = "Thakkar";
const birthDate = 05/03/2002;

console.log("My first name is " + firstName + " and last name is " + lastName);
```

## Template Literals(New concept of ES6)

- Template literals are indicated with backtick (`) and we can add multiple strings.

###  Parameters

**String text :**

- The string text that will become part of the template literal. Almost all characters are allowed literally, including line breaks and other whitespace characters. However, invalid escape sequences will cause a syntax error, unless a tag function is used.

**Expression :**

- An expression to be inserted in the current position, whose value is converted to a string or passed to tagFunction.


**TagFunction**

- If specified, it will be called with the template strings array and substitution expressions, and the return value becomes the value of the template literal. See tagged templates.

**Example:**

```javascript

const firstName = "Nishtha";
const lastName = "Thakkar";
const birthDate = 05/03/2002;

console.log("My first name is " + `${firstName}` + " and last name is " + `${lastName}`);
```


