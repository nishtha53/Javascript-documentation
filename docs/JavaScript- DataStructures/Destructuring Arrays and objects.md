---
sidebar_position: 1
---

## Destructuring Arrays.

- Destructuring means to break down a complex structure into simpler parts. With the syntax of destructuring, you can extract smaller fragments from objects and arrays. It can be used for assignments and declaration of a variable.

- Destructuring is an efficient way to extract multiple values from data that is stored in arrays or objects. When destructuring an array, we use their positions (or index) in an assignment.

- Js sees array on left side, it understands that its destructuring. Original array js not affected.

- If we enter a variable and that element does not exist, value assigned is undefined. A default value can also be set when we don't know the length of array. Used in API calls.

**Example**

```js
const arr = [2, 4, 6, 8];
const [x, , z] = arr;
console.log(x, z);

//output
2 6
```

**Example**

```js
const restaurant = {
  name: 'Classico Italiano',
  location: 'Via Angelo Tavanti 23, Firenze, Italy',
  categories: ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'],
  starterMenu: ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad'],
  mainMenu: ['Pizza', 'Pasta', 'Risotto'],

  orderFood(starterIndex, mainIndex) {
    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
  },

  openingHours: {
		  thu: {
		    open: 12,
		    close: 22,
		  },
		  fri: {
		    open: 11,
		    close: 23,
		  },
		  sat: {
		    open: 0, // Open 24 hours
		    close: 24,
		  },
		},
};

let [first, , secondary] = restaurant.categories; 
console.log(first, secondary); // Italian, Vegeterian

// Switch values
[secondary, first] = [first, secondary];
console.log(first, secondary); // Vegeterian Italian

// receiving two values from function
const [starterItem, mainItem] = restaurant.orderFood(2, 0);
console.log(starterItem, mainItem); // Garlic Bread Pizza

//nested arrays
const nestedArr = [1, 2, [3, 4, 5]];
const [i, , j] = nestedArr; 
console.log(i, j); // 1, [3, 4, 5]

const [k, , [l, , n]] = nestedArr;
console.log(k, l, n); // 1 3 5

//default value
let sampleArr = [1, 2, 3];
// sampleArr = [5];
const [a = 1, b = 1, , d = 1] = sampleArr; // WIll assign default value as 1, used in API calls
console.log(a, b, d); // 1 2 1
```


## Destructuring Objects.

- Objects can also be destructured. This is very helpful as we work with an API, We just need to write properties of the object and those variables will be created. It is very important that properties name are same as in object.

- To reassign a variable name that is used and also present in object, a parenthesis is used.

- Can also be used to de-structure object inside object.


**Example**

```js
const pet = {
 name: 'Captain',
 food: 'Kibble',
 color: 'Black'
};

// if need to access food we will write:

console.log(pet.food)
//output
Kibble
```

Instead of writing out const food = pet.food, we can utilize destructuring and simply write:

```js
const { food } = pet;
```

Now if we print out food again, we can see we've created the food variable:

```js
console.log(food); 
// output: kibble
```

- Remember, within a JavaScript object, a property is a key/value pair. The key is a string, and the value can be any data type. In the pet object, one of the keys is food, and its corresponding value is kibble.  

- When we wrap our food variable in brackets, we look inside of our pet object for a property with the same name. We create a new variable with the name food, and we set its value to kibble, the corresponding value of that key.

**Example**

```js
const restaurant = {
  name: 'Classico Italiano',
  location: 'Via Angelo Tavanti 23, Firenze, Italy',
  categories: ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'],
  starterMenu: ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad'],
  mainMenu: ['Pizza', 'Pasta', 'Risotto'],

  orderFood(starterIndex, mainIndex) {
    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
  },

  openingHours: {
		  thu: {
		    open: 12,
		    close: 22,
		  },
		  fri: {
		    open: 11,
		    close: 23,
		  },
		  sat: {
		    open: 0, // Open 24 hours
		    close: 24,
		  },
		},

	deliveryOrder: function ({
    time: deliveryTime = '22:00',
    starterIndex: starterMenuItem = 'Manchurian',
    mainIndex: mainMenuItem,
    address: deliveryAddress = 'Russia',
  }) {
    console.log(
      `Hi, your order, ${this.starterMenu[starterMenuItem]}, ${this.mainMenu[mainMenuItem]} will be delivered to ${deliveryAddress} at ${deliveryTime}. Thanks!`
    );
  },
};

// Destructuring Objects

const { name, categories, openingHours } = restaurant; // Properties name must be same
const {
  name: restaurantName = 'Sher-e Punjab',
  categories: menuAvailable = [
    'punjabi',
    'chinese',
    'south indian',
    'kathyawadi',
  ],
  openingHours: duration,
} = restaurant; // Assigning desired name for variables in which properties willbe stored and also assigning default values.

// console.log(name, categories, openingHours);

console.log(restaurantName, menuAvailable, duration); // Classico Italiano ['Pizza', 'Pasta', 'Risotto'] {thu: {}, ....}

let a = 99;
let b = 159;
const obj = { a: 23, b: 46 };
// let {a, b} = obj; // Gives error
({ a, b } = obj); // This will overwrite above a and b variables. Need to cover in parenthesis for assigning destructured object properties values.
console.log(a, b); // 23 46

// const { fri } = duration;
const {
  fri: { open: openingTime = 12, close: closingTime = 11 },
} = duration;
console.log(openingTime, closingTime); // 11 23

restaurant.deliveryOrder({
  time: '22:30',
  starterIndex: 2,
  mainIndex: 2,
  address: 'India',
}); // Hi, your order, Garlic Bread, Risotto will be delivered to India at 22:30. Thanks!

restaurant.deliveryOrder({
  mainIndex: 2,
}); // default values will be applied -> Hi, your order, Manchurian, Risotto will be delivered to Russia at 22:00. Thanks!
```





