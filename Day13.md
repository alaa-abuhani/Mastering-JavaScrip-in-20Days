
### Scope determines the accessibility (visibility) of variables.
#### JavaScript has 3 types of scope:
* Block scope
* Function scope
* Global scope

#### Block Scope : keywords let and const provide Block Scope in JavaScript.
* variables declared inside a { } block cannot be accessed from outside the block:
```
{
  let x = 2;
}
// x can NOT be used here
```
* Variables declared with the var keyword can NOT have block scope.
* Variables declared inside a { } block can be accessed from outside the block.
```
{
  var x = 2;
}
// x CAN be used here
```
#### Local Scope : Variables declared within a JavaScript function, become LOCAL to the function.
```
// code here can NOT use carName
function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}
// code here can NOT use carName
```
#### Local variables have Function Scope: They can only be accessed from within the function.
 * Local variables are created when a function starts, and deleted when the function is completed.

### Function Scope:
* JavaScript has function scope: Each function creates a new scope.
* Variables defined inside a function are not accessible (visible) from outside the function.
* Variables declared with var, let and const are quite similar when declared inside a function. They all have Function Scope:



### having two variables at different scopes of the same name, that has a term, it's called shadowing.
### Variable Shadowing happens when a variable in an inner scope is declared with the same name as a variable in the outer scope. In this case, the variable in the inner scope shadows (masks) the variable in the outer 
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/39008554-5308-4690-8076-602bed7d7943)


#### that in a lexically scoped language which JavaScript is all of the scopes that we're dealing with, all of the lexical scopes and identifiers, that's all determined at compile time. It's not determined at run time. It is used at run time, but it is determined at compile time.

