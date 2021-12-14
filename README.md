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

Array grouping is an extremely common operation, best exemplified by
SQL's `GROUP BY` clause and MapReduce programming (which is better
thought of map-group-reduce). The ability to combine like data into
groups allows developers to compute higher order datasets, like the
average age of a cohort or daily LCP values for a webpage.

Two methods are offered, `groupBy` and `groupByMap`. The first returns a
null-prototype object, which allows ergonomic destructuring and prevents
accidental collisions with global Object properties. The second returns
a regular `Map` instance, which allows grouping on complex key types
(imagine a compound key or [tuple]).

## Polyfill

- A polyfill is available in the [core-js] library. You can find it in the [ECMAScript proposals section][core-js-section].

## Related

- Lodash
  - [`_.groupBy`][lodash] ([850k downloads/week][lodash-npm])

[tuple]: https://github.com/tc39/proposal-record-tuple
[core-js]: https://github.com/zloirock/core-js
[core-js-section]: https://github.com/zloirock/core-js#array-grouping
[lodash]: https://lodash.com/docs/4.17.15#groupBy
[lodash-npm]: https://www.npmjs.com/package/lodash.groupby
