# Subtractly - Javascript utility to help you with subtraction

[![NPM version (>=0.4)](https://img.shields.io/npm/v/subtractly.svg?style=flat-square)](https://www.npmjs.com/package/subtractly) [![NPM Downloads](https://img.shields.io/npm/dm/subtractly.svg?style=flat-square)](https://www.npmjs.com/package/subtractly) [![Coverage Status](https://img.shields.io/coveralls/michael-iglesias/subtractly.svg?style=flat-square)](https://coveralls.io/r/michael-iglesias/subtractly) [![Build Status](https://img.shields.io/travis/michael-iglesias/subtractly/master.svg?style=flat-square)](https://travis-ci.org/michael-iglesias/subtractly) [![Dependencies](https://img.shields.io/david/michael-iglesias/subtractly.svg?style=flat-square)](https://david-dm.org/michael-iglesias/subtractly)  [![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square)](http://standardjs.com/) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://raw.githubusercontent.com/michael-iglesias/subtractly/master/LICENSE.md)

_Exports a polymorphic 'subtract()' that can take numbers, strings, objects, & arrays_


## Installation

```
npm install --save subtractly
```

## What is this magic? How does it work?

This super simple library exports a curried function that allows you to subtract numbers, strings, and diff objects & arrays.

* Subtracting two objects
```
let obj1 = {foo: 'bar', baz: 'blob'},
    obj2 = {baz: 'foobar'};

subtractly(obj1, obj2);
// => [{ foo: 'bar' }]
```

* Deleting properties from an object by passing an array of properties to be removed.
```
let obj1 = {foo: '123', bar: '456', baz: '789'},

subtractly(obj1, ['foo', 'bar']);
// => [{ baz: '789' }]
```

* Diffing arrays
```
let arr1 = [1,2,3,4,5],
    arr2 = [2,3];

subtractly(arr1, arr2);
// => [1,4,5]
```

* Removing all instances of a substring from a string
```
subtractly('mississippi', 'i');
// => msssspp
```

* Subtracting numbers is difficult... subtractly can handle that as well ;)
```
subtractly(52, 10);
// => 42
```

## License

MIT, see `LICENSE.md` for more information.
