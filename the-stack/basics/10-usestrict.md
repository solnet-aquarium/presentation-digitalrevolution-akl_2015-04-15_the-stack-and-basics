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

## What `use strict` does

Great list over at [Strict Mode (JavaScript)](https://msdn.microsoft.com/en-us/library/ie/br230269(v=vs.94).aspx)

## Caution!

**Do not apply strict mode to existing code unless you are absolutely certain the code confirms properly.
