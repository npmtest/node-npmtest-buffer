# npmtest-buffer

#### basic test coverage for  [buffer (v5.0.6)](https://github.com/feross/buffer)  [![npm package](https://img.shields.io/npm/v/npmtest-buffer.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-buffer) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-buffer.svg)](https://travis-ci.org/npmtest/node-npmtest-buffer)

#### Node.js Buffer API, for the browser

[![NPM](https://nodei.co/npm/buffer.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/buffer)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-buffer/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-buffer/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-buffer/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-buffer/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-buffer/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-buffer/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-buffer/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-buffer/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-buffer/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-buffer/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-buffer/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-buffer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-buffer/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-buffer/build/test-report.html](https://npmtest.github.io/node-npmtest-buffer/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-buffer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-buffer/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-buffer/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-buffer/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-buffer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-buffer/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-buffer/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-buffer/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Feross Aboukhadijeh",
        "url": "http://feross.org"
    },
    "bugs": {
        "url": "https://github.com/feross/buffer/issues"
    },
    "contributors": [
        {
            "name": "Romain Beauxis"
        },
        {
            "name": "James Halliday"
        }
    ],
    "dependencies": {
        "base64-js": "^1.0.2",
        "ieee754": "^1.1.4"
    },
    "description": "Node.js Buffer API, for the browser",
    "devDependencies": {
        "benchmark": "^2.0.0",
        "browserify": "^14.0.0",
        "concat-stream": "^1.4.7",
        "hyperquest": "^2.0.0",
        "is-buffer": "^1.1.1",
        "is-nan": "^1.0.1",
        "split": "^1.0.0",
        "standard": "*",
        "tape": "^4.0.0",
        "through2": "^2.0.0",
        "uglify-js": "^2.7.3",
        "zuul": "^3.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "2ea669f7eec0b6eda05b08f8b5ff661b28573588",
        "tarball": "https://registry.npmjs.org/buffer/-/buffer-5.0.6.tgz"
    },
    "gitHead": "cf0c27e9bc645fdcfeefaac9f8da0172475a5277",
    "homepage": "https://github.com/feross/buffer",
    "jspm": {
        "map": {
            "./index.js": {
                "node": "@node/buffer"
            }
        }
    },
    "keywords": [
        "arraybuffer",
        "browser",
        "browserify",
        "buffer",
        "compatible",
        "dataview",
        "uint8array"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "feross"
        }
    ],
    "name": "buffer",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/feross/buffer.git"
    },
    "scripts": {
        "perf": "browserify --debug perf/bracket-notation.js > perf/bundle.js && open perf/index.html",
        "perf-node": "node perf/bracket-notation.js && node perf/concat.js && node perf/copy-big.js && node perf/copy.js && node perf/new-big.js && node perf/new.js && node perf/readDoubleBE.js && node perf/readFloatBE.js && node perf/readUInt32LE.js && node perf/slice.js && node perf/writeFloatBE.js",
        "size": "browserify -r ./ | uglifyjs -c -m | gzip | wc -c",
        "test": "standard && node ./bin/test.js",
        "test-browser-es5": "zuul --ui tape -- test/*.js",
        "test-browser-es5-local": "zuul --ui tape --local -- test/*.js",
        "test-browser-es6": "zuul --ui tape -- test/*.js test/node/*.js",
        "test-browser-es6-local": "zuul --ui tape --local -- test/*.js test/node/*.js",
        "test-node": "tape test/*.js test/node/*.js",
        "update-authors": "./bin/update-authors.sh"
    },
    "standard": {
        "ignore": [
            "test/node/**/*.js",
            "test/_polyfill.js",
            "perf/**/*.js"
        ]
    },
    "version": "5.0.6",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
