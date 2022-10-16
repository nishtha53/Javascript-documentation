---
sidebar_position: 2
---

## Let's see some inbuilt JaaScript methods:

**1. Array Length Method**

=> Array Length method used to find length of array elements by this method we can know what is length of array.

Lets understand with good example:

```javascript
 var animals = ["dog" , "cat" , "elephant" , "cow" , "gorilla"];
 console.log(animals.length);

 //output
 5
 ```

 **2. Array toString() Method**

=> Array toString() method converts array to string

Lets understand with good example:

```javascript
 var animals = ["dog" , "cat" , "elephant" , "cow" , "gorilla"];
 console.log(animals.toString());

 //output
 dog,cat,elephant,cow,gorilla
```

**3. Array join() Method**

=> Array join() method converts array to string , but only change is we can add separator.

Lets understand with good example:

```javascript
 var animals = ["dog" , "cat" , "elephant" , "cow" , "gorilla"];
 console.log(animals.join(" - "));

 //output
 dog - cat - elephant - cow - gorilla
 ```

**4. Array pop() Method**

=> Array pop() method removed last element from array.

Lets understand with good example:

```javascript
var animals = ["dog" , "cat" , "elephant" , "cow" , "gorilla"];
animals.pop();
console.log(animals);

 //output
 [ 'dog', 'cat', 'elephant', 'cow' ]
 ```

 **5. Array push() Method**

=> Array push() method add last element in array.

Lets understand with good example:

```javascript
var animals = ["dog" , "cat" , "elephant" , "cow"];
animals.push("gorilla");
console.log(animals);

 //output
 [ 'dog', 'cat', 'elephant', 'cow', 'gorilla' ]
 ```

**6. Array shift() Method**

=> Array shift() method remove first element from array.

Lets understand with good example:

```javascript
var animals = ["dog" , "cat" , "elephant" , "cow"];
animals.shift();
console.log(animals);

 //output
 [ 'cat', 'elephant', 'cow' ]
 ```

**7. Array unshift() Method**

=> Array unshift() method add first element in array.

Lets understand with good example:

```javascript
var animals = [ "cat" , "elephant" , "cow"];
animals.unshift("dog");
console.log(animals);

 //output
 [ 'dog', 'cat', 'elephant', 'cow' ]
```

**8. Array splice() Method**

=> Array splice() method is used to add element in array. There are two parameters while defining 1st parameter is for position where it should be added whereas 2nd parameter is for how may elements should be removed.

Lets understand with good example:

```javascript
var animals = [ "cat" , "elephant" , "cow"];
animals.splice(2 , 1 , "dog");
console.log(animals);
```

- In animal.splice() : 2 means dog will added in index number 2 1 means how much elements should be removed.

```
//output
 [ 'cat', 'elephant', 'dog' ]
```

**9. Array slice() Method**

=> Array slice() method is used to slice an array into pieces and create a new array slice() method has two parameters from which index number need to sliced out till last limit of element.

Also we can give 1 parameter suppose in array there are 5 values and given one parameter is 1 so from first index number all values will sliced out.

Lets understand with good example:

```javascript
var animals = [ "cat" , "elephant" , "cow" , "lion" , "Tiger"];
console.log(animals.slice(2, 4));
```
In console statement 2 value means from index number 2 it will start till 4th Index all values will be sliced out and print

```
 //output
 [ 'cow', 'lion' ]
```

**10. Array concat() Method**

=> Array concat() method is used to concat if there are two or more arrays presented.

Lets understand with good example:

```javascript
var animals = [ "cat" , "elephant" , "cow" , "lion" , "Tiger"];
var food = ["Wheat" , "rice" , "milk"]
console.log(animals.concat(food));
```

```
//output
 [ 'cat', 'elephant', 'cow', 'lion', 'Tiger', 'Wheat', 'rice', 'milk' ]
```

**11. Array includes() Method**

=> Array includes() method is used to find whether given array element is presented in array or not and it return true if present, if not present print false.

Lets understand with good example:

```javascript
var animals = [ "cat" , "elephant" , "cow" , "lion" , "Tiger"];
console.log(animals.includes("cat"));

//output
true
```

