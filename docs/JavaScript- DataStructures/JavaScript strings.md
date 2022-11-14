---
sidebar_position: 9
---

## Meaning of JavaScript Strings

- JavaScript strings are for storing and manipulating text.

- Strings are useful for holding data that can be represented in text form. Some of the most-used operations on strings are to check their length, to build and concatenate them using the + and += string operators, checking for the existence or location of substrings with the indexOf() method, or extracting substrings with the substring() method.



## Methods of JavaScript

### 1) Indexof

- The indexOf string method in javascript is used to get the index of the first occurrence of a specified value in a string.

- If the character or substring is not present then it returns -1. The search string is case-sensitive.

### 2) Slice method

- The slice string method in javascript extracts a part of the string and returns it as a new string.

### 3) charAt method

- The charAt() string method in javascript returns a character at the specific index of the given string.

### 4) charCodeAt method

- The charCodeAt string method in javascript returns the Unicode value (between 0 and 65535) of the character present at the given index of the string. Example Unicode value of 'A' is 65.

- The charCodeAt() method takes an index as an argument and returns the Unicode value of the character present at that index value.

### 5) concat method

- The concat string method in javascript concatenates the passed string in the method to the calling string and returns the concatenated string as a new string.

- The concat() method can take any number of strings as an argument.

- If the passed argument is not a string then it converts the argument to string and then concatenates it.


### 6) endWith method

- The endsWith string method in javascript is used to determines whether the string ends with a specified substring or not.

- If it ends with a specified string then it returns true, else returns false.

- The substring to be checked for the ending is passed as the first argument in the method.


### 7) includes

- The includes string method in javascript is used determines whether a given substring is present in the calling string or not.

- If the string is present then the method returns true, if not substring is not present then the method returns false.

- The matching of includes() method for the string is case-sensitive.

### 8) lastIndexOf method

- The lastIndexOf() string method in javascript searches the last occurrence of a substring within a string. The method starts searching from the end of the string for efficiency.

- If the substring is not in the given string then it returns -1.


### 9) replace method

- The replace method selects one or all matches from a string and replace it with a replacement string and return it as new string.

- To find the match method use string or regular expression. When a string is passed as an argument then it select only the first match while when a regular expression is passed then it selects all the matches.


### 10) search method

- The search string method in javascript is used to determine whether a pattern exists within the calling string or not, if it exists then the method returns the index value of the first match within the string.

- The search method uses regex to search for a pattern in a string, if a string is passed to search for then the method implicitly convert it to regex.



###  11) split method

- The split string method in javascript divides the given string intro substring and returns an array of substrings.

- The method takes an argument which is a pattern to be used for dividing the string.

- f the pattern is an empty string ('') then the method split the string at each character.

- If the pattern is a string (' ') then the method split the string at each space
If the pattern can be a regular expression. '\n' splits the string at each new line
The limit defines the maximum number of substrings to be returned. If it is 0 then an empty array ([]) is returned.



### 12) substr method

- The substr() string method in javascript is used to extract a substring from a string. It returns a part of the string, starting at a specific index and ending after a given number of characters.

- `startIndex` - It specifies the index value from where the substring starts

- `length` - It defines number of characters to be extracted

### 13) substring method

- The substring() method extracts a part of string between 2 given index values. It returns a part of the string, starting at a specific index and ending after a given number of characters.

```js
str.substring(startIndex, endIndex)
```

- `startIndex` - It specifies the index value from where the substring starts

- `endIndex` - It specifies the index value from where the substring ends

- If endIndex is not specified then it is treated as the last character of the string.

- If the value of startIndex is greater than the value of endIndex then value of these two variables is swapped.



### 14) toLowerCase() method

- The toLowerCase() string method in javascript converts the case of a string to lowercase and returns it as a new string.



### 15) toUpperCase() method

- The toUpperCase string method in javascript returns a new string by converting the calling string to uppercase.



### 16) toString method

- The toString() string method in javascript returns a string representing the specified object.

- This method also convert numbers to strings in a different number system. For example you can convert a number to a string in binary system by using toString(2), octal system by using toString(8) and hexadecimal system by using toString(16), etc.


### 17) trim method

- The trim() string method in javascript removes whitespaces from both ends of the string. Whitespaces are space, tabs, newline, etc.

### 18) valueOf method

- The valueOf() string method in javascript returns the primitive value of a String object.



## Example
```js

const airline = 'King Fisher Airlines';
const plane = 'A320';

console.log(plane[0]); // A
console.log(plane[1]); // 3
console.log(plane[2]); // 2
console.log('A316'[3]); // Can be used durectly in string as well. // 6

console.log(`Length: ${airline.length}`); // 20
console.log(`Length: ${'A316'.length}`); // Can be used durectly in string as well. // 20
console.log(airline.indexOf('i')); // 1
console.log(airline.lastIndexOf('i')); // 16
console.log(airline.indexOf('Airlines')); // Will give inex of first element which is 'A' here, if not present returns -1 // 12
console.log(airline.slice(5)); // Returns string from 5th index element, includes 5th element. // Fisher Airlines
console.log(airline.slice(5, 11)); // First included, last not included // Fisher 

console.log(airline.slice(0, airline.indexOf(' '))); // As last not included // King
console.log(airline.slice(airline.indexOf(' ') + 1)); // As first is included, we don't need space to be included // Fisher Airlines

console.log(airline.slice(-5)); // Counts from last. // lines
console.log(airline.slice(0, -1)); // King Fisher Airline

const checkMiddleSeat = function (seat) {
  // B and E are middle seats
  seat = seat.slice(-1);
  seat === 'B' || seat === 'E'
    ? console.log('Sorry, you got a middle seat')
    : console.log('You are lucky');
};

checkMiddleSeat('13A');
checkMiddleSeat('13B');
checkMiddleSeat('23C');
```