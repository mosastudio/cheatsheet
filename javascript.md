## JavaScript

* JavaScript is compatible with ECMAScript, and it provides additional features. [Wiki](https://en.wikipedia.org/wiki/ECMAScript)

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

* command line

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
// indicate that the code should be executed in "strict mode"
"use strict";

// check if an object has a key, https://stackoverflow.com/questions/455338/how-do-i-check-if-an-object-has-a-key-in-javascript
if ('key' in myObj) {}
if (myObj.hasOwnProperty('key')) {}

// get array of keys
Object.keys(obj)

// deep copy, an array
Object.assign([], nums)

// deep copy, an object
Object.assign({}, obj)

// new
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

var boy = new Person('Johnny', 'Jackson');

console.log(JSON.stringify(boy)); // {"firstName":"Johnny","lastName":"Jackson"}

// sort
var nums = [1, 3, 7, 4, 12, 120, 5, 13];

// default, convert to string, and then comapre
nums.sort();
console.log(JSON.stringify(nums)); // [1,12,120,13,3,4,5,7]

// ascending, return value < 0 => index of a < index of b
nums.sort(function(a, b) {
    return a - b;
});
console.log(JSON.stringify(nums)); // [1,3,4,5,7,12,13,120]
```

## conversion

```JS
// string to integer
parseInt(string, radix)

// string to floating point number
parseFloat(string)
```

## Array

|property/method|description|
|-|-|
|length|the number of elements||
|filter()|create a new array, pass a test|
|reverse()|reverse the order|
|join()|join all -> a string|
|concat()|join all -> create a new array|
|splice()|Adds or Removes elements, it will change the original array|

## JSON

|property/method|description|
|-|-|
|JSON.parse(string)|data (a string) -> JavaScript object|
|JSON.stringify(obj)|data (a string) <- JavaScript object|

## Math

|property/method|description|
|-|-|
|Math.floor()||
|Math.ceil()||
|Math.sqrt()||
|Math.max(n1, n2, n3, ..., nX)||
|Math.min(n1, n2, n3, ..., nX)||

## Number

|property/method|description|
|-|-|
|Number.isInteger(value)||
|Number.MAX_SAFE_INTEGER||
|num.toString(radix)||

## String

* All string methods return a new value. They do not change the original variable.

|property/method|description|
|-|-|
|split(separator, limit)||
|indexOf()|Returns the position of the first found occurrence of a specified value in a string|
|lastIndexOf()|Returns the position of the last found occurrence of a specified value in a string|
|substr(start, length)||
|toLocaleLowerCase()
toLocaleUpperCase()
toLowerCase()
toUpperCase()||
|localeCompare(compareString)|result of "abb".localeCompare("baa”); is -1|

```js
function countSubString(string) {
  array = string.split(" ");
  console.log(array.length);
}

countSubString(" ");  // 2
countSubString("  ");  // 3
countSubString("1");  // 1
countSubString(" 1");  // 2
countSubString("1 ");  // 2
countSubString(" 1 ");  // 3
```

