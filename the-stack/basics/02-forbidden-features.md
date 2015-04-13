# Forbidden Features

Part of the difficulty of mastering JS is knowing when to just say NO.

Here is a list of things that JS will tempt you with. Never give in.

## `==` vs `===`

Never use `==`. If you have to / want to be sure you know what you're doing:

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

#### References:

Bad Parts: Appendix B - JavaScript: The Good Parts
http://archive.oreilly.com/pub/a/javascript/excerpts/javascript-good-parts/bad-parts.html
Douglas Crockford
