
*ternary operator : Short Hand If...Else


 variable = (condition) ? expressionTrue :  expressionFalse;

*for/of - loops through the values of an iterable object
```
for (variable of iterable) {
  
}
```
```
const cars = ["BMW", "Volvo", "Mini"];
let text = "";
for (let x of cars) {
  text += x;
}
```

1# use-multiple-conditional-ternary-operators

```
function checkSign(num) {
 return (num > 0) ? "positive" : (num < 0) ? "negative" : "zero";
}

checkSign(10);
```
2# use-the-map-method-to-extract-data-from-an-array

```
// Only change code below this line
const ratings = watchList.map(s => ({
  title: s.Title,
  rating: s.imdbRating
}));
// Only change code above this line
```
3# use-the-filter-method-to-extract-data-from-an-array

```
const filteredList = watchList
.filter(s=> s.imdbRating >= 8.0)
.map(s => ({ title: s.Title, rating: s.imdbRating }));
// Only change code above this line
console.log(filteredList);
```
 4# golf-code

 ```
 const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

function golfScore(par, strokes) {
  // Only change code below this line
 if (strokes == 1) {
    return names[0];
  } else if (strokes <= par - 2) {
    return names[1];
  } else if (strokes === par - 1) {
    return names[2];
  } else if (strokes === par) {
    return names[3];
  } else if (strokes === par + 1) {
    return names[4];
  } else if (strokes === par + 2) {
    return names[5];
  } else {
    return names[6];
  }

  return "Change Me";
  // Only change code above this line
}
golfScore(5, 4);
```








