#### Lexical scoping : refers to when the location of a function's definition determines which variables you have access to.
( where variables and blocks of scope are authored)
What is author-time?
This is the time that when developer writes the code. This can be taken to mean, perception of program as you see it before compilation.

#### dynamic scoping : uses the location of the function's invocation to determine which variables are available.
(Dynamic scope does not concern itself with how and where functions and scopes are declared, but rather where they are called from. That means that, the scope chain is based on call-stack, not the nesting of scopes in code.)

example  when foo() is executed, theoretically the code below would result 3 as the output,
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/0885956f-7f8d-48b5-a1f8-5de3fe4b4c0d)
When foo() cannot resolve the variable reference for a, instead of stepping up the nested (lexical scope — we will mention soon) scope 

chain, it walks up the call-stack, to find where foo() was called from. Since foo() was called from bar() it checks the variables in scope

 for bar(), and finds an a there with value 3.

