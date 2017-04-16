# api documentation for  [gulp-flatten (v0.3.1)](https://github.com/armed/gulp-flatten)  [![npm package](https://img.shields.io/npm/v/npmdoc-gulp-flatten.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-gulp-flatten) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-gulp-flatten.svg)](https://travis-ci.org/npmdoc/node-npmdoc-gulp-flatten)
#### remove or replace relative path for files

[![NPM](https://nodei.co/npm/gulp-flatten.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/gulp-flatten)

[![apidoc](https://npmdoc.github.io/node-npmdoc-gulp-flatten/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-gulp-flatten/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-gulp-flatten/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-gulp-flatten/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Artem Medeusheyev"
    },
    "bugs": {
        "url": "https://github.com/armed/gulp-flatten/issues"
    },
    "dependencies": {
        "gulp-util": "^3.0.7",
        "through2": "^2.0.0"
    },
    "description": "remove or replace relative path for files",
    "devDependencies": {
        "eslint-config-airbnb": "^1.0.2",
        "gulp": "^3.9.0",
        "mocha": "^2.3.4",
        "pre-commit": "^1.1.2",
        "should": "^7.1.1"
    },
    "directories": {},
    "dist": {
        "shasum": "51e7fec13a33c404578d18c1589d1b5bc45fe1d6",
        "tarball": "https://registry.npmjs.org/gulp-flatten/-/gulp-flatten-0.3.1.tgz"
    },
    "engines": {
        "node": ">=0.10"
    },
    "gitHead": "04c2b4625b947cd07acf6a924065eb13fe92f2ea",
    "homepage": "https://github.com/armed/gulp-flatten",
    "keywords": [
        "gulpplugin",
        "gulp",
        "flatten",
        "relative",
        "path"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "armed"
        }
    ],
    "name": "gulp-flatten",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/armed/gulp-flatten.git"
    },
    "scripts": {
        "test": "mocha -R spec"
    },
    "version": "0.3.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module gulp-flatten](#apidoc.module.gulp-flatten)
1.  [function <span class="apidocSignatureSpan"></span>gulp-flatten (opts)](#apidoc.element.gulp-flatten.gulp-flatten)
1.  [function <span class="apidocSignatureSpan">gulp-flatten.</span>toString ()](#apidoc.element.gulp-flatten.toString)



# <a name="apidoc.module.gulp-flatten"></a>[module gulp-flatten](#apidoc.module.gulp-flatten)

#### <a name="apidoc.element.gulp-flatten.gulp-flatten"></a>[function <span class="apidocSignatureSpan"></span>gulp-flatten (opts)](#apidoc.element.gulp-flatten.gulp-flatten)
- description and source-code
```javascript
gulp-flatten = function (opts) {
  opts = opts || {};
  opts.newPath = opts.newPath || '';

  return through2.obj(function(file, enc, next) {
    if (!file.isDirectory()) {
      try {
        file.path = path.join(file.base, opts.newPath, flattenPath(file, opts));
        this.push(file);
      } catch (e) {
        this.emit('error', new PluginError('gulp-flatten', e));
      }
    }
    next();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-flatten.toString"></a>[function <span class="apidocSignatureSpan">gulp-flatten.</span>toString ()](#apidoc.element.gulp-flatten.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
