# proposal-array-grouping

A proposal to make grouping of items in an array easier.

```js
const array = [1, 2, 3, 4, 5];

// groupBy groups items by arbitrary key.
// In this case, we're grouping by even/odd keys
array.groupBy(i => {
  return i % 2 === 0 ? 'even': 'odd';
});

// =>  { odd: [1, 3, 5], even: [2, 4] }
```

## Champions

- Justin Ridgewell ([@jridgewell](https://github.com/jridgewell/))

## Status

Current [Stage](https://tc39.es/process-document/): 1

## Motivation

TODO

## Polyfill

Pending polyfill implementations...

## Related

- Lodash
  - [`_.groupBy`](https://lodash.com/docs/4.17.15#groupBy) ([850k downloads/week](https://www.npmjs.com/package/lodash.groupby))
