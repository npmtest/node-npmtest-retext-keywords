# npmtest-retext-keywords

#### basic test coverage for  [retext-keywords (v4.0.0)](https://github.com/wooorm/retext-keywords#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-retext-keywords.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-retext-keywords) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-retext-keywords.svg)](https://travis-ci.org/npmtest/node-npmtest-retext-keywords)

#### Keyword extraction with Retext

[![NPM](https://nodei.co/npm/retext-keywords.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/retext-keywords)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-retext-keywords/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-retext-keywords/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-retext-keywords/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-retext-keywords/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-retext-keywords/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-retext-keywords/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-retext-keywords/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-retext-keywords/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-retext-keywords/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-retext-keywords/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-retext-keywords/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-retext-keywords/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-retext-keywords/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-retext-keywords/build/test-report.html](https://npmtest.github.io/node-npmtest-retext-keywords/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-retext-keywords/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-retext-keywords/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-retext-keywords/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-retext-keywords/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-retext-keywords/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-retext-keywords/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-retext-keywords/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-retext-keywords/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Titus Wormer",
        "url": "http://wooorm.com"
    },
    "bugs": {
        "url": "https://github.com/wooorm/retext-keywords/issues"
    },
    "contributors": [
        {
            "name": "Titus Wormer",
            "url": "http://wooorm.com"
        },
        {
            "name": "Vladimir Starkov"
        }
    ],
    "dependencies": {
        "has": "^1.0.1",
        "nlcst-to-string": "^2.0.0",
        "retext-pos": "^2.0.0",
        "stemmer": "^1.0.0",
        "unist-util-visit": "^1.0.0"
    },
    "description": "Keyword extraction with Retext",
    "devDependencies": {
        "browserify": "^14.1.0",
        "esmangle": "^1.0.1",
        "nyc": "^10.0.0",
        "remark-cli": "^3.0.0",
        "remark-preset-wooorm": "^2.0.0",
        "retext": "^5.0.0",
        "tape": "^4.0.0",
        "xo": "^0.17.1"
    },
    "directories": {},
    "dist": {
        "shasum": "11ed5b73ed2906d34d32730e4e05ac5c5fa5a6d1",
        "tarball": "https://registry.npmjs.org/retext-keywords/-/retext-keywords-4.0.0.tgz"
    },
    "files": [
        "index.js"
    ],
    "gitHead": "1fe1d9014742867e52c6bcf77d174ccba702fe95",
    "homepage": "https://github.com/wooorm/retext-keywords#readme",
    "keywords": [
        "keyword",
        "phrase",
        "terminology",
        "term",
        "extraction",
        "retext"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "wooorm"
        }
    ],
    "name": "retext-keywords",
    "nyc": {
        "check-coverage": true,
        "lines": 100,
        "functions": 100,
        "branches": 100
    },
    "optionalDependencies": {},
    "remarkConfig": {
        "plugins": [
            "preset-wooorm"
        ]
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/wooorm/retext-keywords.git"
    },
    "scripts": {
        "build": "npm run build-md && npm run build-bundle && npm run build-mangle",
        "build-bundle": "browserify index.js --ignore-missing --bare -s retextKeywords > retext-keywords.js",
        "build-mangle": "esmangle retext-keywords.js > retext-keywords.min.js",
        "build-md": "remark . --quiet --frail",
        "lint": "xo",
        "test": "npm run build && npm run lint && npm run test-coverage",
        "test-api": "node test.js",
        "test-coverage": "nyc --reporter lcov tape test.js"
    },
    "version": "4.0.0",
    "xo": {
        "space": true,
        "rules": {
            "no-negated-condition": "off",
            "guard-for-in": "off",
            "max-lines": "off",
            "max-nested-callbacks": "off"
        },
        "ignores": [
            "retext-keywords.js"
        ]
    },
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
