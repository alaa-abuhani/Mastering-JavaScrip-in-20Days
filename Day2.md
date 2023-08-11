i learned about assignment statement and expression and operators and keyword let , const use to declare variables

The Assignment Operator = assigns a value to a variable.

Arithmetic Operators are used to perform arithmetic on numbers

let : cannot be Redeclared ,  must be Declared before use , have Block Scope (function scope)

const : cannot be Redeclared ,  cannot be Reassigned , chave Block Scope (function scope)


QUESTION #1
Consider the following JavaScript code:

```
let a = 0;
let b = "0";
let c = false;
let d = "false";

console.log(a == b);
console.log(b === c);
console.log(!!d);

```
What will be the output of each console.log statement? You MUST explain WHY.

1-true : (==) compare value not  type

2-false : b and c dont have  same type & data type 

3-true : first it will cast string to true , ! make it false and !!make it true 

QUESTION #2:

Consider the following JavaScript expression:

```
console.log(4 + 5 * "7");
```
39 : priority do multipliaction & cast string to number then do addition

QUESTION #3:
Evaluate the following expression:
```
let result = 5 + 2 * 3 - 1;
```
10 : priority do multiplication then subtraction then addition
 
QUESTION #4:

Consider the following code:
```
let x = 10;
let y = '10';
console.log(x == y);
console.log(x === y);
```
 1- true : == compare the value only

 2- false : === compare the value  & type

QUESTION #5:
Given the code below:
```
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result);
```
true : (num > 10 && isPositive ) => true num cast to number  (  true  || false ) => true 

