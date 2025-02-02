## just-throttle

Part of a [library](https://anguscroll.com/just) of zero-dependency npm modules that do just do one thing.
Guilt-free utilities for every occasion.

[`🍦 Try it`](https://anguscroll.com/just/just-throttle)

```shell
npm install just-throttle
```
```shell
yarn add just-throttle
```

Return a throttled function

```js
import throttle from 'just-throttle';

// no matter how many times the function is called, only invoke once within the given interval
// options: 
// `leading`: invoke  before interval
// `trailing`: invoke afer interval

const fn1 = throttle(() => console.log('hello'), 500, {leading: true});
setInterval(fn1, 400);
// logs 'hello' immediately and then every 500ms

const fn2 = throttle(() => console.log('hello'), 500, {trailing: true});
setInterval(fn2, 400);
// logs 'hello' after 500ms and then every 500ms

const fn3 = throttle(() => console.log('hello'), 500, {leading: true, trailing: true});
// forces trailing to false

const fn4 = throttle(() => console.log('hello'), 500, { leading: false });
fn4();
fn4();
fn4();
fn4.cancel();
// function cancelled before 'hello' is logged

const fn5 = throttle(() => console.log("Hello"), 500);
fn5();
fn5();
fn5();
fn5.flush();
// immediately invoke the throttled function
```
