# Package Management

Reduces / removes "Dependecy Hell"

 > Dependency hell is a colloquial term for the frustration of some software users who have installed software packages which have dependencies on specific versions of other software packages.[1](dependency-hell)

 -- Michael Jang (2006). Linux annoyances for geeks. O'Reilly Media. ISBN 9780596552244. Retrieved 2012-02-16.
 
## Why?

There is an amazing amount of quality free code out there. You should use it.

 - Package managers simplify integration of this code with your project.
 - Package managers make it easy for other people to realise your shining brilliance by using your freely given code

## Which one?

There are quite a few to choose from now. Aren't you lucky.

 - **bower**
 - *npm with browserify*
 - *jspm*

From [Frontend packagers](https://github.com/wilmoore/frontend-packagers).

### Bower 

You've probably heard of it.

 - Installable via `npm install -g bower`
 - Used with `bower install`

#### Main Points

 - Front end only
 - Handles CSS, HTML and JS
 - Massive number of available libraries
 - Can use raw git repositories
 - Can use local filesystem
 - Can be used alongside npm
 - Very easy to find, use and create bower libraries
 - Must manually include bower libraries in your projects - no automatic module loading like npm + browserify or jspm

Reads from a `bower.json` file, e.g.

```JSON
{
  "name": "sn-capitalise",
  "main": "src/sn-capitalise.js",
  "version": "0.0.1",
  "homepage": "https://github.com/solnetdigital/sn-capitalise",
  "authors": [
    "michael.robinson@solnet.co.nz"
  ],
  "description": "Angular JS filter for word capitalisation",
  "license": "MIT",
  "devDependencies": {
    "angular": "~1.3.4",
    "angular-mocks": "*"
  }
}
```

### NPM + Browserify

Allows use of npm (node.js) modules in the browser.

Might cover this in a later presentation.

### JSPM

Apparently "THE" JS 6 package manager
