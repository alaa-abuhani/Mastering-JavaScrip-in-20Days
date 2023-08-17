### JavaScript is a single-threaded language, it is synchronous in nature
#### synchronous calls, all the work is done line by line i.e. the first task is executed then the second task is executed, no matter how much time one task will take.
#### This arises the problem of time wastage as well as resource wastage. These two problems are overcome by asynchronous calls, where one doesn’t wait for one call to complete instead it runs another task simultaneously.

-JS  have a :
- lexical environment, 
- syntax parser, 
- execution context (memory heap and call stack) that is used to execute the JS code


 this parts is not actually  part of JavaScript  but make it to do async call:

- making requests over the network like API calls, we use async calls.
- browsers also have Event Loops, Callback queue,
- WebAPIs that are also used to run the JS code
- DOM, AJAX, and Timeout are not actually part of JavaScript but part of RunTime Environment or browser

![9](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/735c9b3d-9c2a-4c29-9d57-c98393e89146)

