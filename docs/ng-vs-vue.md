
comparison ng vs. vue
=====================

this document summarizes some facts about [ng]() vs [vue](https://vuejs.org/) - largely uncommented.
see also the (quite fair) [framework comparison the vue site](https://vuejs.org/v2/guide/comparison.html),

performance
-----------

as also mentioned in the comparison on the vue site, there is no significant performance
difference that suggests prefering one over the other, see [this benchmark](http://www.stefankrause.net/js-frameworks-benchmark7/table.html).

features (without any claim to completeness)
--------------------------------------------

both frameworks have the following features:

* components with shadow dom and shaded css
* html templates
* two-way binding
* routing (with parameters and guards)
* lazy loading components
* custom directives and pipes (aka filters)
* state management (ng: a simple service must be created / vue: vuex)
* i18n (plugins - ng native i18n cannot switch language at runtime as of now)
* cli (several commands for ng / only template based init for vue)
* webpack build (minified and uglified)
* test support (unit + e2e)
* use of autoprefix
* dev server with hot reload
* devtools in browsers and IDEs
* support for [sass/scss](http://sass-lang.com/)
* support for [bootstrap 4](https://getbootstrap.com/) available

observed differences (again without any claim to completeness)
--------------------------------------------------------------

* cli init: ng has a fixed template, vue uses editable templates from git repos or local filesystem
* language: ng uses typically typescript, vue uses es 6 (can also use es 5) - both can actually be configured to use various languages that compile to some sort of javascript
* webpack: with ng cli opaque (no access of webpack.config), explicit in vue (fully featured webpack)
* cli supported testing: ng uses karma and protractor, vue can use jest or karma/mocha for unit tests and nightwatch for e2e
* dependency injectoin: built-in in ng, on foot in vue (can largely be managed using the top-level app component and/or global state)
* learning curve: ng - steep / vue - less steep (imho)

sizes and build time (after init with respective cli)
-----------------------------------------------------

ng init (v. 1.6.5): `$ ng new landing -v -sg -sc -dir . --routing -style scss`
vue init (v. 2.9.2): `$ vue init webpack landing` (with eslint, jest and nightwatch)

|  | ng | vue |
|---|---:|---:|
| sources | 279 kB | 320 kB |
| node_modules | 271 MB | 134 MB |
| prod build w maps | n/a | 687 kB |
| prod build w/o maps | 299 kB | 132 kB |
| build time | 19.385s | 8.58s |
