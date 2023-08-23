
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

Any value's value-type can be inspected via the typeof operator, which always returns a string value representing the underlying JS value-type:

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

## NaN
- In JavaScript, NaN is short for "Not-a-Number".
- In JavaScript, NaN is a number that is not a legal number.
- The Global NaN property is the same as the Number.NaN property. 
```
var myNextAge = Number("39"); // 39 
var MycastAge = Number("n/a"); // NaN
myAge - "my son age"           // NaN
MycastAge === MycastAge // false

```


#### NaN it is not equal to itself,
#### Undefined is absolutely equal to itself
```
isNaN(myAge);           // false
isNaN(MycastAge);       // true
isNaN("my son age");    // true

```

#### NaN, it is a number, and it is the invalid number, and it is going to occur in your programs
#### the type of a NaN is number. It's just an invalid number.

### The Number() method converts a value to a number.
- If the value cannot be converted, NaN is returned.
##### Notes
- For booleans, Number() returns 0 or 1.
- For dates, Number() returns milliseconds since January 1, 1970 00:00:00.
- For strings, Number() returns a number or NaN.

* - isNaN() method returns true if a value is Not-a-Number. <=> isNaN() converts the value to a number before testing it.
* - Number.isNaN() returns true if a number is Not-a-Number.
- Example :

```
isNaN('Hello');  // This returns true;

Number.isNaN('Hello'); // This returns false; 

```
```
var MycastAge = Number("n/a");
Number.isNaN(MycastAge); // This returns  true; 

```
### Negative Zero
The -0 (Negative Zero) is essentially the zero value, but with the sign bit on. So it is the negative representation of a zero.

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/6f1b4cff-8643-4204-b11a-7b80684553b6)

* - toString() the -0 we got 0.

* - The triple equals operator ( === ) again lies to us, cuz it says the -0 is equal to a 0.

* - the < (less than sign) and the > (greater than sign) , also lie to us.

### The Object.is()
- * The Object.is() static method determines whether two values are the same value.
- * Object.is() is not equivalent to the == operator.
 The == operator applies various coercions to both sides (if they are not the same type) 
 before testing for equality (resulting in such behavior as "" == false being true),
 but Object.is() doesn't coerce either value.

- * Object.is() is also not equivalent to the === operator.
  The only difference between Object.is() and === is in their treatment of signed zeros and NaN values. The === operator 
 (and the == operator) treats the number values -0 and +0 as equal, but treats NaN as not equal to each other.

```

// Case 1: Evaluation result is the same as using ===
Object.is(25, 25); // true
Object.is("foo", "foo"); // true
Object.is("foo", "bar"); // false
Object.is(null, null); // true
Object.is(undefined, undefined); // true
Object.is(window, window); // true
Object.is([], []); // false
const foo = { a: 1 };
const bar = { a: 1 };
const sameFoo = foo;
Object.is(foo, foo); // true
Object.is(foo, bar); // false
Object.is(foo, sameFoo); // true

// Case 2: Signed zero
Object.is(0, -0); // false
Object.is(+0, -0); // false
Object.is(-0, -0); // true

// Case 3: NaN
Object.is(NaN, 0 / 0); // true
Object.is(NaN, Number.NaN); // true
```

### The Math.sign() : method retuns whether a number is negative, positive or zero.
* - If the number is positive, this method returns 1.
* - If the number is negative, it returns -1.
* - If the number is zero, it returns 0.
* - If the number is negative zero, it returns -0
* - If the number is not a number, it returns NaN
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/5cc3b2da-034a-4ccb-a3f9-641c045017b5)

### Fundamental Objects
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/57a3cac0-1fd9-49b4-abb3-17822f0fd859)
====================================================================================================
#### in JavaScript, we refer to type conversion as coercion. 

- * The first abstract operation that we have is called ToPrimitive. if we don't have a primitive, we need to turn it into a primitive. So if we have something non-primitive, like one of the object types, like an object, an array, a function, whatever, and we need to make it into a primitive, this is the abstract operation that's going to be involved in doing that.

## toString abstract operation
toString() :
- * method returns a string as a string.
- * method does not change the original string.
- * method can be used to convert a string object into a string.

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/6c816c8e-ce71-40d5-87d1-257b80a23848)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/ac789c7a-f0fd-4e2a-b8df-a57cf751e2b8)
```
const arr = [1, 2, 3];

arr.toString(); // "1,2,3"
```

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/d6a768e2-2bb9-428d-b2df-228923ebb089)
## toNumber()
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/5e098df7-3419-4355-ba5c-6e12753a404c)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/0760a2ee-d5c7-4e7d-96bc-d106dee2c7e3)

undefine , null convert to empty string convert to zero

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/a90c027a-ba63-49e9-8767-936a74ee33ac)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/208dbbb4-ff78-411e-b594-b43de4d38e49)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/3090c2da-5ed8-473c-88db-ccf8fc211455)




## toBoolean()

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/8cbb3547-54f8-469c-8277-5bbded5e11d4)




### boxing : form of implicit coercion 

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/b06b55ea-b2e5-4e83-b68f-2b2c8c1bc991)

* - that things can behave as objects, but that doesn't make them an object. This is not an object. It is a primitive string that has an optimization in it where you can access a property as if it was an object.

### corner cases of coercion :
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/6a3d7f5e-0ed7-428e-a1f1-00fc0d8c3549)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/9d87c7c2-798a-46ca-8718-03b5b095c00c)

![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/3d17ef13-e056-47aa-8217-02f22db22874)


Question 1:
Write a function called convertStringToNumber that converts a string to a number using the unary plus operator.

If the input is not a string, return an object of the input's value and type.
```
function convertStringToNumber(input) {
    if ((typeof input) === "string")
     return +input;
    else
   return {valueIs : input , typeIs : typeof input} ;
  //write your own code here
}
console.log(convertStringToNumber("15"));
console.log(convertStringToNumber([1 , 2]));
console.log(convertStringToNumber(true));
```

Question 2:
Write a function called checkNaN that takes a single argument and returns true if the argument is NaN and false otherwise.

```
const checkNaN = (value) => {
   return  isNaN(value)
  //write your own code here
}
console.log(checkNaN("ala"));
```




         

         







