# JavaScript Important Interview Questions


## What is JavaScript ?
 JavaScript is a web scripting, high-level, dynamic and versatile programming language primarily used for creating interactive and dynamic content on websites.</br>
**Key features of javascript:-**
- Dynamically Typed</br>
- Multi Paradigm</br>
- Server Side Development</br>


## What is Hoisting ?
 Hoisting is a concept in JavaScript where variable and function declarations are moved to the top of their containing scope during the compilation phase, before the actual code execution.
```
console.log(x); // Output: undefined
var x = 5;
```
In above exapmle x is declared with var keyword which is hoisted and it moved to the top of the scope and initialize with value of "undefined". It's important to note that only the declarations themselves are hoisted, not the initializations. 
```
var x; // Declaration is hoisted to the top
console.log(x); // Output: undefined
x = 5; // Initialization remains in place
console.log(x); //Output: 5
```
we can see variable is available before we actually initialized it yet contains the value undefined until it's explicitly assigned the value 5.

*Note:- let and const are hoisted but not initialized* 

## What is Temporal Dead Zone (TDZ) ?
 Temporal dead zone (TDZ) is the area of a block where a variable is inaccessible until the variable is initialized with a value. It is a safety mechanism in JavaScript that prevents the use of variables before they are properly initialized, helping to catch potential issues and maintain a clearer understanding of variable scope and usage.

## What is Scope in JavaScript ?
Scope refers to the context in which variables are declared and accessed. It defines where that variable can be used within your code.</br>
JavaScript has two main types of scope: **Global Scope** and **Local Scope**.</br>
**Global Scope:-**</br>
Variables declared outside of any function or block have global scope. These variables are accessible from any part of your code, both within functions and at the top level.
```
const globalVar = 42;
function exampleFunction() {
    console.log(globalVar); // Accessible within the function
}
console.log(globalVar); // Accessible outside the function
```
**Local Scope:-** </br>
Variables declared inside a function or block have local scope. These variables are only accessible within the function or block in which they are defined. They are also known as function-scoped variables.
```
function exampleFunction() {
    const localVar = 20; // local to the function
    console.log(localVar); // Accessible within the function
}
console.log(localVar); //throw error: localVar is not defined 
```

## What is Closures ?
 In Closures, A function has always access to the variable enviornment of the execution context in which the function was created even after the execution context is gone from  the call stack.Closures maintain the relationship between a function and its lexical scope.
 
## What is Lexical Scoping ?
 JavaScript uses lexical scoping to determine the scope of variables. When a function is defined, it "captures" its surrounding scope, creating a closure with access to the variables in that scope, regardless of where the function is subsequently invoked.
 
## What is Call Stack ?
 In JavaScript, the call stack is a mechanism used to keep track of function calls during the execution of a program. It's a data structure that follows the Last-In-First-Out (LIFO) principle, meaning that the most recently called function is the first one to be resolved and removed from the stack.
 
## What is Execution Contex ?
 An execution context in JavaScript is a concept that defines the environment in which JavaScript code is executed. It includes information about the scope, variables, functions, and the value of this during the execution of a piece of code.</br>
 </br>
 **Global Execution Context:-** The global execution context represents the outermost scope of a JavaScript program. It's created when the script starts running the global execution context is associated with the global object (window in the browser environment).
 </br>
 </br>
 **Function Execution Context:-** Every time a function is called, a new function execution context is created for that specific call. This context holds information about the function's local variables, parameters, and the function's code. Each function call gets its own execution context, and they are organized in a stack known as the call stack. 
 </br>
 </br>
*Key components of an execution context include:*
- **Variable Environment**: A reference to the variables and functions defined within the current context. In function contexts, this includes function parameters and locally declared variables.

- **Lexical Environment**: Similar to the variable environment, but it also encompasses the outer environment (the context where the current function was defined). This is crucial for resolving scope and closures.

- **This Keyword**: The value of the this keyword, which represents the context or object to which the current code is associated. The value of this can change depending on how a function is called.

## Explain Higher Order Functions in javascript ?
 Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.

## Explain Pure Functions in javascript ?
 In JavaScript, a pure function is a function that produces the same output for the same input and has no side effects. A side effect is any modification or interaction with the external state, such as changing variables outside the function's scope, modifying data structures, or performing I/O operations. 

## What are callbacks ?
 In JavaScript, a callback is a function that is passed as an argument to another function and is intended to be executed after some specific operation or task is completed. Callbacks are a fundamental concept in asynchronous programming and are commonly used to handle asynchronous tasks like data fetching, handling user input, and event handling.

## What is an Immediately Invoked Function in JavaScript ?
 An Immediately Invoked Function ( known as IIFE and pronounced as IIFY) is a function that runs as soon as it is defined. 
 
## What is Memoization ?
 Memoization is an optimization technique used in programming to store the results of expensive function calls and return the cached result when the same inputs occur again. It's a way to avoid redundant computations and improve the performance of certain functions. 
 
## What is Currying ?
 Currying is a functional programming technique in which a function that takes multiple arguments is transformed into a sequence of functions, each taking a single argument. 
 ```
// A non-curried function that adds two numbers
function add(a, b) {
    return a + b;
}

// Curried version of the add function
function curriedAdd(a) {
    return function(b) {
        return a + b;
    };
}
```
 Currying can help improve code readability and enable you to create more flexible and versatile functions by breaking down complex operations into smaller, composable pieces.
 ```
const curriedAdd = a => b => a + b;
const add5 = curriedAdd(5);
console.log(add5(3)); // Outputs: 8
```

## What is Event Bubbling ?
 In event bubbling, when an event occurs on a particular DOM element, the event first triggers on that element, and then it "bubbles up" through its parent elements in the DOM hierarchy, triggering the same event on each ancestor element one by one. This means that the innermost element's event handler is called first, followed by its parent's event handler, and so on, until the root of the DOM tree is reached. Event bubbling is the default behavior for most events in the DOM.
 
## What is Event Capturing ?
 The event starts from the root of the DOM hierarchy and moves down towards the target element. During this phase, event listeners set to capture the event are triggered. This phase provides an opportunity to intercept the event before it reaches the target.
 
## What is Callback Hell ?
 While doing multiple asynchronous operations, the callback can get nested which is known as Callback Hell.
 
## What are Promises ?
 It is a JavaScript object that holds the eventual result or failure of an asynchronous operation. Promises have three states:-
 - Pending
 - Fulfilled
 - Rejected
 
## What is the distinction between client-side and server-side JavaScript ?
- Client-Side JavaScript runs in the user's browser and focuses on enhancing interactivity and UI. It's limited by security and varies across browsers.
- Server-Side JavaScript runs on the web server, handling tasks like data storage and generating dynamic content. It's more secure but can result in slower response times.

## What are Cookies ?
 Cookies in JavaScript are small pieces of data that are stored on a user's device, typically within their web browser, as a means to remember information between different browsing sessions. Cookies are often used to store information like user preferences, login sessions, shopping cart contents, and tracking data. Cookies consist of key-value pairs and can have various attributes that define their behavior
