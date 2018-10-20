## ES7 & ES8

An introduction to the small features that both ES7 & ES8 brings. If contributing please read the contributions section 
and check back from time to time for intermittent updates.

### `Object.entries()`

`Object.entries` gives us the ability to get an object's enurmerable property pairs by returning an array of any given
object's own eumberable properties. /ie: [key, value] pairs. Note that the order is the same as provided by the `for...in` loop.

#### Syntax:

* `Object.entries(obj)`
* @params: `obj`
* returns: Array

#### Examples:

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

### `Object.values()`

`Object.values` lets us return an array of a given object's own enumerable property values. Note that the order is the
same as provided by the `for...in` loop.

#### Syntax:

* `Object.values(obj)`
* @params: `obj`
* returns: Array

#### Examples:

> basic example

```javascript
const obj = { a: 100, b: 200 }
console.log(Object.values(obj))

// => [100, 200]
```

> mixed
```javascript
const obj = { foo: 'foo', bar: [100, 200], baz: 55 }
console.log(Object.values(obj)) 

// => ['foo', [100, 200], 55 ]
```

> string
```javascript
const myStr = 'Lufthansa'
console.log(Object.values(myStr))

// => ["L", "u", "f", "t", "h", "a", "n", "s", "a"]
```

### `Array.prototype.includes`
This one is a bit like `indexOf` and very useful to the language by relying on returinng true or false, not `0`. 


#### Syntax:

* `arr.inlcudes(searchEl[, fromIndex])`
* @searchElement: the element to search for
* @fromIndex: pos in array at which to begin searching
* returns: Boolean

#### Examples:

> basic examples

```javascript
[1, 2, 3].includes(-1)                   // false
[1, 2, 3].includes(1)                    // true
[1, 2, 3].includes(3, 4)                 // false
[1, 2, 3].includes(3, 3)                 // false
[1, 2, NaN].includes(NaN)                // true
['foo', 'bar', 'quux'].includes('foo')   // true
['foo', 'bar', 'quux'].includes('norf')  // false
```

> if `fromIndex` is greater than or equal to the len of array, false is automatically returned
```javascript
let arr = ['x', 'y', 'z'];

arr.includes('x', 3)    // false
arr.includes('z', 100)  // false
```

### Contributions

Contributions in the form of code samples and syntax are welcome - if you spot errors in example code or feel you have a better 
use case for a given feature please issue a pull request. Typos and formatting requests are also considered.
