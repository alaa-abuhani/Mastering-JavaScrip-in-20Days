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


- The setTimeout() method calls a function after a number of milliseconds.
  1 second = 1000 milliseconds.


- setTimeout() is an asynchronous function, meaning that the timer function will not pause execution of other functions in the functions stack. In other words, you cannot use setTimeout() to create a "pause" before the next function in the function stack fires.

- trigger timer in browser 
  


![10](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/014f7b8c-0c49-4938-aedf-98371cbd762f)

- queu call :

![11](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/0a53643c-69c6-45cf-ac89-82fcdfdbe65e)
