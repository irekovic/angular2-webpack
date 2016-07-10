# Modern JavaScript Development

## [Node](nodejs.org)

Prerequisite for all modern JavaScript development is local instance of node JavaScript runtime.

## [NPM](npmjs.com)

`npm` is package manager for java script modules. It is used together
with `nodejs` environment (virtual machine).

When starting a new java script project you would definetly want to
start with empty folder and first thing to type into terminal is:

	npm init

Than answer on the screen questions and you have just created your `package.json` file - that is roughly `pom.xml` for npm.

### [package.json](https://docs.npmjs.com/getting-started/using-a-package.json) file

Package json file has only two required fields: `name` and `version`.

**name**
* all lowercase
* one word, no spaces
* dashes and underscores allowed

**version**
* in the form of x.x.x
* follows [semver spec](https://docs.npmjs.com/getting-started/semantic-versioning)

So here it is - smallest valid `package.json` file:

	{
		"name": "my-app-name",
		"version": "1.0.0"
	}

Please note that version field requires `semantic version` number.

### installing dependencies

Dependencies can be installed globaly or localy

## [TypeScript](https://www.typescriptlang.org)

TypeScript is superset of JavaScript. It is in essence modern JS language with `types`. Also one usefull thing regarding typescript is that it makes gap between latest EcmaScript specification and actual implementation of javascript in browsers.

### [tsconfig.json](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html)

Presence of `tsconfig.json` file indicates that the folder is the root of typescript project.

## [Typings](https://github.com/typings/typings)

Since typescript is strict and statically typed language, if we want to
integrate with plain javascript libraries - we need to `declare` types used in sad libraries. This is the sole reason for typings tool to exist. To search and download *ambient type definitions* of external libraries.

More information about ambient type definitions can be found here:

* [Managing ambient type definitions and dealing with the "Duplicate identifier" TypeScript error](http://blog.mgechev.com/2016/03/28/ambient-type-definitions-duplicate-identifier-typescript-fix/)

## [webpack](http://webpack.github.io) module bundler

WebPack is a module bundler. It is a tool that will take your entry java script file and bundle it up together with all its dependencies in order to create single js file that can be used in browser or node environments.