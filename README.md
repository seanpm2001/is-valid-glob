# is-valid-glob [![NPM version](https://badge.fury.io/js/is-valid-glob.svg)](http://badge.fury.io/js/is-valid-glob)

> Return true if a value is a valid glob pattern or patterns.

This really just checks to make sure that a pattern is either a string or array, and if it's an array it's either empty or consists of only strings.

## Install

Install with [npm](https://www.npmjs.com/)

```sh
$ npm i is-valid-glob --save
```

## Usage

```js
var isValidGlob = require('is-valid-glob');

isValidGlob('foo/*.js');
//=> true
```

**Valid patterns**

```js
isValidGlob('a');
isValidGlob('a.js');
isValidGlob('*.js');
isValidGlob(['a', 'b']);
isValidGlob('');
isValidGlob([]);
//=> all true
```

**Invalid patterns**

```js
isValidGlob();
isValidGlob({});
isValidGlob(null);
isValidGlob(undefined);
isValidGlob(new Buffer('foo'));
isValidGlob(['foo', [[]]]);
isValidGlob(['foo', [['bar']]]);
isValidGlob(['foo', {}]);
//=> all false
```

## Related projects

* [braces](https://github.com/jonschlinkert/braces): Fastest brace expansion for node.js, with the most complete support for the Bash 4.3 braces… [more](https://github.com/jonschlinkert/braces)
* [expand-range](https://github.com/jonschlinkert/expand-range): Fast, bash-like range expansion. Expand a range of numbers or letters, uppercase or lowercase. See… [more](https://github.com/jonschlinkert/expand-range)
* [fill-range](https://github.com/jonschlinkert/fill-range): Fill in a range of numbers or letters, optionally passing an increment or multiplier to… [more](https://github.com/jonschlinkert/fill-range)
* [is-glob](https://github.com/jonschlinkert/is-glob): Returns `true` if the given string looks like a glob pattern.
* [micromatch](https://github.com/jonschlinkert/micromatch): Glob matching for javascript/node.js. A drop-in replacement and faster alternative to minimatch and multimatch. Just… [more](https://github.com/jonschlinkert/micromatch)

## Running tests

Install dev dependencies:

```sh
$ npm i -d && npm test
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/is-valid-glob/issues/new)

## Author

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2015 Jon Schlinkert
Released under the MIT license.

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on July 07, 2015._