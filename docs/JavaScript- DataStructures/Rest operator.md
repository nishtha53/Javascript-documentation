---
sidebar_position: 3
---

- Used to collect different element and condense them into an array. Its opposite of spread operator which expands, rest  collects.

- If used on left side of assignment.

- It is used in parameter (function definition).

- It must be the last element on array if used in parameter, as it condenses all the other element passed during function call so it won’t leave any value for any further variable.

```js
// REST Operator ---> 1. Arrays

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

  orderPasta: function (ingA, ingB, ingC) {
    console.log(`Here is your delicious pasta with ${ingA}, ${ingB}, ${ingC}`);
  },

  orderPizza: function (mainIngredient, ...restIngredient) {
    console.log(mainIngredient);
    console.log(restIngredient);
  },
};

const arr = [1, 2, ...[3, 4, 5]];
console.log(arr); // [1, 2, 3, 4, 5]

const [x, , ...y] = arr;
console.log(x, y); // 1 [3, 4, 5]

console.log([...restaurant.mainMenu, ...restaurant.starterMenu]); // ['Pizza', 'Pasta', 'Risotto', 'Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad']

const [pizza, , risotto, ...otherMenuItems] = [
  ...restaurant.mainMenu,
  ...restaurant.starterMenu,
];
console.log(pizza, risotto, otherMenuItems); // Pizza Risotto ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad']

const { sat, ...weekDays } = restaurant.openingHours;
console.log(sat, weekDays);  // {sat: {..}} {thu: {...}, fri: {..}}

// REST Operator ---> 2. Functions
const add = function (...numbers) {
  console.log(numbers);
  let sum = 0;
  for (let currNumber of numbers) sum += currNumber;
  console.log(sum);
};

add(3, 5); // [3, 5]
add(1, 2, 3, 4, 5); // [1, 2, 3, 4, 5]
add(6, 7, 8, 2, 5, 1, 3); // [6, 7, 8, 2, 5, 1, 3]

restaurant.orderPizza('Tomato'); // Tomato []
restaurant.orderPizza('Tomato', 'Paneer', 'Black Olives'); // Tomato ['Paneer', 'Black Olives']
restaurant.orderPizza('Tomato', 'Cheese', 'Black Olives', 'Pineapple'); // Tomato ['Cheese', 'Black Olives', 'Pineapple']
```
