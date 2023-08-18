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
- no anything interesting in JavaScript
- trigger timer in browser control by setTimeout
  


![10](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/014f7b8c-0c49-4938-aedf-98371cbd762f)

- queue call :

![11](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/50bc9543-a3f6-453f-9837-aae1bfefe6f5)

```
   console.log('A');
      
    setTimeout(() => {
        console.log('B');
    }, 3000);
          
    console.log('C');
```
#### Output:
A 


C 


B
***
* When JS tries to execute the above program, it places the first statement in the call stack which gets executed and prints A in the console and it gets to pop out of the stack. Now, it places the second statement in the call stack and when it tries to execute the statement, it finds out that setTimeout() doesn’t belong to JS so it pops out the function and puts in the WebAPI to get executed there. Since the call stack is now again empty, it places the third statement in the stack and executes it thus printing C in the console.

* In the meanwhile, the WebAPI executes the timeout function and places the code in the callback queue. The event loop checks if the call stack is empty or not or whether there is any statement in the callback queue that needs to be executed all the time. As soon as the event loop checks that the call stack is empty and there is something in the callback queue that needs to be executed, it places the statement in the call stack and the call stack executes the statement and prints B in the console of the browser.

#### Callback Queue 
The Callback queue waits until the call stack is empty. Afterwards, the codes in it are executed in First In, First Out (FIFO) order. As more functions or codes are added to the callback queue, they stay at the back and wait for the ones in the front to leave the queue first.

#### Event Loop
This is a feature in JS which continuously checks if the main stack is empty. And when it is empty, it checks the Callback Queue. If there are codes in the queue to be executed, they are transferred one by one to the call stack. After the code is executed, it leaves the stack and the next one in the queue comes up until the queue is empty.

*good reference : (https://dillionmegida.com/p/callback-queue-and-event-loop/)

========================================================================================================
# promises

#### example one  of the entire map of asynchronicity in JavaScript.
![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/3eaad5b4-1a40-409d-a948-f86e5ea14cff)


#### example two  of the entire map of asynchronicity in JavaScript.
 ![image](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/618f6672-0d09-4647-b42f-b2d4bf0bed93)


![14](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/ce98cc6d-4449-4af9-a659-124c3b13fe85)

promise handel on Rejected


![15](https://github.com/alaa-abuhani/Mastering-JavaScript-in-20Days/assets/65255601/4bea1f40-8b4b-47f7-a7c9-a492c8b88109)



# Question 1:
You are given a function executeInSequenceWithCBs and some code. The task is to modify the executeInSequenceWithCBs function so that it runs and executes all the tasks inside the asyncTasks array.

The function should return an array of messages obtained from each task's execution.

You are only allowed to change the executeInSequenceWithCBs function or add new functions/code. You cannot modify the tasks' functions.
```


const executeInSequenceWithCBs = (tasks, callback) => {
    const messagesAarray=[]
    let count=0
    for (let i =0 ; i< tasks.length;i++){
        const task=tasks[i]
        task((message)=>{
            messagesAarray[i]=message
            count++
            if(count===tasks.length){
              callback(messagesAarray)
            }
        })
    }
}
```
# Question 2:
You are given a function called executeInParallelWithPromises, which takes an array of APIs (represented by objects).

Your task is to write code that fetches the data of each API in parallel using promises. In Parallel means that the api which resolves first, returns its value first, regardless of the execution order.

The output of the executeInParallelWithPromises function should be an array containing the results of each API's execution.

Each result should be an object with three keys: apiName, apiUrl, and apiData..

```
const executeInParallelWithPromises = async (apis) => {
        let final = await Promise.all(
        apis.map((api) =>
            fetch(api.apiUrl)
            .then((response) => response.json())
            .then((apiData) => ({
                apiName: api.apiName,
                apiUrl: api.apiUrl,
                apiData,
            }))
        )
        );
        console.log(final);
    };
    
    executeInParallelWithPromises(apis);
```
# Question 3:
You are given a function called executeInSequenceWithPromises, which takes an array of APIs (represented by objects).

Your task is to write code that fetches the data of each API sequentially (one after the other) using promises.

In Sequence means that the api which executes first, returns its value first.

The output of the executeInSequenceWithPromises function should be an array containing the results of each API's execution.

Each result should be an object with three keys: apiName, apiUrl, and apiData.

```
const executeInSequenceWithPromises = async (api) => {
  let final = []
  for (let i = 0; i < api.length; i++) {
    let apiResult = await fetch(api[i].apiUrl);
    let apiData = await apiResult.json();
    final.push({ apiName: api[i].apiName, apiUrl: api[i].apiUrl, apiData })
    
  }
    
    console.log(final)
};

```



