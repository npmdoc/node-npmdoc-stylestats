# api documentation for  [stylestats (v7.0.1)](http://www.stylestats.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-stylestats.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-stylestats) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-stylestats.svg)](https://travis-ci.org/npmdoc/node-npmdoc-stylestats)
#### StyleStats is a small library to collect CSS statistics!

[![NPM](https://nodei.co/npm/stylestats.png?downloads=true)](https://www.npmjs.com/package/stylestats)

[![apidoc](https://npmdoc.github.io/node-npmdoc-stylestats/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-stylestats_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-stylestats/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-stylestats/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-stylestats/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Koji Ishimoto",
        "email": "ijok.ijok@gmail.com"
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
            "name": "1000ch",
            "email": "shogo.sensui@gmail.com"
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
            "name": "t32k",
            "email": "ijok.ijok@gmail.com"
        },
        {
            "name": "1000ch",
            "email": "shogo.sensui@gmail.com"
        }
    ],
    "name": "stylestats",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module stylestats](#apidoc.module.stylestats)
1.  object <span class="apidocSignatureSpan">stylestats.</span>util

#### [module stylestats.util](#apidoc.module.stylestats.util)
1.  [function <span class="apidocSignatureSpan">stylestats.util.</span>isCSS (str)](#apidoc.element.stylestats.util.isCSS)
1.  [function <span class="apidocSignatureSpan">stylestats.util.</span>isDirectory (dir)](#apidoc.element.stylestats.util.isDirectory)
1.  [function <span class="apidocSignatureSpan">stylestats.util.</span>isFile (file)](#apidoc.element.stylestats.util.isFile)
1.  [function <span class="apidocSignatureSpan">stylestats.util.</span>isFunction {{signature}}](#apidoc.element.stylestats.util.isFunction)
1.  [function <span class="apidocSignatureSpan">stylestats.util.</span>isObject ((type === 'object')](#apidoc.element.stylestats.util.isObject)



# <a name="apidoc.module.stylestats"></a>[module stylestats](#apidoc.module.stylestats)



# <a name="apidoc.module.stylestats.util"></a>[module stylestats.util](#apidoc.module.stylestats.util)

#### <a name="apidoc.element.stylestats.util.isCSS"></a>[function <span class="apidocSignatureSpan">stylestats.util.</span>isCSS (str)](#apidoc.element.stylestats.util.isCSS)
- description and source-code
```javascript
str => {
  try {
    return css.parse(str) instanceof Object;
  } catch (err) {
    return false;
  }
}
```
- example usage
```shell
...
  throw new Error('Argument is invalid');
}

// Requests to stylesheet defined in html
const requestPromisesInner = [];

results.forEach(result => {
  if (util.isCSS(result)) {
    that.styles.push(result);
  } else {
    // Push remote css data
    const type = result.headers['content-type'];
    if (type.indexOf('html') > -1) {
      // Parse result body
      const $ = cheerio.load(result.body);
...
```

#### <a name="apidoc.element.stylestats.util.isDirectory"></a>[function <span class="apidocSignatureSpan">stylestats.util.</span>isDirectory (dir)](#apidoc.element.stylestats.util.isDirectory)
- description and source-code
```javascript
dir => {
  try {
    return fs.existsSync(dir) && fs.statSync(dir).isDirectory();
  } catch (err) {
    return false;
  }
}
```
- example usage
```shell
...
/**
 * Argument is directory path or not
 * @param {String} dir
 * @returns {Boolean}
 */
isDirectory: dir => {
  try {
    return fs.existsSync(dir) && fs.statSync(dir).isDirectory();
  } catch (err) {
    return false;
  }
},
/**
 * Argument is CSS or not
 * @param {String} str
...
```

#### <a name="apidoc.element.stylestats.util.isFile"></a>[function <span class="apidocSignatureSpan">stylestats.util.</span>isFile (file)](#apidoc.element.stylestats.util.isFile)
- description and source-code
```javascript
file => {
  try {
    return fs.existsSync(file) && fs.statSync(file).isFile();
  } catch (err) {
    return false;
  }
}
```
- example usage
```shell
...
/**
 * Argument is file path or not
 * @param {String} file
 * @returns {Boolean}
 */
isFile: file => {
  try {
    return fs.existsSync(file) && fs.statSync(file).isFile();
  } catch (err) {
    return false;
  }
},
/**
 * Argument is directory path or not
 * @param {String} dir
...
```

#### <a name="apidoc.element.stylestats.util.isFunction"></a>[function <span class="apidocSignatureSpan">stylestats.util.</span>isFunction {{signature}}](#apidoc.element.stylestats.util.isFunction)
- description and source-code
```javascript
fn => {
  return typeof fn === 'function' || false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylestats.util.isObject"></a>[function <span class="apidocSignatureSpan">stylestats.util.</span>isObject ((type === 'object')](#apidoc.element.stylestats.util.isObject)
- description and source-code
```javascript
obj => {
  const type = typeof obj;
  return type === 'function' || ((type === 'object') && Boolean(obj));
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
