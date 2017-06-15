# Slasher Flick

### Problem Description

Return the remaining elements of an array after chopping off n elements from the head.

The head means the beginning of the array, or the zeroth index.

### Problem Script

```javascript
function slasher(arr, howMany) {
  // it doesn't always pay to be first
  return arr;
}

slasher([1, 2, 3], 2);
```

### Expected Outcome

* `slasher([1, 2, 3], 2)` should return `[3]`.
* `slasher([1, 2, 3], 0)` should return `[1, 2, 3]`.
* `slasher([1, 2, 3], 9)` should return `[]`.
* `slasher([1, 2, 3], 4)` should return `[]`.
* `slasher(["burgers", "fries", "shake"], 1)` should return `["fries", "shake"]`.
* `slasher([1, 2, "chicken", 3, "potatoes", "cheese", 4], 5)` should return `["cheese", 4]`.


### Solution Script

```javascript
function slasher(arr, howMany) {
  arr.splice(0, howMany);
  return arr;
}

slasher([1, 2, 3], 2);
```

### Solution Explanation

1. Given that the problem description is to always remove the elements from the head (zeroth index), we can pass the start argument as 0 into our `splice()` method
2. As we want to return only the remaining elements in the given array, we pass `howMany` as our second argument in the `splice()` method
3. After the `splice()` method is ran, `arr` is now updated with only the remaining elements.
4. Return `arr`

### Useful Links

* `Array.prototype.splice()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice?v=example)
