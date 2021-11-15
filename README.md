# proposal-array-grouping

A proposal to make grouping of items in an array easier.

```js
const array = [1, 2, 3, 4, 5];

// groupBy groups items by arbitrary key.
// In this case, we're grouping by even/odd keys
array.groupBy((num, index, array) => {
  return num % 2 === 0 ? 'even': 'odd';
});

// =>  { odd: [1, 3, 5], even: [2, 4] }
```

## Champions

- Justin Ridgewell ([@jridgewell](https://github.com/jridgewell/))

## Status

Current [Stage](https://tc39.es/process-document/): 2

## Motivation

TODO

## Polyfill

- A polyfill is available in the [core-js](https://github.com/zloirock/core-js) library. You can find it in the [ECMAScript proposals section](https://github.com/zloirock/core-js#array-grouping).

## Related

- Lodash
  - [`_.groupBy`](https://lodash.com/docs/4.17.15#groupBy) ([850k downloads/week](https://www.npmjs.com/package/lodash.groupby))
