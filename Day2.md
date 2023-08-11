i learned about assignment statement and expression and operators and keyword let , const use to declare variables

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


