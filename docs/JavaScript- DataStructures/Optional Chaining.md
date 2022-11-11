---
sidebar_position: 6
---

- Optional chaining is used in such cases where you need to make sure that said method exists.

- Used to check whether things on left side exist or not, if it returns falsy value(null, undefined) it returns that value, if its truthy value, then it proceeds further. Optional chaining is often used with nullish coalescent operator.

**Example:**

```js
// Optional Chaining

// if (restaurant.openingHours.mon) console.log(restaurant.openingHours.mon.open);
// if (restaurant.openingHours.fri) console.log(restaurant.openingHours.fri.open);

console.log(restaurant.openingHours?.mon?.open); // If restaurant.openingHours exist, if true => .mon exists, if true => get .open // If at any point any one doesn't exist, false value is returned
console.log(restaurant.openingHours?.fri?.open);

const weekDays = ['mon', 'tue', 'wed', 'thu', 'fri', 'sat', 'sun'];
for (let currDay of weekDays) {
  const open = restaurant.openingHours[currDay]?.open ?? 'Closed';
  console.log(`Our hotel opens on ${currDay} at ${open}`);
}
```