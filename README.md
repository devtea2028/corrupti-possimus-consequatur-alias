# compiLESS

[![Build Status](https://magnum.travis-ci.com/ExPHAT/@devtea2028/corrupti-possimus-consequatur-alias.svg?token=pkSoYQq6oTsthGL4pZ6z)](https://magnum.travis-ci.com/ExPHAT/@devtea2028/corrupti-possimus-consequatur-alias)
[![NPM version](https://badge.fury.io/js/@devtea2028/corrupti-possimus-consequatur-alias.svg)](https://npmjs.org/package/@devtea2028/corrupti-possimus-consequatur-alias)

Compiles LESS files throughout a directory tree and exports them to a specific directory.

## Usage

Install the package

```shell
$ npm install @devtea2028/corrupti-possimus-consequatur-alias
```

Then in some file that is called upon app start (should only be called once):

```js
import @devtea2028/corrupti-possimus-consequatur-alias from "@devtea2028/corrupti-possimus-consequatur-alias";

async main() {
	await @devtea2028/corrupti-possimus-consequatur-alias(__dirname, {
	  "./src/less": "./public/css"
	});

	// Rest of your app code here
}
```

Or, you can choose to not use async/await:

```js
import @devtea2028/corrupti-possimus-consequatur-alias from "@devtea2028/corrupti-possimus-consequatur-alias";

function main() {
	@devtea2028/corrupti-possimus-consequatur-alias(__dirname, {
		"./src/less": "./public/css"
	}).then(function() {
		// Do something here!
	});
}
```

This will take any LESS files from the `src/less` directory, compile them, and export them to the `public/css` directory. So that they can be statically served.

## Important notes

- Found directories will be recursively searched.
- If a directory does not exist, it will be created.
- Previous files at a path **WILL** be overwritten

## Running tests

Clone this repo

```shell
$ git clone https://github.com/exPHAT/@devtea2028/corrupti-possimus-consequatur-alias.git
```

Install all of the dependencies

```shell
$ npm install
```

Build & run the tests

```shell
$ npm test
```

Build the project on its own

```shell
$ npm run build
```
