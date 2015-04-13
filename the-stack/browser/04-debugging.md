# Debugging

Unless your bug is apparent only in a particular browser, use Chrome.

Use Chrome.

Chrome.

## Chrome

Chrome ships with powerful development tools. I can't profess I completely grok all of them, and I'm sure there are corners I haven't even looked into yet.

Strongly recommend bookmarking the [Chrome devtools site](https://developer.chrome.com/devtools).

## The console (console tab)

### Golden rules

 - If you think you have a problem, open the console
 - Do not ask for help unless you have looked at the console
 - Keep the console open at all times
 - Seriously, the console
 - If anyone asks you for help and they don't have the console open, ask "Why isn't the console open"?

## Live editing of files (sources tab)

You can edit the JavaScript files powering a website and have the changes applied **without needing to reload the page**.  This can be extremely helpful when

 - attempting to debug why the hell x does y at the end of a very long click chain
 - attempting to help someone debug without needing access to the source code
 - looking good in a presentation
 - debugging an issue that occurs only in an environment you cannot constantly push tiny updates to (test/prod)

## Profiling performance

See [Chrome DevTools performance](https://developer.chrome.com/devtools/docs/network) section for in-depth tutorials on this. 
Profile memory, network, JS performance.

## Inspecting elements

You should know about this already!

Some hidden-in-plain-sight features:

### Inspect event listeners

See a list of events and functions that have been bound to them

### Inspect DOM breakpoints
 
 > If you know your page is breaking when a certain part of the DOM changes, or you just want to find out what script is responsible for changing an elements attributes or children, Chrome and Firebug both allow you to set a breakpoint on DOM modification allowing you to find the culprit in your code. Simply highlight the element you want to monitor and right click to select the conditions to break on.

[Secrets of the Browser Developer Tools](http://devtoolsecrets.com/secret/debugging-dom-breakpoints.html)
