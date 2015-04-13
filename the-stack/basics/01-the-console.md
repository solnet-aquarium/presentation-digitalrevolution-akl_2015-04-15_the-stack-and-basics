# The Console

Doesn't exist in IE unless "F12 Developer tools" is open - therefore don't commit `console.logs`, use them locally only.

Should ALWAYS BE OPEN! Seriously I can't stress this enough. Everytime I see a developer working with the console closed I die a little inside.

## Don't limit yourself

There is more than just `console.log`.

### `console.log`

Browser - Log objects, arrays, *anything* and inspect it in Chrome's console.
 - Chrome will colour types differently (i.e. number, string) helpful for figuring out why your `===` are not doing what you expect
 - Chrome will expand `Date` objects for you 
 
Node - Same, there are extensions that make it even better `node-console-stamp`, `better-console` to name two.

```JS
var a = { one: 1, two: '2', three: new Date() };
console.log(a);
```

### `console.error` & `console.trace`
Similar to `console.log`, but with a trace. Error variant is more alarming. 
 - Outputs the subject and a trace of where the call came from

### `console.time`

Time execution!

```JS
console.time('timer');
// some actions that take ... time
console.timeEnd('timer'); // timer: 0.010ms
```
 
Others that you won't use
 
 - `console.warn`
 - `console.debug`
