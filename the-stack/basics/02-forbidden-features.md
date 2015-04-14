# Forbidden Features `==`

Part of the difficulty of mastering JS is knowing when to just say NO.

Never use `==`. 

If you have to / want to be sure you know what you're doing:

The following table is not a joke

```JS
'' == '0'          // false
0 == ''            // true
0 == '0'           // true

false == 'false'   // false
false == '0'       // true

false == undefined // false
false == null      // false
null == undefined  // true

' \t\r\n ' == 0    // true
```

`==` means "is this thing like this other thing". 
This is nonsense. "like" has no place in programming and you should find using it alarming. 

Instead use `===` the "equivalence" operator. It means what you think you mean. 
It means "is this thing the same type as the other thing, and does it have the same value as the other thing"

```JS
'' === '0'          // false
0 === ''            // false
0 === '0'           // false

false === 'false'   // false
false === '0'       // false

false === undefined // false
false === null      // false
null === undefined  // false

' \t\r\n ' === 0    // false
```

#### References:

Bad Parts: Appendix B - JavaScript: The Good Parts
http://archive.oreilly.com/pub/a/javascript/excerpts/javascript-good-parts/bad-parts.html
Douglas Crockford
