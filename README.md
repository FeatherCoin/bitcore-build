# feathercore-build

A helper to add tasks to gulp.

## Getting started

Install with:

```sh
npm install feathercore-build
```

and use and require in your gulp file: 

```javascript
var gulp = require('gulp');
var feathercoreTasks = require('feathercore-build');

feathercoreTasks('submodule');
gulp.task('default', ['lint', 'test', 'browser', 'coverage']);
```

### Notes

* There's no default task to allow for each submodule to set up their own configuration
* If the module is node-only, avoid adding the browser tasks with:
```javascript
var feathercoreTasks = require('feathercore-build');
feathercoreTasks('submodule', {skipBrowsers: true});
```

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.
Copyright 2018 The Feathercoin Core Developers
