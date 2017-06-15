# Chunky Monkey

### Problem

Write a function that splits an array (first argument) into groups the length of `size` (second argument) and returns them as a two-dimensional array.

```javascript
function chunkArrayInGroups(arr, size) {
  // Break it up.
  return arr;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

### Expected Outcome

* `chunkArrayInGroups(["a", "b", "c", "d"], 2)` should return `[["a", "b"], ["c", "d"]]`.
* `chunkArrayInGroups([0, 1, 2, 3, 4, 5], 3)` should return `[[0, 1, 2], [3, 4, 5]]`.
* `chunkArrayInGroups([0, 1, 2, 3, 4, 5], 2)` should return `[[0, 1], [2, 3], [4, 5]]`.
* `chunkArrayInGroups([0, 1, 2, 3, 4, 5], 4)` should return `[[0, 1, 2, 3], [4, 5]]`.
* `chunkArrayInGroups([0, 1, 2, 3, 4, 5, 6], 3)` should return `[[0, 1, 2], [3, 4, 5], [6]]`.
* `chunkArrayInGroups([0, 1, 2, 3, 4, 5, 6, 7, 8], 4)` should return `[[0, 1, 2, 3], [4, 5, 6, 7], [8]]`.
* `chunkArrayInGroups([0, 1, 2, 3, 4, 5, 6, 7, 8], 2)` should return `[[0, 1], [2, 3], [4, 5], [6, 7], [8]]`.

### Solution Script

```javascript
function chunkArrayInGroups(arr, size) {
  var resultArray = [];
  var positionInArray = 0;

  while(positionInArray < arr.length) {
    resultArray.push(arr.slice(positionInArray, positionInArray += size));
  }
  
  return resultArray;  
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

### Solution Explanation

1. 