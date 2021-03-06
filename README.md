# bep53-range [![travis][travis-image]][travis-url] [![npm][npm-image]][npm-url] [![downloads][downloads-image]][downloads-url] [![javascript style guide][standard-image]][standard-url]

[travis-image]: https://img.shields.io/travis/webtorrent/bep53-range/master.svg
[travis-url]: https://travis-ci.org/webtorrent/bep53-range
[npm-image]: https://img.shields.io/npm/v/bep53-range.svg
[npm-url]: https://npmjs.org/package/bep53-range
[downloads-image]: https://img.shields.io/npm/dm/bep53-range.svg
[downloads-url]: https://npmjs.org/package/bep53-range
[standard-image]: https://img.shields.io/badge/code_style-standard-brightgreen.svg
[standard-url]: https://standardjs.com

### Parse and compose Magnet URI extension (BEP53) ranges.

Also works in the browser with [browserify](http://browserify.org/)! This module is used by [WebTorrent](http://webtorrent.io).

## install

```
npm install bep53-range
```

## usage

### parse

Parse Magnet URI extension (BEP53) range and return all included values.

```js
const bep53Range = require('bep53-range')

const range = ['1-3', '6', '11-13']

const values = bep53Range.parse(range)
console.log(values) // [1, 2, 3, 6, 11, 12, 13]

```

### compose

Compose Magnet URI extension (BEP53) range from all included values.

```js
const bep53Range = require('bep53-range')

const values = [1, 2, 3, 6, 11, 12, 13]

const range = bep53Range.compose(values)
console.log(range) // ['1-3', '6', '11-13']
```

## license

MIT. Copyright (c) [Julen Garcia Leunda](https://github.com/hicom150) and [WebTorrent, LLC](https://webtorrent.io).
