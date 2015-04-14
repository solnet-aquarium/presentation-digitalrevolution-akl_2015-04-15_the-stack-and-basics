# Private Scopes

JS has scopes, starting with the global scope.

This means that unless you protect yourself, it's possible for scripts that exist outside your current files to intefere with your variables.

Instead of running naked through people's browsers, do this:

```JS
// global scope
(function() {
  // private scope
})();
// global scope
```

This is known as an "Immediately Invoked Function Expression" and is a very common way to create a private scope for your file.

I see this as so fundamental that it is the first thing I add when refactoring.

This will 

 - Help you think "modular"
 - Lay the groundwork for more "functional" approaches
 - Help towards grokking scopes in general

```JS
var a = 'global!';
console.log(a);
(function() {
  var a = 'private!';
  console.log(a);
})();
console.log(a);
```

Bottom line - protecting your privates is fundamental to overall health.
