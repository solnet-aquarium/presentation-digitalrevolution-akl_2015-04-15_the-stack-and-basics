# Undefined check

Consistently use:

```JS
typeof a === 'undefined'
```

Yes there are many other ways to do this.  This way has stood the test of time for me and many others.

```JS
var x;
x === undefined // true

var xx = null;
xx === undefined // false

if (xxx === undefined) {
    // Stops execution
}
```
