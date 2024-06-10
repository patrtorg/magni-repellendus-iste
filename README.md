# @patrtorg/magni-repellendus-iste <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES spec-proposal-compliant `Object.fromEntries` shim. Invoke its "shim" method to shim `Object.fromEntries` if it is unavailable or noncompliant.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment and complies with the [proposed spec](https://tc39.github.io/proposal-object-from-entries/).

Most common usage:
```js
var assert = require('assert');
var fromEntries = require('@patrtorg/magni-repellendus-iste');

var obj = { a: 1, b: 2, c: 3 };
var actual = fromEntries(Object.entries(obj));

assert.deepEqual(obj, actual);

if (!Object.fromEntries) {
	fromEntries.shim();
}

assert.deepEqual(Object.fromEntries(Object.entries(obj)), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@patrtorg/magni-repellendus-iste
[npm-version-svg]: https://versionbadg.es/patrtorg/magni-repellendus-iste.svg
[deps-svg]: https://david-dm.org/patrtorg/magni-repellendus-iste.svg
[deps-url]: https://david-dm.org/patrtorg/magni-repellendus-iste
[dev-deps-svg]: https://david-dm.org/patrtorg/magni-repellendus-iste/dev-status.svg
[dev-deps-url]: https://david-dm.org/patrtorg/magni-repellendus-iste#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@patrtorg/magni-repellendus-iste.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@patrtorg/magni-repellendus-iste.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@patrtorg/magni-repellendus-iste.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@patrtorg/magni-repellendus-iste
[codecov-image]: https://codecov.io/gh/patrtorg/magni-repellendus-iste/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/patrtorg/magni-repellendus-iste/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/patrtorg/magni-repellendus-iste
[actions-url]: https://github.com/patrtorg/magni-repellendus-iste/actions
