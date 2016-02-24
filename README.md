Table of Contents
=================

* [Markdown API](#markdown-api)
  * [Install](#install)
  * [Usage](#usage)
  * [API](#api)
    * [concat](#concat)
    * [print](#print)
    * [parse](#parse)
  * [Developer](#developer)
    * [Test](#test)
    * [Cover](#cover)
    * [Lint](#lint)
    * [Clean](#clean)
    * [Readme](#readme)

Markdown API
============

[<img src="https://travis-ci.org/tmpfs/mdapi.svg" alt="Build Status">](https://travis-ci.org/tmpfs/mdapi)
[<img src="http://img.shields.io/npm/v/mdapi.svg" alt="npm version">](https://npmjs.org/package/mdapi)
[<img src="https://coveralls.io/repos/tmpfs/mdapi/badge.svg?branch=master&service=github&v=1" alt="Coverage Status">](https://coveralls.io/github/tmpfs/mdapi?branch=master).

Quick and dirty (but effective) API comments to commonmark compliant markdown.

## Install

```
npm i mdapi
```

## Usage

mdapi [options] [files...]

  --level=[num] Initial heading level.

Report bugs to https://github.com/tmpfs/mdapi/issues.

## API

```javascript
var parse = require('mdapi');
parse(['index.js'], {stream: process.stdout});
```

### concat

```javascript
concat(files, output, cb)
```

Concatenate input files into a single string.

* files: List of input file to load.
* output: The output string.
* cb: Callback function.

### print

```javascript
print(ast, opts, cb)
```

Print the markdown from the parsed ast.

* ast: The parsed comments abstract syntax tree.
* opts: Parse options.
* cb: Callback function.

### parse

```javascript
parse(files, opts, cb)
```

Parse an array of files into a markdown string.

* files: List of files to parse.
* opts: Parse options.
* cb: Callback function.

## Developer

### Test

To run the test suite:

```
npm test
```

### Cover

To generate code coverage run:

```
npm run cover
```

### Lint

Run the source tree through [jshint](http://jshint.com) and [jscs](http://jscs.info):

```
npm run lint
```

### Clean

Remove generated files:

```
npm run clean
```

### Readme

To build the readme file from the partial definitions (requires [mdp](https://github.com/tmpfs/mdp)):

```
npm run readme
```

Generated by [mdp(1)](https://github.com/tmpfs/mdp).

[jshint]: http://jshint.com
[jscs]: http://jscs.info
[mdp]: https://github.com/tmpfs/mdp
