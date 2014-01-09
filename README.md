modern-web-dev-setup
====================

The technologies/tools/ideas involved would include but not be limited by

  * npm/Bower (a dependency/package manager)
  * ES6+
  * Web Components
  * File watching (compilation purposes)
  * Live Reload
  * Friendly to live development in the Browser/Browser as IDE.
  * HTTP 2.0/SPDY

Fallbacks for any environments that don't support the newest technologies will be required, these should not interfere with exploiting the full capabilities of the more up to date environments beyond the impossible to shim/compile/polyfill.

The structure should be build so it's decoupled so you can drop parts as you no longer need them (e.g. targeting only modern ES6 browsers drop the file watching of ES6 code to compile it to ES5).


Package Manager
---------------

What you want are all your dependencies being installed by one package manager, `npm` being the most popular one it seems a reasonable selection.

The problem is `npm` package dependencies are installed in a deep folder hierarchy.

With a set of client side dependencies avoiding loading in many instances of the same package would be a logical requirement.

So a flatter dependencies directory like one that `bower` would create is a requirement for using `npm` as a package manager.

This appears to be achievable if using `peerDependencies`, [explained here](http://domenic.me/2013/02/08/peer-dependencies/).

