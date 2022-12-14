# get-dtype-of

[![NPM version](https://img.shields.io/npm/v/get-dtype-of.svg)](https://www.npmjs.com/package/get-dtype-of)
[![NPM downloads](https://img.shields.io/npm/dm/get-dtype-of.svg)](https://www.npmjs.com/package/get-dtype-of)
[![Known Vulnerabilities](https://snyk.io/test/github/grjan7/get-dtype-of/badge.svg)](https://snyk.io/test/github/grjan7/get-dtype-of)

## Description

This package returns the type of `input`. By default, the returned data type can be a `string | number | boolean | array | object | null | undefined | function`. Setting `refineObject` to `true` returns the refined type of `object` (e.g., Date, Map, Set, Buffer, EventEmitter).

## Installation
```sh
  npm i get-dtype-of
```

### Usage

#### `getTypeOf(input, refineObject)`

  - **input** | any
  - **refineObject** | boolean | default: false

#### Examples

```js

  const getTypeOf = require('get-dtype-of');

```

| Without Option                | Returns   |  With Option (refineObject: true)     | Returns   |
| :-----------------------------|:----------|:--------------------------------------|:----------|
|                               |           |                                       |           |
| getTypeOf(`"Hello"`)          | string    | getTypeOf(`"Hello"`, `true`)          | string    |
|                               |           |                                       |           |
| getTypeOf(`412`)              | number    | getTypeOf(`412`, `true`)              | number    |
|                               |           |                                       |           |
| getTypeOf(`true`)             | boolean   | getTypeOf(`true`, `true`)             | boolean   |
|                               |           |                                       |           |
| getTypeOf(`undefined`)        | undefined | getTypeOf(`undefined`, `true`)        | undefined |
|                               |           |                                       |           |
| getTypeOf(`["a", "b"]`)       | array     | getTypeOf(`["a", "b"]`, `true`)       | array     |
|                               |           |                                       |           |
| getTypeOf(`null`)             | null      | getTypeOf(`null`, `true`)             | null      |
|                               |           |                                       |           |
| getTypeOf(`stream`)           | function  | getTypeOf(`stream`, `true`)           | function  |
|                               |           |                                       |           |
| getTypeOf(`{ name: "John" }`) | object    | getTypeOf(`{ name: "John" }`, `true`) | object    |
|                               |           |                                       |           |
| getTypeOf(`/[a-z]/`)          | object    | getTypeOf(`/[a-z]/`, `true`)          | RegExp    |
|                               |           |                                       |           |
| getTypeOf(`new Date()`)       | object    | getTypeOf(`new Date()`, `true`)       | Date      |
|                               |           |                                       |           |
| getTypeOf(`new Set()`)        | object    | getTypeOf(`new Set()`, `true`)        | Set       |
|                               |           |                                       |           |


