---
sidebar_position: 2
---

- Used to spread/expand an array with all its elements, unpacking all elements at one place.

- It can be used to merge two arrays.

- To print or pass just the elements in a function call.

- Returns new array when merged.

- Difference between spread operator and object destructuring is that spread operator takes elements from an array and can't create new variables, we can use it only where values are written separated by commas, e.g.: [...arr, 7, 8, 9]. Here values were written separated by commas.

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

// Spread operator

const arr = [1, 2, 3];
const newArr = [...arr, 4, 5, 6];
//merge 2 arrays
console.log([...newArr, ...arr]); // [1, 2, 3, 4, 5, 6, 1, 2, 3]
console.log(newArr); // [1, 2, 3, 4, 5, 6]
console.log(arr); // [1, 2, 3]
// Separate elements
console.log(...arr); // 1 2 3 => See elements are not printed in arrays
console.log(...newArr); // 1 2 3 4 5 6

const newMenu = [
  ...restaurant.starterMenu,
  'Paneer Tikka Masala',
  'Manchurian',
];
console.log(newMenu); // ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad', 'Paneer Tikka Masala', 'Manchurian']

const mainMenuCopy = [...restaurant.mainMenu];
const menu = [...mainMenuCopy, ...restaurant.starterMenu];
console.log(menu); // ['Pizza', 'Pasta', 'Risotto', 'Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad']

// Split string into letters
const str = 'Jagrut';
const letters = [...str, ' ', 'S'];
console.log(letters); // ['J', 'A', 'G', 'R', 'U', 'T', ' ', 'S']

// Can be passed as array

const ingredients = ['Tomato', 'Garlic', 'Spices'];
restaurant.orderPasta(...ingredients); // Will pass => Tomato Garlic Spices

// creates a shallow copy
const newRestaurant = { Since: 1989, ...restaurant, ownedBy: 'Bakeri group' };
console.log(newRestaurant); // Prints objects with additional properties as defined

// creates a shallow copy
const restaurantCopy = { ...restaurant };
restaurantCopy.name = 'Sher-E Punjab';
console.log(restaurantCopy);
console.log(restaurant);
```