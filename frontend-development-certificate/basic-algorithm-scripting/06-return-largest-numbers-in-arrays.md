# Problem Script

```javascript
function largestOfFour(arr) {
  // You can do this!
  return arr;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

# Solution Script

```javascript
function largestOfFour(arr) {
  var result = [];
  arr.forEach(function(array) {
    result.push(array.sort(function(a, b) {
      return b - a;
    })[0]);
  });
  return result;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

# Explanation

1. Loop through each array
2. Sort the elements within each sub-array in a descending order
3. From the sort, return the first (highest) element
4. result.push the returned element into they array
5. Thus, returning an array of the highest element
