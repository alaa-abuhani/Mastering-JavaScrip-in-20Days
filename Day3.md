1# basic-data-structures/copy-array-items-using-slice
```
function forecast(arr) {
  // Only change code below this line
arr=arr.slice(2,4)
  return arr;
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```
2#copy-an-array-with-the-spread-operator
```
function copyMachine(arr, num) {
  let newArr = [];
  while (num >= 1) {
    // Only change code below this line
newArr.push([...arr])
    // Only change code above this line
    num--;
  }
  return newArr;
}


console.log(copyMachine([true, false, true], 2));
```

3# profile-lookup
