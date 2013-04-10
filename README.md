# tic

setInterval/setTimeout using a delta tick. Useful for timing things with games.

## example

```js
var tic = require('tic');

var clearInterval = tic.interval(function(param1) {
  console.log(param1 + ' 5 tick seconds!');
}, 5000, 'Every');

var clearTimeout = tic.timeout(function() {
  console.log('Only once after 10 tick seconds!');
}, 10000);

game.on('tick', function(dt) {
  tic.tick(dt);
});
```

## api

### `tic.interval(fn, time, [param1, param2, ...])`

### `tic.timeout(fn, time, [param1, param2, ...])`

### `tic.tick(delta)`

## install
With [npm](http://npmjs.org) do:

```
npm install tic
```

## release history
* 0.1.0 - initial release

## license
Copyright (c) 2013 Kyle Robinson Young<br/>
Licensed under the MIT license.