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








