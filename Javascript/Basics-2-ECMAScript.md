# ECMAScript

## What is ECMAScript?

**ECMAScript (ES)** is a scripting language specification standardized by Ecma International. 
It is a standard for scripting languages, including JavaScript, ActionScript, and JScript. 
ES is often referred to as "JavaScript" or "JS", but **JavaScript** is actually a specific 
implementation of the ECMAScript language specification.  

## Major changes in ES6+

ES6 (ECMAScript 2015) was a major update to the language, adding many new features and improvements 
over the previous version, ES5. Since then, new versions of the language, ES7, ES8, ES9, ES10, and 
ES11, have been released with even more new features.

### Important Changes

 **Let and Const keywords:** In ES5, variables could only be declared with the var keyword, which had some 
 unexpected behaviors. ES6 introduced the let and const keywords, which provide block-scoped variable 
 declaration and better immutability respectively.  
 ```javascript
 // using var
var x = 10;
if (true) {
  var x = 20;
}
console.log(x); // Output: 20

// using let
let y = 10;
if (true) {
  let y = 20;
}
console.log(y); // Output: 10

// using const
const z = 10;
if (true) {
  const z = 20;
}
console.log(z); // Output: 10
```  

 **Arrow Functions:** Arrow functions are a new syntax for writing functions that make use of a new => operator. 
 They provide a more concise syntax for writing functions and they also capture the value of this from the enclosing context.  
```javascript
// ES5
var multiply = function(x, y) {
  return x * y;
};

// ES6+
const multiply = (x, y) => x * y;
```  

 **Classes:** ES6 introduced a new syntax for defining classes in JavaScript. This provides a more structured 
 way of creating objects with methods and properties. Classes also support inheritance and are a more powerful
 way of creating objects compared to the traditional prototypal inheritance.
```javascript
// ES5
function Person(name, age) {
  this.name = name;
  this.age = age;
}
Person.prototype.greet = function() {
  console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
};

// ES6+
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  greet() {
    console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
  }
}
```  

 **Default Parameters:** Default parameters allow you to specify default values for function parameters, 
 which are used if no value is provided when the function is called.
```javascript
function greet(name = "World") {
  console.log(`Hello, ${name}!`);
}

greet(); // Output: "Hello, World!"
greet("John"); // Output: "Hello, John!"
```  

 **Template literals:** Template literals are a new way of defining strings that allow you to interpolate variables 
 and expressions within them. This makes it easier to create dynamic strings.
```javascript
// ES5
var name = 'John';
console.log('My name is ' + name + '.');

// ES6+
const name = 'John';
console.log(`My name is ${name}.`);
```  

 **Destructuring:** Destructuring is a new syntax for extracting values from objects and arrays. It provides a concise
 way of assigning variables to specific properties of an object or elements of an array.
```javascript
// ES5
var user = { name: 'John', age: 30 };
var name = user.name;
var age = user.age;

// ES6+
const user = { name: 'John', age: 30 };
const { name, age } = user;
```  

 **Rest and Spread operators:** The rest operator (...) and spread operator (...) are two new operators introduced in ES6. 
 The rest operator allows you to collect the remaining elements of an array into a new array. The spread operator allows 
 you to spread the elements of an array into a new array.
```javascript
// Rest operator
function sum(...args) {
  return args.reduce((acc, val) => acc + val, 0);
}
console.log(sum(1, 2, 3, 4)); // Output: 10

// Spread operator
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const arr3 = [...arr1, ...arr2];
console.log(arr3); // Output: [1, 2, 3, 4, 5, 6]
```  

 **Promises:** Promises are a new way of handling asynchronous operations in JavaScript. They provide a cleaner and more 
 elegant way of handling asynchronous code compared to callbacks.  
 
   **Promise:**
```javascript
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve('Data successfully fetched.');
    }, 2000);
  });
}

fetchData()
  .then(data => console.log(data))
  .catch(error => console.error(error));
```  

   **async / await:**
```javascript
async function fetchData() {
  try {
    const response = await fetch('https://jsonplaceholder.typicode.com/todos/1');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

fetchData();
```  

 **Modules:** ES6 introduces a new syntax for defining modules in JavaScript. This allows you to encapsulate code and define 
 dependencies between modules. It also provides a more structured way of organizing your code.
```javascript
// export.js
export function add(a, b) {
  return a + b;
}

// import.js
import { add } from './export.js';

console.log(add(2, 3)); // outputs 5
```  

 **Iterators and Generators:** Iterators and generators are two new concepts introduced in ES6 that allow you to work with 
 collections of data in a more powerful and flexible way. Iterators provide a way of iterating over collections of data, 
 while generators provide a way of creating iterators.
```javascript
// iterator example
let arr = [1, 2, 3];

let iterator = arr[Symbol.iterator]();

console.log(iterator.next()); // outputs {value: 1, done: false}
console.log(iterator.next()); // outputs {value: 2, done: false}
console.log(iterator.next()); // outputs {value: 3, done: false}
console.log(iterator.next()); // outputs {value: undefined, done: true}

// generator example
function* myGenerator() {
  yield 1;
  yield 2;
  yield 3;
}

let gen = myGenerator();

console.log(gen.next()); // outputs {value: 1, done: false}
console.log(gen.next()); // outputs {value: 2, done: false}
console.log(gen.next()); // outputs {value: 3, done: false}
console.log(gen.next()); // outputs {value: undefined, done: true}
```  

 **Symbols:** Symbols are a new data type introduced in ES6. They provide a way of creating unique identifiers that can be 
 used as property keys in objects.
```javascript
const mySymbol = Symbol();

let obj = {
  [mySymbol]: 'Hello'
};

console.log(obj[mySymbol]); // outputs 'Hello'
```  
