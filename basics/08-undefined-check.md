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

## Notes

You need to be aware of the different "null" types there are in JS, and perform your comparisons appropriately.

Remember the `===`? 

Consider

```JS
var a = {
    b: 0
}
```

We want to check if b exists:

```JS
if (a.b) // fail (but for the wrong reasons)
if (typeof a.b === 'undefined') // fail
```

We want to remove `b` from `a`

```JS
delete a.b;
if (typeof a.b === 'undefined') // pass
```
