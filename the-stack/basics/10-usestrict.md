# Use Strict

FYI JS has a "Strict Mode" and you should always use it!

The correct way to use it:

```JS
(function() {
  'use strict';
})();
```

Those who have been paying attention will notice the use of an IIFE.

A common usage that is dangerous:

```JS
// File 1
'use strict';

// File 2
```

What will happen when the two files are concatenated together?
