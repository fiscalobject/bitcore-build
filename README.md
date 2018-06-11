# ufocore-build

A helper to add tasks to gulp.

## Getting started

Install with:

```sh
npm install ufocore-build
```

and use and require in your gulp file: 

```javascript
var gulp = require('gulp');
var ufocoreTasks = require('ufocore-build');

ufocoreTasks('submodule');
gulp.task('default', ['lint', 'test', 'browser', 'coverage']);
```

### Notes

* There's no default task to allow for each submodule to set up their own configuration
* If the module is node-only, avoid adding the browser tasks with:
```javascript
var ufocoreTasks = require('ufocore-build');
ufocoreTasks('submodule', {skipBrowsers: true});
```

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.
Copyright 2018 The UFO Core Developers
