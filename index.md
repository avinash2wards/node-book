# Pure Node.js - The Complete Guide<!-- omit in toc -->

![node-logo](assets/node-logo.svg)

- [1. Setup and An Intro](#1-setup-and-an-intro)
  - [1.1. Install](#11-install)
  - [1.2. What is Node](#12-what-is-node)
  - [1.3. Why Node is preferred ?](#13-why-node-is-preferred-)
  - [1.4. Node REPL](#14-node-repl)
    - [1.4.1. Standard REPL](#141-standard-repl)
    - [1.4.2. Build custom REPL](#142-build-custom-repl)
  - [1.5. Executing code](#15-executing-code)
  - [1.6. Node CLI](#16-node-cli)
- [2. Timers](#2-timers)
  - [2.1. Node's Timers](#21-nodes-timers)
  - [2.2. JavaScript timers are not always on time - weirdo ⏳](#22-javascript-timers-are-not-always-on-time---weirdo-)
- [3. Essential Javascript](#3-essential-javascript)
  - [3.1. Variables and Scopes](#31-variables-and-scopes)
  - [3.2. Arrow function expressions](#32-arrow-function-expressions)
    - [3.2.1. Concise syntax](#321-concise-syntax)
    - [3.2.2. *this* with Arrow function](#322-this-with-arrow-function)
  - [3.3. Modern Object Literals - Object initializer](#33-modern-object-literals---object-initializer)
  - [3.4. Destructuring assignment](#34-destructuring-assignment)
    - [3.4.1. Object destructuring](#341-object-destructuring)
    - [3.4.2. Array destructuring](#342-array-destructuring)
  - [3.5. Spread & Rest](#35-spread--rest)
    - [3.5.1. Rest syntax](#351-rest-syntax)
    - [3.5.2. Spread Syntax](#352-spread-syntax)
  - [3.6. Template literals (Template strings)](#36-template-literals-template-strings)
    - [3.6.1. Multiline strings](#361-multiline-strings)
    - [3.6.2. Embedding javascript expression (Expression interpolation)](#362-embedding-javascript-expression-expression-interpolation)
  - [3.7. Classes](#37-classes)
  - [3.8. Callback, Promise and Async/Await](#38-callback-promise-and-asyncawait)
    - [3.8.1. Callback](#381-callback)
    - [3.8.2. Promise](#382-promise)
    - [3.8.3. Async & Await](#383-async--await)
  - [3.9. JavaScript modules & CJS](#39-javascript-modules--cjs)
  - [3.10. The arguments object](#310-the-arguments-object)
  - [3.11. IIFE](#311-iife)
- [4. NPM](#4-npm)
  - [4.1. npm command](#41-npm-command)
  - [4.2. package.json](#42-packagejson)
  - [4.3. Demo package.json & package-lock.json](#43-demo-packagejson--package-lockjson)
  - [4.4. Semantic Versioning (SemVer)](#44-semantic-versioning-semver)
  - [4.5. Creating and publishing public packages](#45-creating-and-publishing-public-packages)
    - [4.5.1. Create a package/module](#451-create-a-packagemodule)
    - [4.5.2. Publish a package/module](#452-publish-a-packagemodule)
    - [4.5.3. Consume a package/module](#453-consume-a-packagemodule)
  - [4.6. NPM scripts](#46-npm-scripts)
- [5. The Node Module System](#5-the-node-module-system)
  - [5.1. What is module in Node.js/JavaScript?](#51-what-is-module-in-nodejsjavascript)
  - [5.2. The module wrapper function](#52-the-module-wrapper-function)
  - [5.3. export import](#53-export-import)
  - [5.4. Flow](#54-flow)
  - [5.5. Module caching](#55-module-caching)
  - [5.6. What is **this** inside the node modules??](#56-what-is-this-inside-the-node-modules)
- [6. Node's Global Object](#6-nodes-global-object)
- [7. `process` object](#7-process-object)
  - [7.1. process.env](#71-processenv)
  - [7.2. process.argv](#72-processargv)
  - [7.3. `process` is an Event Emitter](#73-process-is-an-event-emitter)
- [8. `Buffer`](#8-buffer)
  - [8.1. Basics](#81-basics)
  - [8.2. Buffers and character encodings](#82-buffers-and-character-encodings)
- [9. Node's Concurrency Model and The Event Loop](#9-nodes-concurrency-model-and-the-event-loop)
  - [9.1. An intro](#91-an-intro)
  - [9.2. I/O - Input/Output](#92-io---inputoutput)
  - [9.3. The Event Loop](#93-the-event-loop)
  - [9.4. V8's Call stack](#94-v8s-call-stack)
  - [9.5. Blocking the Node.js process](#95-blocking-the-nodejs-process)
  - [9.6. Non-Blocking the Node.js process](#96-non-blocking-the-nodejs-process)
- [10. Error handling in Node.js](#10-error-handling-in-nodejs)
  - [10.1. Creating exceptions](#101-creating-exceptions)
  - [10.2. Error objects](#102-error-objects)
  - [10.3. Handling exceptions](#103-handling-exceptions)
  - [10.4. Catching uncaught exceptions](#104-catching-uncaught-exceptions)
  - [10.5. Error first callbacks](#105-error-first-callbacks)
  - [10.6. Exceptions with promises](#106-exceptions-with-promises)
  - [10.7. Error handling with async/await](#107-error-handling-with-asyncawait)
- [11. Async Pattern Evolution](#11-async-pattern-evolution)
  - [11.1. Synchronous code](#111-synchronous-code)
  - [11.2. Callback pattern - Asynchronous](#112-callback-pattern---asynchronous)
  - [11.3. Promise pattern - Asynchronous](#113-promise-pattern---asynchronous)
  - [11.4. async/await pattern - Asynchronous](#114-asyncawait-pattern---asynchronous)
- [12. Event-Driven Architecture - Event Emitters](#12-event-driven-architecture---event-emitters)
  - [12.1. Enter Node's **Event Emitters**](#121-enter-nodes-event-emitters)
  - [12.2. Synchronous Events](#122-synchronous-events)
  - [12.3. Asynchronous Events](#123-asynchronous-events)
  - [12.4. Events Arguments and Errors](#124-events-arguments-and-errors)
  - [12.5. Order of Listeners](#125-order-of-listeners)
- [13. Web Server (http)](#13-web-server-http)
  - [13.1. Create an HTTP server](#131-create-an-http-server)
  - [13.2. Peek into res & req objects](#132-peek-into-res--req-objects)
  - [13.3. Streaming in HTTP server](#133-streaming-in-http-server)
  - [13.4. Making HTTP requests with Node.js](#134-making-http-requests-with-nodejs)
  - [13.5. Routing](#135-routing)
  - [13.6. URLs and Query Strings](#136-urls-and-query-strings)
- [14. Node.js with OS - os module](#14-nodejs-with-os---os-module)
- [15. Node.js with File system - fs module](#15-nodejs-with-file-system---fs-module)
  - [15.1. Create & Read files](#151-create--read-files)
  - [15.2. Delete files](#152-delete-files)
- [16. console module](#16-console-module)
- [17. Child Processes](#17-child-processes)
  - [17.1. child_process module](#171-child_process-module)
  - [17.2. `spawn` function](#172-spawn-function)
  - [17.3. `exec` function](#173-exec-function)
  - [17.4. `execFile` function](#174-execfile-function)
  - [17.5. `fork` Function](#175-fork-function)
- [18. Debugging Node.js apps](#18-debugging-nodejs-apps)
  - [18.1. Debugging with Chrome DevTools](#181-debugging-with-chrome-devtools)
  - [18.2. Debugging in VS Code](#182-debugging-in-vs-code)
  - [18.3. Debugging in Terminal](#183-debugging-in-terminal)
- [19. Node's Internal Architecture](#19-nodes-internal-architecture)
  - [19.1. V8](#191-v8)
  - [19.2. libuv](#192-libuv)
  - [19.3. llhttp](#193-llhttp)
  - [19.4. c-ares](#194-c-ares)
  - [19.5. OpenSSL](#195-openssl)
  - [19.6. zlib](#196-zlib)
- [20. Streams](#20-streams)
  - [20.1. Why Streams](#201-why-streams)
  - [20.2. Types of Streams](#202-types-of-streams)
  - [20.3. `pipe`](#203-pipe)
  - [20.4. Stream events](#204-stream-events)
  - [20.5. Implementing Streams](#205-implementing-streams)
  - [20.6. Implementing a Writable Streams](#206-implementing-a-writable-streams)
  - [20.7. Implementing a Readable Streams](#207-implementing-a-readable-streams)
  - [20.8. Implementing Duplex Streams](#208-implementing-duplex-streams)
  - [20.9. Implementing Transform Streams](#209-implementing-transform-streams)
  - [20.10. Built-in transform streams](#2010-built-in-transform-streams)

---

## 1. Setup and An Intro

### 1.1. Install

`https://nodejs.org/en/`
After the installation, we will get 2 things,

- Node runtime environment
- Built-in node modules
- NPM - node package manager

![node-install](assets/node-install.png)

### 1.2. What is Node

- An open-source, cross-platform, JavaScript runtime environment that executes JavaScript code outside of a web browser.

- V8 is the name of the JavaScript engine that powers Google Chrome. It's the thing that takes our JavaScript and executes it while browsing with Chrome

- A wrapper around V8 with built-in modules providing rich features with asynchronous APIs

- Node.js is wrapper around a VM (Virtual Machine) like V8 ( like JVM in Java, CLR in .net).

When we write JavaScript to node, node will pass the code V8. V8 will execute the code and return the result to node. Finally node make this result available to us.

![Alt text](assets/what-is-node.png "what is node")

### 1.3. Why Node is preferred ?

1. It uses fastest VM - V8
2. Best suited for non-blocking I/O operations
3. Asynchronous APIs without threads overhead
4. NPM (Node Package Manager)
5. Built in modules and utilities like fs, http etc. The full list can be found here `https://nodejs.org/api/index.html`
6. Extensible using C++ addons
7. One language - JavaScript to do every aspect of development

### 1.4. Node REPL

#### 1.4.1. Standard REPL

**R**ead **E**val **P**rint **L**oop (REPL)  
We use it to execute JavaScript and Node code.  

![alt](assets/node-repl.png)

REPL is limited when we want edit function in midway, so more flexible option is use built-in editor.  

![alt](assets/node-repl-editor.png)

Other utilities of REPL

![alt](assets/node-repl-help.png)

- .exit - Close the I/O stream, causing the REPL to exit.
- .break - When in the process of inputting a multi-line expression, entering the .break command (or pressing the ctrl + c key combination) will abort further input or processing of that expression.
- .clear - Resets the REPL context to an empty object and clears any multi-line expression currently being input.
- .help - Show this list of special commands.
- .save - Save the current REPL session to a file  

  ```console
  > .save ./file/to/save.js
  ```

- .load - Load a file into the current REPL session.
  
  ```console
  > .load ./file/to/load.js
  ```

- .editor - Enter editor mode (ctrl + d to finish, ctrl + c to cancel)
- control + c -> When pressed once, has the same effect as the .break command.When pressed twice on a blank line, has the same effect as the .exit command.
- control + d -> Has the same effect as the .exit command.
- **tab -> When pressed on a blank line, displays global and local (scope) variables. When pressed while entering other input, displays relevant autocompletion options.**

The built-in `repl` module provides a Read-Eval-Print-Loop (REPL) implementation that is available both as a standalone program (Node's REPL) or include-able in other applications.

In standard Node REPL

```console
> let count = 1
undefined
```

#### 1.4.2. Build custom REPL

As seen above, in standard REPL, it print undefined, in out custom implementation, lets not print these undefined values.

index.js

```js
const repl = require("repl");

const message = "Hello from CUSTOM REPL";

let myRepl = repl.start({
  prompt: "👉👉",
  ignoreUndefined: true,
});

// We can load any code/modules we need to repl session.
myRepl.context.msg = message;
// myRepl.context.expressMod = require("express"
```

The `repl.start()` method creates and starts a repl instance.  
Also it accepts an object for customization,

Ex,

- `prompt` - The input prompt to display. Default: '> '
- `ignoreUndefined` - If true, specifies that the default writer will not output the return value of a command if it evaluates to undefined. Default: false.

Now, run the code as any other node code we run, `node index.js`

Output, We see no undefined now and also prompt has been changed now.

```console
👉👉msg
'Hello from CUSTOM REPL'
👉👉let count = 1
👉👉
```

### 1.5. Executing code

Executing our first Node code.

index.js

```javascript
function welcome(name) {
  console.info(`Hello ${name}!`);
}

welcome("Node.js");
```

run the code,

```console
> node index.js
```

We see *Hello Node.js!*

### 1.6. Node CLI

```console
node -v => check node runtime version
node --version => same as above, but verbose
node --print "os.cpus()" => prints all CPU cores using cpus() fn on os module
node -p "os.cpus().length" => prints number of CPU cores
node -h => list all available option like above
node => this opens REPL
node path/to/script.js => execute a particular javascript file
```

Node's built-in Environment variables

```console
node -help => to see full list
```

NODE_DEBUG => ','-separated list of core modules that should print debug information.  

List of NODE_DEBUG attributes:

timer  
http  
net  
fs  
cluster  
tls  
stream  
child_process  
module

Ex.  
In Windows (PowerShell), set the NODE_DEBUG env variable to timer and execute a timer related code.

```console
$env:NODE_DEBUG="timer"
// dir env: => to check in windows, lists all the env variables
```

Execute the code

```js
setInterval(() => console.log("Hello every 1 seconds"), 2000);
// execute it normally => node index.js, will see below output with 
// complete debug info about timers. 
// try with http or stream module
```

![node-debug-timer](assets/node-debug-timer.png)

In Linux OS,  

```console
NODE_DEBUG="timer,http" node index.js
```

NODE_PATH => ';'-separated list of directories prefixed to the module search path  
Let us say, we want node to lookup in some custom directories while resolving/requiring module, this is where we mention that path.

- How to read entire system/machine env variables inside node.js code?
- In other words, How do we pass the external values to execution context of node process (simply - code 😂 )
- How to set custom new env variables?  
Answer: *process.env* & *process.argv*

## 2. Timers

### 2.1. Node's Timers

JavaScript language itself does not have Timers, usually it is provided by Browser in global window object. Same way, Node also provides timer APIs in global object.

Timer are used for delaying or execute code after a set period of time.

- setTimeout

```javascript
setTimeout(() => console.log("Hello after 5 seconds"), 5 * 1000);
// second argument takes the time in milliseconds
// code outputs after 5 seconds -> Hello after 5 seconds
```

Special case, where we can pass arguments to callback func from setTimeout

```js
setTimeout((delay) => console.log(`Hello after ${delay} seconds`), 5 * 1000, 5);
```

- setInterval

```js
setInterval(() => console.log(`Hello after 2 seconds`), 2 * 1000);
// Hello after 2 seconds
// Hello after 2 seconds
//         .
//         .
//         .
// Control + c to stop the printing by killing the process

```

setImmediate  
When we want to execute some piece of code asynchronously, but as soon as possible.

```js
setImmediate(() => console.log(`Hello immediately`));
// Hello immediately
```

>A setTimeout() callback with a 0ms delay is very similar to setImmediate(). The execution order will depend on various factors, but they will be both run in the next iteration of the event loop.

Cancelling timers  

The setImmediate(), setInterval(), and setTimeout() methods each return objects that represent the scheduled timers. These can be used to cancel the timer and prevent it from triggering.  

```js
clearTimeout(timerId);
clearInterval(timerId);
clearImmediate(timerId);
```

Ex,  

Print message after 1sec, but only 5 times. Solve the memory leak using clear timers.

```js
let count = 0;
const timerId = setInterval(() => {
  count++;
  console.log("Hi after 1");
  if (count === 5) clearInterval(timerId);
}, 1000);
```

### 2.2. JavaScript timers are not always on time - weirdo ⏳

Node is busy executing synchronous code, so, callback is waiting at the queue to get executed. so, it will invoked after node finished running the sync code.

```js
setTimeout(
  () => console.log("Hello after 1 second. Not exactly though! 🥴🥴"),
  1 * 1000
);

for (let i = 0; i < 1e10; i++) {
  // Block Node Synchronously for some time
}

// we see below message, around after 7-10 seconds
// Hello after 1 second. Not exactly though! 🥴🥴"
```

## 3. Essential Javascript

### 3.1. Variables and Scopes

JavaScript has lexical (also called static) scoping and closures. This means you can tell the scope of an identifier by looking at the source code.

The four scopes are:

- Global - visible by everything
- Function - visible within a function (and its sub-functions and blocks)
- Block - visible within a block (and its sub-blocks)
- Module - visible within a module

Pair of curly braces defines a block in JavaScript,  

```js
{ }
```

scene-1,

```js
{
  let nameLet = "nameLet"; // Block Scope
  var nameVar = "nameVar"; // Global Scope
}
console.log(nameVar); // nameVar
console.log(nameLet); // ReferenceError: nameLet is not defined
```

scene-2,

```js
if (true) {
  var nameInSideIfVar = "nameInSideIfVar"; // Global Scope
  let nameInSideIfLet = "nameInSideIfLet"; // Block Scope
}
console.log(nameInSideIfVar); // nameInSideIfVar
console.log(nameInSideIfLet); // ReferenceError: nameInSideIfLet is not defined
```

scene-3,

```js
for (var i = 1; i <= 10; i++) {
  // Global Scope
}
for (let j = 1; j <= 10; j++) {
  // Block Scope
}
console.log(i); // 11
console.log(j); // ReferenceError: j is not defined
```

scene-4,

```js
function sum(a, b) {
  // Function Scope, so available only to nested functions and nested blocks
  var resultVar = a + b;
  let resultLet = a + b;
}
sum(4 + 3);
console.log(resultLet); // resultLet is not defined
console.log(resultVar); // resultVar is not defined
```

> As for as the scope concerned let and const behaves same way. But they are different when it comes to storing the data.

const

We use *const* when the reference assigned to a identifiers is meant to be constant.  
References assigned to const identifiers **cannot be changed**.

```js
// Primitive or Scalar values
const answer = 42;
const greeting = "Hello";

answer = 100; // TypeError: Assignment to constant variable

// Objects
const numbers = [2, 4, 6];
const person = {
  firstName: "Brendan",
  lastName: "Eich",
};
numbers.push(10);
person.firstName = "Avinash";
console.log(numbers); // [ 2, 4, 6, 10 ]
console.log(person.firstName); // Avinash
```

let  
Change the *const* with *let* in above code, everything works as is.
Because references assigned to let identifiers **can be changed**.

Which one to use and when?

```js
const todosCount = 42;
/*
A big chunk of code...
*/
todosCount // is still 42;

// vs

let todosCount = 42;
/*
A big chunk of code...
*/
todosCount // might have changed;
```

### 3.2. Arrow function expressions

Why arrow function?

1. Concise syntax
2. The way it manages the **this** inside of it

#### 3.2.1. Concise syntax

Function declaration

```js
function add(x, y) {
  return x + y;
}
```

Function expression

```js
const add = function (x, y) {
  return x + y;
};
```

Arrow function expression

```js
const add = (x, y) => {
  return x + y;
};
```

Arrow function expression with implicit return

```js
const add = (x, y) => x + y;
```

> Arrows functions are anonymous

#### 3.2.2. *this* with Arrow function

In JavaScript, there are 4 ways you can invoke a regular function.

- *Simple invocation* - the value of this equals to the global object.

globalThis => node  
window => browser

```js
function myFunction() {
  console.log(this);
}
// Simple invocation
myFunction(); // Node's  globalThis object => Object [global] { }
```

- A *Method invocation* - the value of this is the object owning the method  

```js
const myObject = {
  method() {
    console.log(this);
  },
};
// Method invocation
myObject.method(); // logs myObject => { method: [Function: method] }
```

- An *indirect invocation* - the value of this equals to the first argument

```js
function myFunction() {
  console.log(this);
}
const myContext = { value: "A" };
myFunction.call(myContext); // logs { value: 'A' }
myFunction.apply(myContext); // logs { value: 'A' }
```

- A *constructor invocation* using new keyword this equals to the newly created instance.

```js
function MyFunction() {
  console.log(this);
}
new MyFunction(); // logs an instance of MyFunction => MyFunction {}
```

The arrow function doesn't define its own execution context, i.e. **this**.  
No matter how or where being executed, **this** value inside of an arrow function always equals **this** value from the outer function. In other words, the arrow function resolves this lexically (statically or physically).

ex,

```js
const myObject = {
  myMethod(items) {
    console.log(this); // logs myObject
    const callback = () => {
      console.log(this); // logs myObject
    };
    items.forEach(callback);
  },
};
myObject.myMethod([1, 2, 3]);

// { myMethod: [Function: myMethod] }
// { myMethod: [Function: myMethod] }
// { myMethod: [Function: myMethod] }
// { myMethod: [Function: myMethod] }
```

> change the callback to regular function, see the output and why is that out put?

### 3.3. Modern Object Literals - Object initializer

```js
const name = "fullName";
const balloon = "🎈";

const ModernObj = {
  x: 10,
  y: 20,
  f0: function () {},
  f1() {},
  f2: () => {},
  [name]: "avinash",
  balloon,
};
```

### 3.4. Destructuring assignment

The destructuring assignment syntax is a JavaScript expression that makes it possible to **unpack** values from arrays, or properties from objects, into distinct variables.

#### 3.4.1. Object destructuring

```js
const user = {
  id: 42,
  isVerified: true,
};

const { id, isVerified } = user;

const { PI, E, SQRT2 } = Math;

const { readFile } = require("fs");

function userId({ id }) {
  return id;
}
userId(user);
```

#### 3.4.2. Array destructuring

```js
const foo = ['one', 'two', 'three'];

const [red, yellow, green] = foo;

let a, b;

[a, b] = [1, 2];

const foo = ['one', 'two'];

const [red, yellow, green, blue] = foo;
// green and blue will be undefined

function f() {
  return [1, 2];
}

let a, b;
[a, b] = f();

// Selecting few from array
const [a, , b] = [1, 2, 3];
// a = 1
// b = 3
```

### 3.5. Spread & Rest

#### 3.5.1. Rest syntax

This collects multiple elements and "condenses" them into a single element.

With Array

```js
const [first, ...restOfthem] = [1, 2, 3];

console.log(first); // 1
console.log(restOfthem); // [ 2, 3 ]
```

With Object

```js
const data = {
  temp1: "001",
  temp1: "007",
  firstName: "James",
  lastName: "Bond",
};

const { temp1, temp2, ...person } = data;
console.log(temp1, temp1, person);
// 002 002 { firstName: 'James', lastName: 'Bond' }
```

#### 3.5.2. Spread Syntax

Spread syntax (...) allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected.

> It does opposite of Rest operation

With Array

```js
// This creates brand new array by copying the restOfthem array items
const newArray = [...restOfItems];

//-----------------------

function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers)); // 6
```

With Object

```js
// This creates brand new object by copying the person objects properties
const newObject = {
  ...person,
}
```

### 3.6. Template literals (Template strings)

Template literals are literals delimited with **backtick (`)**, allowing embedded expressions called substitutions.

#### 3.6.1. Multiline strings

(old way)

```js
console.log("string text line 1\n" + "string text line 2");
```

(new way)

```js
console.log(`string text line 1 
string text line 2`);
```

#### 3.6.2. Embedding javascript expression (Expression interpolation)

```js
let a = 5;
let b = 10;
console.log(`Fifteen is ${a + b} and
not ${2 * a + b}.`);
// "Fifteen is 15 and
// not 20."
```

```js
const html = `
  <div>
    ${new Date()}
  </div>
`;
console.info(html);

// <div>
//    Thu Dec 23 2021 07:29:09 GMT+0530 (India Standard Time)
// </div>
```

### 3.7. Classes

Classes are a template for creating objects. They encapsulate data with code (method) to work on that data.

> JavaScript classes are syntactic sugar over functions.  
> JavaScript class mechanism are not equivalent to Java, C# or Python class.

```js
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(`Hello ${this.name}!`);
  }
}
const o1 = new Person("Bond");
o1.greet(); // Hello Bond!
```

With Inheritance

```js
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(`Hello ${this.name}!`);
  }
}

class Student extends Person {
  constructor(name, level) {
    super(name);
    this.level = level;
  }
  greet() {
    console.log(`Hello ${this.name} from ${this.level}`);
  }
}

const o1 = new Person("Bond");
const o2 = new Student("Bond Jr. 1", "1st Grade");
const o3 = new Student("Bond Jr. 1", "2nd Grade");

o3.greet = () => console.log("I am special!");

o1.greet(); // Hello Bond!
o2.greet(); // Hello Bond Jr. 1 from 1st Grade
o3.greet(); // I am special!
```

### 3.8. Callback, Promise and Async/Await

In JavaScript, we can code async tasks in 3 ways.

#### 3.8.1. Callback

When an async operation had been completed, a callback function (meaning call me back when the operation has been completed) is executed.  
A function that Node or Browser will “call back” at a later point in the time of a program.  

Ex,

```js
const callbackFunction = result = {
  // Called when the operation completes
};
asyncOperation(params, callbackFunction);
```  

But as soon as you handle multiple async operations, the callback functions nest into each other ending in **callback hell**.

#### 3.8.2. Promise

A promise is a placeholder object for the results of an async task. With the use of promises, we can handle the async operations easier.

```js
const promise = asyncOperation(params);
promise.then(result => {
  // Called when the operation completes
});
```

Problem is chains of promises.then().then()...then()...

#### 3.8.3. Async & Await

The async/await syntax (starting ES2017). It lets you write async code in a concise and sync manner

An async function is a function declared with the async keyword, and the await keyword is permitted within them. The async and await keywords enable asynchronous, promise-based behavior to be written in a cleaner style, avoiding the need to explicitly configure promise chains.

```js
(async function() {
  const result = await asyncOperation(params);
  // Called when the operation completes
})();
```

> Note: async/await is syntactic sugar on top of promises.

ex,

```js
const https = require("https");

// consider this as a browser Fetch API. A tiny library code
function fetch(url) {
  return new Promise((resolve, reject) => {
    https.get(
      url,
      {
        headers: {
          "User-Agent": "request",
        },
      },
      (res) => {
        let data = "";
        res.on("data", (rd) => (data = data + rd));
        res.on("end", () => resolve(data));
        res.on("error", reject);
      }
    );
  });
}

// then and catch pattern
fetch("https://api.github.com/users/ry")
  .then((data) => {
    console.log(data);
  })
  .catch((error) => console.log);

// async await pattern
async function read() {
  try {
    const data = await fetch("https://api.github.com/users/ry");
    console.log(data);
  } catch (error) {
    console.log(error);
  }
}
read();
```

### 3.9. JavaScript modules & CJS

### 3.10. The arguments object

**arguments** is an Array-like local object accessible inside functions that contains the values of the arguments passed to that function.
> Not available in arrow function

```js
function add() {
  console.log(arguments);
}
add(1, 2, 3);
// [Arguments] { '0': 1, '1': 2, '2': 3 }
```

### 3.11. IIFE

## 4. NPM

*npm* is two things, i.e.

- It is an online registry for the publishing (code sharing) of open-source Node.js projects.
  `https://www.npmjs.com/`
- It is a command-line utility (CLI) for interacting with said repository that aids in package installation, version management, and dependency management.

**N**ode **P**ackage **M**anager - NPM

Using npm CLI, we can install node packages (modules).

In Node.js, a module is nothing but,

- a JavaScript file
- a **folder with index.js** containing some JavaScript code

### 4.1. npm command

it gets installed along side with node only.

```console
npm --version
```

How to update it?

```console
npm install -g npm
```

How to download/install node packages?

```console
npm install lodash
```

- The above command will create node_modules folder, and puts the lodash js code inside the folder.
- When we refer this module in the code, node is pre-configured to resolve/look into this folder to load the related code.
  
  Usage

  ```js
  const lodash = require('lodash');
  ```

```md
npm install lodash => install locally
npm uninstall lodash => uninstall locally
npm install create-react-app -g => install globally
npm uninstall create-react-app -g => uninstall globally
npm ls -g --depth=0 => show all the globally installed modules
npm ls --depth=0 => show all the locally installed modules - project directory.
npm ll -g --depth=0 => show all the globally installed modules with description
npm update lodash => updating a single package called lodash
npm update => it updates all the packages listed in `package.json` with SemVer rule.
npm config list => Show all the config settings for npm CLI
npm config list -l => CLI default config values
npm search lodash => search the npm registry right from the terminal
npm home lodash => opens the home page of lodash package
npm repo lodash => opens the home page of lodash package 
```

### 4.2. package.json

- This file holds various metadata relevant to the project.
- This file is used to give information to npm that allows it to identify the project as well as handle the project's dependencies.
- It can also contain other metadata such as a project description, the version of the project in a particular distribution, license information.

Minimal package.json - Metadata

```json
{
  "name" : "fancy-pant",
  "version" : "0.0.0",
}
```

### 4.3. Demo package.json & package-lock.json

Create a  fancy-pant and create a package.json with above content and run again below command

 ```console
 npm install lodash
 ```

Now,this did/created 3 things,

1. Updated the package.json to below content.

    ```json
    {
      "name": "fancy-pant",
      "version": "0.0.0",
      "dependencies": {
        "lodash": "^4.17.21"
      }
    }
    ```

    - `name` is all lowercase and separated by dash
    - `version` is SemVer

2. Created the node_modules folder and inside it downloaded lodash js code.
  
3. Created package-lock.json - this file is to maintain the peer dependency package information like there exact version.

When we want to share out app, we cannot share the node_modules, instead we share `package.json` and `package-lock.json` file.
npm command can read this meta data and install the same package.

Ex,  
Delete node_modules and execute the below command will re-install all the modules according to package files info.

```console
npm install
```

What if a package is required only at the development time (jest), how do i differentiate the package.

```console
npm install jest -D
npm install jest --save-dev
```

then package.json will look like below,

```json
{
  "name": "fancy-pant",
  "version": "0.0.0",
  "dependencies": {
    "lodash": "^4.17.21"
  },
  "devDependencies": {
    "jest": "^27.4.5"
  }
}
```

How to automate the package.json file creation. In other words, how to scaffold new Node.js project.

```console
npm init -y
```

Installing packages globally,

```console
npm install -g create-next-app
```

The global package's node_modules will be stored at here,
C:\Users\avigo\AppData\Roaming\npm

Then, we can use this command anywhere in the application to create react apps.

### 4.4. Semantic Versioning (SemVer)

- npm package uses, SemVer versioning technique.
- SemVer nothing but a contract between package author and consumer.
- It's metadata about a package stored in package.json

![node-semver](assets/node-semver.png)

In package.json, there 3 way to manage the version of packages,

**~ (tilde)** character means, free to install any latest available patch version.  

~ 1.2.3  
  1.2.6 yes  
  1.2.9 yes  
  1.3.0 NO  
  1.2.x where x is greater than or equal to 3.

**^ (caret)** character means, free to install any latest available minor & patch version.

  ^ 1.2.3  
    1.5.3 yes  
    1.6.9 yes  
    2.0.0 NO  
    1.x.y where x is greater than or equal to 2 for minor and y is greater than or equal to 3

Fixed version : 1.2.3, npm will install exact version.

> `https://semver.npmjs.com/`

*npm install lodash* by default will use caret version when installing. if we need exact version then we have to,
*npm install lodash@4.17.21*

How to update npm packages?  

The below command will read the package.json and package-lock.json files and according package's SemVer mentioned for each one, it fetches the latest packages from `www.npmjs.com` and updates the package files also.

```console
npm update
```

### 4.5. Creating and publishing public packages

#### 4.5.1. Create a package/module

```console
mkdir colorful-greet
cd colorful-greet
npm init -y
echo console.log("Hi") > index.js
npm i chalk@4.0.0
```

index.js

```js
const chalk = require("chalk");

const greet = (message) => {
  console.log(chalk.red.greenBright.bold(`${message} 👋 🚀🚀`));
};

module.exports = {
  greet,
};
```

#### 4.5.2. Publish a package/module

Signup at `https://www.npmjs.com/` and continue below command

```console
🚀  npm login

// Username: avinashcodelab
// Password:
// Email: (this IS public) avigowda.c@gmail.com
// Logged in as avinashcodelab on https://registry.npmjs.org/.

npm publish
```

We see the package published at `https://www.npmjs.com/package/colorful-greet`

#### 4.5.3. Consume a package/module

Now, how to consume it?

```console
 mkdir test-greet
 cd test-greet
 npm init -y
 npm i colorful-greet
 echo "" >  app.js
```

app.js

```js
const { greet } = require("colorful-greet");

console.log("yo man....I am normal 😭😭");
greet("yo man....");
```

```console
node app.js

// yo man....I am normal 😭😭
// yo man.... 👋 🚀🚀
```

### 4.6. NPM scripts

NPM scripts are the scripts to automate repetitive tasks. For example, building bundling a project, minifying Cascading Style Sheets (CSS) and JavaScript (JS) files etc.

We specify npm scripts within the **scripts** attribute of the main object in package.json and then run it using below command.

```console
npm run nameofthescript.
```

Example, package.json

```json
{
  "name": "test-greet",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "node app.js",
    "test": "jest",
    "lint": "eslint app.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "colorful-greet": "^1.0.0"
  }
}
```

How to run the scripts

```console
npm run start
npm start
npm run test
npm run lint
```

The complete list of npm scripts can be found here,
`https://docs.npmjs.com/cli/v8/using-npm/scripts`

> **npx** (npm execute) is similar binary as npm and it gets installed along with npm@5.2.0.  
> This command allows us to run the commands from an npm package (either one installed locally, or fetched remotely), in a similar context as running it via **npm run**.

## 5. The Node Module System

### 5.1. What is module in Node.js/JavaScript?

- a JavaScript file, that contains code.
- A folder containing a index.js file that contains code

So, lets define a node module then,

index.js

```js
console.log("Hello Node Module System");
```

Yes, above **index.js** file is node module now.  
Promotion 📣🥂🍻🥳💃🏿🎈🎉🎊 from file to module 🤣

But why not call it just a file????? why all the fancy name?

Answer,
index.js

```js
console.log(arguments);
```

Outputs,

```js
[Arguments] {
  '0': {},
  '1': [Function: require] {
    resolve: [Function: resolve] { paths: [Function: paths] },
    main: Module {
      id: '.',
      path: 'C:\\personal\\node-book',
      exports: {},
      parent: null,
      filename: 'C:\\personal\\node-book\\1-index.js',
      loaded: false,
      children: [],
      paths: [Array]
    },
    extensions: [Object: null prototype] {
      '.js': [Function (anonymous)],
      '.json': [Function (anonymous)],
      '.node': [Function (anonymous)]
    },
    cache: [Object: null prototype] {
      'C:\\personal\\node-book\\1-index.js': [Module]
    }
  },
  '2': Module {
    id: '.',
    path: 'C:\\personal\\node-book',
    exports: {},
    parent: null,
    filename: 'C:\\personal\\node-book\\1-index.js',
    loaded: false,
    children: [],
    paths: [
      'C:\\personal\\node-book\\node_modules',
      'C:\\personal\\node_modules',
      'C:\\node_modules'
    ]
  },
  '3': 'C:\\personal\\node-book\\1-index.js',
  '4': 'C:\\personal\\node-book'
}
```

Wait, was there a function hidden all these time??🤯😲
Yes,

### 5.2. The module wrapper function

Before a module's code is executed, Node.js will wrap it with a function wrapper that looks like the following:

```js
(function (exports, require, module, __filename, __dirname) {
  // Module code actually lives in here
  console.log(arguments);
});
```

By doing this, Node.js achieves a few things:

- It keeps top-level variables (defined with var, const or let) scoped to the module by using IIFE rather than the global object.
- It helps to provide some global-looking variables that are actually specific to the module, such as:
  - The **module** and **exports** objects that the implementor can use to export values from the module.
  - The convenience variables **__filename** and **__dirname**,   containing the module's absolute filename and directory path.

Below code snippet is from Node.js source code at GitHub.  
`https://github.com/nodejs/node/blob/master/lib/internal/modules/cjs/loader.js`

Same available in Node REPL also.

```console
node
require("module").wrapper
```

```js
let wrap = function(script) {
  return Module.wrapper[0] + script + Module.wrapper[1];
};

const wrapper = [
  '(function (exports, require, module, __filename, __dirname) { ',
  '\n});',
];
```

- *exports* - A reference to the `module.exports` that is shorter to type.  
- *require(id)* - Used to import modules, JSON, and local files
- **id** is absolute path of a file or module. For root module it is "."

```js

// Importing a local module
const myLocalModule = require('./path/myLocalModule');

// Importing a JSON file
const jsonData = require('./path/filename.json');

// Importing a module from node_modules or Node.js built-in module:
const crypto = require('crypto');
```

- *module* - A reference to the current module.  
   In particular, **module.exports** is used for defining what a module exports and makes available through **require()**.

- *__filename* - The file name of the current module.
- *__dirname* - The directory name of the current module.

### 5.3. export import

math.js (node module export)

```js
const add = () => {};
const measurementsUnitsMap = {
  in: "Inch",
  cm: "Centimeter",
  kg: "Kilogram",
};
const PI = 3.14;

module.exports = {
  add,
  measurementsUnitsMap,
  PI,
};

console.log("exports => ", exports);
console.log("require => ", require);
console.log("module.exports => ", module.exports);
console.log("__filename => ", __filename);
console.log("__dirname => ", __dirname);
```

```console
node math.js
```

Output,

```json
exports =>  {}
require =>  [Function: require] {
  resolve: [Function: resolve] { paths: [Function: paths] },
      loaded: false,
      children: [],
      paths: [Array]
    }
  }
}
module.exports =>  {
  add: [Function: add],
  measurementsUnitsMap: { in: 'Inch', cm: 'Centimeter', kg: 'Kilogram' },
  PI: 3.14
}
__filename =>  C:\personal\node-book\math.js
__dirname =>  C:\personal\node-book
```

index.js (node module import/consuming)

```js
const mathObj = require("./math");

console.log("mathObj => ", mathObj);
console.log("exports => ", exports);
console.log("require => ", require);
console.log("module.exports => ", module.exports);
console.log("__filename => ", __filename);
console.log("__dirname => ", __dirname);
```

```console
node index.js
```

Output,

```json
mathObj =>  {
  add: [Function: add],
  measurementsUnitsMap: { in: 'Inch', cm: 'Centimeter', kg: 'Kilogram' },
  PI: 3.14
}
exports =>  {}
require =>  [Function: require] {
  resolve: [Function: resolve] { paths: [Function: paths] },
  main: Module {
    id: '.',
    path: 'C:\\personal\\node-book',
    exports: {},
    parent: null,
    filename: 'C:\\personal\\node-book\\index.js',
    loaded: false,
    children: [ [Module] ],
    paths: [
      'C:\\personal\\node-book\\node_modules',
      'C:\\personal\\node_modules',
      'C:\\node_modules'
    ]
  },
  extensions: [Object: null prototype] {
    '.js': [Function (anonymous)],
    '.json': [Function (anonymous)],
    '.node': [Function (anonymous)]
  },
  cache: [Object: null prototype] {
    'C:\\personal\\node-book\\index.js': Module {
      id: '.',
      path: 'C:\\personal\\node-book',
      exports: {},
      parent: null,
      filename: 'C:\\personal\\node-book\\index.js',
      loaded: false,
      children: [Array],
      paths: [Array]
    },
    'C:\\personal\\node-book\\math.js': Module {
      id: 'C:\\personal\\node-book\\math.js',
      path: 'C:\\personal\\node-book',
      exports: [Object],
      parent: [Module],
      filename: 'C:\\personal\\node-book\\math.js',
      loaded: true,
      children: [],
      paths: [Array]
    }
  }
}
module.exports =>  {}
__filename =>  C:\personal\node-book\index.js
__dirname =>  C:\personal\node-book
```

> Note: Now, console only `module` object in math.js file and check whats the parent property is.

In above example, the top level export api is an object, but it can be anything as shown in below examples,

```js
// app.js, top-level API is an array
module.exports = [2, 3, 5, 7];
// const arrayOfItems = import("./app.js")

// --------------

// app.js, top-level API is a string
module.exports = `
  <main>
    <h1>Avinash</h1>
  </main>
`;
// const stringVal = import("./app.js")

// --------------

// app.js, top-level API is a function
module.exports = (header) => `
<main>
  <h1>${header}</h1>
</main>
`;
// const func = import("./app.js")
// func("Node.js")

// --------------

// app.js, top-level API is a simple number
module.exports = 1000;
// const aNumber = import("./app.js")
```

> Note

```js
exports.name = "Avinash"; // works
exports = { name: "Avinash" }; // DOESN'T WORK
module.exports = { name: "Avinash" }; // works

// Why?
// this how internal code is exports = module.exports;
// so, when i try to re-assign something to exports, it will change the reference for // module.exports intern. finally breaking the reference between exports and module.exports

```

### 5.4. Flow

When Node invokes that `require()` function with a local file path as the function’s only argument, Node goes through the following sequence of steps:

- **Resolving**: To find the absolute path of the file (id).
- **Loading**: To determine the type of the file content (parsing the content).
- **Wrapping**: To give the file its private scope. This is what makes both the require and module objects local to every file we require.
- **Evaluating**: This is what the VM eventually does with the loaded code.
- **Caching**: So that when we require this file again, we don’t go over all the steps another time.

Let's say, we are working in project directory called `node-book` and trying to `require("./math.js)` from `index.js`

Node will look for math.js module in all the paths specified by `module.paths`

Node REPL from inside `node-book` folder.

```md
> module
Module {
  id: '<repl>',
  path: '.',
  exports: {},
  parent: undefined,
  filename: null,
  loaded: false,
  children: [],
  paths: [
    'C:\\personal\\node-book\\repl\\node_modules',
    'C:\\personal\\node-book\\node_modules',
    'C:\\personal\\node_modules',
    'C:\\node_modules',
    'C:\\Users\\avigo\\.node_modules',
    'C:\\Users\\avigo\\.node_libraries',
    'C:\\Program Files\\nodejs\\lib\\node'
  ]
}
```

> Node will look for.js .json or .node extensions while resolving.  
> Also inspect below code,

```js
console.log(require.extensions);
console.log(require.extensions[".js"].toString());
console.log(require.extensions[".json"].toString());
```

### 5.5. Module caching

```js
// a.js
console.log("Hello");
```

```js
// index.js
require("./a");
require("./a");
require("./a");

// console.log(require.cache); // we can see the caching here

// prints
// Hello
```

In console we see only once message has been printed. Basically node modules are **singleton**

How to make them load all the time?

1. Delete the cache, `delete require.cache["path here"]`. NOT RECOMMENDED
2. export module code as a function and invoke the fn

```js
// a.js
module.exports = greet = () => console.log("Hello");
```

```js
// index.js
require("./a")();
require("./a")();
require("./a")();

// prints
// Hello
// Hello
// Hello
```

### 5.6. What is **this** inside the node modules??

```js
console.log("outsider", this); // this => module.exports .i.e. {}

function test() {
  console.log("insider", this); // this => globalThis
}
test();
```

## 6. Node's Global Object

As seen in Module system, everything we declare/define inside a module is local to that module.  
Q: But what if we wanted to share a data among across all the modules?
A: global object

> global object is equivalent to browser window object.  
> **Most of the time we don't use this to share the data, we should not pollute the global env.**

```js
console.dir(global, { depth: 0 });

// <ref *1> Object [global] {
//   global: [Circular *1],
//   clearInterval: [Function: clearInterval],
//   clearTimeout: [Function: clearTimeout],
//   setInterval: [Function: setInterval],
//   setTimeout: [Function],
//   queueMicrotask: [Function: queueMicrotask],
//   clearImmediate: [Function: clearImmediate],
//   setImmediate: [Function]
// }
```

As seen above, whatever we import, without importing or referencing , that is, all the timers, **process** object, etc are are coming from global object like below.

```js
setTimeout(() => {}, 1000);
global.setTimeout(() => {}, 1000);

process.env.APP_PORT;
global.process.env.APP_PORT;

// We even can set/get the values across modules

// a.js
global.user = {
  name: "Avinash",
};

// b.js
require("./a");
console.log(global.user);
```

>The following variables may appear to be global but are not.  
They exist only in the scope of modules.

- __dirname  
- __filename  
- exports  
- module  
- require()

Full documentation of all the global APIs can be found here.
`https://nodejs.org/api/globals.html`

## 7. `process` object

- May be, `process` is the most useful property of Node's `global` object.
- The node `process` object provides a bridge between a Node application and its running environment (OS).

### 7.1. process.env

Set the custom env variable
 In Windows (PS),

 ```console
 $env:MY_APP_PORT=8080
 ```

 In Linux,

 ```console
 export MY_APP_PORT=8080
 ```

 Now, lets read it through Node CLI

 ```console
 node -p 'process.env.MY_APP_PORT'
 // 8080
 ```

 Through code,

```console
const appPort = process.env.MY_APP_PORT;
console.log(appPort); // 8080

// This list everything about its running environment 
console.log(process.env);
```

> process.env mainly useful to store deployments specific values, db connection , API details etc.

### 7.2. process.argv

The `process.argv` property is an in-built API of the `process` module which is used to get the arguments passed to the node.js process when run in the command line.

Ex,

```js
console.log(process.argv);

let _3rdArg = process.argv[2];

if (_3rdArg === "yes") {
  console.log("Hi");
} else {
  //do something else
}

// first 2 positions are filled by node, by default
// [
//   'C:\\Program Files\\nodejs\\node.exe',
//   'C:\\personal\\node-book\\process-lesson.js',
//   'yes',
//   '100'
// ]
// Hi
```

Run,

```console
node process-lesson.js yes 100
```

Other frequently properties of process object are,  

1. stdout
2. stdin
3. stderr  

These props (Streams), control the communication(liaison) channel between node process and OS environment (for ex, OS shell, command line).

```js
process.stdout.write("Hell Node\n"); // directly using
console.log("Hell Node\n"); 
// console.log internally uses, above process object's stdout prop to interact with OS command line to show the output.
```

An echo program,

```js
process.stdin.on("readable", () => {
  const chunk = process.stdin.read();
  if (chunk !== null) process.stdout.write(chunk);
});

// does the same thing as above, stdin is readable stream and stdout is writable stream.
// process.stdin.pipe(process.stdout);
```

### 7.3. `process` is an Event Emitter

The `process` can emit as well as listen to events.

1. Let's say, while starting the app, db did'nt get initialized, so we want to terminate the app (the node process) or accidentally process is terminated/stopped, we need to send an email notification or log an error somewhere.

    How do we terminate or exit the node process and log errors?

    ```js
    setTimeout(() => {
      // 💩 happened at the db side, SO, no need to keep the service up. lets terminate the app.
      process.exit("db did not initialize"); // Emitting an event
    }, 2000);

    process.on("exit", (data) => { // Listening or Subscribing to an event
      // We can do one final synchronous operation here before the node process // terminates, like, send an email or logging an error message
        console.log(`Process will exit now. ERROR : ${data}`);
    });

    console.log("Hello!");

    // output
    // Hello!
    // Process will exit now. ERROR : db did not initialize
    ```

    > Why I am seeing Hello message first...🤨 clue - The Event Loop and Async nature.

2. Another example, How to handle the application level errors or the error which are happened at code level and are unhandled, bubbled all the way upto event loop?

    In this case, naturally, **Node will exit the process and shows the callstack trace.**

    Ex,

    ```js
    process.on("exit", (code) => {
      console.log(`About to exit with code: ${code}`);
    });

    // trigger an exception
    console.lg();

    // Output,

    // About to exit with code: 1
    // C:\personal\node-book\process.js:6
    // console.lg();
    //         ^

    // TypeError: console.lg is not a function
    //     at Object.<anonymous> (C:\personal\node-book\process.js:6:9)
    //     at Module._compile (internal/modules/cjs/loader.js:1063:30)
    //     at Object.Module._extensions..js (internal/modules/cjs/loader js:1092:10)
    //     at Module.load (internal/modules/cjs/loader.js:928:32)
    //     at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    //     at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:72:12)
    //     at internal/main/run_main_module.js:17:47
    ```

3. How handle these unhandled JavaScript exception?

    Here, we are just listening to `uncaughtException` event and doing nothing but **process did not exit though we had `exit` event handler listening**. Evidently we don't see message `About to exit with code: 1` in console.

    ```js
    process.on("exit", (code) => {
      console.log(`About to exit with code: ${code}`);
    });

    process.on("uncaughtException", (err) => {
      console.error(err);
    });

    // keep app running by keeping the event loop busy
    process.stdin.resume();

    // trigger an exception
    console.lg();  

    // Outputs,
    // TypeError: console.lg is not a function
    //     at Object.<anonymous> (C:\personal\node-book\process.js:6:9)
    //     at Module._compile (internal/modules/cjs/loader.js:1063:30)
    //     at Object.Module._extensions..js (internal/modules/cjs/loader js:1092:10)
    //     at Module.load (internal/modules/cjs/loader.js:928:32)
    //     at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    //     at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:72:12)
    //     at internal/main/run_main_module.js:17:47
    ```  

    Lets `exit` the process manually.

    ```js
    process.on("uncaughtException", (err) => {
      console.error(err);
      // FORCE exit the process too.
      process.exit(1);
    });

    // Outputs,
    // TypeError: console.lg is not a function
    //     at Object.<anonymous> (C:\personal\node-book\process.js:6:9)
    //     at Module._compile (internal/modules/cjs/loader.js:1063:30)
    //     at Object.Module._extensions..js (internal/modules/cjs/loader js:1092:10)
    //     at Module.load (internal/modules/cjs/loader.js:928:32)
    //     at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    //     at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:72:12)
    //     at internal/main/run_main_module.js:17:47
    // About to exit with code: 1
    ```

## 8. `Buffer`

### 8.1. Basics

- Buffer objects are used to represent a **fixed-length sequence of bytes**.
- A buffer is a chunk of memory allocated outside of the V8 heap, and we can put some data in that memory, and that data can be interpreted in one of many ways, depending on the length of a character.
- Buffer is to hold binary stream of data. Unless until we specify the encoding, we cannot see the data in readable format, otherwise it will be in binary format.
- When we talk about a buffer, there is a character encoding, because whatever we place in a Buffer does not have any character encoding, so to read it, we need to specify an encoding.
- For example, When we read content from files, if we don't specify an encoding, we get back a buffer object.
  
Three ways to create a buffer

- `alloc` creates a filled (by default 0) buffer of given size.
- `allocUnsafe` creates a uninitialized buffer. Might contain old or sensitive data from prev or other buffer memory.
- `from` creates a buffer with `array` of bytes in the range 0 – 255. Array entries outside that range will be truncated to fit into it.

To fill a buffer we can use `buffer.fill()`

```js
// 1. alloc

// Creates a zero-filled Buffer of length 10.
const buf1 = Buffer.alloc(10);
console.log(buf1); // <Buffer 00 00 00 00 00 00 00 00 00 00>

/*
Creates a Buffer of length 10,
filled with bytes which all have the value `1`.
*/
const buf2 = Buffer.alloc(10, 1);
console.log(buf2); // <Buffer 01 01 01 01 01 01 01 01 01 01>

// 2. allocUnsafe

/* 
Creates an uninitialized buffer of length 10.
This is faster than calling Buffer.alloc() but the returned
Buffer instance might contain old data that needs to be overwritten using fill(), write(), or other functions that fill the Buffer's contents.
*/
const buf3 = Buffer.allocUnsafe(10);
console.log(buf3); // <Buffer 00 00 00 00 00 00 00 00 b8 ee>

// 3. from

// Creates a Buffer containing the bytes [1, 2, 3].
const buf4 = Buffer.from([1, 2, 3]);
console.log(buf4); // <Buffer 01 02 03>

// Creates a Buffer containing the UTF-8-encoded bytes for the string 'tést':
const buf5 = Buffer.from("tést");
console.log(buf5);
// [0x74, 0xc3, 0xa9, 0x73, 0x74] (in hexadecimal notation)
// [116, 195, 169, 115, 116] (in decimal notation)
```

### 8.2. Buffers and character encodings

When converting between `Buffers` and strings, a character encoding may be specified. If no character encoding is specified, UTF-8 will be used as the default.

```js
const buf = Buffer.from("hello world", "utf8");

console.log(buf.toString()); // hello world
console.log(buf.toString("hex")); // 68656c6c6f20776f726c64
console.log(buf.toString("base64")); // aGVsbG8gd29ybGQ=
console.log(Buffer.from("good", "utf8")); // <Buffer 67 6f 6f 64>
console.log(Buffer.from("good", "utf16le")); // <Buffer 67 00 6f 00 6f 00 64 00>
```

## 9. Node's Concurrency Model and The Event Loop

### 9.1. An intro

Event loop:  
Pizza analogy for callback and promise concept
1 guy doing multitasking with 10 customers with ticketing mechanism.  
10 guys serving 10 customers parallel.

Ex,  

If we execute the below code,

- node will start the new OS process.
- finished executing the code.
- once node finishes its work, OS terminate the process.

```js
console.log("Hi");
```

By default if node has not having anything to execute, it **will not** keep on running in background.

Let's take another example, which make node process to run in background for some time.

```js
console.log("Hi");

setInterval(() => {
  console.log("Hi, I'm here because of The Event Loop");
}, 1000);
```

The above code snippet will keep the node process alive in background unless it gets killed forcefully. once all the async operations are done and event loop will exit and OS process will terminated.

How do i know it? lets examine the process in windows (PS),

```console
ps | findStr node
    or 
Tasklist /fo table | findStr node
```

Outputs,

14 |  12.06  |   19.92   |  0.05  |  2488  | 1  |  node

How to kill this node process in windows?
Control + c in terminal

or

```console
Taskkill /F /PID 2488
```

Why node behavior this way? **The Event Loop**

### 9.2. I/O - Input/Output

What exactly does this mean?

- In general, I/O is used to label a communication between a process in a computer CPU and anything external to that CPU, including memory, disk, network, and even another process.
- I/O refers primarily to the interaction with the system's disk and network.
- Almost every operation that happens inside and outside computers is an I/O operation.
- The process communicates with these external things with signals or messages. Those signals are input when they are received by the process, and output when they are sent out by the process.

In Node, the term I/O is usually used to reference accessing disk and network resources, which is the most time-expensive (slow) part of all operations.

How to handle these multiple IO operations/requests?

1. **Execute them synchronously** - but one request is going to hold up other requests
2. **Fork (spawn) a new process** (threads) from the OS to handle each request - but scaling issue with a lot of requests and it becomes issue when threads start accessing shared resources. Ex, Apache, IIS are multi-threaded and it usually creates a thread per request.
3. Single threaded frameworks like Node.js use an event loop to handle requests for slow I/O operations without blocking the main execution runtime.

So, How this event loop works anyway?

### 9.3. The Event Loop

- The event loop is an endless loop, where the JavaScript engine waits for tasks, executes them and then sleeps, waiting for more tasks.
- The mechanism that handles external events and converts them into callback invocations.
- It is the loop that picks events from the event queue and pushes their callbacks to the callstack.
- Event loop is what Node uses to process asynchronous actions and interface them for us so that we don’t have to deal with threads.
- JavaScript has a concurrency model based on an **event loop**, which is responsible for executing the code, collecting and processing events, and executing queued sub-tasks. This model is quite different from models in other languages like C and Java or C#.
- The event loop is what orchestrates concurrency model for handling multiple connections and the use of callbacks (the non-blocking nature of Node.js).
- The slow I/O operations are handled with events and callbacks so that they don't block the main single-threaded execution runtime.

> Event loop also exists in browsers.

![event-loop-1](assets/event-loop-1.png)

- The event loop that Node automatically starts when it executes a script
- This event loop is what makes the asynchronous callback programming style possible.
- Node will exit the event loop when there are no more callbacks to perform.
- To understand event loop, we need to understand all the players in this diagram and we need to understand how they interact.
- So V8 has this thing called stack & heap.
- The heap is simple, it is where objects are stored in memory.
- For example, when we invoke a function, an area in this heap is allocated to act as the local scope of that function.
- Both the Stack and the Heap are part of the run-time engine, not Node itself.- Node adds APIs like timers, emitters, and wrappers around OS operations.
- It also provides the event Queue and the event loop using the libuv library.
- The event loop, as the name says, is a simple loop that works between the event queue and the call stack.

### 9.4. V8's Call stack

In, general, a call stack is a simple first in last out stack data structure that stores information about the active subroutines (a function, task, method, procedure etc) of a computer program.

- The Call Stack is part of V8.
- It is the data structure that V8 uses to keep track of function invocations.
- Every time we invoke a function, V8 places a reference to that function on the call stack and it keeps doing so for each nested invocation of other functions.
- This also includes functions that call themselves recursively.
- When the nested invocations of functions reaches an end, V8 will pop one function at a time and use its returned value in its place.
- ONE Call Stack per Node process. If we keep that Call Stack busy, your whole Node process is busy (blocking).
- Since JavaScript is single threaded, there is only one stack, and it can do one thing at a time. If the stack is executing something, nothing else will happen in that single thread.

Ex,

```js
const add = (a, b) => a + b;

const double = (a) => add(a, a);

const printDouble = (a) => {
  const output = double(a);
  console.log(output);
};

printDouble(6); // prints 12
```

- When we call multiple functions that call each other, we naturally form a stack like below,
- When we run this code, V8 uses the stack to record where in the program it is currently executing. Every time we step into a function, it gets pushed to the stack, and every time we return from a function, it gets popped out of the stack. It's really that simple.
- When starts the executing the above code, it starts  global scope and executing whole code as anonymous IIFE.
- Only execution/invocation pushed to stack (printDouble), not declaration.

Let's diagram it,

![call-stack-1](assets/callstack-1.png)

Push

- Start with the IIFE call, which is an anonymous function.
- Push that to the stack. The IIFE function defines other functions, but only executes printDouble. That gets pushed to the stack.
- PrintDouble calls double, so we push double to the stack.
- double calls add, we push add to the stack.
- So far, we're still executing all functions. We have not returned from any of them.

Pop

- When we return from add, we pop add out of the stack. We're done with it.
- Then we return from double, so double gets popped out of the stack, too.
- Now, the execution continues in printDouble. We get into a new function call, `console.log`, that get's pushed into the stack and popped immediately, because it did not call any other functions.
- Then we implicitly return from printDouble, so we pop printDouble out of the stack.
- Finally pop the anonymous IIFE itself out of the stack.
- Note how every time a function is added to the stack, its arguments and local variables are added too in that same level.
- If a function is returns it handover the data bring to parent and exits from callstack like `double`

Let see this in practical, by introducing the error in above code.

In Node,

```js
const add = (a, b) => A + b;

const double = (a) => add(a, a);

const printDouble = (a) => {
  const output = double(a);
  console.log(output);
};

printDouble(6);

console.trace("Show me");
```

It shows.

![callstack-node-2](assets/callstack-node-2.png)

In Browser, added as a snippet

![callstack-browser-3](assets/callstack-browser-3.png)

What happens, if we have recursive call like below,

```js
const add = (a, b) => {
  add(a, b);
};

add(1, 2);
```

It's the equivalent of an infinite loop, but on the stack. We'll keep pushing the same function to the stack until we reach the V8 size limit for the stack, and V8 will error out with this error: **Uncaught RangeError: Maximum call stack size exceeded**

Q. Till now, whatever we had seen, all are quick executions, what about blocking or slow operations (loops, Timers, callback, events, network calls etc).Since javascript is single threaded, it will halt the execution of other function until it done with current execution, how to handle these slow operation.

### 9.5. Blocking the Node.js process

```js
const slowAdd = (x, y, label) => {
  console.time(`blocked-for-${label}`);
  for (let i = 0; i < 999999999; i++) {}
  console.timeEnd(`blocked-for-${label}`);
  return x + y;
};

const a = slowAdd(3, 3, "a");
const b = slowAdd(4, 4, "b");
const c = slowAdd(5, 5, "c");
console.log(a);
console.log(b);
console.log(c);

// blocked-for-a: 721.958ms
// blocked-for-b: 730.045ms
// blocked-for-c: 247.076ms
// 6
// 8
// 10
```

- The first time we step into it - `slowAdd`, it gets pushed to the stack, and then we wait until V8 finishes that useless blocking loop and returns from slowAdd(3, 3) which gets popped out of the stack at that point.
- Then we step into slowAdd 4 4, and we wait, done, return, pop.
- Same thing for slowAdd 5 5, wait, done, return, pop.
- Then we get into the console.log lines, which are fast and thus non blocking, so push, pop, push, pop, push, and pop.
- While Node (V8) is waiting after every slowAdd here, it cannot do anything else.
- Node process exits after this.

Q. Is this a blocking code?
A. YES AND NO

In general, this is not a blocking code in javascript, even if each invocation takes a long time before returning. Because it may taking that long time for image, video or in-memory file processing etc.

May be we can improve a bit using call back pattern. but ultimately it takes same time to operate.

```js
const slowAdd = (x, y, label, cb) => {
  console.time(`blocked-for-${label}`);
  for (let i = 0; i < 999999999; i++) {}
  console.timeEnd(`blocked-for-${label}`);
  const output = x + y;
  cb(output);
};

slowAdd(3, 3, "a", (data) => console.log(data));
slowAdd(4, 4, "b", (data) => console.log(data));
slowAdd(5, 5, "c", (data) => console.log(data));

// blocked-for-a: 734.099ms
// 6
// blocked-for-b: 729.062ms
// 8
// blocked-for-c: 488.683ms
// 10
```

Then, what and where the heck is blocking code/slow operations.

Let's write blocking code with Node.js perspective.

Node's Blocking code

```js
const slowAdd = (x, y) => {
  for (let i = 0; i < 999999999; i++) {}
  return x + y;
};

// Reads a file in a synchronous and blocking way
const data = require("fs").readFileSync(__filename);
console.log("file: ", data);

const a = slowAdd(3, 3);
console.log("a: ", a);

// file:  <Buffer 63 6f 20 3c ... 231 more bytes>
// a:  6
```

Let's diagram it,

![callstack-block](assets/callstack-block.png)

- Invoking the `slowAdd` is same earlier, this how it works, until it finishes, control will not go further.
- Why this?, because javascript is single threaded, and V8(call stack) si busy executing it, no other stuff is allowed.
- Then, we have this `readFileSync` also running, which is executing same as `slowAdd`
- One big difference between `slowAdd` and `readFileSync`, is slowAdd is completely getting executed on V8, but readFileSync start the invocation at JavaScript-land and it goes out of JavaScript-land/V8 to Node/C++/OS land to locate the file, load and parse file content.
- Once the data is ready, it again comes to JavaScript-land/V8 to print the data using `console.log("file: ", data);`

**When javascript execution in Node.js process has to wait until a non-javascript operation completes is called blocking.**

Node process is wasting the time unnecessarily waiting for file data while OS is preparing the file data.

This is blocking programming, and Node's event loop exists to allow us to avoid doing this style of programming.

So, what to do?

### 9.6. Non-Blocking the Node.js process

Let's use callback to solve this problem,

Node's Non-Blocking code

```js
const slowAdd = (x, y) => {
  for (let i = 0; i < 999999999; i++) {}
  return x + y;
};

// Reads a file in a asynchronous and non-blocking way
require("fs").readFile(__filename, (err, data) => {
  console.log("file: ", data);
});

const a = slowAdd(3, 3);
console.log("a: ", a);

// a:  6
// file:  <Buffer 63 6f 20 3c ... 231 more bytes>
```

**WOW... look at the order of logs.**

- Our code did not wait for file locate-load-parse to complete, instead it starts the invocation and moves on to execute the next line
- When file data is ready, Node/C++/libuv/event-loop pushed the `readFile` callback fn to V8 call stack for execution with file data as argument.

Non-Blocking
This is the opposite of the blocking i.e. javascript execution do not wait until the non-javascript operation completes.

Non-Javascript execution refers to mainly I/O operations. So, in the nutshell, I/O operations are blocking.

> Blocking methods execute synchronously and non-blocking methods execute asynchronously.|

But, how my callback fn get pushed to call stack, what if i have 10 files reading simultaneously, or other Node asynchronous API getting executed such as timers, network call, promises etc?

Who keeps track of all these I/O or asynchronous execution, orders of invocation, i.e. NON JavaScript-land executions.

Let diagram, above code execution.

![callstack-non-block](assets/callstack-non-block.png)

- This way Node.js uses the event loop and callback mechanism to lift off I/O operations from the javascript's thread to the system's kernel.
- Since most modern kernels are multi-threaded, they can handle multiple operations executing in the background concurrently (using libuv).
- When one of these operations completes, the kernel notifies Node.js and then the appropriate callback is eventually executed.
- First, it's important to understand that an API call like readFile, setTimeout, http is not part of V8. It's provided by Node itself, just like it's provided by browsers, too.
- Let's talk about the event queue, which is sometimes called the message queue or the callback queue. It's simply a list of things to be processed; let's call these things events.
- When we store an event on the queue, we sometimes store a plain-old function with it. This function is what we know as a callback. A queue data structure is a first in first out structure, so the first event we queue will be the first event to get de-queued.
- To de-queue and process an event from the edge of the queue, we just invoke the function associated with it. Invoking a function will push it to the stack.
- While the Node file read operation is running, the stack is free to continue processing its items.
- Once all the synchronous code done executing, and callstack is empty. Exactly at this moment, the event loop has something important to do. The event loop job is super simple. It monitors the call stack and the event queue. When the stack is empty, and the queue is not empty (there are events waiting to be processed in the queue), it will de-queue one event from the queue and push its callback to the stack. It's called an event loop, because it loops this simple logic until the event Queue is empty.
- Right now, our example's call stack is empty and the queue is not. The event loop will pick `cb`, and push it to the stack. `cb` will push console.log call to the stack, which returns immediately.
- Now, the stack is empty and the queue is empty. Node will exit the process when we reach this state.
- All Node APIs (I/O operation, timers, http, fs etc) work with this concept. Some process will go handle a certain I/O asynchronously, keeping track of a callback, and when it's done it will queue the callback into the event queue.
- Keep in mind that any slow code being executed on the stack directly will block the event loop.

> **For V8/Node/JavaScript execution environment, synchronous code is first priority to execute them, it takes the task/fn/callbacks from queue to execute.**

Pseudo code of Event Loop

```md
When call stack gets empty:
While the queue is not empty:
  event = dequeue an event
  if there is a callback in dequeued event:
    invoke the event's callback
```

Event loop challenges:

Ex - 1

```js
setTimeout(() => {
  console.log(0);
}, 1000);

const one = () => {
  console.log(1);
};

console.log(2);

one();

/* Prints
2 1 0
*/
```

Ex - 2
Usually, Node has other API such as timers, promise, callback etc. when these asynchronous operation is completed, which there is a rule for event loop to pick and push the callbacks/fn to call stack.

**Node's Event Loop Phases** <!-- omit in toc -->

![event-loop-phases](assets/event-loop-phases.png)

**Theses phases run as shown in the above order.**

1. **Poll**

    This is the first phase that gets executed, the I/O callbacks gets executed in this phase. Retrieve new I/O events; execute I/O related callbacks (almost all with the exception of close callbacks, the ones scheduled by timers, and setImmediate())

2. **Check**

    This is the second phase in which `setImmediate()` callbacks gets executed.

3. **Close callbacks**

    The callbacks related to EventEmitter close events gets executed in this third phase. some close callbacks, e.g. `socket.on('close', ...)`.

4. **Timers**

    Callbacks related to timers, `setTimeout()` and `setInterval()` gets executed in this phase.

5. **Pending callbacks**

    Callbacks related to some system operations such as TCP errors executed in this phase. Eg:- ECONNREFUSED during TCP socket connection failure.

In addition to above phases there are two more special microtask queues, these microtask queues takes highest priority than above phases. **First microtask queue contains callbacks related to process.nextTick() and the second microtask queue handles promises. Among these two microtask queues, process.nextTick() has higher priority.**

Let's consider below example to understand the priority of the queues execution.

```js
const one = () => {
  console.log(1);
};

Promise.resolve().then(() => console.log(2));

require("fs").readFile(__filename, () => console.log(3));

setTimeout(() => console.log(4), 1000);

process.nextTick(() => console.log(5));

setImmediate(() => console.log(6));

console.log(7);

one();

/* Prints
7 1 5 2 6 3 4
*/
```

- First 7 gets printed as it is synchronous code in global context.
- Next one() function gets called and prints 1, again its a synchronous code.
- Now as explained above `process.nextTick()` microtask queue has highest priority, so the callback in this queue gets executed which prints 5.
- Next priority will be `Promise` microtask queue which prints 2.
- This completes the current poll phase.
- Although fs.readFile is part of the poll phase the callback won't be placed immediately in the queue in the current poll phase as file reading takes some time, so only in the next poll phase the callback related to readFile will be executed.
- Now the event loop enters check phase which executes setImmediate callback, so it prints 6.
- There is no code related to Close phase.
- So the it enters next phase which is timers, although there is a callback function related to setTimeout place in timers queue it won't be executed as there is a wait time of 1000 ms, so this will be executed only in the next cycle.
- There is no callbacks related to pending phase which concludes the first cycle.
- Now again the second cycle begins in which the event loop again enters poll phase and prints 3 and then goes through the same phases.
- And finally prints 4 that got placed in the timers queue.
- So the final output is 7 1 5 2 6 3 4.

## 10. Error handling in Node.js

### 10.1. Creating exceptions

An exception is created using the **throw** keyword:

```js
throw value
```

As soon as JavaScript executes this line, the normal program flow is halted and the control is held back to the nearest **exception handler**.

In Node.js, we just throw Error objects.

### 10.2. Error objects

An error object is an object that is either an instance of the **Error object**, or extends **the Error class**.

```js
throw new Error('account balance low')
```

or

```js
class LowBankBalanceError extends Error {
  //...
}
throw new LowBankBalanceError()
```

### 10.3. Handling exceptions

An exception handler is a **try/catch** statement.

scene-1

```js
const divide = (a, b) => {
  let result;

  try {
    if (b === 0) throw new Error("Cannot be divisible by 0");

    result = a / b;
  } catch (error) {
    console.log(error.message);
  }
  result;
};
divide(9, 0);
// Cannot be divisible by 0
```

scene-2, propagating the error to calling code.

```js
const divide = (a, b) => {
  let result;

  try {
    if (b === 0) throw new Error("Cannot be divisible by 0");

    result = a / b;
  } catch (error) {
    console.log("Handling at locally => ", error.message);
    throw error;
  }
  result;
};

const processData = (a, b) => {
  try {
    divide(a, b);
  } catch (error) {
    console.log("Propagated outside/upper => ", error.message);
  }
};

processData(0, 0);

// Handling at locally =>  Cannot be divisible by 0
// Propagated outside/upper =>  Cannot be divisible by 0
```

### 10.4. Catching uncaught exceptions

If an uncaught exception gets thrown during the execution of your program, your program will crash.

To solve this, you listen for the uncaughtException event on the process object:

```js
process.on("uncaughtException", (err) => {
  console.error("There was an uncaught error", err);
  process.exit(1);
});
```

scene-3

- try passing invalid path
- try passing valid encoding fs.readFileSync(path, 'utf-8')
- try passing invalid encoding fs.readFileSync(path, 'utf-8090')

```js
const fs = require("fs");

try {
  const data = fs.readFileSync(
    "C:\\Users\\avigo\\Dropbox\\tech-notes\\node\\node-notes\\Node.js - Course Curriculum.md"
  );
  console.log("File data is", data);
} catch (err) {
  if (err.code === "ENOENT") {
    console.log("File not found");
  } else {
    throw err;
  }
}
```

### 10.5. Error first callbacks

### 10.6. Exceptions with promises

### 10.7. Error handling with async/await

Ex1.

> As we see in the above example, when error happens node process will crash and exit. But what happens in Production if the process exits??  
> Usually in prod, we will not be having a single process running, we will be having cluster of node processes.  
> Normally setup would be, a master process will monitor all the worker processes, when one is down. A master can create more.  
> In prod, lets say we have 4 cores processors running, then we can have 4 processes running on each core.
> PM2 - `https://pm2.keymetrics.io/` is such tool to manage node processes in prod env.
> PM2 uses built-in node's **cluster** module.
> PM2 will automatically uses the all processors available in OS and spawn processes accordingly.

## 11. Async Pattern Evolution

### 11.1. Synchronous code

Below code snippet is blocking/slow operation, that doesn't use event loop instead directly uses OS synchronous file reading api.  
Observe the order of console.logs

```js
const fs = require("fs");

const data = fs.readFileSync(__filename);
console.log("File binary data is", data);
console.log("Hi");

// File binary data is <Buffer 63 6f ... 89 more bytes>
// Hi
```

### 11.2. Callback pattern - Asynchronous

This uses the event loop to process the file asynchronously.  
Once the file completed reading the data,OS will invoke the callback function by passing the arguments.

```js
const fs = require("fs");

fs.readFile(__filename, function cb(err, data) {
  console.log("File binary data is", data);
});
console.log("Hi");

// Hi
// File binary data is <Buffer 63 6f ... 101 more bytes>
```

Callback hell (Pyramid of doom)

Create a copy of a file

```js
const fs = require("fs");

fs.readFile(__filename, function cb1(err, data) {
  fs.writeFile(__filename + ".copy", data, function cb2(err) {
    // Nest more callbacks here...
  });
});

console.log("Hi");
```

### 11.3. Promise pattern - Asynchronous

Node.js was handling all the async operation using callbacks only; but with the advent of promises in javascript, now it has given us the tools/utility to program using promise based apis.

Promise pattern - 1

```js
const fs = require("fs");
const util = require("util");

const readFile = util.promisify(fs.readFile);

readFile(__filename).then((data) => {
  console.log("File binary data is", data);
});

console.log("Hi");

// Hi
// File binary data is <Buffer 2f 75 ... 456 more bytes>
```

Promise pattern - 2

```js
const { readFile } = require("fs").promises;
// const { readFile } = require("fs/promises");

readFile(__filename).then((data) => {
  console.log("File binary data is", data);
});

console.log("Hi");

// Hi
// File binary data is <Buffer 63 63 ... 158 more bytes>
```

### 11.4. async/await pattern - Asynchronous

```js
const { readFile } = require("fs/promises");

const run = async () => {
  const data = await readFile(__filename);
  console.log("File binary data is", data);
};
run();
console.log("Hi");

// Hi
// File binary data is <Buffer 63 6f ... 150 more bytes>
```

How it solves the callback hell problem??

```js
const { readFile, writeFile } = require("fs/promises");

const copyFile = async () => {
  const data = await readFile(__filename);
  await writeFile(__filename + ".copy", data);
};
copyFile();
```

> promises => fs/promises, this api may not be available for all the built-in modules.

## 12. Event-Driven Architecture - Event Emitters

Consider, a DOM Event,

```js
const button = document.querySelector("button");
button.addEventListener("click", (event) => {
  /* do something with the event */
});
```

We added a listener to a button **click**. We’ve **subscribed** to an event being **emitted** and we fire a **callback** when it does. Every time we click that button, that event is emitted and our callback fires with the event.

Let's say we want to fire a custom event, not specifically a DOM event like clicking a button, but
want to emit an event based on some other trigger like *open* a file, *close* a file, *finish* etc and have an event to respond.  
We need a custom event emitter to do that.

### 12.1. Enter Node's **Event Emitters**

emitter objects emit named events that cause previously registered listeners to be called. So, an emitter object basically has two main features:

- Emitting name events.
- Registering and un-registering listener functions.

**EventEmitter** is a class which is used to provide a consistent interface for emitting (triggering) and binding callbacks to events.

The **eventEmitter.on()** method is used to register listeners, while the **eventEmitter.emit()** method is used to trigger the event.

```js
const EventEmitter = require("events"); // IMPORT

const eventEmitter = new EventEmitter(); // INIT

eventEmitter.on("open", (data) => { // LISTENER
  console.log(data);
});
eventEmitter.on("open", (data) => {
  console.log(data);
});
eventEmitter.on("close", (data) => {
  console.log(data);
});

eventEmitter.emit("open", "connection opened"); // EMIT
```

We can achieve above functionality using plain code with callback pattern, but, benefit of using events instead of regular callbacks is that we can react to the same signal multiple times by defining multiple listeners. To accomplish the same with callbacks, we have to write more logic inside the single available callback.

Much of the Node.js core API like HTTP requests, responses, and streams (process.stdin,process.stdout etc), fs are implemented (inherit) the EventEmitter module so they can provide a way to emit and listen to events.

Initially Node handled asynchronous events was with callbacks. Now it supports promises and the async/await feature.

callbacks do not guarantee an asynchronous call in the code. A function can call the callback both synchronously and asynchronously.

### 12.2. Synchronous Events

Usually we don't use EventEmitter class directly instead we inherit (extend) and use it. like below.

```js
const EventEmitter = require("events");

class WithLog extends EventEmitter {
  execute(taskFunc) {
    console.log("Before executing");
    this.emit("begin");
    taskFunc();
    this.emit("end");
    console.log("After executing");
  }
}

const withLog = new WithLog();

withLog.on("begin", () => console.log("About to execute"));
withLog.on("end", () => console.log("Done with execute"));

withLog.execute(() => console.log("*** Executing task ***"));

/*
Prints

Before executing
About to execute
*** Executing task ***Done with execute
After executing
*/
```

Class `WithLog` is an event emitter. It defines one instance function `execute`. This execute function receives one argument, a task function, and wraps its execution with log statements. It fires events before and after the execution.

If we look at the output, it all happens synchronously

- We get the *Before executing* line first.
- The `begin` named event then causes the "About to execute" line.
- The actual execution line then outputs the *Executing task* line.
- The `end` named event then causes the "Done with execute" line
- We get the "After executing" line last.

Just like callbacks, do not assume that events mean synchronous or asynchronous code.

Let's demonstrate it, replace emit code with below snippet.  
Since if we pass an asynchronous (timer) taskFunc to execute, the events emitted will no longer be accurate.

```js
withLog.execute(() => {
  setImmediate(() => {
    console.log("*** Executing task ***");
  });
});

/*
Prints

Before executing
About to execute
Done with executeAfter executing
*** Executing task ***
*/
```

This is wrong. The lines after the async call, which were caused the "Done with execute" and "After executing" calls, are not accurate any more.

### 12.3. Asynchronous Events

```js
const fs = require("fs");
const EventEmitter = require("events");

class WithTime extends EventEmitter {
  execute(asyncFunc, ...args) {
    this.emit("begin");
    console.time("execute");
    asyncFunc(...args, (err, data) => {
      if (err) {
        return this.emit("error", err);
      }

      this.emit("data", data);
      console.timeEnd("execute");
      this.emit("end");
    });
  }
}

const withTime = new WithTime();

withTime.on("begin", () => console.log("About to execute"));
withTime.on("end", () => console.log("Done with execute"));
withTime.on("data", (data) => console.log(data));

withTime.execute(fs.readFile, __filename);

/*
Prints

About to execute
<Buffer 63 6f 6 ...
execute: 5.805ms
Done with execute
*/
```

The `WithTime` class executes an `asyncFunc` and reports the time that’s taken by that asyncFunc using console.time and console.timeEnd calls. It emits the right sequence of events before and after the execution. And also emits error/data events to work with the usual signals of asynchronous calls.

We test a `withTime` emitter by passing it an `fs.readFile` call, which is an asynchronous function. Instead of handling file data with a callback, we can now listen to the data event.

Same code with async wait pattern,

```js
const fs = require("fs/promises");
const EventEmitter = require("events");

class WithTime extends EventEmitter {
  async execute(asyncFunc, ...args) {
    this.emit("begin");
    try {
      console.time("execute");
      const data = await asyncFunc(...args);
      this.emit("data", data);
      console.timeEnd("execute");
      this.emit("end");
    } catch (err) {
      this.emit("error", err);
    }
  }
}

const withTime = new WithTime();

withTime.on("begin", () => console.log("About to execute"));
withTime.on("end", () => console.log("Done with execute"));
withTime.on("data", (data) => console.log(data));
withTime.execute(fs.readFile, __filename);

/*
Prints

About to execute
<Buffer 63 6f 6e  6d 69 ... 712 more bytes>
execute: 4.514msDone with execute
*/
```

### 12.4. Events Arguments and Errors

As we see in the above code, the error event is emitted with an error object.

```js
this.emit('error', err);
```

The data event is emitted with a data object.

```js
this.emit('data', data);
```

We can use as many arguments as we need after the named event, and all these arguments will be available inside the listener functions we register for these named events.

Listener function that we register will get access to the data argument that was passed to the emitted event

```js
withTime.on("data", (data) => console.log(data));
```

The `error` event is usually a special one. In our callback-based example, if we don’t handle the error event with a listener, the node process will actually exit.

demo,

```js
const fs = require("fs");
const EventEmitter = require("events");

class WithTime extends EventEmitter {
  execute(asyncFunc, ...args) {
    console.time("execute");
    asyncFunc(...args, (err, data) => {
      if (err) {
        return this.emit("error", err);
      }
      console.timeEnd("execute");
    });
  }
}

const withTime = new WithTime();

withTime.execute(fs.readFile, "abcd");
withTime.execute(fs.readFile, __filename);

/*
events.js:292
      throw er; // Unhandled 'error' event      ^

Error: ENOENT: no such file or directory open:.../abcd
*/
```

The node process is going to crash and exit.The second execute call will be affected by this crash and will potentially not get executed at all.

If we register a listener for the special `error` event, the behavior of the node process will change. For example:

```js
const fs = require("fs");
const EventEmitter = require("events");

class WithTime extends EventEmitter {
  execute(asyncFunc, ...args) {
    console.time("execute");
    asyncFunc(...args, (err, data) => {
      if (err) {
        return this.emit("error", err);
      }
      console.timeEnd("execute");
    });
  }
}

const withTime = new WithTime();

withTime.on("error", (err) => {
  console.log(err);
});

withTime.execute(fs.readFile, "abcd");
withTime.execute(fs.readFile, __filename);

/*
[Error: ENOENT: no such file or directory, open 'C\\..\\abcd'] {
  errno: -4058,
  code: 'ENOENT',
  syscall: 'open',
  path: 'C\\..\\abcd'
}
execute: 13.032ms
*/
```

If we do the above, the error from the first execute call will be reported but the node process will not crash and exit. The other execute call will finish normally.

### 12.5. Order of Listeners

If we register multiple listeners for the same event, the invocation of those listeners will be in order. The first listener that we register is the first listener that gets invoked.

Ex-1

```js
const fs = require("fs");
const EventEmitter = require("events");

class WithTime extends EventEmitter {
  execute(asyncFunc, ...args) {
    asyncFunc(...args, (err, data) => {
      this.emit("data", data);
    });
  }
}

const withTime = new WithTime();

withTime.on("data", (data) => {
  console.log(`Length: ${data.length}`);
});

withTime.on("data", (data) => {
  console.log(`Characters: ${data.toString().length}`);
});

withTime.execute(fs.readFile, __filename);

/*
Length: 493
Characters: 493
*/
```

Ex-2

```js
const fs = require("fs");
const EventEmitter = require("events");

class WithTime extends EventEmitter {
  execute(asyncFunc, ...args) {
    asyncFunc(...args, (err, data) => {
      this.emit("data", data);
    });
  }
}

const withTime = new WithTime();

withTime.on("data", (data) => {
  console.log(`Characters: ${data.toString().length}`);
});

withTime.on("data", (data) => {
  console.log(`Length: ${data.length}`);
});

withTime.execute(fs.readFile, __filename);

/*
Characters: 533
Length: 533
*/
```

Challenge

What is output of below code.

```js
const EventEmitter = require("events");
const eventEmitter = new EventEmitter();
eventEmitter.emit("open", "connection opened");
eventEmitter.on("open", (data) => {
  console.log(data);
});
```

> Hint: We are emitting before subscribing/registering to en event.

## 13. Web Server (http)

### 13.1. Create an HTTP server

```js
const http = require("http");

// requestListener
const eventHandler = (req, res) => {
  // req: http.IncomingMessage
  // res: http.ServerResponse

  res.writeHead(200, { "content-type": "text/plain" });
  res.write("Hello World");
  res.end();
};

const server = http.createServer(); // // server: http.Server
server.on("request", eventHandler);

server.listen(3005, () => {
  console.log("Server is up and running at port 3005 !!");
});

/*
> curl -i localhost:3005

HTTP/1.1 200 OK
content-type: text/plain
Date: Mon, 24 Jan 2022 02:51:25 GMT
Connection: keep-alive
Keep-Alive: timeout=5
Transfer-Encoding: chunked
*/
```

What?

- `require()` fn will import the http built-in module and assign it to `http` const.
- To create a http server, we use `createServer` method.
- The server it created actually extends the `EventEmitter` Class, so we can emit an event and subscribe to it.
- The event we are subscribing is **request** and lister fn is **eventHandler**
- `server.listen(port)` is what opens the socket at given port and waits for incoming http requests/calls.

How it works?

- When we run server/code `node index.js`, node will start the event loop and start listening to incoming http messages.
- Let's call `curl localhost:3005`
- When a machine receives this call, the request arrives at port number 3005
- Node.js/C++(OS) will parse the incoming HTTP request/message and prepares the req and res object.
- Now Node.js/C++ (OS) will emit the `request` event and call push eventHandler callback to the event loop(thru' queue) by passing the 2 positional arguments to it.
- After JavaScript(V8) done executing the code and it calls res.end(), this signals the Node/C++ land, that i am done.
- Once `res.end()` executes, JavaScript will handover the control to Node/C++ land.
- Node/C++ is now responsible for streaming the http message(response) to client.

Shorter version ( not readable one)

```js
const { createServer } = require("http");

createServer((req, res) => {
  res.end("Hello World");
}).listen(3005);

// curl localhost:3005
// Hello World
```

> Use nodemon package to restart the server whenever we change the code while developing the app.  
> `npm install -g nodemon`  
> Then just use `nodemon index.js`

### 13.2. Peek into res & req objects

```js
const eventHandler = (req, res) => {
  res.write("Hello World");
  res.end();
  console.dir(req, { depth: 0 });
  console.dir(res, { depth: 0 });
};
```

```json
IncomingMessage {
  _readableState: [ReadableState],
  _events: [Object: null prototype],
  _eventsCount: 1,
  _maxListeners: undefined,
  socket: [Socket],
  httpVersionMajor: 1,
  httpVersionMinor: 1,
  httpVersion: '1.1',
  complete: false,
  headers: [Object],
  rawHeaders: [Array],
  trailers: {},
  rawTrailers: [],
  aborted: false,
  upgrade: false,
  url: '/',
  method: 'GET',
  statusCode: null,
  statusMessage: null,
  client: [Socket],
  _consuming: false,
  _dumped: false,
  [Symbol(kCapture)]: false,
  [Symbol(RequestTimeout)]: undefined
}
ServerResponse {
  _events: [Object: null prototype],
  _eventsCount: 1,
  _maxListeners: undefined,
  outputData: [],
  outputSize: 0,
  writable: true,
  destroyed: false,
  _last: false,
  chunkedEncoding: true,
  shouldKeepAlive: true,
  _defaultKeepAlive: true,
  useChunkedEncodingByDefault: true,
  sendDate: true,
  _removedConnection: false,
  _removedContLen: false,
  _removedTE: false,
  _contentLength: null,
  _hasBody: true,
  _trailer: '',
  finished: true,
  _headerSent: true,
  socket: [Socket],
  _header: 'HTTP/1.1 200 OK\r\n' +
    'Date: Wed, 29 Dec 2021 10:27:43 GMT\r\n' +
    'Connection: keep-alive\r\n' +
    'Keep-Alive: timeout=5\r\n' +
    'Transfer-Encoding: chunked\r\n' +
    '\r\n',
  _keepAliveTimeout: 5000,
  _onPendingData: [Function: bound updateOutgoingData],
  _sent100: false,
  _expect_continue: false,
  statusMessage: 'OK',
  statusCode: 200,
  [Symbol(kCapture)]: false,
  [Symbol(kNeedDrain)]: false,
  [Symbol(corked)]: 0,
  [Symbol(kOutHeaders)]: null
}
```

- req is of type or class  => http.IncomingMessage  
Full details - `https://nodejs.org/api/http.html#class-httpincomingmessage`

- res is of type or class  => http.ServerResponse  
Full details - `https://nodejs.org/api/http.html#class-httpserverresponse`

Most used props of these objects are url, statusCode, StatusMessage, Headers, body etc.

> res and req both are Streams and streams are intern extends EventEmitter.  
> req - readable stream => http.IncomingMessage
> res - writable stream => http.ServerResponse

### 13.3. Streaming in HTTP server

Node's HTTP module is designed with streaming and low latency in mind.

We see two special headers of Node HTTP server,

`Connection: keep-alive` => this means that the connection to the web server will be persisted. The tcp connection will not be killed after a requester receives a response, so that they can send multiple requests on the same connection.

`Transfer-Encoding: chunked` => is used to send a variable length response text. It basically means that the response is being streamed! Node is ok with us sending partial chunked responses, because the response object is a writable stream.

- After Node sends the 200 ok here, it can do many other things before terminating the response
- Instead of inefficiently buffering everything it wants to write in memory and then write it at once, it can just stream parts of the response as they're ready.
Example, stream video, audio files out of the box.

Ex-1

```js
const http = require("http");

// requestListener
const eventHandler = (req, res) => {
  res.writeHead(200, { "content-type": "text/plain" });
  res.write("1\n");
  setTimeout(() => {
    res.write("2\n");
  }, 4000);

  setTimeout(() => {
    res.write("3\n");
  }, 5000);

  setTimeout(() => {
    res.end("I will terminate the response object.\n");
  }, 9000);
};

const server = http.createServer();
server.on("request", eventHandler);

server.listen(3005, () => {
  console.log("Server is up and running at port 3005 !!");
});
/*
> curl -i localhost:3005
1
2
3
I will terminate the response object.
*/
```

Ex-1, Practically lets stream a file content, assuming a large file

```js
const http = require("http");
const fs = require("fs");

// requestListener
const eventHandler = (req, res) => {
  res.writeHead(200, { "content-type": "text/plain" });
  const fileStream = fs.ReadStream(__filename);
  fileStream.on("data", (content) => {
    res.write(content);
  });
  fileStream.on("end", () => {
    res.end();
  });
};

const server = http.createServer();
server.on("request", eventHandler);

server.listen(3005, () => {
  console.log("Server is up and running at port 3005 !!");
});

> curl -i localhost:3005
```

> Note here, server is not blocked (event loop). it is streaming the data, we can do multiple calls to server to prove this.

### 13.4. Making HTTP requests with Node.js

Lets, say we want to connect to another REST service and fetch the content right from our server.

GET request

```js
const http = require("http");

const options = {
  hostname: "jsonplaceholder.typicode.com",
  path: "/posts/1",
  method: "GET",
};

// req: http.ClientRequest
const req = http.request(options, (res) => {
  // res: http.ServerResponse

  console.log(`statusCode: ${res.statusCode}`);
  console.log(`headers:`, JSON.stringify(res.headers, null, 2));

  res.on("data", (d) => console.log(d.toString()));
});

req.on("error", (error) => console.error(error));

req.end(); // closing the stream or request

/*
statusCode: 200
headers: {
  "date": "Mon, 24 Jan 2022 04:31:34 GMT",
  "content-type": "application/json; charset=utf-8",
  "content-length": "292",
  "connection": "close",
  "x-powered-by": "Express",
  "x-ratelimit-limit": "1000",
  "x-ratelimit-remaining": "999",  "x-ratelimit-reset": "1642579683",
  "vary": "Origin, Accept-Encoding",  "access-control-allow-credentials": "true",
  "cache-control": "max-age=43200",
  "pragma": "no-cache",  "expires": "-1",  "x-content-type-options": "nosniff",  "etag": "W/\"124-yiKdLzqO5gfBrJFrcdJ8Yq0LGnU\"",  "via": "1.1 vegur",
  "cf-cache-status": "HIT",  "age": "27765",  "accept-ranges": "bytes",
  "server": "cloudflare",
  "cf-ray": "6d26886e4eca8b03-BOM",
  "alt-svc": "h3=\":443\"; ma=86400, h3-29=\":443\"; ma=86400"
}
{
  "userId": 1,
  "id": 1,
  "title": "sunt....",
  "body": "quia et.."
}
*/
```

POST request

```js
const http = require("http");

const postData = JSON.stringify({
  title: "foo",
  body: "bar",
  userId: 1,
});

const options = {
  hostname: "jsonplaceholder.typicode.com",
  path: "/posts",
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    "Content-Length": Buffer.byteLength(postData),
  },
};

// req: http.ClientRequest
const req = http.request(options, (res) => {
  // res: http.ServerResponse
  res.on("data", (d) => console.log(d.toString()));
  res.on("end", () => console.log("No more data in response."));
});

req.on("error", (error) => console.error(error));

// Write data to request body
req.write(postData);
req.end();

/*
{
  "title": "foo",
  "body": "bar",
  "userId": 1,
  "id": 101
}
No more data in response.
*/
```

http.Agent

When to do network calls in a browser (Agent), browser is responsible for managing the call and setting some default configuration for each requests.

Likewise, in node all these will be taken care by `http.Agent`.

An `Agent` is responsible for managing connection persistence and reuse for HTTP clients.

We also can override the default configurations while sending the request just like in browser, as shown below.

```js
const http = require("http");

const keepAliveAgent = new http.Agent({ keepAlive: true });

const options = {
  agent: keepAliveAgent,
  hostname: "www.google.com",
};

// req: http.ClientRequest
const req = http.request(options, (res) => {});
req.end();

// http.Agent
console.log(req.agent);

/**
 Agent {
  _events: [Object: null prototype] {
    free: [Function (anonymous)],
    newListener: [Function: maybeEnableKeylog]
  },
  _eventsCount: 2,
  _maxListeners: undefined,
  defaultPort: 80,
  protocol: 'http:',
  options: { keepAlive: true, path: null },
  requests: {},
  sockets: { 'www.google.com:80:': [ [Socket] ] },
  freeSockets: {},
  keepAliveMsecs: 1000,
  keepAlive: true,
  maxSockets: Infinity,
  maxFreeSockets: 256,
  scheduling: 'fifo',
  maxTotalSockets: Infinity,
  totalSocketCount: 1,
  [Symbol(kCapture)]: false
}
 */
```

We often see below two libraries are used in most of the Node.js apps for doing network calls using promised based APIs instead of `http.request`

> [node-fetch](https://www.npmjs.com/package/node-fetch)  
> [axios](https://www.npmjs.com/package/axios)

### 13.5. Routing

```js
// home.html
<h1>Home</h1>
```

```js
// about.html
<h1>About</h1>
```

index.js

```js
const fs = require("fs");
const server = require("http").createServer();
const data = {
  users: ["batman", "iron man"],
};

server.on("request", (req, res) => {
  switch (req.url) {
    case "/api/users":
      res.writeHead(200, { "Content-Type": "application/json" });
      res.end(JSON.stringify(data));
      break;
    case "/home":
    case "/about":
      res.writeHead(200, { "Content-Type": "text/html" });
      res.end(fs.readFileSync(`.${req.url}.html`));
      break;
    case "/":
      res.writeHead(301, { Location: "/home" });
      res.end();
      break;
    default:
      res.writeHead(404);
      res.end();
  }
});

server.listen(3005);
```

```md
Server

> node index.js

Client

> curl -i localhost:3005/api/users
HTTP/1.1 200 OK
Content-Type: application/json
Date: Mon, 24 Jan 2022 05:32:29 GMT
Connection: keep-alive
Keep-Alive: timeout=5Transfer-Encoding: chunked

{"users":["batman","iron man"]}

> curl -i localhost:3005/home     
HTTP/1.1 200 OK
Content-Type: text/html
Date: Mon, 24 Jan 2022 05:33:13 GMT
Connection: keep-alive
Keep-Alive: timeout=5Transfer-Encoding: chunked

<h1>Home</h1>

> curl -i localhost:3005/about
HTTP/1.1 200 OK
Content-Type: text/html
Date: Mon, 24 Jan 2022 05:33:28 GMT
Connection: keep-alive
Keep-Alive: timeout=5
Transfer-Encoding: chunked

<h1>About</h1>

> curl -i localhost:3005      
HTTP/1.1 301 Moved Permanently
Location: /home
Date: Mon, 24 Jan 2022 05:33:46 GMT
Connection: keep-alive
Keep-Alive: timeout=5
Transfer-Encoding: chunked

> curl -i localhost:3005/abcb
HTTP/1.1 404 Not Found
Date: Mon, 24 Jan 2022 05:33:58 GMT
Connection: keep-alive
Keep-Alive: timeout=5
Transfer-Encoding: chunked

```

> REPL - http.STATUS_CODES

### 13.6. URLs and Query Strings

The `url` module provides APIs for working with URLs. When parsed, a URL object is returned containing properties for each of these components.

``` md
REPL - url

{
  Url: [Function: Url],
  parse: [Function: urlParse],
  resolve: [Function: urlResolve],
  resolveObject: [Function: urlResolveObject],
  format: [Function: urlFormat],
  URL: [class URL],
  URLSearchParams: [class URLSearchParams],
  domainToASCII: [Function: domainToASCII],
  domainToUnicode: [Function: domainToUnicode],
  pathToFileURL: [Function: pathToFileURL],
  fileURLToPath: [Function: fileURLToPath]
}
```

URL anatomy

![url-anatomy](assets/url-anatomy.png)

```js
const paredUrlObj = new URL(
  "https://user:pass@sub.example.com:8080/p/a/t/h?query=string#hash"
);

console.log(paredUrlObj);
```

```md
URL {
  href: 'https://user:pass@sub.example.com:8080/p/a/t/h?query=string#hash',
  origin: 'https://sub.example.com:8080',
  protocol: 'https:',
  username: 'user',
  password: 'pass',
  host: 'sub.example.com:8080',
  hostname: 'sub.example.com',
  port: '8080',
  pathname: '/p/a/t/h',
  search: '?query=string',
  searchParams: URLSearchParams { 'query' => 'string' },
  hash: '#hash'
}
```

Ex,

```js
const paredUrlObj = new URL(
  "https://www.amazon.com/Atomic-Habits-Proven-Build-Break/dp/0735211299/?_encoding=UTF8&pd_rd_w=BCpfg"
);

console.log(paredUrlObj);
console.log("qs: ", paredUrlObj.searchParams);
console.log("_encoding: ", paredUrlObj.searchParams.get("_encoding"));
```

Prints,

```md
URL {
  href: 'https://www.amazon.com/Atomic-Habits-Proven-Build-Break/dp/0735211299/?_encoding=UTF8&pd_rd_w=BCpfg',
  origin: 'https://www.amazon.com',
  protocol: 'https:',
  username: '',
  password: '',
  host: 'www.amazon.com',
  hostname: 'www.amazon.com',
  port: '',
  pathname: '/Atomic-Habits-Proven-Build-Break/dp/0735211299/',
  search: '?_encoding=UTF8&pd_rd_w=BCpfg',
  searchParams: URLSearchParams { '_encoding' => 'UTF8', 'pd_rd_w' => 'BCpfg' },
  hash: ''
}
qs:  URLSearchParams { '_encoding' => 'UTF8', 'pd_rd_w' => 'BCpfg' }
_encoding:  UTF8
```

[Node's url module documentation](https://nodejs.org/api/url.html)

## 14. Node.js with OS - os module

The os module provides operating system-related utility methods and properties. It can be accessed using:  
`const os = require('os');`

[Node's os module documentation](https://nodejs.org/api/os.html)

```js
const os = require("os");

console.log("User info", os.userInfo());

// {
//   uid: -1,
//   gid: -1,
//   username: 'avinash',
//   homedir: 'C:\\Users\\avigo',
//   shell: null
// }

console.log("Name of the machine:", os.hostname()); // MSI

console.log("OS platform:", os.platform()); // OS platform: win32

console.log("OS CPU architecture:", os.arch()); // OS CPU architecture: x64

console.log("# of logical CPU cores", os.cpus().length); // # of logical CPU cores 12

console.log("Home directory for current user", os.homedir()); // Home directory for current user C:\Users\avigo

// The operating system-specific end-of-line marker.

// \n on POSIX (unix like)
// \r\n on Windows

console.log("line 1" + os.EOL + "line 2" + os.EOL + "line 3");

// line 1
// line 2
// line 3
```

## 15. Node.js with File system - fs module

The fs module enables interacting with the file system. It can be accessed using:  
`const fs = require('fs');`

[Node's fs module documentation](https://nodejs.org/api/fs.html)

The `path` module provides utilities for working with file and directory paths. It can be accessed using:

`const path = require('path');`

### 15.1. Create & Read files

`writeFile` - Asynchronously writes data to a file, replacing the file if it already exists.

`readFile` - Asynchronously reads the entire contents of a file. If options is a string, then it specifies the encoding.

```js
const { writeFile, readFile } = require("fs/promises");
const path = require("path");

writeFile("test.txt", "Hello").then((data) => {
  console.log("File created successfully!");
});

const absFilePath = path.join(__dirname, "test.txt");
readFile(absFilePath, "utf-8").then((data) => {
  console.log("with encoding: ", data);
});

readFile(absFilePath).then((data) => {
  console.log("without encoding: ", data);
});

// File created successfully!
// without encoding:  <Buffer 48 65 6c 6c 6f>
// with encoding:  Hello
```

### 15.2. Delete files

`unlink` - Removes/Deletes a file

```js
const absFilePath = path.join(__dirname, "test.txt");
unlink(absFilePath).then((data) => {
  console.log("A file deleted");
});
// A file deleted
```

> We are using Promise APIs in all above places.By default all the APIs are asynchronous.  
> There is also equivalent sync APIs for each one.  
> All above can be achieved thru' callback and async/await patterns also.

Ex, more `fs` challenges like, automation such as watch files, delete files older than 1-year, manipulate files data etc.

## 16. console module

The `console` module provides a simple debugging console that is similar to the JavaScript console mechanism provided by web browsers.

The module exports two specific components:

- A `Console` class with methods such as `console.log()`, `console.error()` and `console.warn()` that can be used to write to any Node.js stream.
- A global `console` (what we been using till now) instance configured to write to `process.stdout` and `process.stderr`.
- The global console can be used without calling require('console').

console object api

```md
REPL console

Object [console] {
  log: [Function: log],
  warn: [Function: warn],
  dir: [Function: dir],
  time: [Function: time],
  timeEnd: [Function: timeEnd],
  timeLog: [Function: timeLog],
  trace: [Function: trace],
  assert: [Function: assert],
  clear: [Function: clear],
  count: [Function: count],
  countReset: [Function: countReset],
  group: [Function: group],
  groupEnd: [Function: groupEnd],
  table: [Function: table],
  debug: [Function: debug],
  info: [Function: info],
  dirxml: [Function: dirxml],
  error: [Function: error],
  groupCollapsed: [Function: groupCollapsed],
  Console: [Function: Console],
  profile: [Function: profile],
  profileEnd: [Function: profileEnd],
  timeStamp: [Function: timeStamp],
  context: [Function: context]
}
```

Lets do a thing, `console` writes to terminal using `process.stdout` stream. Same way create one more version of console where we write it to file stream.

```js
const fs = require("fs");

const out = fs.createWriteStream("./out.log");
const err = fs.createWriteStream("./err.log");

const console2 = new console.Console(out, err);

setInterval(function () {
  console2.log(new Date());
  console2.error(new Error("Erorrrrrrrrrrrr"));
}, 5000);

// We see 2 files has been created
```

## 17. Child Processes

Single-threaded, non-blocking performance in Node works great for a single process. But eventually, one process in one CPU is not going to be enough to handle the increasing workload or high availability of our application.

Using multiple processes is the best way to scale a Node application. Node is designed for building distributed applications with many nodes. This is why it's named *Node*. Scalability is baked into the framework unlike other solution, scaling the app is third party tools.

### 17.1. child_process module

- We can easily spawn/spin a child process using Node's `child_process` module and those child processes can easily communicate with each other with a messaging system.
- We can execute any operating system command from within node process using sub process and then get the result of running  that command in our main process.
- The `child_process` module enables us to access Operating System functionalities by running any system command inside a child process.
- We can control that child process input stream and listen to its output stream.
- We can also control the arguments to be passed to the underlying OS command, and we can do whatever we want with that command's output.

There are four different ways to create a child process in Node,

- `spawn()`
- `fork()`
- `exec()`
- `execFile()`.

`spawn` is the one frequently used.

### 17.2. `spawn` function

- The `child_process.spawn()` method spawns a new process using the given command, with command-line arguments in `args`.
- The spawn function launches a command in a new process and we can use it to pass that command any arguments.
- By default, pipes for `stdin`, `stdout`, and `stderr` are established between the parent Node.js process and the spawned subprocess.

For example, here’s code to spawn a new process that will execute the `pwd` command.

> All child_module code have been tested on Ubuntu (linux) - WSL only.

```js
const { spawn } = require("child_process");

const child = spawn("pwd");

child.on("exit", (code, signal) => console.log(`child process exited with code ${code} and signal ${signal}`))

/*
Prints
child process exited with code 0 and signal null
*/
```

- The result of executing the `spawn` function (the `child` object) is a `ChildProcess` instance, which implements the `EventEmitter` API.
- This means we can register handlers for events on this child object directly.
- For example, we can do something when the child process exits by registering a handler for the `exit` event.
- The handler above gives us the exit `code` for the child process and the `signal`, if any, that was used to terminate the child process.
- This signal variable is null when the child process exits normally.

The other events that we can register handlers for with the ChildProcess instances are `disconnect`, `error`, `close`, and `message`.

- The `disconnect` event is emitted when the parent process manually calls the child.disconnect method.
- The `error` event is emitted if the process could not be spawned or killed.
- The `close` event is emitted when the `stdio` streams of a child process get closed.
- The `message` event is the most important one. It’s emitted when the child process uses the `process.send()` function to send messages. This is how parent/child processes can communicate with each other. We’ll see an example of this below.

Every child process also gets the three standard `stdio` streams, which we can access using `child.stdin`, `child.stdout`, and `child.stderr`.

When those streams get closed, the child process that was using them will emit the `close` event. This `close` event is different than the `exit` event because multiple child processes might share the same `stdio` streams, so one child process exiting does not mean that the streams got closed.

Since all streams are event emitters, we can listen to different events on those `stdio` streams that are attached to every child process. Unlike in a normal process though, in a child process the `stdout/stderr` streams are readable streams while the `stdin` stream is a writable one. This is basically the inverse of those types found in a main process. The events we can use for those streams are the standard ones.

Most importantly, on the readable streams we can listen to the data event, which will have the output of the command or any error encountered while executing the command:

```js
const { spawn } = require("child_process");

const child = spawn("pwd");

child.on("exit", (code, signal) => console.log(`child process exited with code ${code} and signal ${signal}`))

child.stdout.on("data", data => {
  console.log(`child stdout:\n${data}`);
});

child.stderr.on("data", data => {
  console.error(`child stderr:\n${data}`);
});

/*
Prints

child stdout:
/home/avinash/projects/node-server

child process exited with code 0 and signal null
*/
```

The two handlers above will log both cases to the **main process stdout and stderr**. When we execute the `spawn` function above, the output of the `pwd` command gets printed and the child process exits with code 0, which means no error occurred.

We can pass arguments to the command that’s executed by the `spawn` function.

Ex-1,

```js
const { spawn } = require("child_process");

const child = spawn("find", [".", "-type", "f"]);

child.stdout.on("data", data => {
  console.log(`child stdout:\n${data}`);
});

/*
Prints

child stdout:
./.git/HEAD
./.git/config
./.git/description
.
.
.
*/
```

> `find . -type f` to list files only in linux system

Ex-2,

```js
const { spawn } = require("child_process");

// Print Working Directory
const pwd = spawn("pwd");
pwd.stdout.pipe(process.stdout);
// /home/avinash/projects/node-server

// List files
const ls = spawn("ls", ["-l", "."]);
ls.stdout.pipe(process.stdout);
// total 4
// -rw-r--r-- 1 avinash avinash 319 Dec 29 17:55 index.js


// Use Shell Syntax using spawn 
const shell = spawn("ls -l .", { shell: true });
shell.stdout.pipe(process.stdout);
// total 4
// -rw-r--r-- 1 avinash avinash 319 Dec 29 17:55 index.js
```

A child process `stdin` is a writable stream. We can use it to send a command some input. Just like any writable stream, the easiest way to consume it is using the `pipe` function. We simply pipe a readable stream into a writable stream. Since the main process `stdin` is a readable stream, we can pipe that into a child process `stdin` stream. For example:

```js
const { spawn } = require("child_process");

const child = spawn("wc"); // word line character count

process.stdin.pipe(child.stdin);

child.stdout.on("data", data => {
  console.log(`child stdout:\n${data}`);
});

/*
Prints: (Enter hello and press Ctrl + d to see the output)

> node index.js
hello
child stdout:
      1       1       6
      word    line    char count
*/
```

### 17.3. `exec` function

By default, the `spawn` function **does not create a shell** to execute the command we pass into it. This makes it slightly more efficient than the `exec` function, which does create a shell. The `exec` function has one other major difference. It buffers the command’s generated output and passes the whole output value to a callback function (instead of using streams, which is what `spawn` does).

Previous examples written using `exec`

```js
const { exec } = require("child_process");

exec("find . -type f", (err, stdout, stderr) => {
  if (err) {
    console.error(`exec error: ${err}`);
    return;
  }

  console.log(`Number of files ${stdout}`);
});
/*
Prints

Number of files
./.git/HEAD
./.git/config
./.git/description
.
.
.
*/
```

Since the `exec` function uses a **shell** to execute the command, we can use the shell syntax directly here.

### 17.4. `execFile` function

If you need to execute a file without using a shell, the `execFile` function is what you need. It behaves exactly like the `exec` function, but does not use a shell, which makes it a bit more efficient.

dailyReportCron.js

```js
console.log("REPORT GENERATED")
```

index.js

```js
const { execFile } = require('child_process');
const child = execFile('node', ["dailyReportCron.js"], (error, stdout, stderr) => {
  if (error) {
    throw error;
  }
  console.log(stdout);
});

// REPORT GENERATED
```

### 17.5. `fork` Function

- The `fork` function is a variation of the `spawn` function for spawning node processes.
- The biggest difference between `spawn` and `fork` is that a communication channel is established to the child process when using fork, so we can use the `send` function on the forked process along with the global `process` object itself to exchange messages between the parent and forked processes.
- We do this through the EventEmitter module interface.

Ex,

parent.js

```js
const { fork } = require("child_process");

const forked = fork("child.js");

forked.on("message", msg => {
  console.log("Message from child", msg);
});

forked.send({ hello: "world" })
```

child.js

```js
process.on("message", msg => {
  console.log("Message from parent:", msg);
});

let counter = 0;

setInterval(() => {
  process.send({ counter: counter++ });
}, 1000);
```

```md
> node parent.js

Message from parent: { hello: 'world' }
Message from child { counter: 0 }
Message from child { counter: 1 }
.
.
```

In the parent file above, we fork `child.js` (which will execute the file with the node command) and then we listen for the `message` event. The `message` event will be emitted whenever the child uses `process.send`, which we’re doing every second.

To pass down messages from the parent to the child, we can execute the `send` function on the forked object itself. Then, in the child script, we can listen to the `message` event on the global `process` object.

When executing the `parent.js` file above, it’ll first send down the `{ hello: 'world' }` object to be printed by the forked child process and then the forked child process will send an incremented counter value every second to be printed by the parent process.

Ex - More practical example

Problem

```js
const http = require("http");

const longComputation = () => {
  let sum = 0;
  for (let i = 0; i < 9999999999; i++) {
    sum += i;
  }
  return sum;
};

const server = http.createServer();

server.on("request", (req, res) => {
  if (req.url === "/compute") {
    const sum = longComputation();
    return res.end(`Sum is ${sum}`);
  } else {
    res.end("Ok");
  }
});

server.listen(3000);

/*
curl localhost:3000/compute => Event loop is blocked for long computation
curl localhost:3000/compute => If i make one more, i call, i have to wait for previous computation to complete, 
                               then to take up another request. simply put, my requests are getting blocked.
*/
```

This program has a big problem; when the`/compute` endpoint is requested, the server will not be able to handle any other requests because the event loop is busy with the long for loop operation.

There are a few ways we can solve this problem depending on the nature of the long operation but one solution that works for all operations is to just move the computational operation into another process using `fork`.

We first move the whole `longComputation` function into its own file and make it invoke that function when instructed via a `message` from the main process:

compute.js

```js
const longComputation = () => {
  let sum = 0;
  for (let i = 0; i < 9999999999; i++) {
    sum += i;
  }
  return sum;
};

process.on("message", msg => {
  const sum = longComputation();
  process.send(sum);
});
```

Now, instead of doing the long operation in the main process event loop, we can `fork` the `compute.js` file and use the messages interface to communicate messages between the server and the forked process.

index.js

```js
const http = require("http");
const { fork } = require("child_process");

const server = http.createServer();

server.on("request", (req, res) => {
  if (req.url === "/compute") {
    const compute = fork("compute.js");
    compute.send("start");
    compute.on("message", sum => {
      res.end(`Sum is ${sum}`);
    });
  } else {
    res.end("Ok");
  }
});

server.listen(3000);
```

When a request to `/compute` happens now with the above code, we simply send a message to the forked process to start executing the long operation. **The main process’s event loop will not be blocked.**

Once the forked process is done with that long operation, it can send its result back to the parent process using `process.send`.

In the parent process, we listen to the `message` event on the forked child process itself. When we get that event, we’ll have a sum value ready for us to send to the requesting user over http.

The code above is limited by the number of processes we can fork, but when we execute it and request the long computation endpoint over http, the main server is not blocked at all and can take further requests.

## 18. Debugging Node.js apps

### 18.1. Debugging with Chrome DevTools

V8 Inspector integration allows attaching Chrome DevTools to Node.js instances for debugging and profiling.

V8 Inspector can be enabled by passing the `--inspect` flag when starting a Node.js application.

To break on the first line of the application code, pass the `--inspect-brk` flag instead of --inspect.

index.js

```js
let str = "";

for (let i = 0; i < 3; i++) {
  str = str + i;
}
console.log(str);
// expected output: "012"
```

1. Run the app `node --inspect-brk index.js`
2. Go to chrome and enter the URL as `brave://inspect`
3. Now click on `inspect` or `Open dedicated DevTools for Node` link on page
4. In below screen, use debugging utilities on upper right corner to go through the code step by step.

![node-chrome-debug](assets/node-chrome-debug.png)

### 18.2. Debugging in VS Code

`https://code.visualstudio.com/docs/nodejs/nodejs-debugging`

### 18.3. Debugging in Terminal

## 19. Node's Internal Architecture

- Node.is is more than a wrapper around the V8 JavaScript Engine. It provides API to work with OS, file system, binary data, networking, crypto etc.
- Node uses V8 via V8's C++ API
- Node itself has an API which we can use in JavaScript and it allows us to interact with the filesystem, network, timers etc.
- Node uses C++ bindings, for each modules exposed to JavaScript land and it eventually executes C++ code.
- Node also handles the waiting for asynchronous events for us using **libuv** library- The Event Loop
- When Node is done waiting for I/O operations or timers, it usually has callback functions to invoke, and when it's time to invoke these callbacks, Node simply passes the control into the V8 engine. When V8 is done with the code in the callback, the control is passed back to Node.
- When the control is with V8 ((i.e. when there is something in callstack) and since V8 is single-threaded, Node cannot execute anymore JavaScript code, no matter how many callbacks have been registered, Node will wait until V8 can handle more operations.
- There's only one thread where our JavaScript code runs.
- This single-thread is what makes execution of code flow predictable and easy.
- Libuv is c library used to abstract the non-blocking I/O operations to a consistent interface across many operating systems. It's what handles operations on the file system, TCP/UDP sockets, child processes, and others.
- Libuv includes a thread pool to handle what can't be done asynchronously at the operating system level.
- Libuv is also what provides Node with the event-loop.
- llhttp is a library for parsing HTTP messages.
- C-ares is what enables performing asynchronous DNS queries
- OpenSSL is used mostly in the tls and crypto modules
- Zlib is used for its fast async and streaming compression and decompression interfaces.

![node-arch](assets/node-arch.png)

There are several dependencies that Node.js relies on to work the way it does.

### 19.1. V8

The V8 library provides Node.js with a JavaScript engine, which Node.js controls via the V8 C++ API.

### 19.2. libuv

- C library that is used to abstract non-blocking asynchronous I/O operations to a consistent interface across all supported platforms.
- The Event Loop mechanism is handled internally by libuv only
- It provides mechanisms to handle file system, DNS, network, child processes, pipes, signal handling, polling and streaming.
  
### 19.3. llhttp

llhttp is a parser for HTTP messages written in C. It parses both requests and responses.

### 19.4. c-ares

For some asynchronous DNS requests, Node.js uses a C library called c-ares.

### 19.5. OpenSSL

OpenSSL is used extensively in both the tls and crypto modules.

### 19.6. zlib

For fast compression and decompression, Node.js relies on the industry-standard zlib library

Let's check all these components version used in our Node.js installation,

```console
node -p process.versions

{
  node: '14.16.1',
  v8: '8.4.371.19-node.18',
  uv: '1.40.0',
  zlib: '1.2.11',
  brotli: '1.0.9',
  ares: '1.16.1',
  modules: '83',
  nghttp2: '1.41.0',
  napi: '7',
  llhttp: '2.1.3',
  openssl: '1.1.1k',
  cldr: '37.0',
  icu: '67.1',
  tz: '2020a',
  unicode: '13.0'
}
```

## 20. Streams

Streams are collections of data – just like arrays or strings. The difference is that streams might not be available all at once and they don’t have to fit in memory.

This makes streams really powerful when working with large amounts of data, or data that’s coming from an external source one chunk at a time.

Many of the built-in modules in Node implement the streaming interface:

![built-in-stream-api](assets/built-in-stream-api.png)

### 20.1. Why Streams

Practical problem,

```js
const fs = require("fs");
const http = require("http");

fs.stat("big.file", function (err, stat) {
  if (err == null) {
    console.log("File exists");
  } else if (err.code === "ENOENT") {
    const file = fs.createWriteStream("./big.file");
    for (let i = 0; i <= 1e6; i++) {
      file.write(
        `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur tempus id metus a sodales. Maecenas faucibus bibendum mauris elementum ultrices. In hac habitasse platea dictumst. Pellentesque consequat augue nec urna interdum, a sagittis arcu ornare. Duis pulvinar odio vitae velit euismod, nec pretium nisi tempus. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras ante lorem, suscipit non lobortis venenatis, interdum a dui. Donec rhoncus magna lectus, ut vestibulum eros rutrum gravida. Aenean sit amet fringilla erat. In varius fermentum justo, in maximus sapien tempus non. Sed malesuada tempor erat eget tristique. Pellentesque diam nulla, pharetra sed luctus nec, euismod non tortor.`
      );
    }
    console.log("big.file created");
    file.end();
  } else {
    console.log("Some other error: ", err.code);
  }
});

const server = http.createServer();

server.on("request", (req, res) => {
  fs.readFile("./big.file", (err, data) => {
    if (err) throw err;

    res.end(data);
  });
});

server.listen(8000, () => console.log("Server is running at localhost:8000"));
```

```console
> node index.js

Server is running at localhost:8000
big.file created
```

After starting the node server, let's see what the memory usage using task manager.

![stream-http-1](assets/stream-http-1.png)

Now, let's curl the endpoint,

```console
> curl localhost:8000

Lorem ipsum dolor sit amet, consectetur adipiscing e......
............................
.......................
```

Now look at the memory consumtion for server task manager.

![stream-http-2](assets/stream-http-2.png)

- When we ran the server, it started out with a normal amount of memory, 5.8 MB
Then we connected to the server. Note what happened to the memory consumed. The memory consumption jumped to ~684mb.

How it is working?

We basically put the whole big.file content in memory before we wrote it out to the response object. This is very inefficient.

Solution.

The HTTP response object (`res` in the code above) is also a writable stream. This means if we have a readable stream that represents the content of big.file, we can just pipe those two on each other and achieve mostly the same result without consuming ~684mb of memory.

Node’s `fs` module can give us a readable stream for any file using the `createReadStream` method. We can pipe that to the response object.

replace the reqest handler code with below content, now measure the memory consumption.

```js
server.on("request", (req, res) => {
  const src = fs.createReadStream("./big.file");
  src.pipe(res);
});
```

```console
> node index.js

Server is running at localhost:8000
big.file created
```

After starting the node server, let's see what the memory usage using task manager.

![stream-http-1](assets/stream-http-1.png)

Now, let's curl the endpoint,

```console
> curl localhost:8000

Lorem ipsum dolor sit amet, consectetur adipiscing e......
............................
.......................
```

Now look at the memory consumtion for server task manager.

![stream-http-3](assets/stream-http-3.png)

- When we ran the server, it started out with a normal amount of memory, 5.8 MB
Then we connected to the server (curl). Note what happened to the memory consumed. The memory consumption is just ~8mb.

Now, whats changed and how its working?

When a client asks for that big file, **we stream it one chunk at a time, which means we don’t buffer it in memory at all.** The memory usage grew by about ~8 mb and that’s it.

These scarios, need not be for just a http server, it may be applicable to cases such as file content manupulation, files creation, socket programming, uploading the file from client to server etc.

### 20.2. Types of Streams

There are four fundamental stream types within Node.js

1. `Writable` : streams to which data can be written (for example, `fs.createWriteStream())`.
  
2. `Readable` : streams from which data can be read (for example, `fs.createReadStream())`.

3. `Duplex` : A duplex stream is both Readable and Writable.  (for example, `net.Socket`).

4. `Transform`  : A transform stream is basically a duplex stream that can be used to modify or transform the data as it is written and read. An example of that is the `zlib.createGzip` stream to compress the data using gzip. We can think of a transform stream as a function where the input is the writable stream part and the output is readable stream part.

**All streams are instances of EventEmitter. They emit events that can be used to read and write data.**

### 20.3. `pipe`

The `readable.pipe()` method attaches a `Writable` stream to the `readable`, causing it to switch automatically into flowing mode and push all of its data to the attached `Writable`.

Syntax,

```js
readableSrc.pipe(writableDest);
```

Ex, Create a clone(copy) of a file using stream and pipe.

```js
const fs = require("fs");

// Creating a file using stream
const file1 = fs.createWriteStream("file1.txt");
file1.write(`Hello World`);
file1.end();

// Create a readable stream out of a file
const readable = fs.createReadStream("file1.txt");

// Now, can you clone this file?

// Create a destination(to clone) file using stream, again
const writable = fs.createWriteStream("file2.txt");

// All the data from readable goes into 'file2.txt'.
readable.pipe(writable);

// it created file1.txt & file2.txt in current project directory
```

What are other ways to work with strems?

### 20.4. Stream events

Besides reading from a readable stream source and writing to a writable destination, the `pipe` method automatically manages a few things along the way. For example, it handles errors, end-of-files, and the cases when one stream is slower or faster than the other.

However, streams can also be consumed with **events** directly.

List of the important events and methods that can be used with readable and writable streams

![stream-events](assets/stream-events.png)

The most important events on a readable stream are:

- The `data` event, which is emitted whenever the stream passes a chunk of data to the consumer.
- The `end` event, which is emitted when there is no more data to be consumed from the stream.

The most important events on a writable stream are:

- The `drain` event, which is a signal that the writable stream can receive more data.
- The `finish` event, which is emitted when all data has been flushed to the underlying system.

Ex, Create a clone(copy) of a file using stream events.

```js
const fs = require("fs");

// Creating a file using stream
const file1 = fs.createWriteStream("file1.txt");
file1.write(`Hello World`);
file1.end();

// Create a readable stream out of a file
const readable = fs.createReadStream("file1.txt");

// Now, can you clone this file?

// Create a destination(to clone) file using stream, again
const writable = fs.createWriteStream("file2.txt");

readable.on("data", (chunk) => {
  writable.write(chunk);
});

readable.on("end", (chunk) => {
  writable.end();
});

// it created file1.txt & file2.txt in current project directory
```

Now, we know what heavy-lifting `pipe` is doing for us.

```md
readable.on("data", (chunk) => {
  writable.write(chunk);
});

readable.on("end", (chunk) => {
  writable.end();
});


readable.pipe(writable);
```

### 20.5. Implementing Streams

When we talk about streams in Node, there are two main different tasks:

- The task of **implementing** the streams. Ex, `require('stream')`
- The task of **consuming** them. Ex, use `pipe/events`

So far, we’ve been talking about only consuming streams. Let’s implement some!

To access the stream module:

`const stream = require('stream');`

### 20.6. Implementing a Writable Streams

To implement a writable stream, we need to use the `Writable` constructor from the `stream` module.

We just create an object from the `Writable` constructor and pass it a number of options. The only required option is a `write` function, which exposes the chunk of data to be written.

```js
const { Writable } = require("stream");

const outStream = new Writable({
  write(chunk, encoding, callback) {
    console.log(chunk.toString());
    callback();
  },
});

process.stdin.pipe(outStream);

/** console
 * > node index.js
 * 12 (press enter)
 * 12
 *
 * hello
 * hello
 */
```

This `write` method takes three arguments.

- The `chunk` is usually a buffer unless we configure the stream differently.
- The `encoding` argument is needed in that case, but we can usually ignore it.
- The `callback` is a function that we need to call after we’re done processing the data chunk. It’s what signals whether the write was successful or not. To signal a failure, call the callback with an error object.

In `outStream`, we simply `console.log` the `chunk` as a string and call the callback after that without an error to indicate success. This is a very simple and probably not so useful echo stream. It will **echo** back anything it receives.

To consume this stream, we can simply use it with `process.stdin`, which is a readable stream, so we can just `pipe` `process.stdin` into our outStream.

When we run the code above, anything we type into `process.stdin` will be echoed back using the `outStream` `console.log` line.

So, whatever we built a writable stream `outStream`is very much equivalent to  built-in `process.stdout`.

```js
process.stdin.pipe(process.stdout);

/** console
 * > node index.js
 * 12 (press enter)
 * 12
 *
 * hello
 * hello
 */
```

### 20.7. Implementing a Readable Streams

To implement a readable stream, we require the `Readable` interface and construct an object from it.

```js
const { Readable } = require("stream");

const inStream = new Readable();

inStream.push("ABCDEFGHIJKLM");
inStream.push("NOPQRSTUVWXYZ");

inStream.push(null); // No more data

inStream.pipe(process.stdout);

/** console
 * > node index.js
 * ABCDEFGHIJKLMNOPQRSTUVWXYZ
 */
```

When we `push` a `null` object, that means we want to signal that the stream does not have any more data.

To consume this simple readable stream, we can simply pipe it into the writable stream `process.stdout`.

When we run the code above, we’ll be reading all the data from `inStream` and echoing it to the standard out. Very simple, but also not very efficient.

We’re basically pushing all the data in the stream before & piping it to `process.stdout`. The much better way is to push data on demand, when a consumer asks for it. We can do that by implementing the `read()` method in a readable stream configuration:

Ex- When the `read` method is called on a readable stream, the implementation can push partial data to the queue.

For example, we can push one letter at a time, starting with character code `65` (which represents `A`), and increment the code on every push,

```js
const { Readable } = require("stream");

const inStream = new Readable({
  read(size) {
    this.push(String.fromCharCode(this.currentCharCode++));
    if (this.currentCharCode > 90) {
      this.push(null);
    }
  },
});

inStream.currentCharCode = 65;

inStream.pipe(process.stdout);

/** console
 * > node index.js
 * ABCDEFGHIJKLMNOPQRSTUVWXYZ
 */
```

While the consumer is reading a readable stream, the `read` method will continue to fire and we’ll push more letters. We need to stop this cycle somewhere, and that’s why I used an if statement to push null when the `currentCharCode` is greater than `90` (which represents `Z`).

We can use timer to add the chars slowly so we can see how `read` method being called each time.

```js
const { Readable } = require("stream");

const inStream = new Readable({
  read(size) {
    setTimeout(() => {
      if (this.currentCharCode > 90) {
        this.push(null);
        return;
      }
      this.push(String.fromCharCode(this.currentCharCode++));
    }, 1000);
  },
});

inStream.currentCharCode = 65;

inStream.pipe(process.stdout);

/** console (each letter will be printed slowly)
 * > node index.js
 * ABCDEFGHIJKLMNOPQRSTUVWXYZ
 */
```

### 20.8. Implementing Duplex Streams

With `Duplex` streams, we can implement both readable and writable streams with the same object. It’s as if we inherit from both interfaces.

```js
const { Duplex } = require("stream");

const inoutStream = new Duplex({
  write(chunk, encoding, callback) {
    console.log(chunk.toString());
    callback();
  },

  read(size) {
    setTimeout(() => {
      if (this.currentCharCode > 90) {
        this.push(null);
        return;
      }
      this.push(String.fromCharCode(this.currentCharCode++));
    }, 1000);
  },
});

inoutStream.currentCharCode = 65;

process.stdin.pipe(inoutStream).pipe(process.stdout);

/** console
 * > node index.js
 * ABCDEFGHIJKLMNOPQRSTUVWXYZhello
 * hello
 */
```

- By combining the `write` and `read` methods, we can use this duplex stream to read the letters from `A` to `Z` and we can also use it for its echo feature.
- We `pipe` the readable `stdin` stream into this duplex stream to use the echo feature and we pipe the duplex stream itself into the writable `stdout` stream to see the letters `A` through `Z`.

It’s important to understand that the readable and writable sides of a duplex stream operate completely independently from one another.

### 20.9. Implementing Transform Streams

A transform stream is the more interesting duplex stream because its output is computed from its input.

For a transform stream, we don’t have to implement the `read` or `write` methods, we only need to implement a `transform` method, which combines both of them. It has the signature of the `write` method and we can use it to `push` data as well.

Ex, transform stream which echoes back anything you type into it after transforming it to uppercase format.

```js
const { Transform } = require("stream");

const upperCaseTr = new Transform({
  transform(chunk, encoding, callback) {
    this.push(chunk.toString().toUpperCase());
    callback();
  },
});

process.stdin.pipe(upperCaseTr).pipe(process.stdout);

/** console
 * > node index.js
 * hello
 * HELLO
 */
```

### 20.10. Built-in transform streams

The useful built-in transform streams such as the `zlib` and `crypto` streams.

Ex, `zlib.createGzip()` stream combined with the `fs` readable/writable streams to create a file-compression script

```js
const fs = require("fs");
const zlib = require("zlib");

const file = "file1.txt";
fs.writeFileSync(file, "stream it i say");

fs.createReadStream(file)
  .pipe(zlib.createGzip())
  .pipe(fs.createWriteStream(file + ".gz"));

/** project directory
 * file1.txt
 * file1.txt.gz
 */
```

We’re piping a readable stream for that file into the zlib built-in transform stream and then into a writable stream for the new gzipped file.

Using pipes is that we can actually combine them with events.

for example, I want the user to see a progress indicator while the script is working and a “Done” message when the script is done. Since the pipe method returns the destination stream, we can chain the registration of events handlers as well.

```js
const fs = require("fs");
const zlib = require("zlib");

const file = "file1.txt";
fs.writeFileSync(file, "stream it i say");

fs.createReadStream(file)
  .pipe(zlib.createGzip())
  .on("data", () => process.stdout.write(".\n"))
  .pipe(fs.createWriteStream(file + ".gz"))
  .on("finish", () => console.log("Completed the zipping"));

/** console
 * .
 * .
 * Completed the zipping
 */

/** project directory
 * file1.txt
 * file1.txt.gz
 */
```
