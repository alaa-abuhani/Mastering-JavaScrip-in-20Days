Closure (scope and execution context)

#### A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment).In other words, a closure gives you access to an outer function's scope from an inner function. 

*Execution Context :specification to track the runtime evaluation of code
 ![execution-context](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/bc9ca27a-c48c-4772-b1ee-d33c3ea50f40)

#### *Functions can be returned from other functions in JavaScript
![1](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/c4e4bffb-8e95-4980-9b5d-c2e8631723aa)

#### *Calling a function in the same function call as it was defined

![6](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/e7ffd35a-daa0-45fb-b396-372653e26dbd)

#### *Calling a function outside of the function call in which it was defined


![3](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/0c375734-aee6-41ea-8f85-9c0f03d8edc7)

**The backpack :

![8](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/84816bf0-2f1c-4758-9421-cded36367ccb)

Question 1:

Write a closure named createCounter that takes an initial value start and returns a function. The returned function, when invoked, should increment the counter by 1 and return the updated value.

```
function createCounter(start){

     let inaitail = start ;
     function increment(){ return inaitail++} 
     return increment
}
 let incremntCounter = createCounter(5);
 console.log(incremntCounter);
```


Question 2:
Write a closure named calculateAverage that takes an array of numbers, nums, and returns a function. The returned function, when invoked, should calculate and return the average of the numbers in the array.
```
 function calculateAverage(arr){
    let sum = 0;
    function average (){
       for(item of arr) {
        sum += item;
    }
    return sum/arr.length
  }
  return average
 }
 const averageArray = calculateAverage([1,2,3]);
 console.log(averageArray);

```
Question 3:
Write a closure named powerOf that takes a base number base and returns a function. The returned function, when invoked with an exponent exp, should calculate and return the result of base raised to the power of exp.

```
function powerOf(base) {

let baseNumber =  base ;
function eponent(exp){
  return Math.pow(base,exp)
}
return eponent
}
const y = powerOf(2);
console.log(y);
```
Question 4:
Write a closure named compose that takes multiple functions as arguments and returns a new function. The returned function should apply the provided functions in reverse order, passing the result of each function as an argument to the next function.

```

function compose(...functions){
   
    function applyFunctions(){

        return functions.reduceRight((funcResult, f) => f(funcResult), 0); // inatial = 0 
    }
 
}

```








