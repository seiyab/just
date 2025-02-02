## just-entries

Part of a [library](https://anguscroll.com/just) of zero-dependency npm modules that do just do one thing.
Guilt-free utilities for every occasion.

[`🍦 Try it`](https://anguscroll.com/just/just-entries)

```shell
npm install just-entries
```
```shell
yarn add just-entries
```

Return object entries as an array of [key, value] pairs

```js
import entries from 'just-entries';

// Object:
entries({c: 8, a: 4}); // [['c', 8], ['a', 4]]
entries({b: {bb: 4}, a: {aa: 2}}); // [['b', {bb: 4}], ['a', {aa: 2}]]
entries({}); // []

// Array:
entries([{c: 8}, {a: 4}]); // [[0, {c: 8}], [1, {a: 4}]]
entries(['À', 'mauvais', 'ouvrier', 'point', 'de', 'bon', 'outil'])
// [[0, 'À'], [1, 'mauvais'] ... [6, 'outil']]
entries([]); // []
```
