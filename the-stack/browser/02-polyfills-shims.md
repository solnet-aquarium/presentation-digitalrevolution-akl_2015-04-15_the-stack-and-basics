# PolyFills & Shims

Will save your life.

 - Code that implements native features of later versions of JS in pure JS, allowing you to code as if they exist even in older browsers
 - [What is a PolyFill](https://remysharp.com/2010/10/08/what-is-a-polyfill)
 
```JS
if(typeof Array.prototype.filter !== "function") {
  Array.prototype.filter = function() {
    // implementation filter functionality here
  };
}
```
 
## Difference between a PolyFill and a Shim
 
> Citing [Axel Rauschmayer](http://rauschma.de/) from his book [Speaking JavaScript](http://speakingjs.com/):
> > A shim is a library that brings a new API to an older environment, using only the means of that environment.
> > A polyfill is a shim for a browser API. It typically checks if a browser supports an API. If it doesn’t, the polyfill installs its own implementation. That allows you to use the API in either case.

From [Bergi's SO answer](http://stackoverflow.com/a/24391813)

 - Often the terms are used interchangeably.
 - Use [es5-shim](https://github.com/es-shims/es5-shim) for general ES5 features
 - Refer to [HTML5 Cross Browser Polyfills](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills)for other more niche features

## Shims and AngularJS

AngularJS 1.3+ dropped support for IE8. Older versions of AngularJS can be convinced to work in IE8 using various tricks

 - See the older versions of the [AngularJS IE guide](https://code.angularjs.org/1.2.27/docs/guide/ie) for details.
