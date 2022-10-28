---
sidebar_position: 2
---

Object methods:

```javascript
const details = {
    "firstName" : "nishtha",
    "lastName" : "thakkar",
    "age" : 21,
    "birthyear" : 2002,
    "study" :"MCA",

    calcAge(birthyear){
		return 2037 - birthyear;
	}
}

console.log(person.calcAge(1991));  // 46
```

##  this keyword

- In JavaScript, the this keyword refers to an object. Which object depends on how this is being invoked (used or called).

- Special varibale that is created for every execution context. Takes the vale from owner of the function in which `this` keyword is used.

- Value of `this` keyword is not static. Its depend on how function is called, and its value only assigned when the function is actually called.

![this](../JavaScript-Behind%20the%20Scenes/this.jpg)


```javascript
const details = {
    "firstName" : "nishtha",
    "lastName" : "thakkar",
    "age" : 21,
    "birthyear" : 2002,
    "study" :"MCA",

   fullName : function() {
  return this.firstName + " " + this.lastName;
}
}
console.log(details.fullName());

//output
nishtha thakkar
```

## Adding key values to object

```javascript
const details = {
    "firstName" : "nishtha",
    "lastName" : "thakkar",
    "age" : 21,
    "birthyear" : 2002,
    "study" :"MCA",  
}

details.location = "India"
console.log(details);

//output
Location added to object.
```


