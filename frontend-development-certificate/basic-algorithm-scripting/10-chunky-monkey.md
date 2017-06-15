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

1. Create an empty array `resultArray` to store the new splitted arrays in them
2. Create another number variable `positionInArray` that starts with 0 for our while loop
3. Step through the array `arr` while our `positionInArray` is less than the length of `arr`
4. While in the loop, we `slice()` our `arr` array with the number given, `size`
5. The first argument in our `slice()` method is where we begin our slice, second argument being the number of elements to return.
6. After the `arr` array is sliced, we use the `push()` method to add the sliced array into our `resultArray`
7. Finally, return the `resultArray`

### Useful Links

* `String.prototype.push()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push?v=example)
* `String.prototype.slice()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice?v=example)
