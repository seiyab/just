## just-index

Part of a [library](https://anguscroll.com/just) of zero-dependency npm modules that do just do one thing.
Guilt-free utilities for every occasion.

[`🍦 Try it`](https://anguscroll.com/just/just-index)

```shell
npm install just-index
```
```shell
yarn add just-index
```

Return an object from an array, keyed by the value at the given id

```js
import index from 'just-index';

index([{id: 'first', val: 1}, {id: 'second', val: 2}], 'id');
// {first: {id: 'first', val: 1}, second: {id: 'second', val: 2}}
index([{id: 'first', val: 1}, null], 'id'); // {first: {id: 'first', val: 1}}
index([], 'id'); // {}
index([], null); // undefined
index({}, 'id'); // undefined
```
