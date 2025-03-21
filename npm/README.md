# @bearz/option

## Overview

The '@bearz/option' module provides the `Option<T>` type with functions some, none,
and from which are all used to help deal with null and undefined values.

![logo](https://raw.githubusercontent.com/bearz-io/js/refs/heads/main/eng/assets/bearz.io.png)

[![JSR](https://jsr.io/badges/@bearz/option)](https://jsr.io/@bearz/option)
[![npm version](https://badge.fury.io/js/@bearz%2Foption.svg)](https://badge.fury.io/js/@bearz%2Foption)
[![GitHub version](https://badge.fury.io/gh/bearz-io%2Fjs-option.svg)](https://badge.fury.io/gh/bearz-io%2Fjs-option)

## Documentation

Documentation is available on [jsr.io](https://jsr.io/@bearz/option/doc)

A list of other modules can be found at [github.com/bearz-io/js](https://github.com/bearz-io/js)

## Usage

```typescript
import { ok, some, none } from "@bearz/functional";

const o1 = none<number>();
console.log(o1.isSome); // false 
console.log(o1.isNone); // true
console.log(o1.unwrapOrElse(() => 50)); // 50

const o = some(10);
console.log(o.isSome); // true
console.log(o.isNone); // false
o.inspect(g => console.log(g));
console.log(o.map(g => g * 60).unwrap()); // 60

```

## License

[MIT License](./LICENSE.md)
