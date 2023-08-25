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



