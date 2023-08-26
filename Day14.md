#### Lexical scoping : refers to when the location of a function's definition determines which variables you have access to.
( where variables and blocks of scope are authored)
What is author-time?
This is the time that when developer writes the code. This can be taken to mean, perception of program as you see it before compilation.
example :
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/8dcdda10-4685-49da-9a8f-063b6975ed17)

There are three nested scopes inherent in this code example
* Bubble 1 encompasses the global scope, and has just one identifier in it: foo.
* Bubble 2 encompasses the scope of foo, which includes the three identifiers: a, bar, b.
* Bubble 3 encompasses the scope of bar, and it includes just one identifier: c.



#### dynamic scoping : uses the location of the function's invocation to determine which variables are available.
(Dynamic scope does not concern itself with how and where functions and scopes are declared, but rather where they are called from. That means that, the scope chain is based on call-stack, not the nesting of scopes in code.)

example : when foo() is executed, theoretically the code below would result 3 as the output,
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/0885956f-7f8d-48b5-a1f8-5de3fe4b4c0d)

When foo() cannot resolve the variable reference for a, instead of stepping up the nested (lexical scope — we will mention soon) scope 

chain, it walks up the call-stack, to find where foo() was called from. Since foo() was called from bar() it checks the variables in scope

 for bar(), and finds an a there with value 3.

my refernce (https://medium.com/@osmanakar_65575/javascript-lexical-and-dynamic-scoping-72c17e4476dd)


### function scope :

example :overlaping name variables 

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/08b7a538-aebd-4c55-98ab-ea741242e8db)


solve overlapping with scop function :

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/269616a6-b3be-4cb4-a826-251702514552)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/bc308390-6cfa-472a-ab1e-771a62cc8850)


### IIEF : immediately invoked function expressions 
 * Self-Invoking Functions || When a function is created at the same time it is called,

syntax :
```
(function() => {})()
```
OR 
```
(() => {})()

```
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/a20d10b8-c503-44bd-8c39-6257806c09d2)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/1ab33017-841c-498d-a9ed-cf8773ebf210)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/9066efe6-4642-4947-bb0e-0c27152e7761)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/840227fb-45bf-4503-80bd-e99d817b2b20)

### block scope :
A block scope is the area within if, switch conditions or for and while loops. Generally speaking, whenever you see {curly brackets}, it is a block. In ES6, const and let keywords allow developers to declare variables in the block scope, which means those variables exist only within the corresponding block.

#### Hoisting : is JavaScript's default behavior of moving declarations to the top.
#### JavaScript Declarations are Hoisted
* JavaScript Declarations are Hoisted
* In JavaScript, a variable can be declared after it has been used.
* In other words; a variable can be used before it has been declared.
* Example 1 gives the same result as Example 2:
* Example 1 :

```
x = 5; // Assign 5 to x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x;                     // Display x in the element

var x; // Declare x`
```
Example 2 :
```
var x; // Declare x
x = 5; // Assign 5 to x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x;                     // Display x in the element
```
* Hoisting is JavaScript's default behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function).
### The let and const Keywords

* Variables defined with let and const are hoisted to the top of the block, but not initialized.
* Meaning: The block of code is aware of the variable, but it cannot be used until it has been declared.
* Using a let variable before it is declared will result in a ReferenceError.
* The variable is in a "temporal dead zone" from the start of the block until it is declared:














