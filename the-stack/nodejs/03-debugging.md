# Debugging

Write unit tests. Unit testing is very easy in node. Mostly, if your test is hard to write, your code needs to be split up some more.

You can get similar debug tools as those available in the browser by using [node-inspector](https://github.com/node-inspector/node-inspector)

```BASH
npm install -g node-inspector
git clone https://github.com/btford/angular-express-blog.git
cd angular-express-blog
npm install
node-debug -p 3001 app.js
```

 - Edit source files live
 - Breakpoints
 - Inspect call stack on breakpoint
 - Conditional breakpoints
 - Profiling
