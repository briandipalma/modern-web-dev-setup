modern-web-dev-setup
====================

The technologies/tools/ideas involved would include but not be limited by

  * ES6+
  * HTTP 2.0/SPDY
  * Bower (or some package manager)
  * Web Components
  * File watching (compilation purposes)
  * Live Reload
  * Friendly to live development in the Browser/Browser as IDE.

Fallbacks for any environments that don't support the newest technologies will be required, these should not interfere with exploiting the full capabilities of the more up to date environments beyond the impossible to shim/compile/polyfill.

The structure should be build so it's decoupled so you can drop parts as you no longer need them (targeting only modern ES6 browsers drop the file watching of ES6 code to compile it to ES5).
