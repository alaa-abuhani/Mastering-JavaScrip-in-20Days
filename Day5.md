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

