i learn :
* function with no  return value will return undefine
* syntax of Arrow function  it useful for simple  function
```
const square = (x) => x*x;  
```
* scope refers to the visibility of variables :

global scope : Variables which are defined outside of a function block have

function scope || narrower scope :Variables which are defined inside of a function block

* Variables declared with let can be modified from within a narrower scope
in this example the reference is only change
```
let feeling = "happy";

function myfeel() {
    feeling = "sad";
}
myfeel();
console.log(feeling);
```
* var and let can be-assignable 
* synatx of addEventListener , when the user clicks somewhere on the page, a click event is fired 

 ```
document.addEventListener("click", () => {
    console.log("clicked")
});
```

DELIVERABLES


1 # global-scope-and-functions

```
// Declare the myGlobal variable below this line
let  myGlobal = 10;


function fun1() {
  // Assign 5 to oopsGlobal here
  oopsGlobal = 5;

}

// Only change code above this line

function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}
```


2 # local-scope-and-functions
```
function myLocalScope() {
  // Only change code below this line
let myVar = 5 ;
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// Run and check the console
// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);
```

3 # global-vs--local-scope-in-functions
```// Setup
const outerWear = "T-Shirt";

function myOutfit() {
  // Only change code below this line
const outerWear = "sweater";
  // Only change code above this line
  return outerWear;
}

myOutfit();

```
4 # stand-in-line

```
function nextInLine(arr, item) {
  // Only change code below this line
  arr.push(item);
  console.log(arr + " mm");

  return arr.shift();
  // Only change code above this line
}

// Setup
let testArr = [1, 2, 3, 4, 5];

// Display code
console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));

```

