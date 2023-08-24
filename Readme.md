# JavaScript Important Interview Questions


## 1.What is JavaScript ?
JavaScript is a web scripting, high-level, dynamic and versatile programming language primarily used for creating interactive and dynamic content on websites.</br>
**Key features of javascript:-**
- Dynamically Typed</br>
- Multi Paradigm</br>
- Server Side Development</br>


## 2.What is Hoisting ?
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

## 3. What is Temporal Dead Zone (TDZ) ?
 Temporal dead zone (TDZ) is the area of a block where a variable is inaccessible until the variable is initialized with a value. It is a safety mechanism in JavaScript that prevents the use of variables before they are properly initialized, helping to catch potential issues and maintain a clearer understanding of variable scope and usage.

## 4. What is Closures ?
 In Closures, A function has always access to the variable enviornment of the execution context in which the function was created even after the execution context is gone from  the call stack.

## 5. What is Memoization ?
Memoization is an optimization technique used in programming to store the results of expensive function calls and return the cached result when the same inputs occur again. It's a way to avoid redundant computations and improve the performance of certain functions. 
