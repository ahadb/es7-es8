## ES7 & ES8

An introduction to the small features that both ES7 & ES8 brings. If contributing please read the contributions section 
and check back from time to time for intermittent updates.

### `Object.entries`

`Object.entries` gives us the ability to get an object's enurmerable property pairs by returning an array of any given
object's own eumberable properties. /ie: [key, value] pairs. Note that the order is the same as provided by the `for...in` loop.

#### Syntax

`Object.entries(obj)`

> basic example

```javascript
const obj = { self: 'that', norf: 'quux' }
console.log(Object.entries(obj))

// => [ ['self', 'that'], ['norf', 'quux'] ]
```

> array like object with random key ordering
```javascript
const obj = { 50: 'a', 1: 'b', 5: 'c' }
console.log(Object.entries(obj)) 

// => [ ['1', 'b'], ['5', 'c'], ['50', 'a'] ]
```

### `Object.values`

`Object.values` lets us return an array of a given object's own enumerable property values. Note that the order is the
same as provided by the `for...in` loop.

> simple example

```javascript
const obj = { self: 'that', norf: 'quux' }
console.log(Object.entries(obj))

// => [ ['self', 'that'], ['norf', 'quux'] ]
```

> array like object with random key ordering
```javascript
const obj = { 50: 'a', 1: 'b', 5: 'c' }
console.log(Object.entries(obj)) 

// => [ ['1', 'b'], ['5', 'c'], ['50', 'a'] ]
```

### Contributions

Contributions in the form of code samples and syntax are welcome - if you spot errors in example code or feel you have a better 
use case for a given feature please issue a pull request. Typos and formatting requests are also considered.
