# npmdoc-fs-extra

#### api documentation for  [fs-extra (v2.1.2)](https://github.com/jprichardson/node-fs-extra)  [![npm package](https://img.shields.io/npm/v/npmdoc-fs-extra.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-fs-extra) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fs-extra.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fs-extra)

#### fs-extra contains methods that aren't included in the vanilla Node.js fs package. Such as mkdir -p, cp -r, and rm -rf.

[![NPM](https://nodei.co/npm/fs-extra.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/fs-extra)

- [https://npmdoc.github.io/node-npmdoc-fs-extra/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-fs-extra/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fs-extra/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fs-extra/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-fs-extra/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-fs-extra/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "JP Richardson"
    },
    "bugs": {
        "url": "https://github.com/jprichardson/node-fs-extra/issues"
    },
    "dependencies": {
        "graceful-fs": "^4.1.2",
        "jsonfile": "^2.1.0"
    },
    "description": "fs-extra contains methods that aren't included in the vanilla Node.js fs package. Such as mkdir -p, cp -r, and rm -rf.",
    "devDependencies": {
        "coveralls": "^2.11.2",
        "istanbul": "^0.4.5",
        "klaw": "^1.0.0",
        "klaw-sync": "^1.1.2",
        "minimist": "^1.1.1",
        "mocha": "^3.1.2",
        "proxyquire": "^1.7.10",
        "read-dir-files": "^0.1.1",
        "rimraf": "^2.2.8",
        "secure-random": "^1.1.1",
        "standard": "^8.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "046c70163cef9aad46b0e4a7fa467fb22d71de35",
        "tarball": "https://registry.npmjs.org/fs-extra/-/fs-extra-2.1.2.tgz"
    },
    "gitHead": "84717b8d03f04785124604a119a9a6769f608853",
    "homepage": "https://github.com/jprichardson/node-fs-extra",
    "keywords": [
        "fs",
        "file",
        "file system",
        "copy",
        "directory",
        "extra",
        "mkdirp",
        "mkdir",
        "mkdirs",
        "recursive",
        "json",
        "read",
        "write",
        "extra",
        "delete",
        "remove",
        "touch",
        "create",
        "text",
        "output",
        "move"
    ],
    "license": "MIT",
    "main": "./lib/index",
    "maintainers": [
        {
            "name": "jprichardson"
        },
        {
            "name": "ryanzim"
        }
    ],
    "name": "fs-extra",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/jprichardson/node-fs-extra.git"
    },
    "scripts": {
        "coverage": "istanbul cover -i 'lib/**' -x '**/__tests__/**' test.js",
        "coveralls": "npm run coverage && coveralls < coverage/lcov.info",
        "lint": "standard",
        "test": "npm run lint && npm run unit",
        "test-find": "find ./lib/**/__tests__ -name *.test.js | xargs mocha",
        "unit": "node test.js"
    },
    "version": "2.1.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
