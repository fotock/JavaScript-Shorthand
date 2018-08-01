
## Assign variables
```javascript
// Longhand
var a = 1;
var b = 1;
var c = 1;
var d = 2;
var e = 3;
var f;

// Shorthand
var a = b = c = 1, d = 2, e = 3, f;
```

## Decimal numbers
```javascript
// Longhand
var a = 100000000

// Shorthand
var a = 1e8
```

## Increment, decrement
```javascript
// Longhand
i = i + 1

// Shorthand
i++
```

## Add, distract, multiply, divide
```javascript
// Longhand
i = i + 5;
j = j - 3;
k = k * 10;
l = l / 2;

// Shorthand
i += 5;
j -= 3;
k *= 10;
l /= 2;
```

## Logical AND
```javascript
// Longhand
if (a > 10) {
   doSomething();
}

// Shorthand
a > 10 && doSomething();
```

## Logical OR
```javascript
// Longhand
if (a !== null || a !== undefined || a !== '') {
     let b = a
}

// Shorthand
let b = a  || 'new'
```

## Declare an associative array
```javascript
// Longhand
var arr = new Array()
arr["Susan Lee"] = "Philadelphia"
arr["Clint Ford"] = "San Francisco"
arr["Leo Benz"] = "Seatle"
arr["Sophia Loren"] = "Rome"
arr["Tom Johnson"] = "Stockholm"

// Shorthand
var myArray  = {
  "Susan Lee": "Philadelphia",
  "Clint Ford": "San Francisco",
  "Leo Benz": "Seatle",
  "Sophia Loren": "Rome",
  "Tom Johnson": "Stockholm"
}
```

## Declare an object
```javascript
// Longhand
var obj = new Object()
obj.name = "Shelley Shyan"
obj.placeOfBirth = "Beijing"
obj.age = 16
obj.wasJamesBond = true

// Shorthand
var obj = { 
  name: "Shelley Shyan", 
  placeOfBirth: "Beijing",
  age: 16, 
  wasJamesBond: true 
}
```

## Object properties
```javascript
// Longhand
const obj = { x:x, y:y };

// Shorthand
const obj = { x, y };
```

## Determine character position
```javascript
// Longhand
"myString".charAt(4)

// Shorthand
"myString"[4]
```

## Ternary operator
```javascript
// Longhand
let x = 20
let y
if (x > 10) {
    y = 'greater than 10'
} else {
    y = 'less than 10'
}

// Shorthand
let y = x > 10 ? 'greater than 10' : 'less than 10'
let y = x > 10 ? 'greater than 10' : x 
```

## if evaluation
```javascript
// Longhand
if (isPresent === true) {}
if (isPresent !== true) {}

// Shorthand
if (isPresent) {}
if (!isPresent) {}
```

## if conditions
```javascript
// Longhand
let host;
if (process.env.HOST) {
  host = process.env.HOST;
} else {
  host = 'localhost';
}

// Shorthand
const host = process.env.HOST || 'localhost';
```

## for loop
```javascript
// Longhand
for (let i = 0; i < myArray.length; i++)

// Shorthand
for (let i of myArray)
```

## Spread operator
```javascript
const odd = [1, 3, 5, 7];
const arr = [1, 2, 3, 4];

// ----- Longhand ----- 
// joining arrays
const nums = [2, 4, 6, 8].concat(odd);
// cloning arrays
const arr2 = arr.slice()


// ----- Shorthand ----- 
// joining arrays
const nums = [2 ,4, 6, 8, ...odd];
// cloning arrays
const arr2 = [...arr];

const nums = [2, ...odd, 4, 6, 8];
```


## Array lookup
```javascript
// Longhand
if (array.indexOf(item) >= -1) {
  doSomething();
}

// Shorthand
if (~array.indexOf(item)) {
  doSomething();
}

// The ~ operator will return a truthy value for anything but -1
```

## Double bitwise NOT
```javascript
// Longhand
Math.floor(1.8) === 1  //true

// Shorthand
~~1.8 === 1  //true
```

## Coercing a string into a number
```javascript
// Longhand
var a = parseFloat("12536.78");
var b = parseInt("12546", 10);

// Shorthand
var c = +"12536";
```

## Coercing a number into a string
```javascript
// Longhand
var a = 123.45;
var b = a.toString(10);

// Shorthand
var c = 1234 + '';
a += '';
```

## Coercing a value into a boolean
```javascript
// Longhand
var a = Boolean(expression);

// Shorthand
var a = !!expression;
```

## RegExp object
```javascript
// Longhand
let re = new RegExp("\d+(.)+\d+","igm")
let result = re.exec("pad 321 word text 87662 padding")

// Shorthand
let result = /d+(.)+d+/igm.exec("pad 321 word text 87662 padding")
```

## Call functions
```javascript
function x() {
  console.log('x')
}

function y() {
  console.log('y')
}

let z = 3;

// Longhand
if (z == 3) {
  x();
} else {
  y();
}

// Shorthand
(z == 3 ? x : y)();
```

## Arrow functions
```javascript
// Longhand
function sayHi(username) {
  console.log('Hi', username);
}

setTimeout(function() {
  console.log('Done')
}, 4500);

listArr.forEach(function(item) {
  console.log(item);
});

// Shorthand
sayHi = username => console.log('Hi', username);
setTimeout(() => console.log('Done'), 4500);
listArr.forEach(item => console.log(item));
```

## Implicit function return
```javascript
// Longhand
function getCircumference(diameter) {
  return Math.PI * diameter
}

// Shorthand
getCircumference = diameter => (Math.PI * diameter)
```

## Default parameter values
```javascript
// Longhand
function myFunc(a, b, c) {
  if (b === undefined)
    b = 3;
  if (c === undefined)
    c = 4;
  return a * b * c;
}

// Shorthand
myFunc = (a, b = 3, c = 4 ) => (a * b * c);
```

## Mandatory parameter values
```javascript
// Longhand
function myFunc(a) {
  if(a === undefined) {
    throw new Error('No parameter!');
  }
  return a;
}

// Shorthand
mandatory = () => {
  throw new Error('No parameter!');
}

myFunc = (a = mandatory()) => {
  return a;
}
```

## Template literals
```javascript
// Longhand
const hi = 'You have logged in as ' + first + ' ' + last + '.'

// Shorthand
const hi = `You have logged in as ${first} ${last}.`
```

## Destructuring Assignment
```javascript
// Longhand
const observable = require('mailbox/observable');
const action = require('mailbox/action');
const reply = require('mailbox/reply');

const from = this.props.from;
const to = this.props.to;
const loading = this.props.loading;
const errors = this.props.errors;
const entity = this.props.entity;

// Shorthand
import { observable, action, reply } from 'mailbox';
const { from, to, loading, errors, entity } = this.props;
// or assign your own variables
const { from, to, loading, errors, entity:contact } = this.props;
```

## Multi-line string
```javascript
// Longhand
const lorem = 'Lorem ipsum dolor sit amet, consectetur\n\t'
    + 'adipisicing elit, sed do eiusmod tempor incididunt\n\t'
    + 'ut labore et dolore magna aliqua. Ut enim ad minim\n\t'
    + 'veniam, quis nostrud exercitation ullamco laboris\n\t'
    + 'nisi ut aliquip ex ea commodo consequat. Duis aute\n\t'
    + 'irure dolor in reprehenderit in voluptate velit esse.\n\t'

// Shorthand
const lorem = `Lorem ipsum dolor sit amet, consectetur
    adipisicing elit, sed do eiusmod tempor incididunt
    ut labore et dolore magna aliqua. Ut enim ad minim
    veniam, quis nostrud exercitation ullamco laboris
    nisi ut aliquip ex ea commodo consequat. Duis aute
    irure dolor in reprehenderit in voluptate velit esse.`
```



# Contributing to JavaScript Shorthand
Please feel free to submit new issues. We would love for you to contribute to  JavaScript Shorthand and help make it even better than it is today! 

# License
The MIT License

Copyright (c) 2010-2018 Google, Inc. http://angularjs.org

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
