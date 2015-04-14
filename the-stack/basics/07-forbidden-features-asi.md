# Forbidden Features - Automatic Semicolon Insertion

## The Problem

A lot of people who use JS seem to think that semi colons are optional.  They are not.

There are a set of rules that govern when the JS interpreter will insert a semi colon. You will not be able to learn these better than the interpreter, *[although you should definitely try](http://stackoverflow.com/a/2846298/187954)*.

Example of how this can cause code to behave unexpectedly:

```JS
// This returns undefined
return 
{
  a: 5
};
```

File minification & concatenation example:

```JS
// File 1
(function awesomeFunction() {
  console.log('1');
})()

// File 2
(function() {
  console.log('2');
})();
```

This works great when the files are served separately

```JS 
// Minified
(function(){console.log("1")})()(function(){console.log("2")})();
// Uncaught TypeError: undefined is not a function!
```

... wtf?

The lack of a semicolon at the end of the first file causes the two files to be concatentated together such that JS thinks the first function's returned value should be executed as a function.

 - Our first function returns nothing, `undefined`
 - `undefined` is not a function

All the author of file 1 had to do was include a `;`!

Note that the author of file 2 could have defended against this by including a `;` at the start of the file.

## The Solution

Use a linter. I strongly recomment JSHint. In fact if I could I'd mandate it's use company-wide.

It will tell you off for missing semicolons, using `==` instead of `===`, and for many tens of other mini-fails you do on a daily basis. I know this because it moans at me constantly.

If you think you can't use it, email me your IDE/editor of choice and I'll work with you to get a solution going. 
