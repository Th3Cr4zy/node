# define-property [![NPM version](https://img.shields.io/npm/v/define-property.svg?style=flat)](https://www.npmjs.com/package/define-property) [![NPM monthly downloads](https://img.shields.io/npm/dm/define-property.svg?style=flat)](https://npmjs.org/package/define-property)  [![NPM total downloads](https://img.shields.io/npm/dt/define-property.svg?style=flat)](https://npmjs.org/package/define-property) [![Linux Build Status](https://img.shields.io/travis/jonschlinkert/define-property.svg?style=flat&label=Travis)](https://travis-ci.org/jonschlinkert/define-property)

> Define a non-enumerable property on an object.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save define-property
```

Install with [yarn](https://yarnpkg.com):

```sh
$ yarn add define-property
```

## Usage

**Params**

* `obj`: The object on which to define the property.
* `prop`: The name of the property to be defined or modified.
* `descriptor`: The descriptor for the property being defined or modified.

```js
var define = require('define-property');
var obj = {};
define(obj, 'foo', function(val) {
  return val.toUpperCase();
});

console.log(obj);
//=> {}

console.log(obj.foo('bar'));
//=> 'BAR'
```

**get/set**

```js
define(obj, 'foo', {
  get: function() {},
  set: function() {}
});
```

## About

### Related projects

* [assign-deep](https://www.npmjs.com/package/assign-deep): Deeply assign the enumerable properties and/or es6 Symbol properies of source objects to the target… [more](https://github.com/jonschlinkert/assign-deep) | [homepage](https://github.com/jonschlinkert/assign-deep "Deeply assign the enumerable properties and/or es6 Symbol properies of source objects to the target (first) object.")
* [extend-shallow](https://www.npmjs.com/package/extend-shallow): Extend an object with the properties of additional objects. node.js/javascript util. | [homepage](https://github.com/jonschlinkert/extend-shallow "Extend an object with the properties of additional objects. node.js/javascript util.")
* [merge-deep](https://www.npmjs.com/package/merge-deep): Recursively merge values in a javascript object. | [homepage](https://github.com/jonschlinkert/merge-deep "Recursively merge values in a javascript object.")
* [mixin-deep](https://www.npmjs.com/package/mixin-deep): Deeply mix the properties of objects into the first object. Like merge-deep, but doesn't clone. | [homepage](https://github.com/jonschlinkert/mixin-deep "Deeply mix the properties of objects into the first object. Like merge-deep, but doesn't clone.")

### Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

### Building docs

_(This project's readme.md is generated by [verb](https://github.com/verbose/verb-generate-readme), please don't edit the readme directly. Any changes to the readme must be made in the [.verb.md](.verb.md) readme template.)_

To generate the readme, run the following command:

```sh
$ npm install -g verbose/verb#dev verb-generate-readme && verb
```

### Running tests

Running and reviewing unit tests is a great way to get familiarized with a library and its API. You can install dependencies and run tests with the following command:

```sh
$ npm install && npm test
```

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](https://twitter.com/jonschlinkert)

### License

Copyright © 2017, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT License](LICENSE).

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.5.0, on April 20, 2017._