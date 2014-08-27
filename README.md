static-reference
================
Annotate file references within the source code of your node packages. These references can be scanned for using the dependency graph of a module. This package only defines the reference itself, other modules are used to scan your source code for this annotation (such as _module-references_ [npm](https://www.npmjs.org/package/module-references) [github](https://github.com/Joris-van-der-Wel/node-module-references) ).

usage
-----
```javascript
require('static-reference')('./foo.css');
require('static-reference')("./foo.less");
require('static-reference')('./foo-mobile.css', 'mobile');
```
Only a string literal will work properly, for example `require('static-reference')('./foo' + '.css');` will be ignored. The require call is looked for while parsing your source code, the call has no effect at runtime. `require('static-reference')` will always return a dummy function that performs no operations.
