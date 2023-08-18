#### Objects are variables too. But objects can contain many values.
#### Object values are written as name : value pairs (name and value separated by a colon)

#### Creating a JavaScript Object
- Create a single object, using an object literal.
```
let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```
- Create a single object, with the keyword new.
```
const person = new Object();
person.firstName = "John";
person.lastName = "Doe";
```

- Define an object constructor, and then create objects of the constructed type.
```
const o = new Object();
o.foo = 42;
console.log(o);// { foo: 42 }
```

- Create an object using Object.create()
```
const person = {
  isHuman: false,
}
const me = Object.create(person);
```
* this key word 
- When used in an object method, this refers to the object.
this refer to person 
```
const person = {
  firstName: "John",
  fullName : function() {
  return this.firstName ;
}
```





# link chalenges (https://www.freecodecamp.org/alaa-abuhani)


 
