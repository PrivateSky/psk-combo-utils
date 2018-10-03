Generate all possible permutations of an object's key-value pairs. Combos
takes all the possible values an object's keys can have and creates all possible
combinations of those values for each key.

## Usage

equire the `psk-combo-utils` function and provide it with an object. The keys of
the object are the keys you desire to have in your final objects. The values are
an array, containing all possible values that given key can have. The return
value is an array containing every version of the object with all possible
combinations of the values.

A simple example helps explain:

```js
// Simple example
// ES2015


const cartesianProduct = require('psk-combo-utils');

// Given an object shape of
// {
//   greeting: string,
//   name: string,
// }

// Generate all possible combinations.
// (Note: you don't have to restrict each
// array of values to all have the same type.)
const permutations = cartesianProduct({
  greeting: ['Hello', 'Hi'],
  name: ['Jeremy', 'Jet']
});

// 'greeting' has 2 possible values
// 'name' has 2 possible values
// Therefore, the final array will have 2*2 = 4 possible objects.

// Output with 4 different objects:
// =================================
// [ { greeting: 'Hello', name: 'Jeremy' },
//   { greeting: 'Hi',    name: 'Jeremy' },
//   { greeting: 'Hello', name: 'Jet'    },
//   { greeting: 'Hi',    name: 'Jet'    } ]
```