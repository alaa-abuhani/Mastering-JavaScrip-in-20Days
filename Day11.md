
### In JavaScript, variables don't have types, values do 
#### Value Types

JS doesn't apply types to variables or properties -- what I call, "container types" -- but rather, values themselves have types -- what I call, "value types".
primitive (non-object) value types:
- undefined
- null
- boolean
- number
- bigint
- symbol
- string

object :
- object 
- array subtype of object

#### The typeof Operator
##### You can use the typeof operator to find the data type of a JavaScript variable.
```
typeof "John"                 // Returns "string"
typeof 3.14                   // Returns "number"
typeof NaN                    // Returns "number"
typeof false                  // Returns "boolean"
typeof [1,2,3,4]              // Returns "object"
typeof {name:'John', age:34}  // Returns "object"
typeof new Date()             // Returns "object"
typeof function () {}         // Returns "function"
typeof myCar                  // Returns "undefined" *
typeof null                   // Returns "object"

```
```
typeof {name:'John', age:34} // Returns "object"
typeof [1,2,3,4]             // Returns "object" (not "array")
typeof null                  // Returns "object"
typeof function myFunc(){}   // Returns "function"
```
##### The typeof operator returns "object" for arrays because in JavaScript arrays are objects.

- you can check if the object is an Array function:
```
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = isArray(fruits);

function isArray(myArray) {
  return myArray.constructor === Array;
}
```
## Undefined vs Undeclared 
* Undefined variable means a variable has been declared but does not have a value.

* Undeclared variable means that the variable does not exist in the program at all.

#### NaN it is not equal to itself,
#### Undefined is absolutely equal to itself



