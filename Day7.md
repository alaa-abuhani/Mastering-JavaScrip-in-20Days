
##### JavaScript is synchronous, blocking and single-threaded. This means that the JavaScript engine executes our program sequentially,one line at a time from top to bottom in the exact order of the statements


##### Call stack: The call stack is a part of the JavaScript engine that helps keep track of function calls. When a function gets invoked, it is pushed to the call stack where its execution begins, and when the execution is complete, the function gets popped off the call stack. It uses the concept of stacks in data structures that follows the Last-In-First-Out (LIFO) principle.

#####  execution contexts : Created to run the code of a function  has 2 parts: 
- Thread of execution
- Memory

##### A callback : 
-is a function passed as an argument to another function. 

-This technique allows a function to call another function

-can run after another function has finished

// A callback function can run after another function has finished
Callbacks are the functions that are slipped or passed into another function to decide the invocation of that function. 

##### Higher Order Function :The outer function that takes in a function 
//The functions that take a function as an argument, or return a function as a return value, are called higher order functions.

 1 # use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem
```
const squareList = arr => {
  // Only change code below this line
return arr.filter(item => item > 0 && (item % 2 === 0|| item % 2 === 1)).map(item => item*item);
  // Only change code above this line
};

const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]);
console.log(squaredIntegers);
```
2 # apply-functional-programming-to-convert-strings-to-url-slugs
```
// Only change code below this line
function urlSlug(title) {

return (title.toLowerCase().split(" ").filter(item => item !== "").join("-"));
}
// Only change code above this line
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");
```
3 #
- Question 1: Functions and Callbacks
Implement a JavaScript function called mapAsync that takes an array and a callback function. The function should map each element of the array to a new value using the callback function asynchronously.
The final result should be returned as a Promise.
```
function mapAsync(array, newArrayFunction) {
  return  new  Promise(function (resolve) {
    let newArray = [];

    for (x of array) {
        newArray.push(newArrayFunction(x))
    }
    resolve(newArray);
  });
}

function newArrayFunction(item) {
  return item / 5;
}
const mapAsyncPromis =   mapAsync([10, 20, 30, 40 , 50], newArrayFunction);
mapAsyncPromis.then(
  (resolve) => {
    console.log(resolve);
  },
);
</script>
```
- Question 2: Call Stack and Recursion

Write a JavaScript function called sumRange that calculates the sum of all integers in a given range. The function should use recursion to handle the calculation and demonstrate understanding of the call stack.
```
 function sumRange(start, end) {
        if(start == end) 
        return start
        else
        return start + sumRange(start +1 , end )
    }
    console.log(sumRange(1,5));
```





