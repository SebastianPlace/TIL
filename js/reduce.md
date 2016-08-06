# Reduce

Reduce can be used to manipulate lists in many ways. Using reduce you can implement the functionality of map, filter, reject etc.

Reduce takes a callback and an optional initial value.

A trivial example:

```
let orders = [
	{amount: 50},
  {amount: 60},
  {amount: 23}
];

let totalCost = orders.reduce((sum, order) => sum + order.amount, 0)
console.log(totalCost);
```
