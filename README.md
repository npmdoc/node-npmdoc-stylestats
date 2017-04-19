# npmdoc-stylestats

#### api documentation for  [stylestats (v7.0.1)](http://www.stylestats.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-stylestats.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-stylestats) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-stylestats.svg)](https://travis-ci.org/npmdoc/node-npmdoc-stylestats)

#### StyleStats is a small library to collect CSS statistics!

[![NPM](https://nodei.co/npm/stylestats.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/stylestats)

- [https://npmdoc.github.io/node-npmdoc-stylestats/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-stylestats/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-stylestats/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-stylestats/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-stylestats/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-stylestats/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Koji Ishimoto"
    },
    "ava": {
        "require": [
            "babel-register"
        ]
    },
    "babel": {
        "presets": [
            "es2015"
        ],
        "plugins": [
            "transform-runtime"
        ],
        "ignore": "test/*.js",
        "env": {
            "development": {
                "sourceMaps": "inline"
            }
        }
    },
    "bin": {
        "stylestats": "bin/cli.js"
    },
    "bugs": {
        "url": "https://github.com/t32k/stylestats/issues"
    },
    "contributors": [
        {
            "name": "1000ch"
        }
    ],
    "dependencies": {
        "chalk": "^1.1.3",
        "cheerio": "^0.22.0",
        "cli-table": "^0.3.1",
        "commander": "^2.9.0",
        "css": "^2.2.1",
        "glob": "^7.1.1",
        "gzip-size": "^3.0.0",
        "handlebars": "^4.0.6",
        "json2csv": "^3.7.3",
        "moment": "^2.18.1",
        "numeral": "^2.0.4",
        "request": "^2.81.0",
        "valid-url": "^1.0.9"
    },
    "description": "StyleStats is a small library to collect CSS statistics!",
    "devDependencies": {
        "ava": "^0.18.2",
        "babel-plugin-transform-runtime": "^6.23.0",
        "babel-preset-es2015": "^6.24.0",
        "coveralls": "^2.12.0",
        "nyc": "^10.1.2",
        "watch": "^1.0.2",
        "xo": "^0.18.0"
    },
    "directories": {},
    "dist": {
        "shasum": "e31801f6785adcdbf3174d2dfd65305fd5b661e6",
        "tarball": "https://registry.npmjs.org/stylestats/-/stylestats-7.0.1.tgz"
    },
    "engines": {
        "node": ">=6.x"
    },
    "files": [
        "lib",
        "bin",
        "assets"
    ],
    "gitHead": "2d30c0360473b8a957537615a5e68cf3c13f7ac6",
    "homepage": "http://www.stylestats.org",
    "keywords": [
        "css",
        "stylesheet",
        "performance",
        "property"
    ],
    "license": "MIT",
    "main": "lib/stylestats.js",
    "maintainers": [
        {
            "name": "t32k"
        },
        {
            "name": "1000ch"
        }
    ],
    "name": "stylestats",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/t32k/stylestats.git"
    },
    "scripts": {
        "lint": "xo",
        "test": "xo && ava",
        "watch": "watch 'npm run lint'"
    },
    "version": "7.0.1",
    "xo": {
        "space": true,
        "esnext": true
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
