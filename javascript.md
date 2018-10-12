## JavaScript

* JavaScript is compatible with ECMAScript, and it provides additional features.

| | | |
|-|-|-|
| ES6 | ES2015 | arrow functions, promises |
| ES7 | ES2016 | |
| ES8 | ES2017 | |

## node.js

* [node.js](https://nodejs.org/en/): JavaScript runtime built on Chrome's V8 JavaScript engine

* nvm: node version manager

* [npm](https://www.npmjs.com): node package manager

* [nvm installation](https://stackoverflow.com/questions/28017374/what-is-the-suggested-way-to-install-brew-node-js-io-js-nvm-npm-on-os-x)

* commands

```sh
# List installed versions (local)
$ nvm ls

## List remote versions available for install
$ nvm ls-remote
## When listing, only show LTS (long-term support) versions
$ nvm ls-remote --lts

## install latest lts
$ nvm install lts/* --reinstall-packages-from=node

## set default node version with NVM (Visual Studio Code refers to 'default')
$ nvm alias default v8.9.3

```

## Reference

* [w3schools, JavaScript Tutorial](https://www.w3schools.com/js/)
* [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS)

## JavaScript

```JS
# indicate that the code should be executed in "strict mode"
"use strict";

# 
```

