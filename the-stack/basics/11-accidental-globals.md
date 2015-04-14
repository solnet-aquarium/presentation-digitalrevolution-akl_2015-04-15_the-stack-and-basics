# Accidental Globals

Use `var` when declaring your variables. Otherwise you're creating/overwriting a variable on the global scope.

```JS
var a = 'global';
console.log(a);
(function() {
  a = 'private';
})();
console.log(a);
```
 
Instead do this:

```JS
var a = 'global';
console.log(a);
(function() {
  var a = 'private';
})();
console.log(a);
```
